# Meeting Configuration

## Overview

| API | Endpoint Abbreviation |
|-----|----------|
| Get Meeting User Settings | `GET extension/meeting/user-settings` |
| Get Locked Meeting Settings | `GET account/meeting/locked-settings` |
| Get Meeting Service Info | `GET extension/meeting/service-info` |



## Get Meeting User Settings

`GET /restapi/v1.0/account/{accountId}/extension/{extensionId}/meeting/user-settings`

```json
{
  "recording":{
    "localRecording":true,
    "cloudRecording":true,
    "recordSpeakerView":true,
    "recordGalleryView":false,
    "recordAudioFile":true,
    "saveChatText":true,
    "showTimestamp":false,
    "autoRecording":"none",
    "autoDeleteCmr":false
  },
  "scheduleMeeting":{
    "pstnPasswordProtected":false,
    "requirePasswordForSchedulingNewMeetings":true,
    "requirePasswordForScheduledMeetings":false,
    "requirePasswordForInstantMeetings":true,
    "requirePasswordForPmiMeetings":"none",
    "pmiPassword":"",
    "startHostVideo":true,
    "startParticipantsVideo":false,
    "audioOptions":[
      "Phone",
      "ComputerAudio"
    ],
    "allowJoinBeforeHost":false,
    "usePmiForScheduledMeetings":false,
    "usePmiForInstantMeetings":false,
    "enforceLogin":true
  },
  "telephony":{
    "thirdPartyAudio":false,
    "audioConferenceInfo":""
  }
}
```

## Get Locked Meeting Settings

`GET /restapi/v1.0/account/{accountId}/meeting/locked-settings`

```json
{
  "scheduleMeeting":{
    "startHostVideo":false,
    "startParticipantsVideo":false,
    "audioOptions":false,
    "allowJoinBeforeHost":false,
    "requirePasswordForSchedulingNewMeetings":false,
    "requirePasswordForInstantMeetings":false,
    "requirePasswordForPmiMeetings":false,
    "enforceLogin":false
  },
  "recording":{
    "localRecording":false,
    "cloudRecording":true,
    "autoRecording":false,
    "cloudRecordingDownload":false,
    "hostDeleteCloudRecording":false,
    "accountUserAccessRecording":false,
    "autoDeleteCmr":false
  },
  "telephony":{
    "thirdPartyAudio":false
  }
}
```

### Get Meeting Service Info

`GET /restapi/v1.0/account/{accountId}/extension/{extensionId}/meeting/service-info`

```json
{
  "uri":"http://platform.ringcentral.com/restapi/v1.0/account/11111111/extension/22222222/meeting/service-info",
  "supportUri":"http://success.ringcentral.com",
  "intlDialInNumbersUri":"https://meetings.ringcentral.com/teleconference",
  "domain":"rcm.ringcentral.com",
  "externalUserInfo":{
    "userId":"3333333333-44444444444",
    "accountId":"11111111",
    "userType":2,
    "userToken":"5555555555555555",
    "hostKey":"666666",
    "personalMeetingId":"7777777",
    "usePmiForInstantMeetings":false
  },
  "dialInNumbers":[
    {
      "phoneNumber":"+14705550100",
      "formattedNumber":"(470) 555-0100",
      "location":"US East",
      "country":{
        "uri":"http://platform.ringcentral.com/restapi/v1.0/dictionary/country/1",
        "id":"1",
        "name":"United States",
        "isoCode":"US",
        "callingCode":"1"
      }
    },
    {
      "phoneNumber":"+14695550100",
      "formattedNumber":"(469) 555-0100",
      "location":"US South",
      "country":{
        "uri":"http://platform.ringcentral.com/restapi/v1.0/dictionary/country/1",
        "id":"1",
        "name":"United States",
        "isoCode":"US",
        "callingCode":"1"
      }
    },
    {
      "phoneNumber":"+17735550100",
      "formattedNumber":"(773) 555-0100",
      "location":"US North",
      "country":{
        "uri":"http://platform.ringcentral.com/restapi/v1.0/dictionary/country/1",
        "id":"1",
        "name":"United States",
        "isoCode":"US",
        "callingCode":"1"
      }
    },
    {
      "phoneNumber":"+16235550100",
      "formattedNumber":"(623) 555-0100",
      "location":"US West",
      "country":{
        "uri":"http://platform.ringcentral.com/restapi/v1.0/dictionary/country/1",
        "id":"1",
        "name":"United States",
        "isoCode":"US",
        "callingCode":"1"
      }
    },
    {
      "phoneNumber":"+17205550100",
      "formattedNumber":"(720) 555-0100",
      "location":"US Central",
      "country":{
        "uri":"http://platform.ringcentral.com/restapi/v1.0/dictionary/country/1",
        "id":"1",
        "name":"United States",
        "isoCode":"US",
        "callingCode":"1"
      }
    }
  ]
}
```