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