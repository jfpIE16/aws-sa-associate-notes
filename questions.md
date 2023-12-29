# Final questions
1. Which set of Amazon S3 features helps to prevent and recover from accidental data loss?
* Object versioning and Multi-factor authentication.

2. What is the minimum time Interval for the data that Amazon CloudWatch receives and aggregates?
* One minute.

3. A user has launched an EC2 instance. The instance got terminated as soon as it was launched. Which of the below mentioned options is not a possible reason for this?
* The user account has reached the maximum EC2 instance limit.

4. Your website is serving on-demand training videos to your workforce. Videos are uploaded monthly in high resolution MP4 format. Your workforce is distributed globally often on the move and using company-provided tablets that require the HTTP Live Streaming (HLS) protocol to watch a video. Your company has no video transcoding expertise and it required you may need to pay for a consultant. How do you implement the most cost-efficient architecture without compromising high availability and quality of video delivery'?
* EBS volumes to host videos and EBS snapshots to incrementally backup original files after a few days. CloudFront to serve HLS transcoded videos from EC2.

5. You are designing an intrusion detection prevention (IDS/IPS) solution for a customer web application in a single VPC. You are considering the options for implementing IOS IPS protection for traffic coming from the Internet. Which of the following options would you consider? (Choose 2 answers)
* Implement IDS/IPS agents on each Instance running in VPC.
* Implement a reverse proxy layer in front of web servers and configure IDS/ IPS agents on each reverse proxy server.

6. Which of the following are valid statements about Amazon S3? (Choose 2 answers)
*  A successful response to a PUT request only occurs when a complete object is saved.
*  S3 provides eventual consistency for overwrite PUTS and DELETE.

7. How can the domain's zone apex, for example, 'myzoneapexdomain.com', be pointed towards an Elastic Load Balancer?
*  By using an Amazon Route 53 Alias record.

8. When should I choose Provisioned IOPS over Standard RDS storage?
*  If you have batch-oriented workloads.

9. Your department creates regular analytics reports from your company's log files All log data is collected in Amazon S3 and processed by daily Amazon Elastic MapReduce (EMR) jobs that generate daily PDF reports and aggregated tables in CSV format for an Amazon Redshift data warehouse. Which of the following alternatives will lower costs without compromising average performance of the system or data integrity for the raw data?
* Use reduced redundancy storage (RRS) for PDF and .csv data in Amazon S3. Add Spot Instances to Amazon EMR jobs. Use Reserved Instances for Amazon Redshift.

10. Because of the extensibility limitations of striped storage attached to Windows Server, Amazon RDS does not currently support increasing storage on a [...] DB Instance.
* SQL Server.

11. In regards to IAM you can edit user properties later, but you cannot use the console to change the [...].
* user name

12. In Amazon ECS Container Service, are other container types supported?
*  No, Docker is the only container platform supported by EC2 Container Service presently.

13. Content and Media Server is the latest requirement that you need to meet for a client. The client has been very specific about his requirements such as low latency, high availability, durability, and access control. Potentially there will be millions of views on this server and because of 'spiky' usage patterns, operations teams will need to provision static hardware, network, and management resources to support the maximum expected need. The Customer base will be initially low but is expected to grow and become more geographically distributed. Which of the following would be a good solution for content distribution?
*  Amazon S3 as the origin server and Amazon CloudFront for caching.

14. Name the disk storage supported by Amazon Elastic Compute Cloud (EC2)
* Amazon Instance Store.

15. After an Amazon VPC instance is launched, can I change the VPC security groups it belongs to?
* Yes. You can.

16. If I want an instance to have a public IP address, which IP address should I use?
*  Elastic IP Address.

17. Amazon RDS supports SOAP only through [...].
* HTTPS

18. Which of the following services natively encrypts data at rest within an AWS region? (Choose 2 answers)
* AWS Storage Gateway
* Amazon Glacier

19. Which one of the following can't be used as an origin server with Amazon CloudFront?
*  Amazon Glacier.

20. Select the most correct The device name /dev/sdal (within Amazon EC2) is [...].
*  reserved for the root device.

21. How can I change the security group membership for interfaces owned by other AWS, such as Elastic Load Balancing?
*  By using the service specific console or API/CLI commands.

22. You have created a Route 53 latency record set from your domain to a machine in Northern Virginia and a similar record to a machine in Sydney. When a user located in US visits your domain he will be routed to
*  Northern Virginia.

