# AWS Fundamentals
## Public vs Private Services
Is related from a network perspective.
### AWS Private Zone
**VPCs** are isolated unless configured otherwise.
### AWS Public Zone
This is where AWS public services operate from.  
* On-premises can access VPCs only if configured via VPN or Direct Connect.
* Access to AWS public via IGW.
* Private services can be fiven a public IP - 1:1 translated by the IGW.
* Access to internet via IGW.

## AWS Global Architecture
### Region
Is an area of the world that AWS selected and inside this region is a full deployment of AWS architecture (Full compute, storage, DB, AI, etc.). Regions are geographically spread.  
Benefits:
* Geographic separation - isolated fault domain
* Geopolitical separation - Different governance
* Location control - Performance

#### Availability zones
Isolated infrastructure inside a region. Connected with high speed redundant network.

### Edge locations
Are smaller than regions and generally they only have content distribution services as well some types of edge computing. Low latency and high speed distribution.


### Service Resilience
* Globally Resilient -> IAM, Route53
* Region Resilient -> VPC
* AZ Resilient


## Virtual private cloud (VPC) Basics
A virtual network inside AWS and is within 1 account & 1 region. Is private and isolated unless you decide otherwise.
1. Default VPC is created once per region when an AWS account is first created.
   1. One per region - can be removed & recreated.
   2. Default VPC CIDR is always 172.31.0.0/16
   3. /20 Subnet in each AZ in the region
   4. Internet Gateway (IGW), Security Group (SG) & NACL
   5. Subnets assign public IPv4 addresses
2. Custom VPCs.

## Elastic Compute Cloud (EC2) Basics
Provide access to virtual machines known as instances. Compute power. Infrastructure as a service, your unite of consumption is the instance.
* IAAS - Provides virtual machines
* Private service by-default - uses VPC networking
* AZ Resilient - Instance fails if AZ fails
* Different instance sizes and capabilities
* On-Demand billing - Per second
* Local on-host storage or Elastic Block Store (EBS)

### Instance Lifecycle
* Running / Is billed all time.
* Stopped / Charges only for storage.
* Terminated &rarr; Irreversible action / No charges since you delete disks.

### Amazon Machine Image (AMI)
An Amazon Machine Image (AMI) is a supported and maintained image provided by AWS that provides the information required to launch an instance. You must specify an AMI when you launch an instance. You can launch multiple instances from a single AMI when you require multiple instances with the same configuration. You can use different AMIs to launch instances when you require instances with different configurations.

### Connection to EC2
1. Windows &rarr; RDP protocol
2. Linux &rarr; SSH using a key-pair.

## Simple Storage Service (S3)
Is a core AWS service. Default storage service in AWS.
* Global Storage Platform - regional based/resilient.
* Public service, unlimited data & multi-user
* ... Movies, Audio, Photos, Text, Large Data sets
* Economical & accessed via UI/CLI/API/HTTP

### Objects
Conceptually an object is associated to a file.
* Key &rarr; file name.
* Value &rarr; content being stored. Zero bytes ... 5TB.
* Version ID
* Metadata
* Access Contro
* Subresources

### Buckets
A bucket is created in an specific region. The bucket name needs to be globally unique across all regions and accounts. Everything is stored at a root level it doesn't work as a filesystem.

### S3 Patterns and Anti-patterns
* S3 is an object store - not file or block
* You can´t mount an S3 bucket.
* Great for large scale data storage, distribution or upload
* Great for offload
* INPUT and/or OUTPUT to many AWS products


## CloudFormation Basics
Is a tool that allows us to create, update and delete infrastructure in an automated way. You could use YAML or JSON format to automate infrastructure operations. Templates are used to create stacks, which are used to interact with resources in an AWS account.  

## CloudWatch Basics
CloudWatch is a core supporting service within AWS which provides metrics, logs and event management services. It's used through other AWS services for health and performance monitoring, log management and neverless architectures.
* Collects and manages operational data
* Metrics - AWS Products, Apps, on-premises
* Logs - AWS Products, Apps, on-premises
* Events - AWS Services & Schedules

