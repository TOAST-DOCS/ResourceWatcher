## Governance & Audit > Resource Watcher > API V2 Guide

> You can set up Resource Watcher to make RESTful API calls to receive notifications of events and changes in the state of your resources.

## User Access Key & Secret Access Key

To use the RESTful API, you must first obtain a User Access Key and Secret Access Key.<br/>
User Access Key and Secret Access Key can be issued in the **API security settings**.<br/>
In the drop-down menu that appears when you hover over your account in the upper-right corner of the console, select **API security settings**, and then click **Create User Access Key ID**.<br/>
For security purposes, it is recommended to create both a User Access Key and a Secret Access Key.

![[Figure 1] API security settings location](http://static.toastoven.net/prod_resource_watcher/img46_1_KO.png)
<center>[Figure 1] API security settings location</center>

![[Figure 2] API security settings page](http://static.toastoven.net/prod_resource_watcher/img47_1_KO.png)
<center>[Figure 2] API security settings page</center>

![[Figure 3] Create a User AccessKey and SecretAccessKey](http://static.toastoven.net/prod_resource_watcher/img48_1_KO.png)
<center>[Figure 3] Generate User Access Key and Secret Access Key</center>

## Check Public API URL & Appkey
Appkey is required to use Restful API.<br/>
You can check the issued key information by clicking **URL & Appkey** on the right side of the console.
![[Figure 4] Public API URL & Appkey](http://static.toastoven.net/prod_resource_watcher/img49_1_KO.png)
<center>[Figure 4] URL &amp; Appkey</center>

## RESTful API Guide

<a id="common-response-body"></a>
### Common Response Body

For all API requests, the HTTP response code is 200.<br/>
For detailed response results, see the header item in the Response Body.

| Key     | Type                              | Description |
|---------|-----------------------------------|-------------|
| header  | [Header](#common-response-header) | [Response Header]       |

- Header <a id="common-response-header"></a>

| Key           | 	Type    | 	Description                             |
|---------------|----------|------------------------------------------|
| isSuccessful  | 	boolean | 	Successful or not (true, false)                      |
| resultCode    | 	int     | 	Response code. Returns 0 on success, error code on failure            |
| resultMessage | 	String  | 	Response message. Returns "SUCCESS" on success, error message on failure  |

```json
{
  "header": {
    "isSuccessful": true,
    "resultCode": 0,
    "resultMessage": "SUCCESS"
  }
}
```

### 1. Notifications

#### 1.1 Register notifications

Basic Information

| Method | 	URI                                                  |
|--------|-------------------------------------------------------|
| POST   | 	/resource-watcher/v2.0/appkeys/{appKey}/event-alarms |

| Permission | 	
|---------------------------------|
| ResourceWatcher:Alarms.Create |

You can set up notifications for events that occur on your resources. <br/>


- For information on which events to set, see the response result in **API Guide > 3.1. Retrieve Events**.<br/>
- Notification targets include members, notification recipient groups, roles, and webhook types, and you can set an audience for each type
Resource targets can be set for **resource groups/tags**.
- Setting **Event All** allows you to receive notifications for all events that occur on a specific resource.
- Setting **Resource All** allows you to receive notifications for specific events regardless of the resource.
- You can’t set **Event All** and **Resource All** at the same time.

**[Request Header]**

| Key                        | 	Value                           |
|----------------------------|----------------------------------|
| X-TC-AUTHENTICATION-ID     | 	User Access Key issued from the console   |
| X-TC-AUTHENTICATION-SECRET | 	Secret Access Key issued from the console |

**[Path Variable]**

| Key    | 	Value                |
|--------|-----------------------|
| appKey  | Appkey issued from the console |


<a id="post-alarm-request"></a>
**[Request Body]**

| Key                         | 	Type                                             | 	Required | 	Description                                         |
|-----------------------------|---------------------------------------------------|-----------|------------------------------------------------------|
| alarm                       | [Alarm](#post-alarm-request-alarm)                | Yes       | Notification information                                                |
| alarmTargets                | [AlarmTarget[]](#post-alarm-request-alarm-target) | Yes       | About Notifications Recipient                                          |
| events                      | [Event[]](#post-alarm-request-event)              | No        | List of notification target events<br/> Unset if you want to be notified of all events as they occur. |
| target                      | [Target](#post-alarm-request-target)              | No        | Information on target resource<br/> Unset if you want to receive events regardless of resources.       |

- Alarm <a id="post-alarm-request-alarm"></a>

| Key               | 	Type     | 	Required | 	Description                     |
|-------------------|-----------|-----------|----------------------------------|
| alarmName   | 	String   | 	Yes      | 	Notification name <br/> Up to 255 characters can be registered   |
| description | 	String   | 	No       | 	Notification description <br/> Up to 1,000 characters can be registered |

- AlarmTarget <a id="post-alarm-request-alarm-target"></a>

| Key                 | 	Type          | 	Required | 	Description                                                                                                                                                                                         |
|---------------------|----------------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| alarmTargetTypeCode     | String     | Yes       | Notification target type code<br/><br/>Type<br/>1. UUID: For a single organization member (NHN Cloud member, IAM member)<br/>2. ROLE: Organization role, project role group, project role<br/>3. ALARM_KEY: Organization notification recipient group, project notification recipient group<br/>4. WEBHOOK: Webhook |
| alarmTarget         | 	String        | 	No       | 	Notification target information<br/><type-specific setting value><br/> 1. **UUID**: Member UUID <br/>2. **ROLE**: Role ID (e.g., ADMIN)<br/>3. **ALARM_KEY**: Group ID to receive alerts<br/>4. **WEBHOOK**: Not entered                                                  |
| emailAlarm          | 	String        | 	No       | 	Whether to receive emails<br/>1. **Y**: Receive emails<br/>2. **N**: Not receive emails<br/>WEBHOOK, ALARM_KEY is not entered.                                                                                                          |
| smsAlarm            | 	String        | 	No       | 	Whether to receive SMS<br/>1. **Y**: Receive SMS<br/>2. **N**: Not receiving SMS<br/>WEBHOOK, ALARM_KEY is not entered.                                                                                                          |
| webhookUrl          | 	String        | 	No       | Webhook URL address<br/>http:// Or https://로 to get started.<br/> Enter when setting the notification destination type **WEBHOOK**                                                                                                               |
| webhookSecret       | 	String        | 	No       | 	Webhook secret key<br/> Enter when setting the notification destination type **WEBHOOK**                                                                                                                                                 |

- Event <a id="post-alarm-request-event"></a>

| Key        | 	Type    | 	Required | 	Description |
|------------|----------|-----------|--------------|
| productId  | 	String  | 	Yes      | 	Service ID      |
| eventId    | 	String  | 	Yes      | 	Event ID      |

For the productId and eventId values, see **API Guide > 3.1 Event list lookup API response values**.

- Target <a id="post-alarm-request-target"></a>

| Key              | 	Type         | 	Required | 	Description      |
|------------------|---------------|-----------|-------------------|
| resourceGroupIds | 	String[]     | 	No       | 	List of resource group IDs     |
| resourceTagIds   | 	Long[]       | 	No       | 	List of resource tag IDs     |

- Examples
```json
{
  "alarm": {
    "alarmName": "",
    "description": ""
  },
  "alarmTargets": [
    {
      "alarmTarget": "",
      "alarmTargetTypeCode": "",
      "emailAlarm": "",
      "smsAlarm": "",
      "webhookSecret": "",
      "webhookUrl": ""
    }
  ],
  "events": [
    {
      "eventId": "",
      "productId": ""
    }
  ],
  "target": {
    "resourceGroupIds": [
      ""
    ],
    "resourceTagIds": [
      ""
    ]
  }
}
```

**[Response Body]**

* Note: This is the same as [](#common-response-body)Common Response Body](#common-response-body).

#### 1.2 View notifications

Basic Information

| Method | 	URI                                                            |
|--------|-----------------------------------------------------------------|
| GET    | 	/resource-watcher/v2.0/appkeys/{appKey}/event-alarms/{alarmId} |

| Permission                             | 	
|--------------------------------|
| ResourceWatcher:Alarms.Get |

Retrieves registered notifications.

**[Request Header]**

| Key                        | 	Value                        |
|----------------------------|-------------------------------|
| X-TC-AUTHENTICATION-ID     | 	User Access Key issued from the console   |
| X-TC-AUTHENTICATION-SECRET | 	Secret Access Key issued from the console |

**[Path Variable]**

| Key     | 	Value            |
|---------|-------------------|
| appKey  | 	Appkey issued from the console |
| alarmId | 	ID of the notification to look up       |

**[Response Body]**


| Key                       | 	Type                                                                           | 	Description                 |
|---------------------------|---------------------------------------------------------------------------------|------------------------------|
| alarm                     | 	[Alarm](#post-alarm-response-alarm)                                            | 	Notification information        |
| alarmTargetAlarmKeys      | 	[AlarmTargetAlarmKey[]](#post-alarm-response-alarm-target-alarm-key)           | 	List of ALARM_KEY information to receive notifications for      |
| alarmTargetMemberProfiles | 	[AlarmTargetMemberProfile[]](#post-alarm-response-alarm-target-member-profile) | 	List of UUID information to receive notifications   |
| alarmTargetRoles          | 	[AlarmTargetRole[]](#post-alarm-response-alarm-target-role)                    | 	List of ROLEs to receive notifications  |
| alarmTargets              | 	[AlarmTarget[]](#post-alarm-response-alarm-target)                             | 	Notification recipient list       |
| events                    | 	[Event[]](#post-alarm-response-event)                                          | 	Notification event list                   |
| target                    | 	[Target](#post-alarm-response-target)                                          | 	Information on target resource         |

- Alarm <a id="post-alarm-response-alarm"></a>

| Key                  | 	Type                                        | 	Description                                                                      |
|----------------------|----------------------------------------------|-----------------------------------------------------------------------------------|
| alarmId              | String                                       | Notification ID                                                                             |
| alarmName            | String                                       | Notification name                                                                             |
| alarmRule            | [AlarmRule](#post-alarm-response-alarm-rule) | Notification rule details                                                                       |
| alarmStatusCode      | String                                       | Notification status codes<br/><br/>Type<br/>1. STABLE: Enable<br/>2. DISABLED: Disabled<br/>3. CLOSED: Delete |
| appKey               | String                                       | About Appkey                                                                         |
| cabAlarmKey          | String                                       | Group ID to receive notifications                                                                       |
| delDatetime          | Date                                         | Date and time of deletion                                                                             |
| description          | String                                       | Notification description                                                                             |
| modDatetime          | Date                                         | Modification date                                                                             |
| operatorUuid         | String                                       | Last Modified User UUID                                                                   |
| regDatetime          | Date                                         | Registered date and time                                                                             |

- AlarmRule <a id="post-alarm-response-alarm-rule"></a>

| Key                     | 	Type    | 	Description                                                                           |
|-------------------------|----------|----------------------------------------------------------------------------------------|
| alarmRuleId             | String   | Notification rule ID                                                                               |
| alarmRuleStatusCode     | String   | Notification rule status codes<br/><br/>Type<br/>1. STABLE: Enable<br/>2. DISABLED: Disabled<br/>3. CLOSED: Delete |
| alarmRuleName           | String   | Notification rule name                                                                               |
| alarmRuleDescription    | String   | Notification rule descriptions                                                                               |
| resourceTypes           | String[] | List of target resource type codes that the alert rule applies to<br/>An empty value targets the entire resource type<br/>List of String types              |

- AlarmTargetAlarmKey <a id="post-alarm-response-alarm-target-alarm-key"></a>

| Key            | 	Type      | 	Description |
|----------------|------------|--------------|
| alarmKey       | String     | Notification keys         |
| alarmGroupName | String     | Group name to receive notifications    |
| alarmGroupDesc | String     | Notification receiver group descriptions  |


- AlarmTargetMemberProfile <a id="post-alarm-response-alarm-target-member-profile"></a>

| Key             | 	Type      | 	Description                                       |
|-----------------|------------|----------------------------------------------------|
| UUID            | String     | Member UUID                                            |
| memberType      | String     | Separate members<br/><br/>Type<br/>1. TOAST_CLOUD<br/>2. IAM |
| name            | String     | Member name                                              |
| corporationName | String     | Business name                                              |
| email           | String     | Member email                                             |
| userId          | String     | Member ID                                              |

- AlarmTargetRole <a id="post-alarm-response-alarm-target-role"></a>

| Key           | 	Type      | 	Description |
|---------------|------------|--------------|
| String          | String     | Role type        |
| roleId        | String     | Role ID        |
| roleName      | String     | Role name          |
| description   | String     | Role descriptions        |

- AlarmTarget <a id="post-alarm-response-alarm-target"></a>

| Key                     | 	Type        | 	Description                                                                                                                                                         |
|-------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| alarmTargetTypeCode     | String       | Notification target type code<br/><br/>Type<br/>1. UUID: For a single organization member (NHN Cloud member, IAM member)<br/>2. ROLE: Organization role, project role group, project role<br/>3. ALARM_KEY: Organization notification recipient group, project notification recipient group<br/>4. WEBHOOK: Webhook |
| alarmTarget             | String       | Notification target information                                                                                                                                                             |
| emailAlarm              | String       | Whether to receive emails (Y, N)                                                                                                                                                      |
| smsAlarm                | string       | Whether SMS is received (Y, N)                                                                                                                                                      |
| webhookUrl              | string       | Webhook URL address |
| webhookSecret           | string       | Webhook secret key                                                                                                                                                         |

- Event <a id="post-alarm-response-event"></a>

| Key          | 	Type        | 	Description   |
|--------------|--------------|----------------|
| productId    | 	String      | 	Product ID         |
| eventId      | 	String      | 	Event ID        |


- Target <a id="post-alarm-response-target"></a>

| Key            | 	Type                                                  | 	Description     |
|----------------|--------------------------------------------------------|------------------|
| resourceGroups | [ResourceGroup[]](#post-alarm-response-resource-group) | Resource Group List        |
| resourceTags   | [ResourceTag[]](#post-alarm-response-resource-tag)     | Resource Tag List        |


- ResourceGroup <a id="post-alarm-response-resource-group"></a>

| Key               | 	Type   | 	Description   |
|-------------------|---------|----------------|
| resourceGroupId   | String  | 	List of resource group IDs  |
| resourceGroupName | String  | List of resource tag IDs   |

- ResourceTag <a id="post-alarm-response-resource-tag"></a>

| Key        | 	Type                                                       | 	Description               |
|------------|-------------------------------------------------------------|----------------------------|
| tagId      | Long                                                        | Resource Tag ID                  |
| tagGroupId | Long                                                        | Resource tag group ID               |
| tagName    | String                                                      | Resource tag name                  |  
| resourceTagTypeCode    | String                                                      | Resource tag type code (DEFAULT, NORMAL) |
| regDatetime    | Date                                                        | Resource tag registration date               |
| modDatetime    | Date                                                        | Resource tag modification date               |
| resourceTagGroup    | [ResourceTagGroup](#post-alarm-response-resource-tag-group) | Resource Tag Groups                  |

- ResourceTagGroup <a id="post-alarm-response-resource-tag-group"></a>

| Key        | 	Type  | 	Description        |
|------------|--------|---------------------|
| tagGroupId      | Long   | Resource tag group ID        |
| tagGroupKey | String | Resource tag key            |
| appKey    | String | Appkey                  |  
| creationTypeCode    | String | Creation type (USER, SYSTEM) |
| regDatetime    | Date   | Resource tag group registration date     |
| modDatetime    | Date | Resource tag group modification date   |

- Examples

```json
{
  "header": {
    "isSuccessful": true,
    "resultCode": 0,
    "resultMessage": ""
  },
  "alarm": {
    "alarmId": "",
    "alarmName": "",
    "alarmRule": {
      "alarmRuleDescription": "",
      "alarmRuleId": "",
      "alarmRuleName": "",
      "alarmRuleStatusCode": "",
      "resourceTypes": [
        ""
      ]
    },
    "alarmStatusCode": "",
    "appKey": "",
    "cabAlarmKey": "",
    "delDatetime": "yyyy-MM-ddTHH:mm:SS",
    "description": "",
    "modDatetime": "yyyy-MM-ddTHH:mm:SS",
    "operatorUuid": "",
    "regDatetime": "yyyy-MM-ddTHH:mm:SS"
  },
  "alarmTargetAlarmKeys": [
    {
      "alarmGroupDesc": "",
      "alarmGroupName": "",
      "alarmKey": ""
    }
  ],
  "alarmTargetMemberProfiles": [
    {
      "corporationName": "",
      "email": "",
      "memberType": "",
      "name": "",
      "userId": "",
      "uuid": ""
    }
  ],
  "alarmTargetRoles": [
    {
      "description": "",
      "roleId": "",
      "roleName": "",
      "type": ""
    }
  ],
  "alarmTargets": [
    {
      "alarmTarget": "",
      "alarmTargetTypeCode": "",
      "emailAlarm": "",
      "smsAlarm": "",
      "webhookSecret": "",
      "webhookUrl": ""
    }
  ],
  "events": [
    {
      "eventId": "",
      "productId": ""
    }
  ],
  "target": {
    "resourceGroups": [
      {
        "resourceGroupId": "",
        "resourceGroupName": ""
      }
    ],
    "resourceTags": [
      {
        "tagId": 0,
        "tagGroupId" : 0,
        "tagName": "",
        "resourceTagTypeCode" : "",
        "regDatetime": "yyyy-MM-ddTHH:mm:SS",
        "modDatetime": "yyyy-MM-ddTHH:mm:SS",
        "resourceTagGroup" : {
            "tagGroupId": 0,
            "tagGroupKey": "",
            "appKey": "",
            "creationTypeCode": "",
            "regDatetime": "yyyy-MM-ddTHH:mm:SS",
            "modDatetime": "yyyy-MM-ddTHH:mm:SS"
        }
      }
    ]
  }
}
```


#### 1.3 Get a list of notifications

Basic Information

| Method | 	URI                                                         |
|--------|--------------------------------------------------------------|
| POST   | 	/resource-watcher/v2.0/appkeys/{appKey}/event-alarms/search |

| Permission                             | 	
|--------------------------------|
| ResourceWatcher:Alarms.List |

Get a list of event notifications you've signed up for.
- You can include search criteria in your request to get the list of notifications you want.
- Supports paging.

**[Request Header]**

| Key                        | 	Value                        |
|----------------------------|-------------------------------|
| X-TC-AUTHENTICATION-ID     | 	User Access Key issued from the console   |
| X-TC-AUTHENTICATION-SECRET | 	Secret Access Key issued from the console |

**[Path Variable]**

| Key    | 	Value             |
|--------|--------------------|
| appKey | 	Appkey issued from the console |


**[Query Parameter]**

| Key  | 	Value                                      | Required |
|------|---------------------------------------------|----------|
| page | 	Page number to search<br/>Default value: 0                | No       |
| size | 	Number of notifications to view<br/>Default value: 10                | No       |
| sort | What and how to sort<br/>Default values: modDatetime, DESC | No       |

**[Request Body]**

| Key                | 	Type    | Required | 	Description                                                                                                                     |
|--------------------|----------|----------|----------------------------------------------------------------------------------------------------------------------------------|
| alarmIds           | String[] | No       | List of notification IDs<br/>List of String types                                                                                                       |
| alarmNameAnyLike   | String   | No       | Alert name (retrieves all alerts that contain the input value)                                                                                                       |
| alarmRuleIds       | String[] | No       | List of alert rule IDs<br/>List of String types                                                                                                    |
| alarmStatusCodes   | String[] | No       | Notification status<br/>List of String types<br/>Default values: STABLE, DISABLED<br/><br/>Type<br/>1. STABLE: Enable<br/>2. DISABLED: Disabled<br/>3. CLOSED: Delete |
| descriptionAnyLike | String   | No       | Alert descriptions (retrieve all alerts that contain the input value)                                                                                                       |
| modDateFrom        | Date     | No       | Start last modification pause                                                                                                                     |
| modDateTo          | Date     | No       | End last modified pause                                                                                                                     |
| operatorUuids      | String[] | No       | List of last modifier UUIDs<br/>List of String types                                                                                                |
| resourceGroupIds   | String[] | No       | Resource Group List<br/>List of String types                                                                                                      |

```json
{
  "alarmIds": [
    ""
  ],
  "alarmNameAnyLike": "",
  "alarmRuleIds": [
    ""
  ],
  "alarmStatusCodes": [
    ""
  ],
  "descriptionAnyLike": "",
  "modDateFrom": "yyyy-MM-ddTHH:mm:SS",
  "modDateTo": "yyyy-MM-ddTHH:mm:SS",
  "operatorUuids": [
    ""
  ],
  "resourceGroupIds": [
    ""
  ]
}
```


**[Response Body]**

| Key        | 	Type                                 | Description |
|------------|---------------------------------------|-------------|
| alarms     | [Alarm](#list-alarm-response-alarm) | Notifications list       |
| totalItems | Long                                  | Total number       |


- Alarm <a id="list-alarm-response-alarm"></a>

| Key             | 	Type                                        | 	Description                                                                      |
|-----------------|----------------------------------------------|-----------------------------------------------------------------------------------|
| alarmId         | String                                       | Notification ID                                                                             |
| alarmName       | String                                       | Notification name                                                                             |
| alarmRule       | [AlarmRule](#list-alarm-response-alarm-rule) | Notification rule details                                                                       |
| alarmStatusCode | String                                       | Notification status codes<br/><br/>Type<br/>1. STABLE: Enable<br/>2. DISABLED: Disabled<br/>3. CLOSED: Delete |
| appKey          | String                                       | About Appkey                                                                         |
| cabAlarmKey     | String                                       | Group ID to receive notifications                                                                       |
| description     | String                                       | Notification description                                                                             |
| operatorUuid    | String                                       | Last Modified User UUID                                                                   |
| delDatetime     | Date                                         | Date and time of deletion                                                                             |
| modDatetime     | Date                                         | Modification date                                                                             |
| regDatetime     | Date                                         | Registered date and time                                                                             |

- AlarmRule <a id ="list_alarm_response_alarm_rule"></a>

| Key                  | 	Type    | 	Description                                                                         |
|----------------------|----------|--------------------------------------------------------------------------------------|
| alarmRuleId          | String   | Notification rule ID                                                                             |
| alarmRuleStatusCode  | String   | Notification rule status codes<br/><br/>Type<br/>1. STABLE: Enable<br/>2. DISABLED: Disabled<br/>3. CLOSED: Delete |
| alarmRuleName        | String   | Notification rule name                                                                             |
| alarmRuleDescription | String   | Notification rule descriptions                                                                             |
| resourceTypes        | String[] | List of target resource type codes that the alert rule applies to<br/>An empty value targets the entire resource type<br/>List of String types            |

- Examples

```json
{
  "header": {
    "isSuccessful": true,
    "resultCode": 0,
    "resultMessage": ""
  },
  "alarms": [
    {
      "alarmId": "",
      "alarmName": "",
      "alarmRule": {
        "alarmRuleDescription": "",
        "alarmRuleId": "",
        "alarmRuleName": "",
        "alarmRuleStatusCode": "",
        "resourceTypes": [
          ""
        ]
      },
      "alarmStatusCode": "",
      "appKey": "",
      "cabAlarmKey": "",
      "delDatetime": "yyyy-MM-ddTHH:mm:SS",
      "description": "",
      "modDatetime": "yyyy-MM-ddTHH:mm:SS",
      "operatorUuid": "",
      "regDatetime": "yyyy-MM-ddTHH:mm:SS"
    }
  ],
  "totalItems": 0
}
```

#### 1.4. Edit notifications

Basic Information

| Method | 	URI                                                            |
|--------|-----------------------------------------------------------------|
| PUT    | 	/resource-watcher/v1.0/appkeys/{appKey}/event-alarms/{alarmId} |

| Permission                             | 	
|--------------------------------|
| ResourceWatcher:Alarms.Update |

Edit a registered alert.
- Since we're changing everything you requested, we need **to transfer the existing setting values for the ones that don't change**.

**[Request Header]**

| Key                        | 	Value                        |
|----------------------------|-------------------------------|
| X-TC-AUTHENTICATION-ID     | 	User Access Key issued from the console   |
| X-TC-AUTHENTICATION-SECRET | 	Secret Access Key issued from the console |

**[Path Variable]**

| Key     | Value            |
|---------|------------------|
| appKey  | Appkey issued from the console |
| alarmId | ID of the alert to modify       |


**[Request Body]**

* Note: This is the same as [](#common-response-body)Common Response Body](#common-response-body).

#### 1.5. Delete a notification

Basic Information

| Method | 	URI                                                            |
|--------|-----------------------------------------------------------------|
| DELETE | 	/resource-watcher/v2.0/appkeys/{appKey}/event-alarms/{alarmId} |

| Permission                             | 	
|--------------------------------|
| ResourceWatcher:Alarms.Delete |

Delete a registered alert.

**[Request Header]**

| Key                        | 	Value                        |
|----------------------------|-------------------------------|
| X-TC-AUTHENTICATION-ID     | 	User Access Key issued from the console   |
| X-TC-AUTHENTICATION-SECRET | 	Secret Access Key issued from the console |

**[Path Variable]**

| Key     | Value              |
|---------|--------------------|
| appKey  | Appkey issued from the console   |
| alarmId | ID of the notification to delete         |


**[Response Body]**

* Note: This is the same as [](#common-response-body)Common Response Body](#common-response-body).


#### 1.6. Delete a batch of notifications


Basic Information

| Method | 	URI                                                  |
|--------|-------------------------------------------------------|
| DELETE | 	/resource-watcher/v2.0/appkeys/{appKey}/event-alarms |

| Permission                             | 	
|--------------------------------|
| ResourceWatcher:Alarms.Delete |

Delete multiple registered alerts.

**[Request Header]**

| Key                        | 	Value                        |
|----------------------------|-------------------------------|
| X-TC-AUTHENTICATION-ID     | 	User Access Key issued from the console   |
| X-TC-AUTHENTICATION-SECRET | 	Secret Access Key issued from the console |

**[Path Variable]**

| Key     | Value            |
|---------|------------------|
| appKey  | Appkey issued from the console |


**[Query Parameter]**재

| Key      | Value                                     | Required |
|----------|-------------------------------------------|----------|
| alarmIds | List of notification IDs to delete<br/>You must enter at least one value. | Yes      |

**[Response Body]**

* Note: This is the same as [Common Response Body](#common-response-body).