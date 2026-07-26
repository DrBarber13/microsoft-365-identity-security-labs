# Conditional Access Design

**Source:** Coursework-derived concepts with an independent security extension  
**Status:** Complete design case study

## Scenario

A fictional hybrid workforce needs stronger authentication without blocking emergency recovery or noninteractive workloads. The design must prevent policy lockout and distinguish users, administrators, guests, and service identities.

## Policy set

| Policy | Scope | Grant/session decision | Key exclusion |
|---|---|---|---|
| Require MFA for administrators | Privileged directory roles | Require strong multifactor authentication | Monitored emergency-access accounts |
| Require MFA for workforce users | Standard users accessing cloud apps | Require MFA | Approved service identities |
| Block legacy authentication | All interactive users | Block unsupported legacy clients | None after compatibility review |
| Protect risky sign-ins | Workforce identities | Require secure authentication or block based on risk | Emergency procedure only |
| Limit unmanaged access | Sensitive applications | Require compliant device or restrict session | Approved exception group |

## Safe deployment sequence

1. Inventory identities, applications, authentication methods, and legacy dependencies.
2. Create two monitored emergency-access identities with separate protections.
3. Build policies in report-only mode.
4. Review projected impact and sign-in telemetry.
5. Test a small pilot group, including expected failures.
6. Enable one policy at a time and monitor help-desk and sign-in results.
7. Record exclusions with an owner, justification, and expiration date.

## Failure-mode analysis

| Failure mode | Preventive control |
|---|---|
| Administrator locks out the tenant | Emergency-access exclusion and change review |
| Service account cannot authenticate | Inventory workload identities before enforcement |
| Legacy client bypasses modern controls | Explicit legacy-authentication block |
| Broad exclusion becomes permanent | Exception owner, expiration, and recurring review |
| MFA fatigue remains possible | Prefer phishing-resistant methods and monitor repeated prompts |

## Validation

Success requires more than a successful user login. The test set includes:

- an administrator challenged for strong authentication;
- a standard user receiving the expected policy;
- a legacy client being denied;
- an unmanaged device receiving the intended restriction;
- an excluded emergency account remaining usable; and
- audit evidence showing who changed the policy and when.

## Limitations

Exact controls and risk features depend on licensing and tenant configuration. This is a security design artifact, not a claim that a current production tenant is configured this way.
