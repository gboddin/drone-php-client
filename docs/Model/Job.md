# Job

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | The unique identifier for the build. | [optional] 
**number** | **int** | The job number.  This number is specified within the context of the build the job belongs to and is unique within that. | [optional] 
**status** | [**\DroneClient\DroneClient\DefinitionsBuildStatus**](DefinitionsBuildStatus.md) | The current status of the job. | [optional] 
**exit_code** | **int** | The exit code for the build. | [optional] 
**enqueued_at** | **int** | When the job was enqueued. | [optional] 
**started_at** | **int** | When the job began execution. | [optional] 
**finished_at** | **int** | When the job finished execution. | [optional] 
**environment** | **object** | The environment that the job was run with.  This is a map containing any values for matrix builds. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


