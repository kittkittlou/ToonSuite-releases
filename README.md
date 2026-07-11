# ToonSuite

Two companion apps for playing Toontown Rewritten and Corporate Clash with a whole team of toons at once. This repository hosts the downloads only. The source is private.

| App | What it does | Platforms |
|---|---|---|
| **Tunetoon** | A launcher for all your toons. Save your accounts, and start any set of toons simultaneously. Works with both Toontown Rewritten and Corporate Clash. | Windows and MacOS |
| **Multicontroller** | Control multiple toons simultaneously. | Windows |

## Download

Everything lives on the [**Releases**](../../releases) page. Each app has its own release train, so check the tag prefix:

- **Tunetoon** releases are tagged `tunetoon-v...`
- **Multicontroller** releases are tagged `multicontroller-v...`

Open the newest release for the app you want and grab the file for your system:

| App | Windows file |
|---|---|
| Tunetoon | `Tunetoon.exe` |
| Multicontroller | `Multicontroller.exe` |

There is no installer. Each download is a single self-contained program. Put it in a folder and run it.

## Install and first run

### Windows

1. Download the `.exe` and drop it in a folder of your choice.
   - Keep **Multicontroller.exe** in its own folder. It saves its settings in a file next to the exe.
   - **Tunetoon** stores its data under `%LocalAppData%\Tunetoon`, so you can move or overwrite the exe freely without losing your accounts.
2. On the first run of a new version, Windows SmartScreen may show a blue "Windows protected your PC" box because the app is not code signed. Click **More info**, then **Run anyway**. You only see this once per version.

### macOS (Tunetoon)

macOS builds are being finalized. Once posted, they will appear on the Tunetoon releases as `Tunetoon-macos-arm64.zip` (Apple Silicon) and `Tunetoon-macos-x64.zip` (Intel). To install:

1. Download the zip for your Mac and unzip it.
2. Drag `Tunetoon.app` anywhere you like.
3. On first launch, right-click (or Control-click) the app and choose **Open**, then **Open** again. macOS shows a warning because the app is not notarized with Apple. This happens only the first time.

## Staying up to date

You only need to download from here once. Both apps check for a newer release when they start, and you can also check any time from **About > Check for updates**. Updates download and install in place, then relaunch the app. On macOS the in-app update does not retrigger the first-launch warning.

## Verifying a download

Every release ships a checksum file so you can confirm your download is intact:

- Tunetoon: `SHA256SUMS-tt.txt`
- Multicontroller: `SHA256SUMS-mc.txt`

On Windows PowerShell:

```powershell
Get-FileHash .\Tunetoon.exe -Algorithm SHA256
```

Compare the printed hash against the matching line in the checksum file.
