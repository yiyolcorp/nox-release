# NOX

NOX NVR Free 에디션 배포 저장소. 각 릴리스에는 `install.sh` 와 `nox-nvr_*-free_amd64.deb` 가 포함됩니다.

Free 에디션은 VLM 미지원 · 사용량 제한 · NIS 자동 비활성화 빌드입니다.

## 설치

```bash
curl -fsSL https://github.com/yiyolcorp/nox-release/releases/latest/download/install.sh \
  | sudo EDITION=free bash
```

## 설치 (Local)
```bash
sudo LOCAL_DEB=/path/to/nox-nvr_26.04_amd64.deb bash ./install.sh
```

## 요구사항

- Ubuntu 24.04 (amd64)
- 인터넷 접속 (Docker · Chrome · `.deb` 다운로드용)
- `sudo` 권한
