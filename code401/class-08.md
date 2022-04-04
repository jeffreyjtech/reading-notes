# Access Control

## Provided Reading Material

### [5 steps to RBAC](https://www.csoonline.com/article/3060780/security/5-steps-to-simple-role-based-access-control.html)

### [wiki - RBAC](https://en.wikipedia.org/wiki/Role-based_access_control)

### [RBAC tutorial](https://www.youtube.com/watch?v=C4NP8Eon3cA)

## My Notes:

**Role-based access control** (RBAC) is a strategy for assigning system access to users based on their role in an organization. Users are assigned roles. Roles are categorizations of employees, which are granted a specific set of rights. Rights are the low-level definitions what is allowed to be done with given document. All together, access to resources in your network is limited only to users to whom those resources are relevant, and access to non-relevant resources are restricted or denied outright.

Implementing RBAC can be done in 5 steps:

1. Systemically find out what resources should require access control
1. Create roles in the RBAC system based on the actual roles present within your workforce.
1. Assign users to their roles within the RBAC.
1. Never give ad-hoc permissions to a single employee, as this exception can undo the purpose of the whole system.
1. Audit roles periodically to assure that capabilities for a role in the RBAC are still appropriate and that the role rosters within the RBAC contain the right people.

There are mutations of the RBAC known as **access control lists** (ACL) and **attribute-based access control** (ABAC). Each gives finer control over resource access:

- Access Control Lists: ACLs define different access levels by user/group AND by document type, thus allowing one group to author and edit one document type while another group can only read that document type.
- Attribute-based Access Control: These systems define different access levels by attributes. Attributes are meant to be mixed-and-matched. This way specific rights can be given to a user if their work requires it. Someone else on the same team as the first user can have different attributes as their work requires.

Roles in RBAC can directly correspond to the hierarchy of the company. Examples of this are:

- A payroll manager will be allowed access to compensation records.
- A project member will be allowed to access project documents
- An HR manager can access employee review records.
