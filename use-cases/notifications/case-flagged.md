---
title: Flagged Case
tags: [notification]
description: >
  Triggers when a case is flagged.
  Useful to create an unambiguous notification when used consistently for a single purpose.
author: Fabien Bloume, StrangeBee
---

# Flagged Case

**Trigger Condition:**  
This notification is triggered when a Case is flagged (meaning the `flag` property is updated to `true`).

**Notes:**  
- Most effective when the flag is reserved and used *only* for a specific process/purpose, such has an out of SLA case.
- Generates only one notification per case as long as the flag remains set.

---

## TheHive Notification Filter

```json
{
    "_and": [
        {
            "_is": {
                "action": "update"
            }
        },
        {
            "_is": {
                "objectType": "Case"
            }
        },
        {
            "_is": {
                "details.flag": true
            }
        }
    ]
}
```
