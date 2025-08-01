---
date: 1726442821.539151
tags:
- autogenerated
- source__oai
- conversation_id__66e757d1-0534-8008-bb6a-afa8342b5ee2
- msg_e16238ce-ac04-4400-89bf-6b6a0efaa34d
- msg_aaa2c71e-7b37-4227-98d7-f5d25151a832
- msg_ae107622-3d0b-4952-b410-9bc678c0724f
- colorclass/decision-making-processes
title: assignment non-trivial agent chaining
---

**ASSISTANT**

:
- **Time management**: The **Strategist Agent** could include time estimates for each task, helping to manage deadlines.
- **Task dependencies**: The strategist could handle more complex workflows, where certain tasks depend on the completion of others.
- **Dynamic strategy adjustment**: The strategist could modify the plan in real-time based on agent feedback, adapting the strategy if problems arise.

---

### **Learning Outcomes**:

1. **Task Breakdown and Planning**: Students learn how to break complex tasks into smaller steps and delegate them to appropriate agents.
   
2. **Workflow Coordination**: The **Strategist Agent** shows how to manage workflows involving multiple agents, ensuring each agent performs the right task at the right time.
   
3. **Modularity**: The pattern demonstrates how to build modular systems where specialized agents can focus on specific tasks while the strategist coordinates the overall process.

4. **Adaptability**: The **Strategist Agent** can adjust its plan based on agent feedback or changing requirements, ensuring flexibility in multi-agent systems.

---

### **Assignment Extension Ideas**:

1. **Complex Workflows**: Implement more complex strategies where multiple agents need to collaborate on multi-step tasks that have dependencies between them.
   
2. **User Feedback Integration**: Allow the user to modify the strategy by adding or removing steps dynamically, creating an interactive strategy development process.
   
3. **Task Prioritization**: The strategist could prioritize tasks based on user preferences (e.g., focusing more on accuracy or style), adjusting the plan accordingly.

---

### **Summary**:

In this assignment, students implement the **Strategist Agent** pattern, where the agent is responsible for creating a plan to achieve complex tasks and delegating those tasks to other specialized agents. By managing multi-step workflows, the **Strategist Agent** ensures efficiency, task prioritization, and smooth collaboration between agents. This pattern helps students understand how to organize and coordinate multi-agent systems to solve complex problems.


**USER**

assignment: non-trivial agent chaining


**ASSISTANT**

### **Assignment: Non-Trivial Agent Chaining**

In this assignment, students will learn how to implement **non-trivial agent chaining**, a pattern where multiple agents work together in a sequence, each building on the output of the previous agent. Unlike simple task delegation, **non-trivial chaining** involves agents that contribute meaningfully to the overall process by refining, transforming, or augmenting the data at each step. This allows for more complex workflows where multiple agents collaborate dynamically.

### **Objective**:
1. Teach students how to implement **non-trivial chaining** of agents, where each agent in the chain transforms or adds value to the output from the previous agent.
2. Demonstrate how chaining can handle complex, multi-step tasks that require collaboration between specialized agents.
3. Explore strategies for managing dependencies and interactions between agents in a chained workflow.

---

### **What Is Non-Trivial Agent Chaining?**

In **non-trivial agent chaining**, multiple agents interact in a predefined sequence, each contributing unique expertise. The output of one agent becomes the input for the next agent, but unlike simple task delegation, each agent in the chain adds significant value by modifying or transforming the data.

#### **Key Characteristics**:
- **Sequential Processing**: Agents perform tasks in a specific order, with each agent processing the output from the previous agent.
- **Transformation**: Agents do more than just pass along data; they transform it by refining, analyzing, or expanding it.
- **Collaboration**: Agents need to work together on multi-step tasks where each step adds a non-trivial contribution to the final output.

#### **Use Cases**:
- **Document Generation**: A research agent gathers information, a writing agent produces a draft, an editor refines the draft, and a critic evaluates the quality.
- **Creative Writing**: A story generation agent creates the basic plot, a character development agent deepens character profiles, and a dialogue agent writes compelling conversations between characters.
- **Data Transformation**: A data extraction agent pulls data from a source, a formatting agent structures the data, and a visualization agent creates charts or graphs.

---

### **Step 1: Defining a Complex Task for Agent Chaining**

Let’s create a **document creation pipeline** where different agents contribute to generating, refining, and evaluating a document in multiple stages.

#### **Example Task**:
We want to create a **research report on climate change** with the following steps:
1. **Research Agent**: Gathers facts and data related to climate change.
2. **Writing Agent**: Uses the research to draft a structured report.
3. **Editor Agent**: Edits the report for clarity and coherence.
4. **Fact-Checker Agent**: Verifies the accuracy of the information in the report.
5. **Critic Agent**: Evaluates the overall quality of the report and suggests improvements.

This multi-step process will be implemented using **non-trivial agent chaining**, where each agent adds value at every step.

---

### **Step 2: Implementing the Agents for Chaining**

First, we’ll define the specialized agents needed for the document generation process. Each agent will have a specific role in the chain, with the output of one agent becoming the input for the next.

