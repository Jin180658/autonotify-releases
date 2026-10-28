# AutoNotify — Windows Downloads

AutoNotify manages customers, vehicles, policy paperwork and automatic **email** renewal reminders on your own laptop. The interface supports **English and 简体中文**.

**[Download the latest installer](https://github.com/Jin180658/autonotify-releases/releases/latest)**

This public repository contains installers, instructions and the update feed only. Application source code, customer records, credentials and database backups are not included.

## Install

1. Use a **64-bit Windows PC** and open the download link above.
2. Under **Assets**, download `AutoNotify-Setup-0.1.16.exe`. The source-code ZIP and TAR files are not the application.
3. Run the installer and choose an installation folder.
4. Keep both recommended options selected:
   - **Start AutoNotify when I sign in to Windows** — starts the local app after Windows sign-in.
   - **Run the renewal reminder check every day at 9:00 AM** — checks due reminders automatically, including eligible catch-up checks after a later Windows sign-in.
5. Open **AutoNotify** from the Desktop or Start Menu. Its shortcut starts the app and opens your default browser.

Node.js and PostgreSQL are bundled. You do not need to install development tools, run terminal commands, buy a domain or arrange cloud hosting.

## First-time setup

1. Choose English or 简体中文 using **Language / 语言** on the setup screen.
2. Enter your Gmail / Google Workspace address and create an AutoNotify password.
3. Enable Google 2-Step Verification and create a [Google App Password](https://myaccount.google.com/apppasswords). Enter that App Password in AutoNotify, **not your normal Google password**. Availability depends on your Google account's security policy.
4. Enter an optional sender name and request the verification email. Enter its code to create the administrator account. Check Spam if necessary.
5. Use **Settings → Email delivery → Send an email test** to confirm your sending configuration. Then add your customers, vehicles and expiry dates.

There is one administrator account per installation. Password recovery uses your verified recovery email; an optional offline backup recovery code is also available. Do not share passwords, App Passwords or verification codes.

The interface language can be changed later in **Settings → Language / 语言**. It is saved in that browser; outgoing reminder emails and CSV exports are not translated by this preference.

## Everyday use

- **Dashboard:** upcoming work, reminder operation status and CSV export.
- **Customers:** customer details, internal remarks, multiple vehicles and All vehicles view.
- **Renewals:** independent policy dates and focused renewal updates.
- **Email History:** attempted reminders and provider acceptance/failure details. Accepted does not guarantee inbox delivery.
- **Settings:** language, account/recovery, email delivery, insurance providers, encrypted backups and software updates.

## Automatic email reminders

Road Tax, Insurance, VEP and P.A. dates are checked independently at **30, 14 and 3 days before expiry, and on expiry day**. Due items for one vehicle can be combined into one email. Paused vehicle reminders do not send.

Keep the laptop **on, signed into Windows and connected to the internet** for sending. With the recommended tasks enabled, checks run at 9:00 AM and after Windows sign-in later than 9:00 AM. Missed 30/14/3-day reminders may be caught up once within seven days; expiry-day reminders are not sent after that policy has expired. Successful sends are deduplicated for the same policy date and reminder window. App password sign-in alone is not the Windows task trigger.

After a customer renews, update the relevant policy's expiry date in AutoNotify. Review Dashboard reminder status and Email History rather than assuming a message has reached the inbox. **SMS and WhatsApp are not supported.**

## Your data and backups

Each Windows user installation has its own local database at:

```text
%LOCALAPPDATA%\AutoNotify\data
```

Separate laptops do not automatically share records. Customer records remain local; sending email sends the recipient address and message through your configured email service. Updates and normal uninstallation retain the separate data folder and account.

Use **Settings → Backup & Restore** to create password-encrypted backups. Keep the backup password safe and copy backups outside the laptop. CSV is a report, not a full restorable backup. Restoring a full backup signs out sessions and pauses restored reminders until their policy dates are reviewed.

## Updates

Open **Settings → Software updates**. A newer published version can be downloaded, verified and installed through AutoNotify; no update is offered for an equal or older version. Keep the laptop on until the app confirms the new version. Normal updates retain your local account, records and email settings.

Older versions can also be upgraded by downloading the latest installer and running it under the **same Windows account**. Back up your data before upgrading. Do not uninstall or delete the data folder to perform a normal update.

## 简体中文快速开始

1. 点击页面顶部的下载链接，在 **Assets** 中下载 `.exe` 安装程序并运行，保留两个建议勾选的自动运行选项。
2. 从桌面或开始菜单打开 AutoNotify，在 **Language / 语言** 中选择简体中文。
3. 使用自己的 Gmail 地址、AutoNotify 登录密码和 Google 应用专用密码完成邮箱验证；不要填写 Google 账号的普通密码。
4. 在 **设置 → 邮件发送** 中测试邮件，再添加客户、车辆及到期日期。
5. 发送提醒时电脑需要开机、登录 Windows 并联网。定期在 **设置 → 备份与恢复** 中备份，并将备份复制到其他设备。

## Release status

Version **0.1.16** passed local automated tests, production browser checks and an upgrade of the existing installation. A fresh second-PC installation, reboot trial and update from an older public release still need real-user acceptance testing. Start with one trial laptop before relying on it across your business.

If startup fails, retain your data folder and check its `logs` directory. When reporting a problem, include the app version and error text, and remove private customer or credential details from screenshots.
