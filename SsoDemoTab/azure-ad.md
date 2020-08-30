# Azure AD application

Please follow these steps to create an Azure AD application for single-sign on for your Teams app. For more details, please see this [article](https://docs.microsoft.com/en-us/microsoftteams/platform/tabs/how-to/authentication/auth-aad-sso).

## 1. Create the app

![Create application](../images/Azure-AD-1.jpg)

## 2. Set name and account types

![Set name and account types](../images/Azure-AD-2.jpg)

## 3. Add a client secret

![Add client secret](../images/Azure-AD-3.jpg)

## 4. Set API permissions

![Set API permissions](../images/Azure-AD-4.jpg)

## 5. Give consent

![Give consent](../images/Azure-AD-6.jpg)

## 6. Expose your API

- Scope name: access_as_user
- Client ID for Teams web: 5e3ce6c0-2b1f-4285-8d4b-75ee78787346
- Client ID for Teams mobile/desktop: 1fec8e78-bce4-4aaf-ab1b-5451cc387264

![Expose API](../images/Azure-AD-5.jpg)
