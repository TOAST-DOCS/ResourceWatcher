## Governance & Audit > Resource Watcher > リソースタイプリスト

* サービスリソースの種類及び関連するイベントのリストです。
* イベントの種類
	* リソース作成：リソースの作成時に発生するイベント
	* リソース修正：リソースの修正時に発生するイベント
	* リソース削除：リソースの削除時に発生するイベント
	* -：リソース作成/修正/削除と関連ないイベント

### Secure Key Manager

#### キーストア (SecureKeyManager:KeyStore)

| イベント ID | イベント名検索 | イベントタイプ |
|--- |--- |--- |
|event_id.skm.keystore.create|キーストアの作成|リソース作成|
|event_id.skm.keystore.delete|キーストアの削除|リソース削除|
|event_id.skm.keystore.update|キーストア情報の変更|リソース修正|
|event_id.skm.secret.create|機密データの作成|-|
|event_id.skm.secret.delete|機密データの即時削除|-|
|event_id.skm.symmetric.create|対称鍵の作成|-|
|event_id.skm.symmetric.delete|対称鍵の即時削除|-|
|event_id.skm.asymmetric.create|非対称鍵の作成|-|
|event_id.skm.asymmetric.delete|非対称鍵の即時削除|-|
|event_id.skm.api.secrets.get|機密データの照会|-|
|event_id.skm.api.symmetric.encrypt|対称鍵による暗号化|-|
|event_id.skm.api.symmetric.decrypt|対称による復号|-|
|event_id.skm.api.symmetric.create_local_key|ローカルキー作成|-|
|event_id.skm.api.symmetric.get|対称鍵の照会|-|
|event_id.skm.api.asymmetric.sign|非対称鍵による署名|-|
|event_id.skm.api.asymmetric.verify|非対称鍵による署名検証|-|
|event_id.skm.api.asymmetric.get.privateKey|秘密鍵の照会|-|
|event_id.skm.api.asymmetric.get.publicKey|公開鍵の照会|-|
|event_id.skm.api.secrets.create|機密データの作成|-|
|event_id.skm.api.symmetric.create|対称鍵の作成|-|
|event_id.skm.api.asymmetric.create|非対称鍵の作成|-|
|event_id.skm.api.secrets.delete|機密データの即時削除|-|
|event_id.skm.api.symmetric.delete|対称鍵の即時削除|-|
|event_id.skm.api.asymmetric.delete|非対称鍵の即時削除|-|
|event_id.skm.secrets.scheduled_delete|機密データの自動削除|-|
|event_id.skm.symmetric.scheduled_delete|対称鍵の自動削除|-|
|event_id.skm.asymmetric.scheduled_delete|非対称鍵の自動削除|-|


### NHN Container Registry(NCR)

#### コンテナレジストリ (NHNContainerRegistry:ContainerRegistry)

| イベント ID | イベント名検索 | イベントタイプ |
|--- |--- |--- |
|event_id.ncr.registry.create|レジストリの作成|リソース作成|
|event_id.ncr.registry.delete|レジストリの削除|リソース削除|
|event_id.ncr.registry.update|レジストリの修正|-|
|event_id.ncr.immutable_tag_rule.create|イメージ保護ポリシー追加|-|
|event_id.ncr.immutable_tag_rule.delete|イメージ保護ポリシー削除|-|
|event_id.ncr.immutable_tag_rule.update|イメージ保護ポリシー修正|-|
|event_id.ncr.retention_rule.create|イメージ整理ポリシー追加|-|
|event_id.ncr.retention_rule.delete|イメージ整理ポリシー削除|-|
|event_id.ncr.retention_rule.execute|イメージ整理ポリシー実行|-|
|event_id.ncr.retention_rule.update|イメージ整理ポリシー修正|-|
|event_id.ncr.webhook.create|Webフック作成|-|
|event_id.ncr.webhook.delete|Webフック削除|-|
|event_id.ncr.webhook.update|Webフック修正|-|


### EasyCache

####  (EasyCache:NodeInstance)

