---
sidebar_position: 3
---

# Methods

| Method Name | Description | Parameters | Returns |
| --- | --- | --- | --- |
| checkIfHasSMSPermission | Checks if the application has READ_SMS and RECEIVE_SMS permissions | N/A | `{ hasReceiveSmsPermission: true/false, hasReadSmsPermission: true/false }` |
| requestReadSMSPermission | Requests READ_SMS and RECEIVE_SMS permission, if missing | N/A | Returns `true` if granted, `false` otherwise |
| startReadSMS | Starts listening for incoming messages. SMS permissions must be granted. | callback fn | Calls callback with `[phoneNumber, messageBody]` |
| stopReadSMS | Stops listening for incoming messages. | N/A | void |
