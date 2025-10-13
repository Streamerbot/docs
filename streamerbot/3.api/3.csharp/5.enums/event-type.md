---
title: EventType
description: C# enum definition for EventType
name: EventType
---

Within any action, the value of the `%__source%`{lang=cs} variable indicates which event triggered the action.

This variable is of type `EventType`{lang=cs}, which is an enumeration (enum) defined in C#.

## Usage Example

:read-more{to=/api/csharp/methods/core/events/get-event-type}

```csharp [Example.cs]
using System;

public class CPHInline
{
  public bool Execute()
  {
    // Get the EventType for the current action
    EventType eventType = CPH.GetEventType();

    // Compare EventType with switch or if
    switch(eventType)
    {
      case EventType.TwitchSub:
        // Do something with TwitchSub events...
        break;
      case EventType.TwitchReSub:
        // Do something with TwithReSub events...
        break;
    }

    return true;
  }
}
```

## Enum Values by Source

### Application

| Value                                 | Description                                     |
| ------------------------------------- | ----------------------------------------------- |
| `EventType.ApplicationActionAdded`    | [No description provided]{.text-muted .text-xs} |
| `EventType.ApplicationActionDeleted`  | [No description provided]{.text-muted .text-xs} |
| `EventType.ApplicationActionUpdated`  | [No description provided]{.text-muted .text-xs} |
| `EventType.ApplicationCommandAdded`   | [No description provided]{.text-muted .text-xs} |
| `EventType.ApplicationCommandDeleted` | [No description provided]{.text-muted .text-xs} |
| `EventType.ApplicationCommandUpdated` | [No description provided]{.text-muted .text-xs} |
| `EventType.ApplicationImport`         | [No description provided]{.text-muted .text-xs} |

### Chat Window

| Value                        | Description                                     |
| ---------------------------- | ----------------------------------------------- |
| `EventType.ChatWindowAction` | [No description provided]{.text-muted .text-xs} |

### Command

| Value                        | Description                                     |
| ---------------------------- | ----------------------------------------------- |
| `EventType.CommandCooldown`  | [No description provided]{.text-muted .text-xs} |
| `EventType.CommandTriggered` | [No description provided]{.text-muted .text-xs} |

### CrowdControl

| Value                                      | Description                                     |
| ------------------------------------------ | ----------------------------------------------- |
| `EventType.CrowdControlCoinExchange`       | [No description provided]{.text-muted .text-xs} |
| `EventType.CrowdControlEffectFailure`      | [No description provided]{.text-muted .text-xs} |
| `EventType.CrowdControlEffectRequest`      | [No description provided]{.text-muted .text-xs} |
| `EventType.CrowdControlEffectSuccess`      | [No description provided]{.text-muted .text-xs} |
| `EventType.CrowdControlGameSessionEnd`     | [No description provided]{.text-muted .text-xs} |
| `EventType.CrowdControlGameSessionStart`   | [No description provided]{.text-muted .text-xs} |
| `EventType.CrowdControlTimedEffectEnded`   | [No description provided]{.text-muted .text-xs} |
| `EventType.CrowdControlTimedEffectStarted` | [No description provided]{.text-muted .text-xs} |
| `EventType.CrowdControlTimedEffectUpdated` | [No description provided]{.text-muted .text-xs} |

### Custom

| Value                       | Description                                     |
| --------------------------- | ----------------------------------------------- |
| `EventType.CustomCodeEvent` | [No description provided]{.text-muted .text-xs} |
| `EventType.CustomEvent`     | [No description provided]{.text-muted .text-xs} |

### DonorDrive

| Value                                | Description                                     |
| ------------------------------------ | ----------------------------------------------- |
| `EventType.DonorDriveDonation`       | [No description provided]{.text-muted .text-xs} |
| `EventType.DonorDriveIncentive`      | [No description provided]{.text-muted .text-xs} |
| `EventType.DonorDriveProfileUpdated` | [No description provided]{.text-muted .text-xs} |

### Elgato Camera Hub

