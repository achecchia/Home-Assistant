# Home-Assistant

Reusable Home Assistant blueprints for UniFi Protect doorbells, Sonos, and Google TTS.

## Included blueprints

### UniFi Doorbell -> Sonos Google Announcement (Sync)
Best option for multi-room sync. Sends one announcement call to all selected Sonos players with one shared volume.

File:
- `automation/sonos-doorbell/unifi_doorbell_sonos_google_announce_sync.yaml`

### UniFi Doorbell -> Sonos Google Announcement (Per Speaker Volume)
Lets you assign a different announcement volume to each Sonos player. This can be slightly less synchronized because Home Assistant sends the announcement one speaker at a time.

File:
- `automation/sonos-doorbell/unifi_doorbell_sonos_google_announce_per_speaker.yaml`

## Features

- Real UniFi Protect doorbell ring detection
- Sonos `announce: true` playback
- Google TTS media source support
- Shared-volume sync blueprint
- Per-speaker volume blueprint
- Duplicate or replay suppression with cooldown

## Requirements

- Home Assistant
- UniFi Protect integration
- Sonos integration
- Google Translate TTS configured in Home Assistant

## Import into Home Assistant

In Home Assistant:

1. Go to **Settings -> Automations & scenes -> Blueprints**
2. Click **Import Blueprint**
3. Paste one of the raw GitHub URLs below

### Raw import URLs

```text
https://raw.githubusercontent.com/achecchia/Home-Assistant/main/automation/sonos-doorbell/unifi_doorbell_sonos_google_announce_sync.yaml
https://raw.githubusercontent.com/achecchia/Home-Assistant/main/automation/sonos-doorbell/unifi_doorbell_sonos_google_announce_per_speaker.yaml
```

## Repo structure

```text
Home-Assistant/
├── .gitignore
├── LICENSE
├── README.md
└── automation/
    └── sonos-doorbell/
        ├── unifi_doorbell_sonos_google_announce_sync.yaml
        └── unifi_doorbell_sonos_google_announce_per_speaker.yaml
```

## Recommended usage

- Use the **Sync** blueprint by default
- Use the **Per Speaker Volume** blueprint only when a site needs different room volumes
- After creating an automation from a blueprint, use Home Assistant's automation editor to test actions

## License

This repository uses the MIT License.
