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

