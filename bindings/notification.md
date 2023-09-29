---
description: Information about the notification binding
---

# Notification

## post

```javascript
notification.post(notification.success, "This is the title", "description")

notification.post(notification.success, "This is the title", "description", 5)
```

Posts a notification with the specified type, title, and description.

| Parameter           | Type                                                 | Description                                                 |
| ------------------- | ---------------------------------------------------- | ----------------------------------------------------------- |
| notificationType    | [NotificationType](notification.md#notificationtype) | The type of notification                                    |
| title               | String                                               | The title of the notification                               |
| description         | String                                               | The description of the notification                         |
| time **(optional)** | Number                                               | Amount of time the notification will display for in seconds |

## NotificationType

### Success

```
notification.success
```

This type of notification will send a notification with a success icon

### Disable

```
notification.disable
```

This type of notification will send a notification with a disable icon

### Info

```
notification.info
```

This type of notification will send a notification with a info icon

### Warning

```
notification.warning
```

This type of notification will send a notification with a warning icon
