## Governance & Audit > Resource Watcher > 리소스 유형 목록

* 서비스 리소스 유형 및 관련된 이벤트 목록입니다.
* 이벤트 유형
  * 리소스 생성: 리소스 생성 시 발생하는 이벤트
  * 리소스 수정: 리소스 수정 시 발생하는 이벤트
  * 리소스 삭제: 리소스 삭제 시 발생하는 이벤트
  * -: 리소스 생성/수정/삭제와 관련 없는 이벤트


### Secure Key Manager

#### 키 저장소 (SecureKeyManager:KeyStore)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.skm.keystore.create|키 저장소 생성|리소스 생성|
|event_id.skm.keystore.delete|키 저장소 삭제|리소스 삭제|
|event_id.skm.keystore.update|키 저장소 정보 변경|리소스 수정|
|event_id.skm.secret.create|기밀 데이터 생성|-|
|event_id.skm.secret.delete|기밀 데이터 즉시 삭제|-|
|event_id.skm.symmetric.create|대칭 키 생성|-|
|event_id.skm.symmetric.delete|대칭 키 즉시 삭제|-|
|event_id.skm.asymmetric.create|비대칭 키 생성|-|
|event_id.skm.asymmetric.delete|비대칭 키 즉시 삭제|-|
|event_id.skm.api.secrets.get|기밀 데이터 조회|-|
|event_id.skm.api.symmetric.encrypt|대칭 키를 통한 암호화|-|
|event_id.skm.api.symmetric.decrypt|대칭 키를 통한 복호화|-|
|event_id.skm.api.symmetric.create_local_key|로컬 키 생성|-|
|event_id.skm.api.symmetric.get|대칭 키 조회|-|
|event_id.skm.api.asymmetric.sign|비대칭 키를 통한 서명|-|
|event_id.skm.api.asymmetric.verify|비대칭 키를 통한 서명 검증|-|
|event_id.skm.api.asymmetric.get.privateKey|개인 키 조회|-|
|event_id.skm.api.asymmetric.get.publicKey|공개 키 조회|-|
|event_id.skm.api.secrets.create|기밀 데이터 생성|-|
|event_id.skm.api.symmetric.create|대칭 키 생성|-|
|event_id.skm.api.asymmetric.create|비대칭 키 생성|-|
|event_id.skm.api.secrets.delete|기밀 데이터 즉시 삭제|-|
|event_id.skm.api.symmetric.delete|대칭 키 즉시 삭제|-|
|event_id.skm.api.asymmetric.delete|비대칭 키 즉시 삭제|-|
|event_id.skm.secrets.scheduled_delete|기밀 데이터 자동 삭제|-|
|event_id.skm.symmetric.scheduled_delete|대칭 키 자동 삭제|-|
|event_id.skm.asymmetric.scheduled_delete|비대칭 키 자동 삭제|-|


### NHN Container Registry(NCR)

#### 컨테이너 레지스트리 (NHNContainerRegistry:ContainerRegistry)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.ncr.registry.create|레지스트리 생성|리소스 생성|
|event_id.ncr.registry.delete|레지스트리 삭제|리소스 삭제|
|event_id.ncr.registry.update|레지스트리 변경|-|
|event_id.ncr.immutable_tag_rule.create|이미지 보호 정책 추가|-|
|event_id.ncr.immutable_tag_rule.delete|이미지 보호 정책 삭제|-|
|event_id.ncr.immutable_tag_rule.update|이미지 보호 정책 변경|-|
|event_id.ncr.retention_rule.create|이미지 정리 정책 추가|-|
|event_id.ncr.retention_rule.delete|이미지 정리 정책 삭제|-|
|event_id.ncr.retention_rule.execute|이미지 정리 정책 실행|-|
|event_id.ncr.retention_rule.update|이미지 정리 정책 변경|-|
|event_id.ncr.webhook.create|웹훅 생성|-|
|event_id.ncr.webhook.delete|웹훅 삭제|-|
|event_id.ncr.webhook.update|웹훅 수정|-|


### EasyCache

#### 노드 인스턴스 (EasyCache:NodeInstance)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.easycache.node.create|노드 추가|리소스 생성|
|event_id.easycache.node.update||리소스 수정|
|event_id.easycache.node.delete|노드 삭제|리소스 삭제|


### 기본 인프라 서비스

