# Cedar Bridge — SOC Foundations & Log Analysis (Labs 1-3)

**Role:** SOC Analyst · **Date:** 6 Oct 2026 (simulated)

A foundational lab series demonstrating core cybersecurity concepts applied to a fictional environment (Cedar Bridge). This project covers risk management, log analysis, network flow, and Linux permissions.

## Scenario
A user (Amara) logged in normally from her office laptop, but minutes later had three failed logins from an unfamiliar external IP, followed by a successful login *without* MFA, and an attempted download of restricted payroll data. 

## Key Takeaways
- **Asset & Risk Management:** Built a risk register for three assets (Invoice Register, Customer Portal, Payroll Export) mapping their primary CIA need, threats, weaknesses, and proposed controls.
- **Authentication vs. Authorization:** Analyzed why the attacker's session (if malicious) was successfully authenticated (due to weak MFA policy) but correctly *denied* authorization to download payroll data (role-based access control worked).
- **Network Flow Analysis:** Mapped the DNS resolution, NAT translation, and firewall inspection points for a laptop connecting to an external website, detailing exactly what a firewall *can* and *cannot* see (TLS limitation).
- **Linux CLI Triage:** Used `grep` and `wc -l` to count failed logins and extract specific event lines from a Linux auth log. Interpreted standard Linux file permissions (`-rw-r-----`).
- **Hypothesis Testing:** Differentiated between benign explanations (user with a typo) and malicious explanations (brute force), outlining the exact evidence needed to prove which is true.

## Repository contents
- `report/`: The final lab workbook (PDF).

## Sanitization note
All IPs are RFC 5737 documentation ranges, all domains use the reserved `.example` TLD, and all data is fictional. No real client data, credentials, or live infrastructure is included.

## Author
**Umar Mohammed**
