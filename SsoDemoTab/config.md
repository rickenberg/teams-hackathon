# How to configure the app

There is a sample configuration in the `sample.env` file. The `.env` file is the actual configuration file. So create that file and set your settings there. Below is the contents of the sample configuration file.

```
HOSTNAME=67c612fc8d78.eu.ngrok.io
PORT=3007
NGROK_AUTH=https
NGROK_SUBDOMAIN=67c612fc8d78
NGROK_REGION=eu
DEBUG=msteams

SSODEMO_APP_ID=4605e3cd-7111-45e3-bcc7-2eeefc078e84
SSODEMO_APP_URI=api://67c612fc8d78.eu.ngrok.io/4605e3cd-7111-45e3-bcc7-2eeefc078e84
SSODEMO_APP_SECRET=niW7N~s8W-TW231BYD_1PrgzBc5o-._h03
SSODEMO_APP_SCOPES=https://graph.microsoft.com/Group.Read.All,https://graph.microsoft.com/User.Read
```

Most settings are pretty self explanatory. You will get the SSODEMO_APP_* settings when creating the Azure AD application. Follow the [Azure AD guide](azure-ad.md) for this. After starting up the ngrok tool, it will show you the current URL, so grab the settings from there. Please note, that the ngrok free version does not allow you to use a specific sub domain. Each time you start the tool, you will get a new sub domain and you will need to reconfigure the application.

The configuration settings here are also used when generating the Teams manifest with the `gulp manifest` command. Please make sure to update the `.env` file before running that command.