| Value                                                        | Description                                     |
| ------------------------------------------------------------ | ----------------------------------------------- |
| `EventType.ElgatoCameraHubConnected`                         | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubDisconnected`                      | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterAutoScrollChapterDisabled` | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterAutoScrollChapterEnabled`  | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterAutoScrollDisabled`        | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterAutoScrollEnabled`         | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterBackgroundColorChanged`    | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterBrightnessChanged`         | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterChannelsChanged`           | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterConnected`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterContrastChanged`           | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterCrosshairColorChanged`     | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterCrosshairDisabled`         | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterCrosshairEnabled`          | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterCrosshairImageChanged`     | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterDisconnected`              | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterFontChanged`               | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterFontColorChanged`          | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterFontSizeChanged`           | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterHorizontalMarginChanged`   | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterLineSpacingChanged`        | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterModeChanged`               | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterOpacityChanged`            | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterScrollSpeedChanged`        | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterSelectedChannelChanged`    | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterSelectedChapterChanged`    | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterSelectedScriptChanged`     | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubPrompterVerticalMarginChanged`     | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubSelectedWebcamChanged`             | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubTiltChanged`                       | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamActivated`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamAntiFlickerChanged`          | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamARLensChanged`               | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamAutoExposureDisabled`        | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamAutoExposureEnabled`         | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamAutoFocusDisabled`           | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamAutoFocusEnabled`            | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamAutoWhiteBalanceDisabled`    | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamAutoWhiteBalanceEnabled`     | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamBitrateChanged`              | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamBrightnessChanged`           | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamConnected`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamContrastChanged`             | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamDeactivated`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamDeviceOrientationChanged`    | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamExposureAutoLockDisabled`    | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamExposureAutoLockEnabled`     | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamFlashDisabled`               | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamFlashEnabled`                | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamFlipped`                     | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamFocusChanged`                | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamISOChanged`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamLensChanged`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamLiveISOChanged`              | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamLiveShutterSpeedChanged`     | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamLiveWhiteBalanceChanged`     | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamLiveWhiteBalanceTintChanged` | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamMirrored`                    | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamNoiseReductionDisabled`      | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamNoiseReductionEnabled`       | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamOverscanChanged`             | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamPanChanged`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamrDisconnected`               | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamSaturationChanged`           | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamSharpnessChanged`            | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamShutterSpeedChanged`         | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamSnapshotTaken`               | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamWhiteBalanceChanged`         | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamWhiteBalanceTintChanged`     | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoCameraHubWebcamZoomChanged`                 | [No description provided]{.text-muted .text-xs} |

### Elgato Stream Deck

| Value                              | Description                                     |
| ---------------------------------- | ----------------------------------------------- |
| `EventType.StreamDeckAction`       | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamDeckConnected`    | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamDeckDisconnected` | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamDeckInfo`         | [No description provided]{.text-muted .text-xs} |

### Elgato Wave Link

| Value                                                   | Description                                     |
| ------------------------------------------------------- | ----------------------------------------------- |
| `EventType.ElgatoWaveLinkConnected`                     | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkDisconnected`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkFilterAdded`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkFilterBypassStateChanged`      | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkFilterChanged`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkFilterDeleted`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkInputLevelMeterChanged`        | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkInputMuteChanged`              | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkInputNameChanged`              | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkInputVolumeChanged`            | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkMicrophoneBalanceChanged`      | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkMicrophoneGainChanged`         | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkMicrophoneMuteChanged`         | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkMicrophoneOutputVolumeChanged` | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkMicrophoneSettingChanged`      | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkOutputLevelMeterChanged`       | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkOutputMuteChanged`             | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkOutputSwitched`                | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkOutputVolumeChanged`           | [No description provided]{.text-muted .text-xs} |
| `EventType.ElgatoWaveLinkSelectedOutputChanged`         | [No description provided]{.text-muted .text-xs} |

### File

| Value                          | Description                                     |
| ------------------------------ | ----------------------------------------------- |
| `EventType.FileTailChanged`    | [No description provided]{.text-muted .text-xs} |
| `EventType.FileWatcherChanged` | [No description provided]{.text-muted .text-xs} |
| `EventType.FileWatcherCreated` | [No description provided]{.text-muted .text-xs} |
| `EventType.FileWatcherDeleted` | [No description provided]{.text-muted .text-xs} |
| `EventType.FileWatcherRenamed` | [No description provided]{.text-muted .text-xs} |

### Fourthwall

