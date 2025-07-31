---
title: VPN 사용법 - macOS
weight: 4
---

이 문서는 macOS에서 VIPLab VPN을 사용하는 방법을 안내합니다.

## 주의사항

macOS에서는 App Store에서 제공하는 GUI 애플리케이션이 아닌, CLI 애플리케이션을 사용해야 합니다.

## WireGuard 설치

Homebrew를 사용하여 아래 명령어를 통해 WireGuard를 설치할 수 있습니다.
```plain
brew install wireguard-tools
```

## 구성파일 배치

NAS에서 다운로드 받은 설정 파일을 `/etc/wireguard` 디렉토리에 배치하는 것을 추천드립니다.
```plain
sudo mkdir /etc/wireguard
sudo mv VIPLab-VPN-M.conf /etc/wireguard
sudo mv VIPLab-VPN-MALL.conf /etc/wireguard
```

## 실행 방법

아래 명령어를 사용하여 VPN을 연결할 수 있습니다:
```plain
sudo wg-quick up VIPLab-VPN-M
```

연결 종료시에는 아래 명령어를 사용합니다:
```plain
sudo wg-quick down VIPLab-VPN-M
```

아래 명령어를 통해 현재 VPN 상태를 확인할 수 있습니다:
```plain
sudo wg show
```