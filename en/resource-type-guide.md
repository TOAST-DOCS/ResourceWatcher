## Governance & Audit > Resource Watcher > List of Resource Type

- Below are service resource types and relevant events
- Event Types
  - Create Resource: Event that occurs when a resource is created
  - Modify Resource: Event that occurs when a resource is modified
  - Delete Resource: Event that occurs when a resource is deleted
  - -: Event not related to Create/Modify/Delete Resource

### Secure Key Manager

#### Key Store (SecureKeyManager:KeyStore)

| Event ID                                    | Event Name                                 | Event Type      |
| ------------------------------------------- | ------------------------------------------ | --------------- |
| event_id.skm.keystore.create                | Create Keystore                            | Create Resource |
| event_id.skm.keystore.delete                | Delete Keystore                            | Delete Resource |
| event_id.skm.keystore.update                | Change Keystore Information                | Modify Resource |
| event_id.skm.secret.create                  | Create Confidential Data                   | -               |
| event_id.skm.secret.delete                  | Immediately Delete Confidential Data       | -               |
| event_id.skm.symmetric.create               | Create Symmetric Key                       | -               |
| event_id.skm.symmetric.delete               | Immediately Delete Symmetric Key           | -               |
| event_id.skm.asymmetric.create              | Create Asymmetric Key                      | -               |
| event_id.skm.asymmetric.delete              | Immediately Delete Asymmetric Key          | -               |
| event_id.skm.api.secrets.get                | Query Confidential Data (API)              | -               |
| event_id.skm.api.symmetric.encrypt          | Encrypt with Symmetric Key (API)           | -               |
| event_id.skm.api.symmetric.decrypt          | Decrypt with Symmetric Key (API)           | -               |
| event_id.skm.api.symmetric.create_local_key | Create Local Key (API)                     | -               |
| event_id.skm.api.symmetric.get              | Query Symmetric Key (API)                  | -               |
| event_id.skm.api.asymmetric.sign            | Sign with Asymmetric Key (API)             | -               |
| event_id.skm.api.asymmetric.verify          | Verify Signature with Asymmetric Key (API) | -               |
| event_id.skm.api.asymmetric.get.privateKey  | Query Private Key (API)                    | -               |
| event_id.skm.api.asymmetric.get.publicKey   | Query Public Key (API)                     | -               |
| event_id.skm.api.secrets.create             | Create Confidential Data (API)             | -               |
| event_id.skm.api.symmetric.create           | Create Symmetric Key (API)                 | -               |
| event_id.skm.api.asymmetric.create          | Create Asymmetric Key (API)                | -               |
| event_id.skm.api.secrets.delete             | Immediately Delete Confidential Data (API) | -               |
| event_id.skm.api.symmetric.delete           | Immediately Delete Symmetric Key (API)     | -               |
| event_id.skm.api.asymmetric.delete          | Immediately Delete Asymmetric Key (API)    | -               |
| event_id.skm.secrets.scheduled_delete       | Auto Delete Confidential Data              | -               |
| event_id.skm.symmetric.scheduled_delete     | Auto Delete Symmetric Key                  | -               |
| event_id.skm.asymmetric.scheduled_delete    | Auto Delete Asymmetric Key                 | -               |

### NHN Container Registry(NCR)

#### CONTAINER REGISTRY (NHNContainerRegistry:ContainerRegistry)

