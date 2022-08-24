---
title: API Versioning
date: 2020-02-15
order: -7
---

APEX API Publisher Portal provides the flexibility to support API versioning. This section provides the methods and steps for the configurations.

## Version update to a published API

1. Add the **new API** to API Manager and publish it.

2. Select the old API, click **Manage** selected, and choose **Upgrade** access to newer API.

!!! Warning
Old API will be depreciated. This method is only recommended for api that is backwards compatible.
!!!

## Host same API with different version

1. Create [new api](/publisher/create-api/) (backend api).

2. Update path to specify the version [!badge e.g. v1/api/getUsers] for the older api version.

3. Specify the version in the path [!badge e.g. v2/api/getUsers] when [publish api](/publisher/publish-api/).
