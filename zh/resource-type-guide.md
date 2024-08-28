## Governance & Audit > Resource Watcher > List of Resource Type

* Below are service resource types and relevant events
* Event Types
  * Create Resource: Event that occurs when a resource is created
  * Modify Resource: Event that occurs when a resource is modified
  * Delete Resource: Event that occurs when a resource is deleted
  * -: Event not related to Create/Modify/Delete Resource

### Secure Key Manager

#### Key Store (SecureKeyManager:KeyStore)

| Event ID | Event Name | Event Type |
|--- |--- |--- |
|event_id.skm.keystore.create|Create Keystore|Create Resource|
|event_id.skm.keystore.delete|Delete Keystore|Delete Resource|
|event_id.skm.keystore.update|Change Keystore Information|Modify Resource|
|event_id.skm.secret.create|Create Confidential Data|-|
|event_id.skm.secret.delete|Immediately Delete Confidential Data|-|
|event_id.skm.symmetric.create|Create Symmectric Key|-|
|event_id.skm.symmetric.delete|Immediately Delete Symmetric Key|-|
|event_id.skm.asymmetric.create|Create Asymmetric Key|-|
|event_id.skm.asymmetric.delete|Immediately Delete Asymmetric Key|-|
|event_id.skm.api.secrets.get|Query Confidential Data|-|
|event_id.skm.api.symmetric.encrypt|Encrypt with Symmetric Key|-|
|event_id.skm.api.symmetric.decrypt|Decrypt with Symmetric Key|-|
|event_id.skm.api.symmetric.create_local_key|Create Local Key|-|
|event_id.skm.api.symmetric.get|Query Symmectric Key|-|
|event_id.skm.api.asymmetric.sign|Sign with Asymmetric Key|-|
|event_id.skm.api.asymmetric.verify|Verify Signature with Asymmetric Key|-|
|event_id.skm.api.asymmetric.get.privateKey|Query Private Key|-|
|event_id.skm.api.asymmetric.get.publicKey|Query Public Key|-|
|event_id.skm.api.secrets.create|Create Confidential Data|-|
|event_id.skm.api.symmetric.create|Create Symmectric Key|-|
|event_id.skm.api.asymmetric.create|Create Asymmetric Key|-|
|event_id.skm.api.secrets.delete|Immediately Delete Confidential Data|-|
|event_id.skm.api.symmetric.delete|Immediately Delete Symmetric Key|-|
|event_id.skm.api.asymmetric.delete|Immediately Delete Asymmetric Key|-|
|event_id.skm.secrets.scheduled_delete|Auto Delete Confidential Data|-|
|event_id.skm.symmetric.scheduled_delete|Auto Delete Symmetric Key|-|
|event_id.skm.asymmetric.scheduled_delete|Auto Delete Asymmetric Key|-|


### NHN Container Registry(NCR)

#### CONTAINER REGISTRY (NHNContainerRegistry:ContainerRegistry)

| Event ID | Event Name | Event Type |
|--- |--- |--- |
|event_id.ncr.registry.create|Create Registry|Create Resource|
|event_id.ncr.registry.delete|Delete Registry|Delete Resource|
|event_id.ncr.registry.update|Modify Registry|-|
|event_id.ncr.immutable_tag_rule.create|Add Image Protection Policy|-|
|event_id.ncr.immutable_tag_rule.delete|Delete Image Protection Policy|-|
|event_id.ncr.immutable_tag_rule.update|Modify Image Protection Policy|-|
|event_id.ncr.retention_rule.create|Create Image Cleanup Policy|-|
|event_id.ncr.retention_rule.delete|Delete Image Cleanup Policy|-|
|event_id.ncr.retention_rule.execute|Run Image Cleanup Policy|-|
|event_id.ncr.retention_rule.update|Modify Image Cleanup Policy|-|
|event_id.ncr.webhook.create|Create Webhook|-|
|event_id.ncr.webhook.delete|Delete Webhook|-|
|event_id.ncr.webhook.update|Modify Webhook|-|


### EasyCache

####  (EasyCache:NodeInstance)

| Event ID | Event Name | Event Type |
|--- |--- |--- |
|event_id.easycache.node.create|Add Node|Create Resource|
|event_id.easycache.node.update||Modify Resource|
|event_id.easycache.node.delete|Delete Node|Delete Resource|


### Default Infrastructure Service

#### CLUSTER (CLUSTER)

