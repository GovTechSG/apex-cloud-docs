# Oauth 2.1

## Onboard Application with Oauth 2.1

1. **Apps** tab > Select **Application**
2. View **Oauth 2.1** > Click on the link **Click here to onboard**

![Image](./image/oauth/onboard-oauth.png)

4. Add **JWKS endpoint** and **callback URLs** > Click **Submit**

   - Make sure the app description is not empty.
   - Multiple callback URLs are allowed with the seperation of comma.

   ![Image](./image/oauth/onboarding-oauth.png)

Once application is onboard successfully, the portal will redirect back to the application page with the following view in Oauth 2.1. The **login url (example)** are just demonstration on how the login url can be constructed with the supplied callbacks. **It cannot be use for production**.

![Image](./image/oauth/onboarded-oauth.png)

### Note:

Once the application is onboard to OAuth 2.1 successfully, portal disable the function to delete the application. OAuth 2.1 status needs to be updated as "inactive" before deleting. View **Oauth 2.1** > Click on **Change Status to inactive**. Once the status become inactive, proceed to delete the application.

## Update Oauth 2.1

1. **Apps** tab > **Select Application** > Click **Edit Application**
2. View **Authentication** tab > **Oauth 2.1**
3. Update **JWKS endpoint** or **callback URLs** > Click **Apply Changes**

![Image](./image/oauth/update-oauth-info.png)
