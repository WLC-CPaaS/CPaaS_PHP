# # ServiceVOIPDeviceAddEdit2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**call_forward** | [**\OpenAPI\Client\Model\ModelsCallForward**](ModelsCallForward.md) |  | [optional]
**caller_id** | [**\OpenAPI\Client\Model\ServiceVOIPDeviceAddEdit3c**](ServiceVOIPDeviceAddEdit3c.md) |  | [optional]
**device_type** | **string** |  | [optional]
**do_not_disturb** | [**\OpenAPI\Client\Model\ModelsVOIPSharedDoNotDisturb**](ModelsVOIPSharedDoNotDisturb.md) |  | [optional]
**enabled** | **bool** | cannot use required, else it has to be true and false is not allowed | [optional]
**mac_address** | **string** | dont use mac, it enforces :, which voip does not like | [optional]
**media** | [**\OpenAPI\Client\Model\ServiceVOIPDeviceAddEdit3d**](ServiceVOIPDeviceAddEdit3d.md) |  | [optional]
**music_on_hold** | [**\OpenAPI\Client\Model\ModelsMusicOnHold**](ModelsMusicOnHold.md) |  | [optional]
**name** | **string** |  |
**owner_id** | **string** | json omitempty is needed else voip fails on \&quot;\&quot; for owner_id | [optional]
**provision** | [**\OpenAPI\Client\Model\ServiceVOIPDeviceAddEditProvision**](ServiceVOIPDeviceAddEditProvision.md) |  | [optional]
**sip** | [**\OpenAPI\Client\Model\ServiceVOIPDeviceAddEdit3a**](ServiceVOIPDeviceAddEdit3a.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
