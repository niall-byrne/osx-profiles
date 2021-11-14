# osx-profiles

### Audio Overlay:
- [![osx-profiles](https://github.com/niall-byrne/osx-profiles/actions/workflows/push.yml/badge.svg?branch=audio_overlay)](https://github.com/niall-byrne/osx-profiles/actions/workflows/push.yml)

## Mac Maker Profile

Audio Overlay Mac Maker machine profile.

Use [Mac Maker](https://github.com/osx-provisioner/mac_maker) to apply this profile to a Mac that is ready to setup.

## Audio Overlay

This branch contains a profile to add music production tools to an existing [development profile](https://github.com/niall-byrne/osx-profiles/tree/development) install.

### Audio Partition
This profile can co-exist with a [development profile](https://github.com/niall-byrne/osx-profiles/tree/development) install, as it segregates the audio content, both in terms of application and media.

The audio partition is a specified disk that will contain project work, samples, patches, and all application data for the installed DAW software.

Before applying the profile:
- create an additional APFS volume to house the audio partition
- set the environment variable `AUDIO_PARTITION` to the '/Volume' mount point of this partition

### Other Dependencies
See the standard precheck metadata for all other requirements:

Before applying the profile:
- set the appropriate [environment variables](./profile/__precheck__/env.yml)
- review the [release notes](./profile/__precheck__/notes.txt)_
