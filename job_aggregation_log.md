# Daily Job Aggregation Log

Tracks results from the daily Gmail job-alert aggregation run: search window, ranked
job table, consulting/body-shop flags, and the cold-outreach drafts generated for the
top 5 companies each day.

**Candidate stack:** GCP, Vertex AI, BigQuery, Kubeflow, Airflow, LightGBM, XGBoost, Python.
2 years production ML at a UK bank. IIT Guwahati.

**Scoring:** sum of 3 sub-scores (1-5 each) — Role fit (ML Engineer/MLOps/Applied AI/Data
Scientist = 5, adjacent = 3, off-target = 1), Location (Delhi/GGN/Noida = 5, Hyderabad = 4,
Remote India = 4, Bangalore = 3, other = 1), Company type (product/fintech/startup = 5,
consulting/outsourcing = 2, other corporate/GCC = 3). Max score = 15.

---

## 2026-07-08

**Search window:** last 48 hours (2026-07-06 12:37 IST → 2026-07-08 12:37 IST)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails with listings were found in this
window** — only a Naukri promotional/engagement email (no job cards), which was excluded.
All 20 ranked jobs below come from LinkedIn job alert digests.

Raw emails scanned: 9 distinct LinkedIn job-alert digest threads (some duplicated across
multiple alert triggers), yielding 39 unique job postings (deduped by Company + Role)
after filtering out non-job-alert LinkedIn emails (application confirmations, engagement/
newsletter emails, invitation notifications).

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Applied Data Scientist | dunnhumby | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437748079) |
| 2 | Data Scientist | NEMA AI | South Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436520433) |
| 3 | Associate Data Scientist | TriNet | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437174315) |
| 4 | Gen AI Engineer | Experian | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4418958775) |
| 5 | AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434223764) |
| 6 | AI/ML Engineer -Tech Lead | State Street | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437133714) |
| 7 | Machine Learning Engineer | Helfie.AI | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433935249) |
| 8 | Data Scientist (ML/AI) | Philips | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4423244065) |
| 9 | Machine Learning Engineer | Toyota Automated Logistics | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437169500) |
| 10 | Software Engineer, Machine Learning | HARMAN India | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433963822) |
| 11 | Data Scientist II - VR Performance Analytics | Expedia Group | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436246042) |
| 12 | Associate - Data Scientist | United Airlines India Knowledge Center | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437425413) |
| 13 | AI Developer | Ciena | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436234134) |
| 14 | Associate Data Scientist - Enterprise & Reporting | Circle K | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436529087) |
| 15 | Senior Associate — Data Scientist, Applied AI/ML | JPMorganChase | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437456730) |
| 16 | AI ML Engineer | Optum India | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437479077) |
| 17 | AI & Automation Associate | NeoFinity | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436203398) |
| 18 | Gen AI Engineer ⚠️ consulting | BigStep Technologies | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434518783) |
| 19 | Data Scientist ⚠️ consulting | Softkode Technologies | New Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433964604) |
| 20 | ML Engineer | Clean Harbors | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4423595925) |

