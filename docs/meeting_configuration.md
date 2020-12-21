# Meeting Configuration

## Overview

| API | Endpoint |
|-----|----------|
| Get Meeting User Settings | `extension/meeting/user-settings` |

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