```python
class Agent:
    def __init__(self, name, system_prompt_template):
        self.name = name
        self.system_prompt_template = system_prompt_template
        self.history = []  # Initialize conversation history
    
    def get_system_prompt(self):
        """
        Render the system prompt based on the agent's name and role.
        """
        template = Template(self.system_prompt_template)
        return template.render(name=self.name)
    
    def query_openai(self, user_input, max_tokens=100, temperature=0.7, top_p=1.0, **kwargs):
        """
        Send the conversation history to OpenAI and maintain the chat log.
        """
        self.history.append({"role": "user", "content": user_input})
        response = openai.ChatCompletion.create(
            model="gpt-3.5-turbo",  # Using a chat model that supports roles
            messages=self.history,
            max_tokens=max_tokens,
            temperature=temperature,
            top_p=top_p,
            **kwargs
        )
        assistant_reply = response.choices[0].message["content"]
        self.history.append({"role": "assistant", "content": assistant_reply})
        return assistant_reply
```

#### **Defining the Specialized Agents**:

```python
# Define system prompts for each agent
research_prompt = "You are a research assistant. Gather detailed facts and data about the topic."
writing_prompt = "You are a writing assistant. Draft a structured report based on the research."
editor_prompt = "You are an editor. Review the draft for clarity and coherence."
fact_checker_prompt = "You are a fact-checker. Verify the accuracy of the information in the report."
critic_prompt = "You are a critic. Provide feedback on the quality of the report and suggest improvements."

# Create instances of each agent
research_agent = Agent(name="ResearchAgent", system_prompt_template=research_prompt)
writing_agent = Agent(name="WritingAgent", system_prompt_template=writing_prompt)
editor_agent = Agent(name="EditorAgent", system_prompt_template=editor_prompt)
fact_checker_agent = Agent(name="FactCheckerAgent", system_prompt_template=fact_checker_prompt)
critic_agent = Agent(name="CriticAgent", system_prompt_template=critic_prompt)

# Create a dictionary to hold all the agents
agents = {
    "ResearchAgent": research_agent,
    "WritingAgent": writing_agent,
    "EditorAgent": editor_agent,
    "FactCheckerAgent": fact_checker_agent,
    "CriticAgent": critic_agent
}
```

---

### **Step 3: Implementing the Agent Chaining Process**

Now, let’s define the **ChainedProcessManager**, which will be responsible for chaining the agents together. Each agent in the chain will contribute to refining or transforming the output of the previous agent.

#### **ChainedProcessManager Implementation**:

```python
class ChainedProcessManager:
    def __init__(self, agents):
        """
        Initialize the Chained Process Manager with the set of agents.
        
        Arguments:
        - agents: A dictionary mapping agent names to Agent objects.
        """
        self.agents = agents

    def execute_chain(self, user_input):
        """
        Execute the agent chain, with each agent contributing to the task.
        
        Arguments:
        - user_input: The original request from the user.
        
        Returns:
        - The final output after all agents in the chain have contributed.
        """
        # Step 1: Research Agent gathers facts and data
        print("Researching topic using Research Agent...")
        research_output = self.agents["ResearchAgent"].query_openai(user_input)
        
        # Step 2: Writing Agent drafts the report based on research
        print("Drafting report using Writing Agent...")
        draft_output = self.agents["WritingAgent"].query_openai(research_output)
        
        # Step 3: Editor Agent reviews the draft for clarity
        print("Editing draft using Editor Agent...")
        edited_output = self.agents["EditorAgent"].query_openai(draft_output)
        
        # Step 4: Fact-Checker Agent verifies the information
        print("Fact-checking report using Fact-Checker Agent...")
        fact_checked_output = self.agents["FactCheckerAgent"].query_openai(edited_output)
        
        # Step 5: Critic Agent provides feedback and suggestions
        print("Providing feedback using Critic Agent...")
        final_feedback = self.agents["CriticAgent"].query_openai(fact_checked_output)
        
        # Return the final fact-checked and critiqued report
        return {
            "research_output": research_output,
            "draft_output": draft_output,
            "edited_output": edited_output,
            "fact_checked_output": fact_checked_output,
            "final_feedback": final_feedback
        }
```

---

### **Step 4: Creating the CLI for Agent Chaining**

We’ll now build a simple CLI interface to interact with the **ChainedProcessManager**. The user will input a task (e.g., generating a research report), and the process manager will chain the agents together to produce the final output.

```python
def chained_process_cli():
    print("Welcome to the Chained Agent System!\n")
    
    while True:
        user_input = input("Enter a topic for the research report (type 'exit' to quit): ")
        
        if user_input.lower() == "exit":
            break
        
        # Execute the chain of agents
        final_output = chained_process_manager.execute_chain(user_input)
        
        # Print the final outputs
        print("\nFinal Report Output:")
        print(f"Research Output: {final_output['research_output']}")
        print(f"Draft Output: {final_output['draft_output']}")
        print(f"Edited Report: {final_output['edited_output']}")
        print(f"Fact-Checked Report: {final_output['fact_checked_output']}")
        print(f"Critic's Feedback: {final_output['final_feedback']}")

# Create an instance of the ChainedProcessManager and run the CLI
chained_process_manager = ChainedProcessManager(agents=agents)

if __name__ == "__main__":
    chained_process_cli()
```

---

### **Step 5: Running the Chained Agent System**

When the user provides a task (e.g., writing a report on a specific topic), the **Chained Process Manager** will delegate the task to each agent in the chain. Each agent will contribute uniquely by refining or transforming the output.

#### **Example Interaction**:

```bash
Enter a topic for the research report (type 'exit' to quit): The impact of climate change on polar ice caps.
Researching topic using Research Agent...
Drafting report using Writing Agent...
Editing draft


---

preceding: [[assignment implementing the strategist agent pattern]]  


following: [[ensemble voting pattern]]