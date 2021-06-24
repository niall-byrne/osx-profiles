# osx-profiles

### Development:
- [![osx-profiles](https://github.com/niall-byrne/osx-profiles/actions/workflows/push.yml/badge.svg?branch=development)](https://github.com/niall-byrne/osx-profiles/actions/workflows/push.yml)

### Audio_Production:
- [![osx-profiles](https://github.com/niall-byrne/osx-profiles/actions/workflows/push.yml/badge.svg?branch=audio)](https://github.com/niall-byrne/osx-profiles/actions/workflows/push.yml)

## Mac Maker Profile

Personal Mac Maker machine profiles.

Use [Mac Maker](https://github.com/osx-provisioner/mac_maker) to apply this profile to a Mac that is ready to setup.

## Development

This is my main development machine profile.

### Shared Applications
This profile is part of a multi-boot setup, and uses a dedicated partition to hold "Shared Applications", used by all boot partitions.

Before applying the profile:
- create an additional AFPS volume on the system drive
- set the environment variable `SHARED_DISK` to the '/Volumes' mount point of this partition

### Patch Disk
This profile also uses an external drive to symlink Python Poetry virtualenvs and Docker's raw image data to save space for the boot partitions.

Before applying the profile:
- create and mount the external partition
- set the environment variable `PATCH_DISK` to the '/Volumes' mount point of this external partition

### Other Dependencies
See the standard precheck metadata for all other requirements:

Before applying the profile:
- set the appropriate [environment variables](./profile/__precheck__/env.yml)
- review the [release notes](./profile/__precheck__/notes.txt)