| Event ID | Event Name | Event Type |
|--- |--- |--- |
|event_id.iaas.cluster.auto_healing.detected|Detected autohealing|-|
|event_id.iaas.cluster.k8s_api_not_working.detected|Detection K8S APISERVER Issue|-|
|event_id.iaas.cluster.k8s_api_not_working.resolved|Resolved K8S APISERVER Issue|-|
|event_id.iaas.cluster.all_nodes_not_ready.detected|Detected all node stop|-|
|event_id.iaas.cluster.all_nodes_not_ready.resolved|Resolved all node stop|-|
|event_id.iaas.cluster.create.start|Create Cluster Started|Create Resource|
|event_id.iaas.cluster.create.end|Create Cluster Completed|-|
|event_id.iaas.cluster.create.failed|Create Cluster Failed|Delete Resource|
|event_id.iaas.cluster.delete.start|Delete Cluster Started|-|
|event_id.iaas.cluster.delete.end|Delete Cluster Completed|Delete Resource|
|event_id.iaas.cluster.delete.failed|Delete Cluster Failed|-|
|event_id.iaas.cluster.suspend.start||-|
|event_id.iaas.cluster.suspend.end||-|
|event_id.iaas.cluster.suspend.failed||-|
|event_id.iaas.cluster.resume.start|Change operational state Started|-|
|event_id.iaas.cluster.resume.end|Change operational state Completed|-|
|event_id.iaas.cluster.resume.failed|Change operational state Failed|-|
|event_id.iaas.cluster.handover.start|Change Cluster OWNER Started|-|
|event_id.iaas.cluster.handover.end|Change Cluster OWNER Completed|-|
|event_id.iaas.cluster.handover.failed|Change Cluster OWNER Failed|-|
|event_id.iaas.cluster.resize.start|Resize Cluster Started|-|
|event_id.iaas.cluster.resize.end|Resize Cluster Completed|-|
|event_id.iaas.cluster.resize.failed|Resize Cluster Failed|-|
|event_id.iaas.cluster.cni_update.start|Change CNI Started|-|
|event_id.iaas.cluster.cni_update.end|Change CNI Completed|-|
|event_id.iaas.cluster.cni_update.failed|Change CNI Failed|-|
|event_id.iaas.nodegroup.create.start|Create Node Group Started|-|
|event_id.iaas.nodegroup.create.end|Create Node Group Completed|-|
|event_id.iaas.nodegroup.create.failed|Create Node Group Failed|-|
|event_id.iaas.nodegroup.delete.start|Delete Node Group Started|-|
|event_id.iaas.nodegroup.delete.end|Delete Node Group Completed|-|
|event_id.iaas.nodegroup.delete.failed|Delete Node Group Failed|-|
|event_id.iaas.nodegroup.update_flavor.start|Change Instance Type Started|-|
|event_id.iaas.nodegroup.update_flavor.end|Change Instance Type Completed|-|
|event_id.iaas.nodegroup.update_flavor.failed|Change Instance Type Failed|-|
|event_id.iaas.nodegroup.upgrade.start|Upgrade Node Group Started|-|
|event_id.iaas.nodegroup.upgrade.end|Upgrade Node Group Completed|-|
|event_id.iaas.nodegroup.upgrade.failed|Upgrade Node Group Failed|-|
|event_id.iaas.nodegroup.userscript.update.start||-|
|event_id.iaas.nodegroup.userscript.update.end||-|
|event_id.iaas.nodegroup.userscript.update.failed||-|
|event_id.iaas.nodegroup.node_action.start_node.start|Start Worker Node Started|-|
|event_id.iaas.nodegroup.node_action.start_node.end|Start Worker Node Completed|-|
|event_id.iaas.nodegroup.node_action.start_node.failed|Start Worker Node Failed|-|
|event_id.iaas.nodegroup.node_action.stop_node.start|Stop Worker Node Started|-|
|event_id.iaas.nodegroup.node_action.stop_node.end|Stop Worker Node Completed|-|
|event_id.iaas.nodegroup.node_action.stop_node.failed|Stop Worker Node Failed|-|
|event_id.iaas.nodegroup.set_cluster_autoscaler.start|Change Autoscaler Settings Started|-|
|event_id.iaas.nodegroup.set_cluster_autoscaler.end|Change Autoscaler Settings Completed|-|
|event_id.iaas.nodegroup.set_cluster_autoscaler.failed|Change Autoscaler Settings Failed|-|
|event_id.iaas.cluster.api_ep_ipacl_update.start|Update Cluster API endpoint IP ACL Started|-|
|event_id.iaas.cluster.api_ep_ipacl_update.end|Update Cluster API endpoint IP ACL Completed|-|
|event_id.iaas.cluster.api_ep_ipacl_update.failed|Update Cluster API endpoint IP ACL Failed|-|
|event_id.iaas.cluster.update_sgw.start|Change SGW Started|-|
|event_id.iaas.cluster.update_sgw.end|Change SGW Completed|-|
|event_id.iaas.cluster.update_sgw.failed|Change SGW Failed|-|
|event_id.iaas.nodegroup.update_extra_volume.end|Additional block storage update completed|-|
|event_id.iaas.nodegroup.update_extra_volume.fail|Additional block storage update failed|-|
|event_id.iaas.nodegroup.update_extra_volume.start|Additional block storage update started|-|
|event_id.iaas.nodegroup.update_extra_security_group.end|Additional security group update completed|-|
|event_id.iaas.nodegroup.update_extra_security_group.fail|Additional security group update failed|-|
|event_id.iaas.nodegroup.update_extra_security_group.start|Additional security group update started|-|
|event_id.iaas.cluster.update_nks_registry.end|NKS registry update completed|-|
|event_id.iaas.cluster.update_nks_registry.fail|NKS registry update failed|-|
|event_id.iaas.cluster.update_nks_registry.start|NKS registry update started|-|

