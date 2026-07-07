# Home Assistant Blueprints

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
- Duplicate/replay suppression with cooldown

## Requirements

- Home Assistant
- UniFi Protect integration
- Sonos integration
- Google Translate TTS configured in Home Assistant

## Import into Home Assistant

In Home Assistant:

1. Go to **Settings -> Automations & scenes -> Blueprints**
2. Click **Import Blueprint**
3. Paste the GitHub file URL or raw GitHub URL for the blueprint you want

## Suggested repo structure

```text
home-assistant-blueprints/
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

## Publishing on GitHub

1. Create a new public repository
2. Upload the files from this folder
3. Commit to `main`
4. Copy either the GitHub file URL or the raw file URL for each blueprint
5. Import that URL into Home Assistant

## Raw URL examples

Replace `YOUR_USERNAME` with your GitHub username:

```text
https://raw.githubusercontent.com/YOUR_USERNAME/home-assistant-blueprints/main/automation/sonos-doorbell/unifi_doorbell_sonos_google_announce_sync.yaml
https://raw.githubusercontent.com/YOUR_USERNAME/home-assistant-blueprints/main/automation/sonos-doorbell/unifi_doorbell_sonos_google_announce_per_speaker.yaml
```

## Screenshots

Add screenshots here later if you want:
- Blueprint import screen
- Sync blueprint configuration
- Per-speaker blueprint configuration

## License

This repository uses the MIT License.