23. In the context of MySQL, version numbers are organized as MySQL version = X.Y.Z. What does X denote here?
* Major version

24. Which one of the below doesn't affect Amazon CloudFront billing?
*  Distribution Type.

25. Just when you thought you knew every possible storage option on AWS you hear someone mention Reduced Redundancy Storage (RRS) within Amazon S3. What is the ideal scenario to use Reduced Redundancy Storage (RRS)?
*  Non-critical or reproducible data.

26. When running my DB Instance as a Multi-AZ deployment, can I use the standby for read or write operations?
* No.

27. In the Launch Db Instance Wizard, where can I select the backup and maintenance options?
*  Under MANAGEMENT OPTIONS.

28. What is the network performance offered by the c4.8xlarge instance in Amazon EC2?
* 10 Gigabit

29. In Amazon EC2, if your EBS volume stays in the detaching state, you can force the detachment by clicking [...].
* Force detach

30. What does Amazon DynamoDB provide?
*  A fast, highly scalable managed NoSQL database service.

31. Security groups act like a firewall at the instance level, whereas [...] are an additional layer of security that act at the subnet level.
* ACL's

32. You have been asked to tighten up the password policies in your organization after a serious security breach, so you need to consider every possible security measure. Which of the following is not an account password policy for IAM Users that can be set?
*  Force IAM users to contact an account administrator when the user has entered his password incorrectly.

33. Multi-AZ deployment [...] supported for Microsoft SQL Server DB Instances.
* is not currently.

34. What does Amazon Elastic Beanstalk provide?
*  An application container on top of Amazon Web Services.

35. You need to quickly set up an email-sending service because a client needs to start using it in the next hour. Amazon Simple Email Service (Amazon SES) seems to be the logical choice but there are several options available to set it up. Which of the following options to set up SES would best meet the needs of the client?
*  Amazon SES console.

36. A user is observing the EC2 CPU utilization metric on CloudWatch. The user has observed some interesting patterns while filtering over the 1 week period for a particular hour. The user wants to zoom that data point to a more granular period. How can the user do that easily with CloudWatch?
*  The user can zoom a particular period by selecting that period with the mouse and then releasing the mouse.

37. A company is running a batch analysis every hour on their main transactional DB. running on an RDS MySQL instance to populate their central Data Warehouse running on Redshift During the execution of the batch their transactional applications are very slow When the batch completes they need to update the top management dashboard with the new data The dashboard is produced by another system running on-premises that is currently started when a manually-sent email notifies that an update is required The on-premises system cannot be modified because is managed by another team. How would you optimize this scenario to solve performance issues and automate the process as much as possible? How would you optimize this scenario to solve performance issues and automate the process as much as possible?
*  Replace RDS with Redshift for the batch analysis and SNS to notify the on-premises system to update the dashboard.

38. You are configuring a new VPC for one of your clients for a cloud migration project, and only a public VPN will be in place. After you created your VPC, you created a new subnet, a new internet gateway, and attached your internet gateway to your VPC. When you launched your first instance into your VPC, you realized that you aren't able to connect to the instance, even if it is configured with an elastic IP. What should be done to access the instance?
*  A route should be created as 0.0.0.0/0 and your internet gateway as target.

39. You have been asked to build a database warehouse using Amazon Redshift. You know a little about it, including that it is a SQL data warehouse solution, and uses industry standard ODBC and JDBCconnections and PostgreSQL drivers. However you are not sure about what sort of storage it uses for database tables. What sort of storage does Amazon Redshift use for database tables?
*  Columnar data storage.

40. A user has attached 1 EBS volume to a EC2 instance. The user wants to achieve the best fault tolerance of data possible. Which of the below mentioned options can help achieve fault tolerance?
*  Attach one more volume with RAID 1 configuration.

41. Which features can be used to restrict access to data in S3? (Choose 2 answers)
*  Set an S3 ACL on the bucket or the object.
*  Set an S3 bucket policy.

42. You are in the process of creating a Route 53 DNS failover to direct traffic to two EC2 zones. Obviously, if one fails, you would like Route 53 to direct traffic to the other region. Each region has an ELB with some instances being distributed. What is the best way for you to configure the Route 53 health check?
*  Route 53 natively supports ELB with an internal health check. Turn 'Evaluate target health' on and 'Associate with Health Check' off and R53 will use the ELB's internal health check.

