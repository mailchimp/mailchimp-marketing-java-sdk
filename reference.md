# Reference
## root
<details><summary><code>client.root.list() -> ListRootResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get links to all other resources available in the API.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.root().list(
    ListRootRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## AccountExports
<details><summary><code>client.accountExports.list() -> SyncPagingIterable&amp;lt;ListAccountExportsResponseExportsItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of account exports for a given account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.accountExports().list(
    ListAccountExportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.accountExports.create(request) -> CreateAccountExportsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new account export in your Mailchimp account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.accountExports().create(
    CreateAccountExportsRequest
        .builder()
        .includeStages(
            Arrays.asList(CreateAccountExportsRequestIncludeStagesItem.AUDIENCES, CreateAccountExportsRequestIncludeStagesItem.GALLERY_FILES)
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**includeStages:** `List<CreateAccountExportsRequestIncludeStagesItem>` — The stages of an account export to include.
    
</dd>
</dl>

<dl>
<dd>

**sinceTimestamp:** `Optional<OffsetDateTime>` — An ISO 8601 date that will limit the export to only records created after a given time. For instance, the reports stage will contain any campaign sent after the given timestamp. Audiences, however, are excluded from this limit.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.accountExports.get(exportId) -> GetAccountExportsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific account export.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.accountExports().get(
    "export_id",
    GetAccountExportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**exportId:** `String` — The unique id for the account export.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## ActivityFeed
<details><summary><code>client.activityFeed.list() -> List&amp;lt;ListActivityFeedResponseItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about the activity feed endpoint's resources.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.activityFeed().list();
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.activityFeed.listChimpChatter() -> SyncPagingIterable&amp;lt;ListChimpChatterActivityFeedResponseChimpChatterItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return the Chimp Chatter for this account ordered by most recent.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.activityFeed().listChimpChatter(
    ListChimpChatterActivityFeedRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Audiences
<details><summary><code>client.audiences.getAudienceContactList(audienceId) -> GetAudienceContactListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of omni-channel contacts for a given audience.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.audiences().getAudienceContactList(
    "audience_id",
    GetAudienceContactListRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**audienceId:** `String` — The unique ID for the audience.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Paginate through a collection of records by setting the `cursor` parameter to a `next_cursor` attribute returned by a previous request. Default value fetches the first "page" of results.
    
</dd>
</dl>

<dl>
<dd>

**createdBefore:** `Optional<OffsetDateTime>` — Restricts the response to contacts created at or before the specified time (inclusive). Uses ISO 8601 format: 2025-04-23T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**createdSince:** `Optional<OffsetDateTime>` — Restricts the response to contacts created after the specified time (exclusive). Uses ISO 8601 format: 2025-04-23T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**updatedBefore:** `Optional<OffsetDateTime>` — Restricts the response to contacts updated at or before the specified time (inclusive). Uses ISO 8601 format: 2025-04-23T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**updatedSince:** `Optional<OffsetDateTime>` — Restricts the response to contacts updated after the specified time (exclusive). Uses ISO 8601 format: 2025-04-23T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<GetAudienceContactListRequestSortField>` — Specifies the field to sort the returned contacts by.
    
</dd>
</dl>

<dl>
<dd>

**sortDir:** `Optional<GetAudienceContactListRequestSortDir>` — Determines the order direction for sorted results.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.audiences.createAudienceContact(audienceId, request) -> AudiencesContact</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new omni-channel contact for an audience.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.audiences().createAudienceContact(
    "audience_id",
    CreateAudienceContactRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**audienceId:** `String` — The unique ID for the audience.
    
</dd>
</dl>

<dl>
<dd>

**mergeFieldValidationMode:** `Optional<CreateAudienceContactRequestMergeFieldValidationMode>` — Defines how merge field validation is handled. When set to `ignore_required_checks`, the API does not raise an error if required merge fields are missing from the request. When set to `strict`, the API enforces validation and returns an error if any required merge field is not provided. If this setting is omitted, `strict` is applied by default.
    
</dd>
</dl>

<dl>
<dd>

**dataMode:** `Optional<CreateAudienceContactRequestDataMode>` — Indicates the data processing mode. In `historical` mode, contact data changes do not trigger automations or webhooks. In `live mode`, such changes do trigger them.
    
</dd>
</dl>

<dl>
<dd>

**emailChannel:** `Optional<CreateAudienceContactRequestEmailChannel>` 
    
</dd>
</dl>

<dl>
<dd>

**language:** `Optional<String>` — The contact's detected language.
    
</dd>
</dl>

<dl>
<dd>

**mergeFields:** `Optional<Map<String, CreateAudienceContactRequestMergeFieldsValue>>` — A dictionary of merge fields where the keys are the merge tags. See the [Merge Fields documentation](https://mailchimp.com/developer/marketing/docs/merge-fields/#structure) for more about the structure.
    
</dd>
</dl>

<dl>
<dd>

**smsChannel:** `Optional<CreateAudienceContactRequestSmsChannel>` 
    
</dd>
</dl>

<dl>
<dd>

**tags:** `Optional<List<CreateAudienceContactRequestTagsItem>>` — An array of tags to add to the contact. Accepts tag name strings or objects with name and status. This operation is append-only; existing tags will be preserved, and only new tags from this array will be added.
    
</dd>
</dl>

<dl>
<dd>

**updateExisting:** `Optional<Boolean>` — If a contact already exists, update them instead of returning a conflict error. When `true` and a matching contact is found (by email or phone), the existing contact is updated with the provided channel data. Defaults to `false`.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.audiences.getAudienceContact(audienceId, contactId) -> AudiencesContact</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a specific omni-channel contact in an audience.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.audiences().getAudienceContact(
    "audience_id",
    "contact_id",
    GetAudienceContactRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**audienceId:** `String` — The unique ID for the audience.
    
</dd>
</dl>

<dl>
<dd>

**contactId:** `String` — A unique identifier for the contact, which can be a Mailchimp contact ID or a channel hash. A channel hash must follow the format email:[md5_hash] (where the hash is the MD5 of the lowercased email address) or sms:[sha256_hash] (where the hash is the SHA256 of the E.164-formatted phone number).
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.audiences.patchAudienceContact(audienceId, contactId, request) -> AudiencesContact</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing omni-channel contact.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.audiences().patchAudienceContact(
    "audience_id",
    "contact_id",
    PatchAudienceContactRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**audienceId:** `String` — The unique ID for the audience.
    
</dd>
</dl>

<dl>
<dd>

**contactId:** `String` — The unique id for the contact.
    
</dd>
</dl>

<dl>
<dd>

**mergeFieldValidationMode:** `Optional<PatchAudienceContactRequestMergeFieldValidationMode>` — Defines how merge field validation is handled. When set to `ignore_required_checks`, the API does not raise an error if required merge fields are missing from the request. When set to `strict`, the API enforces validation and returns an error if any required merge field is not provided. If this setting is omitted, `strict` is applied by default.
    
</dd>
</dl>

<dl>
<dd>

**dataMode:** `Optional<PatchAudienceContactRequestDataMode>` — Indicates the data processing mode. In `historical` mode, contact data changes do not trigger automations or webhooks. In `live mode`, such changes do trigger them.
    
</dd>
</dl>

<dl>
<dd>

**emailChannel:** `Optional<PatchAudienceContactRequestEmailChannel>` 
    
</dd>
</dl>

<dl>
<dd>

**language:** `Optional<String>` — The contact's detected language.
    
</dd>
</dl>

<dl>
<dd>

**mergeFields:** `Optional<Map<String, PatchAudienceContactRequestMergeFieldsValue>>` — A dictionary of merge fields where the keys are the merge tags. See the [Merge Fields documentation](https://mailchimp.com/developer/marketing/docs/merge-fields/#structure) for more about the structure.
    
</dd>
</dl>

<dl>
<dd>

**smsChannel:** `Optional<PatchAudienceContactRequestSmsChannel>` 
    
</dd>
</dl>

<dl>
<dd>

**tags:** `Optional<List<PatchAudienceContactRequestTagsItem>>` — An array of tags to add to the contact. Accepts tag name strings or objects with name and status. This operation is append-only; existing tags will be preserved, and only new tags from this array will be added.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.audiences.postAudiencesContactsActionsArchive(audienceId, contactId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Archives a Contact.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.audiences().postAudiencesContactsActionsArchive(
    "audience_id",
    "contact_id",
    PostAudiencesContactsActionsArchiveRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**audienceId:** `String` — The unique ID for the audience.
    
</dd>
</dl>

<dl>
<dd>

**contactId:** `String` — The unique id for the contact.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.audiences.postAudiencesContactsActionsForget(audienceId, contactId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Forgets a Contact.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.audiences().postAudiencesContactsActionsForget(
    "audience_id",
    "contact_id",
    PostAudiencesContactsActionsForgetRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**audienceId:** `String` — The unique ID for the audience.
    
</dd>
</dl>

<dl>
<dd>

**contactId:** `String` — The unique id for the contact.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## AuthorizedApps
<details><summary><code>client.authorizedApps.list() -> SyncPagingIterable&amp;lt;ListAuthorizedAppsResponseAppsItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of an account's registered, connected applications.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.authorizedApps().list(
    ListAuthorizedAppsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.authorizedApps.get(appId) -> GetAuthorizedAppsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific authorized application.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.authorizedApps().get(
    "app_id",
    GetAuthorizedAppsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appId:** `String` — The unique id for the connected authorized application.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## automations
<details><summary><code>client.automations.list() -> SyncPagingIterable&amp;lt;AutomationWorkflow&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a summary of an account's classic automations.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().list(
    ListAutomationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**beforeCreateTime:** `Optional<OffsetDateTime>` — Restrict the response to automations created before this time. Uses the ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sinceCreateTime:** `Optional<OffsetDateTime>` — Restrict the response to automations created after this time. Uses the ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**beforeStartTime:** `Optional<OffsetDateTime>` — Restrict the response to automations started before this time. Uses the ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sinceStartTime:** `Optional<OffsetDateTime>` — Restrict the response to automations started after this time. Uses the ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**status:** `Optional<ListAutomationsRequestStatus>` — Restrict the results to automations with the specified status.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.create(request) -> AutomationWorkflow</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new classic automation in your Mailchimp account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().create(
    CreateAutomationsRequest
        .builder()
        .recipients(
            CreateAutomationsRequestRecipients
                .builder()
                .build()
        )
        .triggerSettings(
            CreateAutomationsRequestTriggerSettings
                .builder()
                .workflowType(CreateAutomationsRequestTriggerSettingsWorkflowType.ABANDONED_BROWSE)
                .build()
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**recipients:** `CreateAutomationsRequestRecipients` — List settings for the Automation.
    
</dd>
</dl>

<dl>
<dd>

**settings:** `Optional<CreateAutomationsRequestSettings>` — The settings for the Automation workflow.
    
</dd>
</dl>

<dl>
<dd>

**triggerSettings:** `CreateAutomationsRequestTriggerSettings` — Trigger settings for the Automation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.get(workflowId) -> AutomationWorkflow</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a summary of an individual classic automation workflow's settings and content. The `trigger_settings` object returns information for the first email in the workflow.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().get(
    "workflow_id",
    GetAutomationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.createActionArchive(workflowId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Archiving will permanently end your automation and keep the report data. You’ll be able to replicate your archived automation, but you can’t restart it.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().createActionArchive(
    "workflow_id",
    CreateActionArchiveAutomationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.createActionPauseAllEmail(workflowId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Pause all emails in a specific classic automation workflow.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().createActionPauseAllEmail(
    "workflow_id",
    CreateActionPauseAllEmailAutomationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.createActionStartAllEmail(workflowId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start all emails in a classic automation workflow.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().createActionStartAllEmail(
    "workflow_id",
    CreateActionStartAllEmailAutomationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.listEmails(workflowId) -> ListEmailsAutomationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a summary of the emails in a classic automation workflow.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().listEmails(
    "workflow_id",
    ListEmailsAutomationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.getEmail(workflowId, workflowEmailId) -> AutomationWorkflowEmail</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about an individual classic automation workflow email.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().getEmail(
    "workflow_id",
    "workflow_email_id",
    GetEmailAutomationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>

<dl>
<dd>

**workflowEmailId:** `String` — The unique id for the Automation workflow email.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.deleteEmail(workflowId, workflowEmailId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Removes an individual classic automation workflow email. Emails from certain workflow types, including the Abandoned Cart Email (abandonedCart) and Product Retargeting Email (abandonedBrowse) Workflows, cannot be deleted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().deleteEmail(
    "workflow_id",
    "workflow_email_id",
    DeleteEmailAutomationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>

<dl>
<dd>

**workflowEmailId:** `String` — The unique id for the Automation workflow email.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.updateEmail(workflowId, workflowEmailId, request) -> AutomationWorkflowEmail</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update settings for a classic automation workflow email.  Only works with workflows of type: abandonedBrowse, abandonedCart, emailFollowup, or singleWelcome.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().updateEmail(
    "workflow_id",
    "workflow_email_id",
    UpdateEmailAutomationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>

<dl>
<dd>

**workflowEmailId:** `String` — The unique id for the Automation workflow email.
    
</dd>
</dl>

<dl>
<dd>

**delay:** `Optional<UpdateEmailAutomationsRequestDelay>` — The delay settings for an automation email.
    
</dd>
</dl>

<dl>
<dd>

**settings:** `Optional<UpdateEmailAutomationsRequestSettings>` — Settings for the campaign including the email subject, from name, and from email address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.createEmailActionPause(workflowId, workflowEmailId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Pause an automated email.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().createEmailActionPause(
    "workflow_id",
    "workflow_email_id",
    CreateEmailActionPauseAutomationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>

<dl>
<dd>

**workflowEmailId:** `String` — The unique id for the Automation workflow email.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.createEmailActionStart(workflowId, workflowEmailId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start an automated email.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().createEmailActionStart(
    "workflow_id",
    "workflow_email_id",
    CreateEmailActionStartAutomationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>

<dl>
<dd>

**workflowEmailId:** `String` — The unique id for the Automation workflow email.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.listEmailQueue(workflowId, workflowEmailId) -> ListEmailQueueAutomationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a classic automation email queue.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().listEmailQueue(
    "workflow_id",
    "workflow_email_id",
    ListEmailQueueAutomationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>

<dl>
<dd>

**workflowEmailId:** `String` — The unique id for the Automation workflow email.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.createEmailQueue(workflowId, workflowEmailId, request) -> SubscriberInAutomationQueue</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Manually add a subscriber to a workflow, bypassing the default trigger settings. You can also use this endpoint to trigger a series of automated emails in an API 3.0 workflow type.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().createEmailQueue(
    "workflow_id",
    "workflow_email_id",
    CreateEmailQueueAutomationsRequest
        .builder()
        .emailAddress("email_address")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>

<dl>
<dd>

**workflowEmailId:** `String` — The unique id for the Automation workflow email.
    
</dd>
</dl>

<dl>
<dd>

**emailAddress:** `String` — The list member's email address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.getEmailQueue(workflowId, workflowEmailId, subscriberHash) -> SubscriberInAutomationQueue</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific subscriber in a classic automation email queue.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().getEmailQueue(
    "workflow_id",
    "workflow_email_id",
    "subscriber_hash",
    GetEmailQueueAutomationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>

<dl>
<dd>

**workflowEmailId:** `String` — The unique id for the Automation workflow email.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.listRemovedSubscribers(workflowId) -> ListRemovedSubscribersAutomationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about subscribers who were removed from a classic automation workflow.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().listRemovedSubscribers(
    "workflow_id",
    ListRemovedSubscribersAutomationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.createRemovedSubscriber(workflowId, request) -> SubscriberRemovedFromAutomationWorkflow</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a subscriber from a specific classic automation workflow. You can remove a subscriber at any point in an automation workflow, regardless of how many emails they've been sent from that workflow. Once they're removed, they can never be added back to the same workflow.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().createRemovedSubscriber(
    "workflow_id",
    CreateRemovedSubscriberAutomationsRequest
        .builder()
        .emailAddress("email_address")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>

<dl>
<dd>

**emailAddress:** `String` — The list member's email address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.automations.getRemovedSubscriber(workflowId, subscriberHash) -> SubscriberRemovedFromAutomationWorkflow</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific subscriber who was removed from a classic automation workflow.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.automations().getRemovedSubscriber(
    "workflow_id",
    "subscriber_hash",
    GetRemovedSubscriberAutomationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `String` — The unique id for the Automation workflow.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## BatchWebhooks
<details><summary><code>client.batchWebhooks.list() -> SyncPagingIterable&amp;lt;BatchWebhook&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get all webhooks that have been configured for batches.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.batchWebhooks().list(
    ListBatchWebhooksRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.batchWebhooks.create(request) -> CreateBatchWebhooksResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Configure a webhook that will fire whenever any batch request completes processing.  You may only have a maximum of 20 batch webhooks.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.batchWebhooks().create(
    CreateBatchWebhooksRequest
        .builder()
        .url("http://yourdomain.com/webhook")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**enabled:** `Optional<Boolean>` — Whether the webhook receives requests or not.
    
</dd>
</dl>

<dl>
<dd>

**url:** `String` — A valid URL for the Webhook.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.batchWebhooks.get(batchWebhookId) -> BatchWebhook</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific batch webhook.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.batchWebhooks().get(
    "batch_webhook_id",
    GetBatchWebhooksRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**batchWebhookId:** `String` — The unique id for the batch webhook.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.batchWebhooks.delete(batchWebhookId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a batch webhook. Webhooks will no longer be sent to the given URL.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.batchWebhooks().delete(
    "batch_webhook_id",
    DeleteBatchWebhooksRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**batchWebhookId:** `String` — The unique id for the batch webhook.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.batchWebhooks.update(batchWebhookId, request) -> BatchWebhook</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a webhook that will fire whenever any batch request completes processing.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.batchWebhooks().update(
    "batch_webhook_id",
    UpdateBatchWebhooksRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**batchWebhookId:** `String` — The unique id for the batch webhook.
    
</dd>
</dl>

<dl>
<dd>

**enabled:** `Optional<Boolean>` — Whether the webhook receives requests or not.
    
</dd>
</dl>

<dl>
<dd>

**url:** `Optional<String>` — A valid URL for the Webhook.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## batches
<details><summary><code>client.batches.list() -> SyncPagingIterable&amp;lt;Batch&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a summary of batch requests that have been made.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.batches().list(
    ListBatchesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.batches.create(request) -> Batch</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Begin processing a batch operations request.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.batches().create(
    CreateBatchesRequest
        .builder()
        .operations(
            Arrays.asList(
                CreateBatchesRequestOperationsItem
                    .builder()
                    .method(CreateBatchesRequestOperationsItemMethod.GET)
                    .path("/lists")
                    .build()
            )
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**operations:** `List<CreateBatchesRequestOperationsItem>` — An array of objects that describes operations to perform.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.batches.get(batchId) -> Batch</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the status of a batch request.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.batches().get(
    "batch_id",
    GetBatchesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**batchId:** `String` — The unique id for the batch operation.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.batches.delete(batchId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Stops a batch request from running. Since only one batch request is run at a time, this can be used to cancel a long running request. The results of any completed operations will not be available after this call.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.batches().delete(
    "batch_id",
    DeleteBatchesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**batchId:** `String` — The unique id for the batch operation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## CampaignFolders
<details><summary><code>client.campaignFolders.list() -> SyncPagingIterable&amp;lt;CampaignFoldersFoldersItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get all folders used to organize campaigns.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaignFolders().list(
    ListCampaignFoldersRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaignFolders.create(request) -> CampaignFolders</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new campaign folder.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaignFolders().create(
    CreateCampaignFoldersRequest
        .builder()
        .name("name")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `String` — Name to associate with the folder.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaignFolders.get(folderId) -> GetCampaignFoldersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific folder used to organize campaigns.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaignFolders().get(
    "folder_id",
    GetCampaignFoldersRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**folderId:** `String` — The unique id for the campaign folder.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaignFolders.delete(folderId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a specific campaign folder, and mark all the campaigns in the folder as 'unfiled'.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaignFolders().delete(
    "folder_id",
    DeleteCampaignFoldersRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**folderId:** `String` — The unique id for the campaign folder.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaignFolders.update(folderId, request) -> UpdateCampaignFoldersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a specific folder used to organize campaigns.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaignFolders().update(
    "folder_id",
    UpdateCampaignFoldersRequest
        .builder()
        .name("name")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**folderId:** `String` — The unique id for the campaign folder.
    
</dd>
</dl>

<dl>
<dd>

**name:** `String` — Name to associate with the folder.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## campaigns
<details><summary><code>client.campaigns.list() -> SyncPagingIterable&amp;lt;Campaigns&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get all campaigns in an account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().list(
    ListCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<ListCampaignsRequestType>` — The campaign type.
    
</dd>
</dl>

<dl>
<dd>

**status:** `Optional<ListCampaignsRequestStatus>` — The status of the campaign.
    
</dd>
</dl>

<dl>
<dd>

**beforeSendTime:** `Optional<OffsetDateTime>` — Restrict the response to campaigns sent before the set time. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sinceSendTime:** `Optional<OffsetDateTime>` — Restrict the response to campaigns sent after the set time. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**beforeCreateTime:** `Optional<OffsetDateTime>` — Restrict the response to campaigns created before the set time. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sinceCreateTime:** `Optional<OffsetDateTime>` — Restrict the response to campaigns created after the set time. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**listId:** `Optional<String>` — The unique id for the list.
    
</dd>
</dl>

<dl>
<dd>

**folderId:** `Optional<String>` — The unique folder id.
    
</dd>
</dl>

<dl>
<dd>

**memberId:** `Optional<String>` — Retrieve campaigns sent to a particular list member. Member ID is The MD5 hash of the lowercase version of the list member’s email address.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListCampaignsRequestSortField>` — Returns files sorted by the specified field.
    
</dd>
</dl>

<dl>
<dd>

**sortDir:** `Optional<ListCampaignsRequestSortDir>` — Determines the order direction for sorted results.
    
</dd>
</dl>

<dl>
<dd>

**includeResendShortcutEligibility:** `Optional<Boolean>` — Return the `resend_shortcut_eligibility` field in the response, which tells you if the campaign is eligible for the various Campaign Resend Shortcuts offered.
    
</dd>
</dl>

<dl>
<dd>

**includeResendShortcutUsage:** `Optional<Boolean>` — Return the `resend_shortcut_usage` field in the response.  This includes information about campaigns related by a shortcut.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.create(request) -> Campaign</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new Mailchimp campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().create(
    CreateCampaignsRequest
        .builder()
        .type(CreateCampaignsRequestType.REGULAR)
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**contentType:** `Optional<CreateCampaignsRequestContentType>` — How the campaign's content is put together. The old drag and drop editor uses 'template' while the new editor uses 'multichannel'. Defaults to template.
    
</dd>
</dl>

<dl>
<dd>

**recipients:** `Optional<CreateCampaignsRequestRecipients>` — List settings for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**rssOpts:** `Optional<CreateCampaignsRequestRssOpts>` — [RSS](https://mailchimp.com/help/share-your-blog-posts-with-mailchimp/) options, specific to an RSS campaign.
    
</dd>
</dl>

<dl>
<dd>

**settings:** `Optional<CreateCampaignsRequestSettings>` — The settings for your campaign, including subject, from name, reply-to address, and more.
    
</dd>
</dl>

<dl>
<dd>

**socialCard:** `Optional<CreateCampaignsRequestSocialCard>` — The preview for the campaign, rendered by social networks like Facebook and Twitter. [Learn more](https://mailchimp.com/help/enable-and-customize-social-cards/).
    
</dd>
</dl>

<dl>
<dd>

**tracking:** `Optional<CampaignTrackingOptions>` 
    
</dd>
</dl>

<dl>
<dd>

**type:** `CreateCampaignsRequestType` — There are four types of [campaigns](https://mailchimp.com/help/getting-started-with-campaigns/) you can create in Mailchimp. A/B Split campaigns have been deprecated and variate campaigns should be used instead.
    
</dd>
</dl>

<dl>
<dd>

**variateSettings:** `Optional<CreateCampaignsRequestVariateSettings>` — The settings specific to A/B test campaigns.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.get(campaignId) -> Campaign</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().get(
    "campaign_id",
    GetCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**includeResendShortcutEligibility:** `Optional<Boolean>` — Return the `resend_shortcut_eligibility` field in the response, which tells you if the campaign is eligible for the various Campaign Resend Shortcuts offered.
    
</dd>
</dl>

<dl>
<dd>

**includeResendShortcutUsage:** `Optional<Boolean>` — Return the `resend_shortcut_usage` field in the response.  This includes information about campaigns related by a shortcut.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.delete(campaignId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a campaign from your Mailchimp account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().delete(
    "campaign_id",
    DeleteCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.update(campaignId, request) -> Campaign</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update some or all of the settings for a specific campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().update(
    "campaign_id",
    UpdateCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**recipients:** `Optional<UpdateCampaignsRequestRecipients>` — List settings for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**rssOpts:** `Optional<UpdateCampaignsRequestRssOpts>` — [RSS](https://mailchimp.com/help/share-your-blog-posts-with-mailchimp/) options for a campaign.
    
</dd>
</dl>

<dl>
<dd>

**settings:** `Optional<UpdateCampaignsRequestSettings>` — The settings for your campaign, including subject, from name, reply-to address, and more.
    
</dd>
</dl>

<dl>
<dd>

**socialCard:** `Optional<UpdateCampaignsRequestSocialCard>` — The preview for the campaign, rendered by social networks like Facebook and Twitter. [Learn more](https://mailchimp.com/help/enable-and-customize-social-cards/).
    
</dd>
</dl>

<dl>
<dd>

**tracking:** `Optional<CampaignTrackingOptions>` 
    
</dd>
</dl>

<dl>
<dd>

**variateSettings:** `Optional<UpdateCampaignsRequestVariateSettings>` — The settings specific to A/B test campaigns.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.createActionCancelSend(campaignId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cancel a Regular or Plain-Text Campaign after you send, before all of your recipients receive it. This feature is included with Mailchimp Pro.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().createActionCancelSend(
    "campaign_id",
    CreateActionCancelSendCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.createActionCreateResend(campaignId, request) -> Campaign</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove the guesswork for resending a campaign to certain segments. You can use this endpoint as a shortcut to replicate a campaign and resend it to common segments, such as those who didn't open the campaign, or any new subscribers since it was sent.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().createActionCreateResend(
    "campaign_id",
    CreateActionCreateResendCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**shortcutType:** `Optional<CreateActionCreateResendCampaignsRequestShortcutType>` — Which campaign resend shortcut to use. Default is `to_non_openers`.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.createActionPause(campaignId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Pause an RSS-Driven campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().createActionPause(
    "campaign_id",
    CreateActionPauseCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.createActionReplicate(campaignId) -> Campaign</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Replicate a campaign in saved or send status.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().createActionReplicate(
    "campaign_id",
    CreateActionReplicateCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.createActionResume(campaignId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Resume an RSS-Driven campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().createActionResume(
    "campaign_id",
    CreateActionResumeCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.createActionSchedule(campaignId, request)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Schedule a campaign for delivery. If you're using Multivariate Campaigns to test send times or sending RSS Campaigns, use the send action instead.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().createActionSchedule(
    "campaign_id",
    CreateActionScheduleCampaignsRequest
        .builder()
        .scheduleTime(OffsetDateTime.parse("2024-01-15T09:30:00Z"))
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**batchDelivery:** `Optional<CreateActionScheduleCampaignsRequestBatchDelivery>` — Choose whether the campaign should use [Batch Delivery](https://mailchimp.com/help/schedule-batch-delivery/). Cannot be set to `true` for campaigns using [Timewarp](https://mailchimp.com/help/use-timewarp/).
    
</dd>
</dl>

<dl>
<dd>

**scheduleTime:** `OffsetDateTime` — The UTC date and time to schedule the campaign for delivery in ISO 8601 format. Campaigns may only be scheduled to send on the quarter-hour (:00, :15, :30, :45).
    
</dd>
</dl>

<dl>
<dd>

**timewarp:** `Optional<Boolean>` — Choose whether the campaign should use [Timewarp](https://mailchimp.com/help/use-timewarp/) when sending. Campaigns scheduled with Timewarp are localized based on the recipients' time zones. For example, a Timewarp campaign with a `schedule_time` of 13:00 will be sent to each recipient at 1:00pm in their local time. Cannot be set to `true` for campaigns using [Batch Delivery](https://mailchimp.com/help/schedule-batch-delivery/).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.createActionSend(campaignId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send a Mailchimp campaign. For RSS Campaigns, the campaign will send according to its schedule. All other campaigns will send immediately.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().createActionSend(
    "campaign_id",
    CreateActionSendCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.createActionTest(campaignId, request)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send a test email.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().createActionTest(
    "campaign_id",
    CreateActionTestCampaignsRequest
        .builder()
        .sendType(CreateActionTestCampaignsRequestSendType.HTML)
        .testEmails(
            Arrays.asList("test_emails")
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**sendType:** `CreateActionTestCampaignsRequestSendType` — Choose the type of test email to send.
    
</dd>
</dl>

<dl>
<dd>

**testEmails:** `List<String>` — An array of email addresses to send the test email to.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.createActionUnschedule(campaignId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Unschedule a scheduled campaign that hasn't started sending.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().createActionUnschedule(
    "campaign_id",
    CreateActionUnscheduleCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.getContent(campaignId) -> CampaignContent</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the the HTML and plain-text content for a campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().getContent(
    "campaign_id",
    GetContentCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.upsertContent(campaignId, request) -> CampaignContent</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Set the content for a campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().upsertContent(
    "campaign_id",
    UpsertContentCampaignsRequest
        .builder()
        .body(
            CampaignContent
                .builder()
                .build()
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**request:** `CampaignContent` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.listFeedback(campaignId) -> ListFeedbackCampaignsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get team feedback while you're working together on a Mailchimp campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().listFeedback(
    "campaign_id",
    ListFeedbackCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.createFeedback(campaignId, request) -> CreateFeedbackCampaignsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add feedback on a specific campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().createFeedback(
    "campaign_id",
    CreateFeedbackCampaignsRequest
        .builder()
        .message("message")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**blockId:** `Optional<Integer>` — The block id for the editable block that the feedback addresses.
    
</dd>
</dl>

<dl>
<dd>

**isComplete:** `Optional<Boolean>` — The status of feedback.
    
</dd>
</dl>

<dl>
<dd>

**message:** `String` — The content of the feedback.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.getFeedback(campaignId, feedbackId) -> CampaignFeedback</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a specific feedback message from a campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().getFeedback(
    "campaign_id",
    "feedback_id",
    GetFeedbackCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**feedbackId:** `String` — The unique id for the feedback message.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.deleteFeedback(campaignId, feedbackId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a specific feedback message for a campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().deleteFeedback(
    "campaign_id",
    "feedback_id",
    DeleteFeedbackCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**feedbackId:** `String` — The unique id for the feedback message.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.updateFeedback(campaignId, feedbackId, request) -> CampaignFeedback</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a specific feedback message for a campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().updateFeedback(
    "campaign_id",
    "feedback_id",
    UpdateFeedbackCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**feedbackId:** `String` — The unique id for the feedback message.
    
</dd>
</dl>

<dl>
<dd>

**blockId:** `Optional<Integer>` — The block id for the editable block that the feedback addresses.
    
</dd>
</dl>

<dl>
<dd>

**isComplete:** `Optional<Boolean>` — The status of feedback.
    
</dd>
</dl>

<dl>
<dd>

**message:** `Optional<String>` — The content of the feedback.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.listSendChecklist(campaignId) -> ListSendChecklistCampaignsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Review the send checklist for a campaign, and resolve any issues before sending.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.campaigns().listSendChecklist(
    "campaign_id",
    ListSendChecklistCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## ConnectedSites
<details><summary><code>client.connectedSites.list() -> SyncPagingIterable&amp;lt;ConnectedSite&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get all connected sites in an account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.connectedSites().list(
    ListConnectedSitesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.connectedSites.create(request) -> ConnectedSite</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new Mailchimp connected site.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.connectedSites().create(
    CreateConnectedSitesRequest
        .builder()
        .domain("example.com")
        .foreignId("MC001")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domain:** `String` — The connected site domain.
    
</dd>
</dl>

<dl>
<dd>

**foreignId:** `String` — The unique identifier for the site.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.connectedSites.get(connectedSiteId) -> ConnectedSite</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific connected site.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.connectedSites().get(
    "connected_site_id",
    GetConnectedSitesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**connectedSiteId:** `String` — The unique identifier for the site.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.connectedSites.delete(connectedSiteId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a connected site from your Mailchimp account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.connectedSites().delete(
    "connected_site_id",
    DeleteConnectedSitesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**connectedSiteId:** `String` — The unique identifier for the site.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.connectedSites.createActionVerifyScriptInstallation(connectedSiteId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Verify that the connected sites script has been installed, either via the script URL or fragment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.connectedSites().createActionVerifyScriptInstallation(
    "connected_site_id",
    CreateActionVerifyScriptInstallationConnectedSitesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**connectedSiteId:** `String` — The unique identifier for the site.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## conversations
<details><summary><code>client.conversations.list() -> SyncPagingIterable&amp;lt;Conversation&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of conversations for the account. Conversations has been deprecated in favor of Inbox and these endpoints don't include Inbox data. Past Conversations are still available via this endpoint, but new campaign replies and other Inbox messages aren’t available using this endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.conversations().list(
    ListConversationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**hasUnreadMessages:** `Optional<ListConversationsRequestHasUnreadMessages>` — Whether the conversation has any unread messages.
    
</dd>
</dl>

<dl>
<dd>

**listId:** `Optional<String>` — The unique id for the list.
    
</dd>
</dl>

<dl>
<dd>

**campaignId:** `Optional<String>` — The unique id for the campaign.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.conversations.get(conversationId) -> Conversation</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get details about an individual conversation. Conversations has been deprecated in favor of Inbox and these endpoints don't include Inbox data. Past Conversations are still available via this endpoint, but new campaign replies and other Inbox messages aren’t available using this endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.conversations().get(
    "conversation_id",
    GetConversationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**conversationId:** `String` — The unique id for the conversation.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.conversations.listMessages(conversationId) -> ListMessagesConversationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get messages from a specific conversation. Conversations has been deprecated in favor of Inbox and these endpoints don't include Inbox data. Past Conversations are still available via this endpoint, but new campaign replies and other Inbox messages aren’t available using this endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.conversations().listMessages(
    "conversation_id",
    ListMessagesConversationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**conversationId:** `String` — The unique id for the conversation.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**isRead:** `Optional<ListMessagesConversationsRequestIsRead>` — Whether a conversation message has been marked as read.
    
</dd>
</dl>

<dl>
<dd>

**beforeTimestamp:** `Optional<OffsetDateTime>` — Restrict the response to messages created before the set time. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sinceTimestamp:** `Optional<OffsetDateTime>` — Restrict the response to messages created after the set time. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.conversations.getMessage(conversationId, messageId) -> ConversationMessage</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get an individual message in a conversation. Conversations has been deprecated in favor of Inbox and these endpoints don't include Inbox data. Past Conversations are still available via this endpoint, but new campaign replies and other Inbox messages aren’t available using this endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.conversations().getMessage(
    "conversation_id",
    "message_id",
    GetMessageConversationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**conversationId:** `String` — The unique id for the conversation.
    
</dd>
</dl>

<dl>
<dd>

**messageId:** `String` — The unique id for the conversation message.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## CustomerJourneys
<details><summary><code>client.customerJourneys.createJourneyStepActionTrigger(journeyId, stepId, request)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

A step trigger in an Automation flow. To use it, create a starting point or step from the Automation flow builder in the app using the Customer Journeys API condition. We’ll provide a url during the process that includes the {journey_id} and {step_id}. You’ll then be able to use this endpoint to trigger the condition for the posted contact.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.customerJourneys().createJourneyStepActionTrigger(
    1,
    1,
    CreateJourneyStepActionTriggerCustomerJourneysRequest
        .builder()
        .emailAddress("email_address")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**journeyId:** `Integer` — The id for the flow.
    
</dd>
</dl>

<dl>
<dd>

**stepId:** `Integer` — The id for the Step.
    
</dd>
</dl>

<dl>
<dd>

**emailAddress:** `String` — The list member's email address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## ecommerce
<details><summary><code>client.ecommerce.list() -> ListEcommerceResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about the e-commerce endpoint's resources.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().list();
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.listOrders() -> SyncPagingIterable&amp;lt;ECommerceOrder&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about an account's orders.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().listOrders(
    ListOrdersEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**campaignId:** `Optional<String>` — Restrict results to orders with a specific `campaign_id` value.
    
</dd>
</dl>

<dl>
<dd>

**outreachId:** `Optional<String>` — Restrict results to orders with a specific `outreach_id` value.
    
</dd>
</dl>

<dl>
<dd>

**customerId:** `Optional<String>` — Restrict results to orders made by a specific customer.
    
</dd>
</dl>

<dl>
<dd>

**hasOutreach:** `Optional<Boolean>` — Restrict results to orders that have an outreach attached. For example, an email campaign or Facebook ad.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.listStores() -> SyncPagingIterable&amp;lt;ECommerceStore&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about all stores in the account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().listStores(
    ListStoresEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.createStore(request) -> ECommerceStore</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a new store to your Mailchimp account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().createStore(
    CreateStoreEcommerceRequest
        .builder()
        .currencyCode("USD")
        .id("example_store")
        .listId("1a2df69511")
        .name("Freddie's Cat Hat Emporium")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**address:** `Optional<CreateStoreEcommerceRequestAddress>` — The store address.
    
</dd>
</dl>

<dl>
<dd>

**currencyCode:** `String` — The three-letter ISO 4217 code for the currency that the store accepts.
    
</dd>
</dl>

<dl>
<dd>

**domain:** `Optional<String>` — The store domain. This parameter is required for Connected Sites and Google Ads.
    
</dd>
</dl>

<dl>
<dd>

**emailAddress:** `Optional<String>` — The email address for the store.
    
</dd>
</dl>

<dl>
<dd>

**id:** `String` — The unique identifier for the store.
    
</dd>
</dl>

<dl>
<dd>

**isSyncing:** `Optional<Boolean>` — Whether to disable automations because the store is currently [syncing](https://mailchimp.com/developer/marketing/docs/e-commerce/#pausing-store-automations).
    
</dd>
</dl>

<dl>
<dd>

**listId:** `String` — The unique identifier for the list associated with the store. The `list_id` for a specific store cannot change.
    
</dd>
</dl>

<dl>
<dd>

**moneyFormat:** `Optional<String>` — The currency format for the store. For example: `$`, `£`, etc.
    
</dd>
</dl>

<dl>
<dd>

**name:** `String` — The name of the store.
    
</dd>
</dl>

<dl>
<dd>

**phone:** `Optional<String>` — The store phone number.
    
</dd>
</dl>

<dl>
<dd>

**platform:** `Optional<String>` — The e-commerce platform of the store.
    
</dd>
</dl>

<dl>
<dd>

**primaryLocale:** `Optional<String>` — The primary locale for the store. For example: `en`, `de`, etc.
    
</dd>
</dl>

<dl>
<dd>

**timezone:** `Optional<String>` — The timezone for the store.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.getStore(storeId) -> ECommerceStore</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific store.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().getStore(
    "store_id",
    GetStoreEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.deleteStore(storeId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a store. Deleting a store will also delete any associated subresources, including Customers, Orders, Products, and Carts.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().deleteStore(
    "store_id",
    DeleteStoreEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.updateStore(storeId, request) -> ECommerceStore</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a store.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().updateStore(
    "store_id",
    UpdateStoreEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**address:** `Optional<UpdateStoreEcommerceRequestAddress>` — The store address.
    
</dd>
</dl>

<dl>
<dd>

**currencyCode:** `Optional<String>` — The three-letter ISO 4217 code for the currency that the store accepts.
    
</dd>
</dl>

<dl>
<dd>

**domain:** `Optional<String>` — The store domain.
    
</dd>
</dl>

<dl>
<dd>

**emailAddress:** `Optional<String>` — The email address for the store.
    
</dd>
</dl>

<dl>
<dd>

**isSyncing:** `Optional<Boolean>` — Whether to disable automations because the store is currently [syncing](https://mailchimp.com/developer/marketing/docs/e-commerce/#pausing-store-automations).
    
</dd>
</dl>

<dl>
<dd>

**moneyFormat:** `Optional<String>` — The currency format for the store. For example: `$`, `£`, etc.
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — The name of the store.
    
</dd>
</dl>

<dl>
<dd>

**phone:** `Optional<String>` — The store phone number.
    
</dd>
</dl>

<dl>
<dd>

**platform:** `Optional<String>` — The e-commerce platform of the store.
    
</dd>
</dl>

<dl>
<dd>

**primaryLocale:** `Optional<String>` — The primary locale for the store. For example: `en`, `de`, etc.
    
</dd>
</dl>

<dl>
<dd>

**timezone:** `Optional<String>` — The timezone for the store.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.listStoreCarts(storeId) -> SyncPagingIterable&amp;lt;ECommerceCart&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a store's carts.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().listStoreCarts(
    "store_id",
    ListStoreCartsEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.createStoreCart(storeId, request) -> ECommerceCart</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a new cart to a store.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().createStoreCart(
    "store_id",
    CreateStoreCartEcommerceRequest
        .builder()
        .currencyCode("currency_code")
        .customer(
            EcommerceStoresCartsPost
                .builder()
                .id("id")
                .build()
        )
        .id(
            CreateStoreCartEcommerceRequestId.of("id")
        )
        .orderTotal(
            CreateStoreCartEcommerceRequestOrderTotal.of(1.1)
        )
        .lines(
            Arrays.asList(
                CreateStoreCartEcommerceRequestLinesItem
                    .builder()
                    .id("id")
                    .price(
                        CreateStoreCartEcommerceRequestLinesItemPrice.of(1.1)
                    )
                    .productId("product_id")
                    .productVariantId("product_variant_id")
                    .quantity(1)
                    .build()
            )
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**campaignId:** `Optional<String>` — A string that uniquely identifies the campaign for a cart.
    
</dd>
</dl>

<dl>
<dd>

**checkoutUrl:** `Optional<String>` — The URL for the cart. This parameter is required for [Abandoned Cart](https://mailchimp.com/help/create-a-classic-abandoned-cart-email/) automations.
    
</dd>
</dl>

<dl>
<dd>

**currencyCode:** `String` — The three-letter ISO 4217 code for the currency that the cart uses.
    
</dd>
</dl>

<dl>
<dd>

**customer:** `EcommerceStoresCartsPost` 
    
</dd>
</dl>

<dl>
<dd>

**id:** `CreateStoreCartEcommerceRequestId` — A unique identifier for the cart.
    
</dd>
</dl>

<dl>
<dd>

**lines:** `List<CreateStoreCartEcommerceRequestLinesItem>` — An array of the cart's line items.
    
</dd>
</dl>

<dl>
<dd>

**orderTotal:** `CreateStoreCartEcommerceRequestOrderTotal` 
    
</dd>
</dl>

<dl>
<dd>

**taxTotal:** `Optional<CreateStoreCartEcommerceRequestTaxTotal>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.getStoreCart(storeId, cartId) -> ECommerceCart</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific cart.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().getStoreCart(
    "store_id",
    "cart_id",
    GetStoreCartEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**cartId:** `String` — The id for the cart.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.deleteStoreCart(storeId, cartId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a cart.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().deleteStoreCart(
    "store_id",
    "cart_id",
    DeleteStoreCartEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**cartId:** `String` — The id for the cart.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.updateStoreCart(storeId, cartId, request) -> ECommerceCart</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a specific cart.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().updateStoreCart(
    "store_id",
    "cart_id",
    UpdateStoreCartEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**cartId:** `String` — The id for the cart.
    
</dd>
</dl>

<dl>
<dd>

**campaignId:** `Optional<String>` — A string that uniquely identifies the campaign associated with a cart.
    
</dd>
</dl>

<dl>
<dd>

**checkoutUrl:** `Optional<String>` — The URL for the cart. This parameter is required for [Abandoned Cart](https://mailchimp.com/help/create-a-classic-abandoned-cart-email/) automations.
    
</dd>
</dl>

<dl>
<dd>

**currencyCode:** `Optional<String>` — The three-letter ISO 4217 code for the currency that the cart uses.
    
</dd>
</dl>

<dl>
<dd>

**customer:** `Optional<EcommerceStoresCartsPatch>` 
    
</dd>
</dl>

<dl>
<dd>

**id:** `Optional<UpdateStoreCartEcommerceRequestId>` — A unique identifier for the cart.
    
</dd>
</dl>

<dl>
<dd>

**lines:** `Optional<List<UpdateStoreCartEcommerceRequestLinesItem>>` — An array of the cart's line items.
    
</dd>
</dl>

<dl>
<dd>

**orderTotal:** `Optional<UpdateStoreCartEcommerceRequestOrderTotal>` 
    
</dd>
</dl>

<dl>
<dd>

**taxTotal:** `Optional<UpdateStoreCartEcommerceRequestTaxTotal>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.listStoreCartLines(storeId, cartId) -> SyncPagingIterable&amp;lt;ECommerceCartLineItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a cart's line items.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().listStoreCartLines(
    "store_id",
    "cart_id",
    ListStoreCartLinesEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**cartId:** `String` — The id for the cart.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.createStoreCartLine(storeId, cartId, request) -> ECommerceCartLineItem</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a new line item to an existing cart.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().createStoreCartLine(
    "store_id",
    "cart_id",
    CreateStoreCartLineEcommerceRequest
        .builder()
        .id("id")
        .price(
            CreateStoreCartLineEcommerceRequestPrice.of(1.1)
        )
        .productId("product_id")
        .productVariantId("product_variant_id")
        .quantity(1)
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**cartId:** `String` — The id for the cart.
    
</dd>
</dl>

<dl>
<dd>

**id:** `String` — A unique identifier for the cart line item.
    
</dd>
</dl>

<dl>
<dd>

**price:** `CreateStoreCartLineEcommerceRequestPrice` 
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — A unique identifier for the product associated with the cart line item.
    
</dd>
</dl>

<dl>
<dd>

**productVariantId:** `String` — A unique identifier for the product variant associated with the cart line item.
    
</dd>
</dl>

<dl>
<dd>

**quantity:** `Integer` — The quantity of a cart line item.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.getStoreCartLine(storeId, cartId, lineId) -> ECommerceCartLineItem</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific cart line item.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().getStoreCartLine(
    "store_id",
    "cart_id",
    "line_id",
    GetStoreCartLineEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**cartId:** `String` — The id for the cart.
    
</dd>
</dl>

<dl>
<dd>

**lineId:** `String` — The id for the line item of a cart.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.deleteStoreCartLine(storeId, cartId, lineId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a specific cart line item.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().deleteStoreCartLine(
    "store_id",
    "cart_id",
    "line_id",
    DeleteStoreCartLineEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**cartId:** `String` — The id for the cart.
    
</dd>
</dl>

<dl>
<dd>

**lineId:** `String` — The id for the line item of a cart.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.updateStoreCartLine(storeId, cartId, lineId, request) -> ECommerceCartLineItem</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a specific cart line item.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().updateStoreCartLine(
    "store_id",
    "cart_id",
    "line_id",
    UpdateStoreCartLineEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**cartId:** `String` — The id for the cart.
    
</dd>
</dl>

<dl>
<dd>

**lineId:** `String` — The id for the line item of a cart.
    
</dd>
</dl>

<dl>
<dd>

**price:** `Optional<UpdateStoreCartLineEcommerceRequestPrice>` 
    
</dd>
</dl>

<dl>
<dd>

**productId:** `Optional<String>` — A unique identifier for the product associated with the cart line item.
    
</dd>
</dl>

<dl>
<dd>

**productVariantId:** `Optional<String>` — A unique identifier for the product variant associated with the cart line item.
    
</dd>
</dl>

<dl>
<dd>

**quantity:** `Optional<Integer>` — The quantity of a cart line item.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.listStoreCustomers(storeId) -> SyncPagingIterable&amp;lt;ECommerceCustomer&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a store's customers.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().listStoreCustomers(
    "store_id",
    ListStoreCustomersEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**emailAddress:** `Optional<String>` — Restrict the response to customers with the email address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.createStoreCustomer(storeId, request) -> ECommerceCustomer</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a new customer to a store.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().createStoreCustomer(
    "store_id",
    CreateStoreCustomerEcommerceRequest
        .builder()
        .id("id")
        .optInStatus(true)
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**address:** `Optional<CreateStoreCustomerEcommerceRequestAddress>` — The customer's address.
    
</dd>
</dl>

<dl>
<dd>

**company:** `Optional<String>` — The customer's company.
    
</dd>
</dl>

<dl>
<dd>

**emailAddress:** `Optional<String>` — The customer's email address.
    
</dd>
</dl>

<dl>
<dd>

**firstName:** `Optional<String>` — The customer's first name.
    
</dd>
</dl>

<dl>
<dd>

**id:** `String` — A unique identifier for the customer. Limited to 50 characters.
    
</dd>
</dl>

<dl>
<dd>

**lastName:** `Optional<String>` — The customer's last name.
    
</dd>
</dl>

<dl>
<dd>

**optInStatus:** `Boolean` — The customer's opt-in status. This value will never overwrite the opt-in status of a pre-existing Mailchimp list member, but will apply to list members that are added through the e-commerce API endpoints. Customers who don't opt in to your Mailchimp list [will be added as `Transactional` members](https://mailchimp.com/developer/marketing/docs/e-commerce/#customers).
    
</dd>
</dl>

<dl>
<dd>

**smsPhoneNumber:** `Optional<String>` — A US phone number for SMS contact.
    
</dd>
</dl>

<dl>
<dd>

**totalSpent:** `Optional<CreateStoreCustomerEcommerceRequestTotalSpent>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.getStoreCustomer(storeId, customerId) -> ECommerceCustomer</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific customer.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().getStoreCustomer(
    "store_id",
    "customer_id",
    GetStoreCustomerEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**customerId:** `String` — The id for the customer of a store.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.upsertStoreCustomer(storeId, customerId, request) -> ECommerceCustomer</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add or update a customer.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().upsertStoreCustomer(
    "store_id",
    "customer_id",
    UpsertStoreCustomerEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**customerId:** `String` — The id for the customer of a store.
    
</dd>
</dl>

<dl>
<dd>

**address:** `Optional<UpsertStoreCustomerEcommerceRequestAddress>` — The customer's address.
    
</dd>
</dl>

<dl>
<dd>

**company:** `Optional<String>` — The customer's company.
    
</dd>
</dl>

<dl>
<dd>

**emailAddress:** `Optional<String>` — The customer's email address.
    
</dd>
</dl>

<dl>
<dd>

**firstName:** `Optional<String>` — The customer's first name.
    
</dd>
</dl>

<dl>
<dd>

**id:** `Optional<String>` — A unique identifier for the customer. Limited to 50 characters.
    
</dd>
</dl>

<dl>
<dd>

**lastName:** `Optional<String>` — The customer's last name.
    
</dd>
</dl>

<dl>
<dd>

**optInStatus:** `Optional<Boolean>` — The customer's opt-in status. This value will never overwrite the opt-in status of a pre-existing Mailchimp list member, but will apply to list members that are added through the e-commerce API endpoints. Customers who don't opt in to your Mailchimp list [will be added as `Transactional` members](https://mailchimp.com/developer/marketing/docs/e-commerce/#customers).
    
</dd>
</dl>

<dl>
<dd>

**smsPhoneNumber:** `Optional<String>` — A US phone number for SMS contact.
    
</dd>
</dl>

<dl>
<dd>

**totalSpent:** `Optional<UpsertStoreCustomerEcommerceRequestTotalSpent>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.deleteStoreCustomer(storeId, customerId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a customer from a store.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().deleteStoreCustomer(
    "store_id",
    "customer_id",
    DeleteStoreCustomerEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**customerId:** `String` — The id for the customer of a store.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.updateStoreCustomer(storeId, customerId, request) -> ECommerceCustomer</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a customer.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().updateStoreCustomer(
    "store_id",
    "customer_id",
    UpdateStoreCustomerEcommerceRequest
        .builder()
        .body(
            EcommerceStoresCartsPatch
                .builder()
                .build()
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**customerId:** `String` — The id for the customer of a store.
    
</dd>
</dl>

<dl>
<dd>

**request:** `EcommerceStoresCartsPatch` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.listStoreOrders(storeId) -> SyncPagingIterable&amp;lt;ECommerceOrder&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a store's orders.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().listStoreOrders(
    "store_id",
    ListStoreOrdersEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**customerId:** `Optional<String>` — Restrict results to orders made by a specific customer.
    
</dd>
</dl>

<dl>
<dd>

**hasOutreach:** `Optional<Boolean>` — Restrict results to orders that have an outreach attached. For example, an email campaign or Facebook ad.
    
</dd>
</dl>

<dl>
<dd>

**campaignId:** `Optional<String>` — Restrict results to orders with a specific `campaign_id` value.
    
</dd>
</dl>

<dl>
<dd>

**outreachId:** `Optional<String>` — Restrict results to orders with a specific `outreach_id` value.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.createStoreOrder(storeId, request) -> ECommerceOrder</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a new order to a store.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().createStoreOrder(
    "store_id",
    CreateStoreOrderEcommerceRequest
        .builder()
        .currencyCode("currency_code")
        .customer(
            EcommerceStoresCartsPost
                .builder()
                .id("id")
                .build()
        )
        .id("id")
        .orderTotal(
            CreateStoreOrderEcommerceRequestOrderTotal.of(1.1)
        )
        .lines(
            Arrays.asList(
                CreateStoreOrderEcommerceRequestLinesItem
                    .builder()
                    .id("id")
                    .price(
                        CreateStoreOrderEcommerceRequestLinesItemPrice.of(1.1)
                    )
                    .productId("product_id")
                    .productVariantId("product_variant_id")
                    .quantity(1)
                    .build()
            )
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**billingAddress:** `Optional<CreateStoreOrderEcommerceRequestBillingAddress>` — The billing address for the order.
    
</dd>
</dl>

<dl>
<dd>

**campaignId:** `Optional<String>` — A string that uniquely identifies the campaign for an order.
    
</dd>
</dl>

<dl>
<dd>

**cartId:** `Optional<CreateStoreOrderEcommerceRequestCartId>` — A cart id that the order was placed for.
    
</dd>
</dl>

<dl>
<dd>

**cancelledAtForeign:** `Optional<String>` — The date and time the order was cancelled in ISO 8601 format. Note: passing a value for this parameter will cancel the order being created.
    
</dd>
</dl>

<dl>
<dd>

**currencyCode:** `String` — The three-letter ISO 4217 code for the currency that the store accepts.
    
</dd>
</dl>

<dl>
<dd>

**customer:** `EcommerceStoresCartsPost` 
    
</dd>
</dl>

<dl>
<dd>

**discountTotal:** `Optional<CreateStoreOrderEcommerceRequestDiscountTotal>` 
    
</dd>
</dl>

<dl>
<dd>

**financialStatus:** `Optional<String>` — The order status. Use this parameter to trigger [Order Notifications](https://mailchimp.com/developer/marketing/docs/e-commerce/#order-notifications).
    
</dd>
</dl>

<dl>
<dd>

**fulfillmentStatus:** `Optional<String>` — The fulfillment status for the order. Use this parameter to trigger [Order Notifications](https://mailchimp.com/developer/marketing/docs/e-commerce/#order-notifications).
    
</dd>
</dl>

<dl>
<dd>

**id:** `String` — A unique identifier for the order.
    
</dd>
</dl>

<dl>
<dd>

**landingSite:** `Optional<String>` — The URL for the page where the buyer landed when entering the shop.
    
</dd>
</dl>

<dl>
<dd>

**lines:** `List<CreateStoreOrderEcommerceRequestLinesItem>` — An array of the order's line items.
    
</dd>
</dl>

<dl>
<dd>

**orderTotal:** `CreateStoreOrderEcommerceRequestOrderTotal` 
    
</dd>
</dl>

<dl>
<dd>

**orderUrl:** `Optional<String>` — The URL for the order.
    
</dd>
</dl>

<dl>
<dd>

**outreach:** `Optional<CreateStoreOrderEcommerceRequestOutreach>` — The outreach associated with this order. For example, an email campaign or Facebook ad.
    
</dd>
</dl>

<dl>
<dd>

**processedAtForeign:** `Optional<String>` — The date and time the order was processed in ISO 8601 format.
    
</dd>
</dl>

<dl>
<dd>

**promos:** `Optional<List<CreateStoreOrderEcommerceRequestPromosItem>>` — The promo codes applied on the order
    
</dd>
</dl>

<dl>
<dd>

**shippingAddress:** `Optional<CreateStoreOrderEcommerceRequestShippingAddress>` — The shipping address for the order.
    
</dd>
</dl>

<dl>
<dd>

**shippingTotal:** `Optional<CreateStoreOrderEcommerceRequestShippingTotal>` 
    
</dd>
</dl>

<dl>
<dd>

**taxTotal:** `Optional<CreateStoreOrderEcommerceRequestTaxTotal>` 
    
</dd>
</dl>

<dl>
<dd>

**trackingCarrier:** `Optional<String>` — The tracking carrier associated with the order.
    
</dd>
</dl>

<dl>
<dd>

**trackingCode:** `Optional<CreateStoreOrderEcommerceRequestTrackingCode>` — The Mailchimp tracking code for the order. Uses the 'mc_tc' parameter in E-Commerce tracking URLs.
    
</dd>
</dl>

<dl>
<dd>

**trackingNumber:** `Optional<String>` — The tracking number associated with the order.
    
</dd>
</dl>

<dl>
<dd>

**trackingUrl:** `Optional<String>` — The tracking URL associated with the order.
    
</dd>
</dl>

<dl>
<dd>

**updatedAtForeign:** `Optional<String>` — The date and time the order was updated in ISO 8601 format.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.getStoreOrder(storeId, orderId) -> ECommerceOrder</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().getStoreOrder(
    "store_id",
    "order_id",
    GetStoreOrderEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**orderId:** `String` — The id for the order in a store.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.deleteStoreOrder(storeId, orderId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete an order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().deleteStoreOrder(
    "store_id",
    "order_id",
    DeleteStoreOrderEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**orderId:** `String` — The id for the order in a store.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.updateStoreOrder(storeId, orderId, request) -> ECommerceOrder</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a specific order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().updateStoreOrder(
    "store_id",
    "order_id",
    UpdateStoreOrderEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**orderId:** `String` — The id for the order in a store.
    
</dd>
</dl>

<dl>
<dd>

**billingAddress:** `Optional<UpdateStoreOrderEcommerceRequestBillingAddress>` — The billing address for the order.
    
</dd>
</dl>

<dl>
<dd>

**campaignId:** `Optional<String>` — A string that uniquely identifies the campaign associated with an order.
    
</dd>
</dl>

<dl>
<dd>

**cartId:** `Optional<UpdateStoreOrderEcommerceRequestCartId>` — A cart id that the order was placed for.
    
</dd>
</dl>

<dl>
<dd>

**cancelledAtForeign:** `Optional<String>` — The date and time the order was cancelled in ISO 8601 format. Note: passing a value for this parameter will cancel the order being edited.
    
</dd>
</dl>

<dl>
<dd>

**currencyCode:** `Optional<String>` — The three-letter ISO 4217 code for the currency that the store accepts.
    
</dd>
</dl>

<dl>
<dd>

**customer:** `Optional<EcommerceStoresCartsPatch>` 
    
</dd>
</dl>

<dl>
<dd>

**discountTotal:** `Optional<UpdateStoreOrderEcommerceRequestDiscountTotal>` 
    
</dd>
</dl>

<dl>
<dd>

**financialStatus:** `Optional<String>` — The order status. Use this parameter to trigger [Order Notifications](https://mailchimp.com/developer/marketing/docs/e-commerce/#order-notifications).
    
</dd>
</dl>

<dl>
<dd>

**fulfillmentStatus:** `Optional<String>` — The fulfillment status for the order. Use this parameter to trigger [Order Notifications](https://mailchimp.com/developer/marketing/docs/e-commerce/#order-notifications).
    
</dd>
</dl>

<dl>
<dd>

**id:** `Optional<String>` — A unique identifier for the order.
    
</dd>
</dl>

<dl>
<dd>

**landingSite:** `Optional<String>` — The URL for the page where the buyer landed when entering the shop.
    
</dd>
</dl>

<dl>
<dd>

**lines:** `Optional<List<UpdateStoreOrderEcommerceRequestLinesItem>>` — An array of the order's line items.
    
</dd>
</dl>

<dl>
<dd>

**orderTotal:** `Optional<UpdateStoreOrderEcommerceRequestOrderTotal>` 
    
</dd>
</dl>

<dl>
<dd>

**orderUrl:** `Optional<String>` — The URL for the order.
    
</dd>
</dl>

<dl>
<dd>

**outreach:** `Optional<UpdateStoreOrderEcommerceRequestOutreach>` — The outreach associated with this order. For example, an email campaign or Facebook ad.
    
</dd>
</dl>

<dl>
<dd>

**processedAtForeign:** `Optional<String>` — The date and time the order was processed in ISO 8601 format.
    
</dd>
</dl>

<dl>
<dd>

**promos:** `Optional<List<UpdateStoreOrderEcommerceRequestPromosItem>>` — The promo codes applied on the order. Note: Patch will completely replace the value of promos with the new one provided.
    
</dd>
</dl>

<dl>
<dd>

**shippingAddress:** `Optional<UpdateStoreOrderEcommerceRequestShippingAddress>` — The shipping address for the order.
    
</dd>
</dl>

<dl>
<dd>

**shippingTotal:** `Optional<UpdateStoreOrderEcommerceRequestShippingTotal>` 
    
</dd>
</dl>

<dl>
<dd>

**taxTotal:** `Optional<UpdateStoreOrderEcommerceRequestTaxTotal>` 
    
</dd>
</dl>

<dl>
<dd>

**trackingCarrier:** `Optional<String>` — The tracking carrier associated with the order.
    
</dd>
</dl>

<dl>
<dd>

**trackingCode:** `Optional<UpdateStoreOrderEcommerceRequestTrackingCode>` — The Mailchimp tracking code for the order. Uses the 'mc_tc' parameter in E-Commerce tracking URLs.
    
</dd>
</dl>

<dl>
<dd>

**trackingNumber:** `Optional<String>` — The tracking number associated with the order.
    
</dd>
</dl>

<dl>
<dd>

**trackingUrl:** `Optional<String>` — The tracking URL associated with the order.
    
</dd>
</dl>

<dl>
<dd>

**updatedAtForeign:** `Optional<String>` — The date and time the order was updated in ISO 8601 format.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.listStoreOrderLines(storeId, orderId) -> SyncPagingIterable&amp;lt;ECommerceOrderLineItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about an order's line items.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().listStoreOrderLines(
    "store_id",
    "order_id",
    ListStoreOrderLinesEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**orderId:** `String` — The id for the order in a store.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.createStoreOrderLine(storeId, orderId, request) -> ECommerceOrderLineItem</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a new line item to an existing order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().createStoreOrderLine(
    "store_id",
    "order_id",
    CreateStoreOrderLineEcommerceRequest
        .builder()
        .id("id")
        .price(
            CreateStoreOrderLineEcommerceRequestPrice.of(1.1)
        )
        .productId("product_id")
        .productVariantId("product_variant_id")
        .quantity(1)
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**orderId:** `String` — The id for the order in a store.
    
</dd>
</dl>

<dl>
<dd>

**discount:** `Optional<CreateStoreOrderLineEcommerceRequestDiscount>` 
    
</dd>
</dl>

<dl>
<dd>

**id:** `String` — A unique identifier for the order line item.
    
</dd>
</dl>

<dl>
<dd>

**price:** `CreateStoreOrderLineEcommerceRequestPrice` 
    
</dd>
</dl>

<dl>
<dd>

**product:** `Optional<EcommerceStoresOrdersPost>` 
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — A unique identifier for the product associated with the order line item.
    
</dd>
</dl>

<dl>
<dd>

**productVariantId:** `String` — A unique identifier for the product variant associated with the order line item.
    
</dd>
</dl>

<dl>
<dd>

**quantity:** `Integer` — The quantity of an order line item.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.getStoreOrderLine(storeId, orderId, lineId) -> ECommerceOrderLineItem</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific order line item.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().getStoreOrderLine(
    "store_id",
    "order_id",
    "line_id",
    GetStoreOrderLineEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**orderId:** `String` — The id for the order in a store.
    
</dd>
</dl>

<dl>
<dd>

**lineId:** `String` — The id for the line item of an order.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.deleteStoreOrderLine(storeId, orderId, lineId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a specific order line item.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().deleteStoreOrderLine(
    "store_id",
    "order_id",
    "line_id",
    DeleteStoreOrderLineEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**orderId:** `String` — The id for the order in a store.
    
</dd>
</dl>

<dl>
<dd>

**lineId:** `String` — The id for the line item of an order.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.updateStoreOrderLine(storeId, orderId, lineId, request) -> ECommerceOrderLineItem</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a specific order line item.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().updateStoreOrderLine(
    "store_id",
    "order_id",
    "line_id",
    UpdateStoreOrderLineEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**orderId:** `String` — The id for the order in a store.
    
</dd>
</dl>

<dl>
<dd>

**lineId:** `String` — The id for the line item of an order.
    
</dd>
</dl>

<dl>
<dd>

**discount:** `Optional<UpdateStoreOrderLineEcommerceRequestDiscount>` 
    
</dd>
</dl>

<dl>
<dd>

**id:** `Optional<String>` — A unique identifier for the order line item.
    
</dd>
</dl>

<dl>
<dd>

**price:** `Optional<UpdateStoreOrderLineEcommerceRequestPrice>` 
    
</dd>
</dl>

<dl>
<dd>

**productId:** `Optional<String>` — A unique identifier for the product associated with the order line item.
    
</dd>
</dl>

<dl>
<dd>

**productVariantId:** `Optional<String>` — A unique identifier for the product variant associated with the order line item.
    
</dd>
</dl>

<dl>
<dd>

**quantity:** `Optional<Integer>` — The quantity of an order line item.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.listStoreProducts(storeId) -> SyncPagingIterable&amp;lt;ECommerceProduct&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a store's products.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().listStoreProducts(
    "store_id",
    ListStoreProductsEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.createStoreProduct(storeId, request) -> ECommerceProduct</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a new product to a store.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().createStoreProduct(
    "store_id",
    CreateStoreProductEcommerceRequest
        .builder()
        .body(
            EcommerceStoresOrdersPost
                .builder()
                .id(
                    EcommerceStoresOrdersPostId.of("id")
                )
                .title("Cat Hat")
                .variants(
                    Arrays.asList(
                        EcommerceStoresOrdersPostVariantsItem
                            .builder()
                            .id(
                                EcommerceStoresOrdersPostVariantsItemId.of("id")
                            )
                            .title("Cat Hat")
                            .build()
                    )
                )
                .build()
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**request:** `EcommerceStoresOrdersPost` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.getStoreProduct(storeId, productId) -> ECommerceProduct</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific product.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().getStoreProduct(
    "store_id",
    "product_id",
    GetStoreProductEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — The id for the product of a store.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.upsertStoreProduct(storeId, productId, request) -> ECommerceProduct</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a specific product.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().upsertStoreProduct(
    "store_id",
    "product_id",
    UpsertStoreProductEcommerceRequest
        .builder()
        .id(
            UpsertStoreProductEcommerceRequestId.of("id")
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — The id for the product of a store.
    
</dd>
</dl>

<dl>
<dd>

**description:** `Optional<String>` — The description of a product.
    
</dd>
</dl>

<dl>
<dd>

**handle:** `Optional<String>` — The handle of a product.
    
</dd>
</dl>

<dl>
<dd>

**id:** `UpsertStoreProductEcommerceRequestId` — A unique identifier for the product.
    
</dd>
</dl>

<dl>
<dd>

**imageUrl:** `Optional<String>` — The image URL for a product.
    
</dd>
</dl>

<dl>
<dd>

**images:** `Optional<List<UpsertStoreProductEcommerceRequestImagesItem>>` — An array of the product's images.
    
</dd>
</dl>

<dl>
<dd>

**publishedAtForeign:** `Optional<String>` — The date and time the product was published.
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — The title of a product.
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<String>` — The type of product.
    
</dd>
</dl>

<dl>
<dd>

**url:** `Optional<String>` — The URL for a product.
    
</dd>
</dl>

<dl>
<dd>

**variants:** `Optional<List<UpsertStoreProductEcommerceRequestVariantsItem>>` — An array of the product's variants. At least one variant is required for each product. A variant can use the same `id` and `title` as the parent product.
    
</dd>
</dl>

<dl>
<dd>

**vendor:** `Optional<String>` — The vendor for a product.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.deleteStoreProduct(storeId, productId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a product.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().deleteStoreProduct(
    "store_id",
    "product_id",
    DeleteStoreProductEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — The id for the product of a store.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.updateStoreProduct(storeId, productId, request) -> ECommerceProduct</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a specific product.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().updateStoreProduct(
    "store_id",
    "product_id",
    UpdateStoreProductEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — The id for the product of a store.
    
</dd>
</dl>

<dl>
<dd>

**description:** `Optional<String>` — The description of a product.
    
</dd>
</dl>

<dl>
<dd>

**handle:** `Optional<String>` — The handle of a product.
    
</dd>
</dl>

<dl>
<dd>

**id:** `Optional<UpdateStoreProductEcommerceRequestId>` — A unique identifier for the product.
    
</dd>
</dl>

<dl>
<dd>

**imageUrl:** `Optional<String>` — The image URL for a product.
    
</dd>
</dl>

<dl>
<dd>

**images:** `Optional<List<UpdateStoreProductEcommerceRequestImagesItem>>` — An array of the product's images.
    
</dd>
</dl>

<dl>
<dd>

**publishedAtForeign:** `Optional<String>` — The date and time the product was published in ISO 8601 format.
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — The title of a product.
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<String>` — The type of product.
    
</dd>
</dl>

<dl>
<dd>

**url:** `Optional<String>` — The URL for a product.
    
</dd>
</dl>

<dl>
<dd>

**variants:** `Optional<List<UpdateStoreProductEcommerceRequestVariantsItem>>` — An array of the product's variants. At least one variant is required for each product. A variant can use the same `id` and `title` as the parent product.
    
</dd>
</dl>

<dl>
<dd>

**vendor:** `Optional<String>` — The vendor for a product.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.listStoreProductImages(storeId, productId) -> SyncPagingIterable&amp;lt;ListStoreProductImagesEcommerceResponseImagesItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a product's images.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().listStoreProductImages(
    "store_id",
    "product_id",
    ListStoreProductImagesEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — The id for the product of a store.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.createStoreProductImage(storeId, productId, request) -> CreateStoreProductImageEcommerceResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a new image to the product.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().createStoreProductImage(
    "store_id",
    "product_id",
    CreateStoreProductImageEcommerceRequest
        .builder()
        .id("id")
        .url("url")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — The id for the product of a store.
    
</dd>
</dl>

<dl>
<dd>

**id:** `String` — A unique identifier for the product image.
    
</dd>
</dl>

<dl>
<dd>

**url:** `String` — The URL for a product image.
    
</dd>
</dl>

<dl>
<dd>

**variantIds:** `Optional<List<CreateStoreProductImageEcommerceRequestVariantIdsItem>>` — The list of product variants using the image.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.getStoreProductImage(storeId, productId, imageId) -> GetStoreProductImageEcommerceResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific product image.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().getStoreProductImage(
    "store_id",
    "product_id",
    "image_id",
    GetStoreProductImageEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — The id for the product of a store.
    
</dd>
</dl>

<dl>
<dd>

**imageId:** `String` — The id for the product image.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.deleteStoreProductImage(storeId, productId, imageId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a product image.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().deleteStoreProductImage(
    "store_id",
    "product_id",
    "image_id",
    DeleteStoreProductImageEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — The id for the product of a store.
    
</dd>
</dl>

<dl>
<dd>

**imageId:** `String` — The id for the product image.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.updateStoreProductImage(storeId, productId, imageId, request) -> UpdateStoreProductImageEcommerceResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a product image.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().updateStoreProductImage(
    "store_id",
    "product_id",
    "image_id",
    UpdateStoreProductImageEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — The id for the product of a store.
    
</dd>
</dl>

<dl>
<dd>

**imageId:** `String` — The id for the product image.
    
</dd>
</dl>

<dl>
<dd>

**id:** `Optional<String>` — A unique identifier for the product image.
    
</dd>
</dl>

<dl>
<dd>

**url:** `Optional<String>` — The URL for a product image.
    
</dd>
</dl>

<dl>
<dd>

**variantIds:** `Optional<List<UpdateStoreProductImageEcommerceRequestVariantIdsItem>>` — The list of product variants using the image.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.listStoreProductVariants(storeId, productId) -> SyncPagingIterable&amp;lt;ECommerceProductVariant&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a product's variants.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().listStoreProductVariants(
    "store_id",
    "product_id",
    ListStoreProductVariantsEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — The id for the product of a store.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.createStoreProductVariant(storeId, productId, request) -> ECommerceProductVariant</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a new variant to the product.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().createStoreProductVariant(
    "store_id",
    "product_id",
    CreateStoreProductVariantEcommerceRequest
        .builder()
        .id(
            CreateStoreProductVariantEcommerceRequestId.of("id")
        )
        .title("Cat Hat")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — The id for the product of a store.
    
</dd>
</dl>

<dl>
<dd>

**backorders:** `Optional<String>` — The backorders of a product variant.
    
</dd>
</dl>

<dl>
<dd>

**id:** `CreateStoreProductVariantEcommerceRequestId` — A unique identifier for the product variant.
    
</dd>
</dl>

<dl>
<dd>

**imageUrl:** `Optional<String>` — The image URL for a product variant.
    
</dd>
</dl>

<dl>
<dd>

**inventoryQuantity:** `Optional<Integer>` — The inventory quantity of a product variant.
    
</dd>
</dl>

<dl>
<dd>

**price:** `Optional<CreateStoreProductVariantEcommerceRequestPrice>` 
    
</dd>
</dl>

<dl>
<dd>

**sku:** `Optional<String>` — The stock keeping unit (SKU) of a product variant.
    
</dd>
</dl>

<dl>
<dd>

**title:** `String` — The title of a product variant.
    
</dd>
</dl>

<dl>
<dd>

**url:** `Optional<String>` — The URL for a product variant.
    
</dd>
</dl>

<dl>
<dd>

**visibility:** `Optional<String>` — The visibility of a product variant.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.getStoreProductVariant(storeId, productId, variantId) -> ECommerceProductVariant</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific product variant.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().getStoreProductVariant(
    "store_id",
    "product_id",
    "variant_id",
    GetStoreProductVariantEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — The id for the product of a store.
    
</dd>
</dl>

<dl>
<dd>

**variantId:** `String` — The id for the product variant.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.upsertStoreProductVariant(storeId, productId, variantId, request) -> ECommerceProductVariant</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add or update a product variant.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().upsertStoreProductVariant(
    "store_id",
    "product_id",
    "variant_id",
    UpsertStoreProductVariantEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — The id for the product of a store.
    
</dd>
</dl>

<dl>
<dd>

**variantId:** `String` — The id for the product variant.
    
</dd>
</dl>

<dl>
<dd>

**backorders:** `Optional<String>` — The backorders of a product variant.
    
</dd>
</dl>

<dl>
<dd>

**id:** `Optional<String>` — A unique identifier for the product variant.
    
</dd>
</dl>

<dl>
<dd>

**imageUrl:** `Optional<String>` — The image URL for a product variant.
    
</dd>
</dl>

<dl>
<dd>

**inventoryQuantity:** `Optional<Integer>` — The inventory quantity of a product variant.
    
</dd>
</dl>

<dl>
<dd>

**price:** `Optional<UpsertStoreProductVariantEcommerceRequestPrice>` 
    
</dd>
</dl>

<dl>
<dd>

**sku:** `Optional<String>` — The stock keeping unit (SKU) of a product variant.
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — The title of a product variant.
    
</dd>
</dl>

<dl>
<dd>

**url:** `Optional<String>` — The URL for a product variant.
    
</dd>
</dl>

<dl>
<dd>

**visibility:** `Optional<String>` — The visibility of a product variant.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.deleteStoreProductVariant(storeId, productId, variantId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a product variant.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().deleteStoreProductVariant(
    "store_id",
    "product_id",
    "variant_id",
    DeleteStoreProductVariantEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — The id for the product of a store.
    
</dd>
</dl>

<dl>
<dd>

**variantId:** `String` — The id for the product variant.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.updateStoreProductVariant(storeId, productId, variantId, request) -> ECommerceProductVariant</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a product variant.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().updateStoreProductVariant(
    "store_id",
    "product_id",
    "variant_id",
    UpdateStoreProductVariantEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**productId:** `String` — The id for the product of a store.
    
</dd>
</dl>

<dl>
<dd>

**variantId:** `String` — The id for the product variant.
    
</dd>
</dl>

<dl>
<dd>

**backorders:** `Optional<String>` — The backorders of a product variant.
    
</dd>
</dl>

<dl>
<dd>

**imageUrl:** `Optional<String>` — The image URL for a product variant.
    
</dd>
</dl>

<dl>
<dd>

**inventoryQuantity:** `Optional<Integer>` — The inventory quantity of a product variant.
    
</dd>
</dl>

<dl>
<dd>

**price:** `Optional<UpdateStoreProductVariantEcommerceRequestPrice>` 
    
</dd>
</dl>

<dl>
<dd>

**sku:** `Optional<String>` — The stock keeping unit (SKU) of a product variant.
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — The title of a product variant.
    
</dd>
</dl>

<dl>
<dd>

**url:** `Optional<String>` — The URL for a product variant.
    
</dd>
</dl>

<dl>
<dd>

**visibility:** `Optional<String>` — The visibility of a product variant.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.listStorePromoRules(storeId) -> SyncPagingIterable&amp;lt;ECommercePromoRule&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a store's promo rules.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().listStorePromoRules(
    "store_id",
    ListStorePromoRulesEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.createStorePromoRule(storeId, request) -> ECommercePromoRule</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a new promo rule to a store.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().createStorePromoRule(
    "store_id",
    CreateStorePromoRuleEcommerceRequest
        .builder()
        .amount(
            CreateStorePromoRuleEcommerceRequestAmount.of(1.1)
        )
        .description("Save BIG during our summer sale!")
        .id("id")
        .target(CreateStorePromoRuleEcommerceRequestTarget.PER_ITEM)
        .type(CreateStorePromoRuleEcommerceRequestType.FIXED)
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**amount:** `CreateStorePromoRuleEcommerceRequestAmount` 
    
</dd>
</dl>

<dl>
<dd>

**createdAtForeign:** `Optional<String>` — The date and time the promotion was created in ISO 8601 format.
    
</dd>
</dl>

<dl>
<dd>

**description:** `String` — The description of a promotion restricted to UTF-8 characters with max length 255.
    
</dd>
</dl>

<dl>
<dd>

**enabled:** `Optional<Boolean>` — Whether the promo rule is currently enabled.
    
</dd>
</dl>

<dl>
<dd>

**endsAt:** `Optional<CreateStorePromoRuleEcommerceRequestEndsAt>` 
    
</dd>
</dl>

<dl>
<dd>

**id:** `String` — A unique identifier for the promo rule. If Ecommerce platform does not support promo rule, use promo code id as promo rule id. Restricted to UTF-8 characters with max length 50.
    
</dd>
</dl>

<dl>
<dd>

**startsAt:** `Optional<CreateStorePromoRuleEcommerceRequestStartsAt>` 
    
</dd>
</dl>

<dl>
<dd>

**target:** `CreateStorePromoRuleEcommerceRequestTarget` — The target that the discount applies to.
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — The title that will show up in promotion campaign. Restricted to UTF-8 characters with max length of 100 bytes.
    
</dd>
</dl>

<dl>
<dd>

**type:** `CreateStorePromoRuleEcommerceRequestType` — Type of discount. For free shipping set type to fixed.
    
</dd>
</dl>

<dl>
<dd>

**updatedAtForeign:** `Optional<String>` — The date and time the promotion was updated in ISO 8601 format.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.getStorePromoRule(storeId, promoRuleId) -> ECommercePromoRule</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific promo rule.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().getStorePromoRule(
    "store_id",
    "promo_rule_id",
    GetStorePromoRuleEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**promoRuleId:** `String` — The id for the promo rule of a store.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.deleteStorePromoRule(storeId, promoRuleId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a promo rule from a store.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().deleteStorePromoRule(
    "store_id",
    "promo_rule_id",
    DeleteStorePromoRuleEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**promoRuleId:** `String` — The id for the promo rule of a store.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.updateStorePromoRule(storeId, promoRuleId, request) -> ECommercePromoRule</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a promo rule.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().updateStorePromoRule(
    "store_id",
    "promo_rule_id",
    UpdateStorePromoRuleEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**promoRuleId:** `String` — The id for the promo rule of a store.
    
</dd>
</dl>

<dl>
<dd>

**amount:** `Optional<UpdateStorePromoRuleEcommerceRequestAmount>` 
    
</dd>
</dl>

<dl>
<dd>

**createdAtForeign:** `Optional<String>` — The date and time the promotion was created in ISO 8601 format.
    
</dd>
</dl>

<dl>
<dd>

**description:** `Optional<String>` — The description of a promotion restricted to UTF-8 characters with max length 255.
    
</dd>
</dl>

<dl>
<dd>

**enabled:** `Optional<Boolean>` — Whether the promo rule is currently enabled.
    
</dd>
</dl>

<dl>
<dd>

**endsAt:** `Optional<UpdateStorePromoRuleEcommerceRequestEndsAt>` 
    
</dd>
</dl>

<dl>
<dd>

**id:** `Optional<String>` — A unique identifier for the promo rule. If Ecommerce platform does not support promo rule, use promo code id as promo rule id. Restricted to UTF-8 characters with max length 50.
    
</dd>
</dl>

<dl>
<dd>

**startsAt:** `Optional<UpdateStorePromoRuleEcommerceRequestStartsAt>` 
    
</dd>
</dl>

<dl>
<dd>

**target:** `Optional<UpdateStorePromoRuleEcommerceRequestTarget>` — The target that the discount applies to.
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — The title that will show up in promotion campaign. Restricted to UTF-8 characters with max length of 100 bytes.
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<UpdateStorePromoRuleEcommerceRequestType>` — Type of discount. For free shipping set type to fixed.
    
</dd>
</dl>

<dl>
<dd>

**updatedAtForeign:** `Optional<String>` — The date and time the promotion was updated in ISO 8601 format.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.listStorePromoRulePromoCodes(storeId, promoRuleId) -> SyncPagingIterable&amp;lt;ECommercePromoCode&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a store's promo codes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().listStorePromoRulePromoCodes(
    "store_id",
    "promo_rule_id",
    ListStorePromoRulePromoCodesEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**promoRuleId:** `String` — The id for the promo rule of a store.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.createStorePromoRulePromoCode(storeId, promoRuleId, request) -> ECommercePromoCode</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a new promo code to a store.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().createStorePromoRulePromoCode(
    "store_id",
    "promo_rule_id",
    CreateStorePromoRulePromoCodeEcommerceRequest
        .builder()
        .code("summersale")
        .id("id")
        .redemptionUrl("A url that applies promo code directly at checkout or a url that points to sale page or store url")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**promoRuleId:** `String` — The id for the promo rule of a store.
    
</dd>
</dl>

<dl>
<dd>

**code:** `String` — The discount code. Restricted to UTF-8 characters with max length 50.
    
</dd>
</dl>

<dl>
<dd>

**createdAtForeign:** `Optional<String>` — The date and time the promotion was created in ISO 8601 format.
    
</dd>
</dl>

<dl>
<dd>

**enabled:** `Optional<Boolean>` — Whether the promo code is currently enabled.
    
</dd>
</dl>

<dl>
<dd>

**id:** `String` — A unique identifier for the promo code. Restricted to UTF-8 characters with max length 50.
    
</dd>
</dl>

<dl>
<dd>

**redemptionUrl:** `String` — The url that should be used in the promotion campaign restricted to UTF-8 characters with max length 2000.
    
</dd>
</dl>

<dl>
<dd>

**updatedAtForeign:** `Optional<String>` — The date and time the promotion was updated in ISO 8601 format.
    
</dd>
</dl>

<dl>
<dd>

**usageCount:** `Optional<Integer>` — Number of times promo code has been used.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.getStorePromoRulePromoCode(storeId, promoRuleId, promoCodeId) -> ECommercePromoCode</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific promo code.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().getStorePromoRulePromoCode(
    "store_id",
    "promo_rule_id",
    "promo_code_id",
    GetStorePromoRulePromoCodeEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**promoRuleId:** `String` — The id for the promo rule of a store.
    
</dd>
</dl>

<dl>
<dd>

**promoCodeId:** `String` — The id for the promo code of a store.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.deleteStorePromoRulePromoCode(storeId, promoRuleId, promoCodeId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a promo code from a store.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().deleteStorePromoRulePromoCode(
    "store_id",
    "promo_rule_id",
    "promo_code_id",
    DeleteStorePromoRulePromoCodeEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**promoRuleId:** `String` — The id for the promo rule of a store.
    
</dd>
</dl>

<dl>
<dd>

**promoCodeId:** `String` — The id for the promo code of a store.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.updateStorePromoRulePromoCode(storeId, promoRuleId, promoCodeId, request) -> ECommercePromoCode</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a promo code.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ecommerce().updateStorePromoRulePromoCode(
    "store_id",
    "promo_rule_id",
    "promo_code_id",
    UpdateStorePromoRulePromoCodeEcommerceRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**storeId:** `String` — The store id.
    
</dd>
</dl>

<dl>
<dd>

**promoRuleId:** `String` — The id for the promo rule of a store.
    
</dd>
</dl>

<dl>
<dd>

**promoCodeId:** `String` — The id for the promo code of a store.
    
</dd>
</dl>

<dl>
<dd>

**code:** `Optional<String>` — The discount code. Restricted to UTF-8 characters with max length 50.
    
</dd>
</dl>

<dl>
<dd>

**createdAtForeign:** `Optional<String>` — The date and time the promotion was created in ISO 8601 format.
    
</dd>
</dl>

<dl>
<dd>

**enabled:** `Optional<Boolean>` — Whether the promo code is currently enabled.
    
</dd>
</dl>

<dl>
<dd>

**id:** `Optional<String>` — A unique identifier for the promo code. Restricted to UTF-8 characters with max length 50.
    
</dd>
</dl>

<dl>
<dd>

**redemptionUrl:** `Optional<String>` — The url that should be used in the promotion campaign restricted to UTF-8 characters with max length 2000.
    
</dd>
</dl>

<dl>
<dd>

**updatedAtForeign:** `Optional<String>` — The date and time the promotion was updated in ISO 8601 format.
    
</dd>
</dl>

<dl>
<dd>

**usageCount:** `Optional<Integer>` — Number of times promo code has been used.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## FacebookAds
<details><summary><code>client.facebookAds.list() -> SyncPagingIterable&amp;lt;FacebookAds&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get list of Facebook ads.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.facebookAds().list(
    ListFacebookAdsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListFacebookAdsRequestSortField>` — Returns files sorted by the specified field.
    
</dd>
</dl>

<dl>
<dd>

**sortDir:** `Optional<ListFacebookAdsRequestSortDir>` — Determines the order direction for sorted results.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.facebookAds.get(outreachId) -> FacebookAds</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get details of a Facebook ad.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.facebookAds().get(
    "outreach_id",
    GetFacebookAdsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**outreachId:** `String` — The outreach id.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## FileManager
<details><summary><code>client.fileManager.list() -> List&amp;lt;ListFileManagerResponseItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about the file-manager endpoint's resources
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.fileManager().list();
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.fileManager.listFiles() -> SyncPagingIterable&amp;lt;GalleryFile&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of available images and files stored in the File Manager for the account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.fileManager().listFiles(
    ListFilesFileManagerRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<String>` — The file type for the File Manager file.
    
</dd>
</dl>

<dl>
<dd>

**createdBy:** `Optional<String>` — The Mailchimp account user who created the File Manager file.
    
</dd>
</dl>

<dl>
<dd>

**beforeCreatedAt:** `Optional<String>` — Restrict the response to files created before the set date. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sinceCreatedAt:** `Optional<String>` — Restrict the response to files created after the set date. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListFilesFileManagerRequestSortField>` — Returns files sorted by the specified field.
    
</dd>
</dl>

<dl>
<dd>

**sortDir:** `Optional<ListFilesFileManagerRequestSortDir>` — Determines the order direction for sorted results.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.fileManager.createFile(request) -> GalleryFile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Upload a new image or file to the File Manager.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.fileManager().createFile(
    CreateFileFileManagerRequest
        .builder()
        .fileData("file_data")
        .name("name")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fileData:** `String` — The base64-encoded contents of the file.
    
</dd>
</dl>

<dl>
<dd>

**folderId:** `Optional<Integer>` — The id of the folder.
    
</dd>
</dl>

<dl>
<dd>

**name:** `String` — The name of the file.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.fileManager.getFile(fileId) -> GalleryFile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific file in the File Manager.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.fileManager().getFile(
    "file_id",
    GetFileFileManagerRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fileId:** `String` — The unique id for the File Manager file.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.fileManager.deleteFile(fileId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a specific file from the File Manager.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.fileManager().deleteFile(
    "file_id",
    DeleteFileFileManagerRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fileId:** `String` — The unique id for the File Manager file.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.fileManager.updateFile(fileId, request) -> GalleryFile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a file in the File Manager.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.fileManager().updateFile(
    "file_id",
    UpdateFileFileManagerRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fileId:** `String` — The unique id for the File Manager file.
    
</dd>
</dl>

<dl>
<dd>

**folderId:** `Optional<Integer>` — The id of the folder. Setting `folder_id` to `0` will remove a file from its current folder.
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — The name of the file.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.fileManager.listFolders() -> SyncPagingIterable&amp;lt;ListFoldersFileManagerResponseFoldersItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of all folders in the File Manager.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.fileManager().listFolders(
    ListFoldersFileManagerRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**createdBy:** `Optional<String>` — The Mailchimp account user who created the File Manager file.
    
</dd>
</dl>

<dl>
<dd>

**beforeCreatedAt:** `Optional<String>` — Restrict the response to files created before the set date. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sinceCreatedAt:** `Optional<String>` — Restrict the response to files created after the set date. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.fileManager.createFolder(request) -> CreateFolderFileManagerResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new folder in the File Manager.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.fileManager().createFolder(
    CreateFolderFileManagerRequest
        .builder()
        .name("name")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `String` — The name of the folder.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.fileManager.getFolder(folderId) -> GetFolderFileManagerResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific folder in the File Manager.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.fileManager().getFolder(
    "folder_id",
    GetFolderFileManagerRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**folderId:** `String` — The unique id for the File Manager folder.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.fileManager.deleteFolder(folderId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a specific folder in the File Manager.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.fileManager().deleteFolder(
    "folder_id",
    DeleteFolderFileManagerRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**folderId:** `String` — The unique id for the File Manager folder.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.fileManager.updateFolder(folderId, request) -> UpdateFolderFileManagerResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a specific File Manager folder.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.fileManager().updateFolder(
    "folder_id",
    UpdateFolderFileManagerRequest
        .builder()
        .name("name")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**folderId:** `String` — The unique id for the File Manager folder.
    
</dd>
</dl>

<dl>
<dd>

**name:** `String` — The name of the folder.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.fileManager.listFolderFiles(folderId) -> SyncPagingIterable&amp;lt;GalleryFile&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of available images and files stored in this folder.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.fileManager().listFolderFiles(
    "folder_id",
    ListFolderFilesFileManagerRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**folderId:** `String` — The unique id for the File Manager folder.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<String>` — The file type for the File Manager file.
    
</dd>
</dl>

<dl>
<dd>

**createdBy:** `Optional<String>` — The Mailchimp account user who created the File Manager file.
    
</dd>
</dl>

<dl>
<dd>

**beforeCreatedAt:** `Optional<String>` — Restrict the response to files created before the set date. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sinceCreatedAt:** `Optional<String>` — Restrict the response to files created after the set date. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListFolderFilesFileManagerRequestSortField>` — Returns files sorted by the specified field.
    
</dd>
</dl>

<dl>
<dd>

**sortDir:** `Optional<ListFolderFilesFileManagerRequestSortDir>` — Determines the order direction for sorted results.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## LandingPages
<details><summary><code>client.landingPages.list() -> ListLandingPagesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get all landing pages.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.landingPages().list(
    ListLandingPagesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sortDir:** `Optional<ListLandingPagesRequestSortDir>` — Determines the order direction for sorted results.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListLandingPagesRequestSortField>` — Returns files sorted by the specified field.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.landingPages.create(request) -> LandingPage</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create an unpublished and contentless Mailchimp landing page.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.landingPages().create(
    CreateLandingPagesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**useDefaultList:** `Optional<Boolean>` — Will create the Landing Page using the account's Default List instead of requiring a list_id.
    
</dd>
</dl>

<dl>
<dd>

**description:** `Optional<String>` — The description of this landing page.
    
</dd>
</dl>

<dl>
<dd>

**listId:** `Optional<String>` — The list's ID associated with this landing page.
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — The name of this landing page.
    
</dd>
</dl>

<dl>
<dd>

**storeId:** `Optional<String>` — The ID of the store associated with this landing page.
    
</dd>
</dl>

<dl>
<dd>

**templateId:** `Optional<Integer>` — The template_id of this landing page.
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — The title of this landing page seen in the browser's title bar.
    
</dd>
</dl>

<dl>
<dd>

**tracking:** `Optional<CreateLandingPagesRequestTracking>` — The tracking settings applied to this landing page.
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<CreateLandingPagesRequestType>` — The type of template the landing page has.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.landingPages.get(pageId) -> LandingPage</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific page.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.landingPages().get(
    "page_id",
    GetLandingPagesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pageId:** `String` — The unique id for the page.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.landingPages.delete(pageId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a landing page.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.landingPages().delete(
    "page_id",
    DeleteLandingPagesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pageId:** `String` — The unique id for the page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.landingPages.update(pageId, request) -> LandingPage</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a landing page.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.landingPages().update(
    "page_id",
    UpdateLandingPagesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pageId:** `String` — The unique id for the page.
    
</dd>
</dl>

<dl>
<dd>

**description:** `Optional<String>` — The description of this landing page.
    
</dd>
</dl>

<dl>
<dd>

**listId:** `Optional<String>` — The list's ID associated with this landing page.
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — The name of this landing page.
    
</dd>
</dl>

<dl>
<dd>

**storeId:** `Optional<String>` — The ID of the store associated with this landing page.
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — The title of this landing page seen in the browser's title bar.
    
</dd>
</dl>

<dl>
<dd>

**tracking:** `Optional<UpdateLandingPagesRequestTracking>` — The tracking settings applied to this landing page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.landingPages.createActionPublish(pageId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Publish a landing page that is in draft, unpublished, or has been previously published and edited.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.landingPages().createActionPublish(
    "page_id",
    CreateActionPublishLandingPagesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pageId:** `String` — The unique id for the page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.landingPages.createActionUnpublish(pageId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Unpublish a landing page that is in draft or has been published.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.landingPages().createActionUnpublish(
    "page_id",
    CreateActionUnpublishLandingPagesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pageId:** `String` — The unique id for the page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.landingPages.listContent(pageId) -> ListContentLandingPagesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the the HTML for your landing page.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.landingPages().listContent(
    "page_id",
    ListContentLandingPagesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pageId:** `String` — The unique id for the page.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## lists
<details><summary><code>client.lists.list() -> SyncPagingIterable&amp;lt;SubscriberList&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about all lists in the account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().list(
    ListListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**beforeDateCreated:** `Optional<String>` — Restrict response to lists created before the set date. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sinceDateCreated:** `Optional<String>` — Restrict results to lists created after the set date. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**beforeCampaignLastSent:** `Optional<String>` — Restrict results to lists created before the last campaign send date. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sinceCampaignLastSent:** `Optional<String>` — Restrict results to lists created after the last campaign send date. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**email:** `Optional<String>` — Restrict results to lists that include a specific subscriber's email address.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListListsRequestSortField>` — Returns files sorted by the specified field.
    
</dd>
</dl>

<dl>
<dd>

**sortDir:** `Optional<ListListsRequestSortDir>` — Determines the order direction for sorted results.
    
</dd>
</dl>

<dl>
<dd>

**hasEcommerceStore:** `Optional<Boolean>` — Restrict results to lists that contain an active, connected, undeleted ecommerce store.
    
</dd>
</dl>

<dl>
<dd>

**includeTotalContacts:** `Optional<Boolean>` — Deprecated. Return the total_contacts field in the stats response, which contains an approximate count of subscribed, unsubscribed, and transactional contacts. For a complete audience contact count, use the /audiences endpoint instead.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.create(request) -> SubscriberList</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new list in your Mailchimp account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().create(
    CreateListsRequest
        .builder()
        .campaignDefaults(
            CreateListsRequestCampaignDefaults
                .builder()
                .fromEmail("from_email")
                .fromName("from_name")
                .language("language")
                .subject("subject")
                .build()
        )
        .contact(
            CreateListsRequestContact
                .builder()
                .address1("address1")
                .city("city")
                .company("company")
                .country("country")
                .build()
        )
        .emailTypeOption(true)
        .name("name")
        .permissionReminder("permission_reminder")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignDefaults:** `CreateListsRequestCampaignDefaults` — [Default values for campaigns](https://mailchimp.com/help/edit-your-emails-subject-preview-text-from-name-or-from-email-address/) created for this list.
    
</dd>
</dl>

<dl>
<dd>

**contact:** `CreateListsRequestContact` — [Contact information displayed in campaign footers](https://mailchimp.com/help/about-campaign-footers/) to comply with international spam laws.
    
</dd>
</dl>

<dl>
<dd>

**doubleOptin:** `Optional<Boolean>` — Whether or not to require the subscriber to confirm subscription via email.
    
</dd>
</dl>

<dl>
<dd>

**emailTypeOption:** `Boolean` — Whether the list supports [multiple formats for emails](https://mailchimp.com/help/audience-settings-and-defaults/). When set to `true`, subscribers can choose whether they want to receive HTML or plain-text emails. When set to `false`, subscribers will receive HTML emails, with a plain-text alternative backup.
    
</dd>
</dl>

<dl>
<dd>

**marketingPermissions:** `Optional<Boolean>` — Whether or not the list has marketing permissions (eg. GDPR) enabled.
    
</dd>
</dl>

<dl>
<dd>

**name:** `String` — The name of the list.
    
</dd>
</dl>

<dl>
<dd>

**notifyOnSubscribe:** `Optional<String>` — The email address to send [subscribe notifications](https://mailchimp.com/help/change-subscribe-and-unsubscribe-notifications/) to.
    
</dd>
</dl>

<dl>
<dd>

**notifyOnUnsubscribe:** `Optional<String>` — The email address to send [unsubscribe notifications](https://mailchimp.com/help/change-subscribe-and-unsubscribe-notifications/) to.
    
</dd>
</dl>

<dl>
<dd>

**permissionReminder:** `String` — The [permission reminder](https://mailchimp.com/help/edit-the-permission-reminder/) for the list.
    
</dd>
</dl>

<dl>
<dd>

**useArchiveBar:** `Optional<Boolean>` — Whether campaigns for this list use the [Archive Bar](https://mailchimp.com/help/about-email-campaign-archives-and-pages/) in archives by default.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.get(listId) -> SubscriberList</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific list in your Mailchimp account. Results include list members who have signed up but haven't confirmed their subscription yet and unsubscribed or cleaned.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().get(
    "list_id",
    GetListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**includeTotalContacts:** `Optional<Boolean>` — Deprecated. Return the total_contacts field in the stats response, which contains an approximate count of subscribed, unsubscribed, and transactional contacts. For a complete audience contact count, use the /audiences endpoint instead.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.batchSubscribeOrUnsubscribe(listId, request) -> BatchSubscribeOrUnsubscribeListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Batch subscribe or unsubscribe list members.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().batchSubscribeOrUnsubscribe(
    "list_id",
    BatchSubscribeOrUnsubscribeListsRequest
        .builder()
        .members(
            new ArrayList<BatchSubscribeOrUnsubscribeListsRequestMembersItem>()
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**skipMergeValidation:** `Optional<Boolean>` — If skip_merge_validation is true, member data will be accepted without merge field values, even if the merge field is usually required. This defaults to false.
    
</dd>
</dl>

<dl>
<dd>

**skipDuplicateCheck:** `Optional<Boolean>` — If skip_duplicate_check is true, we will ignore duplicates sent in the request when using the batch sub/unsub on the lists endpoint. The status of the first appearance in the request will be saved. This defaults to false.
    
</dd>
</dl>

<dl>
<dd>

**members:** `List<BatchSubscribeOrUnsubscribeListsRequestMembersItem>` — An array of objects, each representing an email address and the subscription status for a specific list. Up to 500 members may be added or updated with each API call.
    
</dd>
</dl>

<dl>
<dd>

**syncTags:** `Optional<Boolean>` — Whether this batch operation will replace all existing tags with tags in request.
    
</dd>
</dl>

<dl>
<dd>

**updateExisting:** `Optional<Boolean>` — Whether this batch operation will change existing members' subscription status.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.delete(listId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a list from your Mailchimp account. If you delete a list, you'll lose the list history—including subscriber activity, unsubscribes, complaints, and bounces. You’ll also lose subscribers’ email addresses, unless you exported and backed up your list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().delete(
    "list_id",
    DeleteListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.update(listId, request) -> SubscriberList</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update the settings for a specific list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().update(
    "list_id",
    UpdateListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**campaignDefaults:** `Optional<UpdateListsRequestCampaignDefaults>` — [Default values for campaigns](https://mailchimp.com/help/edit-your-emails-subject-preview-text-from-name-or-from-email-address/) created for this list.
    
</dd>
</dl>

<dl>
<dd>

**contact:** `Optional<UpdateListsRequestContact>` — [Contact information displayed in campaign footers](https://mailchimp.com/help/about-campaign-footers/) to comply with international spam laws.
    
</dd>
</dl>

<dl>
<dd>

**doubleOptin:** `Optional<Boolean>` — Whether or not to require the subscriber to confirm subscription via email.
    
</dd>
</dl>

<dl>
<dd>

**emailTypeOption:** `Optional<Boolean>` — Whether the list supports [multiple formats for emails](https://mailchimp.com/help/audience-settings-and-defaults/). When set to `true`, subscribers can choose whether they want to receive HTML or plain-text emails. When set to `false`, subscribers will receive HTML emails, with a plain-text alternative backup.
    
</dd>
</dl>

<dl>
<dd>

**marketingPermissions:** `Optional<Boolean>` — Whether or not the list has marketing permissions (eg. GDPR) enabled.
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — The name of the list.
    
</dd>
</dl>

<dl>
<dd>

**notifyOnSubscribe:** `Optional<String>` — The email address to send [subscribe notifications](https://mailchimp.com/help/change-subscribe-and-unsubscribe-notifications/) to.
    
</dd>
</dl>

<dl>
<dd>

**notifyOnUnsubscribe:** `Optional<String>` — The email address to send [unsubscribe notifications](https://mailchimp.com/help/change-subscribe-and-unsubscribe-notifications/) to.
    
</dd>
</dl>

<dl>
<dd>

**permissionReminder:** `Optional<String>` — The [permission reminder](https://mailchimp.com/help/edit-the-permission-reminder/) for the list.
    
</dd>
</dl>

<dl>
<dd>

**useArchiveBar:** `Optional<Boolean>` — Whether campaigns for this list use the [Archive Bar](https://mailchimp.com/help/about-email-campaign-archives-and-pages/) in archives by default.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listAbuseReports(listId) -> SyncPagingIterable&amp;lt;ListsAbuseReports&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get all abuse reports for a specific list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listAbuseReports(
    "list_id",
    ListAbuseReportsListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.getAbuseReport(listId, reportId) -> ListsAbuseReports</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get details about a specific abuse report.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().getAbuseReport(
    "list_id",
    "report_id",
    GetAbuseReportListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**reportId:** `String` — The id for the abuse report.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listActivity(listId) -> SyncPagingIterable&amp;lt;ListActivityListsResponseActivityItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get up to the previous 180 days of daily detailed aggregated activity stats for a list, not including Automation activity.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listActivity(
    "list_id",
    ListActivityListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listClients(listId) -> ListClientsListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of the top email clients based on user-agent strings.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listClients(
    "list_id",
    ListClientsListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listGrowthHistory(listId) -> SyncPagingIterable&amp;lt;GrowthHistory&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a month-by-month summary of a specific list's growth activity.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listGrowthHistory(
    "list_id",
    ListGrowthHistoryListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListGrowthHistoryListsRequestSortField>` — Returns files sorted by the specified field.
    
</dd>
</dl>

<dl>
<dd>

**sortDir:** `Optional<ListGrowthHistoryListsRequestSortDir>` — Determines the order direction for sorted results.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.getGrowthHistory(listId, month) -> GrowthHistory</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a summary of a specific list's growth activity for a specific month and year.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().getGrowthHistory(
    "list_id",
    "month",
    GetGrowthHistoryListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**month:** `String` — A specific month of list growth history.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listInterestCategories(listId) -> SyncPagingIterable&amp;lt;InterestCategory&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a list's interest categories.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listInterestCategories(
    "list_id",
    ListInterestCategoriesListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<String>` — Restrict results a type of interest group
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListInterestCategoriesListsRequestSortField>` — Returns interest categories sorted by the specified field. Defaults to display_order.
    
</dd>
</dl>

<dl>
<dd>

**sortDir:** `Optional<ListInterestCategoriesListsRequestSortDir>` — Determines the order direction for sorted results.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.createInterestCategory(listId, request) -> InterestCategory</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new interest category.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().createInterestCategory(
    "list_id",
    CreateInterestCategoryListsRequest
        .builder()
        .title("title")
        .type(CreateInterestCategoryListsRequestType.CHECKBOXES)
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**displayOrder:** `Optional<Integer>` — The order that the categories are displayed in the list. Lower numbers display first.
    
</dd>
</dl>

<dl>
<dd>

**title:** `String` — The text description of this category. This field appears on signup forms and is often phrased as a question.
    
</dd>
</dl>

<dl>
<dd>

**type:** `CreateInterestCategoryListsRequestType` — Determines how this category’s interests appear on signup forms.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.getInterestCategory(listId, interestCategoryId) -> InterestCategory</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific interest category.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().getInterestCategory(
    "list_id",
    "interest_category_id",
    GetInterestCategoryListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**interestCategoryId:** `String` — The unique ID for the interest category.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.deleteInterestCategory(listId, interestCategoryId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a specific interest category.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().deleteInterestCategory(
    "list_id",
    "interest_category_id",
    DeleteInterestCategoryListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**interestCategoryId:** `String` — The unique ID for the interest category.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.updateInterestCategory(listId, interestCategoryId, request) -> InterestCategory</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a specific interest category.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().updateInterestCategory(
    "list_id",
    "interest_category_id",
    UpdateInterestCategoryListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**interestCategoryId:** `String` — The unique ID for the interest category.
    
</dd>
</dl>

<dl>
<dd>

**displayOrder:** `Optional<Integer>` — The order that the categories are displayed in the list. Lower numbers display first.
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — The text description of this category. This field appears on signup forms and is often phrased as a question.
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<UpdateInterestCategoryListsRequestType>` — Determines how this category’s interests appear on signup forms.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listInterestCategoryInterests(listId, interestCategoryId) -> SyncPagingIterable&amp;lt;Interest&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of this category's interests.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listInterestCategoryInterests(
    "list_id",
    "interest_category_id",
    ListInterestCategoryInterestsListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**interestCategoryId:** `String` — The unique ID for the interest category.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.createInterestCategoryInterest(listId, interestCategoryId, request) -> Interest</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new interest or 'group name' for a specific category.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().createInterestCategoryInterest(
    "list_id",
    "interest_category_id",
    CreateInterestCategoryInterestListsRequest
        .builder()
        .name("name")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**interestCategoryId:** `String` — The unique ID for the interest category.
    
</dd>
</dl>

<dl>
<dd>

**displayOrder:** `Optional<Integer>` — The display order for interests.
    
</dd>
</dl>

<dl>
<dd>

**name:** `String` — The name of the interest. This can be shown publicly on a subscription form.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.getInterestCategoryInterest(listId, interestCategoryId, interestId) -> Interest</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get interests or 'group names' for a specific category.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().getInterestCategoryInterest(
    "list_id",
    "interest_category_id",
    "interest_id",
    GetInterestCategoryInterestListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**interestCategoryId:** `String` — The unique ID for the interest category.
    
</dd>
</dl>

<dl>
<dd>

**interestId:** `String` — The specific interest or 'group name'.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.deleteInterestCategoryInterest(listId, interestCategoryId, interestId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete interests or group names in a specific category.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().deleteInterestCategoryInterest(
    "list_id",
    "interest_category_id",
    "interest_id",
    DeleteInterestCategoryInterestListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**interestCategoryId:** `String` — The unique ID for the interest category.
    
</dd>
</dl>

<dl>
<dd>

**interestId:** `String` — The specific interest or 'group name'.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.updateInterestCategoryInterest(listId, interestCategoryId, interestId, request) -> Interest</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update interests or 'group names' for a specific category.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().updateInterestCategoryInterest(
    "list_id",
    "interest_category_id",
    "interest_id",
    UpdateInterestCategoryInterestListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**interestCategoryId:** `String` — The unique ID for the interest category.
    
</dd>
</dl>

<dl>
<dd>

**interestId:** `String` — The specific interest or 'group name'.
    
</dd>
</dl>

<dl>
<dd>

**displayOrder:** `Optional<Integer>` — The display order for interests.
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — The name of the interest. This can be shown publicly on a subscription form.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listLocations(listId) -> ListLocationsListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the locations (countries) that the list's subscribers have been tagged to based on geocoding their IP address.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listLocations(
    "list_id",
    ListLocationsListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listMembers(listId) -> SyncPagingIterable&amp;lt;ListMembers&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about members in a specific Mailchimp list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listMembers(
    "list_id",
    ListMembersListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**emailType:** `Optional<String>` — The email type.
    
</dd>
</dl>

<dl>
<dd>

**status:** `Optional<ListMembersListsRequestStatus>` — The subscriber's status.
    
</dd>
</dl>

<dl>
<dd>

**sinceTimestampOpt:** `Optional<String>` — Restrict results to subscribers who opted-in after the set timeframe. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**beforeTimestampOpt:** `Optional<String>` — Restrict results to subscribers who opted-in before the set timeframe. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sinceLastChanged:** `Optional<String>` — Restrict results to subscribers whose information changed after the set timeframe. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**beforeLastChanged:** `Optional<String>` — Restrict results to subscribers whose information changed before the set timeframe. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**uniqueEmailId:** `Optional<String>` — A unique identifier for the email address across all Mailchimp lists.
    
</dd>
</dl>

<dl>
<dd>

**vipOnly:** `Optional<Boolean>` — A filter to return only the list's VIP members. Passing `true` will restrict results to VIP list members, passing `false` will return all list members.
    
</dd>
</dl>

<dl>
<dd>

**interestCategoryId:** `Optional<String>` — The unique id for the interest category.
    
</dd>
</dl>

<dl>
<dd>

**interestIds:** `Optional<String>` — Used to filter list members by interests. Must be accompanied by interest_category_id and interest_match. The value must be a comma separated list of interest ids present for any supplied interest categories.
    
</dd>
</dl>

<dl>
<dd>

**interestMatch:** `Optional<ListMembersListsRequestInterestMatch>` — Used to filter list members by interests. Must be accompanied by interest_category_id and interest_ids. "any" will match a member with any of the interest supplied, "all" will only match members with every interest supplied, and "none" will match members without any of the interest supplied.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListMembersListsRequestSortField>` — Returns files sorted by the specified field.
    
</dd>
</dl>

<dl>
<dd>

**sortDir:** `Optional<ListMembersListsRequestSortDir>` — Determines the order direction for sorted results.
    
</dd>
</dl>

<dl>
<dd>

**sinceLastCampaign:** `Optional<Boolean>` — Filter subscribers by those subscribed/unsubscribed/pending/cleaned since last email campaign send. Member status is required to use this filter.
    
</dd>
</dl>

<dl>
<dd>

**unsubscribedSince:** `Optional<String>` — Filter subscribers by those unsubscribed since a specific date. Using any status other than unsubscribed with this filter will result in an error.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.createMember(listId, request) -> ListMembers</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a new member to the list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().createMember(
    "list_id",
    CreateMemberListsRequest
        .builder()
        .emailAddress("email_address")
        .status(CreateMemberListsRequestStatus.SUBSCRIBED)
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**skipMergeValidation:** `Optional<Boolean>` — If skip_merge_validation is true, member data will be accepted without merge field values, even if the merge field is usually required. This defaults to false.
    
</dd>
</dl>

<dl>
<dd>

**emailAddress:** `String` — Email address for a subscriber.
    
</dd>
</dl>

<dl>
<dd>

**emailType:** `Optional<String>` — Type of email this member asked to get ('html' or 'text').
    
</dd>
</dl>

<dl>
<dd>

**interests:** `Optional<Map<String, Boolean>>` — The key of this object's properties is the ID of the interest in question.
    
</dd>
</dl>

<dl>
<dd>

**ipOpt:** `Optional<String>` — The IP address the subscriber used to confirm their opt-in status.
    
</dd>
</dl>

<dl>
<dd>

**ipSignup:** `Optional<String>` — IP address the subscriber signed up from.
    
</dd>
</dl>

<dl>
<dd>

**language:** `Optional<String>` — If set/detected, the [subscriber's language](https://mailchimp.com/help/view-and-edit-contact-languages/).
    
</dd>
</dl>

<dl>
<dd>

**location:** `Optional<CreateMemberListsRequestLocation>` — Subscriber location information.
    
</dd>
</dl>

<dl>
<dd>

**marketingPermissions:** `Optional<List<CreateMemberListsRequestMarketingPermissionsItem>>` — The marketing permissions for the subscriber.
    
</dd>
</dl>

<dl>
<dd>

**mergeFields:** `Optional<Map<String, CreateMemberListsRequestMergeFieldsValue>>` — A dictionary of merge fields where the keys are the merge tags. See the [Merge Fields documentation](https://mailchimp.com/developer/marketing/docs/merge-fields/#structure) for more about the structure.
    
</dd>
</dl>

<dl>
<dd>

**status:** `CreateMemberListsRequestStatus` — Subscriber's current status.
    
</dd>
</dl>

<dl>
<dd>

**tags:** `Optional<List<String>>` — The tags that are associated with a member.
    
</dd>
</dl>

<dl>
<dd>

**timestampOpt:** `Optional<CreateMemberListsRequestTimestampOpt>` 
    
</dd>
</dl>

<dl>
<dd>

**timestampSignup:** `Optional<CreateMemberListsRequestTimestampSignup>` 
    
</dd>
</dl>

<dl>
<dd>

**vip:** `Optional<Boolean>` — [VIP status](https://mailchimp.com/help/designate-and-send-to-vip-contacts/) for subscriber.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.getMember(listId, subscriberHash) -> ListMembers</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific list member, including a currently subscribed, unsubscribed, or bounced member.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().getMember(
    "list_id",
    "subscriber_hash",
    GetMemberListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address. This endpoint also accepts a list member's email address or contact_id.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.upsertMember(listId, subscriberHash, request) -> ListMembers</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add or update a list member.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().upsertMember(
    "list_id",
    "subscriber_hash",
    UpsertMemberListsRequest
        .builder()
        .emailAddress("email_address")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address. This endpoint also accepts a list member's email address or contact_id.
    
</dd>
</dl>

<dl>
<dd>

**skipMergeValidation:** `Optional<Boolean>` — If skip_merge_validation is true, member data will be accepted without merge field values, even if the merge field is usually required. This defaults to false.
    
</dd>
</dl>

<dl>
<dd>

**emailAddress:** `String` — Email address for a subscriber. This value is required only if the email address is not already present on the list.
    
</dd>
</dl>

<dl>
<dd>

**emailType:** `Optional<String>` — Type of email this member asked to get ('html' or 'text').
    
</dd>
</dl>

<dl>
<dd>

**interests:** `Optional<Map<String, Boolean>>` — The key of this object's properties is the ID of the interest in question.
    
</dd>
</dl>

<dl>
<dd>

**ipOpt:** `Optional<String>` — The IP address the subscriber used to confirm their opt-in status.
    
</dd>
</dl>

<dl>
<dd>

**ipSignup:** `Optional<String>` — IP address the subscriber signed up from.
    
</dd>
</dl>

<dl>
<dd>

**language:** `Optional<String>` — If set/detected, the [subscriber's language](https://mailchimp.com/help/view-and-edit-contact-languages/).
    
</dd>
</dl>

<dl>
<dd>

**location:** `Optional<UpsertMemberListsRequestLocation>` — Subscriber location information.
    
</dd>
</dl>

<dl>
<dd>

**marketingPermissions:** `Optional<List<UpsertMemberListsRequestMarketingPermissionsItem>>` — The marketing permissions for the subscriber.
    
</dd>
</dl>

<dl>
<dd>

**mergeFields:** `Optional<Map<String, UpsertMemberListsRequestMergeFieldsValue>>` — A dictionary of merge fields where the keys are the merge tags. See the [Merge Fields documentation](https://mailchimp.com/developer/marketing/docs/merge-fields/#structure) for more about the structure.
    
</dd>
</dl>

<dl>
<dd>

**status:** `Optional<UpsertMemberListsRequestStatus>` — Subscriber's current status.
    
</dd>
</dl>

<dl>
<dd>

**statusIfNew:** `Optional<UpsertMemberListsRequestStatusIfNew>` — Subscriber's status. This value is required only if the email address is not already present on the list.
    
</dd>
</dl>

<dl>
<dd>

**tags:** `Optional<List<String>>` — The tags that are associated with a member.
    
</dd>
</dl>

<dl>
<dd>

**timestampOpt:** `Optional<UpsertMemberListsRequestTimestampOpt>` 
    
</dd>
</dl>

<dl>
<dd>

**timestampSignup:** `Optional<UpsertMemberListsRequestTimestampSignup>` 
    
</dd>
</dl>

<dl>
<dd>

**vip:** `Optional<Boolean>` — [VIP status](https://mailchimp.com/help/designate-and-send-to-vip-contacts/) for subscriber.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.deleteMember(listId, subscriberHash)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Archive a list member. To permanently delete, use the delete-permanent action.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().deleteMember(
    "list_id",
    "subscriber_hash",
    DeleteMemberListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address. This endpoint also accepts a list member's email address or contact_id.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.updateMember(listId, subscriberHash, request) -> ListMembers</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update information for a specific list member.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().updateMember(
    "list_id",
    "subscriber_hash",
    UpdateMemberListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address. This endpoint also accepts a list member's email address or contact_id.
    
</dd>
</dl>

<dl>
<dd>

**skipMergeValidation:** `Optional<Boolean>` — If skip_merge_validation is true, member data will be accepted without merge field values, even if the merge field is usually required. This defaults to false.
    
</dd>
</dl>

<dl>
<dd>

**emailAddress:** `Optional<String>` — Email address for a subscriber.
    
</dd>
</dl>

<dl>
<dd>

**emailType:** `Optional<String>` — Type of email this member asked to get ('html' or 'text').
    
</dd>
</dl>

<dl>
<dd>

**interests:** `Optional<Map<String, Boolean>>` — The key of this object's properties is the ID of the interest in question.
    
</dd>
</dl>

<dl>
<dd>

**ipOpt:** `Optional<String>` — The IP address the subscriber used to confirm their opt-in status.
    
</dd>
</dl>

<dl>
<dd>

**ipSignup:** `Optional<String>` — IP address the subscriber signed up from.
    
</dd>
</dl>

<dl>
<dd>

**language:** `Optional<String>` — If set/detected, the [subscriber's language](https://mailchimp.com/help/view-and-edit-contact-languages/).
    
</dd>
</dl>

<dl>
<dd>

**location:** `Optional<UpdateMemberListsRequestLocation>` — Subscriber location information.
    
</dd>
</dl>

<dl>
<dd>

**marketingPermissions:** `Optional<List<UpdateMemberListsRequestMarketingPermissionsItem>>` — The marketing permissions for the subscriber.
    
</dd>
</dl>

<dl>
<dd>

**mergeFields:** `Optional<Map<String, UpdateMemberListsRequestMergeFieldsValue>>` — A dictionary of merge fields where the keys are the merge tags. See the [Merge Fields documentation](https://mailchimp.com/developer/marketing/docs/merge-fields/#structure) for more about the structure.
    
</dd>
</dl>

<dl>
<dd>

**status:** `Optional<UpdateMemberListsRequestStatus>` — Subscriber's current status.
    
</dd>
</dl>

<dl>
<dd>

**timestampOpt:** `Optional<UpdateMemberListsRequestTimestampOpt>` 
    
</dd>
</dl>

<dl>
<dd>

**timestampSignup:** `Optional<UpdateMemberListsRequestTimestampSignup>` 
    
</dd>
</dl>

<dl>
<dd>

**vip:** `Optional<Boolean>` — [VIP status](https://mailchimp.com/help/designate-and-send-to-vip-contacts/) for subscriber.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.createMemberActionDeletePermanent(listId, subscriberHash)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete all personally identifiable information related to a list member, and remove them from a list. This will make it impossible to re-import the list member.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().createMemberActionDeletePermanent(
    "list_id",
    "subscriber_hash",
    CreateMemberActionDeletePermanentListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listMemberActivity(listId, subscriberHash) -> ListMemberActivityListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the last 50 events of a member's activity on a specific list, including opens, clicks, and unsubscribes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listMemberActivity(
    "list_id",
    "subscriber_hash",
    ListMemberActivityListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address. This endpoint also accepts a list member's email address or contact_id.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**action:** `Optional<ListMemberActivityListsRequestActionItem>` — A comma seperated list of actions to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listMemberActivityFeed(listId, subscriberHash) -> SyncPagingIterable&amp;lt;Object&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a member's activity on a specific list, including opens, clicks, and unsubscribes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listMemberActivityFeed(
    "list_id",
    "subscriber_hash",
    ListMemberActivityFeedListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address. This endpoint also accepts a list member's email address or contact_id.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**activityFilters:** `Optional<ListMemberActivityFeedListsRequestActivityFiltersItem>` — A comma-separated list of activity filters that correspond to a set of activity types, e.g "?activity_filters=open,bounce,click".
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listMemberEvents(listId, subscriberHash) -> SyncPagingIterable&amp;lt;ListMemberEventsListsResponseEventsItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get events for a contact.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listMemberEvents(
    "list_id",
    "subscriber_hash",
    ListMemberEventsListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address. This endpoint also accepts a list member's email address or contact_id.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.createMemberEvent(listId, subscriberHash, request)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add an event for a list member.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().createMemberEvent(
    "list_id",
    "subscriber_hash",
    CreateMemberEventListsRequest
        .builder()
        .name("name")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address. This endpoint also accepts a list member's email address or contact_id.
    
</dd>
</dl>

<dl>
<dd>

**isSyncing:** `Optional<Boolean>` — Events created with the is_syncing value set to `true` will not trigger automations.
    
</dd>
</dl>

<dl>
<dd>

**name:** `String` — The name for this type of event ('purchased', 'visited', etc). Must be 2-30 characters in length
    
</dd>
</dl>

<dl>
<dd>

**occurredAt:** `Optional<OffsetDateTime>` — The date and time the event occurred in ISO 8601 format.
    
</dd>
</dl>

<dl>
<dd>

**properties:** `Optional<Map<String, String>>` — An optional list of properties
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listMemberGoals(listId, subscriberHash) -> ListMemberGoalsListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the last 50 Goal events for a member on a specific list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listMemberGoals(
    "list_id",
    "subscriber_hash",
    ListMemberGoalsListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address. This endpoint also accepts a list member's email address or contact_id.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listMemberNotes(listId, subscriberHash) -> SyncPagingIterable&amp;lt;MemberNotes&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get recent notes for a specific list member.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listMemberNotes(
    "list_id",
    "subscriber_hash",
    ListMemberNotesListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListMemberNotesListsRequestSortField>` — Returns notes sorted by the specified field.
    
</dd>
</dl>

<dl>
<dd>

**sortDir:** `Optional<ListMemberNotesListsRequestSortDir>` — Determines the order direction for sorted results.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.createMemberNote(listId, subscriberHash, request) -> MemberNotes</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a new note for a specific subscriber.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().createMemberNote(
    "list_id",
    "subscriber_hash",
    CreateMemberNoteListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address.
    
</dd>
</dl>

<dl>
<dd>

**note:** `Optional<String>` — The content of the note. Note length is limited to 1,000 characters.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.getMemberNote(listId, subscriberHash, noteId) -> MemberNotes</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a specific note for a specific list member.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().getMemberNote(
    "list_id",
    "subscriber_hash",
    "note_id",
    GetMemberNoteListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address. This endpoint also accepts a list member's email address or contact_id.
    
</dd>
</dl>

<dl>
<dd>

**noteId:** `String` — The id for the note.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.deleteMemberNote(listId, subscriberHash, noteId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a specific note for a specific list member.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().deleteMemberNote(
    "list_id",
    "subscriber_hash",
    "note_id",
    DeleteMemberNoteListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address. This endpoint also accepts a list member's email address or contact_id.
    
</dd>
</dl>

<dl>
<dd>

**noteId:** `String` — The id for the note.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.updateMemberNote(listId, subscriberHash, noteId, request) -> MemberNotes</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a specific note for a specific list member.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().updateMemberNote(
    "list_id",
    "subscriber_hash",
    "note_id",
    UpdateMemberNoteListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address. This endpoint also accepts a list member's email address or contact_id.
    
</dd>
</dl>

<dl>
<dd>

**noteId:** `String` — The id for the note.
    
</dd>
</dl>

<dl>
<dd>

**note:** `Optional<String>` — The content of the note. Note length is limited to 1,000 characters.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listMemberTags(listId, subscriberHash) -> SyncPagingIterable&amp;lt;ListMemberTagsListsResponseTagsItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the tags on a list member.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listMemberTags(
    "list_id",
    "subscriber_hash",
    ListMemberTagsListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address. This endpoint also accepts a list member's email address or contact_id.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.createMemberTag(listId, subscriberHash, request)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add or remove tags from a list member. If a tag that does not exist is passed in and set as 'active', a new tag will be created.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().createMemberTag(
    "list_id",
    "subscriber_hash",
    CreateMemberTagListsRequest
        .builder()
        .tags(
            Arrays.asList(
                CreateMemberTagListsRequestTagsItem
                    .builder()
                    .name("name")
                    .status(CreateMemberTagListsRequestTagsItemStatus.INACTIVE)
                    .build()
            )
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address.
    
</dd>
</dl>

<dl>
<dd>

**isSyncing:** `Optional<Boolean>` — When is_syncing is true, automations based on the tags in the request will not fire
    
</dd>
</dl>

<dl>
<dd>

**tags:** `List<CreateMemberTagListsRequestTagsItem>` — A list of tags assigned to the list member.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listMergeFields(listId) -> SyncPagingIterable&amp;lt;MergeField&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of all merge fields for an audience.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listMergeFields(
    "list_id",
    ListMergeFieldsListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<String>` — The merge field type.
    
</dd>
</dl>

<dl>
<dd>

**required:** `Optional<Boolean>` — Whether it's a required merge field.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.createMergeField(listId, request) -> MergeField</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a new merge field for a specific audience.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().createMergeField(
    "list_id",
    CreateMergeFieldListsRequest
        .builder()
        .name("name")
        .type(CreateMergeFieldListsRequestType.TEXT)
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**defaultValue:** `Optional<String>` — The default value for the merge field if `null`.
    
</dd>
</dl>

<dl>
<dd>

**displayOrder:** `Optional<Integer>` — The order that the merge field displays on the list signup form.
    
</dd>
</dl>

<dl>
<dd>

**helpText:** `Optional<String>` — Extra text to help the subscriber fill out the form.
    
</dd>
</dl>

<dl>
<dd>

**name:** `String` — The name of the merge field (audience field).
    
</dd>
</dl>

<dl>
<dd>

**options:** `Optional<CreateMergeFieldListsRequestOptions>` — Extra options for some merge field types.
    
</dd>
</dl>

<dl>
<dd>

**public_:** `Optional<Boolean>` — Whether the merge field is displayed on the signup form.
    
</dd>
</dl>

<dl>
<dd>

**required:** `Optional<Boolean>` — Whether the merge field is required to import a contact.
    
</dd>
</dl>

<dl>
<dd>

**tag:** `Optional<String>` — The merge tag used for Mailchimp campaigns and [adding contact information](https://mailchimp.com/developer/marketing/docs/merge-fields/#add-merge-data-to-contacts).
    
</dd>
</dl>

<dl>
<dd>

**type:** `CreateMergeFieldListsRequestType` — The [type](https://mailchimp.com/developer/marketing/docs/merge-fields/#structure) for the merge field.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.getMergeField(listId, mergeId) -> MergeField</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific merge field.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().getMergeField(
    "list_id",
    "merge_id",
    GetMergeFieldListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**mergeId:** `String` — The id for the merge field.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.deleteMergeField(listId, mergeId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a specific merge field.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().deleteMergeField(
    "list_id",
    "merge_id",
    DeleteMergeFieldListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**mergeId:** `String` — The id for the merge field.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.updateMergeField(listId, mergeId, request) -> MergeField</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a specific merge field.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().updateMergeField(
    "list_id",
    "merge_id",
    UpdateMergeFieldListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**mergeId:** `String` — The id for the merge field.
    
</dd>
</dl>

<dl>
<dd>

**defaultValue:** `Optional<String>` — The default value for the merge field if `null`.
    
</dd>
</dl>

<dl>
<dd>

**displayOrder:** `Optional<Integer>` — The order that the merge field displays on the list signup form.
    
</dd>
</dl>

<dl>
<dd>

**helpText:** `Optional<String>` — Extra text to help the subscriber fill out the form.
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — The name of the merge field (audience field).
    
</dd>
</dl>

<dl>
<dd>

**options:** `Optional<UpdateMergeFieldListsRequestOptions>` — Extra options for some merge field types.
    
</dd>
</dl>

<dl>
<dd>

**public_:** `Optional<Boolean>` — Whether the merge field is displayed on the signup form.
    
</dd>
</dl>

<dl>
<dd>

**required:** `Optional<Boolean>` — Whether the merge field is required to import a contact.
    
</dd>
</dl>

<dl>
<dd>

**tag:** `Optional<String>` — The merge tag used for Mailchimp campaigns and [adding contact information](https://mailchimp.com/developer/marketing/docs/merge-fields/#add-merge-data-to-contacts).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listSegments(listId) -> SyncPagingIterable&amp;lt;List&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about all available segments for a specific list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listSegments(
    "list_id",
    ListSegmentsListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<String>` — Limit results based on segment type.
    
</dd>
</dl>

<dl>
<dd>

**sinceCreatedAt:** `Optional<String>` — Restrict results to segments created after the set time. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**beforeCreatedAt:** `Optional<String>` — Restrict results to segments created before the set time. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**includeCleaned:** `Optional<Boolean>` — Include cleaned members in response
    
</dd>
</dl>

<dl>
<dd>

**includeTransactional:** `Optional<Boolean>` — Include transactional members in response
    
</dd>
</dl>

<dl>
<dd>

**includeUnsubscribed:** `Optional<Boolean>` — Include unsubscribed members in response
    
</dd>
</dl>

<dl>
<dd>

**sinceUpdatedAt:** `Optional<String>` — Restrict results to segments update after the set time. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**beforeUpdatedAt:** `Optional<String>` — Restrict results to segments update before the set time. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**excludeType:** `Optional<ListSegmentsListsRequestExcludeType>` — Exclude results based on segment type. For example, use `exclude_type=static` to exclude tags from the response.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.createSegment(listId, request) -> List</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new segment in a specific list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().createSegment(
    "list_id",
    CreateSegmentListsRequest
        .builder()
        .name("name")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**name:** `String` — The name of the segment.
    
</dd>
</dl>

<dl>
<dd>

**options:** `Optional<CreateSegmentListsRequestOptions>` — The [conditions of the segment](https://mailchimp.com/help/save-and-manage-segments/). Static and fuzzy segments don't have conditions.
    
</dd>
</dl>

<dl>
<dd>

**staticSegment:** `Optional<List<String>>` — An array of emails to be used for a static segment. Any emails provided that are not present on the list will be ignored. Passing an empty array will create a static segment without any subscribers. This field cannot be provided with the options field.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.getSegment(listId, segmentId) -> List</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific segment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().getSegment(
    "list_id",
    "segment_id",
    GetSegmentListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**segmentId:** `String` — The unique id for the segment.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**includeCleaned:** `Optional<Boolean>` — Include cleaned members in response
    
</dd>
</dl>

<dl>
<dd>

**includeTransactional:** `Optional<Boolean>` — Include transactional members in response
    
</dd>
</dl>

<dl>
<dd>

**includeUnsubscribed:** `Optional<Boolean>` — Include unsubscribed members in response
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.batchAddOrRemoveMembers(listId, segmentId, request) -> BatchAddOrRemoveMembersListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Batch add/remove list members to static segment
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().batchAddOrRemoveMembers(
    "list_id",
    "segment_id",
    BatchAddOrRemoveMembersListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**segmentId:** `String` — The unique id for the segment.
    
</dd>
</dl>

<dl>
<dd>

**membersToAdd:** `Optional<List<String>>` — An array of emails to be used for a static segment. Any emails provided that are not present on the list will be ignored. A maximum of 500 members can be sent.
    
</dd>
</dl>

<dl>
<dd>

**membersToRemove:** `Optional<List<String>>` — An array of emails to be used for a static segment. Any emails provided that are not present on the list will be ignored. A maximum of 500 members can be sent.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.deleteSegment(listId, segmentId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a specific segment in a list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().deleteSegment(
    "list_id",
    "segment_id",
    DeleteSegmentListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**segmentId:** `String` — The unique id for the segment.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.updateSegment(listId, segmentId, request) -> List</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a specific segment in a list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().updateSegment(
    "list_id",
    "segment_id",
    UpdateSegmentListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**segmentId:** `String` — The unique id for the segment.
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — The name of the segment.
    
</dd>
</dl>

<dl>
<dd>

**options:** `Optional<UpdateSegmentListsRequestOptions>` — The [conditions of the segment](https://mailchimp.com/help/save-and-manage-segments/). Static and fuzzy segments don't have conditions.
    
</dd>
</dl>

<dl>
<dd>

**staticSegment:** `Optional<List<String>>` — An array of emails to be used for a static segment. Any emails provided that are not present on the list will be ignored. Passing an empty array for an existing static segment will reset that segment and remove all members. This field cannot be provided with the `options` field.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listSegmentMembers(listId, segmentId) -> SyncPagingIterable&amp;lt;ListsSegmentsMembers&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about members in a saved segment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listSegmentMembers(
    "list_id",
    "segment_id",
    ListSegmentMembersListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**segmentId:** `String` — The unique id for the segment.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**includeCleaned:** `Optional<Boolean>` — Include cleaned members in response
    
</dd>
</dl>

<dl>
<dd>

**includeTransactional:** `Optional<Boolean>` — Include transactional members in response
    
</dd>
</dl>

<dl>
<dd>

**includeUnsubscribed:** `Optional<Boolean>` — Include unsubscribed members in response
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.createSegmentMember(listId, segmentId, request) -> ListsSegmentsMembers</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a member to a static segment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().createSegmentMember(
    "list_id",
    "segment_id",
    CreateSegmentMemberListsRequest
        .builder()
        .emailAddress("email_address")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**segmentId:** `String` — The unique id for the segment.
    
</dd>
</dl>

<dl>
<dd>

**emailAddress:** `String` — Email address for a subscriber.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.deleteSegmentMember(listId, segmentId, subscriberHash)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a member from the specified static segment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().deleteSegmentMember(
    "list_id",
    "segment_id",
    "subscriber_hash",
    DeleteSegmentMemberListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**segmentId:** `String` — The unique id for the segment.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listSignupForms(listId) -> ListSignupFormsListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get signup forms for a specific list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listSignupForms(
    "list_id",
    ListSignupFormsListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.createSignupForm(listId, request) -> SignupForm</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Customize a list's default signup form.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().createSignupForm(
    "list_id",
    CreateSignupFormListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**contents:** `Optional<List<CreateSignupFormListsRequestContentsItem>>` — The signup form body content.
    
</dd>
</dl>

<dl>
<dd>

**header:** `Optional<CreateSignupFormListsRequestHeader>` — Options for customizing your signup form header.
    
</dd>
</dl>

<dl>
<dd>

**styles:** `Optional<List<CreateSignupFormListsRequestStylesItem>>` — An array of objects, each representing an element style for the signup form.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listSurveys(listId) -> Object</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about all available surveys for a specific list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listSurveys(
    "list_id",
    ListSurveysListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.createSurvey(listId, request) -> Object</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a draft survey for an audience.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().createSurvey(
    "list_id",
    CreateSurveyListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — The title of the survey.
    
</dd>
</dl>

<dl>
<dd>

**sections:** `Optional<List<SurveySectionRequest>>` — Initial survey sections.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.getSurvey(listId, surveyId) -> Object</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get details about a specific survey.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().getSurvey(
    "list_id",
    "survey_id",
    GetSurveyListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**surveyId:** `String` — The ID of the survey.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.deleteSurvey(listId, surveyId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a survey.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().deleteSurvey(
    "list_id",
    "survey_id",
    DeleteSurveyListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**surveyId:** `String` — The ID of the survey.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.updateSurvey(listId, surveyId, request) -> Object</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a survey. When sections is provided, send the complete section list in display order. Any existing section not included is deleted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().updateSurvey(
    "list_id",
    "survey_id",
    UpdateSurveyListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**surveyId:** `String` — The ID of the survey.
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — The title of the survey.
    
</dd>
</dl>

<dl>
<dd>

**isPipedToInbox:** `Optional<Boolean>` — Whether responses are sent to Mailchimp Inbox.
    
</dd>
</dl>

<dl>
<dd>

**sections:** `Optional<List<SurveySectionRequest>>` — The complete survey section list in display order. On update, sections omitted from this array are deleted. Include section id to update an existing section; omit section id to add a new section.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.createListSurveyActionReplicate(listIdPathParam, surveyId, request) -> Object</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Replicate a survey.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().createListSurveyActionReplicate(
    "list_id",
    "survey_id",
    CreateListSurveyActionReplicateListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listIdPathParam:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**surveyId:** `String` — The ID of the survey.
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — The title for the replicated survey.
    
</dd>
</dl>

<dl>
<dd>

**listId:** `Optional<String>` — The unique ID of the audience for the replicated survey. Defaults to the source survey audience.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listTagSearch(listId) -> ListTagSearchListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Search for tags on a list by name. If no name is provided, will return all tags on the list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listTagSearch(
    "list_id",
    ListTagSearchListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — The search query used to filter tags.  The search query will be compared to each tag as a prefix, so all tags that have a name starting with this field will be returned.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.listWebhooks(listId) -> ListWebhooksListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about all webhooks for a specific list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().listWebhooks(
    "list_id",
    ListWebhooksListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.createWebhook(listId, request) -> CreateWebhookListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new webhook for a specific list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().createWebhook(
    "list_id",
    CreateWebhookListsRequest
        .builder()
        .body(
            AddWebhook
                .builder()
                .build()
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**request:** `AddWebhook` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.getWebhook(listId, webhookId) -> ListWebhooks</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific webhook.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().getWebhook(
    "list_id",
    "webhook_id",
    GetWebhookListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**webhookId:** `String` — The webhook's id.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.deleteWebhook(listId, webhookId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a specific webhook in a list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().deleteWebhook(
    "list_id",
    "webhook_id",
    DeleteWebhookListsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**webhookId:** `String` — The webhook's id.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lists.updateWebhook(listId, webhookId, request) -> ListWebhooks</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update the settings for an existing webhook.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.lists().updateWebhook(
    "list_id",
    "webhook_id",
    UpdateWebhookListsRequest
        .builder()
        .body(
            AddWebhook
                .builder()
                .build()
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**webhookId:** `String` — The webhook's id.
    
</dd>
</dl>

<dl>
<dd>

**request:** `AddWebhook` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## surveys
<details><summary><code>client.surveys.createListSurveyActionCreateEmail(listId, surveyId) -> Campaign</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Utilize the List ID and Survey ID to generate a Campaign that links to your survey.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.surveys().createListSurveyActionCreateEmail(
    "list_id",
    "survey_id",
    CreateListSurveyActionCreateEmailSurveysRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**surveyId:** `String` — The ID of the survey.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.surveys.createListSurveyActionPublish(listId, surveyId) -> Object</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Publish a survey that is in draft, unpublished, or has been previously published and edited.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.surveys().createListSurveyActionPublish(
    "list_id",
    "survey_id",
    CreateListSurveyActionPublishSurveysRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**surveyId:** `String` — The ID of the survey.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.surveys.createListSurveyActionUnpublish(listId, surveyId) -> Object</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Unpublish a survey that has been published.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.surveys().createListSurveyActionUnpublish(
    "list_id",
    "survey_id",
    CreateListSurveyActionUnpublishSurveysRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**listId:** `String` — The unique ID for the list.
    
</dd>
</dl>

<dl>
<dd>

**surveyId:** `String` — The ID of the survey.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## ping
<details><summary><code>client.ping.list() -> ListPingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

A health check for the API that won't return any account-specific information.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ping().list();
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## reporting
<details><summary><code>client.reporting.list() -> List&amp;lt;ListReportingResponseItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about the reporting endpoint's resources.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reporting().list();
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reporting.listFacebookAds() -> SyncPagingIterable&amp;lt;ReportingFacebookAd&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get reports of Facebook ads.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reporting().listFacebookAds(
    ListFacebookAdsReportingRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListFacebookAdsReportingRequestSortField>` — Returns files sorted by the specified field.
    
</dd>
</dl>

<dl>
<dd>

**sortDir:** `Optional<ListFacebookAdsReportingRequestSortDir>` — Determines the order direction for sorted results.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reporting.getFacebookAd(outreachId) -> ReportingFacebookAd</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get report of a Facebook ad.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reporting().getFacebookAd(
    "outreach_id",
    GetFacebookAdReportingRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**outreachId:** `String` — The outreach id.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reporting.listFacebookAdEcommerceProductActivity(outreachId) -> SyncPagingIterable&amp;lt;ListFacebookAdEcommerceProductActivityReportingResponseProductsItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get breakdown of product activity for an outreach.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reporting().listFacebookAdEcommerceProductActivity(
    "outreach_id",
    ListFacebookAdEcommerceProductActivityReportingRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**outreachId:** `String` — The outreach id.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListFacebookAdEcommerceProductActivityReportingRequestSortField>` — Returns files sorted by the specified field.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reporting.listLandingPages() -> SyncPagingIterable&amp;lt;LandingPageReport&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get reports of landing pages.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reporting().listLandingPages(
    ListLandingPagesReportingRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reporting.getLandingPage(outreachId) -> LandingPageReport</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get report of a landing page.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reporting().getLandingPage(
    "outreach_id",
    GetLandingPageReportingRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**outreachId:** `String` — The outreach id.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reporting.listSurveys() -> SyncPagingIterable&amp;lt;ListSurveysReportingResponseSurveysItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get reports for surveys.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reporting().listSurveys(
    ListSurveysReportingRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reporting.getSurvey(surveyId) -> GetSurveyReportingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get report for a survey.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reporting().getSurvey(
    "survey_id",
    GetSurveyReportingRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**surveyId:** `String` — The ID of the survey.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reporting.listSurveyQuestions(surveyId) -> ListSurveyQuestionsReportingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get reports for survey questions.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reporting().listSurveyQuestions(
    "survey_id",
    ListSurveyQuestionsReportingRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**surveyId:** `String` — The ID of the survey.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reporting.getSurveyQuestion(surveyId, questionId) -> SurveyQuestionReport</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get report for a survey question.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reporting().getSurveyQuestion(
    "survey_id",
    "question_id",
    GetSurveyQuestionReportingRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**surveyId:** `String` — The ID of the survey.
    
</dd>
</dl>

<dl>
<dd>

**questionId:** `String` — The ID of the survey question.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reporting.listSurveyQuestionAnswers(surveyId, questionId) -> ListSurveyQuestionAnswersReportingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get answers for a survey question.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reporting().listSurveyQuestionAnswers(
    "survey_id",
    "question_id",
    ListSurveyQuestionAnswersReportingRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**surveyId:** `String` — The ID of the survey.
    
</dd>
</dl>

<dl>
<dd>

**questionId:** `String` — The ID of the survey question.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**respondentFamiliarityIs:** `Optional<ListSurveyQuestionAnswersReportingRequestRespondentFamiliarityIs>` — Filter survey responses by familiarity of the respondents.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reporting.listSurveyResponses(surveyId) -> ListSurveyResponsesReportingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get responses to a survey.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reporting().listSurveyResponses(
    "survey_id",
    ListSurveyResponsesReportingRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**surveyId:** `String` — The ID of the survey.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**answeredQuestion:** `Optional<Integer>` — The ID of the question that was answered.
    
</dd>
</dl>

<dl>
<dd>

**choseAnswer:** `Optional<String>` — The ID of the option chosen to filter responses on.
    
</dd>
</dl>

<dl>
<dd>

**respondentFamiliarityIs:** `Optional<ListSurveyResponsesReportingRequestRespondentFamiliarityIs>` — Filter survey responses by familiarity of the respondents.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reporting.getSurveyRespons(surveyId, responseId) -> GetSurveyResponsReportingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single survey response.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reporting().getSurveyRespons(
    "survey_id",
    "response_id",
    GetSurveyResponsReportingRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**surveyId:** `String` — The ID of the survey.
    
</dd>
</dl>

<dl>
<dd>

**responseId:** `String` — The ID of the survey response.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## reports
<details><summary><code>client.reports.list() -> SyncPagingIterable&amp;lt;CampaignReport&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get campaign reports.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().list(
    ListReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<ListReportsRequestType>` — The campaign type.
    
</dd>
</dl>

<dl>
<dd>

**beforeSendTime:** `Optional<OffsetDateTime>` — Restrict the response to campaigns sent before the set time. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sinceSendTime:** `Optional<OffsetDateTime>` — Restrict the response to campaigns sent after the set time. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.get(campaignId) -> CampaignReport</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get report details for a specific sent campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().get(
    "campaign_id",
    GetReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.listAbuseReports(campaignId) -> ListAbuseReportsReportsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of abuse complaints for a specific campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().listAbuseReports(
    "campaign_id",
    ListAbuseReportsReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.getAbuseReport(campaignId, reportId) -> AbuseComplaint</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific abuse report for a campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().getAbuseReport(
    "campaign_id",
    "report_id",
    GetAbuseReportReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**reportId:** `String` — The id for the abuse report.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.listAdvice(campaignId) -> ListAdviceReportsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get feedback based on a campaign's statistics. Advice feedback is based on campaign stats like opens, clicks, unsubscribes, bounces, and more.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().listAdvice(
    "campaign_id",
    ListAdviceReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.listClickDetails(campaignId) -> SyncPagingIterable&amp;lt;ClickDetailReport&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about clicks on specific links in your Mailchimp campaigns.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().listClickDetails(
    "campaign_id",
    ListClickDetailsReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListClickDetailsReportsRequestSortField>` — Returns click reports sorted by the specified field.
    
</dd>
</dl>

<dl>
<dd>

**sortDir:** `Optional<ListClickDetailsReportsRequestSortDir>` — Determines the order direction for sorted results.
    
</dd>
</dl>

<dl>
<dd>

**filterBots:** `Optional<Boolean>` — When true, exclude automated bot clicks so the returned click counts reflect human clicks only, matching the in-app Recipient Activity view. Filtering changes a link's counts, but never removes a link from the response. Defaults to false (all clicks).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.getClickDetail(campaignId, linkId) -> ClickDetailReport</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get click details for a specific link in a campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().getClickDetail(
    "campaign_id",
    "link_id",
    GetClickDetailReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**linkId:** `String` — The id for the link.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**filterBots:** `Optional<Boolean>` — When true, exclude automated bot clicks so the returned click counts reflect human clicks only, matching the in-app Recipient Activity view. Filtering changes a link's counts, but never removes a link from the response. Defaults to false (all clicks).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.listClickDetailMembers(campaignId, linkId) -> SyncPagingIterable&amp;lt;ClickDetailMember&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about list members who clicked on a specific link in a campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().listClickDetailMembers(
    "campaign_id",
    "link_id",
    ListClickDetailMembersReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**linkId:** `String` — The id for the link.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.getClickDetailMember(campaignId, linkId, subscriberHash) -> ClickDetailMember</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific subscriber who clicked a link in a specific campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().getClickDetailMember(
    "campaign_id",
    "link_id",
    "subscriber_hash",
    GetClickDetailMemberReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**linkId:** `String` — The id for the link.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.listDomainPerformance(campaignId) -> ListDomainPerformanceReportsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get statistics for the top-performing email domains in a campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().listDomainPerformance(
    "campaign_id",
    ListDomainPerformanceReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.listEcommerceProductActivity(campaignId) -> SyncPagingIterable&amp;lt;ListEcommerceProductActivityReportsResponseProductsItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get breakdown of product activity for a campaign
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().listEcommerceProductActivity(
    "campaign_id",
    ListEcommerceProductActivityReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListEcommerceProductActivityReportsRequestSortField>` — Returns files sorted by the specified field.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.listEepurl(campaignId) -> ListEepurlReportsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a summary of social activity for the campaign, tracked by EepURL.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().listEepurl(
    "campaign_id",
    ListEepurlReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.listEmailActivity(campaignId) -> SyncPagingIterable&amp;lt;EmailActivity&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of member's subscriber activity in a specific campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().listEmailActivity(
    "campaign_id",
    ListEmailActivityReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**since:** `Optional<String>` — Restrict results to email activity events that occur after a specific time. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**filterBots:** `Optional<Boolean>` — When true, exclude automated bot and Apple Mail Privacy Protection (MPP) proxy activity so the returned activity reflects human-only opens and clicks, matching the in-app Recipient Activity view. Filtering removes events from a member's activity, but never removes the member from the response. Defaults to false (all activity).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.getEmailActivity(campaignId, subscriberHash) -> EmailActivity</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a specific list member's activity in a campaign including opens, clicks, and bounces.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().getEmailActivity(
    "campaign_id",
    "subscriber_hash",
    GetEmailActivityReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**since:** `Optional<String>` — Restrict results to email activity events that occur after a specific time. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**filterBots:** `Optional<Boolean>` — When true, exclude automated bot and Apple Mail Privacy Protection (MPP) proxy activity so the returned activity reflects human-only opens and clicks, matching the in-app Recipient Activity view. Filtering removes events from a member's activity, but never removes the member from the response. Defaults to false (all activity).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.listLocations(campaignId) -> SyncPagingIterable&amp;lt;ListLocationsReportsResponseLocationsItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get top open locations for a specific campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().listLocations(
    "campaign_id",
    ListLocationsReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.listOpenDetails(campaignId) -> SyncPagingIterable&amp;lt;OpenActivity&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get detailed information about any campaign emails that were opened by a list member.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().listOpenDetails(
    "campaign_id",
    ListOpenDetailsReportsRequest
        .builder()
        .since("2016-04-12 12:00:00")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**since:** `Optional<String>` — Restrict results to campaign open events that occur after a specific time. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListOpenDetailsReportsRequestSortField>` — Returns open reports sorted by the specified field.
    
</dd>
</dl>

<dl>
<dd>

**sortDir:** `Optional<ListOpenDetailsReportsRequestSortDir>` — Determines the order direction for sorted results.
    
</dd>
</dl>

<dl>
<dd>

**filterBots:** `Optional<Boolean>` — When true, exclude automated (proxy/bot) opens so the returned open counts reflect human opens only, matching the in-app Recipient Activity view. A member whose opens are all automated is excluded from the human-only view. Defaults to false (all opens).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.getOpenDetail(campaignId, subscriberHash) -> OpenActivity</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific subscriber who opened a campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().getOpenDetail(
    "campaign_id",
    "subscriber_hash",
    GetOpenDetailReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**filterBots:** `Optional<Boolean>` — When true, exclude automated (proxy/bot) opens so the returned open counts reflect human opens only, matching the in-app Recipient Activity view. A member whose opens are all automated is excluded from the human-only view. Defaults to false (all opens).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.listSentTo(campaignId) -> SyncPagingIterable&amp;lt;SentTo&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about campaign recipients.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().listSentTo(
    "campaign_id",
    ListSentToReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.getSentTo(campaignId, subscriberHash) -> SentTo</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific campaign recipient.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().getSentTo(
    "campaign_id",
    "subscriber_hash",
    GetSentToReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.listSubReports(campaignId) -> ListSubReportsReportsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of reports with child campaigns for a specific parent campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().listSubReports(
    "campaign_id",
    ListSubReportsReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.listUnsubscribed(campaignId) -> SyncPagingIterable&amp;lt;Unsubscribes&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about members who have unsubscribed from a specific campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().listUnsubscribed(
    "campaign_id",
    ListUnsubscribedReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.getUnsubscribed(campaignId, subscriberHash) -> Unsubscribes</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific list member who unsubscribed from a campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().getUnsubscribed(
    "campaign_id",
    "subscriber_hash",
    GetUnsubscribedReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**campaignId:** `String` — The unique id for the campaign.
    
</dd>
</dl>

<dl>
<dd>

**subscriberHash:** `String` — The MD5 hash of the lowercase version of the list member's email address.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## SearchCampaigns
<details><summary><code>client.searchCampaigns.list() -> ListSearchCampaignsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Search all campaigns for the specified query terms.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.searchCampaigns().list(
    ListSearchCampaignsRequest
        .builder()
        .query("query")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**query:** `String` — The search query used to filter results.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## SmsCampaigns
<details><summary><code>client.smsCampaigns.list() -> SyncPagingIterable&amp;lt;SmsCampaign&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get all SMS campaigns in an account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.smsCampaigns().list(
    ListSmsCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.create(request) -> SmsCampaign</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new SMS campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.smsCampaigns().create(
    CreateSmsCampaignsRequest
        .builder()
        .name("name")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `String` — The name of the campaign.
    
</dd>
</dl>

<dl>
<dd>

**listId:** `Optional<Integer>` — The numeric ID of the list to send the campaign to.
    
</dd>
</dl>

<dl>
<dd>

**folderId:** `Optional<String>` — The ID of the folder to place this campaign in.
    
</dd>
</dl>

<dl>
<dd>

**segments:** `Optional<List<Integer>>` — The segment IDs to target for this campaign.
    
</dd>
</dl>

<dl>
<dd>

**excludedSegments:** `Optional<List<Integer>>` — The segment IDs to exclude from this campaign.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.get(smsCampaignId) -> SmsCampaign</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the details for a single SMS campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.smsCampaigns().get(
    "sms_campaign_id",
    GetSmsCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**smsCampaignId:** `String` — The unique id for the SMS campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.delete(smsCampaignId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a campaign from your Mailchimp account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.smsCampaigns().delete(
    "sms_campaign_id",
    DeleteSmsCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**smsCampaignId:** `String` — The unique id for the SMS campaign.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.update(smsCampaignId, request) -> SmsCampaign</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an SMS campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.smsCampaigns().update(
    "sms_campaign_id",
    UpdateSmsCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**smsCampaignId:** `String` — The unique id for the SMS campaign.
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — The name of the campaign.
    
</dd>
</dl>

<dl>
<dd>

**folderId:** `Optional<String>` — The ID of the folder to place this campaign in.
    
</dd>
</dl>

<dl>
<dd>

**segments:** `Optional<List<Integer>>` — The segment IDs to target for this campaign.
    
</dd>
</dl>

<dl>
<dd>

**excludedSegments:** `Optional<List<Integer>>` — The segment IDs to exclude from this campaign.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.createActionCancelSend(smsCampaignId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cancel a scheduled or sending SMS campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.smsCampaigns().createActionCancelSend(
    "sms_campaign_id",
    CreateActionCancelSendSmsCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**smsCampaignId:** `String` — The unique id for the SMS campaign.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.createActionSchedule(smsCampaignId, request)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Schedule an SMS campaign for delivery.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.smsCampaigns().createActionSchedule(
    "sms_campaign_id",
    CreateActionScheduleSmsCampaignsRequest
        .builder()
        .scheduleTime(OffsetDateTime.parse("2024-01-15T09:30:00Z"))
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**smsCampaignId:** `String` — The unique id for the SMS campaign.
    
</dd>
</dl>

<dl>
<dd>

**scheduleTime:** `OffsetDateTime` — The UTC date and time to schedule the campaign.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.createActionSend(smsCampaignId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send an SMS campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.smsCampaigns().createActionSend(
    "sms_campaign_id",
    CreateActionSendSmsCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**smsCampaignId:** `String` — The unique id for the SMS campaign.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.getContent(smsCampaignId) -> SmsCampaignContent</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the content for an SMS campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.smsCampaigns().getContent(
    "sms_campaign_id",
    GetContentSmsCampaignsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**smsCampaignId:** `String` — The unique id for the SMS campaign.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.upsertContent(smsCampaignId, request) -> SmsCampaignContent</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Set the content for an SMS campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.smsCampaigns().upsertContent(
    "sms_campaign_id",
    UpsertContentSmsCampaignsRequest
        .builder()
        .messageBody("message_body")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**smsCampaignId:** `String` — The unique id for the SMS campaign.
    
</dd>
</dl>

<dl>
<dd>

**messageBody:** `String` — The SMS message body.
    
</dd>
</dl>

<dl>
<dd>

**media:** `Optional<List<UpsertContentSmsCampaignsRequestMediaItem>>` — Attached images or files. Limited to one item. Omitting this field or sending an empty array removes any existing media; to keep the current media while updating other fields, re-send the media array.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## SearchMembers
<details><summary><code>client.searchMembers.list() -> ListSearchMembersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Search for list members. This search can be restricted to a specific list, or can be used to search across all lists in an account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.searchMembers().list(
    ListSearchMembersRequest
        .builder()
        .query("query")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**query:** `String` — The search query used to filter results. Query should be a valid email, or a string representing a contact's first or last name.
    
</dd>
</dl>

<dl>
<dd>

**listId:** `Optional<String>` — The unique id for the list.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## TemplateFolders
<details><summary><code>client.templateFolders.list() -> SyncPagingIterable&amp;lt;ListTemplateFoldersResponseFoldersItem&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get all folders used to organize templates.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.templateFolders().list(
    ListTemplateFoldersRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.templateFolders.create(request) -> CreateTemplateFoldersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new template folder.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.templateFolders().create(
    CreateTemplateFoldersRequest
        .builder()
        .name("name")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `String` — The name of the folder.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.templateFolders.get(folderId) -> GetTemplateFoldersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific folder used to organize templates.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.templateFolders().get(
    "folder_id",
    GetTemplateFoldersRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**folderId:** `String` — The unique id for the template folder.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.templateFolders.delete(folderId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a specific template folder, and mark all the templates in the folder as 'unfiled'.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.templateFolders().delete(
    "folder_id",
    DeleteTemplateFoldersRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**folderId:** `String` — The unique id for the template folder.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.templateFolders.update(folderId, request) -> UpdateTemplateFoldersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a specific folder used to organize templates.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.templateFolders().update(
    "folder_id",
    UpdateTemplateFoldersRequest
        .builder()
        .name("name")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**folderId:** `String` — The unique id for the template folder.
    
</dd>
</dl>

<dl>
<dd>

**name:** `String` — The name of the folder.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## templates
<details><summary><code>client.templates.list() -> SyncPagingIterable&amp;lt;TemplateInstance&amp;gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of an account's available templates.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.templates().list(
    ListTemplatesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**count:** `Optional<Integer>` — The number of records to return. Default value is 10. Maximum value is 1000
    
</dd>
</dl>

<dl>
<dd>

**offset:** `Optional<Integer>` — Used for [pagination](https://mailchimp.com/developer/marketing/docs/methods-parameters/#pagination), this is the number of records from a collection to skip. Default value is 0.
    
</dd>
</dl>

<dl>
<dd>

**createdBy:** `Optional<String>` — The Mailchimp account user who created the template.
    
</dd>
</dl>

<dl>
<dd>

**sinceDateCreated:** `Optional<String>` — Restrict the response to templates created after the set date. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**beforeDateCreated:** `Optional<String>` — Restrict the response to templates created before the set date. Uses ISO 8601 time format: 2015-10-21T15:41:36+00:00.
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<String>` — Limit results based on template type.
    
</dd>
</dl>

<dl>
<dd>

**category:** `Optional<String>` — Limit results based on category.
    
</dd>
</dl>

<dl>
<dd>

**folderId:** `Optional<String>` — The unique folder id.
    
</dd>
</dl>

<dl>
<dd>

**sortField:** `Optional<ListTemplatesRequestSortField>` — Returns user templates sorted by the specified field.
    
</dd>
</dl>

<dl>
<dd>

**contentType:** `Optional<ListTemplatesRequestContentType>` — Limit results based on how the template's content is put together. Only templates of type `user` can be filtered by `content_type`. If you want to retrieve saved templates created with the legacy email editor, then filter `content_type` to `template`. If you'd rather pull your saved templates for the new editor, filter to `multichannel`. For code your own templates, filter to `html`.
    
</dd>
</dl>

<dl>
<dd>

**sortDir:** `Optional<ListTemplatesRequestSortDir>` — Determines the order direction for sorted results.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.templates.create(request) -> TemplateInstance</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new template for the account. Only Classic templates are supported.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.templates().create(
    CreateTemplatesRequest
        .builder()
        .html("html")
        .name("Freddie's Jokes")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**folderId:** `Optional<String>` — The id of the folder the template is currently in.
    
</dd>
</dl>

<dl>
<dd>

**html:** `String` — The raw HTML for the template. We  support the Mailchimp [Template Language](https://mailchimp.com/help/getting-started-with-mailchimps-template-language/) in any HTML code passed via the API.
    
</dd>
</dl>

<dl>
<dd>

**name:** `String` — The name of the template.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.templates.get(templateId) -> TemplateInstance</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about a specific template.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.templates().get(
    "template_id",
    GetTemplatesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**templateId:** `String` — The unique id for the template.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.templates.delete(templateId)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a specific template.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.templates().delete(
    "template_id",
    DeleteTemplatesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**templateId:** `String` — The unique id for the template.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.templates.update(templateId, request) -> TemplateInstance</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update the name, HTML, or `folder_id` of an existing template.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.templates().update(
    "template_id",
    UpdateTemplatesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**templateId:** `String` — The unique id for the template.
    
</dd>
</dl>

<dl>
<dd>

**folderId:** `Optional<String>` — The id of the folder the template is currently in.
    
</dd>
</dl>

<dl>
<dd>

**html:** `Optional<String>` — The raw HTML for the template. We  support the Mailchimp [Template Language](https://mailchimp.com/help/getting-started-with-mailchimps-template-language/) in any HTML code passed via the API.
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — The name of the template.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.templates.listDefaultContent(templateId) -> ListDefaultContentTemplatesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the sections that you can edit in a template, including each section's default content.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.templates().listDefaultContent(
    "template_id",
    ListDefaultContentTemplatesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**templateId:** `String` — The unique id for the template.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `Optional<String>` — A comma-separated list of fields to return. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>

<dl>
<dd>

**excludeFields:** `Optional<String>` — A comma-separated list of fields to exclude. Reference parameters of sub-objects with dot notation.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## VerifiedDomains
<details><summary><code>client.verifiedDomains.list() -> ListVerifiedDomainsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get all of the sending domains on the account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.verifiedDomains().list();
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.verifiedDomains.create(request) -> CreateVerifiedDomainsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a domain to the account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.verifiedDomains().create(
    CreateVerifiedDomainsRequest
        .builder()
        .verificationEmail("verification_email")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**verificationEmail:** `String` — The e-mail address at the domain you want to verify. This will receive a two-factor challenge to be used in the verify action.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.verifiedDomains.get(domainName) -> GetVerifiedDomainsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the details for a single domain on the account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.verifiedDomains().get(
    "domain_name",
    GetVerifiedDomainsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `String` — The domain name.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.verifiedDomains.delete(domainName)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a verified domain from the account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.verifiedDomains().delete(
    "domain_name",
    DeleteVerifiedDomainsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `String` — The domain name.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.verifiedDomains.createActionVerify(domainName, request) -> CreateActionVerifyVerifiedDomainsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Verify a domain for sending.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.verifiedDomains().createActionVerify(
    "domain_name",
    CreateActionVerifyVerifiedDomainsRequest
        .builder()
        .code("code")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `String` — The domain name.
    
</dd>
</dl>

<dl>
<dd>

**code:** `String` — The code that was sent to the email address provided when adding a new domain to verify.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