| Value                                       | Description                                     |
| ------------------------------------------- | ----------------------------------------------- |
| `EventType.FourthwallDonation`              | [No description provided]{.text-muted .text-xs} |
| `EventType.FourthwallGiftDrawEnded`         | [No description provided]{.text-muted .text-xs} |
| `EventType.FourthwallGiftDrawStarted`       | [No description provided]{.text-muted .text-xs} |
| `EventType.FourthwallGiftPurchase`          | [No description provided]{.text-muted .text-xs} |
| `EventType.FourthwallNewsletterSubscribed`  | [No description provided]{.text-muted .text-xs} |
| `EventType.FourthwallOrderPlaced`           | [No description provided]{.text-muted .text-xs} |
| `EventType.FourthwallOrderUpdated`          | [No description provided]{.text-muted .text-xs} |
| `EventType.FourthwallProductCreated`        | [No description provided]{.text-muted .text-xs} |
| `EventType.FourthwallProductUpdated`        | [No description provided]{.text-muted .text-xs} |
| `EventType.FourthwallSubscriptionChanged`   | [No description provided]{.text-muted .text-xs} |
| `EventType.FourthwallSubscriptionExpired`   | [No description provided]{.text-muted .text-xs} |
| `EventType.FourthwallSubscriptionPurchased` | [No description provided]{.text-muted .text-xs} |
| `EventType.FourthwallThankYouSent`          | [No description provided]{.text-muted .text-xs} |

### Global Variable

| Value                             | Description                                     |
| --------------------------------- | ----------------------------------------------- |
| `EventType.GlobalVariableCreated` | [No description provided]{.text-muted .text-xs} |
| `EventType.GlobalVariableDeleted` | [No description provided]{.text-muted .text-xs} |
| `EventType.GlobalVariableUpdated` | [No description provided]{.text-muted .text-xs} |

### Group

| Value                         | Description                                     |
| ----------------------------- | ----------------------------------------------- |
| `EventType.GroupAdded`        | [No description provided]{.text-muted .text-xs} |
| `EventType.GroupCleared`      | [No description provided]{.text-muted .text-xs} |
| `EventType.GroupRemoved`      | [No description provided]{.text-muted .text-xs} |
| `EventType.GroupUsersAdded`   | [No description provided]{.text-muted .text-xs} |
| `EventType.GroupUsersRemoved` | [No description provided]{.text-muted .text-xs} |

### HypeRate.io

| Value                                 | Description                                     |
| ------------------------------------- | ----------------------------------------------- |
| `EventType.HypeRateConnected`         | [No description provided]{.text-muted .text-xs} |
| `EventType.HypeRateDisconnected`      | [No description provided]{.text-muted .text-xs} |
| `EventType.HypeRateHeartRatePulse`    | [No description provided]{.text-muted .text-xs} |
| `EventType.HypeRateTwitchClipCreated` | [No description provided]{.text-muted .text-xs} |

### Input

| Value                       | Description                                     |
| --------------------------- | ----------------------------------------------- |
| `EventType.InputKeyPress`   | [No description provided]{.text-muted .text-xs} |
| `EventType.InputMouseClick` | [No description provided]{.text-muted .text-xs} |

### Kick

