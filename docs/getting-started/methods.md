---
sidebar_position: 3
---

# Methods

| Method Name | Description | Paramateres | Returns |
| --- | --- | --- | --- |
| checkIfHasSMSPermission | Function which checks if the application has READ_SMS and RECEIVE_SMS permissions | N/A |  ```{ hasReceiveSmsPermission: true/false, hasReadSmsPermission: true \ false } ```|
| requestReadSMSPermission | Requests READ_SMS and RECEIVE_SMS permission, if missing | N/A | Returns true if granted, and false otherwise |
| startReadSMS |  Starts listening for incoming messages. Note: SMS Permissions should be present. | a callback fn | Incoming message body |