| イベント ID | イベント名検索 | イベントタイプ |
|--- |--- |--- |
|event_id.easycache.node.create|ノード追加|リソース作成|
|event_id.easycache.node.update||リソース修正|
|event_id.easycache.node.delete|ノード削除|リソース削除|


### 基本インフラサービス

#### クラスター (CLUSTER)

| イベント ID | イベント名検索 | イベントタイプ |
|--- |--- |--- |
|event_id.iaas.cluster.auto_healing.detected|オートヒーリング検出|-|
|event_id.iaas.cluster.k8s_api_not_working.detected|K8S APISERVERの問題検出|-|
|event_id.iaas.cluster.k8s_api_not_working.resolved|K8S APISERVERのトラブルシューティング|-|
|event_id.iaas.cluster.all_nodes_not_ready.detected|すべてのノード停止問題の検出|-|
|event_id.iaas.cluster.all_nodes_not_ready.resolved|すべてのノード停止のトラブルシューティング|-|
|event_id.iaas.cluster.create.start|クラスター作成起動|リソース作成|
|event_id.iaas.cluster.create.end|クラスター作成完了|-|
|event_id.iaas.cluster.create.failed|クラスター作成失敗|リソース削除|
|event_id.iaas.cluster.delete.start|クラスター削除起動|-|
|event_id.iaas.cluster.delete.end|クラスター削除完了|リソース削除|
|event_id.iaas.cluster.delete.failed|クラスター削除失敗|-|
|event_id.iaas.cluster.suspend.start||-|
|event_id.iaas.cluster.suspend.end||-|
|event_id.iaas.cluster.suspend.failed||-|
|event_id.iaas.cluster.resume.start|クラスタ動作可能な移行の開始|-|
|event_id.iaas.cluster.resume.end|クラスタ動作可能な移行完了|-|
|event_id.iaas.cluster.resume.failed|クラスター動作可能遷移失敗|-|
|event_id.iaas.cluster.handover.start|クラスタOWNERの変更起動|-|
|event_id.iaas.cluster.handover.end|クラスタOWNERの変更完了|-|
|event_id.iaas.cluster.handover.failed|クラスタOWNERの変更失敗|-|
|event_id.iaas.cluster.resize.start|クラスターサイズ調整起動|-|
|event_id.iaas.cluster.resize.end|クラスターサイズ調整完了|-|
|event_id.iaas.cluster.resize.failed|クラスターサイズ調整失敗|-|
|event_id.iaas.cluster.cni_update.start|CNI変更起動|-|
|event_id.iaas.cluster.cni_update.end|CNI変更完了|-|
|event_id.iaas.cluster.cni_update.failed|CNI変更失敗|-|
|event_id.iaas.nodegroup.create.start|ノードグループ作成起動|-|
|event_id.iaas.nodegroup.create.end|ノードグループ作成完了|-|
|event_id.iaas.nodegroup.create.failed|ノードグループ作成失敗|-|
|event_id.iaas.nodegroup.delete.start|ノードグループ削除起動|-|
|event_id.iaas.nodegroup.delete.end|ノードグループ削除完了|-|
|event_id.iaas.nodegroup.delete.failed|ノードグループ削除失敗|-|
|event_id.iaas.nodegroup.update_flavor.start|インスタンスタイプの変更|-|
|event_id.iaas.nodegroup.update_flavor.end|インスタンスタイプの変更完了|-|
|event_id.iaas.nodegroup.update_flavor.failed|インスタンスタイプの変更失敗|-|
|event_id.iaas.nodegroup.upgrade.start|ノードグループーのアップグレード起動|-|
|event_id.iaas.nodegroup.upgrade.end|ノードグループーのアップグレード完了|-|
|event_id.iaas.nodegroup.upgrade.failed|ノードグループーのアップグレード失敗|-|
|event_id.iaas.nodegroup.userscript.update.start||-|
|event_id.iaas.nodegroup.userscript.update.end||-|
|event_id.iaas.nodegroup.userscript.update.failed||-|
|event_id.iaas.nodegroup.node_action.start_node.start|ワーカーノードの起動|-|
|event_id.iaas.nodegroup.node_action.start_node.end|ワーカーノードの起動完了|-|
|event_id.iaas.nodegroup.node_action.start_node.failed|ワーカーノードの起動失敗|-|
|event_id.iaas.nodegroup.node_action.stop_node.start|ワーカーノードの停止起動|-|
|event_id.iaas.nodegroup.node_action.stop_node.end|ワーカーノードの停止完了|-|
|event_id.iaas.nodegroup.node_action.stop_node.failed|ワーカーノードの停止失敗|-|
|event_id.iaas.nodegroup.set_cluster_autoscaler.start|オートスケーラーの設定を変更起動|-|
|event_id.iaas.nodegroup.set_cluster_autoscaler.end|オートスケーラーの設定を変更完了|-|
|event_id.iaas.nodegroup.set_cluster_autoscaler.failed|オートスケーラーの設定を変更失敗|-|
|event_id.iaas.cluster.api_ep_ipacl_update.start|クラスタAPIエンドポイントIPアクセス制御の変更の起動|-|
|event_id.iaas.cluster.api_ep_ipacl_update.end|クラスタAPIエンドポイントIPアクセス制御の変更の完了|-|
|event_id.iaas.cluster.api_ep_ipacl_update.failed|クラスタAPIエンドポイントIPアクセス制御の変更の失敗|-|
|event_id.iaas.cluster.update_sgw.start|SGW 変更|-|
|event_id.iaas.cluster.update_sgw.end|SGW 変更完了|-|
|event_id.iaas.cluster.update_sgw.failed|SGW 変更失敗|-|
|event_id.iaas.nodegroup.update_extra_volume.end|追加ブロックストレージアップデートの完了|-|
|event_id.iaas.nodegroup.update_extra_volume.fail|追加ブロックストレージの更新に失敗しました|-|
|event_id.iaas.nodegroup.update_extra_volume.start|追加ブロックストレージアップデートの開始|-|
|event_id.iaas.nodegroup.update_extra_security_group.end|追加セキュリティグループの更新が完了しました|-|
|event_id.iaas.nodegroup.update_extra_security_group.fail|追加のセキュリティグループの更新に失敗しました|-|
|event_id.iaas.nodegroup.update_extra_security_group.start|追加のセキュリティグループの更新を開始|-|
|event_id.iaas.cluster.update_nks_registry.end|NKSレジストリ更新の完了|-|
|event_id.iaas.cluster.update_nks_registry.fail|NKSレジストリ更新に失敗しました|-|
|event_id.iaas.cluster.update_nks_registry.start|NKSレジストリ更新の開始|-|

