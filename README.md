# Meow Universal Recovery Project
Main repository for the manifest files used to get the Meow Universal Recovery Project sources.

> [!NOTE]
> Make sure you have enough space to store MURP source code.

## Getting Started

> [!CAUTION]
> Not ready for building, bugs may occur.

First, create new folder and cd to it:<br>
`mkdir MURP && cd MURP`<br>

Then, sync source code:<br>
`repo init --depth=1 -u https://github.com/Meow-Universal-Recovery-Project/manifest.git -b main`<br>
`repo sync -jX`<br>

Clone your devie-specific repositories and start building:<br>
`export ALLOW_MISSING_DEPENDENCIES=true`<br>
`export FOX_BUILD_DEVICE=<device>`<br>
`export LC_ALL="C"`<br>
`source build/envsetup.sh`<br>

for the 11.0 (or higher) branch, if the device has a separate recovery partition<br>
`lunch twrp_<device>-eng && mka adbd recoveryimage`<br>

for the 11.0 (or higher) branch, with A/B partitioning, and no separate recovery partition<br>
`lunch twrp_<device>-eng && mka adbd bootimage`<br>

for the 12.1 (or higher) branch, vendor_boot-as-recovery builds [this is highly experimental and unsupported!]<br>
`lunch twrp_<device>-eng && mka adbd vendorbootimage`<br>
