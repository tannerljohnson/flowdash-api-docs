# Introduction

The Flowdash API makes it easy to seamlessly add tasks to Flowdash and to wire up actions within Flowdash back to your application. These docs will walk through the process of setting up an integration.

For the examples below, we'll use a flow with the following fields configured:

![](../../assets/images/sample-custom-fields.png)

## Task API
Flowdash's Task API makes it easy to create new tasks and update existing tasks programmatically.

## Actions
While the Task API makes it easy to get data into Flowdash, Actions make it easy to get data out of Flowdash and back into your application via a RESTful API. All you need to do is specify a URL to call and any relevant headers, and Flowdash will call your API every time a user performs the specified action.
