# NOX

NOX NVR Free 에디션 배포 저장소. 각 릴리스에는 `install.sh` 와 `nox-nvr_*-free_amd64.deb` 가 포함됩니다.

Free 에디션은 VLM 미지원 · 사용량 제한 · NIS 자동 비활성화 빌드입니다.

## 설치

```bash
curl -fsSL https://github.com/yiyolcorp/nox-release/releases/latest/download/install.sh \
  | sudo EDITION=free bash
```

> `sudo` **뒤**, `bash` **앞**에 `EDITION=free` 를 둬야 환경변수로 전달됩니다.
> (예: `sudo bash EDITION=free` 는 동작하지 않습니다.)

## 고급 사용법

### 특정 버전 설치

```bash
curl -fsSL https://github.com/yiyolcorp/nox-release/releases/latest/download/install.sh \
  | sudo EDITION=free VERSION=26.04 bash
```

### 스크립트를 먼저 내려받고 실행

파이프 실행이 꺼려지는 환경이라면 스크립트를 먼저 저장해 검토한 뒤 실행할 수 있습니다.

```bash
curl -fsSL -o install.sh \
  https://github.com/yiyolcorp/nox-release/releases/latest/download/install.sh
chmod +x install.sh
sudo EDITION=free ./install.sh
```

## 설치 과정에서 수행되는 작업

`install.sh` 는 다음을 순서대로 실행합니다.

1. 환경 검증 (root 권한, amd64 아키텍처, `EDITION=free`)
2. `curl` 설치 (없을 때만)
3. Docker 설치 — `https://get.docker.com` 스크립트 사용 (없을 때만)
4. Google Chrome 설치 — `dl.google.com` 공식 `.deb` (없을 때만)
5. 릴리스 태그 조회 및 `nox-nvr_{VERSION}-free_amd64.deb` 다운로드
6. `apt install -y` 로 `.deb` 설치

## 환경변수

| 변수 | 기본값 | 설명 |
|------|--------|------|
| `EDITION` | — | Free 에디션 설치 시 **반드시 `free` 로 지정**. |
| `VERSION` | `latest` | 설치할 버전 태그. `latest` 지정 시 GitHub API로 자동 조회. |
| `REPO`    | `yiyolcorp/nox-release` | 릴리스 저장소. |

## 요구사항

- Ubuntu 22.04 / 24.04 (amd64)
- 인터넷 접속 (Docker · Chrome · `.deb` 다운로드용)
- `sudo` 권한

## 설치 후 확인

```bash
systemctl status nox
journalctl -u nox -f
docker compose -f /opt/nox/current/docker-compose.yml logs -f
```
