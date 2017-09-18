# Repo

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | The unique identifier for the repository. | [optional] 
**scm** | **string** | The source control management being used.  Currently this is either &#39;git&#39; or &#39;hg&#39; (Mercurial). | [optional] 
**owner** | **string** | The owner of the repository. | [optional] 
**name** | **string** | The name of the repository. | [optional] 
**full_name** | **string** | The full name of the repository.  This is created from the owner and name of the repository. | [optional] 
**avatar_url** | **string** | The url for the avatar image. | [optional] 
**link_url** | **string** | The link to view the repository. | [optional] 
**clone_url** | **string** | The url used to clone the repository. | [optional] 
**default_branch** | **string** | The default branch of the repository. | [optional] 
**private** | **bool** | Whether the repository is publicly visible. | [optional] 
**trusted** | **bool** | Whether the repository has trusted access for builds.  If the repository is trusted then the host network can be used and volumes can be created. | [optional] 
**timeout** | **int** | The amount of time in minutes before the build is killed. | [optional] 
**allow_pr** | **bool** | Whether pull requests should trigger a build. | [optional] 
**allow_push** | **bool** | Whether push events should trigger a build. | [optional] 
**allow_deploys** | **bool** | Whether deployment events should trigger a build. | [optional] 
**allow_tags** | **bool** | Whether tags should trigger a build. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


