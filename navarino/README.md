# SODA ODF Navarino v1.7.1 RC1 Release - Dec 2022

## Release Summary :
SODA Open Data Framework (ODF) Navarino v1.7.1 release comes with a matured Kahu, our new project for data back & restore for Kubernetes based container application deployment. Currently it supports data protection features like Volume backup & restore using LVM, pre hooks and post hooks execution for backup & restore, CSI volume snapshots,  etc.
Project delfin, SODA solution for heterogeneous storage performance monitoring, comes with more storage models support and improvements.
Projects like multicloud, dashboard and installer come with bug fixes and improvements. 

Navarino : Together we meet the challenges and grow!
(The rugged Navarino Island in Chile’s Tierra del Fuego archipelago is home to some of the most spectacular scenery in South America)
 
Thanks to all the new contributors to SODA Projects from SODACODE2022!
 
Please find a summary of key projects below. Please note, the new projects are under design/development and will have initial releases in the upcoming releases.

## SODA Framework Projects:
 - Terra is a universal SDS controller for connecting storage to Kubernetes, OpenStack, and VMware environments
 - Delfin provides a single unified view of storage performance for heterogeneous storage infrastructure
 - Strato simplifies hybrid and multicloud solutions by using a single S3-compatible interface to connect to public cloud storage
 - Kahu is a new project to streamline data protection for Kubernetes and application data
 - Como is a newly proposed virtual data lake project to provide seamless access to data stored in different clouds


## SODA ODF Navarino v1.7.1 RC1 Release Highlights:
 - Individual installer for Strato, Delfin with individual Dashboard installation
 - SODA Support for Ubuntu 20.04 LTS
 - SODA Kahu supports data protection features like, 
    * Data protection solution for Kubernetes applications. 
    * Backup scope 
       - cluster level 
       - namespace level 
       - label selector 
       - specific kind 
       - a specific resource instance
    * Support storage provider framework which enable users to add plug-able metadata and volume driver for backup/restore
    * In tree support of NFS provider metadata driver
    *  Execution of pre and post hooks during backup and restore
    * E2E test framework design and implementation
    * E2E test case integration for key backup/restore usecases 
    * Documentation enhancements and API Reference

 - SODA Delfin enhancements and feature additions
   - Added support for Storage Devices like MacroSAN, Dell EMC ScaleIO, H3C Unistore, Inspur AS5xxx, etc 
   - Added support for Ubuntu 20.04 deployment
   - Enhanced Delfin installer to support Ansible installation locally with Visualization Tools and Dashboard
  - Fixes and updates in the Framework & Driver code, OpenAPI Spec, Documentation etc.
- Bug fixes and improvements for Strato, Delfin, Dashboard, Installer and Documentation


## Release Link
 - SODA Navarino Release v1.7.1 RC1 - Please check [here](https://github.com/sodafoundation/soda/releases/tag/v1.7.1)

## Previous Release :
SODA ODF Navarino RC1 release is an incremental release on top of SODA ODF Madagascar v1.7.0 release by SODA Foundation.
The earlier stable release Madagascar, you can get [here](https://github.com/sodafoundation/soda/releases/tag/v1.7.0).

