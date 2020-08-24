# teams-hackathon
Microsoft Teams hackathon at Schultz


Teams overview
Teams tab using Graph API
Graph overview

Tenant creator
berschultz@hotmail.com

Tenant
berschultz.onmicrosoft.com
admin@berschultz.onmicrosoft.com
other users password
admin.microsoft.com

Kør lokalt
c:\tools\ngrok.exe http 3007 -region eu
https://67c612fc8d78.eu.ngrok.io

Simple Tab

1. Opret en mail konto
2. Opret en developer subscription
3. Aktiver side-loading in teams: https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/build-and-test/prepare-your-o365-tenant
4. Installer ngrok og kør
5. Installer yeoman: https://docs.microsoft.com/en-us/microsoftteams/platform/tutorials/get-started-yeoman
6. Generer teams app og kør lokalt
7. Installer app studio
8. Opret og deploy app

yo teams
npm install
gulp manifest
gulp build
gulp serve

Graph Tab

1. Opret AD applikation - https://docs.microsoft.com/en-us/microsoftteams/platform/tabs/how-to/authentication/auth-aad-sso
   Permissions: email, Group.Read.All, offline_access, openid, profile, User.Read
   App ID URI: api://67c612fc8d78.eu.ngrok.io/4605e3cd-7111-45e3-bcc7-2eeefc078e84
   Scope: access_as_user
   Authorized Client ID: 5e3ce6c0-2b1f-4285-8d4b-75ee78787346
2. Hent SsoTabDemo
3. Konfigurer .env

gulp manifest
gulp build
gulp serve

Auth token
https://www.wictorwilen.se/blog/microsoft-teams-tabs-sso-and-microsoft-graph-the-on-behalf-of-blog-post/

Consent (er det nødvendigt?)
https://login.microsoftonline.com/common/adminconsent?client_id=4605e3cd-7111-45e3-bcc7-2eeefc078e84




