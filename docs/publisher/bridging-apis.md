# Bridging API

- https://manage.api.gov.sg/home - Internet API Manager
- https://manage.int.api.gov.sg/home - Intranet API Manager

## Backend hosted in Intranet and exposing in Internet

1. Internet API Manager (Ext): [Create](docs/publisher/create-api.md) and [Publish](docs/publisher/publish-api.md) API.

```
Frontend URL (Ext): https://public.api.gov.sg/eservice/ndi/v1/authinfo
```

2. Intranet API Manager (Int): [Create](docs/publisher/create-api.md) and [Publish](docs/publisher/publish-api.md) API.

3. Int: Select **Frontend** > **Select API** > **Outbound**.

4. Int: Enter **Frontend URL** (Ext) as **Backend service URL**.

```
Backend service URL: https://public.api.gov.sg/eservice/ndi/v1/authinfo
```

TODO: Add image

## Backend hosted in Internet and exposing in Intranet

1. Intranet API Manager (Int): [Create](docs/publisher/create-api.md) and [Publish](docs/publisher/publish-api.md) API.

```
Frontend URL (Int): https://public.int.api.gov.sg/eservice/ndi/v1/authinfo
```

2. Internet API Manager (Ext): [Create](docs/publisher/create-api.md) and [Publish](docs/publisher/publish-api.md) API.

3. Ext: Select **Frontend** > **Select API** > **Outbound**.

4. Ext: Enter **Frontend URL** (Int) as **Backend service URL**.

```
Backend service URL: https://public.int.api.gov.sg/eservice/ndi/v1/authinfo
```

TODO: Add image
