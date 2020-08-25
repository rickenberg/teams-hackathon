# teams-hackathon
Microsoft Teams hackathon at Schultz 2020

## Agenda

1. Simple tab demo
2. MS Graph tour
3. SSO tab demo

## Prerequisites

- Create a one-off mail account (e.g. outlook.com)
- Use that e-mail address to create a [Microsoft 365 developer tenant](https://developer.microsoft.com/en-us/microsoft-365/dev-program) with
- If you want, load the test users and their test data in the new tenant
- Enable app [side-loading in Teams](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/build-and-test/)
- Install [app studio in Teams](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/build-and-test/app-studio-overview) on the new tenant

## Demo setup

The two demos here are based on Team tabs you deploy to your Microsoft 365 developer tenant. The code for tabs will run on your local machine. This allows a faster development cycle from making your code changes until you can see the running app in Teams. Since Teams is a cloud offering and because there is no local test bench you can install, you will need a reverse proxy, such as [ngrok](https://ngrok.com/) to route HTTP requests from the cloud to a web server on your machine.

The ngrok free version has the limitation that you cannot give it a sub domain when starting up. Every time you start up ngrok, you will hence get a new URL. When the URL of your app changes, you will have to update the manifest in Teams and, if applicable, the Azure AD application backing it.

## Simple tab demo
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


## SSO tab demo
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