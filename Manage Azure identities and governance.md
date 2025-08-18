## Manage Azure identities and governance

in a free Microsoft Entra ID tenant, you can only assign licenses to individual users like User1. Group-based licensing (for Group1 or Group2) requires a paid version of Microsoft Entra ID (such as P1 or P2).

`SSPR` can be directly assigned only to a group of users or to ALL users but not to individual users.

- in order to configure Self-Service Password Reset (SSPR) in Microsoft Entra, a user must have at least the Authentication Policy Administrator role.
- Self-Service Password Reset (SSPR) can be enabled for security groups and Microsoft 365 groups.

`Azure  Entra ID licenses `can be assigned to user accounts directly or to groups, which then assign the licenses to all group members. According to the official documentation, licenses can be assigned to Microsoft 365 groups and security groups, but they must be security-enabled.

The `User Access Administrator` role allows to manage access for other users on that resource, including assigning roles and permissions. This role provides the capability to delegate access without providing permissions to modify the resource itself.

Only users with the Global Administrator or Authentication Administrator roles have the necessary permissions to modify security questions in the SSPR settings.

in a free Microsoft Entra ID tenant, you can only assign licenses to individual users like User1. Group-based licensing (for Group1 or Group2) requires a paid version of Microsoft Entra ID (such as P1 or P2).

 `Security Admin `role is focused on managing security-related policies and configurations but does not grant the ability to manage access to a

`custom security attributes` in Microsoft Entra ID can only be assigned to `users` and `service principals` (enterprise applications). 

Azure supports Azure role assignment conditions for Blob Storage containers and Queue Storage. This means you can apply conditional access controls—such as limiting access by IP address, resource tags, or actions—when assigning RBAC roles to these services. This feature enhances fine-grained access control, enabling you to enforce least privilege principles more effectively.

By default, Azure applies a two-gate password reset policy for all administrator accounts. This two-gate policy requires two pieces of authentication data, such as an email address, authenticator app, or phone number, and does not permit the use of security questions for administrators.
the regular SSPR policy does not apply to users in administrative roles, such as Security Administrator. Administrators must go through a two-gate policy to reset their password, which differs from the standard SSPR process configured for non-admin users. 

Nnesting is supported for groups that can be assigned a role.
 Azure role assignments do not support nested groups when the nested group is a Microsoft 365 group.

`Co-administrator `role can only be assigned at the subscription level. This role grants the same access as the built-in Owner role but does not allow modifying role assignments within the subscription.