| Value                                       | Description                                     |
| ------------------------------------------- | ----------------------------------------------- |
| `EventType.KickBroadcasterAuthenticated`    | [No description provided]{.text-muted .text-xs} |
| `EventType.KickBroadcasterChatConnected`    | [No description provided]{.text-muted .text-xs} |
| `EventType.KickBroadcasterChatDisconnected` | [No description provided]{.text-muted .text-xs} |
| `EventType.KickChannelUpdate`               | [No description provided]{.text-muted .text-xs} |
| `EventType.KickChatMessage`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.KickFirstWords`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.KickFollow`                      | [No description provided]{.text-muted .text-xs} |
| `EventType.KickGiftSubscription`            | [No description provided]{.text-muted .text-xs} |
| `EventType.KickMassGiftSubscription`        | [No description provided]{.text-muted .text-xs} |
| `EventType.KickPresentViewers`              | [No description provided]{.text-muted .text-xs} |
| `EventType.KickResubscription`              | [No description provided]{.text-muted .text-xs} |
| `EventType.KickSevenTVEmoteAdded`           | [No description provided]{.text-muted .text-xs} |
| `EventType.KickSevenTVEmoteRemoved`         | [No description provided]{.text-muted .text-xs} |
| `EventType.KickStreamOffline`               | [No description provided]{.text-muted .text-xs} |
| `EventType.KickStreamOnline`                | [No description provided]{.text-muted .text-xs} |
| `EventType.KickSubscription`                | [No description provided]{.text-muted .text-xs} |
| `EventType.KickUserBanned`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.KickUserTimedOut`                | [No description provided]{.text-muted .text-xs} |
| `EventType.KickViewerCountUpdate`           | [No description provided]{.text-muted .text-xs} |

### Ko-Fi

| Value                          | Description                                     |
| ------------------------------ | ----------------------------------------------- |
| `EventType.KofiCommission`     | [No description provided]{.text-muted .text-xs} |
| `EventType.KofiDonation`       | [No description provided]{.text-muted .text-xs} |
| `EventType.KofiResubscription` | [No description provided]{.text-muted .text-xs} |
| `EventType.KofiShopOrder`      | [No description provided]{.text-muted .text-xs} |
| `EventType.KofiSubscription`   | [No description provided]{.text-muted .text-xs} |

### Meld Studio

| Value                                             | Description                                     |
| ------------------------------------------------- | ----------------------------------------------- |
| `EventType.MeldStudioConnected`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.MeldStudioDisconnected`                | [No description provided]{.text-muted .text-xs} |
| `EventType.MeldStudioEvent`                       | [No description provided]{.text-muted .text-xs} |
| `EventType.MeldStudioLayerVisbilityChanged`       | [No description provided]{.text-muted .text-xs} |
| `EventType.MeldStudioLEffectEnabledStateChanged`  | [No description provided]{.text-muted .text-xs} |
| `EventType.MeldStudioRecordingStarted`            | [No description provided]{.text-muted .text-xs} |
| `EventType.MeldStudioRecordingStopped`            | [No description provided]{.text-muted .text-xs} |
| `EventType.MeldStudioSceneChanged`                | [No description provided]{.text-muted .text-xs} |
| `EventType.MeldStudioStreamingStarted`            | [No description provided]{.text-muted .text-xs} |
| `EventType.MeldStudioStreamingStopped`            | [No description provided]{.text-muted .text-xs} |
| `EventType.MeldStudioTrackMonitoringStateChanged` | [No description provided]{.text-muted .text-xs} |
| `EventType.MeldStudioTrackMustedStateChanged`     | [No description provided]{.text-muted .text-xs} |

### MIDI

| Value                   | Description                                     |
| ----------------------- | ----------------------------------------------- |
| `EventType.MidiMessage` | [No description provided]{.text-muted .text-xs} |

### Misc

| Value              | Description                                     |
| ------------------ | ----------------------------------------------- |
| `EventType.Custom` | [No description provided]{.text-muted .text-xs} |
| `EventType.Test`   | [No description provided]{.text-muted .text-xs} |

### OBS Studio

| Value                           | Description                                     |
| ------------------------------- | ----------------------------------------------- |
| `EventType.ObsConnected`        | [No description provided]{.text-muted .text-xs} |
| `EventType.ObsDisconnected`     | [No description provided]{.text-muted .text-xs} |
| `EventType.ObsEvent`            | [No description provided]{.text-muted .text-xs} |
| `EventType.ObsRecordingStarted` | [No description provided]{.text-muted .text-xs} |
| `EventType.ObsRecordingStopped` | [No description provided]{.text-muted .text-xs} |
| `EventType.ObsSceneChanged`     | [No description provided]{.text-muted .text-xs} |
| `EventType.ObsStreamingStarted` | [No description provided]{.text-muted .text-xs} |
| `EventType.ObsStreamingStopped` | [No description provided]{.text-muted .text-xs} |
| `EventType.ObsVendorEvent`      | [No description provided]{.text-muted .text-xs} |

### Pally.gg

| Value                           | Description                                     |
| ------------------------------- | ----------------------------------------------- |
| `EventType.PallyggCampaignTip`  | [No description provided]{.text-muted .text-xs} |
| `EventType.PallyggConnected`    | [No description provided]{.text-muted .text-xs} |
| `EventType.PallyggDisconnected` | [No description provided]{.text-muted .text-xs} |

