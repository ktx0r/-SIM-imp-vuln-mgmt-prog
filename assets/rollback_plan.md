# Change Advisory Board (CAB) Change & Rollback Plan

## Change Title

Vulnerability Remediation – Protocol Hardening and Access Control Improvements

## Change ID

CAB-VM-001

## Change Type

Standard / Scheduled

## Requested By

Security Team

## Date Submitted

<enter date>

---

## 1. Change Summary

This change implements remediation actions identified during vulnerability scanning activities. The objective is to reduce the organization's attack surface and align systems with current security standards.

Remediation actions include:

* Removal of deprecated protocols (TLS 1.0 / 1.1)
* Disabling weak cipher suites
* Removal of unauthorized or outdated software (e.g., Wireshark)
* Removal of guest account administrative privileges

---

## 2. Scope of Change

This change applies to:

* Approximately 200 Windows-based servers
* Core infrastructure and application systems
* Systems identified during credentialed vulnerability scans

---

## 3. Implementation Plan

The change will be deployed using a phased (tiered) approach:

1. Pilot deployment on a limited subset of servers
2. Monitor system performance and application behavior
3. Gradual rollout to remaining server groups
4. Continuous monitoring throughout deployment

All changes will be executed during approved maintenance windows.

---

## 4. Risk Assessment

Potential risks associated with this change include:

* Service disruption due to protocol or cipher modifications
* Compatibility issues with legacy applications
* Authentication or authorization issues after privilege changes

Risk level: **Moderate**, mitigated by staged deployment and rollback readiness.

---

## 5. Rollback Trigger Conditions

Rollback procedures will be initiated if any of the following conditions occur:

* Critical service outage
* Application failures impacting business operations
* Authentication or access failures affecting users or services
* Unexpected system instability

---

## 6. Rollback Plan

If rollback is required, the following steps will be performed:

1. Re-enable previously disabled protocols (TLS 1.0 / 1.1) where necessary
2. Restore prior cipher suite configurations
3. Reinstall removed software if required for operations
4. Restore previous group memberships for affected accounts
5. Restart affected services and systems as needed
6. Validate system stability and functionality

---

## 7. Validation Plan

Post-change validation will include:

* Verification of system availability and uptime
* Confirmation of application functionality
* Review of system and security logs for anomalies
* Follow-up vulnerability scans to confirm remediation success

---

## 8. Backout Time Estimate

Estimated rollback time: 1–2 hours per affected system group

---

## 9. Communication Plan

* Notify stakeholders prior to maintenance window
* Provide status updates during deployment
* Communicate completion and any issues post-change

---

## 10. Management Approval

| Role          | Name   | Status   |
| ------------- | ------ | -------- |
| Change Advisory Board Head | <name> ____________________ | Approved |
| Security Team Manager | <name> ____________________ | Approved |
| Server Team Manager | <name> ____________________ | Approved |

---

## 11. Notes

This change is part of the organization’s Vulnerability Management Program lifecycle and represents the first full remediation cycle following initial scan and analysis.
