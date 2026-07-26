# Audit Investigation: Suspicious Role Assignment

**Source:** Independent tabletop exercise  
**Status:** Complete case study  
**Severity:** Medium pending authorization verification

## Alert

An audit record shows a privileged directory role assigned outside the normal change window. The goal is to determine whether the change was authorized and whether the account performed follow-on actions.

## Evidence plan

- Directory audit record for the role assignment
- Initiating identity, target identity, role name, and result
- Sign-in records around the event
- Authentication method, device, location, and risk indicators
- PIM activation or approval history
- Related group, application, and policy changes
- Change ticket or administrator confirmation

## Investigation timeline

| Relative time | Event | Analyst interpretation |
|---|---|---|
| T-15 min | Initiator signs in with MFA from a known managed device | Reduces risk but does not prove authorization |
| T0 | Privileged role assignment succeeds | Primary event requiring validation |
| T+4 min | Target account opens an administrative portal | Possible use of newly assigned privilege |
| T+11 min | No policy, application, or credential changes found | Limits observed impact |
| T+25 min | Change owner confirms an approved maintenance action | Supports benign disposition |

## Decision logic

The event is closed as authorized only when the initiating administrator, approval record, target role, duration, and business purpose all agree. A familiar device or successful MFA alone is insufficient.

If authorization cannot be established:

1. remove or expire the role assignment;
2. revoke active sessions for the involved accounts;
3. preserve audit and sign-in evidence;
4. review subsequent administrative actions;
5. reset authentication methods if compromise is suspected; and
6. open an incident with the known facts and confidence level.

## Detection opportunities

- privileged assignment outside PIM;
- role activation without expected approval;
- assignment followed by Conditional Access or authentication-method changes;
- privileged activity from a new device or location; and
- emergency-access account use.

## Outcome

This tabletop case is intentionally resolved as an authorized but poorly documented change. The key lesson is that identity telemetry must be correlated with change-management evidence before assigning an incident disposition.
