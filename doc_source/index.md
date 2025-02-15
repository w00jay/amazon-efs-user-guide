# Amazon Elastic File System User Guide

-----
*****Copyright &copy; Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in 
     connection with any product or service that is not Amazon's, 
     in any manner that is likely to cause confusion among customers, 
     or in any manner that disparages or discredits Amazon. All other 
     trademarks not owned by Amazon are the property of their respective
     owners, who may or may not be affiliated with, connected to, or 
     sponsored by Amazon.

-----
## Contents
+ [What is Amazon Elastic File System?](whatisefs.md)
+ [Amazon EFS: How it works](how-it-works.md)
+ [Setting Up](setting-up.md)
+ [Getting started with Amazon Elastic File System](getting-started.md)
   + [Step 1: Create your Amazon EFS file system](gs-step-two-create-efs-resources.md)
   + [Step 2: Create your EC2 resources and launch your EC2 instance](gs-step-one-create-ec2-resources.md)
   + [Step 3: Transfer files to Amazon EFS using AWS DataSync](gs-step-four-sync-files.md)
   + [Step 4: Clean up resources and protect your AWS account](gs-step-five-cleanup.md)
+ [EFS storage classes](storage-classes.md)
+ [Working with Amazon EFS resources](creating-using.md)
   + [Resource IDs](resource-ids.md)
   + [Creating Amazon EFS file systems](creating-using-create-fs.md)
   + [Deleting an Amazon EFS file system](delete-efs-fs.md)
   + [Creating and managing mount targets](accessing-fs.md)
   + [Creating security groups](accessing-fs-create-security-groups.md)
   + [Creating file system policies](create-file-system-policy.md)
   + [Creating and deleting access points](create-access-point.md)
   + [Tagging resources](manage-fs-tags.md)
+ [Using file systems in Amazon EFS](using-fs.md)
+ [Using the amazon-efs-utils Tools](using-amazon-efs-utils.md)
   + [Overview](overview-amazon-efs-utils.md)
   + [Using AWS Systems Manager to automatically install or update Amazon EFS clients](manage-efs-utils-with-aws-sys-manager.md)
   + [Manually installing the Amazon EFS client](installing-amazon-efs-utils.md)
   + [Installing botocore](install-botocore.md)
   + [Upgrading stunnel](upgrading-stunnel.md)
+ [Mounting EFS file systems](mounting-fs.md)
   + [Mounting file systems using the EFS mount helper](efs-mount-helper.md)
   + [Additional mounting considerations](mounting-fs-mount-cmd-general.md)
   + [Troubleshooting AMI and kernel versions](ami-kernel-versions-troubleshooting.md)
+ [Transferring data into and out of Amazon EFS](transfer-data-to-efs.md)
   + [Using AWS DataSync to transfer data in Amazon EFS](trnsfr-data-using-datasync.md)
   + [Using AWS Transfer Family to access files in your Amazon EFS file system](using-aws-transfer-integration.md)
+ [Managing Amazon EFS file systems](managing.md)
   + [Managing file system network accessibility](manage-fs-access.md)
   + [Managing file system throughput](managing-throughput.md)
   + [Amazon EFS lifecycle management](lifecycle-management-efs.md)
   + [Managing access to encrypted file systems](managing-encrypt.md)
   + [Metering: How Amazon EFS reports file system and object sizes](metered-sizes.md)
   + [Managing Amazon EFS file system costs using AWS Budgets](use-aws-budgets-efs-cost.md)
   + [File system status](file-system-state.md)
+ [Monitoring Amazon EFS](monitoring_overview.md)
   + [Monitoring tools](monitoring_automated_manual.md)
   + [Monitoring Amazon EFS with Amazon CloudWatch](monitoring-cloudwatch.md)
      + [Amazon CloudWatch metrics for Amazon EFS](efs-metrics.md)
      + [How do I use Amazon EFS metrics?](how_to_use_metrics.md)
      + [Using metric math with Amazon EFS](monitoring-metric-math.md)
      + [Monitoring EFS file system mount status](how-to-monitor-mount-status.md)
      + [Accessing CloudWatch metrics](accessingmetrics.md)
      + [Creating CloudWatch alarms to monitor Amazon EFS](creating_alarms.md)
   + [Logging Amazon EFS API Calls with AWS CloudTrail](logging-using-cloudtrail.md)
