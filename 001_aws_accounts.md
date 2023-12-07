# AWS Accounts
An AWS account is a container for identities (users) and Resources. When creating an AWS account you provide an account name e.g PROD, a unique email address and a credit card.  
Every account has a **ROOT USER**, the account **ROOT USER** has full control over all of this AWS account and any resources created within it & can't be restricted.  
Identity and Access Management (IAM) users, groups and roles can also be created and given full or limited permissions.  
Resources bill to the AWS account payment method as they are consumed.  
AWS Accounts can contain the impact of admin errors, or exploits by bad actors. Use separate accounts for separate things (DEV, TEST, PROD) or teams or products or clients.

## IAM Identity and Access Management
Identity and Access Management is a core AWS service you will use as a Solutions Architect.  
IAM is what allows additional identities to be created within an AWS account - identities which can be given restricted levels of access.  
IAM identities start with **no permissions** on an AWS account, but can be granted permissions (almost) up to those held by the Account Root User.  
* Users: Identities which represent humans or applications that need access to your account.
* Group: Collection of related users e.g. development team, finance or HR.
* Role: Can be used by AWS Services, or for granting external access to your account.