#### 클러스터 (CLUSTER)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.cluster.auto_healing.detected|오토힐링 탐지|-|
|event_id.iaas.cluster.k8s_api_not_working.detected|K8S APISERVER 문제 탐지|-|
|event_id.iaas.cluster.k8s_api_not_working.resolved|K8S APISERVER 문제 해결|-|
|event_id.iaas.cluster.all_nodes_not_ready.detected|모든 노드 정지 문제 탐지|-|
|event_id.iaas.cluster.all_nodes_not_ready.resolved|모든 노드 정지 문제 해결|-|
|event_id.iaas.cluster.create.start|클러스터 생성 시작|리소스 생성|
|event_id.iaas.cluster.create.end|클러스터 생성 완료|-|
|event_id.iaas.cluster.create.failed|클러스터 생성 실패|리소스 삭제|
|event_id.iaas.cluster.delete.start|클러스터 삭제 시작|-|
|event_id.iaas.cluster.delete.end|클러스터 삭제 완료|리소스 삭제|
|event_id.iaas.cluster.delete.failed|클러스터 삭제 실패|-|
|event_id.iaas.cluster.suspend.start||-|
|event_id.iaas.cluster.suspend.end||-|
|event_id.iaas.cluster.suspend.failed||-|
|event_id.iaas.cluster.resume.start|클러스터 동작 가능 전환 시작|-|
|event_id.iaas.cluster.resume.end|클러스터 동작 가능 전환 완료|-|
|event_id.iaas.cluster.resume.failed|클러스터 동작 가능 전환 실패|-|
|event_id.iaas.cluster.handover.start|클러스터 OWNER 변경 시작|-|
|event_id.iaas.cluster.handover.end|클러스터 OWNER 변경 완료|-|
|event_id.iaas.cluster.handover.failed|클러스터 OWNER 변경 실패|-|
|event_id.iaas.cluster.resize.start|클러스터 크기 조정 시작|-|
|event_id.iaas.cluster.resize.end|클러스터 크기 조정 완료|-|
|event_id.iaas.cluster.resize.failed|클러스터 크기 조정 실패|-|
|event_id.iaas.cluster.cni_update.start|CNI 변경 시작|-|
|event_id.iaas.cluster.cni_update.end|CNI 변경 완료|-|
|event_id.iaas.cluster.cni_update.failed|CNI 변경 실패|-|
|event_id.iaas.nodegroup.create.start|노드 그룹 생성 시작|-|
|event_id.iaas.nodegroup.create.end|노드 그룹 생성 완료|-|
|event_id.iaas.nodegroup.create.failed|노드 그룹 생성 실패|-|
|event_id.iaas.nodegroup.delete.start|노드 그룹 삭제 시작|-|
|event_id.iaas.nodegroup.delete.end|노드 그룹 삭제 완료|-|
|event_id.iaas.nodegroup.delete.failed|노드 그룹 삭제 실패|-|
|event_id.iaas.nodegroup.update_flavor.start|인스턴스 타입 변경 시작|-|
|event_id.iaas.nodegroup.update_flavor.end|인스턴스 타입 변경 완료|-|
|event_id.iaas.nodegroup.update_flavor.failed|인스턴스 타입 변경 실패|-|
|event_id.iaas.nodegroup.upgrade.start|노드 그룹 업그레이드 시작|-|
|event_id.iaas.nodegroup.upgrade.end|노드 그룹 업그레이드 완료|-|
|event_id.iaas.nodegroup.upgrade.failed|노드 그룹 업그레이드 실패|-|
|event_id.iaas.nodegroup.userscript.update.start||-|
|event_id.iaas.nodegroup.userscript.update.end||-|
|event_id.iaas.nodegroup.userscript.update.failed||-|
|event_id.iaas.nodegroup.node_action.start_node.start|워커 노드 시작|-|
|event_id.iaas.nodegroup.node_action.start_node.end|워커 노드 시작 완료|-|
|event_id.iaas.nodegroup.node_action.start_node.failed|워커 노드 시작 실패|-|
|event_id.iaas.nodegroup.node_action.stop_node.start|워커 노드 중지 시작|-|
|event_id.iaas.nodegroup.node_action.stop_node.end|워커 노드 중지 완료|-|
|event_id.iaas.nodegroup.node_action.stop_node.failed|워커 노드 중지 실패|-|
|event_id.iaas.nodegroup.set_cluster_autoscaler.start|오토 스케일러 설정 변경 시작|-|
|event_id.iaas.nodegroup.set_cluster_autoscaler.end|오토 스케일러 설정 변경 완료|-|
|event_id.iaas.nodegroup.set_cluster_autoscaler.failed|오토 스케일러 설정 변경 실패|-|
|event_id.iaas.cluster.api_ep_ipacl_update.start|클러스터 API 엔드포인트 IP 접근 제어 변경 시작|-|
|event_id.iaas.cluster.api_ep_ipacl_update.end|클러스터 API 엔드포인트 IP 접근 제어 변경 완료|-|
|event_id.iaas.cluster.api_ep_ipacl_update.failed|클러스터 API 엔드포인트 IP 접근 제어 변경 실패|-|
|event_id.iaas.cluster.update_sgw.start|SGW 변경 시작|-|
|event_id.iaas.cluster.update_sgw.end|SGW 변경 완료|-|
|event_id.iaas.cluster.update_sgw.failed|SGW 변경 실패|-|
|event_id.iaas.nodegroup.update_extra_volume.end|추가 블록 스토리지 업데이트 완료|-|
|event_id.iaas.nodegroup.update_extra_volume.fail|추가 블록 스토리지 업데이트 실패|-|
|event_id.iaas.nodegroup.update_extra_volume.start|추가 블록 스토리지 업데이트 시작|-|
|event_id.iaas.nodegroup.update_extra_security_group.end|추가 보안 그룹 업데이트 완료|-|
|event_id.iaas.nodegroup.update_extra_security_group.fail|추가 보안 그룹 업데이트 실패|-|
|event_id.iaas.nodegroup.update_extra_security_group.start|추가 보안 그룹 업데이트 시작|-|
|event_id.iaas.cluster.update_nks_registry.end|NKS 레지스트리 업데이트 완료|-|
|event_id.iaas.cluster.update_nks_registry.fail|NKS 레지스트리 업데이트 실패|-|
|event_id.iaas.cluster.update_nks_registry.start|NKS 레지스트리 업데이트 시작|-|
|event_id.iaas.cluster.update_k8s_args.start|k8s 아규먼트 업데이트 시작|-|
|event_id.iaas.cluster.update_k8s_args.end|k8s 아규먼트 업데이트 완료|-|
|event_id.iaas.cluster.update_k8s_args.failed|k8s 아규먼트 업데이트 실패|-|
|event_id.iaas.cluster.update_oidc_args.start|OIDC 아규먼트 업데이트 시작|-|
|event_id.iaas.cluster.update_oidc_args.end|OIDC 아규먼트 업데이트 완료|-|
|event_id.iaas.cluster.update_oidc_args.failed|OIDC 아규먼트 업데이트 실패|-|
|event_id.iaas.cluster.update_vm_auth_key.start|키페어 업데이트 시작|-|
|event_id.iaas.cluster.update_vm_auth_key.end|키페어 업데이트 완료|-|
|event_id.iaas.cluster.update_vm_auth_key.failed|키페어 업데이트 실패|-|
|event_id.iaas.nodegroup.set_metric_base_autoscaler.start|노드 그룹 지표 기반 오토스케일러 설정 시작|-|
|event_id.iaas.nodegroup.set_metric_base_autoscaler.end|노드 그룹 지표 기반 오토스케일러 설정 완료|-|
|event_id.iaas.nodegroup.set_metric_base_autoscaler.failed|노드 그룹 지표 기반 오토스케일러 설정 실패|-|
|event_id.iaas.nodegroup.metric_base_autoscaler_node_scale_out.start|지표 기반 오토 스케일러 노드 그룹 노드 증설 시작|-|
|event_id.iaas.nodegroup.metric_base_autoscaler_node_scale_out.end|지표 기반 오토 스케일러 노드 그룹 노드 증설 완료|-|
|event_id.iaas.nodegroup.metric_base_autoscaler_node_scale_out.failed|지표 기반 오토 스케일러 노드 그룹 노드 증설 실패|-|
|event_id.iaas.nodegroup.metric_base_autoscaler_node_scale_in.start|지표 기반 오토 스케일러 노드 그룹 노드 감축 시작|-|
|event_id.iaas.nodegroup.metric_base_autoscaler_node_scale_in.end|지표 기반 오토 스케일러 노드 그룹 노드 감축 완료|-|
|event_id.iaas.nodegroup.metric_base_autoscaler_node_scale_in.failed|지표 기반 오토 스케일러 노드 그룹 노드 감축 실패|-|
|event_id.iaas.nodegroup.update_k8s_node_labels.start|노드 그룹 쿠버네티스 노드 레이블 변경 시작|-|
|event_id.iaas.nodegroup.update_k8s_node_labels.end|노드 그룹 쿠버네티스 노드 레이블 변경 완료|-|
|event_id.iaas.nodegroup.update_k8s_node_labels.failed|노드 그룹 쿠버네티스 노드 레이블 변경 실패|-|
|event_id.iaas.nodegroup.update_fip_auto_bind.start|플로팅 IP 자동 할당 변경 시작|-|
|event_id.iaas.nodegroup.update_fip_auto_bind.end|플로팅 IP 자동 할당 변경 완료|-|
|event_id.iaas.nodegroup.update_fip_auto_bind.failed|플로팅 IP 자동 할당 변경 실패|-|
|event_id.iaas.nodegroup.scale_in.start|노드 감축 시작|-|
|event_id.iaas.nodegroup.scale_in.end|노드 감축 완료|-|
|event_id.iaas.nodegroup.scale_in.failed|노드 감축 실패|-|
|event_id.iaas.nodegroup.scale_out.start|노드 증설 시작|-|
|event_id.iaas.nodegroup.scale_out.end|노드 증설 완료|-|
|event_id.iaas.nodegroup.scale_out.failed|노드 증설 실패|-|
|event_id.iaas.cluster.update_control_plane_log.start|컨트롤 플레인 로그 수집 업데이트 시작|-|
|event_id.iaas.cluster.update_control_plane_log.end|컨트롤 플레인 로그 수집 업데이트 완료|-|
|event_id.iaas.cluster.update_control_plane_log.failed|컨트롤 플레인 로그 수집 업데이트 실패|-|
|event_id.iaas.cluster.uninstall_addon.start|Addon 제거 시작|-|
|event_id.iaas.cluster.uninstall_addon.end|Addon 제거 완료|-|
|event_id.iaas.cluster.uninstall_addon.failed|Addon 제거 실패|-|
|event_id.iaas.cluster.install_addon.start|Addon 설치 시작|-|
|event_id.iaas.cluster.install_addon.end|Addon 설치 완료|-|
|event_id.iaas.cluster.install_addon.failed|Addon 설치 실패|-|
|event_id.iaas.cluster.update_addon.start|Addon 업데이트 시작|-|
|event_id.iaas.cluster.update_addon.end|Addon 업데이트 완료|-|
|event_id.iaas.cluster.update_addon.failed|Addon 업데이트 실패|-|

