[🇰🇷 한국어](README.md) | [🇺🇸 English](README_en.md)
# NOX
NOX는 Enterprise 급 NVR/VMS 시스템입니다. 무료 버전은 최대 4채널을 지원합니다.

## 요구사항
- Ubuntu 24.04 (amd64) or Raspberry Pi 4B/5 (arm64, Debian 13 Trixie)
- RAM 8GiB 이상

## 설치

### KIOSK 모드 (NVR형태)
모니터가 직접 연결되는 시스템으로 디코딩 및 디스플레이용도로 GPU가 필요합니다.
```bash
curl -fsSL https://github.com/yiyolcorp/nox-release/releases/latest/download/install.sh \
  | sudo KIOSK_ENABLED=1 bash
```

### Headless 모드 (VMS형태)
모니터기 직접 연결되지 않는 시스템으로 분석기능 외에는 GPU를 필요로 하지 않습니다.
```bash
curl -fsSL https://github.com/yiyolcorp/nox-release/releases/latest/download/install.sh \
  | sudo bash
```

## 제한사항
### 무료 버전
- 최대 4채널의 라이브 모니터링과 녹화가 가능합니다
- 녹화 데이터는 최대 7일까지 보관 가능합니다.
- 분석은 제공되지 않습니다.
- 사전에 협의되지 않은 어떠한 상업적 이용도 허용되지 않습니다.


## 앱 다운로드
### Android
**https://play.google.com/store/apps/details?id=com.yiyol.nox.mobile&hl=ko**

### iOS
**https://apps.apple.com/kr/app/nox-mobile/id6744322969**


## 정보
- 홈페이지 **https://nox.yiyol.com**
- Youtube **https://www.youtube.com/@YiyolNox**