#### ブロックストレージ (Infrastructure:BLOCK_STORAGE)

| イベント ID | イベント名検索 | イベントタイプ |
|--- |--- |--- |
|event_id.iaas.volume.create_end|ブロックストレージ作成完了|リソース作成|
|event_id.iaas.volume.transfer_accept||リソース作成|
|event_id.iaas.volume.copy_end|ブロックストレージ複製完了|リソース作成|
|event_id.iaas.volume.delete_end|ブロックストレージ削除完了|リソース削除|
|event_id.iaas.volume.transfer_create||リソース削除|
|event_id.iaas.volume.update_end|ブロックストレージ修正完了|リソース修正|

#### イメージの (Infrastructure:IMAGE)

| イベント ID | イベント名検索 | イベントタイプ |
|--- |--- |--- |
|event_id.iaas.image.create_end|イメージ作成完了|リソース作成|
|event_id.iaas.image.transfer_accept||リソース作成|
|event_id.iaas.image.delete_end|イメージ削除完了|リソース削除|
|event_id.iaas.image.transfer_create||リソース削除|
|event_id.iaas.image.update_end|イメージ修正完了|リソース修正|

#### イメージテンプレート (Infrastructure:ImageTemplate)

| イベント ID | イベント名検索 | イベントタイプ |
|--- |--- |--- |
|event_id.iaas.image_template.create|イメージテンプレートの作成|リソース作成|
|event_id.iaas.image_template.update|イメージテンプレートの修正|リソース修正|
|event_id.iaas.image_template.build|イメージビルド|-|
|event_id.iaas.image_template.cancel_build|イメージビルドのキャンセル|-|
|event_id.iaas.image_template.delete|イメージテンプレートの削除|リソース削除|

