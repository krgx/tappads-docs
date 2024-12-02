# SDK Integration Guide

## Step 1: Add SDK to Your Project

Insert the following script into the `<head>` of your page:

```html
<script src="https://sdk.tappads.io/pub/sdk_v1.js"></script>
```

## Step 2: Initialize SDK

```javascript
TappAdsPubSdk.init('your_api_key', { debug: true })
  .then(() => console.log('SDK Initialized'))
  .catch(err => console.error('Initialization Error:', err));
```

## Step 3: Fetch Tasks

```javascript
TappAdsPubSdk.getFeed()
  .then(feed => console.log('Feed:', feed))
  .catch(err => console.error('Error fetching feed:', err));
```

## Step 4: Start a Task

```javascript
TappAdsPubSdk.taskStart(taskId)
  .then(() => console.log('Task started:', taskId))
  .catch(err => console.error('Error starting task:', err));
```

## Step 5: Check Task Statuses

```javascript
TappAdsPubSdk.getTaskStatus([taskId1, taskId2])
  .then(statuses => console.log('Task statuses:', statuses))
  .catch(err => console.error('Error fetching statuses:', err));
```

For more details, [visit the server-to-server guide](server_to_server.md).