<div align="center">

# Voicemail Service

![BW_all](../../.readme_images/BW_Voice_Messaging.png)

</div>

## Description
A sample app that mimics a voicemail service using Bandwidth's Voice API and Recording

## How It Works
When someone calls the number, they are given a prompt to leave a voicemail. After a timeout of 3 minutes or `#` is pressed, the recording ends. The user has the option of hearing the recording, and re-recording if necessary.

Once the recording is done, the user will receive an MMS with the recording.

## Running The App

### Environmental Variables
The following environmental variables need to be set

| Variable | Description |
|--|--|
| MESSAGING_ACCOUNT_ID | Your Bandwidth Messaging account ID |
| MESSAGING_API_TOKEN | Your Bandwidth Messaging API token |
| MESSAGING_API_SECRET | Your Bandwidth Messaging API secret |
| MESSAGING_APPLICATION_ID | Your Bandwidth Messaging application ID |
| VOICE_ACCOUNT_ID | Your Bandwidth Voice account ID |
| VOICE_API_USERNAME | Your Bandwidth Voice API username |
| VOICE_API_PASSWORD | Your Bandwidth Voice API password |
| VOICE_APPLICATION_ID | Your Bandwidth Voice application ID |
| BASE_URL | The base url of the server running this application |

### Callback URLs For Bandwidth Applications

| Callback Type | URL |
|--|--|
| Inbound Voice Callback | <url>/VoiceCallback |
| Call Status Callback | <url>/VoiceCallbackStatus |

### Commands
Run the following commands to get started

```
gem install bundler
bundle install
ruby app.rb -p <port>
```

where `port` is the port to run the app on. Unassigned, `port` will default to `4567`.
