# \GroupsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddMembersToGroup**](GroupsApi.md#AddMembersToGroup) | **Post** /warden/groups/{id}/members | Add members to a group
[**CreateGroup**](GroupsApi.md#CreateGroup) | **Post** /warden/groups | Create a group
[**DeleteGroup**](GroupsApi.md#DeleteGroup) | **Delete** /warden/groups/{id} | Delete a group by id
[**FindGroupsByMember**](GroupsApi.md#FindGroupsByMember) | **Get** /warden/groups | Find group IDs by member
[**GetGroup**](GroupsApi.md#GetGroup) | **Get** /warden/groups/{id} | Get a group by id
[**RemoveMembersFromGroup**](GroupsApi.md#RemoveMembersFromGroup) | **Delete** /warden/groups/{id}/members | Remove members from a group


# **AddMembersToGroup**
> AddMembersToGroup($id, $body)

Add members to a group

The subject making the request needs to be assigned to a policy containing:  ``` { \"resources\": [\"rn:hydra:warden:groups:<id>\"], \"actions\": [\"members.add\"], \"effect\": \"allow\" } ```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int64**| The id of the group to modify. | 
 **body** | [**MembersRequest**](MembersRequest.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateGroup**
> Group CreateGroup()

Create a group

The subject making the request needs to be assigned to a policy containing:  ``` { \"resources\": [\"rn:hydra:warden:groups\"], \"actions\": [\"create\"], \"effect\": \"allow\" } ```


### Parameters
This endpoint does not need any parameter.

### Return type

[**Group**](group.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DeleteGroup**
> DeleteGroup($id)

Delete a group by id

The subject making the request needs to be assigned to a policy containing:  ``` { \"resources\": [\"rn:hydra:warden:groups:<id>\"], \"actions\": [\"delete\"], \"effect\": \"allow\" } ```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int64**| The id of the group to look up. | 

### Return type

void (empty response body)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **FindGroupsByMember**
> []string FindGroupsByMember($member)

Find group IDs by member

The subject making the request needs to be assigned to a policy containing:  ``` { \"resources\": [\"rn:hydra:warden:groups:<member>\"], \"actions\": [\"get\"], \"effect\": \"allow\" } ```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **member** | **int64**| The id of the member to look up. | [optional] 

### Return type

**[]string**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetGroup**
> Group GetGroup($id)

Get a group by id

The subject making the request needs to be assigned to a policy containing:  ``` { \"resources\": [\"rn:hydra:warden:groups:<id>\"], \"actions\": [\"create\"], \"effect\": \"allow\" } ```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int64**| The id of the group to look up. | 

### Return type

[**Group**](group.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RemoveMembersFromGroup**
> RemoveMembersFromGroup($id, $body)

Remove members from a group

The subject making the request needs to be assigned to a policy containing:  ``` { \"resources\": [\"rn:hydra:warden:groups:<id>\"], \"actions\": [\"members.remove\"], \"effect\": \"allow\" } ```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int64**| The id of the group to modify. | 
 **body** | [**MembersRequest**](MembersRequest.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
