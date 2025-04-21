# AWS Service Control Policies (SCP) Collection

## Why Service Control Policies (SCPs) Are Important
In AWS Organizations, Service Control Policies (SCPs) are a crucial governance tool.
They allow you to centrally manage permissions across all accounts in your organization, helping you:

- Enforce security best practices at scale

- Prevent accidental or malicious actions

- Align account activities with your compliance and governance requirements

- Ensure consistent configurations across environments (development, staging, production)


✨ Important: SCPs do not grant permissions — they only restrict them. Users must still have IAM permissions to perform actions.

# SCP Policies Included
Here’s a list of the SCP policies available in this repository:


| SCP Filename                              | Description                                                                                   |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|
| `deny-creating-iam-users.json`            | Denies the creation of new IAM users.                                                         |
| `deny-disabling-security-services.json`   | Denies disabling security services like AWS Security Hub or GuardDuty.                        |
| `deny-leaving-organization.json`          | Prevents an AWS account from leaving the organization.                                        |
| `deny-modifying-ou.json`                  | Denies modification of Organizational Units (OUs) inside the AWS Organization.                |
| `deny-modifying-service-roles.json`       | Denies changes to AWS Service-linked roles (roles managed by AWS services).                   |
| `deny-root-account-activity.json`         | Completely blocks the use of the root account for any activity.                               |
| `require-tag-ec2.json`                    | Requires specific tags to be provided when launching new EC2 instances.                       |
| `restrict-access-to-listed-services.json` | Restricts access to only a predefined list of AWS services.                                   |
| `restrict-regions.json`                   | Restricts usage of AWS services to specific approved regions only.                            |
