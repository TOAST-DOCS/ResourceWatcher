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
|event_id.skm.api.secrets.get|기밀 데이터 조회|-|
|event_id.skm.api.symmetric.encrypt|대칭 키를 통한 암호화|-|
|event_id.skm.api.symmetric.decrypt|대칭 키를 통한 복호화|-|
|event_id.skm.api.symmetric.create_local_key|로컬 키 생성|-|
|event_id.skm.api.symmetric.get|대칭 키 조회|-|
|event_id.skm.api.asymmetric.sign|비대칭 키를 통한 서명|-|
|event_id.skm.api.asymmetric.verify|비대칭 키를 통한 서명 검증|-|
|event_id.skm.api.asymmetric.get.privateKey|개인 키 조회|-|
|event_id.skm.api.asymmetric.get.publicKey|공개 키 조회|-|
|event_id.skm.api.secrets.create|기밀 데이터 생성|-|
|event_id.skm.api.symmetric.create|대칭 키 생성|-|
|event_id.skm.api.asymmetric.create|비대칭 키 생성|-|
|event_id.skm.api.secrets.delete|기밀 데이터 즉시 삭제|-|
|event_id.skm.api.symmetric.delete|대칭 키 즉시 삭제|-|
|event_id.skm.api.asymmetric.delete|비대칭 키 즉시 삭제|-|
|event_id.skm.secrets.scheduled_delete|기밀 데이터 자동 삭제|-|
|event_id.skm.symmetric.scheduled_delete|대칭 키 자동 삭제|-|
|event_id.skm.asymmetric.scheduled_delete|비대칭 키 자동 삭제|-|


### EasyCache

####  (EasyCache:NodeInstance)

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

#### 이미지 템플릿 (Infrastructure:ImageTemplate)

| 이벤트 ID | 이벤트 명 | 이벤트 유형 |
|--- |--- |--- |
|event_id.iaas.image_template.create|이미지 템플릿 생성|리소스 생성|
|event_id.iaas.image_template.update|이미지 템플릿 수정|리소스 수정|
|event_id.iaas.image_template.build|이미지 빌드|-|
|event_id.iaas.image_template.cancel_build|이미지 빌드 취소|-|
|event_id.iaas.image_template.delete|이미지 템플릿 삭제|리소스 삭제|

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
|event_id.iaas.ncs.workload_loadbalancer_update.start||리소스 수정|
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


