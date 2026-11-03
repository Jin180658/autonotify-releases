# AutoNotify 0.1.19

Fixes a Windows updater stall where the download finished but the page stayed on **Installing program files**. The update worker now runs independently of the app during installation and restart. Software updates shows a percentage when the download size is known and a moving bar for stages without a percentage. If the worker stops, the page reports the failure and offers the installer download.

## Upgrade from 0.1.18 or earlier

If the old updater stalls, download **AutoNotify-Setup-0.1.19.exe** below and run it once. Users on **0.1.17** can upgrade directly. Use the same Windows account and existing installation folder to retain your records and settings.

## Verification

178 unit tests, 15 database integration tests, a production build and a Windows installer handoff test passed. The repair was installed over an existing 0.1.16 copy, and its customer records, vehicles, admin account and email settings matched the backup afterward. A browser-triggered update from 0.1.19 awaits a later release.

## Installer checksum

SHA-256 for `AutoNotify-Setup-0.1.19.exe` (57,970,471 bytes)

```text
F9606FDAA337D46A30234F690A60386432A5AE53B61007A487C9AA56B41F447F
```
