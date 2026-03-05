---
title: Orchestra Workflow
description: Use when a user starts their line with '/orch' (but not: '/orch status')
---

# Orchestra Workflow
When the user starts a line with /orch, they want to create an artifact (blog posts, tweets, videos, research flows, ...) using a deterministic execution plan and the available skills in this repository.

Plans are explained in detail in markdown files in the `blueprints` folder. 

The `blueprint-index.md` provides an index of the available blueprints.

## Normal run
Primary usage example

```
/orch <brief>
```

The brief will explain the requested artifact, topic and/or additional instructions.

First, find all blueprints in the index that would generate the reqested artifact.
  - if there are no matches, the run terminates. Let the user know you found no matching blueprints in the repo
  - if there are multiple matches, ask the user to pick the best one
  
Then, locate the full blueprint and run through the steps to create the user's artifact.


Example:
```
/orch Create a tweet about plant based protein
/orch Create a blog post about building software, the LEAN way. Target audience: 19 year old college grads. Primary language: English. Keep it light, no emoticons or bullet points.
```



### System instructions

ALWAYS: in the first reply, tell the user you are using a blueprint and identify by blueprint title and filename.

ALWAYS: All output should be placed in a subfolder of the `./output` folder.





## Abort
```
/orch abort
```
Stop the currently executing blueprint