#### IMAGE TEMPLATE (Infrastructure:ImageTemplate)

| Event ID | Event Name | Event Type |
|--- |--- |--- |
|event_id.iaas.image_template.create|Create Image Template|Create Resource|
|event_id.iaas.image_template.update|Modify Image Template|Modify Resource|
|event_id.iaas.image_template.build|Build Image|-|
|event_id.iaas.image_template.cancel_build|Cancel Image Build|-|
|event_id.iaas.image_template.delete|Delete Image Template|Delete Resource|

#### INSTANCE (INSTANCE)

| Event ID | Event Name | Event Type |
|--- |--- |--- |
|event_id.iaas.instance.create_end|Create Instance Completed|Create Resource|
|event_id.iaas.instance.delete_end|Delete Instance Completed|Delete Resource|
|event_id.iaas.instance.update|Change Instance Information|Modify Resource|
|event_id.iaas.instance_action.reboot_end|Reboot Instance Completed|-|
|event_id.iaas.instance_action.resize_end|Change Instance Type Completed|-|
|event_id.iaas.instance_action.start_end|Start Stopped Instance Completed|-|
|event_id.iaas.instance_action.stop_end|Stop Instance Completed|-|

#### WORKLOAD (NHNContainerService:Workload)

| Event ID | Event Name | Event Type |
|--- |--- |--- |
|event_id.iaas.ncs.workload_create.start|Create Workload Started|Create Resource|
|event_id.iaas.ncs.workload_create.failed|Create Workload Failed|Delete Resource|
|event_id.iaas.ncs.workload.delete|Delete Workload|Delete Resource|
|event_id.iaas.ncs.workload.stop|Stop Workload|Modify Resource|
|event_id.iaas.ncs.workload_restart.start|Restart Workload Started|Modify Resource|
|event_id.iaas.ncs.workload_template_update.start|Change Workload Template Started|Modify Resource|
|event_id.iaas.ncs.workload_desired_update.start|Change Number of Workload Task Requests Start|Modify Resource|
|event_id.iaas.ncs.workload_schedule.update|Change Scheduled Run|Modify Resource|
|event_id.iaas.ncs.workload_loadbalancer_update.start||Modify Resource|
|event_id.iaas.ncs.workload_create.end|Create Workload Completed|-|
|event_id.iaas.ncs.workload_restart.end|Restart Workload Completed|-|
|event_id.iaas.ncs.workload_restart.failed|Restart Workload Failed|-|
|event_id.iaas.ncs.workload_template_update.end|Change Workload Template Completed|-|
|event_id.iaas.ncs.workload_template_update.failed|Change Workload Template Failed|-|
|event_id.iaas.ncs.workload_desired_update.end|Change Number of Workload Task Requests Completed|-|
|event_id.iaas.ncs.workload_desired_update.failed|Change Number of Workload Task Requests Failed|-|
|event_id.iaas.ncs.workload_loadbalancer_update.end|Change Workload Load Balancer Failed|-|
|event_id.iaas.ncs.workload_active_deadline.update|Change Schedule Termination|-|
|event_id.iaas.ncs.workload_internal_loadbalancer.update|Change Workload Internal Load Balancer|-|
|event_id.iaas.ncs.workload_description.update|Change Workload Description|-|


### DataQuery

#### Cluster (DataQuery:Cluster)

| Event ID | Event Name | Event Type |
|--- |--- |--- |
|event_id.dataquery.cluster_on|Trino Cluster On|Create Resource|
|event_id.dataquery.cluster_off|Trino Cluster Off|Delete Resource|
|event_id.dataquery.kr3.cluster_on||Create Resource|
|event_id.dataquery.kr3.cluster_off||Delete Resource|
|event_id.dataquery.pj1.cluster_on||Create Resource|
|event_id.dataquery.pj1.cluster_off||Delete Resource|


