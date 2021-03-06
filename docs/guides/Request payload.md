---
tags: [Task]
---

# Request payload

When the specified action is performed, Flowdash will call your application at the URL provided and the request body will include the name of the action as well as a JSON representation of the task. Following the example from above, the request body would look like:

```json
{
  "action": "Finish"
  "task": {
    "Stage": "Completed",
    "Assigned To": "user@example.com",
    "Company ID": "42",
    "Company Name": "Acme Corp",
    "Number of Employees": "20",
    "Contract Value": "10000",
    "International?": false,
    "Expected Close Date": "2020-01-31"
  }
}
```