| Event ID                               | Event Name                     | Event Type      |
| -------------------------------------- | ------------------------------ | --------------- |
| event_id.ncr.registry.create           | Create Registry                | Create Resource |
| event_id.ncr.registry.delete           | Delete Registry                | Delete Resource |
| event_id.ncr.registry.update           | Modify Registry                | -               |
| event_id.ncr.immutable_tag_rule.create | Add Image Protection Policy    | -               |
| event_id.ncr.immutable_tag_rule.delete | Delete Image Protection Policy | -               |
| event_id.ncr.immutable_tag_rule.update | Modify Image Protection Policy | -               |
| event_id.ncr.retention_rule.create     | Create Image Cleanup Policy    | -               |
| event_id.ncr.retention_rule.delete     | Delete Image Cleanup Policy    | -               |
| event_id.ncr.retention_rule.execute    | Run Image Cleanup Policy       | -               |
| event_id.ncr.retention_rule.update     | Modify Image Cleanup Policy    | -               |
| event_id.ncr.webhook.create            | Create Webhook                 | -               |
| event_id.ncr.webhook.delete            | Delete Webhook                 | -               |
| event_id.ncr.webhook.update            | Modify Webhook                 | -               |

### EasyCache

#### NODE INSTANCE (EasyCache:NodeInstance)

| Event ID                       | Event Name  | Event Type      |
| ------------------------------ | ----------- | --------------- |
| event_id.easycache.node.create | Add Node    | Create Resource |
| event_id.easycache.node.update |             | Modify Resource |
| event_id.easycache.node.delete | Delete Node | Delete Resource |

### Default Infrastructure Service

#### CLUSTER (CLUSTER)

