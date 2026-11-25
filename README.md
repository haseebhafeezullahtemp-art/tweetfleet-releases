# TweetFleet

**TweetFleet** is a local desktop app by **Automation Champs** for managing X/Twitter accounts, saving sessions, composing posts with media, and publishing to one or more accounts.

It opens as a normal Windows app window. It does **not** open in Chrome or any browser tab.

## Download

- **Stable** (recommended for everyone): `https://github.com/haseebhafeezullahtemp-art/tweetfleet-releases/releases/latest`
- **Beta** (early test builds): `https://github.com/haseebhafeezullahtemp-art/tweetfleet-releases/releases` and choose the build marked **Pre-release**

Always download from the links above. Do not trust copies from other sites.

## Install

1. Download **TweetFleet Setup x.x.x.exe**.
2. Double-click it.
3. Windows may show a SmartScreen warning because the app is not code-signed yet.
   - Click **More info**, then **Run anyway**.
4. The installer installs TweetFleet for your Windows user only. Administrator rights are not needed.
5. A **TweetFleet** shortcut appears on your Desktop and in the Start Menu.

## Open the app

Double-click the **TweetFleet** shortcut.

The app opens its own window. You will not see a browser address bar. A hidden local service runs inside the app so TweetFleet can do its work; you do not need to manage it.

## First setup

1. Open **Settings**.
2. Add your Gemini API key if you want AI-generated captions. Leave it blank if you will write captions yourself.
3. Click **Add** in the Accounts panel.
4. Enter a name and optional handle.
5. Paste cookies JSON, or choose a `.json` cookie file.
6. Optionally set a media folder path.
7. Click **Save account**.

TweetFleet injects the cookies into a private Chromium session, opens X, verifies the login, and saves the session on your PC.

If X does not accept the cookies, the account card shows **Re-login**. Click it, sign in in the window that opens, then click **Save cookies**.

## Publish a post

1. Tick one or more accounts in the left **Accounts** panel.
2. Write the caption in the **Caption** box, or generate it with Gemini.
3. Add media by dropping files into the media area, browsing, or using the account’s folder.
4. Set **Repeat** (1–10) and **Delay** in seconds (minimum 15).
5. Click **Publish now**.

The automation browser is hidden during normal posting. It appears only when a login or bot check needs your attention. The tab stays open until the whole run finishes.

> Posting the same text many times or to many accounts can look like spam to X. Use a sensible repeat count and delay.

## Updates

TweetFleet checks for updates when it starts and every 6 hours while it is open.

When an update is available, you will see an **Update** button in the top bar. Click it to read the release notes and install.

### Update channels

Open **Settings → Update channel**:

- **Stable** — recommended for everyone.
- **Beta** — early builds for testing before everyone gets them.

### Your data is safe

Updates replace only the app files. They never include or replace:

- accounts
- cookies/sessions
- settings
- media uploads
- activity history

Your data is stored in:

```text
%LOCALAPPDATA%\TweetFleet\data
```

You can open this folder from **Settings → Open data folder**.

Before installing an update, TweetFleet copies your accounts, cookies, settings, and activity history into a timestamped folder under `backups` inside your data folder. Uploaded media files are left where they are and are not replaced.

## Uninstall

If you uninstall TweetFleet, choose **Keep my data** if you plan to reinstall later. The uninstaller is set to keep data by default.

## Privacy

- Cookies and sessions stay on your PC.
- TweetFleet does not send cookie values to GitHub or anywhere else.
- The update check only asks GitHub: “What is the newest version?”
- Use only accounts you own or manage with permission.

## Troubleshooting

### Windows says “Windows protected your PC”

This app is not code-signed yet. Click **More info → Run anyway**. A code-signed build can be added later.

### An account stops working

Open the app, find the account card, and click **Re-login**. Sign in, then click **Save cookies**.

### I cannot find my data

Open **Settings → Open data folder**, or paste this into File Explorer:

```text
%LOCALAPPDATA%\TweetFleet\data
```

---

Made by **Automation Champs**.
