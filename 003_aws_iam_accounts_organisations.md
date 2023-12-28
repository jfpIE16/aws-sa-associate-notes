# IAM, ACCOUNTS AND AWS ORGANISATIONS
## IAM Identity Policies
You manage access in AWS by creating policies and attaching them to IAM identities (users, groups of users or roles) or AWS resources. A policy is an object in AWS that, when associated with an identity or resource, defines their permissions. AWS evaluates these policies when an IAM principal (user or role) makes a request. IAM policies define permissions for an action regardless of the method that you use to perform the operation.

## Identity-based policies
Identity-based policies are JSON permissions policy documents that control what actions an identity can perform, on which resources and under what conditions.
* Managed policies: Standalone identity-based policies that can attach to multiple users, groups and roles in your AWS account.
* Inline policies: Policies that you add directly to a single user, group or role. Inline policies maintain a strict one-to-one relationship between a policy and an identity.

Managed policies:
* Reusable
* Low Management Overhead

## IAM Users
IAM Users are an identity used for anything requiring long-term AWS access e.g. Humans, Applications or service accounts.
* Authentication is how a principal can prove to IAM that is the identity that it claims to be.
* Authorization is IAM checking the statements that apply to that identity.
* 5000 IAM Users per account
* IAM User can be a member of 10 groups
* This has systems design impacts..
* IAM Roles & Identity Federation fix this
* Internet-scale application
* Large orgs & org merges

## Amazon Resource Name (ARN)
Uniquely identify resources within any AWS accounts.
* **arn:partition:service:region:account-id:resource-id**
* **arn:partition:service:region:account-id:resource-type/resource-id**
* **arn:partition:service:region:account-id:resource-type:resource-id**

## IAM Groups
Are containers for Users. An IAM User can be member of different groups (limit 10). You can add permissions to groups.
* Groups are NOT real identities ... can't be used from resource policies and have no credentials to login with.
* 300 Groups per account.

## IAM Roles
An IAM role is an IAM identity that you can create in your account that has specific permissions. An IAM role is similar to an IAM user, in that it is an AWS identity with permission policies that determine what the identity can and cannot do in AWS. However, instead of being uniquely associated with one person, a role is intended to be assumable by anyone who needs it. Also, a role does not have standard long-term credentials such as a password or access keys associated with it. Instead, when you assume a role, it provides you with temporary security credentials for your role session.

### When to use IAM Roles
You can use roles to delegate access to users, applications, or services that don't normally have access to your AWS resources. For example, you might want to grant users in your AWS account access to resources they don't usually have, or grant users in one AWS account access to resources in another account.

### Service-linked roles
A service-linked role is a unique type of IAM role that is linked directly to an AWS service. Service-linked roles are predefined by the service and include all the permissions that the service requires to call other AWS services on your behalf. The linked service also defines how you create, modify, and delete a service-linked role. A service might automatically create or delete the role. It might allow you to create, modify, or delete the role as part of a wizard or process in the service. Or it might require that you use IAM to create or delete the role.

## AWS Organizations
AWS Organizations is an account management service that enables you to consolidate multiple AWS accounts into an organization that you create and centrally manage. AWS Organizations includes account management and consolidated billing capabilities that enable you to better meet the budgetary, security, and compliance needs of your business. As an administrator of an organization, you can create accounts in your organization and invite existing accounts to join the organization.

### Service Control Policies
Service control policies (SCPs) are a type of organization policy that you can use to manage permissions in your organization. SCPs offer central control over the maximum available permissions for all accounts in your organization. SCPs help you to ensure your accounts stay within your organization’s access control guidelines.

SCPs are available only in an organization that has all features enabled. SCPs aren't available if your organization has enabled only the consolidated billing features. For instructions on enabling SCPs, see Enabling and disabling policy types.

* SCPs are account permissions boundaries
* They limit what the account (including account root user) can do.
* They don't grant permissions.

SCPs DON'T GIVE permission - they just control what an account CAN and CANNOT grant via identity policies.