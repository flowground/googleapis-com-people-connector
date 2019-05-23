# ![LOGO](logo.png) People **flow**ground Connector

## Description

A generated **flow**ground connector for the People API (version v1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/people/v1/swagger.json<br/>
Generated at: 2019-05-23T12:13:32+03:00

## API Description

Provides access to information about profiles and contacts.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### List all contact groups owned by the authenticated user. Members of the<br/>
> contact groups are not populated.

*Tags:* `contactGroups`

#### Input Parameters
* `pageSize` - _optional_ - The maximum number of resources to return.
* `pageToken` - _optional_ - The next_page_token value returned from a previous call to
[ListContactGroups](/people/api/rest/v1/contactgroups/list).
Requests the next page of resources.
* `syncToken` - _optional_ - A sync token, returned by a previous call to `contactgroups.list`.
Only resources changed since the sync token was created will be returned.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Create a new contact group owned by the authenticated user.

*Tags:* `contactGroups`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Get a list of contact groups owned by the authenticated user by specifying<br/>
> a list of contact group resource names.

*Tags:* `contactGroups`

#### Input Parameters
* `maxMembers` - _optional_ - Specifies the maximum number of members to return for each group.
* `resourceNames` - _optional_ - The resource names of the contact groups to get.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Provides information about a list of specific people by specifying a list<br/>
> of requested resource names. Use `people/me` to indicate the authenticated<br/>
> user.<br/>
> <br><br/>
> The request throws a 400 error if 'personFields' is not specified.

*Tags:* `people`

#### Input Parameters
* `personFields` - _optional_ - **Required.** A field mask to restrict which fields on each person are
returned. Multiple fields can be specified by separating them with commas.
Valid values are:

* addresses
* ageRanges
* biographies
* birthdays
* braggingRights
* coverPhotos
* emailAddresses
* events
* genders
* imClients
* interests
* locales
* memberships
* metadata
* names
* nicknames
* occupations
* organizations
* phoneNumbers
* photos
* relations
* relationshipInterests
* relationshipStatuses
* residences
* sipAddresses
* skills
* taglines
* urls
* userDefined
* `requestMask.includeField` - _optional_ - **Required.** Comma-separated list of person fields to be included in the
response. Each path should start with `person.`: for example,
`person.names` or `person.photos`.
* `resourceNames` - _optional_ - The resource names of the people to provide information about.

- To get information about the authenticated user, specify `people/me`.
- To get information about a google account, specify
  `people/`<var>account_id</var>.
- To get information about a contact, specify the resource name that
  identifies the contact as returned by
[`people.connections.list`](/people/api/rest/v1/people.connections/list).

You can include up to 50 resource names in one request.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Create a new contact and return the person resource for that contact.

*Tags:* `people`

#### Input Parameters
* `parent` - _optional_ - The resource name of the owning person resource.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Delete an existing contact group owned by the authenticated user by<br/>
> specifying a contact group resource name.

*Tags:* `contactGroups`

#### Input Parameters
* `deleteContacts` - _optional_ - Set to true to also delete the contacts in the specified group.
* `resourceName` - _required_ - The resource name of the contact group to delete.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Get a specific contact group owned by the authenticated user by specifying<br/>
> a contact group resource name.

*Tags:* `contactGroups`

#### Input Parameters
* `maxMembers` - _optional_ - Specifies the maximum number of members to return.
* `requestMask.includeField` - _optional_ - **Required.** Comma-separated list of person fields to be included in the
response. Each path should start with `person.`: for example,
`person.names` or `person.photos`.
* `resourceName` - _required_ - The resource name of the contact group to get.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Update the name of an existing contact group owned by the authenticated<br/>
> user.

*Tags:* `contactGroups`

#### Input Parameters
* `resourceName` - _required_ - The resource name for the contact group, assigned by the server. An ASCII
string, in the form of `contactGroups/`<var>contact_group_id</var>.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Provides a list of the authenticated user's contacts merged with any<br/>
> connected profiles.<br/>
> <br><br/>
> The request throws a 400 error if 'personFields' is not specified.

*Tags:* `people`

#### Input Parameters
* `pageSize` - _optional_ - The number of connections to include in the response. Valid values are
between 1 and 2000, inclusive. Defaults to 100.
* `pageToken` - _optional_ - The token of the page to be returned.
* `personFields` - _optional_ - **Required.** A field mask to restrict which fields on each person are
returned. Multiple fields can be specified by separating them with commas.
Valid values are:

* addresses
* ageRanges
* biographies
* birthdays
* braggingRights
* coverPhotos
* emailAddresses
* events
* genders
* imClients
* interests
* locales
* memberships
* metadata
* names
* nicknames
* occupations
* organizations
* phoneNumbers
* photos
* relations
* relationshipInterests
* relationshipStatuses
* residences
* sipAddresses
* skills
* taglines
* urls
* userDefined
* `requestMask.includeField` - _optional_ - **Required.** Comma-separated list of person fields to be included in the
response. Each path should start with `person.`: for example,
`person.names` or `person.photos`.
* `requestSyncToken` - _optional_ - Whether the response should include a sync token, which can be used to get
all changes since the last request. For subsequent sync requests use the
`sync_token` param instead. Initial sync requests that specify
`request_sync_token` have an additional rate limit.
* `resourceName` - _required_ - The resource name to return connections for. Only `people/me` is valid.
* `sortOrder` - _optional_ - The order in which the connections should be sorted. Defaults to
`LAST_MODIFIED_ASCENDING`.
    Possible values: LAST_MODIFIED_ASCENDING, FIRST_NAME_ASCENDING, LAST_NAME_ASCENDING.
* `syncToken` - _optional_ - A sync token returned by a previous call to `people.connections.list`.
Only resources changed since the sync token was created will be returned.
Sync requests that specify `sync_token` have an additional rate limit.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Modify the members of a contact group owned by the authenticated user.<br/>
> <br><br/>
> The only system contact groups that can have members added are<br/>
> `contactGroups/myContacts` and `contactGroups/starred`. Other system<br/>
> contact groups are deprecated and can only have contacts removed.

*Tags:* `contactGroups`

#### Input Parameters
* `resourceName` - _required_ - The resource name of the contact group to modify.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Delete a contact person. Any non-contact data will not be deleted.

*Tags:* `people`

#### Input Parameters
* `resourceName` - _required_ - The resource name of the contact to delete.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Update contact data for an existing contact person. Any non-contact data<br/>
> will not be modified.<br/>
> <br/>
> The request throws a 400 error if `updatePersonFields` is not specified.<br/>
> <br><br/>
> The request throws a 400 error if `person.metadata.sources` is not<br/>
> specified for the contact to be updated.<br/>
> <br><br/>
> The request throws a 412 error if `person.metadata.sources.etag` is<br/>
> different than the contact's etag, which indicates the contact has changed<br/>
> since its data was read. Clients should get the latest person and re-apply<br/>
> their updates to the latest person.

*Tags:* `people`

#### Input Parameters
* `resourceName` - _required_ - The resource name for the person, assigned by the server. An ASCII string
with a max length of 27 characters, in the form of
`people/`<var>person_id</var>.
* `updatePersonFields` - _optional_ - **Required.** A field mask to restrict which fields on the person are
updated. Multiple fields can be specified by separating them with commas.
All updated fields will be replaced. Valid values are:

* addresses
* biographies
* birthdays
* emailAddresses
* events
* genders
* imClients
* interests
* locales
* names
* nicknames
* occupations
* organizations
* phoneNumbers
* relations
* residences
* sipAddresses
* urls
* userDefined
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-people-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
