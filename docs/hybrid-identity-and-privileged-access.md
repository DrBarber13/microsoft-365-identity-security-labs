# Hybrid Identity and Privileged Access

**Source:** Coursework-derived case study, independently rewritten  
**Status:** Complete analytical case study

## Scenario

A fictional organization is moving from basic cloud accounts to managed Microsoft 365 identities. Administrators need repeatable user lifecycle controls, least-privilege role assignment, auditable activity, hybrid authentication, and time-bound privileged access.

The reviewed coursework contained task evidence and reflections covering tenant initialization, licensing, groups, administrative delegation, monitoring, identity synchronization, secure authentication, and Privileged Identity Management. The original worksheets and screenshots are not included.

## Administrative capabilities practiced

### Tenant and identity foundations

- Assigned service licenses and verified access
- Created collaboration and security groups
- Managed users, owners, members, and administrative roles
- Reviewed organization-wide settings and release preferences

### Least privilege and automation

- Applied role-based administrative delegation
- Used Microsoft Graph PowerShell concepts for directory operations
- Practiced deleted-object recovery and role assignment workflows
- Verified that delegated administrators received only their intended capabilities

### Monitoring and troubleshooting

- Enabled or reviewed unified audit capabilities
- Investigated mail-delivery failures and diagnostic headers
- Used service-health information to distinguish platform incidents from tenant configuration issues
- Reviewed support and troubleshooting pathways

### Hybrid identity

- Worked with Microsoft Entra Connect concepts
- Compared password-hash synchronization, pass-through authentication, and federation
- Configured and verified pass-through authentication in a lab
- Reviewed Smart Lockout and password-protection controls

### Privileged Identity Management

- Located the PIM administration workflow
- Configured approval requirements for sensitive roles
- Assigned eligible rather than permanently active privileges
- Practiced request, approval, activation, and verification steps

## Security reasoning

Permanent global privileges create avoidable exposure. A stronger design combines:

- Role-based access aligned to job duties
- Eligible, time-bound privileged assignments
- Approval for sensitive activation
- Audit evidence for administrative actions
- Emergency-access planning
- Regular access review

The public model uses fictional roles such as `Helpdesk Operator`, `Security Reader`, and `Privileged Role Administrator`. Real tenant IDs, domains, emails, object IDs, tokens, and browser-session details are excluded.

## Validation matrix

| Control | Positive test | Negative test | Evidence |
|---|---|---|---|
| Delegated administration | Helpdesk operator performs an approved password-reset workflow | Operator cannot change privileged role assignments | Directory audit records and denied-action result |
| Graph reporting | Read-only query returns selected directory metadata | Mutation request is not authorized | Sanitized command shape and permission review |
| Pass-through authentication | Test identity completes the intended sign-in flow | Disabled test identity is denied | Sign-in record and authentication detail |
| PIM eligibility | Eligible administrator activates a role after approval | Role is unavailable outside the activation window | PIM audit history and role-assignment state |
| Emergency access | Excluded emergency identity remains available under the documented procedure | Routine use triggers review | Sign-in monitoring and access-review record |

## Skills demonstrated

Microsoft 365 administration, Microsoft Entra ID, licensing, user and group lifecycle, RBAC, Microsoft Graph PowerShell, audit logging, service health, hybrid authentication, Smart Lockout, and PIM.

## Limitations

The original submissions contain school instructions and lab identities, so they remain private. This public artifact demonstrates the control design, administrator reasoning, and validation method without claiming a current production tenant deployment.
# Hybrid Identity and Privileged Access

**Source:** Coursework-derived case study, independently rewritten  
**Status:** Skills documented; independent tenant revalidation and sanitized evidence pending

## Scenario

A fictional organization is moving from basic cloud accounts to managed Microsoft 365 identities. Administrators need repeatable user lifecycle controls, least-privilege role assignment, auditable activity, hybrid authentication, and time-bound privileged access.

The reviewed coursework contained task evidence and reflections covering tenant initialization, licensing, groups, administrative delegation, monitoring, identity synchronization, secure authentication, and Privileged Identity Management. The original worksheets and screenshots are not included.

## Administrative capabilities practiced

### Tenant and identity foundations

- Assigned service licenses and verified access
- Created collaboration and security groups
- Managed users, owners, members, and administrative roles
- Reviewed organization-wide settings and release preferences

### Least privilege and automation

- Applied role-based administrative delegation
- Used Microsoft Graph PowerShell concepts for directory operations
- Practiced deleted-object recovery and role assignment workflows
- Verified that delegated administrators received only their intended capabilities

### Monitoring and troubleshooting

- Enabled or reviewed unified audit capabilities
- Investigated mail-delivery failures and diagnostic headers
- Used service-health information to distinguish platform incidents from tenant configuration issues
- Reviewed support and troubleshooting pathways

### Hybrid identity

- Worked with Microsoft Entra Connect concepts
- Compared password-hash synchronization, pass-through authentication, and federation
- Configured and verified pass-through authentication in a lab
- Reviewed Smart Lockout and password-protection controls

### Privileged Identity Management

- Located the PIM administration workflow
- Configured approval requirements for sensitive roles
- Assigned eligible rather than permanently active privileges
- Practiced request, approval, activation, and verification steps

## Security reasoning

Permanent global privileges create avoidable exposure. A stronger design combines:

- Role-based access aligned to job duties
- Eligible, time-bound privileged assignments
- Approval for sensitive activation
- Audit evidence for administrative actions
- Emergency-access planning
- Regular access review

The independent rebuild will use fictional accounts such as `analyst01@example.com` and will avoid real tenant IDs, domains, emails, object IDs, tokens, and browser-session details.

## Independent validation plan

1. Create fictional users and groups in a disposable tenant or approved sandbox.
2. Assign a limited administrative role and verify both permitted and denied actions.
3. Run a redacted Microsoft Graph query that does not expose tokens or object IDs.
4. Configure a safe PIM demonstration where licensing permits.
5. Review sign-in and audit evidence.
6. Capture sanitized screenshots with tenant and identity details removed.

## Skills demonstrated

Microsoft 365 administration, Microsoft Entra ID, licensing, user and group lifecycle, RBAC, Microsoft Graph PowerShell, audit logging, service health, hybrid authentication, Smart Lockout, and PIM.

## Limitations

The original submissions contain school instructions and lab identities, so they are evidence for private review only. Public screenshots and commands must come from a new, independently documented environment.