#### 블록 스토리지 (Infrastructure:BLOCK_STORAGE)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.volume.create_end|블록 스토리지 생성 완료|리소스 생성|
|event_id.iaas.volume.transfer_accept|블록 스토리지 이동 완료(대상)|리소스 생성|
|event_id.iaas.volume.copy_end|블록 스토리지 복제 완료|리소스 생성|
|event_id.iaas.volume.delete_end|블록 스토리지 삭제 완료|리소스 삭제|
|event_id.iaas.volume.transfer_create|블록 스토리지 이동 완료(소스)|리소스 삭제|
|event_id.iaas.volume.update_end|블록 스토리지 수정 완료|리소스 수정|

#### 플로팅 IP (Infrastructure:FLOATING_IP)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.floating_ip.create_end|플로팅 IP 생성 완료|리소스 생성|
|event_id.iaas.floating_ip.update_end|플로팅 IP 변경 완료|리소스 수정|
|event_id.iaas.floating_ip.delete_end|플로팅 IP 삭제 완료|리소스 삭제|

#### 이미지 (Infrastructure:IMAGE)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.image.create_end|이미지 생성 완료|리소스 생성|
|event_id.iaas.image.transfer_accept|이미지 이동 완료 (대상)|리소스 생성|
|event_id.iaas.image.delete_end|이미지 삭제 완료|리소스 삭제|
|event_id.iaas.image.transfer_create|이미지 이동 완료 (소스)|리소스 삭제|
|event_id.iaas.image.update_end|이미지 수정 완료|리소스 수정|

