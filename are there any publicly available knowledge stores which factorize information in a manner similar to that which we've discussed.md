---
date: '2024-11-28T19:28:40.489099Z'
tags:
- autogenerated
- source__claude
- conversation_id__3cd80afe-4f42-4110-a989-afd7d7eaaf33
- msg_8e558f48-f8fa-4b62-a5c1-21f729da9eb6
- msg_6aab957b-7b27-4a14-aab4-a0a6708e4430
- colorclass/research-knowledge-graph-schema
title: are there any publicly available knowledge stores which factorize information
  in a manner similar to that which we've discussed
---

**USER**

are there any publicly available knowledge stores which factorize information in a manner similar to that which we've discussed?


**ASSISTANT**

Several existing knowledge bases share aspects of our proposed approach:

1. [[Semantic Scholar]] organizes claims and citations in research papers, tracking influence through citation graphs. However, it lacks:
- Granular claim decomposition
- Explicit theoretical/empirical relationships
- Benchmark reliability tracking

2. [[Papers with Code]] maintains:
- Benchmark leaderboards
- Implementation links
- Model comparisons
But misses:
- Theoretical foundations
- Claim decomposition
- Reliability propagation

3. [[Stanford DAWN]] project's [[ML Metadata]] system tracks:
- Training runs
- Hyperparameters
- Hardware configurations
But lacks:
- Theoretical connections
- Claim validation
- Cross-paper relationships

4. [[OpenReview]]'s knowledge graph contains:
- Paper relationships
- Review comments
- Community discussion
Missing:
- Atomic knowledge units
- Formal reliability tracking
- Benchmark dependencies

No existing system fully implements the granular claim tracking and reliability propagation we've discussed.


---

preceding: [[let's marry empirical and theoretical claims into a unified schema. my main interest here is in tracking the state of the art with respect to actionable recommendations for training, and our current t]]  


following: [[tell me more about the claim tracking in semantic scholar]]