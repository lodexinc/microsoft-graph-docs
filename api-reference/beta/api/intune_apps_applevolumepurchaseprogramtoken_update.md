﻿# Update appleVolumePurchaseProgramToken
Update the properties of a [appleVolumePurchaseProgramToken](../resources/intune_apps_applevolumepurchaseprogramtoken.md) object.
### Prerequisites
One of the following **scopes** is required to execute this API:

*DeviceManagementApps.ReadWrite.All*
### HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
```http
PATCH /deviceAppManagement/mobileApps/<id>/microsoft.graph.iosVppApp/vppToken/
```

### Request headers
|Header|Value|
|---|---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

### Request body
In the request body, supply a JSON representation of a [appleVolumePurchaseProgramToken](../resources/intune_apps_applevolumepurchaseprogramtoken.md) object.
The following table shows the properties that are required when you create a [appleVolumePurchaseProgramToken](../resources/intune_apps_applevolumepurchaseprogramtoken.md).

|Property|Type|Description|
|---|---|---|
|id|String|Not yet documented|
|organizationName|String|The organization associated with the Apple Volume Purchase Program Token.|
|volumePurchaseProgramTokenAccountType|String|The type of volume purchase program which the given Apple Volume Purchase Program Token is associated with. Possible values are: `business`, `education`.|
|appleId|String|The apple Id associated with the given Apple Volume Purchase Program Token.|
|expirationDateTime|DateTimeOffset|The expiration date time of the Apple Volume Purchase Program Token.|
|lastSyncDateTime|DateTimeOffset|The last time when an application sync was done with the Apple volume purchase program service using the the Apple Volume Purchase Program Token.|
|token|String|The Apple Volume Purchase Program Token string downloaded from the Apple Volume Purchase Program.|
|lastModifiedDateTime|DateTimeOffset|Last modification date time associated with the Apple Volume Purchase Program Token.|
|state|String|Current state of the Apple Volume Purchase Program Token. Possible values are: `unknown`, `valid`, `expired`, `invalid`.|
|lastSyncStatus|String|Current sync status of the last application sync which was triggered using the Apple Volume Purchase Program Token. Possible values are: `none`, `inProgress`, `completed`, `failed`.|



### Response
If successful, this method returns a `200 OK` response code and an updated [appleVolumePurchaseProgramToken](../resources/intune_apps_applevolumepurchaseprogramtoken.md) object in the response body.

### Example
##### Request
Here is an example of the request.
```http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/<id>/microsoft.graph.iosVppApp/vppToken/
Content-type: application/json
Content-length: 411

{
  "organizationName": "Organization Name value",
  "volumePurchaseProgramTokenAccountType": "education",
  "appleId": "Apple Id value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "token": "Token value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "state": "valid",
  "lastSyncStatus": "inProgress"
}
```

##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 530

{
  "@odata.type": "#microsoft.graph.appleVolumePurchaseProgramToken",
  "id": "7284da05-da05-7284-05da-847205da8472",
  "organizationName": "Organization Name value",
  "volumePurchaseProgramTokenAccountType": "education",
  "appleId": "Apple Id value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "token": "Token value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "state": "valid",
  "lastSyncStatus": "inProgress"
}
```