### Patreon

| Value                            | Description                                     |
| -------------------------------- | ----------------------------------------------- |
| `EventType.PatreonFollowCreated` | [No description provided]{.text-muted .text-xs} |
| `EventType.PatreonFollowDeleted` | [No description provided]{.text-muted .text-xs} |
| `EventType.PatreonPledgeCreated` | [No description provided]{.text-muted .text-xs} |
| `EventType.PatreonPledgeDeleted` | [No description provided]{.text-muted .text-xs} |
| `EventType.PatreonPledgeUpdated` | [No description provided]{.text-muted .text-xs} |

### Process

| Value                      | Description                                     |
| -------------------------- | ----------------------------------------------- |
| `EventType.ProcessStarted` | [No description provided]{.text-muted .text-xs} |
| `EventType.ProcessStopped` | [No description provided]{.text-muted .text-xs} |

### Pulsoid

| Value                             | Description                                     |
| --------------------------------- | ----------------------------------------------- |
| `EventType.PulsoidHeartRatePulse` | [No description provided]{.text-muted .text-xs} |

### Quote

| Value                  | Description                                     |
| ---------------------- | ----------------------------------------------- |
| `EventType.QuoteAdded` | [No description provided]{.text-muted .text-xs} |
| `EventType.QuoteShow`  | [No description provided]{.text-muted .text-xs} |

### Raw

| Value                          | Description                                     |
| ------------------------------ | ----------------------------------------------- |
| `EventType.RawAction`          | [No description provided]{.text-muted .text-xs} |
| `EventType.RawActionCompleted` | [No description provided]{.text-muted .text-xs} |
| `EventType.RawSubAction`       | [No description provided]{.text-muted .text-xs} |

### Shopify

| Value                           | Description                                     |
| ------------------------------- | ----------------------------------------------- |
| `EventType.ShopifyOrderCreated` | [No description provided]{.text-muted .text-xs} |
| `EventType.ShopifyOrderPaid`    | [No description provided]{.text-muted .text-xs} |

### Speaker.bot

| Value                              | Description                                     |
| ---------------------------------- | ----------------------------------------------- |
| `EventType.SpeakerBotConnected`    | [No description provided]{.text-muted .text-xs} |
| `EventType.SpeakerBotDisconnected` | [No description provided]{.text-muted .text-xs} |

### Speech

| Value                             | Description                                     |
| --------------------------------- | ----------------------------------------------- |
| `EventType.SpeechToTextCommand`   | [No description provided]{.text-muted .text-xs} |
| `EventType.SpeechToTextDictation` | [No description provided]{.text-muted .text-xs} |

### StreamElements

| Value                                   | Description                                     |
| --------------------------------------- | ----------------------------------------------- |
| `EventType.StreamElementsAuthenticated` | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamElementsConnected`     | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamElementsDisconnected`  | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamElementsMerch`         | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamElementsTip`           | [No description provided]{.text-muted .text-xs} |

### Streamer.bot

| Value                                             | Description                                     |
| ------------------------------------------------- | ----------------------------------------------- |
| `EventType.StreamerBotCustomWebook`               | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamerBotRemoteInstanceConnected`    | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamerBotRemoteInstanceDisconnected` | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamerBotRemoteInstanceSignal`       | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamerBotRemoteInstanceTrigger`      | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamerbotExiting`                    | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamerbotStarted`                    | [No description provided]{.text-muted .text-xs} |

### Streamlabs

| Value                                 | Description                                     |
| ------------------------------------- | ----------------------------------------------- |
| `EventType.StreamlabsAuthenticated`   | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamlabsCharityDonation` | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamlabsConnected`       | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamlabsDisconnected`    | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamlabsDonation`        | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamlabsMerchandise`     | [No description provided]{.text-muted .text-xs} |

### Streamlabs Desktop

| Value                                         | Description                                     |
| --------------------------------------------- | ----------------------------------------------- |
| `EventType.StreamlabsDesktopConnected`        | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamlabsDesktopDisconnected`     | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamlabsDesktopRecordingStarted` | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamlabsDesktopRecordingStopped` | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamlabsDesktopSceneChanged`     | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamlabsDesktopStreamingStarted` | [No description provided]{.text-muted .text-xs} |
| `EventType.StreamlabsDesktopStreamingStopped` | [No description provided]{.text-muted .text-xs} |