#### 이미지 템플릿 (Infrastructure:ImageTemplate)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.image_template.create|이미지 템플릿 생성|리소스 생성|
|event_id.iaas.image_template.update|이미지 템플릿 수정|리소스 수정|
|event_id.iaas.image_template.build|이미지 빌드|-|
|event_id.iaas.image_template.cancel_build|이미지 빌드 취소|-|
|event_id.iaas.image_template.delete|이미지 템플릿 삭제|리소스 삭제|

#### 로드 밸런서 (Infrastructure:LOAD_BALANCER)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.loadbalancer.create_end|로드 밸런서 생성 완료|리소스 생성|
|event_id.iaas.loadbalancer.update_end|로드 밸런서 정보 변경 완료|리소스 수정|
|event_id.iaas.loadbalancer.delete_end|로드 밸런서 삭제 완료|리소스 삭제|

#### NAS 스토리지 (Infrastructure:NAS.STORAGE)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.nas.volume.create|NAS 볼륨 생성|리소스 생성|
|event_id.iaas.nas.volume.update_end||리소스 수정|
|event_id.iaas.nas.volume.delete_end||리소스 삭제|
|event_id.iaas.nas.snapshot.create|NAS 스냅숏 생성|-|
|event_id.iaas.nas.snapshot.delete|NAS 스냅숏 삭제|-|
|event_id.iaas.nas.snapshot.restore|NAS 스냅숏 복원|-|
|event_id.iaas.nas.replication.set||-|
|event_id.iaas.nas.replication.unset||-|
|event_id.iaas.nas.replication.start||-|
|event_id.iaas.nas.replication.stop||-|
|event_id.iaas.nas.replication.change_direction||-|
|event_id.iaas.nas.subnet.attach||-|
|event_id.iaas.nas.subnet.detach||-|