| Event ID                                                  | Event Name                                   | Event Type      |
| --------------------------------------------------------- | -------------------------------------------- | --------------- |
| event_id.iaas.cluster.auto_healing.detected               | Detected autohealing                         | -               |
| event_id.iaas.cluster.k8s_api_not_working.detected        | Detected K8S APISERVER Issue                 | -               |
| event_id.iaas.cluster.k8s_api_not_working.resolved        | Resolved K8S APISERVER Issue                 | -               |
| event_id.iaas.cluster.all_nodes_not_ready.detected        | Detected all node stop                       | -               |
| event_id.iaas.cluster.all_nodes_not_ready.resolved        | Resolved all node stop                       | -               |
| event_id.iaas.cluster.create.start                        | Create Cluster Started                       | Create Resource |
| event_id.iaas.cluster.create.end                          | Create Cluster Completed                     | -               |
| event_id.iaas.cluster.create.failed                       | Create Cluster Failed                        | Delete Resource |
| event_id.iaas.cluster.delete.start                        | Delete Cluster Started                       | -               |
| event_id.iaas.cluster.delete.end                          | Delete Cluster Completed                     | Delete Resource |
| event_id.iaas.cluster.delete.failed                       | Delete Cluster Failed                        | -               |
| event_id.iaas.cluster.suspend.start                       |                                              | -               |
| event_id.iaas.cluster.suspend.end                         |                                              | -               |
| event_id.iaas.cluster.suspend.failed                      |                                              | -               |
| event_id.iaas.cluster.resume.start                        | Change operational state Started             | -               |
| event_id.iaas.cluster.resume.end                          | Change operational state Completed           | -               |
| event_id.iaas.cluster.resume.failed                       | Change operational state Failed              | -               |
| event_id.iaas.cluster.handover.start                      | Change Cluster OWNER Started                 | -               |
| event_id.iaas.cluster.handover.end                        | Change Cluster OWNER Completed               | -               |
| event_id.iaas.cluster.handover.failed                     | Change Cluster OWNER Failed                  | -               |
| event_id.iaas.cluster.resize.start                        | Resize Cluster Started                       | -               |
| event_id.iaas.cluster.resize.end                          | Resize Cluster Completed                     | -               |
| event_id.iaas.cluster.resize.failed                       | Resize Cluster Failed                        | -               |
| event_id.iaas.cluster.cni_update.start                    | Change CNI Started                           | -               |
| event_id.iaas.cluster.cni_update.end                      | Change CNI Completed                         | -               |
| event_id.iaas.cluster.cni_update.failed                   | Change CNI Failed                            | -               |
| event_id.iaas.nodegroup.create.start                      | Create Node Group Started                    | -               |
| event_id.iaas.nodegroup.create.end                        | Create Node Group Completed                  | -               |
| event_id.iaas.nodegroup.create.failed                     | Create Node Group Failed                     | -               |
| event_id.iaas.nodegroup.delete.start                      | Delete Node Group Started                    | -               |
| event_id.iaas.nodegroup.delete.end                        | Delete Node Group Completed                  | -               |
| event_id.iaas.nodegroup.delete.failed                     | Delete Node Group Failed                     | -               |
| event_id.iaas.nodegroup.update_flavor.start               | Change Instance Type Started                 | -               |
| event_id.iaas.nodegroup.update_flavor.end                 | Change Instance Type Completed               | -               |
| event_id.iaas.nodegroup.update_flavor.failed              | Change Instance Type Failed                  | -               |
| event_id.iaas.nodegroup.upgrade.start                     | Upgrade Node Group Started                   | -               |
| event_id.iaas.nodegroup.upgrade.end                       | Upgrade Node Group Completed                 | -               |
| event_id.iaas.nodegroup.upgrade.failed                    | Upgrade Node Group Failed                    | -               |
| event_id.iaas.nodegroup.userscript.update.start           |                                              | -               |
| event_id.iaas.nodegroup.userscript.update.end             |                                              | -               |
| event_id.iaas.nodegroup.userscript.update.failed          |                                              | -               |
| event_id.iaas.nodegroup.node_action.start_node.start      | Start Worker Node Started                    | -               |
| event_id.iaas.nodegroup.node_action.start_node.end        | Start Worker Node Completed                  | -               |
| event_id.iaas.nodegroup.node_action.start_node.failed     | Start Worker Node Failed                     | -               |
| event_id.iaas.nodegroup.node_action.stop_node.start       | Stop Worker Node Started                     | -               |
| event_id.iaas.nodegroup.node_action.stop_node.end         | Stop Worker Node Completed                   | -               |
| event_id.iaas.nodegroup.node_action.stop_node.failed      | Stop Worker Node Failed                      | -               |
| event_id.iaas.nodegroup.set_cluster_autoscaler.start      | Change Autoscaler Settings Started           | -               |
| event_id.iaas.nodegroup.set_cluster_autoscaler.end        | Change Autoscaler Settings Completed         | -               |
| event_id.iaas.nodegroup.set_cluster_autoscaler.failed     | Change Autoscaler Settings Failed            | -               |
| event_id.iaas.cluster.api_ep_ipacl_update.start           | Update Cluster API endpoint IP ACL Started   | -               |
| event_id.iaas.cluster.api_ep_ipacl_update.end             | Update Cluster API endpoint IP ACL Completed | -               |
| event_id.iaas.cluster.api_ep_ipacl_update.failed          | Update Cluster API endpoint IP ACL Failed    | -               |
| event_id.iaas.cluster.update_sgw.start                    | Change SGW Started                           | -               |
| event_id.iaas.cluster.update_sgw.end                      | Change SGW Completed                         | -               |
| event_id.iaas.cluster.update_sgw.failed                   | Change SGW Failed                            | -               |
| event_id.iaas.nodegroup.update_extra_volume.end           | Additional block storage update completed    | -               |
| event_id.iaas.nodegroup.update_extra_volume.fail          | Additional block storage update failed       | -               |
| event_id.iaas.nodegroup.update_extra_volume.start         | Additional block storage update started      | -               |
| event_id.iaas.nodegroup.update_extra_security_group.end   | Additional security group update completed   | -               |
| event_id.iaas.nodegroup.update_extra_security_group.fail  | Additional security group update failed      | -               |
| event_id.iaas.nodegroup.update_extra_security_group.start | Additional security group update started     | -               |
| event_id.iaas.cluster.update_nks_registry.end             | NKS registry update completed                | -               |
| event_id.iaas.cluster.update_nks_registry.fail            | NKS registry update failed                   | -               |
| event_id.iaas.cluster.update_nks_registry.start           | NKS registry update started                  | -               |
| event_id.iaas.cluster.update_k8s_args.start               | K8S Audent Update Started                    | -               |
| event_id.iaas.cluster.update_k8s_args.end                 | K8S Audent Update Completed                  | -               |
| event_id.iaas.cluster.update_k8s_args.failed              | K8S Audent Update Failed                     | -               |
| event_id.iaas.cluster.update_oidc_args.start              | OIDC Audent Update Started                   | -               |
| event_id.iaas.cluster.update_oidc_args.end                | OIDC Audent Update Completed                 | -               |
| event_id.iaas.cluster.update_oidc_args.failed             | OIDC Audent Update Failed                    | -               |
| event_id.iaas.cluster.update_vm_auth_key.start            | Keypair Update Started                       | -               |
| event_id.iaas.cluster.update_vm_auth_key.end              | Keypair Update Completed                     | -               |
| event_id.iaas.cluster.update_vm_auth_key.failed           | Keypair Update Failed                        | -               |

