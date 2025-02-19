# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased](https://github.com/fivetran/go-fivetran/compare/v0.6.10...HEAD)

## [0.6.9](https://github.com/fivetran/go-fivetran/compare/v0.6.9...v0.6.10) - 2022-11-24

## Fixed
- `ConnectorConfigResponse.UseAPIKeys` wrong type `string` -> `bool`
- `ConnectorConfigResponse.IsSecure` wrong type `string` -> `bool`
- `ConnectorConfigResponse.SkipBefore` wrong type `int` -> `*int`
- `ConnectorConfigResponse.SkipAfter` wrong type `int` -> `*int`

## Added
- `DestinationConfigResponse.Catalog` missing field added (Databricks)

## [0.6.9](https://github.com/fivetran/go-fivetran/compare/v0.6.8...v0.6.9) - 2022-10-04

## Fixed
- `DestinationConfigResponse.IsPrivateKeyEncrypted` wrong type

## [0.6.8](https://github.com/fivetran/go-fivetran/compare/v0.6.7...v0.6.8) - 2022-09-13

## Added
- `DestinationConfigResponse.Role` missing field added (Snowflake)
- `DestinationConfigResponse.IsPrivateKeyEncrypted` missing field added (Snowflake)
- `DestinationConfigResponse.Passphrase` missing field added (Snowflake)

## [0.6.7](https://github.com/fivetran/go-fivetran/compare/v0.6.6...v0.6.7) - 2022-08-29

## Added
- `ConnectorSchemaConfigTable.SyncMode` field that allows to switch table sync mode

## [0.6.6](https://github.com/fivetran/go-fivetran/compare/v0.6.5...v0.6.6) - 2022-08-15

## Fixed
- `DestinationConfigResponse.Location` missing field added (field is used by BQ destination as `data_set_location` field)

## [0.6.5](https://github.com/fivetran/go-fivetran/compare/v0.6.4...v0.6.5) - 2022-08-15

## Fixed
- `DestinationConfigResponse.PublicKey` missing field added (field is readonly and represented only in response)
- `DestinationConfigResponse.PrivateKey` missing field added

## [0.6.4](https://github.com/fivetran/go-fivetran/compare/v0.6.3...v0.6.4) - 2022-07-27

## Added
Mock HttpClient class with a unit test example

## Fixed
- `ConnectorSchemaDetailsResponse.Data.Schemas` type changed: 
    - Old `map[string]ConnectorSchemaConfigSchemaResponse`
    - New `map[string]*ConnectorSchemaConfigSchemaResponse`

## [0.6.3](https://github.com/fivetran/go-fivetran/compare/v0.6.2...v0.6.3) - 2022-07-20

## Fixed
- `ConnectorSchemaConfigTableResponse.EnabledPatchSettings` missing field added
- `ConnectorSchemaConfigTableResponse.NameInDestination` missing field added
- `ConnectorSchemaConfigSchemaResponse.NameInDestination` missing field added

## [0.6.2](https://github.com/fivetran/go-fivetran/compare/v0.6.1...v0.6.2) - 2022-07-20

## Fixed
- `ConnectorConfig.TokenKey` missing field added
- `ConnectorConfig.TokenSecret` missing field added

## [0.6.1](https://github.com/fivetran/go-fivetran/compare/v0.6.0...v0.6.1) - 2022-07-15

## Fixed
- `ConnectorSchemaConfigTableResponse` type accesibility

## [0.6.0](https://github.com/fivetran/go-fivetran/compare/v0.5.11...v0.6.0) - 2022-07-08

