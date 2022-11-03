# IAM: Identity and access management

IAM Identity and access management, a Global Service.

Root account should only be used to set up user account. Then it should only be used to create users and that is all. 

One user per person in ORG. These can be grouped. Groups can't belong to other groups but users can belong to multiple groups.

Why create users and groups?

They can be assigned JSON docs called policies. Which grant access to services. These contain permissions. 

When you apply permissions you use the **least privlege principal** only giving users access to what they need and nothing more. This maintains security. 

## IAM Policies

Policeis assigned at the group level will be inherited by users in the group. 

There are also inline policies which apply to an individual. 

Users in more than one group will inherit policies from all groups. 

Polices consist of...

- Version: Policy language version, always include "2012-10-17"
- Id: an identifier for the policy(optional) 
- Statement: One or more individual statements (required)

Statements consist of...

- Sid: An identifier for the statement (OPtional)
- Effect: whether the statement allows or denies access (Boolean - "Allow"/"Deny")
- Principal: account/user/role that policy is applied to. 
- Action: List of resources this policy allows/denies
-Resource: List of resources to which the actions are applied to
- Condition: Conditions for when this policy is in effect (Optional)

## Account Security

In AWS you can set a password policy. Strong passwords = more account security.

### Password policy

Options for Password policy:

- Set minimum password length
- Require specific characters
  - include uppercase
  - include lowercase
  - numbers
  - non-alphanumeric
- Allow users to change thier passwords freely
- Require users to change thier passwords after a set amount of time. (Expiration)
- Prevent password reuse

### MFA - Multi-factor authentication

- Users have access to your account and can possibly change configurations or delete resources in your AWS account.
- You want to protect your Root Accts and IAM users
- A MFA = A Password you know + Security device you own.
- Even if an account is compromised, they require a physuical device 

MFA Device options

- Virtual MFA Device
  - Google Authenticator
    - Phone Only
  - Authy
    - Phone and Computer
      - Support for multiple accounts on same device
- Universal 2nd factor U2F Security Key (Physical device)
  - YubiKey by Yubico (3rd party)
    - Supports many users and root accounts with a single key
  - Hardware Key fob MFA
    - Gemalto (3rd Party)
  - Hardware Key FOB MFA device for AWS GovCloud
    - SurePassID (3rd Party)

## AWS Access Keys, CLI and SDK

There are three options to access AWS

- AWS Management Console (Web interface - User + Pass + MFA)
- AWS Command Line interface (CLI): Protected by access keys
- AWS Software Developer Kit (SDK): - for code: protected by access Keys

- Access keys are generated through the Management Console. 
- Users manage thier own access keys
- **Access Keys are Secret, Just like a password. DO NOT SHARE**
- Access Key ID ~= username
- Secret Access Key ~= password

### What is AWS CLI

AWS CLI is a command line interface tahe enables you to interact with AWS using your command line shell. 

Gives direct access to the public APIs of AWS services. This allows you to run scripts to manage your resources.

It is open source, and a good alternative to using AWS Managment Console.

### What is AWS SDK

- AWS Software Development Kit
- LAnguage Specific APIs (Libraries)
- Enables you to access and manage AWS Programaticalyly
- embedded within your application
- Supports
  - SDKs (JS, Python, PHP, .NET, Ruby, Java, Go, Node.js, C++)
  - Mobile SDKS (Android, iOS)
  IoI Device SDKs (Embedded D, Arduino)
- AWS CLI is built on AWS SDK Python

## AWS Cloudshell 

Virtual CLI, you can use it and it will default to the region being used in. If you want to specify a specific region for use use the `--region` modifier `aws iam list-users --region us-east-1`

Your cloud shell environment has a full repository and you can download and upload files. 

You can also creat new terminal tabs.

