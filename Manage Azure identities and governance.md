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