+ [Amazon EFS performance](performance.md)
   + [Amazon EFS performance tips](performance-tips.md)
+ [Backing up your Amazon EFS file systems](efs-backup-solutions.md)
   + [Using AWS Backup to back up and restore Amazon EFS file systems](awsbackup.md)
+ [Amazon EFS replication](efs-replication.md)
+ [Amazon Elastic File System Walkthroughs](walkthroughs.md)
   + [Walkthrough: Create an Amazon EFS file system and mount it on an Amazon EC2 instance using the AWS CLI](wt1-getting-started.md)
      + [Step 1: Create Amazon EC2 resources](wt1-create-ec2-resources.md)
      + [Step 2: Create Amazon EFS resources](wt1-create-efs-resources.md)
      + [Step 3: Mount the file system on the EC2 instance and test](wt1-test.md)
      + [Step 4: Clean up](wt1-clean-up.md)
   + [Walkthrough: Set up an Apache web server and serve Amazon EFS files](wt2-apache-web-server.md)
   + [Walkthrough: Create Writable Per-User Subdirectories and Configure Automatic Remounting on Reboot](accessing-fs-nfs-permissions-per-user-subdirs.md)
   + [Walkthrough: Create and mount a file system on-premises with AWS Direct Connect and VPN](efs-onpremises.md)
   + [Walkthrough: Mount a File System from a Different VPC](efs-different-vpc.md)
   + [Walkthrough: Enforcing Encryption on an Amazon EFS File System at Rest](efs-enforce-encryption.md)
   + [Walkthrough: Enable root squashing using IAM authorization for NFS clients](enable-root-squashing.md)
+ [Security in Amazon EFS](security-considerations.md)
   + [Data encryption in Amazon EFS](encryption.md)
      + [Encrypting data at rest](encryption-at-rest.md)
      + [Encrypting data in transit](encryption-in-transit.md)
   + [Identity and access management for Amazon EFS](auth-and-access-control.md)
      + [Overview of managing access permissions to your Amazon EFS resources](access-control-overview.md)
      + [Controlling access to the EFS API](access-control-managing-permissions.md)
      + [Using IAM to control file system data access](iam-access-control-nfs-efs.md)
      + [Using IAM to enforce creating encrypted file systems](using-iam-to-enforce-encryption-at-rest.md)
      + [Blocking public access](access-control-block-public-access.md)
      + [Using the Amazon EFS Service-Linked Role](using-service-linked-roles.md)
   + [Controlling network access to Amazon EFS file systems for NFS clients](NFS-access-control-efs.md)
      + [Using VPC security groups for Amazon EC2 instances and mount targets](network-access.md)
      + [Source ports for working with EFS](source-ports.md)
      + [Security considerations for network access](sg-information.md)
      + [Working with Interface VPC Endpoints in Amazon EFS](efs-vpc-endpoints.md)
   + [Working with users, groups, and permissions at the Network File System (NFS) Level](accessing-fs-nfs-permissions.md)
      + [File and directory permissions](user-and-group-permissions.md)
   + [Working with Amazon EFS Access Points](efs-access-points.md)
   + [Logging and Monitoring in Amazon EFS](logging-monitoring.md)
   + [AWS managed policies for Amazon EFS](security-iam-awsmanpol.md)
   + [Compliance Validation for Amazon Elastic File System](SERVICENAME-compliance.md)
   + [Resilience in Amazon Elastic File System](disaster-recovery-resiliency.md)
   + [Amazon Elastic File System Network Isolation](network-isolation.md)
+ [Amazon EFS quotas and limits](limits.md)
+ [Troubleshooting Amazon EFS](troubleshooting.md)
   + [Troubleshooting Amazon EFS: General Issues](troubleshooting-efs-general.md)
   + [Troubleshooting File Operation Errors](troubleshooting-efs-fileop-errors.md)
   + [Troubleshooting AMI and Kernel Issues](troubleshooting-efs-ami-kernel.md)
   + [Troubleshooting Mount Issues](troubleshooting-efs-mounting.md)
   + [Troubleshooting Encryption](troubleshooting-efs-encryption.md)