A metric is a collection of different data points time ordered. For example, CPU Usage, Network, Disk IO.
Dimensions separate datapoints for different things or perspectives within the same metric. An alarm is setted within a metric and take actions when the defined value matchs the conditions.

## CloudWatch Logs
* Public Service - Usable from AWS or on-premises.
* Store, Monitor and access logging data.
* AWS Integrations - EC2, VPC Flow Logs, Lambda, CloudTrail, Route53 and more...
* Can generate metrics based on logs - metric filter.

## CloudTrail
* Logs API calls/activities as a CloudTrail Event
* 90 days stored by default in Event History
* Enabled by default - no cost for 90 day history
* To customize the service .. create 1 or more Trails
* Trails are how you configure S3 and CWLogs
* Management Events and Data Events
* Not realtime - there is a delay

## AWS Control Tower
AWS Control Tower offers a straightforward way to set up and govern an AWS multi-account environment, following prescriptive best practices. AWS Control Tower orchestrates the capabilities of several other AWS services, including AWS Organizations, AWS Service Catalog, and AWS IAM Identity Center (successor to AWS Single Sign-On), to build a landing zone in less than an hour. Resources are set up and managed on your behalf.

AWS Control Tower orchestration extends the capabilities of AWS Organizations. To help keep your organizations and accounts from drift, which is divergence from best practices, AWS Control Tower applies preventive and detective controls (guardrails). For example, you can use guardrails to help ensure that security logs and necessary cross-account access permissions are created, and not altered.

## HA - FT - DR
* High-Availability &rarr; Aims to ensure an agreed level of operational performance, usually uptime, for a higher than normal period. Minimize outages.
* Fault-Tolerance &rarr; Is the property that enables a system to continue operating properly in the event of the failure of some (one or more faults within) of its components. Operate through failure.
* Disaster-Recovery &rarr; Is a set of policies, tools and procedures to enable the recovery or continuation of vital technology infrastructure and systems following a natural or human-induced disaster.


## Route53
AWS managed DNS product.
1. Register Domains
2. Host Zones.. managed nameservers

* Global Service &rarr; single database
* Globally Resilient

### Hosted zones
* Zone files in AWS
* Hosted on four managed name servers
* Can be public..
* Or private &rarr; linked to VPC's
* .. Stores records (recordsets)

### DNS Record Types
* Nameserver (NS)
* A and AAAA Records &rarr; Host to IP (v4 or v6)
* CNAME records &rarr; Canonical name, Host to Host
* MX Records &rarr; A mail. Find a mail server (SMTP) for a domain.
* TXT Records &rarr; Add attributes

#### DNS TTL - Time To Live

# Key Management Service (KMS)
AWS Key Management Service (AWS KMS) makes it easy for you to create and manage cryptographic keys and control their use across a wide range of AWS services and in your applications. AWS KMS is a secure and resilient service that uses hardware security modules that have been validated under FIPS 140-2, or are in the process of being validated, to protect your keys.
* Regional & Public Service
* Create, Store and Manage Keys
* Symmetric and Asymmetric Keys
* Cryptographic operations (encrypt, decrypt & ...)
* Keys never leave KMS - Provides FIPS 140-2 (L2)
* KMS Keys are logical - ID, date, policy, desc & state
* ... backed by physical key material
* Generated or imported
* KMS Keys can be used for up to 4KB of data

Data encryption Keys
* GeneratedDataKey - works on > 4KB
* Plaintext Version
* Ciphertext
* Encrypt data using plaintext key
* Discard
* Store encrypted key with data

Key concepts
* KMS Keys are isolated to a region & never leave
* AWS Owned & customer owned
* Customer owned ... AWS Managed or customer managed keys
* Customer managed keys are more configurable
* KMS Keys support rotation
* Backing Key (and previous backing keys)
* Aliases