#### Block Storage (Infrastructure:BLOCK_STORAGE)

| Event ID                             | Event Name                        | Event Type      |
| ------------------------------------ | --------------------------------- | --------------- |
| event_id.iaas.volume.create_end      | Create Block Storage Completed    | Create Resource |
| event_id.iaas.volume.transfer_accept |                                   | Create Resource |
| event_id.iaas.volume.copy_end        | Replicate Block Storage Completed | Create Resource |
| event_id.iaas.volume.delete_end      | Delete Block Storage Completed    | Delete Resource |
| event_id.iaas.volume.transfer_create |                                   | Delete Resource |
| event_id.iaas.volume.update_end      | Modify Block Storage Completed    | Modify Resource |

#### Floating IP (Infrastructure:FLOATING_IP)

| Event ID                             | Event Name                   | Event Type      |
| ------------------------------------ | ---------------------------- | --------------- |
| event_id.iaas.floating_ip.create_end | Create Floating IP Completed | Create Resource |
| event_id.iaas.floating_ip.update_end | Update Floating IP Completed | Modify Resource |
| event_id.iaas.floating_ip.delete_end | Delete Floating IP Completed | Delete Resource |

#### Flow Log Logger (Infrastructure:FLOW_LOG_LOGGER)

| Event ID                                | Event Name                       | Event Type      |
| --------------------------------------- | -------------------------------- | --------------- |
| event_id.iaas.flowlog_logger.create_end | Create Flow Log Logger Completed | Create Resource |
| event_id.iaas.flowlog_logger.update_end | Modify Flow Log Logger Completed | Modify Resource |
| event_id.iaas.flowlog_logger.delete_end | Delete Flow Log Logger Completed | Delete Resource |

#### Image (Infrastructure:IMAGE)

| Event ID                            | Event Name             | Event Type      |
| ----------------------------------- | ---------------------- | --------------- |
| event_id.iaas.image.create_end      | Create Image Completed | Create Resource |
| event_id.iaas.image.transfer_accept |                        | Create Resource |
| event_id.iaas.image.delete_end      | Delete Image Completed | Delete Resource |
| event_id.iaas.image.transfer_create |                        | Delete Resource |
| event_id.iaas.image.update_end      | Modify Image Completed | Modify Resource |

#### IMAGE TEMPLATE (Infrastructure:ImageTemplate)

| Event ID                                  | Event Name            | Event Type      |
| ----------------------------------------- | --------------------- | --------------- |
| event_id.iaas.image_template.create       | Create Image Template | Create Resource |
| event_id.iaas.image_template.update       | Modify Image Template | Modify Resource |
| event_id.iaas.image_template.build        | Build Image           | -               |
| event_id.iaas.image_template.cancel_build | Cancel Image Build    | -               |
| event_id.iaas.image_template.delete       | Delete Image Template | Delete Resource |

