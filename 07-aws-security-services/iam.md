# IAM - Identity and Access Management

- It is a global AWS services

## IAM Terminology

- Root account: created by default, should not be used or shared
- Users: are people within our organization
- Groups: groups of users (for example, by department, role, etc.). Groups cannot contain other groups. Users can belong to no group, one group or many groups
- Permissions:
    - Users or groups can be assigned JSON documents named **policies**
    - Policies define the permissions of the user
    - Recommended to use the least privilege principle: don't give more permissions than a user needs
- IAM Roles for Services:
    - Some AWS services will need to perform actions on our behalf
    - To do so, we need to assign permissions to AWS services with the help of IAM Roles
