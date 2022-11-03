# IAM: Identity and access management

IAM Identity and access management, a Global Service.

Root account should only be used to set up user account. Then it should only be used to create users and that is all. 

One user per person in ORG. These can be grouped. Groups can't belong to other groups but users can belong to multiple groups.

Why create users and groups?

They can be assigned JSON docs called policies. Which grant access to services. These contain permissions. 

When you apply permissions you use the **least privlege principal** only giving users access to what they need and nothing more. This maintains security. 