#### Load Balancer (Infrastructure:LOAD_BALANCER)

| Event ID                              | Event Name                                 | Event Type      |
| ------------------------------------- | ------------------------------------------ | --------------- |
| event_id.iaas.loadbalancer.create_end | Create Load Balancer Completed             | Create Resource |
| event_id.iaas.loadbalancer.update_end | Change Load Balancer Information Completed | Modify Resource |
| event_id.iaas.loadbalancer.delete_end | Delete Load Balancer Completed             | Delete Resource |

#### NAS Storage (Infrastructure:NAS.STORAGE)

| Event ID                                       | Event Name           | Event Type      |
| ---------------------------------------------- | -------------------- | --------------- |
| event_id.iaas.nas.volume.create                | Create NAS Volume    | Create Resource |
| event_id.iaas.nas.volume.update_end            |                      | Modify Resource |
| event_id.iaas.nas.volume.delete_end            |                      | Delete Resource |
| event_id.iaas.nas.snapshot.create              | Create NAS Snapshot  | -               |
| event_id.iaas.nas.snapshot.delete              | Delete NAS Snapshot  | -               |
| event_id.iaas.nas.snapshot.restore             | Restore NAS Snapshot | -               |
| event_id.iaas.nas.replication.set              |                      | -               |
| event_id.iaas.nas.replication.unset            |                      | -               |
| event_id.iaas.nas.replication.start            |                      | -               |
| event_id.iaas.nas.replication.stop             |                      | -               |
| event_id.iaas.nas.replication.change_direction |                      | -               |
| event_id.iaas.nas.subnet.attach                |                      | -               |
| event_id.iaas.nas.subnet.detach                |                      | -               |

#### NAT Gateway (Infrastructure:NAT_GATEWAY)

| Event ID                             | Event Name                   | Event Type      |
| ------------------------------------ | ---------------------------- | --------------- |
| event_id.iaas.nat_gateway.create_end | Create NAT Gateway Completed | Create Resource |
| event_id.iaas.nat_gateway.update_end | Change NAT Gateway Completed | Modify Resource |
| event_id.iaas.nat_gateway.delete_end | Delete NAT Gateway Completed | Delete Resource |

#### Private DNS Zone (Infrastructure:PRIVATE_DNS_ZONE)

| Event ID                                  | Event Name                        | Event Type      |
| ----------------------------------------- | --------------------------------- | --------------- |
| event_id.iaas.private_dns.zone.create_end | Create Private DNS Zone Completed | Create Resource |
| event_id.iaas.private_dns.zone.update_end | Modify Private DNS Zone Completed | Modify Resource |
| event_id.iaas.private_dns.zone.delete_end | Delete Private DNS Zone Completed | Delete Resource |

#### Block Storage Snapshot (Infrastructure:SNAPSHOT)

| Event ID                          | Event Name                              | Event Type      |
| --------------------------------- | --------------------------------------- | --------------- |
| event_id.iaas.snapshot.create_end | Create Block Storage Snapshot Completed | Create Resource |
| event_id.iaas.snapshot.delete_end | Delete Block Storage Snapshot Completed | Delete Resource |

#### Storage Gateway (Infrastructure:STORAGE_GATEWAY.GATEWAY)

| Event ID                                         | Event Name | Event Type      |
| ------------------------------------------------ | ---------- | --------------- |
| event_id.iaas.storage_gateway.gateway.create     |            | Create Resource |
| event_id.iaas.storage_gateway.gateway.update_end |            | Modify Resource |
| event_id.iaas.storage_gateway.gateway.delete_end |            | Delete Resource |
| event_id.iaas.storage_gateway.share.create       |            | -               |
| event_id.iaas.storage_gateway.share.update_end   |            | -               |
| event_id.iaas.storage_gateway.share.delete_end   |            | -               |

#### Transit Hub (Infrastructure:TRANSIT_HUB)

