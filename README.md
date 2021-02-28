# SHRP Device configuration for Xiaomi Redmi 8A Pro/Dual (olivewood)

The Redmi 8a Pro/Dual (codenamed _"olivewood"_) is a smartphone from Xiaomi.
It was released in April 2020.

<p align="center">
  <a href="#compile">⚙️ Compile</a> •
  <a href="#test">💡 Test</a> •
  <a href="#specification">📱 Specification</a> •
</p>

![r8ap](https://raw.githubusercontent.com/askanakmala/template_me/main/r8ap.jpg "r8ap")

## Download Release

[SHRP_v2.3.2_olivewood🚀](https://github.com/askanakmala/device_xiaomi_olivewood-SHRP/releases/download/v2.3.2/SHRP_v2.3.2_olivewood-201727122020.zip)

## Compile

First sync SHRP manifest:
```
repo init -u git://github.com/SKYHAWK-Recovery-Project/platform_manifest_twrp_omni.git -b android-9.0
```

Then add these projects to .repo/local_manifests/roomservice.xml (If you don't have it, you can add in .repo/manifest.xml)
```xml
<project name="askanakmala/device_xiaomi_olivewood-SHRP" path="device/xiaomi/olivewood" remote="github" revision="android_9.0-Q" />
```

Now you can sync your source:

```
repo sync
```

Finally execute these:

```
. build/envsetup.sh
export ALLOW_MISSING_DEPENDENCIES=true
export LC_ALL=C
lunch omni_olivewood-eng 
mka recoveryimage
```
## Test

To test it:

```
fastboot boot out/target/product/olivewood/recovery.img
```
## Specification
Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Octa-core (4x1.95 GHz Cortex-A53 & 4x1.45 GHz Cortex A53)
CHIPSET | Qualcomm SDM439 Snapdragon 439 (12 nm)
GPU     | Adreno 505
Memory  | 2/3 GB
Shipped Android Version | 9.0 update to 10.0
Storage | 32 GB
MicroSD | Up to 512 GB
Battery | 5000 mAh (non-removable)
Display | 720 x 1520 pixels, 19:9 ratio (~270 ppi density)
Rear Camera  | 13 MP, f/2.2, (wide), 1/3.1", 1.12µm, PDAF
Rear Depth Sensor  | 2 MP, f/2.4, (depth)
Front Camera | 8 MP, f/2.0, 1/4", 1.12µm
Release Date | 02 April 2020
