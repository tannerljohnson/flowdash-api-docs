---
tags: [Task]
---

# Creating a new action

While the Task API makes it easy to get data into Flowdash, Actions make it easy to get data out of Flowdash and back into your application via a RESTful API. All you need to do is specify a URL to call and any relevant headers, and Flowdash will call your API every time a user performs the specified action.

1. First, open the Flow Builder:

![](../../assets/images/actions-create_new_1.png)

2. Next, create a new action, or select an existing action from the canvas. In the screenshot below, **Start** and **Finish** are existing actions:

![](../../assets/images/actions-create_new_2.png)

3. In the left sidebar, click the **+ New Step** button and select **API Call** from the dropdown:

![](../../assets/images/actions-create_new_3.png)

4. In the modal that opens, you can specify the URL of your API endpoint as well as any additional headers (for example, authorization headers):

![](../../assets/images/actions-create_new_4.png)

5. Once you're done, click **Apply**, then click **Save** in the left sidebar to commit your changes.

![](../../assets/images/actions-create_new_5.png)