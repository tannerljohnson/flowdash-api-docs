---
tags: [Task]
---

# Updating an existing task

If your workflow includes a Unique ID field, you can use the Flowdash API to update an existing task in addition to creating new tasks. Simply include the unique id field in your request body and Flowdash will update the existing task instead of creating a new one. If no existing task with the specified unique id is found, a new task will be created.

For example, if we'd like to update the Number of Employees in the example above from 10 to 20, we can issue a POST request to the same endpoint with the following request body:

```json
{
  "Company ID": "42",
  "Number of Employees": "20"
}
```

You can also update the built-in Stage and Assigned To fields:

```json
{
  "Company ID": "42",
  "Assigned To": "user@example.com",
  "Stage": "In Progress"
}
```

Similar to creating a task, a response code of 2xx indicates success and the response will include all fields of the given task. A 422 response indicates invalid data and the response body will provide more details about the specific error.

## POST vs. PUT

You can update existing tasks with either an HTTP POST or PUT, with one subtle difference.

In our tasks API, POST follows *upsert* semantics. That means that if a task with the specified unique id already exists, it will update that task. However, if the task does not exist, it will create a new one.

On the other hand, PUT follows *update* semantics. That means that, like POST, if a task with the specified unique id already exists, it will update that task. However, if the task does not exist, the request will fail and the API will return a 404.
