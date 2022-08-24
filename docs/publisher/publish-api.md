# Published API (Frontend API)

## Create New API

### Import from Backend API

1. Click the **API > Frontend API** in API Manager.
2. Click **New API > New API from backend API**.

![import-backend-api](./image/publish-api/import-backend-api.jpg)s

3. Select an existing back-end API in the dialog, and click **Create**.

![import-api-dialog](./image/publish-api/import-api-dialog.jpg)

### Import API via .dat file

1. Click **API > Frontend API view** in API Manager.
2. Click **New API > Import API collection**.
3. In the **Import** from dialog, complete the following:
   - **File**: Click to browse to the previously exported API (.dat file).
   - **Password**: Enter the password if required.
   - **Organization**: Select the organization from the list.
4. Click **Import**.
5. **Press F5** to **reload** the API Manager web console.

![import-api-from-file](./image/publish-api/import-api-from-file.jpg)

## Configure Inbound Request Settings

Configuration for inbound request settings between the client and the API Gateway:

1. Select the **Inbound** tab.
2. Edit **Resource** path for the API.
   !!!
   If there are more than 1 version of the api, state the version number in the path e.g. v1/api/getUsers. [API Versioning](/publisher/api-versioning)
   !!!
3. Select API Key from the **Inbound Security** list.
   - **API key field name**: Enter name for API key field in the inbound request.
   - **API key location**: Select Request Headers or Query string/form body.
   - **Remove credentials on success**: Default to enable it. Inbound authorization header will be removed to use different authentication method for the outbound to the backend services.
4. Click the **Advanced** button on the right to configure settings such as monitoring, sharing resources across domains, and per-API method overrides.

## Configure Outbound Request Settings

Configuration of the outbound request settings between the API Gateway and the backend services:

1. Select the **Outbound** tab.
2. Select an **authentication profile** for the backend services.
   - [No Authentication](#no-authentication)
   - [HTTP Basic authentication](#http-basic-authentication)
   - [OAuth authentication](#oauth-authentication)
   - [API Key authentication](#api-key-authentication)
   - [SSL authentication](#ssl-authentication)
3. Click the **Advanced** button on the right to configure settings such as request or response processing, routing, and per-API method overrides.

!!!
Advance option can be use in situation where additional headers (e.g. client ID and secret) are required.

1. Under Outbound tab, **Expand pre-method override > Click + sign**.
2. **Select API**.
3. Click **Edit API Proxy > Input necessary headers and value(s)**.

!!!

### No Authentication

No authentication is performed between the API Gateway and the back-end API.

### HTTP Basic Authentication

**Name**: Enter a required name for the profile. Defaults to HTTP Basic.

**Username**: Enter the required username (API key).

**Password**: Enter the optional password (API secret).

### OAuth Authentication

**Provider Profile**: Select the OAuth service provider profile.

**Token Key (Owner ID)**: Enter Token Key. This must be set to the authentication value you require for the OAuth token. Defaults to ${authentication.subject.id}.

### API Key Authentication

**Name**: Enter a required name for the profile.

**API key field name**: Enter name for API key field in the outbound request.

**API key**: Enter the API key.

**Pass credentials as HTTP**: Select Header, Query string or Form of the API key in the outbound request.

### SSL Authentication

**Name**: Enter a required name for the profile.

**PFX/P12 Source**: Select whether to specify the certificate using a .pfx or .p12 file, or using a URL.

**PFX/P12 File or PFX/P12 URL**: Browse to the PFX/P12 file, or enter the PFX/P12 URL.

**PFX/P12 Password**: Enter the password for the certificate.

**Trust all certificates in chain**: Select whether to trust all the CA certificates in the certificate chain. If this is not selected, only the top-level CA is trusted.

!!!Warning
To enable SSL authentication, the API Gateway must supply a certificate signed by certificate authority used by the API.
!!!

## Publish API(s)

1. Click **API > Frontend API view > Select API** in API Manager.
2. Click **Manage Selected** and select **Publish**.
3. Enter **Virtual Host** and click **Publish**.

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
