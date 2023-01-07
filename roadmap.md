# SODA Releases Roadmap

<img src="https://sodafoundation.io/wp-content/uploads/2020/01/SODA_logo_outline_color_800x800.png" width="200" height="200">

## Introduction
SODA Foundation release will be an umbrella release comprising of multiple projects viz., SODA Framework Projects and other participating projects(if any)

SODA Foundation release version number is not linked to any of the projects included in the  release. Please refer the first SODA Foundation release [here](https://github.com/sodafoundation/releases/releases/tag/v0.20.0)

Notes:
SODA Framework Projects: Maintained and owned by SODA Foundation
SODA Eco Projects: Projects joined formally for collaborative development and integration with SODA Framework Projects. Projects are owned by the respective community/organization.

## Release Roadmap and Scope
The SODA Releases are made at least once in 6 months (or on demand)
# 2023
## May/June 2023 Scope ('O' Release) (Under planning)
 - Container Data Management
   - Replication & Failover
   - Restic / S3 support
   - Performance optimization 
 - Heterogeneous Monitoring
   - Enhanced features and drivers
   - Kubernetes native monitoring
 - Multicloud Data Management
   - Cloud Metadata Management (Store, Classification, Search..)
   - Support externally provisioned storages 
 - Data Lake Project kick start with S3 poc 
 - SODA Experience
   - Decoupled Dashboards for projects
   - Pluggable installers
 - Eco project integrations 


# 2022
## Dec 2022 Scope ('N' Release) (Navarino Release v1.8.0)
 - Container data backup and restore for Kubernetes
   - Storage Provider Framework
   - Pre-Post Hooks for Backup / Restore
   - NFS Provider, CSI Support
 - Heterogeneous SPM with an improved installer
   - New Drivers Support (like MacroSAN, Dell EMC ScaleIO, H3C Unistore, Inspur AS5xxx)
   - Enhanced Installer tested with existing features of heterogeneous storage resource, alert and performance monitoring
- SODA Strato for Multicloud Data Management
  - External metadata management (experimental) for multicloud
  - Enhanced Installer tested with existing features of s3/file/block provisioning, data mobility, and lifecycle management across multiple clouds
- SODA Experience & QA
  - Updates for Delfin dashboard changes to support new devices
  - Delfin fake driver support to Dashboard
  - Testing and bug fixes
  - Separate installers for Delfin, Strato and Kahu
- SODA Support for Ubuntu 20.04 LTS
### The release is available [here](https://github.com/sodafoundation/soda/releases/tag/v1.8.0)

## May 2022 Scope ('M' Release) (Madagascar Release v1.7.0 ) 
 - Heterogeneous Performance Monitoring
   - Centralized Manager for wider integration for more storage models
   - Host mapping support added for IBM SVC, DS8000, Dell EMC VNX Block, Dell EMC VMAX, NetApp, HPE 3PAR, Pure Storage, Fujitsu Eternus, Hitachi VSP etc
   - Performance metrics collection support added for HPE 3PAR, Dell EMC Unity
   - Detailed verification on Ubuntu 20.04 LTS
 - Container Data Protection for Kubernetes
   - Kahu, the new Project for Backup/Restore with Metadata Backup PoC
 - Bug fixes and improvements for Multicloud, Dashboard, Installer and Documentation
### The release is available [here](https://github.com/sodafoundation/soda/releases/tag/v1.7.0)

# 2021
## Q4 2021 Scope ('L' Release) (Lamu Release v1.6.0)
- Enhanced SPM (Storage Performance Monitoring) : Collection, Scheduling etc
- Driver Enhancements for SPM: NetApp, VMAX resource collection, new drivers for more storages (Fujitsu, Hitachi, HPE, IBM and Pure Storage)
- SPM deployment in Kubernetes
- Multicloud OpenAPI Spec Updates

### The release is available [here](https://github.com/sodafoundation/soda/releases/tag/v1.6.0)

## Q3 2021 Scope ('K' Release) (Kalpeni Release v1.5.0)
* Enhanced Heterogeneous Performance Metric Collection Framework with improved job distribution, load balancing, multi processing
* Host Mapping with support group based mapping
* Filesystem metrics Added
* Driver Enhancements for SPM
  * Netapp C mode Performance metric collection
  * EMC VMAX port and controller resources
  * EMC VMAX pool, port and controller metrics collection
* Host mapping from Huawei Oceanstor
* Visualization enhanced
* Multi-Cloud User level storage tiering Fixes

### The release is available [here](https://github.com/sodafoundation/soda/releases/tag/v1.5.0)
  
## Q2 2021 Scope ('J' Release) (Jerba Release v1.4.0) 
* Plug-in support for any CSI driver
* Support multiple concurrent CSI drivers in Kubernetes deployment
* Container data protection framework based on Restic
* Policy-based application-consistent snapshot to cloud
* Storage performance monitoring enhanced with distributed scheduler, host mapping, and additional metrics support
* Storage Service Plan framework for multi-cloud
* Bucket management extended to all major cloud backends

### The release is available [here](https://github.com/sodafoundation/soda/releases/tag/v1.4.0)

## Q1 2021 Scope ('I' Release) (Isabela Release v1.3.0)
* Heterogeneous SPM(Storage Performance Monitoring) with Enhanced Performance Framework
* NAS Resource support
* Upgraded SPM Visualization (along with Grafana integration)
* Multi-cloud HA support
* More Cloud Backends for Data Archival/Restore
* Cold Storage Support
* Cloud Native storage with more CSI drivers.
* More Storage Backends (On-prem/Cloud)

### The release is available [here](https://github.com/sodafoundation/soda/releases/tag/v1.3.0)

*Please contact us in [SODA Slack](https://sodafoundation.io/slack/) or raise [issues](https://github.com/sodafoundation/soda/issues) if you have use cases or feature suggestions*

# 2020

## Q4 2020 Scope ('H' Release) - Hawaii Release v1.2.0 
Focus on E2E use cases.
- Heterogeneous SPM with Anomaly Detection
- SPM Visualization (Grafana integration)
- Resource Monitoring for Port, Controller, and Disk
- Enhanced Multi-cloud File & Block Store
- Hybrid Cloud Data Archival/Restore
- Data Replication & CSI Plug and play use cases
- More Storage Drivers
### The release is available [here](https://github.com/sodafoundation/soda/releases/tag/v1.2.0)

## Q3 2020 Scope ('G' Release) - Greenland Release v1.1.0 
- Heterogeneous Storage Performance Monitoring; Enhance resource and alert features
- Prometheus Integration with Storage Performance Monitoring
- SODA CSI plug-and-play
- Multi-cloud file services added support for GCP in addition to AWS and Azure; enhance block service feature
- SODA Edge Experiment
- File Support for NetApp ONTAP and more South Bound Drivers
- SODA Experience (Installer, Dashboard and Documentation) updates
### The release is available [here](https://github.com/sodafoundation/soda/releases/tag/v1.1.0)

## Q2 2020 Scope ('F' Release) - Faroe Release v1.0.0
- First Major Version (1.0.0) release
- SODA Infrastructure Manager (SIM) (Storage Resource, Alarm)
- Multicloud: Dashboard fix for S3 compatible API, File/Block Service Support Design and Prototypes, Alibaba backend support added
- Installer & Documentations: Installer configurable and improved to handle all projects; all the facing documents are updated
- API Specification v0.1 Draft for File/block(on prem) , Multicloud and SIM
- Orchestartion and Anomaly Detection: No Change
- github community healthfiles streamlined for SODA Core projects
- CSI Plug and Play Prototype (experimental)
### The release is available [here](https://github.com/sodafoundation/releases/releases/tag/v1.0.0)

## Q1 2020 Scope ('E' Release) - Elba Release v0.20.0
- Projects Migration from OpenSDS
- Project Reorganization (Decouple API, Controller and DOCK, Refine interfaces)
- S3 Compatible APIs in Multicloud
- Quality improvements across the project (Testing, Bug Fixes)
- Update installer and documentation for the migraiton of the projects and reorganization
- CSI Plug and play design
- Streaming use case demo using Multicloud
### The release is available [here](https://github.com/sodafoundation/releases/releases/tag/v0.20.0)

## Older Releases Information (2017-2019)
_NOTE: The older release roadmap from 2017-2019 under OpenSDS(previous name for SODA Foundation) is shown below
<img src="https://github.com/sodafoundation/documentation/blob/master/content/releases/releases2017-2019.png">
