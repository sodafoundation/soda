# SODA ODF Navarino v1.8.0 Release - Dec 2022

## Release Summary :
SODA Open Data Framework (ODF) Navarino v1.8.0 is released with backup and restore features of container data protection for Kubernetes, enhanced features for heterogeneous storage performance monitoring, and multicloud data management features

Navarino : New start to explore greater heights!
(Navarino is a Chilean island popular for its trekking trails and beautiful landscapes.) 
 
Please find a summary of key projects below. Please note, the new projects are under design/development and will have initial releases in the upcoming releases.

## SODA Framework Projects:
 - Terra is a universal SDS controller for connecting storage to Kubernetes, OpenStack, and VMware environments
 - Delfin provides a single unified view of storage performance for heterogeneous storage infrastructure
 - Strato simplifies hybrid and multicloud solutions by using a single S3-compatible interface to connect to public cloud storage
 - Kahu is a new project to streamline data protection for Kubernetes and application data
 - Como is a newly proposed virtual data lake project to provide seamless access to data stored in different clouds


## SODA ODF Navarino v1.8.0 Release Highlights:
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
 - SODA Navarino Release v1.8.0 - Please check [here](https://github.com/sodafoundation/soda/releases/tag/v1.8.0)

## Previous Release :
SODA ODF Navarino release is an incremental release on top of SODA ODF Madagascar v1.7.0 release by SODA Foundation.
The earlier stable release Madagascar, you can get [here](https://github.com/sodafoundation/soda/releases/tag/v1.7.0).

