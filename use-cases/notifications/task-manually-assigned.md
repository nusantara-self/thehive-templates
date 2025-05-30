---
title: Task Manually Assigned
tags: [notification]
description: >
  Triggers when a Task is manually assigned to a user. 
  Does not trigger when a Task is automatically assigned by the user saving the first Task log.
author: Fabien Bloume, StrangeBee
---

# Task Manually Assigned

**Trigger Condition:**  
This notification is triggered when a Task is manually assigned to a user.  
It **does not** trigger if the assignment happens as a side effect when the user saves the first Task log in a Task.

**Notes:**  
- Useful for team workload notifications or alerting when responsibilities shift.
- May be combined with other filters for more granular workflows.

---

## TheHive Notification Filter

```json
{
    "_and": [
        { "_is": { "action": "update" } },
        { "_is": { "objectType": "Task" } },
        { "_contains": { "details.assignee": "" } }
    ]
}
```
