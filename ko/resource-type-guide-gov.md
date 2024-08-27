## Governance & Audit > Resource Watcher > 리소스 유형 목록

* 서비스 리소스 유형 및 관련된 이벤트 목록입니다.
* 이벤트 유형
	* 리소스 생성: 리소스 생성 시 발생하는 이벤트
	* 리소스 수정: 리소스 수정 시 발생하는 이벤트
	* 리소스 삭제: 리소스 삭제 시 발생하는 이벤트
	* -: 리소스 생성/수정/삭제와 관련 없는 이벤트


### 기본 인프라 서비스

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


