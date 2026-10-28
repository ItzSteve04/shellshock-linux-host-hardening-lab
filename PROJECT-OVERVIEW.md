# Project overview and purpose

## Purpose

Assess how a vulnerable Bash-backed CGI application can lead to command execution on an Ubuntu server, and evaluate what Linux host-hardening measures can reduce the attack surface and limit the consequences of compromise.

## Objectives

1. Build a controlled two-VM environment using Kali Linux as an attacker workstation and Ubuntu as an Apache web server.
2. Research and recreate **Shellshock (CVE-2014-6271)** using intentionally vulnerable Bash and a CGI entry point.
3. Test connectivity and exposure using service discovery, HTTP inspection and vulnerability scanning.
4. Demonstrate initial command execution and distinguish low-privilege access from later root-level escalation.
5. Apply host-hardening measures and document further remediation options.
6. Record technical evidence and evaluate the strengths and limitations of the controls.

## Summary of methodology

The lab used Oracle VirtualBox NAT networking with Kali Linux (attacker) and Ubuntu 20.04 (target web server). Apache CGI was configured to invoke a deliberately vulnerable Bash implementation. The group verified the issue and recorded a limited-access shell, then demonstrated a separate escalation path using an intentionally misconfigured SUID binary. The team documented UFW policy, running-service review, package cleanup, account and password configuration, and Apache temporary-directory isolation.

The PwnKit (CVE-2021-4034) attempt described in the report did not work due to library compatibility issues. It should not be confused with the successful SUID-based escalation demonstration.

## Deliverables and limitations

- Evidence-based project report with screenshots and references.
- Repository documentation on lab architecture, attack sequence and hardening controls.
- Extracted screenshots and two VM configuration images.

No runnable exploit files, complete environment configuration, restored VM images or new test results are included. The repository reflects only the supplied evidence from the completed university project.

## Educational scope

All testing was performed in a controlled, intentionally vulnerable lab. The repository is for learning and portfolio review; it does not document an assessment of a real organisation or production system.

## Team

This was completed as a group project by five contributors. See [CONTRIBUTORS.md](CONTRIBUTORS.md) for names and acknowledgement.
