# OpenAPIClient-php

A CPaaS platform API

For more information, please visit [https://whitelabelcomm.com](https://whitelabelcomm.com).

## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$start_key = 'start_key_example'; // string | start_key for pagination that was returned as next_start_key from your previous call
$page_size = 56; // int | number of records to return, range 1 to 50

try {
    $result = $apiInstance->v1AccountAccountidChildrenGet($accountid, $start_key, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountAccountidChildrenGet: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *http://api.beta.cpaaslabs.net*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AccountApi* | [**v1AccountAccountidChildrenGet**](docs/Api/AccountApi.md#v1accountaccountidchildrenget) | **GET** /v1/account/{accountid}/children | Get Sub Account List
*AccountApi* | [**v1AccountAccountidDelete**](docs/Api/AccountApi.md#v1accountaccountiddelete) | **DELETE** /v1/account/{accountid} | Delete Account
*AccountApi* | [**v1AccountAccountidDnsrecordGet**](docs/Api/AccountApi.md#v1accountaccountiddnsrecordget) | **GET** /v1/account/{accountid}/dnsrecord | Get Account DNS Record
*AccountApi* | [**v1AccountAccountidDnsrecordPost**](docs/Api/AccountApi.md#v1accountaccountiddnsrecordpost) | **POST** /v1/account/{accountid}/dnsrecord | Create Account DNS Record
*AccountApi* | [**v1AccountAccountidDnsrecordPut**](docs/Api/AccountApi.md#v1accountaccountiddnsrecordput) | **PUT** /v1/account/{accountid}/dnsrecord | Convert Account DNS Record
*AccountApi* | [**v1AccountAccountidGet**](docs/Api/AccountApi.md#v1accountaccountidget) | **GET** /v1/account/{accountid} | Get Account Details
*AccountApi* | [**v1AccountAccountidLimitGet**](docs/Api/AccountApi.md#v1accountaccountidlimitget) | **GET** /v1/account/{accountid}/limit | Get Account Limits
*AccountApi* | [**v1AccountAccountidLimitPut**](docs/Api/AccountApi.md#v1accountaccountidlimitput) | **PUT** /v1/account/{accountid}/limit | Set Account Limits
*AccountApi* | [**v1AccountAccountidPost**](docs/Api/AccountApi.md#v1accountaccountidpost) | **POST** /v1/account/{accountid} | Create Sub Account
*AccountApi* | [**v1AccountAccountidProvisioningdetailsGet**](docs/Api/AccountApi.md#v1accountaccountidprovisioningdetailsget) | **GET** /v1/account/{accountid}/provisioningdetails | Get Account Provisioning Details
*AccountApi* | [**v1AccountAccountidProvisioningdetailsResetpwPut**](docs/Api/AccountApi.md#v1accountaccountidprovisioningdetailsresetpwput) | **PUT** /v1/account/{accountid}/provisioningdetails/resetpw | Reset the provisioning details password.
*AccountApi* | [**v1AccountAccountidPut**](docs/Api/AccountApi.md#v1accountaccountidput) | **PUT** /v1/account/{accountid} | Update Account
*AccountApi* | [**v1AccountApikeyGet**](docs/Api/AccountApi.md#v1accountapikeyget) | **GET** /v1/account/apikey | 
*AccountApi* | [**v1AccountGet**](docs/Api/AccountApi.md#v1accountget) | **GET** /v1/account | Get Account List
*AccountApi* | [**v1AccountPost**](docs/Api/AccountApi.md#v1accountpost) | **POST** /v1/account | Create Account
*CPaaSManagementApi* | [**v1MgmtUserGet**](docs/Api/CPaaSManagementApi.md#v1mgmtuserget) | **GET** /v1/mgmt/user | Get All CPaaS Users
*CPaaSManagementApi* | [**v1MgmtUserPost**](docs/Api/CPaaSManagementApi.md#v1mgmtuserpost) | **POST** /v1/mgmt/user | Invite CPaaS User
*CPaaSManagementApi* | [**v1MgmtUserUserIDDelete**](docs/Api/CPaaSManagementApi.md#v1mgmtuseruseriddelete) | **DELETE** /v1/mgmt/user/{userID} | Delete CPaaS User
*CPaaSManagementApi* | [**v1MgmtUserUserIDGet**](docs/Api/CPaaSManagementApi.md#v1mgmtuseruseridget) | **GET** /v1/mgmt/user/{userID} | Get CPaaS User Details
*CPaaSManagementApi* | [**v1MgmtUserUserIDPut**](docs/Api/CPaaSManagementApi.md#v1mgmtuseruseridput) | **PUT** /v1/mgmt/user/{userID} | Update CPaaS User Role
*CallParkApi* | [**v1AccountAccountIDParkedcallGet**](docs/Api/CallParkApi.md#v1accountaccountidparkedcallget) | **GET** /v1/account/{accountID}/parkedcall | Get Call Park List
*CallQueueManagementApi* | [**v1AccountAccountIDCallqueueGet**](docs/Api/CallQueueManagementApi.md#v1accountaccountidcallqueueget) | **GET** /v1/account/{accountID}/callqueue | Get Call Queues
*CallQueueManagementApi* | [**v1AccountAccountIDCallqueuePost**](docs/Api/CallQueueManagementApi.md#v1accountaccountidcallqueuepost) | **POST** /v1/account/{accountID}/callqueue | Create Call Queue
*CallQueueManagementApi* | [**v1AccountAccountIDCallqueueQueueIDDelete**](docs/Api/CallQueueManagementApi.md#v1accountaccountidcallqueuequeueiddelete) | **DELETE** /v1/account/{accountID}/callqueue/{queueID} | Delete Call Queue
*CallQueueManagementApi* | [**v1AccountAccountIDCallqueueQueueIDGet**](docs/Api/CallQueueManagementApi.md#v1accountaccountidcallqueuequeueidget) | **GET** /v1/account/{accountID}/callqueue/{queueID} | Get Call Queue Details
*CallQueueManagementApi* | [**v1AccountAccountIDCallqueueQueueIDPut**](docs/Api/CallQueueManagementApi.md#v1accountaccountidcallqueuequeueidput) | **PUT** /v1/account/{accountID}/callqueue/{queueID} | Update Call Queue
*CallQueueManagementApi* | [**v1AccountAccountIDCallqueueQueueIDStatusGet**](docs/Api/CallQueueManagementApi.md#v1accountaccountidcallqueuequeueidstatusget) | **GET** /v1/account/{accountID}/callqueue/{queueID}/status | Get Call Queue Status
*CallQueueManagementApi* | [**v1AccountAccountIDQueuerolesGet**](docs/Api/CallQueueManagementApi.md#v1accountaccountidqueuerolesget) | **GET** /v1/account/{accountID}/queueroles | Get Queue Roles of Account
*CallQueueManagementApi* | [**v1AccountAccountIDQueuerolesQueueIDPost**](docs/Api/CallQueueManagementApi.md#v1accountaccountidqueuerolesqueueidpost) | **POST** /v1/account/{accountID}/queueroles/{queueID} | Assign Queue Role to Call Queue
*CallQueueMembershipApi* | [**v1AccountAccountIDQueuemembershipPost**](docs/Api/CallQueueMembershipApi.md#v1accountaccountidqueuemembershippost) | **POST** /v1/account/{accountID}/queuemembership | Grant Queue Membership to User
*CallQueueMembershipApi* | [**v1AccountAccountIDQueuemembershipRecipientIDDisablePost**](docs/Api/CallQueueMembershipApi.md#v1accountaccountidqueuemembershiprecipientiddisablepost) | **POST** /v1/account/{accountID}/queuemembership/{recipientID}/disable | Disable Queue Membership
*CallQueueMembershipApi* | [**v1AccountAccountIDQueuemembershipRecipientIDEnablePost**](docs/Api/CallQueueMembershipApi.md#v1accountaccountidqueuemembershiprecipientidenablepost) | **POST** /v1/account/{accountID}/queuemembership/{recipientID}/enable | Enable Queue Membership
*CallQueueRecipientApi* | [**v1AccountAccountIDLoginrecipientRecipientIDPost**](docs/Api/CallQueueRecipientApi.md#v1accountaccountidloginrecipientrecipientidpost) | **POST** /v1/account/{accountID}/loginrecipient/{recipientID} | Login as Recipient
*CallQueueRecipientApi* | [**v1AccountAccountIDQueuerecipientGet**](docs/Api/CallQueueRecipientApi.md#v1accountaccountidqueuerecipientget) | **GET** /v1/account/{accountID}/queuerecipient | Change Recipient Status
*CallQueueRecipientApi* | [**v1AccountAccountIDRecipientRecipientIDStatusPost**](docs/Api/CallQueueRecipientApi.md#v1accountaccountidrecipientrecipientidstatuspost) | **POST** /v1/account/{accountID}/recipient/{recipientID}/status | Get Recipient List
*CallRecordingApi* | [**v1AccountAccountIDRecordingGet**](docs/Api/CallRecordingApi.md#v1accountaccountidrecordingget) | **GET** /v1/account/{accountID}/recording | Get Account Call Recording
*CallRecordingApi* | [**v1AccountAccountIDRecordingRecordingIDDelete**](docs/Api/CallRecordingApi.md#v1accountaccountidrecordingrecordingiddelete) | **DELETE** /v1/account/{accountID}/recording/{recordingID} | Delete Call Recording
*CallRecordingApi* | [**v1AccountAccountIDRecordingRecordingIDGet**](docs/Api/CallRecordingApi.md#v1accountaccountidrecordingrecordingidget) | **GET** /v1/account/{accountID}/recording/{recordingID} | Get Call Recording Details
*CallRecordingApi* | [**v1AccountAccountIDUserUserIDRecordingGet**](docs/Api/CallRecordingApi.md#v1accountaccountiduseruseridrecordingget) | **GET** /v1/account/{accountID}/user/{userID}/recording | Get User Call Recording
*CallflowApi* | [**v1AccountAccountIDCallflowCallflowIDDelete**](docs/Api/CallflowApi.md#v1accountaccountidcallflowcallflowiddelete) | **DELETE** /v1/account/{accountID}/callflow/{callflowID} | Delete Call Group
*CallflowApi* | [**v1AccountAccountIDCallflowCallflowIDGet**](docs/Api/CallflowApi.md#v1accountaccountidcallflowcallflowidget) | **GET** /v1/account/{accountID}/callflow/{callflowID} | Get Call Group Details
*CallflowApi* | [**v1AccountAccountIDCallflowCallflowIDPut**](docs/Api/CallflowApi.md#v1accountaccountidcallflowcallflowidput) | **PUT** /v1/account/{accountID}/callflow/{callflowID} | Update Call Group
*CallflowApi* | [**v1AccountAccountIDCallflowGet**](docs/Api/CallflowApi.md#v1accountaccountidcallflowget) | **GET** /v1/account/{accountID}/callflow | Get Callflow List
*CallflowApi* | [**v1AccountAccountIDCallflowPost**](docs/Api/CallflowApi.md#v1accountaccountidcallflowpost) | **POST** /v1/account/{accountID}/callflow | Create Call Group
*ChannelApi* | [**v1AccountAccountIDChannelChannelIDGet**](docs/Api/ChannelApi.md#v1accountaccountidchannelchannelidget) | **GET** /v1/account/{accountID}/channel/{channelID} | Get Channel Details
*ChannelApi* | [**v1AccountAccountIDChannelChannelIDPost**](docs/Api/ChannelApi.md#v1accountaccountidchannelchannelidpost) | **POST** /v1/account/{accountID}/channel/{channelID} | Associate Action to Channel
*ChannelApi* | [**v1AccountAccountIDChannelChannelIDPut**](docs/Api/ChannelApi.md#v1accountaccountidchannelchannelidput) | **PUT** /v1/account/{accountID}/channel/{channelID} | Associate Metaflow to Channel
*ChannelApi* | [**v1AccountAccountIDChannelGet**](docs/Api/ChannelApi.md#v1accountaccountidchannelget) | **GET** /v1/account/{accountID}/channel | Get Account Channel List
*ChannelApi* | [**v1AccountAccountIDDeviceDeviceIDChannelGet**](docs/Api/ChannelApi.md#v1accountaccountiddevicedeviceidchannelget) | **GET** /v1/account/{accountID}/device/{deviceID}/channel | Get Device Channel List
*ChannelApi* | [**v1AccountAccountIDUserUserIDChannelGet**](docs/Api/ChannelApi.md#v1accountaccountiduseruseridchannelget) | **GET** /v1/account/{accountID}/user/{userID}/channel | Get User Channel List
*DataApi* | [**v1AccountAccountIDCdrCdrIDGet**](docs/Api/DataApi.md#v1accountaccountidcdrcdridget) | **GET** /v1/account/{accountID}/cdr/{cdrID} | Get CDR Details
*DataApi* | [**v1AccountAccountIDCdrGet**](docs/Api/DataApi.md#v1accountaccountidcdrget) | **GET** /v1/account/{accountID}/cdr | Get CDR List
*DataApi* | [**v1DataCallDailySummaryGet**](docs/Api/DataApi.md#v1datacalldailysummaryget) | **GET** /v1/data/call_daily_summary | Get Call Daily Summary List
*DataApi* | [**v1DataCallDetailGet**](docs/Api/DataApi.md#v1datacalldetailget) | **GET** /v1/data/call_detail | Get Call Detail List
*DataApi* | [**v1DataCallMonthlySummaryGet**](docs/Api/DataApi.md#v1datacallmonthlysummaryget) | **GET** /v1/data/call_monthly_summary | Get Call Detail List
*DataApi* | [**v1DataEndpointListGet**](docs/Api/DataApi.md#v1dataendpointlistget) | **GET** /v1/data/endpoint_list | Get Endpoint List
*DataApi* | [**v1DataEventDailySummaryGet**](docs/Api/DataApi.md#v1dataeventdailysummaryget) | **GET** /v1/data/event_daily_summary | Get Event Daily Summary List
*DataApi* | [**v1DataEventDetailGet**](docs/Api/DataApi.md#v1dataeventdetailget) | **GET** /v1/data/event_detail | Get Event Details
*DataApi* | [**v1DataEventMonthlySummaryGet**](docs/Api/DataApi.md#v1dataeventmonthlysummaryget) | **GET** /v1/data/event_monthly_summary | Get Event Monthly Summary List
*DataApi* | [**v1DataFeatureDailySummaryGet**](docs/Api/DataApi.md#v1datafeaturedailysummaryget) | **GET** /v1/data/feature_daily_summary | Get Feature Daily Summary List
*DataApi* | [**v1DataFeatureMonthlySummaryGet**](docs/Api/DataApi.md#v1datafeaturemonthlysummaryget) | **GET** /v1/data/feature_monthly_summary | Get Feature Monthly Summary List
*DeviceApi* | [**v1AccountAccountidDeviceDeviceidDelete**](docs/Api/DeviceApi.md#v1accountaccountiddevicedeviceiddelete) | **DELETE** /v1/account/{accountid}/device/{deviceid} | Delete Device
*DeviceApi* | [**v1AccountAccountidDeviceDeviceidGet**](docs/Api/DeviceApi.md#v1accountaccountiddevicedeviceidget) | **GET** /v1/account/{accountid}/device/{deviceid} | Get Device Details
*DeviceApi* | [**v1AccountAccountidDeviceDeviceidPut**](docs/Api/DeviceApi.md#v1accountaccountiddevicedeviceidput) | **PUT** /v1/account/{accountid}/device/{deviceid} | Update Device
*DeviceApi* | [**v1AccountAccountidDeviceDeviceidRebootPost**](docs/Api/DeviceApi.md#v1accountaccountiddevicedeviceidrebootpost) | **POST** /v1/account/{accountid}/device/{deviceid}/reboot | Reboot Device
*DeviceApi* | [**v1AccountAccountidDeviceGet**](docs/Api/DeviceApi.md#v1accountaccountiddeviceget) | **GET** /v1/account/{accountid}/device | Get Device List
*DeviceApi* | [**v1AccountAccountidDevicePost**](docs/Api/DeviceApi.md#v1accountaccountiddevicepost) | **POST** /v1/account/{accountid}/device | Create Device
*DeviceApi* | [**v1AccountAccountidDeviceStatusGet**](docs/Api/DeviceApi.md#v1accountaccountiddevicestatusget) | **GET** /v1/account/{accountid}/device/status | Get Device Status
*E911Api* | [**v1E911Get**](docs/Api/E911Api.md#v1e911get) | **GET** /v1/e911 | Get E911 List
*E911Api* | [**v1E911LocationLocationIDActivatePut**](docs/Api/E911Api.md#v1e911locationlocationidactivateput) | **PUT** /v1/e911/location/{locationID}/activate | Activate E911 Location
*E911Api* | [**v1E911LocationLocationIDDelete**](docs/Api/E911Api.md#v1e911locationlocationiddelete) | **DELETE** /v1/e911/location/{locationID} | Delete E911 Location
*E911Api* | [**v1E911LocationValidatePut**](docs/Api/E911Api.md#v1e911locationvalidateput) | **PUT** /v1/e911/location/validate | Validate a Location
*E911Api* | [**v1E911PhoneNumberDelete**](docs/Api/E911Api.md#v1e911phonenumberdelete) | **DELETE** /v1/e911/{phoneNumber} | Delete E911 Phone Number
*E911Api* | [**v1E911PhoneNumberLocationActiveGet**](docs/Api/E911Api.md#v1e911phonenumberlocationactiveget) | **GET** /v1/e911/{phoneNumber}/location/active | Get Actvie Location for a Phone Number
*E911Api* | [**v1E911PhoneNumberLocationGet**](docs/Api/E911Api.md#v1e911phonenumberlocationget) | **GET** /v1/e911/{phoneNumber}/location | Get Location List for Phone Number
*E911Api* | [**v1E911Post**](docs/Api/E911Api.md#v1e911post) | **POST** /v1/e911 | Create an E911 Location
*GroupApi* | [**v1AccountAccountIDGroupGet**](docs/Api/GroupApi.md#v1accountaccountidgroupget) | **GET** /v1/account/{accountID}/group | Get Group List
*GroupApi* | [**v1AccountAccountIDGroupGroupIDDelete**](docs/Api/GroupApi.md#v1accountaccountidgroupgroupiddelete) | **DELETE** /v1/account/{accountID}/group/{groupID} | Delete Group
*GroupApi* | [**v1AccountAccountIDGroupGroupIDGet**](docs/Api/GroupApi.md#v1accountaccountidgroupgroupidget) | **GET** /v1/account/{accountID}/group/{groupID} | Get Group Details
*GroupApi* | [**v1AccountAccountIDGroupGroupIDPut**](docs/Api/GroupApi.md#v1accountaccountidgroupgroupidput) | **PUT** /v1/account/{accountID}/group/{groupID} | Update Group
*GroupApi* | [**v1AccountAccountIDGroupPost**](docs/Api/GroupApi.md#v1accountaccountidgrouppost) | **POST** /v1/account/{accountID}/group | Create Group
*MediaApi* | [**v1AccountAccountIDMediaMediaIDFileGet**](docs/Api/MediaApi.md#v1accountaccountidmediamediaidfileget) | **GET** /v1/account/{accountID}/media/{mediaID}/file | Get Media File
*MediaApi* | [**v1AccountAccountIDMediaMediaIDFilePost**](docs/Api/MediaApi.md#v1accountaccountidmediamediaidfilepost) | **POST** /v1/account/{accountID}/media/{mediaID}/file | Add Media File
*MediaApi* | [**v1AccountAccountidMediaGet**](docs/Api/MediaApi.md#v1accountaccountidmediaget) | **GET** /v1/account/{accountid}/media | Get Media List
*MediaApi* | [**v1AccountAccountidMediaMediaidDelete**](docs/Api/MediaApi.md#v1accountaccountidmediamediaiddelete) | **DELETE** /v1/account/{accountid}/media/{mediaid} | Delete Media
*MediaApi* | [**v1AccountAccountidMediaMediaidGet**](docs/Api/MediaApi.md#v1accountaccountidmediamediaidget) | **GET** /v1/account/{accountid}/media/{mediaid} | Get Media Details
*MediaApi* | [**v1AccountAccountidMediaPost**](docs/Api/MediaApi.md#v1accountaccountidmediapost) | **POST** /v1/account/{accountid}/media | Create Media
*MenuApi* | [**v1AccountAccountIDMenuGet**](docs/Api/MenuApi.md#v1accountaccountidmenuget) | **GET** /v1/account/{accountID}/menu | Get Menu List
*MenuApi* | [**v1AccountAccountIDMenuMenuIDDelete**](docs/Api/MenuApi.md#v1accountaccountidmenumenuiddelete) | **DELETE** /v1/account/{accountID}/menu/{menuID} | Delete Menu
*MenuApi* | [**v1AccountAccountIDMenuMenuIDGet**](docs/Api/MenuApi.md#v1accountaccountidmenumenuidget) | **GET** /v1/account/{accountID}/menu/{menuID} | Get Menu Details
*MenuApi* | [**v1AccountAccountIDMenuMenuIDPut**](docs/Api/MenuApi.md#v1accountaccountidmenumenuidput) | **PUT** /v1/account/{accountID}/menu/{menuID} | Update Menu
*MenuApi* | [**v1AccountAccountIDMenuPost**](docs/Api/MenuApi.md#v1accountaccountidmenupost) | **POST** /v1/account/{accountID}/menu | Create Menu
*MetaflowApi* | [**v1AccountAccountIDDeviceDeviceIDMetaflowDelete**](docs/Api/MetaflowApi.md#v1accountaccountiddevicedeviceidmetaflowdelete) | **DELETE** /v1/account/{accountID}/device/{deviceID}/metaflow | Delete Device Metaflow
*MetaflowApi* | [**v1AccountAccountIDDeviceDeviceIDMetaflowGet**](docs/Api/MetaflowApi.md#v1accountaccountiddevicedeviceidmetaflowget) | **GET** /v1/account/{accountID}/device/{deviceID}/metaflow | Get Device Metaflow List
*MetaflowApi* | [**v1AccountAccountIDDeviceDeviceIDMetaflowPost**](docs/Api/MetaflowApi.md#v1accountaccountiddevicedeviceidmetaflowpost) | **POST** /v1/account/{accountID}/device/{deviceID}/metaflow | Create Device Metaflow
*MetaflowApi* | [**v1AccountAccountIDMetaflowDelete**](docs/Api/MetaflowApi.md#v1accountaccountidmetaflowdelete) | **DELETE** /v1/account/{accountID}/metaflow | Delete Account Metaflow
*MetaflowApi* | [**v1AccountAccountIDMetaflowGet**](docs/Api/MetaflowApi.md#v1accountaccountidmetaflowget) | **GET** /v1/account/{accountID}/metaflow | Get Account Metaflow List
*MetaflowApi* | [**v1AccountAccountIDMetaflowPost**](docs/Api/MetaflowApi.md#v1accountaccountidmetaflowpost) | **POST** /v1/account/{accountID}/metaflow | Create Account Metaflow
*MetaflowApi* | [**v1AccountAccountIDUserUserIDMetaflowDelete**](docs/Api/MetaflowApi.md#v1accountaccountiduseruseridmetaflowdelete) | **DELETE** /v1/account/{accountID}/user/{userID}/metaflow | Delete User Metaflow
*MetaflowApi* | [**v1AccountAccountIDUserUserIDMetaflowGet**](docs/Api/MetaflowApi.md#v1accountaccountiduseruseridmetaflowget) | **GET** /v1/account/{accountID}/user/{userID}/metaflow | Get User Metaflow List
*MetaflowApi* | [**v1AccountAccountIDUserUserIDMetaflowPost**](docs/Api/MetaflowApi.md#v1accountaccountiduseruseridmetaflowpost) | **POST** /v1/account/{accountID}/user/{userID}/metaflow | Create User Metaflow
*PhoneNumberApi* | [**v1AccountAccountidPhonenumberGet**](docs/Api/PhoneNumberApi.md#v1accountaccountidphonenumberget) | **GET** /v1/account/{accountid}/phonenumber | Get Assigned Numbers List
*PhoneNumberApi* | [**v1AccountPhonenumberAssignPost**](docs/Api/PhoneNumberApi.md#v1accountphonenumberassignpost) | **POST** /v1/account/phonenumber/assign | Assign Number
*PhoneNumberApi* | [**v1AccountPhonenumberDisconnectPost**](docs/Api/PhoneNumberApi.md#v1accountphonenumberdisconnectpost) | **POST** /v1/account/phonenumber/disconnect | Disconnect Number
*PhoneNumberApi* | [**v1AccountPhonenumberGet**](docs/Api/PhoneNumberApi.md#v1accountphonenumberget) | **GET** /v1/account/phonenumber | Get Unassigned Numbers List
*PhoneNumberApi* | [**v1AccountPhonenumberPost**](docs/Api/PhoneNumberApi.md#v1accountphonenumberpost) | **POST** /v1/account/phonenumber | Purchase Number
*PhoneNumberApi* | [**v1AccountPhonenumberUnassignPost**](docs/Api/PhoneNumberApi.md#v1accountphonenumberunassignpost) | **POST** /v1/account/phonenumber/unassign | Unassign Number
*PhoneNumberApi* | [**v1PhonenumberSearchGet**](docs/Api/PhoneNumberApi.md#v1phonenumbersearchget) | **GET** /v1/phonenumber/search | Search New Numbers
*PresenceApi* | [**v1AccountAccountIDPresenceExtensionPut**](docs/Api/PresenceApi.md#v1accountaccountidpresenceextensionput) | **PUT** /v1/account/{accountID}/presence/{extension} | Set/Reset Presence for Extension
*PresenceApi* | [**v1AccountAccountIDPresenceGet**](docs/Api/PresenceApi.md#v1accountaccountidpresenceget) | **GET** /v1/account/{accountID}/presence | Get Presence Details
*PresenceApi* | [**v1AccountAccountIDUserUserIDPresencePut**](docs/Api/PresenceApi.md#v1accountaccountiduseruseridpresenceput) | **PUT** /v1/account/{accountID}/user/{userID}/presence | Set/Reset Presence for User
*ProvisioningApi* | [**v1AccountAccountIDProvisionFilenameGet**](docs/Api/ProvisioningApi.md#v1accountaccountidprovisionfilenameget) | **GET** /v1/account/{accountID}/provision/{filename} | Get Config File Details
*ProvisioningApi* | [**v1ApBrandBrandFamilyFamilyGet**](docs/Api/ProvisioningApi.md#v1apbrandbrandfamilyfamilyget) | **GET** /v1/ap/brand/{brand}/family/{family} | Get Family Details
*ProvisioningApi* | [**v1ApBrandBrandFamilyFamilyModelGet**](docs/Api/ProvisioningApi.md#v1apbrandbrandfamilyfamilymodelget) | **GET** /v1/ap/brand/{brand}/family/{family}/model | Get Model List
*ProvisioningApi* | [**v1ApBrandBrandFamilyFamilyModelModelGet**](docs/Api/ProvisioningApi.md#v1apbrandbrandfamilyfamilymodelmodelget) | **GET** /v1/ap/brand/{brand}/family/{family}/model/{model} | Get Model Details
*ProvisioningApi* | [**v1ApBrandBrandFamilyFamilyModelModelTemplateGet**](docs/Api/ProvisioningApi.md#v1apbrandbrandfamilyfamilymodelmodeltemplateget) | **GET** /v1/ap/brand/{brand}/family/{family}/model/{model}/template | Get Template List
*ProvisioningApi* | [**v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet**](docs/Api/ProvisioningApi.md#v1apbrandbrandfamilyfamilymodelmodeltemplatetemplateget) | **GET** /v1/ap/brand/{brand}/family/{family}/model/{model}/template/{template} | Get Template Details
*ProvisioningApi* | [**v1ApBrandBrandFamilyGet**](docs/Api/ProvisioningApi.md#v1apbrandbrandfamilyget) | **GET** /v1/ap/brand/{brand}/family | Get Family List
*ProvisioningApi* | [**v1ApBrandBrandGet**](docs/Api/ProvisioningApi.md#v1apbrandbrandget) | **GET** /v1/ap/brand/{brand} | Get Brand Details
*ProvisioningApi* | [**v1ApBrandGet**](docs/Api/ProvisioningApi.md#v1apbrandget) | **GET** /v1/ap/brand | Get Brand List
*ProvisioningApi* | [**v1ApConfigfileGeneratePost**](docs/Api/ProvisioningApi.md#v1apconfigfilegeneratepost) | **POST** /v1/ap/configfile/generate | Generate Config File
*SMSApi* | [**v1SmsAccountAccountIDCampaignCampaignIDImportGet**](docs/Api/SMSApi.md#v1smsaccountaccountidcampaigncampaignidimportget) | **GET** /v1/sms/account/{accountID}/campaign/{campaignID}/import | 
*SMSApi* | [**v1SmsAccountAccountIDCampaignCampaignIDImportPost**](docs/Api/SMSApi.md#v1smsaccountaccountidcampaigncampaignidimportpost) | **POST** /v1/sms/account/{accountID}/campaign/{campaignID}/import | 
*SMSApi* | [**v1SmsAccountAccountIDCampaignCampaignIDPhonenumberGet**](docs/Api/SMSApi.md#v1smsaccountaccountidcampaigncampaignidphonenumberget) | **GET** /v1/sms/account/{accountID}/campaign/{campaignID}/phonenumber | 
*SMSApi* | [**v1SmsAccountAccountIDCampaignCampaignIDPhonenumberPut**](docs/Api/SMSApi.md#v1smsaccountaccountidcampaigncampaignidphonenumberput) | **PUT** /v1/sms/account/{accountID}/campaign/{campaignID}/phonenumber | 
*SMSApi* | [**v1SmsAccountAccountIDCampaignImportGet**](docs/Api/SMSApi.md#v1smsaccountaccountidcampaignimportget) | **GET** /v1/sms/account/{accountID}/campaign/import | 
*StorageApi* | [**v1AccountAccountIDStorageDelete**](docs/Api/StorageApi.md#v1accountaccountidstoragedelete) | **DELETE** /v1/account/{accountID}/storage | Delete Storage
*StorageApi* | [**v1AccountAccountIDStorageGet**](docs/Api/StorageApi.md#v1accountaccountidstorageget) | **GET** /v1/account/{accountID}/storage | Get Storage Details
*StorageApi* | [**v1AccountAccountIDStoragePost**](docs/Api/StorageApi.md#v1accountaccountidstoragepost) | **POST** /v1/account/{accountID}/storage | Create Storage
*StorageApi* | [**v1AccountAccountIDStoragePut**](docs/Api/StorageApi.md#v1accountaccountidstorageput) | **PUT** /v1/account/{accountID}/storage | Update Storage
*SystemStatusApi* | [**v1ApPingGet**](docs/Api/SystemStatusApi.md#v1appingget) | **GET** /v1/ap/ping | Provisioning Ping
*SystemStatusApi* | [**v1PingGet**](docs/Api/SystemStatusApi.md#v1pingget) | **GET** /v1/ping | Ping Backend
*SystemStatusApi* | [**v1PingseccognitoGet**](docs/Api/SystemStatusApi.md#v1pingseccognitoget) | **GET** /v1/pingseccognito | Ping Cognito
*SystemStatusApi* | [**v1SystemStatusGet**](docs/Api/SystemStatusApi.md#v1systemstatusget) | **GET** /v1/system_status | Get System Status
*TemporalRuleApi* | [**v1AccountAccountIDTemporalruleGet**](docs/Api/TemporalRuleApi.md#v1accountaccountidtemporalruleget) | **GET** /v1/account/{accountID}/temporalrule | Get Temporal Rule List
*TemporalRuleApi* | [**v1AccountAccountIDTemporalrulePost**](docs/Api/TemporalRuleApi.md#v1accountaccountidtemporalrulepost) | **POST** /v1/account/{accountID}/temporalrule | Create Temporal Rule
*TemporalRuleApi* | [**v1AccountAccountIDTemporalruleTemporalRuleIDDelete**](docs/Api/TemporalRuleApi.md#v1accountaccountidtemporalruletemporalruleiddelete) | **DELETE** /v1/account/{accountID}/temporalrule/{temporalRuleID} | Delete Temporal Rule
*TemporalRuleApi* | [**v1AccountAccountIDTemporalruleTemporalRuleIDGet**](docs/Api/TemporalRuleApi.md#v1accountaccountidtemporalruletemporalruleidget) | **GET** /v1/account/{accountID}/temporalrule/{temporalRuleID} | Get Temporal Rule Details
*TemporalRuleApi* | [**v1AccountAccountIDTemporalruleTemporalRuleIDPut**](docs/Api/TemporalRuleApi.md#v1accountaccountidtemporalruletemporalruleidput) | **PUT** /v1/account/{accountID}/temporalrule/{temporalRuleID} | Update Temporal Rule
*TemporalRuleSetApi* | [**v1AccountAccountIDTemporalrulesetGet**](docs/Api/TemporalRuleSetApi.md#v1accountaccountidtemporalrulesetget) | **GET** /v1/account/{accountID}/temporalruleset | Get Temporal Rule Set List
*TemporalRuleSetApi* | [**v1AccountAccountIDTemporalrulesetPost**](docs/Api/TemporalRuleSetApi.md#v1accountaccountidtemporalrulesetpost) | **POST** /v1/account/{accountID}/temporalruleset | Create Temporal Rule Set
*TemporalRuleSetApi* | [**v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete**](docs/Api/TemporalRuleSetApi.md#v1accountaccountidtemporalrulesettemporalrulesetiddelete) | **DELETE** /v1/account/{accountID}/temporalruleset/{temporalRuleSetID} | Delete Temporal Rule Set
*TemporalRuleSetApi* | [**v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet**](docs/Api/TemporalRuleSetApi.md#v1accountaccountidtemporalrulesettemporalrulesetidget) | **GET** /v1/account/{accountID}/temporalruleset/{temporalRuleSetID} | Get Temporal Rule Set Details
*TemporalRuleSetApi* | [**v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut**](docs/Api/TemporalRuleSetApi.md#v1accountaccountidtemporalrulesettemporalrulesetidput) | **PUT** /v1/account/{accountID}/temporalruleset/{temporalRuleSetID} | Update Temporal Rule Set
*VoIPUserApi* | [**v1AccountAccountidUserGet**](docs/Api/VoIPUserApi.md#v1accountaccountiduserget) | **GET** /v1/account/{accountid}/user | Get User List
*VoIPUserApi* | [**v1AccountAccountidUserPost**](docs/Api/VoIPUserApi.md#v1accountaccountiduserpost) | **POST** /v1/account/{accountid}/user | Create User
*VoIPUserApi* | [**v1AccountAccountidUserUseridDelete**](docs/Api/VoIPUserApi.md#v1accountaccountiduseruseriddelete) | **DELETE** /v1/account/{accountid}/user/{userid} | Delete User
*VoIPUserApi* | [**v1AccountAccountidUserUseridGet**](docs/Api/VoIPUserApi.md#v1accountaccountiduseruseridget) | **GET** /v1/account/{accountid}/user/{userid} | Get User Details
*VoIPUserApi* | [**v1AccountAccountidUserUseridPut**](docs/Api/VoIPUserApi.md#v1accountaccountiduseruseridput) | **PUT** /v1/account/{accountid}/user/{userid} | Update User
*VoIPUserApi* | [**v1AccountAccountidUserUseridUserauthPost**](docs/Api/VoIPUserApi.md#v1accountaccountiduseruseriduserauthpost) | **POST** /v1/account/{accountid}/user/{userid}/userauth | Impersonate a User
*VoicemailApi* | [**v1AccountAccountIDVoicemailGet**](docs/Api/VoicemailApi.md#v1accountaccountidvoicemailget) | **GET** /v1/account/{accountID}/voicemail | Get Voicemail Box List
*VoicemailApi* | [**v1AccountAccountIDVoicemailPost**](docs/Api/VoicemailApi.md#v1accountaccountidvoicemailpost) | **POST** /v1/account/{accountID}/voicemail | Create Voicemail Box
*VoicemailApi* | [**v1AccountAccountIDVoicemailVoicemailIDDelete**](docs/Api/VoicemailApi.md#v1accountaccountidvoicemailvoicemailiddelete) | **DELETE** /v1/account/{accountID}/voicemail/{voicemailID} | Delete Voicemail Box
*VoicemailApi* | [**v1AccountAccountIDVoicemailVoicemailIDGet**](docs/Api/VoicemailApi.md#v1accountaccountidvoicemailvoicemailidget) | **GET** /v1/account/{accountID}/voicemail/{voicemailID} | Get Voicemail Box Details
*VoicemailApi* | [**v1AccountAccountIDVoicemailVoicemailIDMessageGet**](docs/Api/VoicemailApi.md#v1accountaccountidvoicemailvoicemailidmessageget) | **GET** /v1/account/{accountID}/voicemail/{voicemailID}/message | Get Voicemail Message List
*VoicemailApi* | [**v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDDelete**](docs/Api/VoicemailApi.md#v1accountaccountidvoicemailvoicemailidmessagemessageiddelete) | **DELETE** /v1/account/{accountID}/voicemail/{voicemailID}/message/{messageID} | Delete Voicemail Message
*VoicemailApi* | [**v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDGet**](docs/Api/VoicemailApi.md#v1accountaccountidvoicemailvoicemailidmessagemessageidget) | **GET** /v1/account/{accountID}/voicemail/{voicemailID}/message/{messageID} | Get Voicemail Message Details
*VoicemailApi* | [**v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDPut**](docs/Api/VoicemailApi.md#v1accountaccountidvoicemailvoicemailidmessagemessageidput) | **PUT** /v1/account/{accountID}/voicemail/{voicemailID}/message/{messageID} | Update Voicemail Message
*VoicemailApi* | [**v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawGet**](docs/Api/VoicemailApi.md#v1accountaccountidvoicemailvoicemailidmessagemessageidrawget) | **GET** /v1/account/{accountID}/voicemail/{voicemailID}/message/{messageID}/raw | Get Voicemail Message File
*VoicemailApi* | [**v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawPost**](docs/Api/VoicemailApi.md#v1accountaccountidvoicemailvoicemailidmessagemessageidrawpost) | **POST** /v1/account/{accountID}/voicemail/{voicemailID}/message/{messageID}/raw | Add Voicemail Message File
*VoicemailApi* | [**v1AccountAccountIDVoicemailVoicemailIDMessagePost**](docs/Api/VoicemailApi.md#v1accountaccountidvoicemailvoicemailidmessagepost) | **POST** /v1/account/{accountID}/voicemail/{voicemailID}/message | Create Voicemail Message
*VoicemailApi* | [**v1AccountAccountIDVoicemailVoicemailIDPut**](docs/Api/VoicemailApi.md#v1accountaccountidvoicemailvoicemailidput) | **PUT** /v1/account/{accountID}/voicemail/{voicemailID} | Update Voicemail Box
*WebhookApi* | [**v1WebhookAccountAccountIDGet**](docs/Api/WebhookApi.md#v1webhookaccountaccountidget) | **GET** /v1/webhook/account/{accountID} | Get Webhook List
*WebhookApi* | [**v1WebhookAccountAccountIDPost**](docs/Api/WebhookApi.md#v1webhookaccountaccountidpost) | **POST** /v1/webhook/account/{accountID} | Create Webhook
*WebhookApi* | [**v1WebhookAccountAccountIDWebhookIDDelete**](docs/Api/WebhookApi.md#v1webhookaccountaccountidwebhookiddelete) | **DELETE** /v1/webhook/account/{accountID}/{webhookID} | Delete Webhook
*WebhookApi* | [**v1WebhookAccountAccountIDWebhookIDGet**](docs/Api/WebhookApi.md#v1webhookaccountaccountidwebhookidget) | **GET** /v1/webhook/account/{accountID}/{webhookID} | Get Webhook Details
*WebhookApi* | [**v1WebhookAccountAccountIDWebhookIDPut**](docs/Api/WebhookApi.md#v1webhookaccountaccountidwebhookidput) | **PUT** /v1/webhook/account/{accountID}/{webhookID} | Update Webhook

## Models

- [CPAASError](docs/Model/CPAASError.md)
- [MenuInputData](docs/Model/MenuInputData.md)
- [MenuOutputDetail](docs/Model/MenuOutputDetail.md)
- [MenuOutputDetailData](docs/Model/MenuOutputDetailData.md)
- [MenuOutputDetailMedia](docs/Model/MenuOutputDetailMedia.md)
- [MenuOutputList](docs/Model/MenuOutputList.md)
- [MenuOutputListData](docs/Model/MenuOutputListData.md)
- [ModelAccountProvisioning](docs/Model/ModelAccountProvisioning.md)
- [ModelAccountWebhook](docs/Model/ModelAccountWebhook.md)
- [ModelCallDailySummary](docs/Model/ModelCallDailySummary.md)
- [ModelCallDetail](docs/Model/ModelCallDetail.md)
- [ModelCallMonthlySummary](docs/Model/ModelCallMonthlySummary.md)
- [ModelEndpointList](docs/Model/ModelEndpointList.md)
- [ModelEventDailySummary](docs/Model/ModelEventDailySummary.md)
- [ModelEventDetail](docs/Model/ModelEventDetail.md)
- [ModelEventMonthlySummary](docs/Model/ModelEventMonthlySummary.md)
- [ModelFeatureDailySummary](docs/Model/ModelFeatureDailySummary.md)
- [ModelFeatureMonthlySummary](docs/Model/ModelFeatureMonthlySummary.md)
- [ModelsAccountOutputFull](docs/Model/ModelsAccountOutputFull.md)
- [ModelsAccountOutputFullCalleridEmergency](docs/Model/ModelsAccountOutputFullCalleridEmergency.md)
- [ModelsAccountOutputFullCalleridExternal](docs/Model/ModelsAccountOutputFullCalleridExternal.md)
- [ModelsAccountOutputFullCalleridInternal](docs/Model/ModelsAccountOutputFullCalleridInternal.md)
- [ModelsBrand](docs/Model/ModelsBrand.md)
- [ModelsCallForward](docs/Model/ModelsCallForward.md)
- [ModelsCallRecordingParameters](docs/Model/ModelsCallRecordingParameters.md)
- [ModelsCallRecordingSettings](docs/Model/ModelsCallRecordingSettings.md)
- [ModelsCallRecordingSource](docs/Model/ModelsCallRecordingSource.md)
- [ModelsConfigFileParameter](docs/Model/ModelsConfigFileParameter.md)
- [ModelsDeviceOutputFull](docs/Model/ModelsDeviceOutputFull.md)
- [ModelsDeviceOutputFullCallerid](docs/Model/ModelsDeviceOutputFullCallerid.md)
- [ModelsDeviceOutputFullCalleridEmergency](docs/Model/ModelsDeviceOutputFullCalleridEmergency.md)
- [ModelsDeviceOutputFullCalleridExternal](docs/Model/ModelsDeviceOutputFullCalleridExternal.md)
- [ModelsDeviceOutputFullCalleridInternal](docs/Model/ModelsDeviceOutputFullCalleridInternal.md)
- [ModelsDeviceOutputFullMedia](docs/Model/ModelsDeviceOutputFullMedia.md)
- [ModelsDeviceOutputFullMediaAudio](docs/Model/ModelsDeviceOutputFullMediaAudio.md)
- [ModelsDeviceOutputFullProvision](docs/Model/ModelsDeviceOutputFullProvision.md)
- [ModelsDeviceOutputFullSIP](docs/Model/ModelsDeviceOutputFullSIP.md)
- [ModelsFamily](docs/Model/ModelsFamily.md)
- [ModelsGenerateConfigFileRequest](docs/Model/ModelsGenerateConfigFileRequest.md)
- [ModelsModel](docs/Model/ModelsModel.md)
- [ModelsMusicOnHold](docs/Model/ModelsMusicOnHold.md)
- [ModelsTemplate](docs/Model/ModelsTemplate.md)
- [ModelsUserOutputFull](docs/Model/ModelsUserOutputFull.md)
- [ModelsUserOutputFullCallerid](docs/Model/ModelsUserOutputFullCallerid.md)
- [ModelsUserOutputFullCalleridEmergency](docs/Model/ModelsUserOutputFullCalleridEmergency.md)
- [ModelsUserOutputFullCalleridExternal](docs/Model/ModelsUserOutputFullCalleridExternal.md)
- [ModelsUserOutputFullCalleridInternal](docs/Model/ModelsUserOutputFullCalleridInternal.md)
- [ModelsVOIPAccountMusicOnHold](docs/Model/ModelsVOIPAccountMusicOnHold.md)
- [ModelsVOIPAccountOutputFullCallerid](docs/Model/ModelsVOIPAccountOutputFullCallerid.md)
- [ModelsVOIPDeviceOutputLineKey](docs/Model/ModelsVOIPDeviceOutputLineKey.md)
- [ModelsVOIPSharedDoNotDisturb](docs/Model/ModelsVOIPSharedDoNotDisturb.md)
- [ProvisioningDocsDocsBrandOutputSingle](docs/Model/ProvisioningDocsDocsBrandOutputSingle.md)
- [ProvisioningDocsDocsBrandsOutput](docs/Model/ProvisioningDocsDocsBrandsOutput.md)
- [ProvisioningDocsDocsConfigFileOutput](docs/Model/ProvisioningDocsDocsConfigFileOutput.md)
- [ProvisioningDocsDocsFamilyOutput](docs/Model/ProvisioningDocsDocsFamilyOutput.md)
- [ProvisioningDocsDocsFamilyOutputSingle](docs/Model/ProvisioningDocsDocsFamilyOutputSingle.md)
- [ProvisioningDocsDocsModelOutput](docs/Model/ProvisioningDocsDocsModelOutput.md)
- [ProvisioningDocsDocsModelOutputSingle](docs/Model/ProvisioningDocsDocsModelOutputSingle.md)
- [ProvisioningDocsDocsPingOutput](docs/Model/ProvisioningDocsDocsPingOutput.md)
- [ProvisioningDocsDocsPingOutputData](docs/Model/ProvisioningDocsDocsPingOutputData.md)
- [ProvisioningDocsDocsTemplateOutputSingle](docs/Model/ProvisioningDocsDocsTemplateOutputSingle.md)
- [ProvisioningDocsDocsTemplatesOutput](docs/Model/ProvisioningDocsDocsTemplatesOutput.md)
- [RepositoryLocationsResponse](docs/Model/RepositoryLocationsResponse.md)
- [ResponseProvisionError](docs/Model/ResponseProvisionError.md)
- [ServiceAPIKey](docs/Model/ServiceAPIKey.md)
- [ServiceAPIResponse](docs/Model/ServiceAPIResponse.md)
- [ServiceAPIResponseStatusCodeOnly](docs/Model/ServiceAPIResponseStatusCodeOnly.md)
- [ServiceAccountLimitOutput](docs/Model/ServiceAccountLimitOutput.md)
- [ServiceAccountOutputShort](docs/Model/ServiceAccountOutputShort.md)
- [ServiceAdminUserAddData](docs/Model/ServiceAdminUserAddData.md)
- [ServiceAdminUserDeleteOutput](docs/Model/ServiceAdminUserDeleteOutput.md)
- [ServiceAdminUserEditData](docs/Model/ServiceAdminUserEditData.md)
- [ServiceAdminUserOutput](docs/Model/ServiceAdminUserOutput.md)
- [ServiceCallQueueOutputFull](docs/Model/ServiceCallQueueOutputFull.md)
- [ServiceCallQueueOutputShort](docs/Model/ServiceCallQueueOutputShort.md)
- [ServiceCallQueueRolesOutput](docs/Model/ServiceCallQueueRolesOutput.md)
- [ServiceCallQueueStatusOutput](docs/Model/ServiceCallQueueStatusOutput.md)
- [ServiceCallQueueStatusStats](docs/Model/ServiceCallQueueStatusStats.md)
- [ServiceCallRecordingOutput](docs/Model/ServiceCallRecordingOutput.md)
- [ServiceCallflowAddEditData](docs/Model/ServiceCallflowAddEditData.md)
- [ServiceCallflowAddEditFlowData](docs/Model/ServiceCallflowAddEditFlowData.md)
- [ServiceCallflowOutputFull](docs/Model/ServiceCallflowOutputFull.md)
- [ServiceCallflowOutputShort](docs/Model/ServiceCallflowOutputShort.md)
- [ServiceCampaignImportOutput](docs/Model/ServiceCampaignImportOutput.md)
- [ServiceCampaignImportOutputMnoStatusListInner](docs/Model/ServiceCampaignImportOutputMnoStatusListInner.md)
- [ServiceCampaignPhoneNumberOutput](docs/Model/ServiceCampaignPhoneNumberOutput.md)
- [ServiceCampaignTagDetagPhonenumbers](docs/Model/ServiceCampaignTagDetagPhonenumbers.md)
- [ServiceCampaignTagDetagPhonenumbersOutput](docs/Model/ServiceCampaignTagDetagPhonenumbersOutput.md)
- [ServiceCdrOutputShort](docs/Model/ServiceCdrOutputShort.md)
- [ServiceChannelOutput](docs/Model/ServiceChannelOutput.md)
- [ServiceDeviceOutputShort](docs/Model/ServiceDeviceOutputShort.md)
- [ServiceDeviceStatusOutput](docs/Model/ServiceDeviceStatusOutput.md)
- [ServiceDocGroupGetAll](docs/Model/ServiceDocGroupGetAll.md)
- [ServiceDocGroupGetSingle](docs/Model/ServiceDocGroupGetSingle.md)
- [ServiceDocsAccountAPIKey](docs/Model/ServiceDocsAccountAPIKey.md)
- [ServiceDocsAccountGetAll](docs/Model/ServiceDocsAccountGetAll.md)
- [ServiceDocsAccountGetSingle](docs/Model/ServiceDocsAccountGetSingle.md)
- [ServiceDocsAccountLimit](docs/Model/ServiceDocsAccountLimit.md)
- [ServiceDocsAccountPhonenumberGetAll](docs/Model/ServiceDocsAccountPhonenumberGetAll.md)
- [ServiceDocsAccountProvisioning](docs/Model/ServiceDocsAccountProvisioning.md)
- [ServiceDocsAdminUserDelete](docs/Model/ServiceDocsAdminUserDelete.md)
- [ServiceDocsAdminUserGetAll](docs/Model/ServiceDocsAdminUserGetAll.md)
- [ServiceDocsAdminUserGetSingle](docs/Model/ServiceDocsAdminUserGetSingle.md)
- [ServiceDocsCallDailySummary](docs/Model/ServiceDocsCallDailySummary.md)
- [ServiceDocsCallDetail](docs/Model/ServiceDocsCallDetail.md)
- [ServiceDocsCallMonthlySummary](docs/Model/ServiceDocsCallMonthlySummary.md)
- [ServiceDocsCallQueueGetAll](docs/Model/ServiceDocsCallQueueGetAll.md)
- [ServiceDocsCallQueueGetRoles](docs/Model/ServiceDocsCallQueueGetRoles.md)
- [ServiceDocsCallQueueGetSingle](docs/Model/ServiceDocsCallQueueGetSingle.md)
- [ServiceDocsCallQueueGetSingleStatus](docs/Model/ServiceDocsCallQueueGetSingleStatus.md)
- [ServiceDocsCallQueueRecipientLoginLogoutOutput](docs/Model/ServiceDocsCallQueueRecipientLoginLogoutOutput.md)
- [ServiceDocsCallRecordingGetAll](docs/Model/ServiceDocsCallRecordingGetAll.md)
- [ServiceDocsCallRecordingGetSingle](docs/Model/ServiceDocsCallRecordingGetSingle.md)
- [ServiceDocsCallflowGetAll](docs/Model/ServiceDocsCallflowGetAll.md)
- [ServiceDocsCallflowGetSingle](docs/Model/ServiceDocsCallflowGetSingle.md)
- [ServiceDocsCallparkGet](docs/Model/ServiceDocsCallparkGet.md)
- [ServiceDocsCampaignImportOutput](docs/Model/ServiceDocsCampaignImportOutput.md)
- [ServiceDocsCampaignImportedGetAllOutput](docs/Model/ServiceDocsCampaignImportedGetAllOutput.md)
- [ServiceDocsCampaignPhoneNumberOutput](docs/Model/ServiceDocsCampaignPhoneNumberOutput.md)
- [ServiceDocsCampaignTagDetagPhonenumbersOutput](docs/Model/ServiceDocsCampaignTagDetagPhonenumbersOutput.md)
- [ServiceDocsCdrGetAll](docs/Model/ServiceDocsCdrGetAll.md)
- [ServiceDocsCdrGetSingle](docs/Model/ServiceDocsCdrGetSingle.md)
- [ServiceDocsChannelGetAll](docs/Model/ServiceDocsChannelGetAll.md)
- [ServiceDocsChannelGetSingle](docs/Model/ServiceDocsChannelGetSingle.md)
- [ServiceDocsDeviceGetAll](docs/Model/ServiceDocsDeviceGetAll.md)
- [ServiceDocsDeviceGetSingle](docs/Model/ServiceDocsDeviceGetSingle.md)
- [ServiceDocsDeviceReboot](docs/Model/ServiceDocsDeviceReboot.md)
- [ServiceDocsDeviceStatus](docs/Model/ServiceDocsDeviceStatus.md)
- [ServiceDocsE911ActiveLocationOutput](docs/Model/ServiceDocsE911ActiveLocationOutput.md)
- [ServiceDocsE911ActiveLocationURIApiOutput](docs/Model/ServiceDocsE911ActiveLocationURIApiOutput.md)
- [ServiceDocsE911AddLocationOutput](docs/Model/ServiceDocsE911AddLocationOutput.md)
- [ServiceDocsE911LocationsURIApiOutput](docs/Model/ServiceDocsE911LocationsURIApiOutput.md)
- [ServiceDocsE911RemoveLocationOutput](docs/Model/ServiceDocsE911RemoveLocationOutput.md)
- [ServiceDocsE911RemoveURIApiOutput](docs/Model/ServiceDocsE911RemoveURIApiOutput.md)
- [ServiceDocsE911URIsApiOutput](docs/Model/ServiceDocsE911URIsApiOutput.md)
- [ServiceDocsE911ValidateLocationOutput](docs/Model/ServiceDocsE911ValidateLocationOutput.md)
- [ServiceDocsEndpointList](docs/Model/ServiceDocsEndpointList.md)
- [ServiceDocsEventDailySummary](docs/Model/ServiceDocsEventDailySummary.md)
- [ServiceDocsEventDetail](docs/Model/ServiceDocsEventDetail.md)
- [ServiceDocsEventMonthlySummary](docs/Model/ServiceDocsEventMonthlySummary.md)
- [ServiceDocsFeatureDailySummary](docs/Model/ServiceDocsFeatureDailySummary.md)
- [ServiceDocsFeatureMonthlySummary](docs/Model/ServiceDocsFeatureMonthlySummary.md)
- [ServiceDocsGetQueueRecipients](docs/Model/ServiceDocsGetQueueRecipients.md)
- [ServiceDocsImpersonateUserGetSingle](docs/Model/ServiceDocsImpersonateUserGetSingle.md)
- [ServiceDocsMediaGetAll](docs/Model/ServiceDocsMediaGetAll.md)
- [ServiceDocsMediaGetSingle](docs/Model/ServiceDocsMediaGetSingle.md)
- [ServiceDocsMetaflowGet](docs/Model/ServiceDocsMetaflowGet.md)
- [ServiceDocsOrderPhonenumber](docs/Model/ServiceDocsOrderPhonenumber.md)
- [ServiceDocsPhonenumberAssignPayload](docs/Model/ServiceDocsPhonenumberAssignPayload.md)
- [ServiceDocsPhonenumberSearchGetAll](docs/Model/ServiceDocsPhonenumberSearchGetAll.md)
- [ServiceDocsPhonenumberUnassignPayload](docs/Model/ServiceDocsPhonenumberUnassignPayload.md)
- [ServiceDocsPingGet](docs/Model/ServiceDocsPingGet.md)
- [ServiceDocsPresenceGet](docs/Model/ServiceDocsPresenceGet.md)
- [ServiceDocsQueueMembershipOutput](docs/Model/ServiceDocsQueueMembershipOutput.md)
- [ServiceDocsStorageGet](docs/Model/ServiceDocsStorageGet.md)
- [ServiceDocsSystemStatusGetSingle](docs/Model/ServiceDocsSystemStatusGetSingle.md)
- [ServiceDocsTemporalRuleGetAll](docs/Model/ServiceDocsTemporalRuleGetAll.md)
- [ServiceDocsTemporalRuleGetSingle](docs/Model/ServiceDocsTemporalRuleGetSingle.md)
- [ServiceDocsTemporalRuleSetGetAll](docs/Model/ServiceDocsTemporalRuleSetGetAll.md)
- [ServiceDocsTemporalRuleSetGetSingle](docs/Model/ServiceDocsTemporalRuleSetGetSingle.md)
- [ServiceDocsUserGetAll](docs/Model/ServiceDocsUserGetAll.md)
- [ServiceDocsUserGetSingle](docs/Model/ServiceDocsUserGetSingle.md)
- [ServiceDocsVoicemailGetAll](docs/Model/ServiceDocsVoicemailGetAll.md)
- [ServiceDocsVoicemailGetSingle](docs/Model/ServiceDocsVoicemailGetSingle.md)
- [ServiceDocsVoicemailMessageGetAll](docs/Model/ServiceDocsVoicemailMessageGetAll.md)
- [ServiceDocsVoicemailMessageGetSingle](docs/Model/ServiceDocsVoicemailMessageGetSingle.md)
- [ServiceDocsWebhookDelete](docs/Model/ServiceDocsWebhookDelete.md)
- [ServiceDocsWebhookGetAll](docs/Model/ServiceDocsWebhookGetAll.md)
- [ServiceDocsWebhookGetSingle](docs/Model/ServiceDocsWebhookGetSingle.md)
- [ServiceE911ActiveLocationOutput](docs/Model/ServiceE911ActiveLocationOutput.md)
- [ServiceE911ActiveLocationStatus](docs/Model/ServiceE911ActiveLocationStatus.md)
- [ServiceE911AddLocationInput](docs/Model/ServiceE911AddLocationInput.md)
- [ServiceE911AddLocationOutput](docs/Model/ServiceE911AddLocationOutput.md)
- [ServiceE911LegacyDataOutput](docs/Model/ServiceE911LegacyDataOutput.md)
- [ServiceE911LocationInput](docs/Model/ServiceE911LocationInput.md)
- [ServiceE911LocationOutput](docs/Model/ServiceE911LocationOutput.md)
- [ServiceE911LocationURI](docs/Model/ServiceE911LocationURI.md)
- [ServiceE911LocationURILegacyData](docs/Model/ServiceE911LocationURILegacyData.md)
- [ServiceE911LocationURIStatus](docs/Model/ServiceE911LocationURIStatus.md)
- [ServiceE911RemoveLocationOutput](docs/Model/ServiceE911RemoveLocationOutput.md)
- [ServiceE911RemoveLocationStatus](docs/Model/ServiceE911RemoveLocationStatus.md)
- [ServiceE911StatusOutput](docs/Model/ServiceE911StatusOutput.md)
- [ServiceE911URIInput](docs/Model/ServiceE911URIInput.md)
- [ServiceE911ValidateLocationInput](docs/Model/ServiceE911ValidateLocationInput.md)
- [ServiceE911ValidateLocationOutput](docs/Model/ServiceE911ValidateLocationOutput.md)
- [ServiceEndpoint](docs/Model/ServiceEndpoint.md)
- [ServiceFeatureCode](docs/Model/ServiceFeatureCode.md)
- [ServiceGroupOutputFull](docs/Model/ServiceGroupOutputFull.md)
- [ServiceGroupOutputShort](docs/Model/ServiceGroupOutputShort.md)
- [ServiceImpersonateUserOutputFull](docs/Model/ServiceImpersonateUserOutputFull.md)
- [ServiceImpersonatedUserInfo](docs/Model/ServiceImpersonatedUserInfo.md)
- [ServiceMediaOutputFull](docs/Model/ServiceMediaOutputFull.md)
- [ServiceMediaOutputShort](docs/Model/ServiceMediaOutputShort.md)
- [ServiceMetaflowOutput](docs/Model/ServiceMetaflowOutput.md)
- [ServiceMetaflowPattern](docs/Model/ServiceMetaflowPattern.md)
- [ServiceParkingSlotData](docs/Model/ServiceParkingSlotData.md)
- [ServicePhoneNumberResult](docs/Model/ServicePhoneNumberResult.md)
- [ServicePhoneNumberSearchOutput](docs/Model/ServicePhoneNumberSearchOutput.md)
- [ServicePhonenumberOutput](docs/Model/ServicePhonenumberOutput.md)
- [ServicePingOutput](docs/Model/ServicePingOutput.md)
- [ServiceQueueRecipientOutput](docs/Model/ServiceQueueRecipientOutput.md)
- [ServiceQueueRecipientOutputRecipient](docs/Model/ServiceQueueRecipientOutputRecipient.md)
- [ServiceQueueRecipientOutputRecipientFeatures](docs/Model/ServiceQueueRecipientOutputRecipientFeatures.md)
- [ServiceRemoveURIApiOutput](docs/Model/ServiceRemoveURIApiOutput.md)
- [ServiceStorageOutput](docs/Model/ServiceStorageOutput.md)
- [ServiceStoragePlan](docs/Model/ServiceStoragePlan.md)
- [ServiceStoragePlanDatabase](docs/Model/ServiceStoragePlanDatabase.md)
- [ServiceStoragePlanDatabaseAttachment](docs/Model/ServiceStoragePlanDatabaseAttachment.md)
- [ServiceStoragePlanDatabaseDocument](docs/Model/ServiceStoragePlanDatabaseDocument.md)
- [ServiceStoragePlanDatabaseProperties](docs/Model/ServiceStoragePlanDatabaseProperties.md)
- [ServiceStoragePlanDatabaseTypes](docs/Model/ServiceStoragePlanDatabaseTypes.md)
- [ServiceSystemStatusCPAASService](docs/Model/ServiceSystemStatusCPAASService.md)
- [ServiceSystemStatusMessagingService](docs/Model/ServiceSystemStatusMessagingService.md)
- [ServiceSystemStatusOutput](docs/Model/ServiceSystemStatusOutput.md)
- [ServiceSystemStatusSupportService](docs/Model/ServiceSystemStatusSupportService.md)
- [ServiceSystemStatusVOIPService](docs/Model/ServiceSystemStatusVOIPService.md)
- [ServiceTTS](docs/Model/ServiceTTS.md)
- [ServiceTemporalRuleOutputFull](docs/Model/ServiceTemporalRuleOutputFull.md)
- [ServiceTemporalRuleOutputShort](docs/Model/ServiceTemporalRuleOutputShort.md)
- [ServiceTemporalRuleSetOutputFull](docs/Model/ServiceTemporalRuleSetOutputFull.md)
- [ServiceTemporalRuleSetOutputShort](docs/Model/ServiceTemporalRuleSetOutputShort.md)
- [ServiceUpdateRecordTypeForAccount](docs/Model/ServiceUpdateRecordTypeForAccount.md)
- [ServiceUserOutputShort](docs/Model/ServiceUserOutputShort.md)
- [ServiceVOIPAccountAddData](docs/Model/ServiceVOIPAccountAddData.md)
- [ServiceVOIPAccountEditData](docs/Model/ServiceVOIPAccountEditData.md)
- [ServiceVOIPAccountLimit2](docs/Model/ServiceVOIPAccountLimit2.md)
- [ServiceVOIPCallQueueAddEditData](docs/Model/ServiceVOIPCallQueueAddEditData.md)
- [ServiceVOIPCallQueueEnableMembershipData](docs/Model/ServiceVOIPCallQueueEnableMembershipData.md)
- [ServiceVOIPCallQueueRecipientLoginLogoutData](docs/Model/ServiceVOIPCallQueueRecipientLoginLogoutData.md)
- [ServiceVOIPCallQueueRecipientStatusData](docs/Model/ServiceVOIPCallQueueRecipientStatusData.md)
- [ServiceVOIPCallQueueRoleAssignData](docs/Model/ServiceVOIPCallQueueRoleAssignData.md)
- [ServiceVOIPChannelRunActionData](docs/Model/ServiceVOIPChannelRunActionData.md)
- [ServiceVOIPChannelRunMetaflowData](docs/Model/ServiceVOIPChannelRunMetaflowData.md)
- [ServiceVOIPDeviceAddEdit2](docs/Model/ServiceVOIPDeviceAddEdit2.md)
- [ServiceVOIPDeviceAddEdit3a](docs/Model/ServiceVOIPDeviceAddEdit3a.md)
- [ServiceVOIPDeviceAddEdit3c](docs/Model/ServiceVOIPDeviceAddEdit3c.md)
- [ServiceVOIPDeviceAddEdit3d](docs/Model/ServiceVOIPDeviceAddEdit3d.md)
- [ServiceVOIPDeviceAddEdit4](docs/Model/ServiceVOIPDeviceAddEdit4.md)
- [ServiceVOIPDeviceAddEdit5](docs/Model/ServiceVOIPDeviceAddEdit5.md)
- [ServiceVOIPDeviceAddEditLineKey](docs/Model/ServiceVOIPDeviceAddEditLineKey.md)
- [ServiceVOIPDeviceAddEditProvision](docs/Model/ServiceVOIPDeviceAddEditProvision.md)
- [ServiceVOIPGroupAddEdit2](docs/Model/ServiceVOIPGroupAddEdit2.md)
- [ServiceVOIPImpersonateUser](docs/Model/ServiceVOIPImpersonateUser.md)
- [ServiceVOIPMediaAddEditData](docs/Model/ServiceVOIPMediaAddEditData.md)
- [ServiceVOIPMetaflowAddData](docs/Model/ServiceVOIPMetaflowAddData.md)
- [ServiceVOIPPresenceSetResetEditData](docs/Model/ServiceVOIPPresenceSetResetEditData.md)
- [ServiceVOIPQueueMembershipAddData](docs/Model/ServiceVOIPQueueMembershipAddData.md)
- [ServiceVOIPStorageAddEditData](docs/Model/ServiceVOIPStorageAddEditData.md)
- [ServiceVOIPTemporalRuleAddEdit2](docs/Model/ServiceVOIPTemporalRuleAddEdit2.md)
- [ServiceVOIPTemporalRuleSetAddEditData](docs/Model/ServiceVOIPTemporalRuleSetAddEditData.md)
- [ServiceVOIPUserAdd2](docs/Model/ServiceVOIPUserAdd2.md)
- [ServiceVOIPVoicemailAddEditData](docs/Model/ServiceVOIPVoicemailAddEditData.md)
- [ServiceVOIPVoicemailMessageAddData](docs/Model/ServiceVOIPVoicemailMessageAddData.md)
- [ServiceVOIPVoicemailMessageChange](docs/Model/ServiceVOIPVoicemailMessageChange.md)
- [ServiceVoicemailMedia](docs/Model/ServiceVoicemailMedia.md)
- [ServiceVoicemailMessageOutput](docs/Model/ServiceVoicemailMessageOutput.md)
- [ServiceVoicemailOutputFull](docs/Model/ServiceVoicemailOutputFull.md)
- [ServiceVoicemailOutputShort](docs/Model/ServiceVoicemailOutputShort.md)
- [ServiceWebhookAdd](docs/Model/ServiceWebhookAdd.md)
- [ServiceWebhookDeleteOutput](docs/Model/ServiceWebhookDeleteOutput.md)
- [ServiceWebhookEdit](docs/Model/ServiceWebhookEdit.md)

## Authorization

Authentication schemes defined for the API:
### BearerAuth

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author

support@whitelabelcomm.com

## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.1`
    - Generator version: `7.11.0-SNAPSHOT`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