#### NAT 게이트웨이 (Infrastructure:NAT_GATEWAY)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.nat_gateway.create_end|NAT 게이트웨이 생성 완료|리소스 생성|
|event_id.iaas.nat_gateway.update_end|NAT 게이트웨이 변경 완료|리소스 수정|
|event_id.iaas.nat_gateway.delete_end|NAT 게이트웨이 삭제 완료|리소스 삭제|

#### Private DNS Zone (Infrastructure:PRIVATE_DNS_ZONE)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.private_dns.zone.create_end|Private DNS Zone 생성 완료|리소스 생성|
|event_id.iaas.private_dns.zone.update_end|Private DNS Zone 수정 완료|리소스 수정|
|event_id.iaas.private_dns.zone.delete_end|Private DNS Zone 삭제 완료|리소스 삭제|

#### 블록 스토리지 스냅숏 (Infrastructure:SNAPSHOT)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.snapshot.create_end|블록 스토리지 스냅숏 생성 완료|리소스 생성|
|event_id.iaas.snapshot.delete_end|블록 스토리지 스냅숏 삭제 완료|리소스 삭제|

#### 트랜짓 허브 (Infrastructure:TRANSIT_HUB)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.transit_hub.create_end|트랜짓 허브 생성 완료|리소스 생성|
|event_id.iaas.transit_hub.update_end|트랜짓 허브 수정 완료|리소스 수정|
|event_id.iaas.transit_hub.delete_end|트랜짓 허브 삭제 완료|리소스 삭제|

#### 트랜짓 허브 연결 (Infrastructure:TRANSIT_HUB_ATTACHMENT)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.transit_hub_attachment.create_end|트랜짓 허브 연결 생성 완료|리소스 생성|
|event_id.iaas.transit_hub_attachment.update_end|트랜짓 허브 연결 변경 완료|리소스 수정|
|event_id.iaas.transit_hub_attachment.delete_end|트랜짓 허브 연결 삭제 완료|리소스 삭제|

#### VPC (Infrastructure:VPC)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.vpc.create_end|VPC 생성 완료|리소스 생성|
|event_id.iaas.vpc.update_end|VPC 정보 변경 완료|리소스 수정|
|event_id.iaas.vpc.delete_end|VPC 삭제 완료|리소스 삭제|

#### 인스턴스 (INSTANCE)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.instance.create_end|인스턴스 생성 완료|리소스 생성|
|event_id.iaas.instance.delete_end|인스턴스 삭제 완료|리소스 삭제|
|event_id.iaas.instance.update|인스턴스 정보 변경|리소스 수정|
|event_id.iaas.instance_action.reboot_end|인스턴스 재부팅 완료|-|
|event_id.iaas.instance_action.resize_end|인스턴스 타입 변경 완료|-|
|event_id.iaas.instance_action.start_end|중지된 인스턴스 시작 완료|-|
|event_id.iaas.instance_action.stop_end|인스턴스 중지 완료|-|
|event_id.iaas.instance_action.shelve_end|인스턴스 종료 완료|-|
|event_id.iaas.instance_action.unshelve_end|종료된 인스턴스 시작 완료|-|

