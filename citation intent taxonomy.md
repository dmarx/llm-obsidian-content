---
date: '2024-11-28T19:46:29.411519Z'
tags:
- autogenerated
- source__claude
- conversation_id__3cd80afe-4f42-4110-a989-afd7d7eaaf33
- msg_e78175a0-d568-4bed-99f2-72f54d23b4b6
- msg_11625774-067f-4838-9465-b55309467b7d
- colorclass/research-knowledge-graph-schema
title: citation intent taxonomy
---

**USER**

elaborate on the notion of "citation intents"


**ASSISTANT**

# Citation Intent Taxonomy

## Core Intent Categories
```
Citation_Intent = {
  background: {
    type: "Uses",  // References prior work/concepts
    subtypes: ["Definition", "Problem_Statement"]
  },
  method: {
    type: "Builds_On",  // Extends/modifies prior work
    subtypes: ["Uses_Method", "Adapts_Method"]
  },
  result: {
    type: "Compares",  // Empirical comparison
    subtypes: ["Outperforms", "Validates", "Contradicts"]
  },
  motivation: {
    type: "Identifies_Gap", // Problem statements
    subtypes: ["Limitation", "Open_Question"]
  }
}
```

## Example from ML Literature
```
Paper: "Vision Transformer"
Citations: {
  "Attention Is All You Need": {
    intent: "method.Uses_Method",
    context: "We adapt the Transformer architecture..."
  },
  "ResNet": {
    intent: "result.Outperforms",
    context: "ViT achieves 88.5% accuracy compared to ResNet's 85.8%"
  },
  "CNN Inductive Bias": {
    intent: "motivation.Limitation",
    context: "CNNs have inherent limitations due to local receptive fields"
  }
}
```

This system enables analyzing research lineage but lacks granularity for tracking specific claims or theoretical developments.


---

preceding: [[tell me more about the claim tracking in semantic scholar]]