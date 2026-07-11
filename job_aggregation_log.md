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

## 2026-07-11

**Search window:** last 48 hours (Gmail `newer_than:2d`, run at 2026-07-11).
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri emails at all were found in this window** (job alert
or otherwise). All 20 ranked jobs below come from LinkedIn.

Raw threads matching the search: 13. Of those, 4 were not job-listing alerts (application
status/"viewed"/"sent" notifications for Callaway Digital Technologies, Recykal.com, and
Quillbot) and were excluded. The remaining 9 job-alert/digest threads (10 messages, after
skipping 3 near-identical re-sends of the same digest) yielded 54 unique job postings
after deduping by Company + Role.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | AI Engineer (Agentic Systems) | SureBright | Gurugram, Haryana | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4435785772) |
| 2 | Deputy Manager - Data Science | PepsiCo | Gurugram, Haryana | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4390003782) |
| 3 | Applied Data Scientist | dunnhumby | Gurugram, Haryana | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4437748079) |
| 4 | Analyst-Data Science | American Express | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4415686962) |
| 5 | AI/ML Engineer | AVP Vigilant Technology Pvt Ltd | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4437391350) |
| 6 | Senior Analyst-Data Science | American Express | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4436877141) |
| 7 | Machine Learning Engineer | S&P Global | Hyderabad, Telangana | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4434607893) |
| 8 | Associate AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4438135722) |
| 9 | Machine Learning Engineer | Helfie.AI | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4433935249) |
| 10 | AI Engineer (Computer Vision & Deep Learning) | Tesselonix Private Limited | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4437370579) |
| 11 | AI/ML Developer (Toll industry) | MG | Delhi, India | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4437092390) |
| 12 | Backend Engineer (Node.js/NestJS + AI Agents) | Eazybe | New Delhi | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4437351831) |
| 13 | Associate - AI Engineer I/II | Philips | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4437028963) |
| 14 | AI/ML Engineer | Chubb | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4432236514) |
| 15 | Applied AI Engineer | Clueso | Greater Bengaluru Area | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4437379737) |
| 16 | Data Engineer | Aeris | Gurugram (122002) | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4422482257) |
| 17 | AI Engineer | PayU | Gurgaon | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4401226291) |
| 18 | Data Engineer (AI) | Gresham | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4411883088) |
| 19 | AI Engineer - AI, Data & Platforms | KKR | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4422277100) |
| 20 | Data Scientist (ML/AI) | Philips | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4423244065) |

⚠️ **Consulting/body-shop roles flagged (none landed in today's top 20 — all pushed down
by the company-type sub-score):** EXL, Accenture in India, Bain & Company (x2 postings),
Trigent Software, CodeVyasa, VLink Inc, GlobalLogic, Happiest Minds Technologies, UST,
Mercer, Portage Point Partners, Infosys, Prospect Infosystem Inc., YASH Technologies —
all present in the wider 54-job pool but ranked outside the top 20. Skip these fast if
you see them elsewhere.

### Top 5 companies → cold outreach drafts

Drafts were created in Gmail (not sent) for the top 5 *distinct* companies from the
ranked list: **SureBright, PepsiCo, dunnhumby, American Express, AVP Vigilant Technology
Pvt Ltd**.

| Company | Role targeted | Draft subject | Recipient in draft |
|---|---|---|---|
| SureBright | AI Engineer (Agentic Systems) | ML Engineer - Suryatej - SureBright | `recruiter@surebright.com` (placeholder — unverified domain, replace with a real recruiter's address before sending) |
| PepsiCo | Deputy Manager - Data Science | ML Engineer - Suryatej - PepsiCo | `recruiter@pepsico.com` (placeholder — replace before sending) |
| dunnhumby | Applied Data Scientist | ML Engineer - Suryatej - dunnhumby | `recruiter@dunnhumby.com` (placeholder — replace before sending) |
| American Express | Analyst-Data Science | ML Engineer - Suryatej - American Express | `recruiter@aexp.com` (placeholder — replace before sending) |
| AVP Vigilant Technology Pvt Ltd | AI/ML Engineer | ML Engineer - Suryatej - AVP Vigilant Technology | `recruiter@avpvigilant.com` (placeholder — unverified domain, replace before sending) |

**Note on labeling:** creating/applying the `job-outreach` Gmail label failed again this
run with the same OAuth scope error as 2026-07-08 (`create_label` → 403 "requires
re-authorization" / "upscoping" error), even though drafting and searching worked fine.
Find the 5 drafts by subject prefix `ML Engineer - Suryatej -` in Gmail Drafts. Re-
authorize the Gmail connector with label-management scope to fix this for future runs.
