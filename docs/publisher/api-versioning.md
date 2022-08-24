# API Versioning

## Version update to a published API

1. Add the **new API** to API Manager and publish it.

2. Select the old API, click **Manage** selected, and choose **Upgrade** access to newer API.

Note:

- Old API will be depreciated. This method is only recommended for api that is backwards compatible.

TODO: Add image.

## Host same API with different version

1. Create [new api](docs/publisher/create-api.md) (backend api).

2. Update path to specify the version (e.g. /eservice/ndi/v1]) for the older api version.

3. Specify the version in the path (e.g. /eservice/ndi/v2]) when [publish api](docs/publisher/publish-api.md).

TODO: Add image.
