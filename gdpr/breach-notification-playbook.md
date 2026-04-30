# GDPR Data Breach Notification Playbook

> 72 hours from awareness. That is the GDPR clock. This playbook walks through exactly what to do from the moment a potential breach is detected.

---

## GDPR Breach Notification Requirements

**Article 33** — Notification to Supervisory Authority (72 hours)  
**Article 34** — Communication to Data Subjects (without undue delay, if high risk)

**What is a "personal data breach"?**
> A breach of security leading to the accidental or unlawful destruction, loss, alteration, unauthorised disclosure of, or access to, personal data transmitted, stored or otherwise processed.

**Not every breach requires notification:**
- If the breach is **unlikely to result in a risk** to individuals: Log it, no notification required
- If the breach results in a **risk** to individuals: Notify supervisory authority (72 hours)
- If the breach results in a **high risk** to individuals: Also notify affected individuals

---

## Hour-by-Hour Response Timeline

### T+0: Breach Detected / Reported

**Immediate Actions (first 30 minutes):**
```
1. Do NOT dismiss as false positive — treat as real until proven otherwise
2. Preserve evidence (logs, system state, affected files)
3. Notify DPO immediately (within 1 hour)
4. Open incident ticket: INC-GDPR-[YEAR]-[NNN]
5. Start breach assessment
```

---

### T+1 to T+4: Initial Assessment

**DPO-led assessment:**

**1. Confirm breach has occurred:**
- What data was affected? (categories, estimated records)
- How was it accessed/disclosed? (vector, method)
- Is access ongoing or contained?

**2. Scope assessment:**
| Question | Answer |
|----------|--------|
| Personal data involved? | Yes / No |
| Special category data? | Yes / No (health, biometric, criminal, etc.) |
| Children's data? | Yes / No |
| Financial data (PCI)? | Yes / No |
| Number of individuals affected | Estimate |
| Countries of individuals | List |

**3. Risk assessment:**
| Risk Factor | Assessment |
|------------|-----------|
| Nature of data | High / Medium / Low sensitivity |
| Volume | Large / Medium / Small |
| Likely consequence | Identity theft / Financial harm / Reputational / Discrimination |
| Likelihood of harm | High / Medium / Low |
| **Overall risk** | **High / Medium / Low** |

**Decision point:**
- **Low risk** → Document only; no supervisory authority notification required (but best practice to document reasoning)
- **Medium/High risk** → Proceed with supervisory authority notification within 72 hours
- **High risk AND likely significant harm** → Additionally notify affected individuals

---

### T+4 to T+24: Containment & Preparation

**Technical containment:**
- Isolate affected systems if breach ongoing
- Reset compromised credentials
- Block attacker access vectors
- Preserve forensic evidence

**Notification preparation:**
- Draft supervisory authority notification (see template below)
- Identify which supervisory authority (lead authority for multinational organisations)
- Assess whether individual notification required

**Supervisory Authority — EU Lead Authorities:**
| Country | Supervisory Authority |
|---------|----------------------|
| Ireland | Data Protection Commission (DPC) |
| Germany | Multiple Landesbeauftragter |
| France | CNIL |
| Netherlands | Autoriteit Persoonsgegevens |
| UK | ICO (post-Brexit, separate from EU) |

---

### T+24 to T+72: Notification

**Supervisory Authority Notification — Article 33 Template:**

```
TO: [Supervisory Authority Contact]
FROM: [DPO Name], [Organisation]
DATE: [Date/Time]
SUBJECT: Personal Data Breach Notification — Article 33 GDPR

1. NATURE OF THE BREACH
   [Describe what happened: e.g., Unauthorised access to customer database via SQL injection]

2. CATEGORIES AND APPROXIMATE NUMBER OF DATA SUBJECTS
   - Categories: [e.g., Customers — names, email addresses, account numbers]
   - Estimated number: [e.g., approximately 5,000 individuals]
   - Special categories involved: Yes / No [if yes, describe]

3. CATEGORIES AND APPROXIMATE NUMBER OF RECORDS
   - Record types: [e.g., Customer account records]
   - Estimated number: [e.g., 12,000 records]

4. NAME AND CONTACT DETAILS OF DPO
   - Name: [DPO Name]
   - Email: [DPO email]
   - Phone: [DPO phone]

5. LIKELY CONSEQUENCES OF THE BREACH
   [Describe potential harm: e.g., Risk of phishing attacks using disclosed email addresses;
   low risk of financial fraud as no payment data involved]

6. MEASURES TAKEN OR PROPOSED
   - Immediate: [e.g., System isolated, attacker access blocked, passwords reset]
   - Short-term: [e.g., Vulnerability patched, full forensic investigation underway]
   - Long-term: [e.g., WAF implementation, enhanced monitoring]

7. IF NOT NOTIFIED WITHIN 72 HOURS, REASONS FOR DELAY
   [If applicable: describe why 72-hour deadline could not be met and ongoing investigation status]

[Organisation Name] | DPO: [Name] | Notification Date: [DATE/TIME]
```

---

### Individual Notification (If Required — Article 34)

**Required when breach is likely to result in HIGH RISK to individuals** (identity theft, financial harm, discrimination, loss of confidentiality of professional secrets, etc.)

**Individual Notification must include:**
- Nature of the breach (in plain language)
- Contact details of DPO
- Likely consequences of the breach
- Measures taken or proposed
- Recommended actions for individuals to protect themselves

**What NOT to include:**
- Sensitive technical details that could aid attackers
- Information that could create unnecessary panic
- Legally privileged communications

---

## Post-Breach Documentation Requirements

**Article 33(5):** The controller shall document any personal data breaches, comprising the facts relating to the breach, its effects, and the remedial action taken.

Maintain for **minimum 5 years** (best practice):
- Breach incident report
- Risk assessment reasoning
- Notification(s) sent (with timestamps)
- Supervisory authority correspondence
- Individual notifications sent
- Post-incident review report

---
*Template: GDPR Breach Notification Playbook | DPO Resource | Review: Annual*
