# Multi-Cloud

# March 18

### Aws and Azure cloud


**Backup and Archival**

- Backup is taken for recovering from failures quickly whereas archiving is done to recover from disasters & it will take more time.
- Cloud is all about using some one else’s hardware
- AWS and Azure offer Backup and Archival solutions

**What are different storage needs for organization**

- Disk Storage: A disk typically is attached to a server
- Network Storage: A disk that is typically mounted on multiple systems with in a network
- Blob Storage: This storage refers to accessing the data over internet with urls

**Disks**
- A disk typically needs a filesystem to be identified by OS. Windows supports NTFS and linux has many filesystems (ext4, xfs,..)
- In window a disk can be partitioned and drives (C, D..) can be created
- In linux, a disk can be partitioned and mounted

![image](https://github.com/user-attachments/assets/4bfb306f-b9d4-430c-ae82-eb6239fd4f18)


# March 19

### Disk Performance
- **Hardware Types**: Disks have the following hardware types
     - Magnetic Disks
     - HDD (Hard disk Drive)
     - SSD (Solid State Drives)
- To measure the harddisk performance we have two units
     - IOPS (I/O per second):
     - Throughput

![image](https://github.com/user-attachments/assets/7d7b49d0-056f-4fa9-a3e8-52f407b11d01)

#### Units of measurement:
- 1 kibi (kib) = 1024 bytes
- 1 kb = 1000 bytes
- When you create storage in cloud we get (GiB, MiB, KiB, TiB) options
**Storage Migration is of two Types**

**Online:**
- Agent Based
- Dedicated Hardware (Regular Data Transfers)

**Offline: (One-time)**

### AWS Snowball
- [ Azure](https://directdevops.blog/2025/03/19/multicloud-classroom-notes-19-mar-2025/#) Data Box

#### **Virtualization**
**Explore Virtualization and findout what vmware, kvm and Hyper-V are ?**

- Virtualization is a technology that allows multiple virtual machines (VMs) to run on a single physical hardware system by creating an abstraction layer over the hardware. This enables more efficient use of resources and is foundational for cloud computing. Three prominent virtualization technologies are VMware, KVM (Kernel-based Virtual Machine), and Hyper-V.

**VMware**

- **Overview:** VMware is a leading provider of virtualization and cloud computing software, founded in 1998 and now a subsidiary of Dell Technologies. Its primary product is the VMware hypervisor, which allows multiple VMs to operate on a single physical server, each capable of running its own operating system.

**KVM (Kernel-based Virtual Machine)**

- **Overview:** KVM is an open-source virtualization technology integrated into the Linux kernel. It transforms Linux into a Type 1 hypervisor, allowing it to host multiple isolated VMs.

**Hyper-V**

- **Overview:** Hyper-V is Microsoft’s hardware virtualization product that allows users to create and manage VMs. It is included in Windows Server and some client versions of Windows.


# March 20

## AWS Storage Services
- **Storage Services offered by AWS**

![image](https://github.com/user-attachments/assets/6e8c1674-29c6-4c39-b198-a387bad2198f)

- In addition to the above services we also have EBS (Elastic Block Storage) which is used by virtual machines (EC2 instances)



## Azure Storage Services

- Storage Services offered by [ Azure](https://directdevops.blog/2025/03/20/multicloud-classroom-notes-20-mar-2025/#)

![image](https://github.com/user-attachments/assets/718980e9-e14f-4930-93f2-b64df3590a36)

### Categories

- Disk Storage (Block Storage)
- File Shares (Network Storage)
- Blob Storage
- Hybrid Storage Solutions
- CDN

### Activities

- Managing Storage
- Managing Backups & Archivals
     - Full Backups
     - Incremental Backups

### SnapShot

- This is copy of a disk at a particular time
- Snapshots can be implemented using
    - Terms
    - Latency

![image](https://github.com/user-attachments/assets/358d425d-7f0a-4ac8-abf0-c5ecda4afbc4)


### Global Infra

- [Azure Global infra](https://datacenters.microsoft.com/globe/explore/)
- [AWS Global Infra](https://aws.amazon.com/about-aws/global-infrastructure/)


### Cloud Infra categories

- Region
- Availability Zone
- Edge Locations
- PoP locations
- 5G Zone
- Local Zones (AWS)


# March 22

### Blob Storage

- This is a file [ storage](https://directdevops.blog/2025/03/22/multicloud-classroom-notes-22-mar-2025/#) where
    - you need not deal with filesystems
    - you can access the files over http(s)
    - you can use this for any file types
    - you can treat it is as unlimited storage.
    - individual file size restrictions are applicable (5TB)

**Why do we need this?**

- Google Drive, One Drive, iCloud all of them are internally blob storages.
- All streaming/ott platforms uses blob storages
- Data lakes on Blob storage

**How cloud’s charge for Blob [ Storage](https://directdevops.blog/2025/03/22/multicloud-classroom-notes-22-mar-2025/#) ? Google Cloud Platform training**

- Size
- Data transfer costs

**To fine tune costs we have pricing models**

- Frequently accessed data:
     - Storage cost will be high
     - Data transfer cost will be least

- In-Frequently accessed data:
     - Storage cost will be less
     - Data transfer cost will be high

- Archival Storage:
     - Storage cost will be least
     - Data transfer (accessing) might not be allowed

- Blob Storages have options to enable them as Data Lakes.
- Blob Storages will have integration with Content Delivery Networks (CDN)
- Blob Storages can serve web applications (Static Webpages – HTML CSS, JavaScript)

### AWS

#### Infrastructure

- **Region:** This is geographical area which has Availability Zones (AZ)
- **AZ:** This a location/site with in region where AWS hosts datacenters

#### S3

- Simple Storage Service (S3) is a service offered by AWS for Blob Storages.
- To use S3 we need to create a bucket (S3 Bucket)
- A Bucket will have a unique name across AWS.
- We can consider Bucket as unlimited storage with a restriction of individual file size cannot be greater than 5 TB
- Bucket will have permissions of who can access the data
- Buckets support versioning.

#### Terms

- **Bucket:** Bucket can have objects or folders or both
- **Object:** This represents file
- **Permission**

#### Creating first s3 bucket

- I will be creating s3 bucket in Hyderabad region with public read access enabled

![image](https://github.com/user-attachments/assets/72e26ceb-21fe-4a1a-828a-f42cdb3637a4)

![image](https://github.com/user-attachments/assets/548b6678-113c-47b1-8419-b9c9cecd95c6)

- While creating bucket ensure ACL’s are enabled, and unselect disable public access

![image](https://github.com/user-attachments/assets/f55932f9-7055-4300-8632-b2e63912d88f)


#### **Uploading content to buckets**
- Navigate into s3 bucket

![image](https://github.com/user-attachments/assets/23b7bd3c-5982-4b53-9b13-0b1d026d5e29)

Upload any file (png or mp3 or mp4 or pdf)

![image](https://github.com/user-attachments/assets/24eed6f2-1742-458a-a7ba-d716934dc5ea)
![image](https://github.com/user-attachments/assets/63b6d39e-3f8d-4be0-b185-57e03b78edfb)

#### **Delete the buckets**
- S3 buckets have to be empty before delete
- **Note:** Watch classroom video for steps

#### **Exercise**
- Create an s3 bucket in any region
- upload 3 files
- Ensure you can access over http(s)
- Delete the buckets

# March 23

### S3 Contd

#### Storage Classes

- [S3 Storage Classes](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-class-intro.html)
- When we upload data into s3 bucket, it creates multiple copies and stores it in multiple locations
- This is done to address two major factors
    - Durability: Chance of data getting lost or corrupted.
    - Availability: How much data is available for access.

- Frequently accessed Data
- **Standard:**
      - This is default [ storage](https://directdevops.blog/2025/03/23/multicloud-classroom-notes-23-mar-2025/#) class. As part of free tier accounts we 
        can use 5GB of Standard Storage for free.
      - Availability: 99.99%
      - Durability: 99.99999999999 (eleven 9s)
      - High storage cost and less access cost
- S3 Express One Zone
- Reduced Redundancy Storage

- Infrequently accessed Data
    - S3 Standard-IA
    - S3 One Zone-IA

- Rarely accessed Data
    - S3 Glacier Instant Retrieval (GLACIER_IR)
    - S3 Glacier Flexible Retrieval (GLACIER)
    - S3 Glacier Deep Archive (DEEP_ARCHIVE)


# AWS S3 Storage Classes Comparison

| Storage Class                    | Use Cases                                                  | Durability            | Availability | Latency        | Minimum Storage Duration | Retrieval Charges     |
|-----------------------------------|-----------------------------------------------------------|-----------------------|--------------|---------------|-------------------------|----------------------|
| S3 Standard                      | Frequently accessed data (e.g., websites, big data)      | 99.999999999% (11 nines) | 99.99%       | Milliseconds   | None                    | None                 |
| S3 Intelligent-Tiering           | Data with unknown or changing access patterns            | 99.999999999% (11 nines) | 99.9%        | Milliseconds   | None                    | None                 |
| S3 Standard-IA                   | Infrequently accessed data needing rapid access         | 99.999999999% (11 nines) | 99.9%        | Milliseconds   | 30 days                 | Per GB retrieved     |
| S3 One Zone-IA                   | Re-creatable infrequently accessed data stored in a single zone | 99.999999999% (11 nines) | 99.5%        | Milliseconds   | 30 days                 | Per GB retrieved     |
| S3 Glacier Instant Retrieval     | Archive data that needs immediate access                | 99.999999999% (11 nines) | 99.9%        | Milliseconds   | 90 days                 | Per GB retrieved     |
| S3 Glacier Flexible Retrieval    | Rarely accessed long-term archive data                  | 99.999999999% (11 nines) | 99.9%        | Minutes to hours | 90 days                 | Per GB retrieved     |
| S3 Glacier Deep Archive          | Long-term archive data accessed once or twice per year  | 99.999999999% (11 nines) | 99.9%        | Hours          | 180 days                | Per GB retrieved     |



- Intelligent Tiering: In this case depending on your access patterns, storage class is automatically chosen.


#### Choosing storage classes

- Create an s3 bucket with acls enabled is Block public access is unchecked
- Upload any file and add public-read access
- Navigate to the properties section

![image](https://github.com/user-attachments/assets/07ba0513-42ea-42c9-aa5e-8a0391d3c901)

- Once the file is uploaded

![image](https://github.com/user-attachments/assets/b3a893c4-7b5d-40f1-9c01-cde1e03c265a)

![image](https://github.com/user-attachments/assets/ff0682bd-cb46-43e7-a2bc-1684776a1660)

- AWS Offers lifecycle tranistion rules

![image](https://github.com/user-attachments/assets/926e4984-2238-44bb-ac91-9c12815e9186)

![image](https://github.com/user-attachments/assets/ffdc0c23-5920-4e54-b582-c188826db39b)

- If the access patterns are not predictable then use intelligent tiering.


# March 25

## S3

- Note: For screenshots watch recording

## Versioning

- S3 buckets versioning can be enabled and suspended
- Navigate to the Bucket -> Properties -> Bucket Versioning -> Enable
- Generally it is recommended to enable versioning, we can write a lifecycle to delete/move to cheaper storages older versions

## Prefix

- The buckets which we have created so far are called as General Purpose Buckets.
- Each blobs name with folder path is called as prefix

## Requester Pays

- S3 charges for storage and access,
- I can have s3 bucket and enable requester pays i.e. storage cost will be paid by me and request cost will be paid by requester (who is generally other 
  aws account)

## S3 Static Website Hosting

- Since s3 is capable of urls, we can configure s3 to host a website
- A static website referes to a website developed in html, css and javascript
- Upload website from [here](https://www.free-css.com/free-css-templates/page295/applight)

![image](https://github.com/user-attachments/assets/f2077c73-f674-4a7f-83d8-d5f26323a4ac)

![image](https://github.com/user-attachments/assets/698c1686-67c9-480e-a7b0-407b4511d2e5)


![image](https://github.com/user-attachments/assets/0596b0bf-e2fb-4023-8543-c907ffdc5e8f)


# March 26

## Directory and Table Buckets

- These are two new types of buckets added.
     - Directory Buckets: They use file paths rather than prefixes, This is useful for data lakes
     - Table Buckets: This is based on Apache Iceberg to store the data in tabular formats for quick retireval
- They are used for storing semistructure data in large volume Data Pipelines.

## Cross region Replications

- When the data is added to one bucket either all content or some selected content based on prefixes can be synced to other buckets in other regions

![image](https://github.com/user-attachments/assets/23da15e9-e3a1-4ae9-9185-d9d2f15c3821)

- Navigate to Management -> Replication Rules

## Storage in Azure
- [ Azure](https://directdevops.blog/2025/03/26/multicloud-classroom-notes-26-mar-2025/#) Storage Account is a service offered by Azure which handles
     - blob storage
     - Table Storage
     - File Shares
     - Queue Storage
- In Azure Blob Storage has 3 types
     - Page Blob: Hard disks
     - Block Blob: blobs (like s3 objects)
     - Append Blod: for log files
- Azure Global Infra:
     - Azure has two types of regions
         - regions
         - regions with zones

- [Azure Storage Accounts](https://learn.microsoft.com/en-us/azure/storage/common/storage-account-overview)
- [Storage Account types](https://learn.microsoft.com/en-us/azure/storage/common/storage-account-overview#types-of-storage-accounts)
- [Azure Storage Redundancy](https://learn.microsoft.com/en-us/azure/storage/common/storage-redundancy)
- [Durability And Availability](https://learn.microsoft.com/en-us/azure/storage/common/storage-redundancy#durability-and-availability-parameters)
- [Access Tiers](https://learn.microsoft.com/en-us/azure/storage/blobs/access-tiers-overview)



# March 27

## Azure Resource Creation

- Resources can be create only in Resource Groups

![image](https://github.com/user-attachments/assets/94b7dcbf-3bda-44c4-8b31-85911d04950b)


- Creating [storage account](https://learn.microsoft.com/en-us/azure/storage/common/storage-account-create?tabs=azure-portal)
- Pattern for storage account blob url

```
https://<storage-acc-name>.blob.core.windows.net/<container>/<blob-path>
https://qtstorageaccount27march.blob.core.windows.net/documents/1.txt
```

- [Enable versions in Azure Storage Account](https://learn.microsoft.com/en-us/azure/storage/blobs/versioning-enable?tabs=portal)
- [Host a static website](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blob-static-website)
- [Lifecycle Transitions/Lifecycle policy](https://learn.microsoft.com/en-us/azure/storage/blobs/lifecycle-management-policy-configure?tabs=azure-portal): Move from one Archive tier to another based on rules
- [ReHydrate](https://learn.microsoft.com/en-us/azure/storage/blobs/archive-rehydrate-overview)


# April 1

#### Disk Storage
- A virtual disk in a cloud caters to one virtual machine generally.
- Cloud offerings generally charge for hardware utilization.
- If the disk and virtual machine are created from same physical server
    - disk will have temporary/ephemeral storage i.e. shutting down the vm will erase data
- If the disk and virtual machine are created from different physical servers
    - disks will have persistent/non ephemeral storage i.e. shuttidng down the vm will not erase data
#### AWS:
- Non ephemeral/persistent disks are called as EBS Volumes
- ephemeral/temporary disk are called as instance storages.
#### Azure:
- Non ephemeral/persistent disks are called as Managed Disks
- ephemeral/temporary disksts are called as Temp/Local Disks.
- In both clouds the os disk (root volume) has to be persistent
- No cloud allows you to reduce disk size, they support only increasing the sizes
- VM Size has impacts on disk performance
- The compressed copy of the disk contents is called as snapshot (Backup of a disk)
- Snapshots are generated either incrementally or as part of full backups

#### AWS Disk Storage for single ec2 instance
- AWS has two types of disks
    - EBS Volumes:
        - Default storage type for all root volume (disk with OS in it)
        - This is supported in all ec2 instance types.
        - Size is flexible
        - Max number of EBS Volumes have nothing to do with instance types

    - Instance Storage:
        - This is supported only by few instance types
        - Sizes are fixed
        - Max number of instance stores are defined in instance type.

#### Disk Hardware types supported by AWS
- ssd
- hdd
- magnetic

#### Azure Disk Storage for single VM
- Azure has two types of disk
- Persistent
    - OS Disk: Persistent and is supposed to be boot disk
    - Data Disk: Additional persistent disks, Number of Data disks also depends on VM Size.
- Temporary
    - Local Disk: Is more common is Azure
        - This is temporary disk
        - Size of Local Disk is fixed and is dependent on VM Size
- Disk Hardware types supported by Azure
    - ssd
    - hdd


# April 3

### MVP FOR Cloud And DevOps Engineers

```
Cloud + DevOps
Engineer (0-2)
CI/CD (Git, GitHubActions/AzureDevOps/Jenkins)
Terraform
Containers
Docker
Kubernetes
Python (scripting)
Bash
Cloud:
Compute (VM)
Networking
Storage
```

### Engineer (2-5)
```
 CI/CD (Git, GitHubActions/AzureDevOps/Jenkins)
 Terraform
 Containers
   Docker
   Kubernetes (RBAC, ARGO CD, Istio)
 Python API, Serverless (AWS Lambda)
 Bash
 Cloud: (Add Automation with Terraform/Cloud Formation/Azure Bicep)
   Compute (VM, App Services, Serverless)
   Networking  (LB, VPN Networking)
   Storage (Access)
 Observability
```

### Sr Engineer (5+)
```
 Design (Case studies)
 CI/CD (Git, GitHubActions/AzureDevOps/Jenkins)
 Terraform
 Containers
   Docker
   Kubernetes (RBAC, ARGO CD, Istio)
 Python API, Serverless (AWS Lambda)
 Bash
 Cloud: (Add Automation with Terraform/Cloud Formation/Azure Bicep)
   Compute (VM, App Services, Serverless)
   Networking  (LB, VPN Networking)
   Storage (Access)
 Observability
```

# April 4

### Disk and Network Storages

- Activities:
    - Creating the disks and attaching the disks to vms (vm disks)
    - Creating the network disks and attaching the disks to vms
        - Third party disk
        - File systems
    - Performance and sizing
    - Increasing disk sizes and making it usable in Virtual machines
    - Backups and backup retentions
    - Replicating or recreating disks in other regions
    - Disk Encryptions

### Creating Disks and Attaching them to EC2 instances in AWS
- Create an ec2 instance with ubuntu with only root disk
- In AWS, the disk and ec2 instance should belong to the same zone,
- Lets create a disk of size 1 GB in same zone as ec2
- Now Attach the disk the ec2 instance
- To effective deal with mounting, go through following linux topics
    - lsblk
    - mkfs
    - mount
    - fstab
    - [disk partitions](https://www.digitalocean.com/community/tutorials/create-a-partition-in-linux)
    - [extending partition](https://learn.microsoft.com/en-us/windows-server/storage/disk-management/extend-a-basic-volume)

### Diffferent Volume Types
- General purpose 2
- General Puprose 3
- Provisioned IOPS io1
- Provisioned IOPS io2
- Cold HDD
- Throughput optimized HDD
- Magnetic

Here is a comparison of the various AWS EBS volume types with respect to IOPS, Throughput, Minimum Size, and Maximum Size:

| Volume Type                     | IOPS                                                                 | Throughput                                                                 | Min Size  | Max Size  |
|----------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------|-----------|-----------|
| General Purpose SSD (gp2)       | 100 to 16,000 IOPS (3 IOPS per GiB, burst up to 3,000 IOPS for smaller volumes) | Up to 250 MiB/s (burst)                                                     | 1 GiB     | 16 TiB    |
| General Purpose SSD (gp3)       | Baseline of 3,000 IOPS, provisionable up to 16,000 IOPS              | Baseline of 125 MiB/s, provisionable up to 1,000 MiB/s                      | 1 GiB     | 16 TiB    |
| Provisioned IOPS SSD (io1)      | Up to 256,000 IOPS depending on instance type and size               | Up to 4,000 MiB/s depending on configuration                                | 4 GiB     | 16 TiB    |
| Provisioned IOPS SSD (io2)      | Up to 256,000 IOPS depending on instance type and size               | Up to 4,000 MiB/s depending on configuration                                | 4 GiB     | 16 TiB    |
| Throughput Optimized HDD (st1)  | Baseline: 40 MiB/s per TiB; Burst: up to 500 MiB/s                   | Burst throughput: up to 500 MiB/s; baseline scales with volume size         | 125 GiB   | 16 TiB    |
| Cold HDD (sc1)                  | Baseline: lower than st1; Burst: up to 250 MiB/s                     | Burst throughput: up to 250 MiB/s; baseline scales with volume size         | 125 GiB   | 16 TiB    |
| Magnetic (Standard)             | Very low and inconsistent performance                                | Limited throughput; not recommended for new workloads                       | N/A       | Up to 3 TiB |



### Key Observations:
- SSD-backed volumes (gp2, gp3, io1, io2) are optimized for high IOPS and consistent performance. They are ideal for transactional workloads.
- HDD-backed volumes (st1, sc1) are optimized for throughput-intensive workloads. They perform best with large sequential I/O operations.
- Magnetic disks are legacy storage options and are not recommended for new workloads due to their limited performance capabilities.


# April 5

## Disk Storage activities
### Windows
- Lets create an additional disk of 2 GB to an windows server
- This additional disk will be partioned into two volumes of 1 GB each
- Now lets increase the disk size to 3 GB and increase the size of first partition to 2 GB
- Watch classroom recording

### Linux
- In Linux, we have disks
- Disk can be partitioned (option)
- Partitioned disks can be mounted to a folder
- [Refer Here](https://learn.microsoft.com/en-us/azure/virtual-machines/linux/attach-disk-portal) for steps to partition and mount disks

### Activity 1: Attaching, Mounting and Extending Disks
- Attaching disks to AWS EC2 Linux Instance (Ubuntu)
- Create Partitions
- Extend partitions
- Repeat the similar activity on Azure
- Watch Classroom Recording.

### Activity 2: Backup of the Disks
- In Cloud, We use a term called as snapshot to refer a backup of disk
- Creating a disk backup manually in AWS

![image](https://github.com/user-attachments/assets/76ee37c7-442f-4676-8e77-ee01cc1a9a9a)

![image](https://github.com/user-attachments/assets/2a700a61-ea90-49f8-807b-2b73b404a9e1)

![image](https://github.com/user-attachments/assets/c32a84b9-8383-4b55-812e-4f9c0a59fe62)

- AWS Snapshots are incremental in nature
- Creating a disk backup manually in Azure

![image](https://github.com/user-attachments/assets/54e4c892-77a7-479a-aa7a-2ad4806aff21)


- Azure gives incremental as well as full backup options

![image](https://github.com/user-attachments/assets/3f634a57-49e1-4d7e-8b89-0c7b65eaae9b)

- Using Snapshots
- we can create new disks with the same content.
- If the snapshot has OS in it we can create AMI/Azure VM Image
- Copy the snapshot to other regions
- Share the snapshot with other accounts.
- Automating Snapshot creation:
    - Use Snapshot policies
    - Azure Backup/AWS Backup

# April 7

## Network file shares
- Overview

![image](https://github.com/user-attachments/assets/80fa63e4-9a35-49ba-afdf-477957cd1803)

- Mounting happens over the network

![image](https://github.com/user-attachments/assets/d3c22033-0000-4c4e-93e7-af741b3d9aaf)

### Options for Network Storage
- Here is a comparison of different network storage options in tabular format, covering their types, features, and use cases:

| Type                     | Description                                                              | Key Features                                                                 | Ideal Use Cases                                   |
|--------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------------|---------------------------------------------------|
| Direct Attached Storage (DAS) | Storage directly attached to a server or workstation.                   | – Simple setup  <br> – Low cost  <br> – Limited scalability  <br> – No network sharing | Small networks, single-server environments         |
| Network Attached Storage (NAS) | Dedicated storage device connected to a network, providing file-based data access. | – Centralized storage  <br> – Easy file sharing  <br> – Supports NFS/SMB protocols  <br> – RAID for redundancy | Small to medium businesses, file sharing           |
| Storage Area Network (SAN)     | High-speed network that provides block-level storage access to multiple servers. | – High performance  <br> – Scalable  <br> – Uses Fibre Channel or iSCSI  <br> – Suitable for mission-critical apps | Large enterprises, data centers, high-speed needs |
| Cloud Storage                  | Storage solutions offered by cloud providers like AWS, Azure, and Google Cloud. | – Pay-as-you-go model  <br> – Scalable on demand  <br> – Accessible globally  <br> – Managed services available | Backup, disaster recovery, remote collaboration   |


- Examples of Products for Each Type

| Type                     | Description                                                              | Key Features                                                                 | Ideal Use Cases                                   | Examples                                                                 |
|--------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------------|---------------------------------------------------|--------------------------------------------------------------------------|
| Direct Attached Storage (DAS) | Storage directly attached to a server or workstation.                   | – Simple setup  <br> – Low cost  <br> – Limited scalability  <br> – No network sharing | Small networks, single-server environments         | JBOD (Just a Bunch of Disks), RAID arrays                                |
| Network Attached Storage (NAS) | Dedicated storage device connected to a network, providing file-based data access. | – Centralized storage  <br> – Easy file sharing  <br> – Supports NFS/SMB protocols  <br> – RAID for redundancy | Small to medium businesses, file sharing           | Synology DiskStation DS1522+, QNAP TS-233-US, TerraMaster F4-423        |
| Storage Area Network (SAN)     | High-speed network that provides block-level storage access to multiple servers. | – High performance  <br> – Scalable  <br> – Uses Fibre Channel or iSCSI  <br> – Suitable for mission-critical apps | Large enterprises, data centers, high-speed needs | Dell EMC PowerMax, HPE Primera, IBM FlashSystem                         |
| Cloud Storage                  | Storage solutions offered by cloud providers like AWS, Azure, and Google Cloud. | – Pay-as-you-go model  <br> – Scalable on demand  <br> – Accessible globally  <br> – Managed services available | Backup, disaster recovery, remote collaboration   | Amazon S3, Google Filestore, Microsoft Azure Blob Storage                |


## AWS Network File share Offerings
- EFS (Elastic File Share)
- FSx (File Share x)
- EFS Overview

![image](https://github.com/user-attachments/assets/8d41ebc6-f127-4bf3-a0b7-b4c3d9e15f7a)


#### EFS in existing network (VPC)
- Create two ubuntu systems in two different zones

![image](https://github.com/user-attachments/assets/641cc0cd-c04c-48b8-88e1-7e432d9f3fe1)

- Now create an EFS as discussed in the class
- [Refer Here](https://docs.aws.amazon.com/efs/latest/ug/mounting-fs.html) for instructions on how to mount
- On ubuntu install nfs client
```
sudo apt update
sudo apt-get -y install nfs-common
```
- Create a folder called as /projects
- Now mount using instructions

![image](https://github.com/user-attachments/assets/af682a96-9b4b-431f-9335-b71aa1a12b54)

- We have mounted to /projects
```sudo mount -t nfs4 -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport fs-07760194a1be46edf.efs.ap-south-1.amazonaws.com:/ /projects```

- Now execute df -h

![image](https://github.com/user-attachments/assets/c3ba79d6-6dee-4327-bb6a-50db164c966c)

#### EFS in new network (VPC)
- Note: Watch classroom video for steps
- I will create a network and security group
- Exercise: Repeat the exact same with Redhat Instances

# April 8

## Azure File Storage
- [Refer Here](https://learn.microsoft.com/en-us/azure/storage/files/storage-files-introduction) for Azure file share
- [Creating file shares](https://learn.microsoft.com/en-us/azure/storage/files/storage-how-to-use-files-portal?tabs=azure-portal)
    - [NFS File share](https://learn.microsoft.com/en-us/azure/storage/files/storage-files-quick-create-use-linux)
    - [SMB File share](https://learn.microsoft.com/en-us/azure/storage/files/storage-how-to-create-file-share?tabs=azure-portal)
- [Azure File Share Tiers](https://learn.microsoft.com/en-us/azure/storage/files/storage-files-planning#available-protocols)
- Watch the clasroom video for mounting fileshares on linux machines

#### AWS Third Party Storage Solutions
- AWS Offers a service called as fsX which is a file share supporting third party vendors

#### Findout Pricing for
- Using EFS with 100 TB with different options
- Using FSx with 100 TB with different options
- USing Azure File share with 100 TB
- Usign Azure Netapp File with 100 TB
- Note: Shared Disk and Multi-Attach EBS are used primarily for systems to quickly recover from failures i.e. Failover kind of Scenarios.

# April 9

## Databases
- Database as a service is offered by Cloud Providers
- Watch classroom video to understand what database as a service is.


# April 10

## Database as a Service

### Relational Databases

- In this category of Databases, Data is stored in a database, which is categorized into tables.
- Each Table will have columns which represent fields and rows which represent records
- Tables will have relationships between them
- We need DBMS to manage database, [ Softwares](https://directdevops.blog/2025/04/10/multicloud-classroom-notes-10-apr-2025/#) which offer them are
    - Microsoft SQL Server
    - Oracle
    - mysql
    - Postgres
    - DB2
- AWS has a service called as [ RDS](https://directdevops.blog/2025/04/10/multicloud-classroom-notes-10-apr-2025/#) where the following database engines are offered as service
    - SQL Server
    - Oracle
    - mysql/mariadb
    - Postgres
    - SQL Server
    - Aurora:
        - Postgres
        - mysql
- Azure offers Database as a service for
    - SQL Server
    - mysql/maria
    - postgres

#### AWS RDS
- Overview

![image](https://github.com/user-attachments/assets/9c090ec8-f9ff-4a0a-88de-1fe77d0566a3)


- RDS is created in the network (VPC) and requires at least two subnets provided to RDS (DB Subnet Group) while creation.
- RDS instances can be public or private
- RDS instances will have pricing similar to ec2 i.e. hourly billing and storage charges
- RDS instances support disks with autoscaling (Start from 20 GB and AWS will automatically increase disk size when needed)
- AWS Generally gives 3 ways of creating a database instance
    - Single AZ
    - Multi AZ
    - Multi Az Cluster

### Lets create a Single AZ mysql instance
- Single AZ mysql
- network: default
- subnet group: default
- access: public
- free tier:
- Watch classroom video for screen shots

![image](https://github.com/user-attachments/assets/de926db6-f0a5-4fcd-b2d5-bfe5e5d1c717)

![image](https://github.com/user-attachments/assets/ce8467a7-fb21-4fdc-840f-7331623c56d8)

- Terms to understand
    - Replications
    - Failover
- Exercise: Try creating
    - Single Database with mysql in Azure
    - Single Database with Postgres in AWS


# April 12

## AWS RDS
### Read – Replica
- Overview

![image](https://github.com/user-attachments/assets/162f89ba-7819-48fe-8efc-b0f218acb03e)

- We will an [ RDS](https://directdevops.blog/2025/04/12/multicloud-classroom-notes-12-apr-2025/#) instance which is primary instance, we can add a read replica which helps in
    - distributing the load
    - Reducing downtime

## Multi-AZ
- Overview

![image](https://github.com/user-attachments/assets/57e22aa2-3aca-4293-9495-2196122c9974)

- We will have master and standby instance and failover is automatic

![image](https://github.com/user-attachments/assets/28749d77-79b0-4699-b086-7225b49040dd)

### Multi-AZ Cluster
- Overview

![image](https://github.com/user-attachments/assets/08ac32b9-e797-4d83-b61c-b1c679d73eb2)

### Aurora
- Amazon offers aurora databases for mysql and postgres
- Amazon’s claim Aurora delivers up to 5x the performance of MySQL and 3x that of PostgreSQL without requiring changes to most applications

![image](https://github.com/user-attachments/assets/9763481c-a0d9-4d4a-83c1-7b95739af06f)

## Azure Microsoft SQL Server
- Azure offers Microsoft Server in 3 services
    - Azure SQL
    - Azure SQL VM
    - Azure SQL Managed Instances

### Create an azure sql database

- [Refer Here](https://learn.microsoft.com/en-us/azure/azure-sql/database/single-database-create-quickstart?view=azuresql&tabs=azure-portal)

![image](https://github.com/user-attachments/assets/5f04154e-eb7c-45bc-99a5-23b3ad91a1a1)

- Purchasing models
    - DTU:
        - Basic
        - Standard
        - Premium
    - vCore:
        - General purpose
        - Hyperscale
        - Business Critical

# May 19

### Topics (for next 3 weeks)

- Infra Provisioning: (Easier Deployments and updates)
    - Azure:
        - ARM
        - Azure Bicep
    - AWS:
        - Cloudformation
- Operations: (Administrative activities)
    - Backups
    - Disaster Recovery
    - Basic operations
    - Monitoring
- Databases (DBA without tuning)
    - Relational Databases
    - NoSQL Databases

# May 20

## Cloud Terminology

- Public Cloud: We will be using someone else’s hardware to create our virtual infrastructure.
- Popular Providers:
    - AWS
    - Azure
    - GCP
    - Ali Cloud
- Private Cloud: We will be using our org’s hardware to create our virtual infrastructure.
- Popular option:
    - Openstack
- Cloud offers Services:
    - Example Services
        - Compute
        - Storage
        - Databases
        - Kubernetes
        - AI/ML
        - LLM Models
        - ..
        - ..
- Service: What cloud offers
- Resource: What we create
- A service is a way to create virtual infra where you can use the resource for your business needs.
    - you own the resource
    - cloud service provider they own the service.
- Resources will be charged based on usage (metered)
- All cloud providers offer free tiers
    -  AWS:
        - Some services are free for 12 months
        - Some services are free for ever
        - some are never free.
    - Azure:
        - first 1 month: till 200$ of usage everything is free.
        - post 1 month
            - Some services are free for 12 months
            - Some services are free for ever
            - some are never free.
    - GCP:
        - first 3 months: till 300$ of usage everything is free
        - post 3 months
            - Some services are free for ever
            - some are never free.

### Lets create a virtual machine
- Linux:
    - Linux Supports two kinds of credentials
        - password
        - key based
- Watch classroom recording

# May 21

### Nop Commerce
- This is an open source ecommerce application
- [link](https://www.nopcommerce.com/en?srsltid=AfmBOoqInDUQFYHL9WkV-DHUly_XpryFp6sAeyluDDnj3v-j7RTDrHyt)
- System Components
    - App Server
    - Database Server

![image](https://github.com/user-attachments/assets/4efa8dbe-b426-4db3-a222-4103d2827e0e)

- Minimum infra required
    - network
    - 2 servers with ubuntu os connected to the network
- To make this application available to public we need public ip address which is mapped to some domain

![image](https://github.com/user-attachments/assets/32e7bc7d-faac-4984-b299-fd9e0758edb7)


### How to make this work on AWS
- We need a Network which is capable of having both public and private ip address (VPC)
- We would need a server running mysql database (RDS)
- We would need a server running ubuntu where we can install nop Commerce (EC2)
- We need to configure restricted access for administration and free access over web

### How to make this work on Azure
- We need a Network which is capable of having both public and private ip address (Virtual Network)
- We would need a server running mysql database ( Azure For mysql)
- We would need a server running ubuntu where we can install nop Commerce (Virtual Machines)
- We need to configure restricted access for administration and free access over web
- [Refer Here](https://github.com/milanm/Cloud-Product-Mapping) for Service Equivalents

### Realizing nop commerce in AWS
- Create a network using vpc, we need to give private ip range 10.0.0.0/16
- To understand the next topic, today explore
    - Region
        - Zones (AZ): This will have many datacenters in it

# May 22

### Realizing nop commerce in AWS
- Create a network using vpc, we need to give private ip range 10.0.0.0/16
- To understand the next topic, [today explore](https://datacenters.microsoft.com/globe/explore/datacenter)
    - Region
        - Zones (AZ): This will have many datacenters in it
- As we need to create subnets
    - AWS: Subnet is mapped to a availability zone
- For nop Commerce lets create two subnets
    - app
    - db
- AWS: AWS used id’s over names
- Watch recording for steps
- We have create a network with one public and one private subnet
- Lets create two security groups
    - one for nop commmerce (80,5000,22)
    - one for mysql (3306)
- Lets create an ec2 instance in app subnet (Watch recording)
- To connect to linux instance
```ssh -i <path to pem> username@ipaddress```

# May 24

## Create mysql database in AWS
- AWS has Relational Database as a Service option (RDS)
- Watch classroom recording for steps

### Installing nopCommerce on ubuntu
- [Refer Here](https://docs.nopcommerce.com/en/installation-and-upgrading/installing-nopcommerce/installing-on-linux.html) for steps
- Softwares:
    - [.net core 9 SDK](https://learn.microsoft.com/en-us/dotnet/core/install/linux-ubuntu-install?tabs=dotnet9&pivots=os-linux-ubuntu-2404)
    - [nopCommercePackage](https://github.com/nopSolutions/nopCommerce/releases/download/release-4.80.6/nopCommerce_4.80.6_NoSource_linux_x64.zip)
- Commands

```
sudo -i
mkdir -p /opt/nop
cd /opt/nop
wget https://github.com/nopSolutions/nopCommerce/releases/download/release-4.80.6/nopCommerce_4.80.6_NoSource_linux_x64.zip
apt install unzip -y
unzip nopCommerce_4.80.6_NoSource_linux_x64.zip
mkdir bin logs
dotnet Nop.Web.dll --urls "http://0.0.0.0:5000"
```

# May 31

## Cloudformation
- AWS Cloudformation allows us to create infra based on a template
- Template can be written in json/yaml format
- JSON is a file format for representing data. JSON follows key value pair to define it structure
```"<key>": <value>```
- Value can be of different types
    - text: this is generally surrounded with single or double quotes "movie": "retro" or 'movie': 'retro'
    - numer: This is any number 'runtime': 130
    - boolean: This has two values true or false 'theare': false
    - list/array: this has values of any type in [] 'actors': ['surya', 'pooja']
    - map/dictionary/object: this generally represents a complex type which requires more key value pairs to describe. This is surronded with {}

```
{
    "name": "Multicloud",
    "starttime": "19:00",
    "topics": ["json", "yaml", "cf"],
    "mode": ["online", "offline"],
    "where": {
        "flat": "601-A",
        "building": "nilgiri",
        "city": "Hyberabad"
    }
}
```
- YAML is a file format for representing data. YAML follows key value pair to define it structure
```key: <value>```

- Value can be of different types
    - text: this is generally surrounded with single or double quotes movie: "retro" or movie: 'retro' or movie: retro
    - numer: This is any number runtime: 130
    - boolean: This has two values true or false or yes or no theare: no
    - list/array: this has values of any type in [] actors: ['surya', 'pooja']
    ```
    “`yaml
    actors:</li>
    <li>surya</li>
    <li>pooja
    “`
    ```

    - map/dictionary/object: this generally represents a complex type which requires more key value pairs to describe. This is surronded with {}

```
“`yaml
address:
flatno: 601-A
building: nilgiri</li>
    </ul>
    “`
    * Example
---
name: Multicloud
starttime: '19:00'
topics:
  - json
  - yaml
  - cf
mode:
  - online
  - offline
where:
  flat: 601-A
  building: nilgiri
  city: Hyberabad
```

![image](https://github.com/user-attachments/assets/fb918e63-82b7-481a-8c42-439a53c15ee3)

#### Building Blocks of Cloudformation
- Template: This uses a json or a yaml file in a format defined by aws [Format](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-formats.html)
- Stack: When we want to create infra, we create a cloudformation stack, where we pass the template. By default stack creates everything or nothing. stacks can be updated to recreate/modify the infrastructure created.

#### Template components
- [Version](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/format-version-structure.html)
- [Parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html)
- [Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resources-section-structure.html)
- [Outputs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html)

#### Minimial Template
- This requires only Resources

```
{
    "Resources": {
        "mybucket": {
            "Type" : "AWS::ServiceName::ResourceType",
            "Properties" : {
                "PropertyName1" : "PropertyValue1",
            }

        }
    }
}
```

#### Lets create a cloudformation template for Network
- Create a new folder & open in visual studio code
- Create a new file main.json
- To find the structure of vpc google aws cloudformation vpc
![image](https://github.com/user-attachments/assets/0831368f-6c3a-464c-b439-fa30077ceb5f)
![image](https://github.com/user-attachments/assets/ab54d568-8cc8-4a49-8f1c-7dad960a2918)

- This is our first template

```
{
    "Resources": {
        "network" : {
            "Type" : "AWS::EC2::VPC",
            "Properties": {
                "CidrBlock": "192.168.0.0/16",
                "EnableDnsHostnames": true,
                "Tags": [{
                    "Key": "Name",
                    "Value": "from-cf"
                }]
            }
        }
    }
}
```

- To create a cf stack watch classroom recording
- To be productive in terms of authoring templates, visual studio code has extensions
![image](https://github.com/user-attachments/assets/7bc1be53-83a4-453f-a538-6759f41e3604)
- [Refer Here](https://github.com/asquarezone/MultiCloudZone/commit/e28dae6109d1cc22fb54d10449678a1b4d6daff1) for the changes done.

# June 1

### Cloudformation

##### Parameters
- [Refer Here](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html) for parameters

##### Functions
- [Refer Here](https://docs.aws.amazon.com/AWSCloudFormation/latest/TemplateReference/intrinsic-function-reference.html) for official docs of functions
- [Refer Here](https://github.com/asquarezone/MultiCloudZone/commit/6e26876abd1f5fe34a487afe245cf222035d4805) for changes done

### Azure Resource Manager (ARM) Templates
- Azure subscriptions will have Resource Providers. Each Resource Provider will have resources.
- When creating any resources, resource providers do the heavy lifting and create resources.
- Azure Portal Based creation, end up creating templates by default

![image](https://github.com/user-attachments/assets/a1b40a8f-0dbd-40ae-8ace-13e7c5710364)

- ARM Template Components
    - [Syntax](https://learn.microsoft.com/bs-latn-ba/azure/azure-resource-manager/templates/syntax)
- [Visual Studio Code](https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/quickstart-create-templates-use-visual-studio-code?tabs=CLI)
- Install ARM Tools extension

![image](https://github.com/user-attachments/assets/50f054b9-c8f2-42fe-9737-6a8c02913fe0)

- basic arm template version
```
{
    "$schema": "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "functions": [],
    "variables": {},
    "resources": [],
    "outputs": {}
}
```

- [ARM Template functions](https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/template-functions)
- [Refer Here](https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/copy-resources) for copying i.e. looping

# June 3

## ARM Templates contd
- [Refer Here](https://github.com/asquarezone/MultiCloudZone/commit/8c6181c9249d8c9d2909c0faa3e1ac0b703f6c96) for the changes done so far.
- Lets create a [nsg](https://learn.microsoft.com/en-us/azure/virtual-network/manage-network-security-group?tabs=network-security-group-portal)
- [Refer Here](https://github.com/asquarezone/MultiCloudZone/commit/a709baac10c7b6ab6a7457c0ed4489b1cbc7c2a4) for changes
- Now lets add a public ip address [Refer Here](https://learn.microsoft.com/en-us/azure/templates/microsoft.network/publicipaddresses?pivots=deployment-language-arm-template)
- [Refer Here](https://github.com/asquarezone/MultiCloudZone/commit/a44fdb00e055803ca925bf4a8387be4428805cc7) for network interfaces
- [Refer Here](https://github.com/asquarezone/MultiCloudZone/commit/0713a8c7ed59863caee7e3a4691b847d0ddc2ea9) for changes done to add vm.

# June 4

### Azure Bicep
- [Refer Here](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview?tabs=bicep) for official docs
- Azure Bicep is infra provisioning tool with a new domain specific language introduced by Microsoft.
- Install Bicep Extension and getting started with [vscode](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/quickstart-create-bicep-use-visual-studio-code?tabs=azure-cli)
- [Refer Here](https://github.com/asquarezone/MultiCloudZone/commit/8ef8580e4ac38cbae7bc54fa4384b7b5916f6217) for the sample done in the class.

# June 5

### AWS – Operations
- Operations:
    - Backup
    - Restore
    - Archival
    - Access to Compute
#### Backup & Restore
- Terms:
    - Snapshot: Refers to the backup of a resource at a point in time
    - Restore: Snapshots can be use to restore the data
## Activity – 1: Create an ec2 instance and snapshot, restore disks
- We have create an ec2 instance with 2 ebs volumes (Disk) and mounted as shown below

![image](https://github.com/user-attachments/assets/f174f816-bc9e-4187-9ef7-28d001fdaef2)

- Option 1: Taking back up of disks manually
- Option 2: Creating Snapshot Lifecycle
- Option 3:
    - Create a tag for every disk which requires backup Backup = Enabled
    - Launch AWS Backup Service
    - Create/use an vault
    - Create a backup plan with resources assigned

# June 8

## Backups in Azure
- Azure also has centralized Backup service
- Azure has Backup Vaults which are used to store backups and recovery services vaults which also store backups but during failures they can create resources automatically
- Watch class room video for configuring backups and restoring.

### Controlling Virtual Machines in Azure As Admin
- Azure Gives options of Extensions, where admins can run the commands, install/configure softwares without having ssh keys
- Also we have seen how to use instance connect and systems manager run command to acheive the same in AWS

##### Terms
- Landing Zone
- Onboarding
- Centralization:
    - Backups
    - Monitoring and Logging
    - Service availability

# June 9

### AWS Landing Zone
- AWS Control Tower: To create landing zone
- AWS Config: Evaulates policies
- AWS Service Catalog:
- AWS IAM
- AWS CloudWatch
- AWS Cloudtrail
- AWS SNS
- AWS Billing

#### Activity – Audit trail
- 1.Create any thing (s3 bucket, vpc, ….)
- 2.logout
- 3.login
- 4.Delete what you have created
- 5.Findout How to know who has created/deleted

#### Using AWS Control Tower
- Ensure you have a new AWS Account and follow the instructions to create a landing zone

![image](https://github.com/user-attachments/assets/00722526-8277-4788-a7f0-08db7b9f69c7)

##### Azure Landing Zones

![image](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/landing-zone/media/alz-design-areas.svg)

![image](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/enterprise-scale/media/azure-landing-zone-architecture-diagram-hub-spoke.svg#lightbox)

# June 11

### Landing Zone in AWS

![image](https://github.com/user-attachments/assets/a8738434-f5eb-427c-9488-6aaec4e06c68)

#### Landing Zone in Azure
##### Detailed Steps to Create an Azure Landing Zone Using Bicep
- 1. Understand the Modular and Layered Approach:
    -  Azure Landing Zones with Bicep use a modular architecture, where each module encapsulates a core capability (e.g., management groups, networking, policies). Modules are grouped into layers or stages, allowing incremental and flexible deployment[1].

- 2. Prepare Prerequisites:
    - Azure Subscription: Ensure you have Owner or Contributor access.
    - Azure CLI & Bicep CLI: Install the latest versions.
    - Source Code: Clone the official [Azure Landing Zones (ALZ) Bicep repository](https://github.com/Azure/ALZ-Bicep) to get ready-made modules and orchestrators[1][8].
    - CI/CD Tools (optional): Set up Azure DevOps or GitHub Actions for automated deployments[1].

- 3. Plan Your Landing Zone Design:
    - Decide on the Topology: Choose between Hub & Spoke, Virtual WAN, or custom network architectures.
    - Define Management Group Hierarchy: Plan how your subscriptions and resources will be organized (e.g., platform, corp, online management groups)[1].
    - Select Required Modules: Identify which modules (networking, identity, policies, monitoring, etc.) are needed for your environment.

- 4. Customize Bicep Modules (If Needed)
    - Parameterization: Adjust parameters in modules for naming, locations, and resource sizing.
    - Custom Policies/Roles: Modify or add custom policy and role definition modules as per your organizationâ€™s requirements[1].
    - Orchestrator Modules: Use or customize orchestrator modules to deploy multiple modules in a single step, simplifying complex deployments[1].

- 5. Organize Deployment Layers
    - Typical layers include:
        - Core Layer: Management groups, policies, role definitions, subscription placement.
        - Management Layer: Logging, automation, Sentinel, monitoring.
        - Connectivity Layer: Networking (VNets, subnets, NSGs).
        - Identity Layer: Role assignments, managed identities[1].
        - Each layer can be deployed independently or together, depending on your rollout strategy.

- 6. Deploy the Landing Zone
    - A. Deploy with Orchestrator Module (Recommended)
    - Navigate to the orchestrator Bicep file (e.g., main.bicep in the repo).
    - Use Azure CLI to deploy: sh
    - az deployment sub create --location --template-file main.bicep --parameters
    - The orchestrator will handle dependencies and deploy the required modules in the correct order[1][8].
    
    - B. Deploy Individual Modules (Advanced/Custom)
    - Deploy modules one by one, respecting dependencies (e.g., deploy management groups before policies).
    - Example for deploying a networking module: sh
    - az deployment sub create --location --template-file ./modules/networking.bicep --parameters

- 7. Validate and Iterate
    - Check Resources: Confirm that management groups, policies, networks, and other resources are created as expected.
    - Review Compliance: Ensure policies and security controls are enforced.
    - Iterate: Modify modules or parameters as your requirements evolve. The modular approach allows you to add or update layers without redeploying the entire landing zone[1].

- 8. Maintain and Extend
    - Stay Updated: Use the ALZ Bicep Accelerator and its CI/CD pipelines to keep your landing zone in sync with new releases and best practices[1].
    - Customize Further: Add new modules or layers for additional workloads, environments, or compliance requirements.
    - Application Landing Zones: Once the platform landing zone is in place, deploy application-specific landing zones under the appropriate management groups for workload teams[1].
        - Tip: The [ALZ Bicep Accelerator](https://github.com/Azure/ALZ-Bicep) provides step-by-step guidance, automation templates, and branching strategies for managing and customizing your landing zone deployments[1].

#### Summary Table: Core Steps and Actions
| Step                 | Action                                                                 |
|----------------------|------------------------------------------------------------------------|
| Prepare prerequisites| Install tools, clone repo, set up permissions                          |
| Plan design          | Define architecture, management groups, network topology               |
| Customize modules    | Adjust parameters, add custom policies/roles                           |
| Organize layers      | Group modules into logical deployment stages                           |
| Deploy landing zone  | Use orchestrator or individual module deployments via Azure CLI or CI/CD |
| Validate and iterate | Review deployed resources, compliance, and update as needed            |
| Maintain and extend  | Use automation pipelines, keep up with updates, add new modules/layers |


##### For more details, refer to the [Azure Landing Zones Bicep documentation](https://learn.microsoft.com/en-us/azure/architecture/landing-zones/bicep/landing-zone-bicep) and the [ALZ Bicep Wiki Deployment Flow](https://github.com/Azure/ALZ-Bicep/wiki/DeploymentFlow)[1][8].

- [1] https://learn.microsoft.com/en-us/azure/architecture/landing-zones/bicep/landing-zone-bicep
- [2] https://learn.microsoft.com/en-us/azure/architecture/landing-zones/landing-zone-deploy
- [3] https://learn.microsoft.com/en-us/shows/azure-essentials-show/introduction-to-azure-landing-zones-bicep
- [4] https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/landing-zone/implementation-options
- [5] https://azureis.fun/posts/Deploy-Azure-Landing-Zone-with-Azure-Bicep/
- [6] https://zure.com/blog/azure-landing-zones-in-bicep-part-2/
- [7] https://zure.com/blog/azure-landing-zones-in-bicep-part-1/
- [8] https://github.com/Azure/ALZ-Bicep/wiki/DeploymentFlow


# June 13

## Relational Databases
#### What does it take to bring up the relational database
- Create a server
- install relational database software like mysql
- configure mysql
- create necessary users

#### Operational activities
- User Management
- Backups and Restorations.
- Replications
- Performance Tuning
- Patching
    - operating systems
    - databases

#### What cloud offers
- Almost everything above apart from
    - Performance Tuning:
        - But they provide tools to view query performances
- Backups: We need to just tell how many days of backup we need
- In the case of cloud we are responsible of data in database not the other infra.
- AWS Relational Database services (RDS)
    - mysql/mariadb
    - postgres
    - microsoft sql server
    - oracle
    - IBM DB2
- Azure SQL
    - microsoft sql server
    - postgres
    - mysql/mariadb
