<p align="center">
    <img src="https://i.imgur.com/coW0xko.jpg" />
</p>

Get started
-----------

Before trying to build the ROM yourself, make sure you have established your building environment.

# Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```
For more info on how to do exactly that, check [AOSP's official documentation](https://source.android.com/setup/build/initializing).

Downloading the source
----------------------

You can download the source by simply doing:
```bash

$ repo init -u https://github.com/simplixone/manifest -b o9x
$ repo sync --no-tags --no-clone-bundle --force-sync -c
```
    
On multithread CPUs (which you probably have, considering you would like to build Android :P) you can set multiple sync jobs by doing:
```bash

    repo sync --no-tags --no-clone-bundle --force-sync -c -jX
```

where X is the count of your CPU threads.

Building the ROM
----------------

Simplix One build commands are the standard one from AOSP:

```bash

$ . build/envsetup.sh

$ lunch aosp_$device-userdebug

$ mka bacon -jX
```
    
Credits
-------
 * [**Pixel Experience**](https://github.com/PixelExperience)
 * [**Lineage OS**](https://github.com/LineageOS)
 
 