| Event ID                             | Event Name                   | Event Type      |
| ------------------------------------ | ---------------------------- | --------------- |
| event_id.iaas.transit_hub.create_end | Create Transit Hub Completed | Create Resource |
| event_id.iaas.transit_hub.update_end | Modify Transit Hub Completed | Modify Resource |
| event_id.iaas.transit_hub.delete_end | Delete Transit Hub Completed | Delete Resource |

#### Transit Hub Attachment (Infrastructure:TRANSIT_HUB_ATTACHMENT)

| Event ID                                        | Event Name                              | Event Type      |
| ----------------------------------------------- | --------------------------------------- | --------------- |
| event_id.iaas.transit_hub_attachment.create_end | Create Transit Hub Attachment Completed | Create Resource |
| event_id.iaas.transit_hub_attachment.update_end | Modify Transit Hub Attachment Completed | Modify Resource |
| event_id.iaas.transit_hub_attachment.delete_end | Delete Transit Hub Attachment Completed | Delete Resource |

#### VPC (Infrastructure:VPC)

| Event ID                     | Event Name                       | Event Type      |
| ---------------------------- | -------------------------------- | --------------- |
| event_id.iaas.vpc.create_end | Create VPC Completed             | Create Resource |
| event_id.iaas.vpc.update_end | Change VPC Information Completed | Modify Resource |
| event_id.iaas.vpc.delete_end | Delete VPC Completed             | Delete Resource |

#### INSTANCE (INSTANCE)

| Event ID                                   | Event Name                          | Event Type      |
| ------------------------------------------ | ----------------------------------- | --------------- |
| event_id.iaas.instance.create_end          | Create Instance Completed           | Create Resource |
| event_id.iaas.instance.delete_end          | Delete Instance Completed           | Delete Resource |
| event_id.iaas.instance.update              | Change Instance Information         | Modify Resource |
| event_id.iaas.instance_action.reboot_end   | Reboot Instance Completed           | -               |
| event_id.iaas.instance_action.resize_end   | Change Instance Type Completed      | -               |
| event_id.iaas.instance_action.start_end    | Start Stopped Instance Completed    | -               |
| event_id.iaas.instance_action.stop_end     | Stop Instance Completed             | -               |
| event_id.iaas.instance_action.shelve_end   | Terminate Instance Completed        | -               |
| event_id.iaas.instance_action.unshelve_end | Start Terminated Instance Completed | -               |

#### WORKLOAD (NHNContainerService:Workload)

| Event ID                                                | Event Name                                        | Event Type      |
| ------------------------------------------------------- | ------------------------------------------------- | --------------- |
| event_id.iaas.ncs.workload_create.start                 | Create Workload Started                           | Create Resource |
| event_id.iaas.ncs.workload_create.failed                | Create Workload Failed                            | Delete Resource |
| event_id.iaas.ncs.workload.delete                       | Delete Workload                                   | Delete Resource |
| event_id.iaas.ncs.workload.stop                         | Stop Workload                                     | Modify Resource |
| event_id.iaas.ncs.workload_restart.start                | Restart Workload Started                          | Modify Resource |
| event_id.iaas.ncs.workload_template_update.start        | Change Workload Template Started                  | Modify Resource |
| event_id.iaas.ncs.workload_desired_update.start         | Change Number of Workload Task Requests Start     | Modify Resource |
| event_id.iaas.ncs.workload_schedule.update              | Change Scheduled Run                              | Modify Resource |
| event_id.iaas.ncs.workload_loadbalancer_update.start    | Change Workload Load Balancer Start               | Modify Resource |
| event_id.iaas.ncs.workload_create.end                   | Create Workload Completed                         | -               |
| event_id.iaas.ncs.workload_restart.end                  | Restart Workload Completed                        | -               |
| event_id.iaas.ncs.workload_restart.failed               | Restart Workload Failed                           | -               |
| event_id.iaas.ncs.workload_template_update.end          | Change Workload Template Completed                | -               |
| event_id.iaas.ncs.workload_template_update.failed       | Change Workload Template Failed                   | -               |
| event_id.iaas.ncs.workload_desired_update.end           | Change Number of Workload Task Requests Completed | -               |
| event_id.iaas.ncs.workload_desired_update.failed        | Change Number of Workload Task Requests Failed    | -               |
| event_id.iaas.ncs.workload_loadbalancer_update.end      | Change Workload Load Balancer Completed           | -               |
| event_id.iaas.ncs.workload_active_deadline.update       | Change Schedule Termination                       | -               |
| event_id.iaas.ncs.workload_internal_loadbalancer.update | Change Workload Internal Load Balancer            | -               |
| event_id.iaas.ncs.workload_description.update           | Change Workload Description                       | -               |

