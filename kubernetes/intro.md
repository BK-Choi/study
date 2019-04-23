# Kubernetes 소개

- **de facto** container orchestator
- 모든 클라우드 서비스에서 지원
  - Google Kubernetes Engine; GKE in Google Cloud
  - Azure Container Service; AKS
  - Cisco Container Platform; CCP
  - Amazon Elastic Container Service for Kubernetes; Amazon EKS

## History
- 구글이 2014년에 발표 (구글 사내도구인 Borg의 후배)
- CNCF의 1st project
  - CNCF의 목표는 MSA와 관련된 생태계를 지속가능하게 만드는 것
- K8s가 표준이 될 수 있었던 이유
  - 구글 "CNCF 덕분에 경쟁자 사이에서 표준이 될 수 있었다."
  - K8s "사실은 구글 서비스의 검증이 있었기 때문"
    - (Borg 포함) 15년 이상 주당 수십업 개의 컨테이너를 생성한 경험을 반영

## 기능
Orchestration의 끝판왕
- Scaling
  - 수동
  - 자동 : CPU 사용률 기준
- Scheduling
  - 배포 자동화
    - 다양한 배포 방식 지원 : roll-out, canary, blue green
  - 장애복구 등
- Management
  - Docker, containerd, cri-o, rktlet, Kubernetes CRI (Container Runtime Interface) 를 구현한 모든 엔진을 지원
  - Service Discovery
  - L4/L7 routing 설정가능
  - Load Balancing : 비율조정 가능
  - 동일 Pod의 컨테이너끼리 공유하는 Volumn : 컨테이너가 다 사라져야 volume 사라짐
    - local volume spec은 삭제됨
    - 장점? 단점?

기능에 대한 자세한 설명은 Kubernetes.io 문서로 토스

## versus docker swarm
- 단점
  - 쿠베가 더 무겁기 때문에 scaling/deployment가 더 느림
  - 설치, 설정이 더 어려움
- 장점
  - **Production level; 안정적**
  - 커뮤니티 지원

# Conclusion
아직도 안써봤니?

# News
- kNative, Kubeless; K8s X Serverless
  - code만 변경하면 (컨테이너 생성/배포준비, 네트워크 설정 등이 자동으로 처리되어) 바로 배포가능
  - 인프라 엔지니어는 이 자동화를 잘하는 걸로 먹고 살자
- IoT X K8s : High Spec IoT에 대한 배포/관리의 용이성, 그러나 고난예상
- 1.14부터 Windows Server 2019 도 worker nodes로 사용가능; beta 딱지 뗌

# 참고
- [어린이를 위한 쿠베동화](https://www.youtube.com/watch?v=4ht22ReBjno&feature=youtu.be)
- [CNCF linked in(news)](https://www.linkedin.com/company/cloud-native-computing-foundation/)
- [k8s cheatsheet](https://kubernetes.io/ko/docs/reference/kubectl/cheatsheet/?fbclid=IwAR2Z5Thp5Jvs65JfcAcQ7GysF09e3IXaL08D1aHMC7xTG6qvosRMS9PDBcg)
