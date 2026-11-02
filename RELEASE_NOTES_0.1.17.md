# AutoNotify 0.1.17 — Windows startup repair

Fixes the startup path behind the reported error **"Execution of PostgreSQL by a user with administrative permissions is not permitted."** Earlier versions started the database directly and could inherit administrator privileges from Windows.

## Changes

- Start PostgreSQL through its bundled `pg_ctl` restricted-privilege launcher. The database does not run as administrator.
- Wait for the selected database cluster to be ready and check startup failures, including Windows PowerShell 5.1 process exit handling.
- Show the real user-data log directory rather than a misleading installation-folder path.
- Keep existing accounts, records, email settings and reminder behavior. No database migration or reset is added.

## Install or upgrade

Download **AutoNotify-Setup-0.1.17.exe** below and run it normally under the **same Windows account**, using the existing installation folder. Keep both recommended startup/reminder options checked. You do not need to uninstall, delete your data folder, change account type or disable UAC.

If the old copy cannot start, download the installer here directly; the in-app updater requires a running app. Working older copies can use **Settings → Software updates**. Back up data before upgrading where the old copy is accessible.

New users can follow the [installation and Gmail setup guide](https://github.com/Jin180658/autonotify-releases#install). English and 简体中文 interface support and the features from 0.1.16 are included.

## Verification

155 unit tests, 15 PostgreSQL integration tests, lint, translation audit, production build and script parsing passed. Disposable Windows tests verified actual launcher cold-start, spaced paths, loopback binding, repeated launches, restart/data preservation, scoped shutdown, and deliberate database startup failures reporting correct logs.

The development machine runs a non-elevated token, so the original affected user's elevated Windows configuration still requires confirmation on that PC. Fresh second-PC/reboot and public in-app update acceptance remain pending.

If startup fails, send the latest `initialization.log`, `postgres.log` and `postgres-control-error.log` from `%LOCALAPPDATA%\AutoNotify\data\logs`. Do not send environment files or passwords.

## Installer checksum

SHA-256 (`AutoNotify-Setup-0.1.17.exe`, 57,968,754 bytes):

```text
CBF76D80C62F1ECB43319AA75D6553C1D5D538F17AF24FEA2287C5A78C4F213D
```
