---
title: VPN 개요
weight: 2

resources:
    - name: I1
      src: "image1.png"
      title: VPN 설정 파일 위치
    - name: I2
      src: "image2.png"
      title: VPN Configuration 디렉토리 내부 구성
---

VIPLab은 연구실 내부망과 인천대학교 교내망 접속을 위해, WireGuard를 이용한 VPN 서비스를 제공합니다.

## VPN 설정 파일 확인 방법

{{< img name="I1" size="large" lazy=false >}}

각 학생 계정 NAS의 VPN Configurations 디렉토리 내에서 VPN 설정 파일을 확인하실 수 있습니다.

## VPN Configuration 파일 구성

{{< img name="I2" size="large" lazy=false >}}

총 4개의 .conf 파일이 제공되며 각 설정의 용도는 아래와 같습니다:

- **VIPLab-VPN.conf**: Windows, Android 환경에서 연구실 또는 교내 통신을 위해 사용
- **VIPLab-VPN-ALL.conf**: Windows, Android 환경에서 모든 트래픽 VPN 이용을 위해 사용
- **VIPLab-VPN-M.conf**: macOS 환경에서 연구실 또는 교내 통신을 위해 사용
- **VIPLab-VPN-MALL.conf**: macOS 환경에서 모든 트래픽 VPN 이용을 위해 사용

교내 서버는 labserver.local 도메인을 이용해 접속하실 수 있으며, 교육 기관 IP 인증이 필요하실 경우에만 ALL 또는 MALL 설정을 이용하시는 것을 추천드립니다.

> **안내**: ALL 또는 MALL 설정의 경우 모든 트래픽을 교내 VPN 서버를 경유하기 때문에 교외에서 교내에서만 접속 가능한 인터넷 서비스 등을 이용 가능합니다. (예: dbpia, 해외 특정 저널 등) 
