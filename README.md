# compile Custom Recovery with Github Actions
```
only Supports TWRP  14 / 12.1 / 11 / 9.0
```
---

## Release Notes
```
= 2024-09-22
- Now Supports TWRP 14


= 2024-09-05
- Include Recovery to tar for Samsung devices
- Include recovery installer zip
- LDCheck for checking missing dependencies.
- TWRP Allow non-Github/Gitlab remotes for device trees
- Clarify options in README
- Increase swap size for kernel inline builds
- Remove common tree input fields (not needed)
- Fix build with Omni manifests
- Update to ubuntu-20.04
- Updated to work with Android 12.1 AOSP minimal TWRP manifest
- Completely reconstruct the use logic to reduce the difficulty of use
- Optimize the parameter transfer part, now you can run multiple Workers at the same time
- TWRP compilation test passed

```

-----

## Output will be like this
![](https://s3.bmp.ovh/imgs/2024/09/07/17b331e17bc4ccd9.png)

## Parameter Description
| Name | Description | Example |
| ------------ | -------------------- | ------------ |
| `MANIFEST_BRANCH` | Source branch | twrp-14 |
| `DEVICE_TREE_URL` | Device tree address | https://github.com/kinguser981/android_device_samsung_a05s.git |
| `DEVICE_TREE_BRANCH` | Device branch that you want to use for build (typically corresponds to the manifest branch) | android-14.0 |
| `DEVICE_PATH` | Device tree location for syncing, relative to workspace root (usually listed as "LOCAL_PATH" or "DEVICE_PATH" in BoardConfig.mk) | device/samsung/a05s |
| `DEVICE_NAME` | Model name (same as twrp_`<DEVICE_NAME>`.mk from device tree) | a05s |
| `DEVICE_MAKEFILE` | Name of device-specific makefile from tree (format: `<PREFIX>_<DEVICE_NAME>`) | twrp_a05s
| `BUILD_TARGET` | Build Target Partition (boot/recovery/vendor_boot) | recovery |
| `RECOVERY_INSTALLER` | Include recovery installer zip | Optional |
| `RECOVERY_TAR` | Recovery to tar for Samsung devices | Optional |

-----

## Usage Instructions

#### 1. Click 'Fork' in the upper right corner of this repo
![](https://s3.bmp.ovh/imgs/2024/09/07/acd37b59bde6971e.png)
#### 2. After waiting for the automatic redirection, you will see your own username
## Building the Recovery
#### 3. Click on 'Actions' then Click no 'TWRP Recovery Builder 2024'
![](https://s3.bmp.ovh/imgs/2024/09/07/4e0db9b997ea3522.png)
#### 4. Click 'Run workflow', choose the branch for the recovery that you want to build, and fill in according to the above 'Parameter Description'
![](https://s3.bmp.ovh/imgs/2024/09/07/29a2d0acf63c6e4f.png)
#### 5. After filling in, click 'Run workflow' to start running

-----

## Compilation results
Can be downloaded at [Release](../../releases)

-----
## Reference and Credits
- https://github.com/that1
- https://github.com/TeamWin
- https://github.com/CaptainThrowback
- https://github.com/cd-Crypton
- https://github.com/azwhikaru
- And to all Contributors in every repositories and scripts I used.