### System

| Value                              | Description                                     |
| ---------------------------------- | ----------------------------------------------- |
| `EventType.SystemClipboardChanged` | [No description provided]{.text-muted .text-xs} |

### T.I.T.S.

| Value                                           | Description                                     |
| ----------------------------------------------- | ----------------------------------------------- |
| `EventType.ThrowingSystemConnected`             | [No description provided]{.text-muted .text-xs} |
| `EventType.ThrowingSystemEventsConnected`       | [No description provided]{.text-muted .text-xs} |
| `EventType.ThrowingSystemEventsDisconnected`    | [No description provided]{.text-muted .text-xs} |
| `EventType.ThrowingSystemItemHit`               | [No description provided]{.text-muted .text-xs} |
| `EventType.ThrowingSystemTriggerActivated`      | [No description provided]{.text-muted .text-xs} |
| `EventType.ThrowingSystemTriggerEnded`          | [No description provided]{.text-muted .text-xs} |
| `EventType.ThrowingSystemWebsocketConnected`    | [No description provided]{.text-muted .text-xs} |
| `EventType.ThrowingSystemWebsocketDisconnected` | [No description provided]{.text-muted .text-xs} |

### Timed Actions

| Value                   | Description                                     |
| ----------------------- | ----------------------------------------------- |
| `EventType.TimedAction` | [No description provided]{.text-muted .text-xs} |

### TipeeeStream

| Value                            | Description                                     |
| -------------------------------- | ----------------------------------------------- |
| `EventType.TipeeeStreamDonation` | [No description provided]{.text-muted .text-xs} |

### Toast

| Value                       | Description                                     |
| --------------------------- | ----------------------------------------------- |
| `EventType.ToastActivation` | [No description provided]{.text-muted .text-xs} |

### TreatStream

| Value                                | Description                                     |
| ------------------------------------ | ----------------------------------------------- |
| `EventType.TreatStreamAuthenticated` | [No description provided]{.text-muted .text-xs} |
| `EventType.TreatStreamConnected`     | [No description provided]{.text-muted .text-xs} |
| `EventType.TreatStreamDisconnected`  | [No description provided]{.text-muted .text-xs} |
| `EventType.TreatStreamTreat`         | [No description provided]{.text-muted .text-xs} |

### Trovo