#### ブロックストレージスナップショット (Infrastructure:SNAPSHOT)

| イベント ID | イベント名検索 | イベントタイプ |
|--- |--- |--- |
|event_id.iaas.snapshot.create_end|ブロックストレージスナップショット作成完了|リソース作成|
|event_id.iaas.snapshot.delete_end|ブロックストレージスナップショット削除完了|リソース削除|

#### インスタンス (INSTANCE)

| イベント ID | イベント名検索 | イベントタイプ |
|--- |--- |--- |
|event_id.iaas.instance.create_end|インスタンスの作成完了|リソース作成|
|event_id.iaas.instance.delete_end|インスタンスの削除完了|リソース削除|
|event_id.iaas.instance.update|インスタンス情報の変更|リソース修正|
|event_id.iaas.instance_action.reboot_end|インスタンスの再起動完了|-|
|event_id.iaas.instance_action.resize_end|インスタンスタイプの変更完了|-|
|event_id.iaas.instance_action.start_end|停止したインスタンスの起動完了|-|
|event_id.iaas.instance_action.stop_end|インスタンスの停止完了|-|
|event_id.iaas.instance_action.shelve_end|インスタンス終了完了|-|
|event_id.iaas.instance_action.unshelve_end|終了したインスタンスの起動完了|-|

#### ワークロード (NHNContainerService:Workload)

| イベント ID | イベント名検索 | イベントタイプ |
|--- |--- |--- |
|event_id.iaas.ncs.workload_create.start|ワークロードの作成|リソース作成|
|event_id.iaas.ncs.workload_create.failed|ワークロードの作成失敗|リソース削除|
|event_id.iaas.ncs.workload.delete|ワークロードの削除|リソース削除|
|event_id.iaas.ncs.workload.stop|ワークロード停止|リソース修正|
|event_id.iaas.ncs.workload_restart.start|ワークロード再起動|リソース修正|
|event_id.iaas.ncs.workload_template_update.start|ワークロードのテンプレート変更|リソース修正|
|event_id.iaas.ncs.workload_desired_update.start|ワークロード作業リクエスト数の変更|リソース修正|
|event_id.iaas.ncs.workload_schedule.update|ワークロードの予約実行変更|リソース修正|
|event_id.iaas.ncs.workload_loadbalancer_update.start||リソース修正|
|event_id.iaas.ncs.workload_create.end|ワークロードの作成完|-|
|event_id.iaas.ncs.workload_restart.end|ワークロード再起動完了|-|
|event_id.iaas.ncs.workload_restart.failed|ワークロード再起動失敗|-|
|event_id.iaas.ncs.workload_template_update.end|ワークロードのテンプレート変更完了|-|
|event_id.iaas.ncs.workload_template_update.failed|ワークロードのテンプレート変更失敗|-|
|event_id.iaas.ncs.workload_desired_update.end|ワークロード作業リクエスト数の変更完了|-|
|event_id.iaas.ncs.workload_desired_update.failed|ワークロード作業リクエスト数の変更失敗|-|
|event_id.iaas.ncs.workload_loadbalancer_update.end|ワークロードロードバランサーの変更完了|-|
|event_id.iaas.ncs.workload_active_deadline.update|ワークロードの終了予約設定を変更|-|
|event_id.iaas.ncs.workload_internal_loadbalancer.update|ワークロード内部ロードバランサーの変更|-|
|event_id.iaas.ncs.workload_description.update|ワークロード説明の変更|-|


### DataQuery

#### クラスタオン (DataQuery:Cluster)

| イベント ID | イベント名検索 | イベントタイプ |
|--- |--- |--- |
|event_id.dataquery.cluster_on|Trinoクラスタオン|リソース作成|
|event_id.dataquery.cluster_off|Trinoクラスタオフ|リソース削除|
|event_id.dataquery.kr3.cluster_on||リソース作成|
|event_id.dataquery.kr3.cluster_off||リソース削除|
|event_id.dataquery.pj1.cluster_on||リソース作成|
|event_id.dataquery.pj1.cluster_off||リソース削除|


