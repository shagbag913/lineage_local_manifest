# LineageOS fork local manifest

## Why does this exist?
I'm just having fun and messing around. I really enjoy LineageOS, but I just wanted the ability to mess around in source, without having the overhead of bringing up common custom ROM stuff (inline kernel building, APNs, etc).

## Main differences from LineageOS
- Includes Google Pixel alarm, ringtone, notification, and UI sounds
- Google Sans font family used in some areas
- Quick settings vibration when tapping tile
- Minor performance improvements (disabled debugging in some areas)
- Lawnchair launcher included as default launcher
- Slimmed down the power menu

## Updates
Lineage's upstream changes are *never* merged into my forks. Instead, I rebase my commits on top of Lineage's. This means force pushes happen pretty much every time Lineage pushes commits to the affected project.

## Syncing
First, initialize LineageOS manifest:
```
repo init -u https://github.com/LineageOS/android/ -b lineage-17.0
```

Then, add my local manifest (run this from top of Lineage source):
```
curl --create-dirs -o .repo/local_manifests/lineage_fork.xml https://raw.githubusercontent.com/shagbag913/lineage_local_manifest/lineage-17.0/lineage_fork.xml
```

Now, you can sync normally:
```
repo sync
```

## Device support
If your device has official LineageOS 16.0 trees available, you can use them here without any changes. This will always remain as an unofficial LineageOS - not something else (in other words, I'm not rebranding).
