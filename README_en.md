# NOX
NOX is an Enterprise-grade NVR/VMS system. The free version supports up to 4 channels.

## Requirements
* Ubuntu 24.04 (amd64) or Raspberry Pi 4B/5 (arm64, Debian 13 Trixie)
* RAM 8GiB or higher

## Installation

### KIOSK Mode (NVR type)
This setup is for systems with a directly connected monitor. It requires a GPU for decoding and display purposes. (Raspberry Pi is not recommended due to GPU limitations.)

```bash
curl -fsSL [https://github.com/yiyolcorp/nox-release/releases/latest/download/install.sh](https://github.com/yiyolcorp/nox-release/releases/latest/download/install.sh) \
  | sudo KIOSK_ENABLED=1 bash

```

### Headless Mode (VMS type)
This setup is for systems without a directly connected monitor. It does not require a GPU, except for video analytics features.

```bash
curl -fsSL [https://github.com/yiyolcorp/nox-release/releases/latest/download/install.sh](https://github.com/yiyolcorp/nox-release/releases/latest/download/install.sh) \
  | sudo bash
```

## Limitations
### Free Version
- Live monitoring and recording are available for up to 4 channels.
- Recorded data can be stored for up to 7 days.
- Video analytics features are not provided.
- Any commercial use without prior agreement is strictly prohibited.


## App Download
### Android
**https://play.google.com/store/apps/details?id=com.yiyol.nox.mobile&hl=ko**

### iOS
**https://apps.apple.com/kr/app/nox-mobile/id6744322969**


## Information
- Homepage **https://nox.yiyol.com**
- Youtube **https://www.youtube.com/@YiyolNox**