### Object Storage

#### CONTAINER (ObjectStorage:Container)

| Event ID                                          | Event Name                            | Event Type      |
| ------------------------------------------------- | ------------------------------------- | --------------- |
| event_id.object_storage.container.create          | Create Containers                     | Create Resource |
| event_id.object_storage.container.delete          | Delete Containers                     | Delete Resource |
| event_id.object_storage.container.metadata.update | Register/Modify Container Metadata    | -               |
| event_id.object_storage.container.sync.enable     | Set Container Replication             | -               |
| event_id.object_storage.container.sync.update     | Change Container Replication Settings | -               |
| event_id.object_storage.container.sync.disable    | Unset Container Replication           | -               |

### DataQuery

#### Cluster (DataQuery:Cluster)

| Event ID                           | Event Name  | Event Type      |
| ---------------------------------- | ----------- | --------------- |
| event_id.dataquery.cluster_on      | Cluster On  | Create Resource |
| event_id.dataquery.cluster_off     | Cluster Off | Delete Resource |
| event_id.dataquery.kr3.cluster_on  |             | Create Resource |
| event_id.dataquery.kr3.cluster_off |             | Delete Resource |
| event_id.dataquery.pj1.cluster_on  |             | Create Resource |
| event_id.dataquery.pj1.cluster_off |             | Delete Resource |

### DNS Plus

#### DNS Plus GSLB (DNSPlus:GSLB)

| Event ID                     | Event Name  | Event Type      |
| ---------------------------- | ----------- | --------------- |
| event_id.dnsplus.gslb.create | Create GSLB | Create Resource |
| event_id.dnsplus.gslb.update | Modify GSLB | Modify Resource |
| event_id.dnsplus.gslb.delete | Delete GSLB | Delete Resource |

#### DNS Plus Health Check (DNSPlus:HealthCheck)

| Event ID                             | Event Name           | Event Type      |
| ------------------------------------ | -------------------- | --------------- |
| event_id.dnsplus.health_check.create | Create Health Checks | Create Resource |
| event_id.dnsplus.health_check.update | Modify Health Checks | Modify Resource |
| event_id.dnsplus.health_check.delete | Delete Health Checks | Delete Resource |

#### DNS Plus Pool (DNSPlus:Pool)

| Event ID                     | Event Name   | Event Type      |
| ---------------------------- | ------------ | --------------- |
| event_id.dnsplus.pool.create | Create Pools | Create Resource |
| event_id.dnsplus.pool.update | Modify Pools | Modify Resource |
| event_id.dnsplus.pool.delete | Delete Pools | Delete Resource |

#### DNS Plus Zone (DNSPlus:Zone)

| Event ID                     | Event Name      | Event Type      |
| ---------------------------- | --------------- | --------------- |
| event_id.dnsplus.zone.create | Create DNS Zone | Create Resource |
| event_id.dnsplus.zone.update | Modify DNS Zone | Modify Resource |
| event_id.dnsplus.zone.delete | Delete DNS Zone | Delete Resource |