#### 워크로드 (NHNContainerService:Workload)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.ncs.workload_create.start|워크로드 생성 시작|리소스 생성|
|event_id.iaas.ncs.workload_create.failed|워크로드 생성 실패|리소스 삭제|
|event_id.iaas.ncs.workload.delete|워크로드 삭제|리소스 삭제|
|event_id.iaas.ncs.workload.stop|워크로드 중지|리소스 수정|
|event_id.iaas.ncs.workload_restart.start|워크로드 재시작 시작|리소스 수정|
|event_id.iaas.ncs.workload_template_update.start|워크로드 템플릿 변경 시작|리소스 수정|
|event_id.iaas.ncs.workload_desired_update.start|워크로드 작업 요청 수 변경 시작|리소스 수정|
|event_id.iaas.ncs.workload_schedule.update|워크로드 예약 실행 변경|리소스 수정|
|event_id.iaas.ncs.workload_loadbalancer_update.start|워크로드 로드 밸런서 설정 변경 시작|리소스 수정|
|event_id.iaas.ncs.workload_create.end|워크로드 생성 완료|-|
|event_id.iaas.ncs.workload_restart.end|워크로드 재시작 완료|-|
|event_id.iaas.ncs.workload_restart.failed|워크로드 재시작 실패|-|
|event_id.iaas.ncs.workload_template_update.end|워크로드 템플릿 변경 완료|-|
|event_id.iaas.ncs.workload_template_update.failed|워크로드 템플릿 변경 실패|-|
|event_id.iaas.ncs.workload_desired_update.end|워크로드 작업 요청 수 변경 완료|-|
|event_id.iaas.ncs.workload_desired_update.failed|워크로드 작업 요청 수 변경 실패|-|
|event_id.iaas.ncs.workload_loadbalancer_update.end|워크로드 로드 밸런서 설정 변경 완료|-|
|event_id.iaas.ncs.workload_active_deadline.update|워크로드 종료 예약 변경|-|
|event_id.iaas.ncs.workload_internal_loadbalancer.update|워크로드 내부 로드 밸런서 설정 변경|-|
|event_id.iaas.ncs.workload_description.update|워크로드 설명 변경|-|


### Object Storage

#### 컨테이너 (ObjectStorage:Container)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.object_storage.container.create|컨테이너 생성|리소스 생성|
|event_id.object_storage.container.delete|컨테이너 삭제|리소스 삭제|
|event_id.object_storage.container.metadata.update|컨테이너 메타데이터 등록/수정|-|
|event_id.object_storage.container.sync.enable|컨테이너 복제 설정|-|
|event_id.object_storage.container.sync.update|컨테이너 복제 설정 변경|-|
|event_id.object_storage.container.sync.disable|컨테이너 복제 설정 해제|-|


### DNS Plus

#### DNS Plus GSLB (DNSPlus:GSLB)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.dnsplus.gslb.create|GSLB 생성|리소스 생성|
|event_id.dnsplus.gslb.update|GSLB 수정|리소스 수정|
|event_id.dnsplus.gslb.delete|GSLB 삭제|리소스 삭제|

#### DNS Plus 헬스 체크 (DNSPlus:HealthCheck)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.dnsplus.health_check.create|헬스 체크 생성|리소스 생성|
|event_id.dnsplus.health_check.update|헬스 체크 수정|리소스 수정|
|event_id.dnsplus.health_check.delete|헬스 체크 삭제|리소스 삭제|

#### DNS Plus Pool (DNSPlus:Pool)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.dnsplus.pool.create|Pool 생성|리소스 생성|
|event_id.dnsplus.pool.update|Pool 수정|리소스 수정|
|event_id.dnsplus.pool.delete|Pool 삭제|리소스 삭제|

#### DNS Plus Zone (DNSPlus:Zone)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.dnsplus.zone.create|DNS Zone 생성|리소스 생성|
|event_id.dnsplus.zone.update|DNS Zone 수정|리소스 수정|
|event_id.dnsplus.zone.delete|DNS Zone 삭제|리소스 삭제|

