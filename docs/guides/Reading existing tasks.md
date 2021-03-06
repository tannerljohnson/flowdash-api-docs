---
tags: [Task]
---

# Reading existing tasks

*Note: this method is only available if you're using the API token authorization method.*

To fetch existing tasks from a workflow, simply issue a GET request to the tasks endpoint:

```
https://app.flowdash.com/api/v1/tasks
```

With the workflow's API token included in the Authorization header:

```json
Authorization: Bearer YOUR_API_TOKEN
```

An sample response might look like:

```json
[
    {
        "Stage": "In Progress",
        "Assigned To": null,
        "Task URL": "https://app.flowdash.com/workflows/2ylSaZ/tasks/ooCwnZ",
        "Company ID": "42",
        "Company Name": "Acme Corp",
        "Number of Employees": "10",
        "Contract Value": "10000.00",
        "Expected Close Date": "2020-01-31",
        "International?": false
    },
    {
        "Stage": "Not Started",
        "Assigned To": null,
        "Task URL": "https://app.flowdash.com/workflows/2ylSaZ/tasks/gqCQRO",
        "Company ID": "43",
        "Company Name": "XYZ Inc.",
        "Number of Employees": "300",
        "Contract Value": "500000.00",
        "Expected Close Date": "2020-03-31",
        "International?": true
    }
]
```

## Filters

You can also filter tasks based on their stage, who they're assigned to, or any other field. For example, let's say I wanted to fetch all tasks that are unassigned and in the Not Started stage:

```
https://app.flowdash.com/api/v1/tasks?Assigned%20To=&Stage=Not%20Started
```

Following from our example above, this would return:

```json
[
    {
        "Stage": "Not Started",
        "Assigned To": null,
        "Task URL": "https://app.flowdash.com/workflows/2ylSaZ/tasks/ooCwnZ",
        "Company ID": "43",
        "Company Name": "XYZ Inc.",
        "Number of Employees": "300",
        "Contract Value": "500000.00",
        "Expected Close Date": "2020-03-31",
        "International?": true
    }
]
```

Similarly, I can fetch all tasks that are In Progress and have a Company ID of 42:

```
https://app.flowdash.com/api/v1/tasks?Stage=In%20Progress&Company%20ID=42
```

This would return:

```json
[
    {
        "Stage": "In Progress",
        "Assigned To": null,
        "Task URL": "https://app.flowdash.com/workflows/2ylSaZ/tasks/ooCwnZ",
        "Company ID": "42",
        "Company Name": "Acme Corp",
        "Number of Employees": "10",
        "Contract Value": "10000.00",
        "Expected Close Date": "2020-01-31",
        "International?": false
    }
]
```