43. For each DB Instance class, what is the maximum size of associated storage capacity?
* 1TB

44. A user is planning a highly available application deployment with EC2. Which of the below mentioned options will not help to achieve HA?
* Provisioned IOPS

45. What does specifying the mapping /dev/sdc=none when launching an instance do?
*  Prevents /dev/sdc from attaching to the instance.

46. Which of the following statements is true of tagging an Amazon EC2 resource?
*  You can't terminate, stop, or delete a resource based solely on its tags.

47. You are deploying an application to collect votes for a very popular television show. Millions of users will submit votes using mobile devices. The votes must be collected into a durable, scalable, and highly available data store for real-time public tabulation. Which service should you use?
* Dynamo DB

48. Are Reserved Instances available for Multi-AZ Deployments?
*  Yes for all instance types.

49. A [...] for a VPC is a collection of subnets (typically private) that you may want to designate for your backend RDS DB Instances.
* DB Subnet group

50. An instance is launched into a VPC subnet with the network ACL configured to allow all inbound traffic and deny all outbound traffic. The instance's security group is configured to allow SSH from any IPaddress and deny all outbound traffic. What changes need to be made to allow SSH access to the instance?

*  The outbound network ACL needs to be modified to allow outbound traffic.

51. You can modify the backup retention period; valid values are 0 (for no backup retention) to a maximum of [...] days.
* 365

52. To serve Web traffic for a popular product your chief financial officer and IT director have purchased 10 ml large heavy utilization Reserved Instances (RIs) evenly spread across two Availability Zones: Route 53 is used to deliver the traffic to an Elastic Load Balancer (ELB). After several months, the product grows even more popular and you need additional capacity As a result, your company purchases two C3.2xlarge medium utilization RIs You register the two c3 2xlarge instances with your ELB and quickly find that the ml large instances are at 100% of capacity and the c3 2xlarge instances have significant capacity that's unused Which option is the most cost effective and uses EC2 capacity most effectively?
*  Configure ELB with two c3 2xiarge Instances and use on-demand Autoscaling group for up to two additional c3.2xlarge instances Shut on mi .large instances.

53. An existing application stores sensitive information on a non-boot Amazon EBS data volume attached to an Amazon Elastic Compute Cloud instance. Which of the following approaches would protect the sensitive data on an Amazon EBS volume?
*  Create and mount a new, encrypted Amazon EBS volume. Move the data to the new volume. Delete the old Amazon EBS volume.

54. A user has launched one EC2 instance in the US West region. The user wants to access the RDS instance launched in the US East region from that EC2 instance. How can the user configure the access for that EC2 instance?
*  Configure the IP range of the US West region instance as the ingress security rule of RDS.

55. You have been asked to build AWS infrastructure for disaster recovery for your local applications and within that you should use an AWS Storage Gateway as part of the solution. Which of the following best describes the function of an AWS Storage Gateway?
*  Connects an on-premises software appliance with cloud-based storage to provide seamless and secure integration between your on-premises IT environment and AWS's storage infrastructure.

56. While creating an Amazon RDS DB, your first task is to set up a DB [...] that controls which IP address or EC2 instance can access your DB Instance.
* security group

57. You need to import several hundred megabytes of data from a local Oracle database to an Amazon RDS DB instance. What does AWS recommend you use to accomplish this?
* Oracle Data Pump.

58. In the context of AWS support, why must an EC2 instance be unreachable for 20 minutes rather than allowing customers to open tickets immediately?
*  Because most reachability issues are resolved by automated processes in less than 20 minutes.

59. HTTP Query-based requests are HTTP requests that use the HTTP verb GET or POST and a Query parameter named [...].
* Action

60. A friend tells you he is being charged $100 a month to host his WordPress website, and you tell him you can move it to AWS for him and he will only pay a fraction of that, which makes him very happy. He then tells you he is being charged $50 a month for the domain, which is registered with the same people that set it up, and he asks if it's possible to move that to AWS as well. You tell him you aren't sure, but will look into it. Which of the following statements is true in regards to transferring domain names to AWS?
*  You can transfer existing domains into Amazon Route 53's management.

61. While creating the snapshots using the command line tools, which command should I be using?
* ec2-create-snapshot

62. All Amazon EC2 instances are assigned two IP addresses at launch, out of which one can only be reached from within the Amazon EC2 network?
* Private IP address