| Value                                        | Description                                     |
| -------------------------------------------- | ----------------------------------------------- |
| `EventType.TrovoBroadcasterAuthenticated`    | [No description provided]{.text-muted .text-xs} |
| `EventType.TrovoBroadcasterChatConnected`    | [No description provided]{.text-muted .text-xs} |
| `EventType.TrovoBroadcasterChatDisconnected` | [No description provided]{.text-muted .text-xs} |
| `EventType.TrovoChatMessage`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.TrovoCustomSpellCast`             | [No description provided]{.text-muted .text-xs} |
| `EventType.TrovoFirstWords`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.TrovoFollow`                      | [No description provided]{.text-muted .text-xs} |
| `EventType.TrovoGiftSubscription`            | [No description provided]{.text-muted .text-xs} |
| `EventType.TrovoMassGiftSubscription`        | [No description provided]{.text-muted .text-xs} |
| `EventType.TrovoPresentViewers`              | [No description provided]{.text-muted .text-xs} |
| `EventType.TrovoRaid`                        | [No description provided]{.text-muted .text-xs} |
| `EventType.TrovoResubscription`              | [No description provided]{.text-muted .text-xs} |
| `EventType.TrovoSpellCast`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.TrovoStreamOffline`               | [No description provided]{.text-muted .text-xs} |
| `EventType.TrovoStreamOnline`                | [No description provided]{.text-muted .text-xs} |
| `EventType.TrovoSubscription`                | [No description provided]{.text-muted .text-xs} |

### Twitch

| Value                                             | Description                                     |
| ------------------------------------------------- | ----------------------------------------------- |
| `EventType.TwitchAdRun`                           | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchAnnouncement`                    | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchAutomaticRewardRedemption`       | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchAutoModMessageHeld`              | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchAutoModMessageUpdate`            | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchBetterTTVEmoteAdded`             | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchBetterTTVEmoteRemoved`           | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchBitsBadgeTier`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchBlockedTermsAdded`               | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchBlockedTermsDeleted`             | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchBotEventSubConnected`            | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchBotEventSubDisconnected`         | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchBotWhisper`                      | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchBroadcasterAuthenticated`        | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchBroadcasterChatConnected`        | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchBroadcasterChatDisconnected`     | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchBroadcasterEventSubConnected`    | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchBroadcasterEventSubDisconnected` | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchBroadcastUpdate`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchCharityCompleted`                | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchCharityDonation`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchCharityProgress`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchCharityStarted`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchChatCleared`                     | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchChatEmoteModeOff`                | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchChatEmoteModeOn`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchChatFollowerModeChanged`         | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchChatFollowerModeOff`             | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchChatFollowerModeOn`              | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchChatMessage`                     | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchChatMessageDeleted`              | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchChatSlowModeChanged`             | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchChatSlowModeOff`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchChatSlowModeOn`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchChatSubscriberModeOff`           | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchChatSubscriberModeOn`            | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchChatUniqueModeOff`               | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchChatUniqueModeOn`                | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchCheer`                           | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchCoinCheer`                       | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchCommunityGoalContribution`       | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchCommunityGoalEnded`              | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchFirstWord`                       | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchFollow`                          | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchGiftBomb`                        | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchGiftPaidUpgrade`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchGiftSub`                         | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchGoalBegin`                       | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchGoalEnd`                         | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchGoalProgress`                    | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchGuestStarGuestUpdate`            | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchGuestStarSessionBegin`           | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchGuestStarSessionEnd`             | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchGuestStarSettingsUpdate`         | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchGuestStarSlotUpdate`             | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchHypeChat`                        | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchHypeChatLevel`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchHypeTrainEnd`                    | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchHypeTrainLevelUp`                | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchHypeTrainStart`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchHypeTrainUpdate`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchModeratorAdded`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchModeratorRemoved`                | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPayItForward`                    | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPermittedTermsAdded`             | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPermittedTermsDeleted`           | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPollArchived`                    | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPollCompleted`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPollCreated`                     | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPollTerminated`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPollUpdated`                     | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPowerUp`                         | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPredictionCanceled`              | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPredictionCompleted`             | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPredictionCreated`               | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPredictionLocked`                | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPredictionUpdated`               | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPresentViewers`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPrimePaidUpgrade`                | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPyramidBroken`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchPyramidSuccess`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchRaid`                            | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchRaidCancelled`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchRaidSend`                        | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchRaidStart`                       | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchReSub`                           | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchRewardCreated`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchRewardDeleted`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchRewardRedemption`                | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchRewardRedemptionUpdated`         | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchRewardUpdated`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSevenTVEmoteAdded`               | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSevenTVEmoteRemoved`             | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatAnnouncement`          | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatCommunitySubGift`      | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatGiftPaidUpgrade`       | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatMessageDeleted`        | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatPayItForward`          | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatPrimePaidUpgrade`      | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatRaid`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatResub`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatSessionBegin`          | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatSessionEnd`            | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatSessionUpdate`         | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatSub`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatSubGift`               | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatUserBanned`            | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatUserTimedout`          | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatUserUnbanned`          | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSharedChatUserUntimedout`        | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchShieldModeBegin`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchShieldModeEnd`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchShoutoutCreated`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchShoutoutReceived`                | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchStreamOffline`                   | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchStreamOnline`                    | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchStreamUpdate`                    | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchStreamUpdateGameOnConnect`       | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSub`                             | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSubCounterRollover`              | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSuspiciousUserMessage`           | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchSuspiciousUserUpdate`            | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchUnbanRequestApproved`            | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchUnbanRequestCreated`             | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchUnbanRequestDenied`              | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchUpcomingAd`                      | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchUserBanned`                      | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchUserTimedOut`                    | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchUserUnbanned`                    | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchUserUntimedOut`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchViewerCountUpdate`               | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchVipAdded`                        | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchVipRemoved`                      | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchWarnedUser`                      | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchWarningAcknowledged`             | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchWatchStreak`                     | [No description provided]{.text-muted .text-xs} |
| `EventType.TwitchWhisper`                         | [No description provided]{.text-muted .text-xs} |