## Added
Supported the following Fivetran API endpoints:
- [Retrieve a Connector Schema Config](https://fivetran.com/docs/rest-api/connectors#retrieveaconnectorschemaconfig)
- [Reload a Connector Schema Config](https://fivetran.com/docs/rest-api/connectors#reloadaconnectorschemaconfig)
- [Modify a Connector Schema Config](https://fivetran.com/docs/rest-api/connectors#modifyaconnectorschemaconfig)

## [0.5.11](https://github.com/fivetran/go-fivetran/compare/v0.5.10...v0.5.11) - 2022-07-05

## Fixed
- `ConnectorConfig.PAT` missing field added (Personal Access Token for github connector)

## [0.5.10](https://github.com/fivetran/go-fivetran/compare/v0.5.9...v0.5.10) - 2022-06-16

## Fixed
- `ConnectorConfig.EuRegion` missing field added

## [0.5.9](https://github.com/fivetran/go-fivetran/compare/v0.5.8...v0.5.9) - 2022-06-09

## Fixed
- `ConnectorConfig.PublicationName` missing field added

## [0.5.8](https://github.com/fivetran/go-fivetran/compare/v0.5.7...v0.5.8) - 2022-05-24

## Fixed 
- `DestinationConfigResponse.CreateExternalTables` field type updated

## [0.5.7](https://github.com/fivetran/go-fivetran/compare/v0.5.6...v0.5.7) - 2022-05-13

## Fixed
- `ConnectorConfig.SkipBefore` field transformed to type `int`
- `ConnectorConfig.SkipAfter`  field transformed to type `int`

## [0.5.6](https://github.com/fivetran/go-fivetran/compare/v0.5.5...v0.5.6) - 2022-04-26

## Fixed
- `ConnectorConfig.APIKeys` field transformed to type `[]string`
- `ConnectorConfig.AccountIds` field transfromed to type `[]string`

## [0.5.5](https://github.com/fivetran/go-fivetran/compare/v0.5.4...v0.5.5) - 2022-04-20

## Fixed
- Added `folder_id` missed field to connector config.

## [0.5.4](https://github.com/fivetran/go-fivetran/compare/v0.5.3...v0.5.4) - 2022-02-25

## Fixed
- Added `base_url` missed field to connector config.
- Added `entity_id` missed field to connector config.
- Added `soap_uri` missed field to connector config.
- Added `user_id` missed field to connector config.
- Added `encryption_key` missed field to connector config.

## [0.5.3](https://github.com/fivetran/go-fivetran/compare/v0.5.2...v0.5.3) - 2022-02-21

## Fixed
- Added `api_type` missed field to connector config.

## [0.5.2](https://github.com/fivetran/go-fivetran/compare/v0.5.1...v0.5.2) - 2022-01-31

## Fixed
- Added `is_multi_entity_feature_enabled` missed field to connector config.
- Added `always_encrypted` missed field to connector config.

## [0.5.1](https://github.com/fivetran/go-fivetran/compare/v0.5.0...v0.5.1) - 2022-01-31

## Fixed
- Used `connection_type` key in destination config responses with v2 accept header for consistency.
- Added `connection_type` missed field to connector config.

## [0.5.0](https://github.com/fivetran/go-fivetran/compare/v0.4.0...v0.5.0) - 2022-01-24

## Added
The following fields were added to user resource responses
- UserDetailsResponse.Data.Role - RoleName for user role in account
- UserInviteResponse.Data.Role - RoleName for user role in account
- UserModifyResponse.Data.Role - RoleName for user role in account

## [0.4.0](https://github.com/fivetran/go-fivetran/compare/v0.3.1...v0.4.0) - 2022-01-18

## Added
- E2E tests. 
To be sure that SDK is stable we have added e2e tests which are triggered on each pull request to the main branch. Each e2e test has `E2E` suffix and located in a corresponding `_test.go` file.
- GitHub actions workflow to run tests on a testing account.

## Fixed
- `ConnectorConfigRequest.IsNewPackage` missing field added
- `ConnectorConfigRequest.AdobeAnalyticsConfigurations` missing field added

## [0.3.1](https://github.com/fivetran/go-fivetran/compare/v0.3.0...v0.3.1) - 2021-12-08

## Fixed
- `DestinationConfigRequest.ClusterId` missing field added.
- `DestinationConfigRequest.ClusterRegion` missing field added.

## [0.3.0](https://github.com/fivetran/go-fivetran/compare/v0.2.2...v0.3.0) - 2021-11-10

### Added
- `CustomUserAgent` method for overriding User-Agent header in http-responses (for applications that uses SDK)

## [0.2.2](https://github.com/fivetran/go-fivetran/compare/v0.2.1...v0.2.2) - 2021-09-22

## Fixed
- `DestinationConfigRequest.SecretKey` missing field added.

## [0.2.1](https://github.com/fivetran/go-fivetran/compare/v0.2.0...v0.2.1) - 2021-07-27

## Fixed
- `ConnectorConfigResponse.Port` type is now *int as the response type has been fixed in the REST API v2.

## [0.2.0](https://github.com/fivetran/go-fivetran/compare/v0.1.0...v0.2.0) - 2021-07-16

### Added
- `UsersListResponse.Role`
- `GroupListUsersResponse.Role`
- `ConnectorConfig.AuthType`
- `ConnectorCreateService.SyncFrequency`
- `ConnectorCreateService.DailySyncTime`
- `ConnectorCreateService.PauseAfterTrial`
- `ConnectorCreateResponse.Data.Paused`
- `ConnectorCreateResponse.Data.DailySyncTime`
- `ConnectorCreateResponse.Data.PauseAfterTrial`
- `ConnectorDetailsResponse.Data.Paused`
- `ConnectorDetailsResponse.Data.PauseAfterTrial`
- `ConnectorDetailsResponse.Data.DailySyncTime`
- `ConnectorModifyService.PauseAfterTrial` 

### Changed
- `ConnectorCreateService`, `ConnectorDetailsService`, `ConnectorModifyService`, and `ConnectorSetupTestsService` are now using REST API v2.
- All `int` and `bool` fields of all response types are now `*int` and `*bool`. 

### Removed
- Removed the unnecessary `ConnectorsSourceMetadataResponse.LinkToErd` JSON annotation `omitempty`.

### Fixed
- `DestinationConfigResponse` field `ConnectionType` has changed to `ConnectionMethod` to adequate to the REST API response.

## [0.1.0](https://github.com/fivetran/go-fivetran/releases/tag/v0.1.0) - 2021-07-05

Initial release. 

### Added

- User Management API: List all Users, Retrieve user details, Invite a user, Modify a user, Delete a user.
- Group Management API: Create a group, List all groups, Retrieve group details, Modify a group, List all connectors within a group, List all users within a group, Add a user to a group, Remove a user from a group, Delete a group.
- Certificate Management API: Approve a connector certificate, Approve a connector fingerprint, Approve a destination certificate, Approve a destination fingerprint.
- Destination Management API: Create a destination, Retrieve destination details, Modify a destination, Run destination setup tests, Delete a destination, Destination Config.
- Connector Management API: Retrieve source metadata, Create a connector, Retrieve connector details, Modify a connector, Sync connector data, Re-sync connector table data, Run connector setup tests, Delete a connector, Connector Config, Connector Auth.
