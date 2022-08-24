# Virtualize Frontend API

### Import from Backend API

1. Click the **API > Frontend API view** in API Manager.
2. Click **New API > New API from backend API**.
3. Select an existing back-end API in the dialog, and click **Create**.

Note:

- Download of swagger is not supported in API Catalog if the virtualized API is not a Swagger 2.0-compatible REST API

### Import API via .dat file

1. Click **API > Frontend API view** in API Manager.
2. Click **New API > Import API collection**.
3. In the **Import** from dialog, complete the following:
   - **File**: Click to browse to the previously exported API (.dat file).
   - **Password**: Enter the password if required.
   - **Organization**: Select the organization from the list.
4. Click **Import**.
5. **Press F5** to **reload** the API Manager web console.

## Authentication Settings

[Configure API secuirty policy](/configue-api-security-policies/) for the inbound and outbound between API Gateway and backend services.

## Publish API(s)

1. Click **API > Frontend API view** in API Manager.
2. **Select API(s)**.
3. Click **Manage Selected** and select **Publish**.
4. Enter **Virtual Host** and click **Publish**.

## Manage Frontend API Lifecycle

1. Click **API Registration > Frontend API view** in API Manager.
2. **Select API**
3. Click **Manage Selected** and select any of the following
   - **Unpublish API(s)**.
   - **Delete and Update** API(s). (TODO: to check. api manager do not see the update option.)
   - **Grant access** to organisation(s). Refer to [Manage access to APIs](/publisher/manage-access-to-apis/).
   - **Export API(s)** to .dat extension.

// add update api
// the updated version should show in the app
// only active will be presented
// retired only developer will see. consumer unable to see retired apis.