+ [Amazon EFS API](api-reference.md)
   + [Actions](API_Operations.md)
      + [CreateAccessPoint](API_CreateAccessPoint.md)
      + [CreateFileSystem](API_CreateFileSystem.md)
      + [CreateMountTarget](API_CreateMountTarget.md)
      + [CreateReplicationConfiguration](API_CreateReplicationConfiguration.md)
      + [CreateTags](API_CreateTags.md)
      + [DeleteAccessPoint](API_DeleteAccessPoint.md)
      + [DeleteFileSystem](API_DeleteFileSystem.md)
      + [DeleteFileSystemPolicy](API_DeleteFileSystemPolicy.md)
      + [DeleteMountTarget](API_DeleteMountTarget.md)
      + [DeleteReplicationConfiguration](API_DeleteReplicationConfiguration.md)
      + [DeleteTags](API_DeleteTags.md)
      + [DescribeAccessPoints](API_DescribeAccessPoints.md)
      + [DescribeAccountPreferences](API_DescribeAccountPreferences.md)
      + [DescribeBackupPolicy](API_DescribeBackupPolicy.md)
      + [DescribeFileSystemPolicy](API_DescribeFileSystemPolicy.md)
      + [DescribeFileSystems](API_DescribeFileSystems.md)
      + [DescribeLifecycleConfiguration](API_DescribeLifecycleConfiguration.md)
      + [DescribeMountTargets](API_DescribeMountTargets.md)
      + [DescribeMountTargetSecurityGroups](API_DescribeMountTargetSecurityGroups.md)
      + [DescribeReplicationConfigurations](API_DescribeReplicationConfigurations.md)
      + [DescribeTags](API_DescribeTags.md)
      + [ListTagsForResource](API_ListTagsForResource.md)
      + [ModifyMountTargetSecurityGroups](API_ModifyMountTargetSecurityGroups.md)
      + [PutAccountPreferences](API_PutAccountPreferences.md)
      + [PutBackupPolicy](API_PutBackupPolicy.md)
      + [PutFileSystemPolicy](API_PutFileSystemPolicy.md)
      + [PutLifecycleConfiguration](API_PutLifecycleConfiguration.md)
      + [TagResource](API_TagResource.md)
      + [UntagResource](API_UntagResource.md)
      + [UpdateFileSystem](API_UpdateFileSystem.md)
   + [Data Types](API_Types.md)
      + [AccessPointDescription](API_AccessPointDescription.md)
      + [BackupPolicy](API_BackupPolicy.md)
      + [CreationInfo](API_CreationInfo.md)
      + [Destination](API_Destination.md)
      + [DestinationToCreate](API_DestinationToCreate.md)
      + [FileSystemDescription](API_FileSystemDescription.md)
      + [FileSystemSize](API_FileSystemSize.md)
      + [LifecyclePolicy](API_LifecyclePolicy.md)
      + [MountTargetDescription](API_MountTargetDescription.md)
      + [PosixUser](API_PosixUser.md)
      + [ReplicationConfigurationDescription](API_ReplicationConfigurationDescription.md)
      + [ResourceIdPreference](API_ResourceIdPreference.md)
      + [RootDirectory](API_RootDirectory.md)
      + [Tag](API_Tag.md)
+ [Additional information for Amazon EFS](appendices.md)
   + [Backing up Amazon EFS file systems using AWS Data Pipeline](alternative-efs-backup.md)
   + [Mounting file systems without the EFS mount helper](mounting-fs-old.md)
      + [Recommended NFS mount options](mounting-fs-nfs-mount-settings.md)
      + [Mounting on Amazon EC2 with a DNS name](mounting-fs-mount-cmd-dns-name.md)
      + [Mounting with an IP address](mounting-fs-mount-cmd-ip-addr.md)
+ [Document History](document-history.md)