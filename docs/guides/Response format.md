---
tags: [Task]
---

# Response format

If your application responds with a 2xx code, Flowdash will interpret the API call as successful and move on to the next step in the action. If your application responds with a non-2xx code, Flowdash will abort the action on the current step and alert the user that an error has occurred.

In addition to being able to indicate success/failure, you can also modify the task in your response in the success case. For example, if we wanted to update the Expected Close Date, you could include the following in the response payload.

```json
{
  "task": {
    "Expected Close Date": "2020-02-01"
  }
}
```