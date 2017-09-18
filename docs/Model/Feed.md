# Feed

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**owner** | **string** | The owner of the repository. | [optional] 
**name** | **string** | The name of the repository. | [optional] 
**full_name** | **string** | The full name of the repository.  This is created from the owner and name of the repository. | [optional] 
**number** | **int** | The build number.  This number is specified within the context of the repository the build belongs to and is unique within that. | [optional] 
**status** | [**\DroneClient\DroneClient\DefinitionsBuildStatus**](DefinitionsBuildStatus.md) | The current status of the build. | [optional] 
**created_at** | **int** | When the build request was received. | [optional] 
**enqueued_at** | **int** | When the build was enqueued. | [optional] 
**started_at** | **int** | When the build began execution. | [optional] 
**finished_at** | **int** | When the build was finished. | [optional] 
**commit** | **string** | The commit for the build. | [optional] 
**branch** | **string** | The branch the commit was pushed to. | [optional] 
**message** | **string** | The commit message. | [optional] 
**timestamp** | **int** | When the commit was created. | [optional] 
**ref** | **string** | The alias for the commit. | [optional] 
**refspec** | **string** | The mapping from the local repository to a branch in the remote. | [optional] 
**remote** | **string** | The remote repository. | [optional] 
**author** | **string** | The login for the author of the commit. | [optional] 
**author_avatar** | **string** | The avatar for the author of the commit. | [optional] 
**author_email** | **string** | The email for the author of the commit. | [optional] 
**link_url** | **string** | The link to view the repository.  This link will point to the repository state associated with the build&#39;s commit. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


