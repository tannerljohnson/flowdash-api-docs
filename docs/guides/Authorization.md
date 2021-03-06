---
tags: [Task]
---

# Authorization

The Task API supports two authorization methods: (i) an incoming webhook URL, or (ii) an API  token embedded in the Authorization header. You can get your workflow's webhook URL and API token from the **Settings > API** page.

![](../../assets/images/task_api-authorization.png)

## Incoming Webhook URL

The simplest way to integrate is using the workflow's unique incoming webhook URL. You can use the webhook URL to create new tasks or update existing tasks, but you won't be able to read tasks. An example URL might look like:

```
https://app.flowdash.com/api/v1/workflows/JFBhoD1ZaaTWeBbkFqXQ8qkA/tasks
```

## API Token

For additional security, you can choose to use our API token authorization method. In addition to creating and updating tasks, using this authorization method also allows you to read tasks. Instead of posting to your workflow's unique incoming webhook URL, you would instead POST to:

```
https://app.flowdash.com/api/v1/tasks
```

And specify the access token in your headers (don't forget the "Bearer"):

```
Authorization: Bearer YOUR_API_TOKEN
```