⚠️ **Consulting/body-shop roles flagged in this batch (skip fast unless desperate):**
BigStep Technologies (#18), Softkode Technologies (#19). Also present in the wider
39-job pool but ranked outside the top 20: PwC Acceleration Center India, Bain & Company,
Deloitte, Luxoft, Accenture in India, EY, L.E.K. Consulting, PwC India, Thought Pilot,
IBM, Infosys — all scored down via the company-type sub-score (2/5) and mostly bumped
further down by weak role fit.

### Top 5 companies → cold outreach drafts

Drafts were created in Gmail (not sent) for the top 5 *distinct* companies from the
ranked list: **dunnhumby, NEMA AI, TriNet, Experian, Optum India**.

| Company | Role targeted | Draft subject | Recipient in draft |
|---|---|---|---|
| dunnhumby | Applied Data Scientist | ML Engineer - Suryatej - dunnhumby | `recruiter@dunnhumby.com` (placeholder — replace with a real recruiter's address before sending) |
| NEMA AI | Data Scientist | ML Engineer - Suryatej - NEMA AI | `talent@nemaai.com` (placeholder — unverified domain, replace before sending) |
| TriNet | Associate Data Scientist | ML Engineer - Suryatej - TriNet | `recruiter@trinet.com` (placeholder — replace before sending) |
| Experian | Gen AI Engineer | ML Engineer - Suryatej - Experian | `recruiter@experian.com` (placeholder — replace before sending) |
| Optum India | AI/ML Engineer | ML Engineer - Suryatej - Optum India | `recruiter@optum.com` (placeholder — replace before sending) |

**Note on labeling:** the `job-outreach` Gmail label could not be created/applied this
run — the connected Gmail account's OAuth grant allows creating drafts but returned a
403/scope error on label management. Find the 5 drafts by subject prefix `ML Engineer -
Suryatej -` in Gmail Drafts until the label issue is resolved (re-authorize the Gmail
connector with label-management scope, then label them manually or re-run).

**Also flagged:** a stray test draft ("test draft - please ignore", thread
`19f41c4d25872fd5`) was created while probing the Gmail connection issue above and
could not be trashed due to the same scope error — delete it manually from Drafts.

---

## 2026-07-14

**Search window:** last 48 hours (2026-07-12 04:37 → 2026-07-14 01:36)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** —
same as the prior run. All 20 ranked jobs below come from LinkedIn job alert
digests and recommendation emails.

Raw emails scanned: 11 LinkedIn emails (2 "jobs you may be interested in" /
saved-job-reminder emails, 9 job-alert digest emails, one digest duplicated across
two alert triggers). Excluded as non-job-alert content: 2 LinkedIn engagement
emails ("X reacted to this post") and 1 newsletter email. Yielded 56 unique job
postings (deduped by Company + Role) after filtering.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Machine Learning Engineer | Opniscience | Gurgaon | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439599070) |
| 2 | Research Engineer - Applied AI/ML | ixigo | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439061772) |
| 3 | Software Development Engineer -AI | Airtel Payments Bank | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439052557) |
| 4 | AI/ML Engineer -Tech Lead | State Street | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437133714) |
| 5 | Machine Learning Engineer | Helfie.AI | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433935249) |
| 6 | Associate Data Scientist | TriNet | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437174315) |
| 7 | Data Science Associate | The Depository Trust & Clearing Corporation (DTCC) | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439046946) |
| 8 | Junior Data Scientist | UPSTA Analytics | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439562311) |
| 9 | Applied Scientist, Traffic Quality | Amazon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4431162871) |
| 10 | Data Scientist | XCaliber Health | Bengaluru East | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439579576) |
| 11 | Applied Scientist II, FinAuto | Amazon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4420937427) |
| 12 | Applied Scientist I | Amazon Science | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4412834723) |
| 13 | Deputy Manager - Data Science | PepsiCo | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4390003782) |
| 14 | Analyst-Data Analytics (Python, SQL, Gen AI) | American Express | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437978853) |
| 15 | Applied Scientist I, Alexa Ads | Amazon Science | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436624922) |
| 16 | AI Engineer | Nomia Ltd | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435970494) |
| 17 | Data Scientist | Applix | Greater Bengaluru Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438308421) |
| 18 | Applied Scientist, Amazon Core Search | Amazon Science | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436630903) |
| 19 | Clinical Prompt Engineer | Truveta | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4411352864) |
| 20 | Associate – AI/ML Innovation Engineer | Amgen | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436740658) |

No consulting/body-shop roles landed in this run's top 20 — all 20 are product
companies, fintechs, startups, or GCCs of non-consulting firms. Consulting/
staffing/outsourcing postings present in the wider 56-job pool but ranked outside
the top 20 (skip fast unless desperate): Luxoft, Deloitte, Accenture in India,
Accenture services Pvt Ltd, Infosys (×2 postings), EXL (×2), UST (×4 postings,
incl. MLOps Engineer and AI Engineer), Maganti IT Resources, Talent500, Jobs
Opportunity (×3 — generic recruiter-posted listings), Tech Economy (×2), ANSR,
RZR, and CloudSutra/Technoidentity Careers.

### Top 5 companies → cold outreach drafts

Drafts were created in Gmail (not sent) for the top 5 *distinct* companies from
the ranked list: **Opniscience, ixigo, Airtel Payments Bank, State Street,
Helfie.AI**.

| Company | Role targeted | Draft subject | Recipient in draft |
|---|---|---|---|
| Opniscience | Machine Learning Engineer | ML Engineer - Suryatej - Opniscience | `careers@opniscience.com` (placeholder — unverified domain, replace before sending) |
| ixigo | Research Engineer - Applied AI/ML | ML Engineer - Suryatej - ixigo | `careers@ixigo.com` (placeholder — replace with a real recruiter's address before sending) |
| Airtel Payments Bank | Software Development Engineer -AI | ML Engineer - Suryatej - Airtel Payments Bank | `careers@airtelbank.com` (placeholder — replace before sending) |
| State Street | AI/ML Engineer -Tech Lead | ML Engineer - Suryatej - State Street | `recruiting@statestreet.com` (placeholder — replace before sending) |
| Helfie.AI | Machine Learning Engineer | ML Engineer - Suryatej - Helfie.AI | `careers@helfie.ai` (placeholder — replace before sending) |

**Note on labeling:** the `job-outreach` Gmail label still could not be
created/applied this run — the connected Gmail account's OAuth grant allows
creating drafts but returns a 403/"requires re-authorization" error on any label
read-write operation (`create_label`, `label_message`, `apply_sensitive_message_label`).
This is the same unresolved issue flagged in the 2026-07-08 run. Find the 5 drafts
by subject prefix `ML Engineer - Suryatej -` in Gmail Drafts until the Gmail
connector is re-authorized with label-management scope (via claude.ai connector
settings), then label them manually or re-run.

**Also flagged:** a stray test draft ("TEST DRAFT - please ignore", id
`r-3635200928529874289`) was created while probing the Gmail label-scope issue
above and could not be trashed due to the same scope error — delete it manually
from Drafts.
