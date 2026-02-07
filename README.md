# Home Assistant Card for use with YT-DLP

The integration [`yt_dlp_hass`](https://github.com/keywork/yt_dlp_hass) needs to be enabled before using the card.

**Compatible with Home Assistant 2026.2.0+**

![image](https://raw.githubusercontent.com/ybk5053/yt_dlp-card/main/img/downloading.jpg)
*Download info*
![image](https://raw.githubusercontent.com/ybk5053/yt_dlp-card/main/img/waiting.jpg)
*Empty  Card*

## HACS

- Add Custom Repositories

```text
Repository: https://github.com/keywork/yt_dlp-card
Category: Lovelace
```

## Manual Installation

- Download [yt_dlp-card.js](https://github.com/keywork/yt_dlp-card/blob/main/dist/yt_dlp-card.js)
- Copy to www/yt_dlp-card/
- Add the following to your resources

```text
url: /local/yt_dlp-card/yt_dlp-card.js
type: Javascript Module
```

## Adding the Card to the Dashboard

Look for "Custom: Youtube-DLP Card" in the card list.

### Configuration Options
- **header** (optional): Card title text
- **entity**: Must be `yt_dlp.downloader` (default)
- **colour**: Progress bar color (default: #005eff)

## Features
- Real-time download progress display
- Speed and ETA information
- Direct URL input and download trigger
- **Playlist control**: Checkbox to download entire playlists (default: single video only)
- Visual progress bars for multiple concurrent downloads
- Card editor for easy configuration

## Usage
1. Paste a video URL into the input field
2. **Optional**: Check "Download entire playlist" if the URL contains a playlist and you want all videos
3. Click the download arrow button
4. Monitor progress in real-time

**Note**: By default, only the specific video is downloaded, even if the URL contains a playlist. This prevents accidentally downloading hundreds of videos.