63. When an EC2 instance that is backed by an S3-based AMI is terminated, what happens to the data on the root volume?
*  Data is automatically deleted.

64. You've created your first load balancer and have registered your EC2 instances with the load balancer. Elastic Load Balancing routinely performs health checks on all the registered EC2 instances and automatically distributes all incoming requests to the DNS name of your load balancer across your registered, healthy EC2 instances. By default, the load balancer uses the [...] protocol for checking the health of your instances.
* HTTP

65. Amazon Elastic Load Balancing is used to manage traffic on a fleet of Amazon EC2 instances, distributing traffic to instances across all Availability Zones within a region. Elastic Load Balancing has all the advantages of an on-premises load balancer, plus several security benefits. Which of the following is not an advantage of ELB over an on-premise load balancer?
*  ELB uses a four-tier, key-based architecture for encryption.

66. A web company is looking to implement an external payment service into their highly available application deployed in a VPC Their application EC2 instances are behind a public lacing ELB Auto scaling is used to add additional instances as traffic increases under normal load the application runs 2 instances in the Auto Scaling group but at peak it can scale 3x in size. The application instances need to communicate with the payment service over the Internet which requires whitelisting of all public IP addresses used to communicate with it. A maximum of 4 whitelisting IP addresses are allowed at a time and can be added through an API. How should they architect their solution?
*  Automatically assign public IP addresses to the application instances in the Auto Scaling group and run a script on boot that adds each instances public IP address to the payment validation whitelist AP.

67. You are using Amazon SES as an email solution but are unsure of what its limitations are. Which statement below is correct in regards to that?
*  Every Amazon SES sender has a unique set of sending limits.

68. Your company is getting ready to do a major public announcement of a social media site on AWS. The website is running on EC2 instances deployed across multiple Availability Zones with a Multi-AZ RDS MySQL Extra Large DB Instance. The site performs a high number of small reads and writes per second and relies on an eventual consistency model. After comprehensive tests you discover that there is read contention on RDS MySQL. Which are the best approaches to meet these requirements? (Choose 2 answers)
*  Deploy ElasticCache in-memory cache running in each Availability Zone.
*  Add an RDS MySQL read replica in each Availability Zone.

69. What does a 'Domain' refer to in Amazon SWF?
*  A collection of related Workflows.

70. The SQL Server [...] feature is an efficient means of copying data from a source database to your DB Instance. It writes the data that you specify to a data file, such as an ASCII file.
* bulk copy

71. Any person or application that interacts with AWS requires security credentials. AWS uses these credentials to identify who is making the call and whether to allow the requested access. You have just set up a VPC network for a client and you are now thinking about the best way to secure this network. You set up a security group called vpcsecuritygroup. Which following statement is true in respect to the initial settings that will be applied to this security group if you choose to use the default settings for this group?
*  Allow no inbound traffic and allow all outbound traffic.

72. Which one of the below is not an AWS Storage Service?
*  Amazon CloudFront.

73. You are trying to launch an EC2 instance, however the instance seems to go into a terminated status immediately. What would probably not be a reason that this is happening?
*  You need to create storage in EBS first.

74. A company is building software on AWS that requires access to various AWS services. Which configuration should be used to ensure mat AWS credentials (i.e., Access Key ID/Secret Access Key combination) are not compromised?
* Assign an IAM role to the Amazon EC2 instance

75. Can we attach an EBS volume to more than one EC2 instance at the same time?
* Yes

76. You need to measure the performance of your EBS volumes as they seem to be under performing. You have come up with a measurement of 1,024 KB I/O but your colleague tells you that EBS volume performance is measured in IOPS. How many IOPS is equal to 1,024 KB I/O?
* 4 

77. You are designing Internet connectivity for your VPC. The Web servers must be available on the Internet. The application must have a highly available architecture. Which alternatives should you consider? (Choose 2 answers)
*  Place all your web servers behind ELB Configure a Route 53 CNAME to point to the ELB DNS name.
*   Assign EIPs to all web servers. Configure a Route 53 record set with all EIPs. With health checks and DNS failover.

78. You need to configure an Amazon S3 bucket to serve static assets for your public-facing web application. Which methods ensure that all objects uploaded to the bucket are set to public read? (Choose 2 answers)
*  Set permissions on the object to public read during upload.
*  Configure the bucket policy to set all objects to public read.