### User Global Variable

| Value                                 | Description                                     |
| ------------------------------------- | ----------------------------------------------- |
| `EventType.UserGlobalVariableUpdated` | [No description provided]{.text-muted .text-xs} |

### VoiceMod

| Value                                 | Description                                     |
| ------------------------------------- | ----------------------------------------------- |
| `EventType.VoiceModConnected`         | [No description provided]{.text-muted .text-xs} |
| `EventType.VoiceModDisconnected`      | [No description provided]{.text-muted .text-xs} |
| `EventType.VoiceModSoundboardChanged` | [No description provided]{.text-muted .text-xs} |
| `EventType.VoiceModVoiceLoaded`       | [No description provided]{.text-muted .text-xs} |

### VTube Studio

| Value                                        | Description                                     |
| -------------------------------------------- | ----------------------------------------------- |
| `EventType.VTubeStudioBackgroundChanged`     | [No description provided]{.text-muted .text-xs} |
| `EventType.VTubeStudioConnected`             | [No description provided]{.text-muted .text-xs} |
| `EventType.VTubeStudioDisconnected`          | [No description provided]{.text-muted .text-xs} |
| `EventType.VTubeStudioHotkeyTriggered`       | [No description provided]{.text-muted .text-xs} |
| `EventType.VTubeStudioItemEvent`             | [No description provided]{.text-muted .text-xs} |
| `EventType.VTubeStudioModelAnimation`        | [No description provided]{.text-muted .text-xs} |
| `EventType.VTubeStudioModelClicked`          | [No description provided]{.text-muted .text-xs} |
| `EventType.VTubeStudioModelConfigChanged`    | [No description provided]{.text-muted .text-xs} |
| `EventType.VTubeStudioModelLoaded`           | [No description provided]{.text-muted .text-xs} |
| `EventType.VTubeStudioModelUnloaded`         | [No description provided]{.text-muted .text-xs} |
| `EventType.VTubeStudioTrackingStatusChanged` | [No description provided]{.text-muted .text-xs} |

### Websocket Client

| Value                              | Description                                     |
| ---------------------------------- | ----------------------------------------------- |
| `EventType.WebsocketClientClose`   | [No description provided]{.text-muted .text-xs} |
| `EventType.WebsocketClientMessage` | [No description provided]{.text-muted .text-xs} |
| `EventType.WebsocketClientOpen`    | [No description provided]{.text-muted .text-xs} |

### Websocket Custom Server

| Value                                    | Description                                     |
| ---------------------------------------- | ----------------------------------------------- |
| `EventType.WebsocketCustomServerClose`   | [No description provided]{.text-muted .text-xs} |
| `EventType.WebsocketCustomServerMessage` | [No description provided]{.text-muted .text-xs} |
| `EventType.WebsocketCustomServerOpen`    | [No description provided]{.text-muted .text-xs} |

### YouTube

| Value                                         | Description                                     |
| --------------------------------------------- | ----------------------------------------------- |
| `EventType.YouTubeBetterTTVEmoteAdded`        | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeBetterTTVEmoteRemoved`      | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeBroadcastAdded`             | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeBroadcastEnded`             | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeBroadcastMonitoringEnded`   | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeBroadcastMonitoringStarted` | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeBroadcastRemoved`           | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeBroadcastStarted`           | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeBroadcastUpdated`           | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeFirstWords`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeGiftMembershipReceived`     | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeMemberMileStone`            | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeMembershipGift`             | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeMessage`                    | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeMessageDeleted`             | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeNewSponsor`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeNewSponsorOnlyEnded`        | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeNewSponsorOnlyStarted`      | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeNewSubscriber`              | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubePollClosed`                 | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubePollStarted`                | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubePollUpdated`                | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubePresentViewers`             | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeSevenTVEmoteAdded`          | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeSevenTVEmoteRemoved`        | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeStatisticsUpdated`          | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeSuperChat`                  | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeSuperSticker`               | [No description provided]{.text-muted .text-xs} |
| `EventType.YouTubeUserBanned`                 | [No description provided]{.text-muted .text-xs} |
