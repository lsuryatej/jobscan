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

## 2026-07-09

**Search window:** last 48 hours (2026-07-07 12:37 IST → 2026-07-09 IST)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window at
all** (zero matching threads) — the connected inbox does not appear to receive
Naukri alerts currently. All jobs below come from LinkedIn.

Raw emails scanned: 9 distinct LinkedIn job-alert/digest threads. Initial HTML-based
extraction was unreliable (tracking-link corruption caused some job IDs to bleed
across cards), so extraction was redone from each email's plaintext body, which
cleanly lists Title/Company/Location/"View job" per card. This yielded 53 unique
job postings after deduping by Company + Role. Many postings (dunnhumby, NEMA AI,
TriNet, Experian, Optum India, State Street, Helfie.AI, Toyota, HARMAN, Circle K,
United Airlines, Ciena, BigStep, Softkode, Clean Harbors) are recurring alerts for
the same live listings as 2026-07-08, confirmed by matching LinkedIn job IDs.
New postings today include several Amsterdam-based roles (Adyen, Booking.com,
TomTom, Mistral, Xomnia, Da Vinci, Elsevier, Cocoroco.com, Planner 5D — all
off-target on location, scored low) and new India roles (Amgen, S&P Global,
Prismforce, SureBright, Sitetracker, JioStar, Honeywell, PwC (x2), Bain & Company,
Deloitte, Luxoft, Accenture in India, Lonza, Advance Auto Parts, NeoFinity,
Qualys, Thought Pilot, IBM, Infosys, Lowe's India, L.E.K. Consulting).

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Data Scientist | NEMA AI | South Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436520433) |
| 2 | AI Engineer (Agentic Systems) | SureBright | Gurugram, Haryana, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435785772) |
| 3 | Applied Data Scientist | dunnhumby | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437748079) |
| 4 | Gen AI Engineer | Experian | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4418958775) |
| 5 | Machine Learning Engineer | Helfie.AI | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433935249) |
| 6 | AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434223764) |
| 7 | AI/ML Engineer -Tech Lead | State Street | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437133714) |
| 8 | Associate Data Scientist | TriNet | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437174315) |
| 9 | Associate Data Scientist - Enterprise & Reporting | Circle K | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436529087) |
| 10 | Data Scientist II - VR Performance Analytics | Expedia Group | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436246042) |
| 11 | Senior Associate — Data Scientist, Applied AI/ML | JPMorganChase | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437456730) |
| 12 | AI & Automation Associate | NeoFinity | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436203398) |
| 13 | AI ML Engineer | Optum India | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437479077) |
| 14 | Data Scientist - LLM Training and Fine Tuning | Prismforce | Bengaluru, Karnataka, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436948519) |
| 15 | Associate - Data Scientist | United Airlines India Knowledge Center | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437425413) |
| 16 | Associate Data Scientist | Amgen | Hyderabad, Telangana, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433337253) |
| 17 | Gen AI Engineer ⚠️ consulting | BigStep Technologies | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434518783) |
| 18 | ML Engineer | Clean Harbors | Hyderabad, Telangana, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4423595925) |
| 19 | Machine Learning & LLM Engineer ⚠️ consulting | L.E.K. Consulting | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436061210) |
| 20 | Data Scientist | Lonza | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437758229) |

⚠️ **Consulting/body-shop roles flagged in this batch (skip fast unless desperate):**
BigStep Technologies (#17), L.E.K. Consulting (#19). Also present in the wider
53-job pool but ranked outside the top 20: Softkode Technologies, Deloitte,
Luxoft, Accenture in India, PwC Acceleration Center India, PwC India, Bain &
Company, Xomnia, EY, Infosys — all scored down via the company-type sub-score
(2/5) and mostly bumped further down by weaker location/role fit.

**Also flagged (not consulting, but off-target role — skip fast):** Sitetracker's
"AI Developer - Salesforce Admin" (Salesforce admin work, not ML) and JioStar's
"Senior Executive - Social Media Marketing" both showed up in LinkedIn's digest
under ML-adjacent subject lines but are not ML roles at all; both scored low and
fell well outside the top 20.

### Top 5 companies → cold outreach drafts

Drafts were created in Gmail (not sent) for the top 5 *distinct* companies from the
ranked list: **NEMA AI, SureBright, dunnhumby, Experian, Helfie.AI**.

| Company | Role targeted | Draft subject | Recipient in draft |
|---|---|---|---|
| NEMA AI | Data Scientist | ML Engineer - Suryatej - NEMA AI | `recruiter@nemaai.com` (placeholder — unverified domain, replace before sending) |
| SureBright | AI Engineer (Agentic Systems) | ML Engineer - Suryatej - SureBright | `recruiter@surebright.com` (placeholder — unverified domain, replace before sending) |
| dunnhumby | Applied Data Scientist | ML Engineer - Suryatej - dunnhumby | `recruiter@dunnhumby.com` (placeholder — replace with a real recruiter's address before sending) |
| Experian | Gen AI Engineer | ML Engineer - Suryatej - Experian | `recruiter@experian.com` (placeholder — replace before sending) |
| Helfie.AI | Machine Learning Engineer | ML Engineer - Suryatej - Helfie.AI | `recruiter@helfie.ai` (placeholder — unverified domain, replace before sending) |

**Note on labeling:** the `job-outreach` Gmail label still could not be created or
applied this run — `create_label`, `label_message`, and `apply_sensitive_message_label`
all failed with a token/scope re-authorization error (read operations and
`create_draft` work fine, so this is a scoped-permissions issue, not a full outage).
Same unresolved issue as 2026-07-08. Find today's 5 drafts by subject prefix
`ML Engineer - Suryatej -` in Gmail Drafts until the Gmail connector is
re-authorized with label-management scope.

## 2026-07-10

**Search window:** last 48 hours (2026-07-08 ~04:36 IST → 2026-07-10 ~06:06 IST)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window.**
All jobs below come from LinkedIn job-alert digests, "jobs picked for you," and
similar-jobs notifications.

Raw emails scanned: 18 LinkedIn threads in the window; 6 were excluded as
non-job-alert noise (application-viewed/sent confirmations, an engagement/reactions
digest). The remaining 12 job-alert/digest emails yielded 59 unique job postings
(by LinkedIn job ID), 57 after deduping identical Company + Role combinations
(e.g. duplicate "AI Engr I at Honeywell Technologies" postings, duplicate "Data
Engineer at Aeris" postings across locations).

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Senior Analyst-Data Science | American Express | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436877141) |
| 2 | Machine Learning Ops Engineer | Inovalon | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4362256862) |
| 3 | Applied Data Scientist | dunnhumby | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437748079) |
| 4 | Associate Data Scientist | Amgen | Hyderabad, Telangana, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433337253) |
| 5 | Machine Learning Engineer | Helfie.AI | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433935249) |
| 6 | Associate AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438135722) |
| 7 | AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434223764) |
| 8 | Machine Learning Engineer | S&P Global | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434607893) |
| 9 | AI/ML Engineer -Tech Lead | State Street | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437133714) |
| 10 | Associate Data Scientist - Enterprise & Reporting | Circle K | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436529087) |
| 11 | Associate - Data Scientist | United Airlines India Knowledge Center | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437425413) |
| 12 | Data Scientist | Affluense | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436869995) |
| 13 | Data Scientist II - VR Performance Analytics | Expedia Group | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436246042) |
| 14 | Data Scientist | Fast Code AI | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436561944) |
| 15 | Senior Associate — Data Scientist, Applied AI/ML | JPMorganChase | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437456730) |
| 16 | Data Scientist - LLM Training and Fine Tuning | Prismforce | Bengaluru, Karnataka, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436948519) |
| 17 | Data Scientist | TWID | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436579954) |
| 18 | Data Engineer | Aeris | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4422482257) |
| 19 | Data Engineer (AI) | Gresham | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4411883088) |
| 20 | AI Engineer - AI, Data & Platforms | KKR | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4422277100) |

⚠️ **Consulting/body-shop roles flagged (skip fast unless desperate):** none landed
in today's top 20. In the wider 57-job pool, ranked outside the top 20 and scored
down via the company-type sub-score (2/5): Portage Point Partners (#28, financial
advisory), Trigent Software - Professional Services (#29, IT staffing), Accenture
in India (#30), GlobalLogic (#33), Luxoft (#35), Bain & Company (#42 and #54, two
separate roles), BigStep Technologies (#43), Mercer (#44), Deloitte (#47), Prospect
Infosystem Inc. (#52), and PwC Acceleration Center India (#55).

Also excluded from the ranking pool as off-target on role fit (score 1): "AI
Developer - Salesforce Admin" at Sitetracker, "Associate Software Developer" at
Advance Auto Parts India, and "Associate – Data Ops & Estimations" at Bain &
Company. A batch of Amsterdam-based roles (Booking.com, TomTom, Mistral, Xomnia,
Da Vinci, Elsevier, Cocoroco.com, Planner 5D) surfaced via a "similar jobs" digest
but scored low on location (1/5, non-India) and were excluded from the top 20.

### Top 5 companies → cold outreach drafts

Drafts were created in Gmail (not sent) for the top 5 *distinct* companies from the
ranked list: **American Express, Inovalon, dunnhumby, Amgen, Helfie.AI**.

| Company | Role targeted | Draft subject | Recipient in draft |
|---|---|---|---|
| American Express | Senior Analyst-Data Science | ML Engineer - Suryatej - American Express | `recruiting@aexp.com` (placeholder — replace with a real recruiter's address before sending) |
| Inovalon | Machine Learning Ops Engineer | ML Engineer - Suryatej - Inovalon | `recruiting@inovalon.com` (placeholder — replace before sending) |
| dunnhumby | Applied Data Scientist | ML Engineer - Suryatej - dunnhumby | `recruitment@dunnhumby.com` (placeholder — replace before sending) |
| Amgen | Associate Data Scientist | ML Engineer - Suryatej - Amgen | `recruiting@amgen.com` (placeholder — replace before sending) |
| Helfie.AI | Machine Learning Engineer | ML Engineer - Suryatej - Helfie.AI | `careers@helfie.ai` (placeholder — unverified domain, replace before sending) |

**Note on labeling:** the `job-outreach` Gmail label could not be created this run
either — `create_label` returned "MCP server Gmail requires re-authorization (token
expired)," the same recurring scope issue noted on 2026-07-08. Drafts were created
successfully; find them by subject prefix `ML Engineer - Suryatej -` in Gmail
Drafts until the Gmail connector is re-authorized with label-management scope,
then label them manually (or re-run this step once fixed).

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

## 2026-07-12

**Search window:** last 48 hours (2026-07-10 ~10:06 IST → 2026-07-12 ~06:06 IST)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs" / "jobs for you"). **No Naukri job-alert emails were found in this
window** (checked out to a 3-day window as a sanity check — still zero). All 20 ranked
jobs below come from LinkedIn job alert digests and reminder emails.

Raw emails scanned: 11 LinkedIn threads (13 messages) in the window — a mix of job-alert
digests, a "similar jobs" recommendation digest, and "saved job" apply reminders. Two
threads were pure application-confirmation emails ("Your application to ... at Callaway
Digital Technologies", "... at Recykal.com") and were excluded as non-alerts. Parsing the
remaining threads yielded 62 unique job postings (by LinkedIn job ID), which collapsed to
59 after deduping by Company + Role (AVP Vigilant Technology's "AI/ML Engineer" and
American Express's "Analyst-Data Science" each appeared as separate postings in two
different cities and were merged).

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Analyst-Data Science | American Express | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4415686962) |
| 2 | Applied Data Scientist | dunnhumby | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437748079) |
| 3 | Machine Learning Engineer | Helfie.AI | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433935249) |
| 4 | Machine Learning Engineer | S&P Global | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434607893) |
| 5 | Deputy Manager - Data Science | PepsiCo | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4390003782) |
| 6 | AI/ML Developer (Toll industry) | MG | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437092390) |
| 7 | Associate AI/ML Engineer – Predictive Maintenance | Boeing | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435943294) |
| 8 | Applied Data Scientist — Medical AI & Model Fine Tuning | Clinvvo | Greater Bengaluru Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435976099) |
| 9 | Machine Learning Engineer | Spydra | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435980095) |
| 10 | Applied AI Engineer | Clueso | Greater Bengaluru Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437379737) |
| 11 | Backend Engineer (Node.js/NestJS + AI Agents) | Eazybe | New Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437351831) |
| 12 | AI Engineer (Computer Vision & Deep Learning) | Tesselonix Private Limited | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437370579) |
| 13 | Quantitative Developer (Python) | Open Futures Group | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437962673) |
| 14 | Forward Deployed Engineer - Gen AI & Voice AI (Backend Engineer) - Delhi | Blue Machines AI | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438886777) |
| 15 | Artificial Intelligence Engineer | SKV (Studiokon Ventures Private Limited) | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439000797) |
| 16 | AI/ML Engineer ⚠️ consulting | EXL | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434892560) |
| 17 | AI / ML Engineer ⚠️ consulting | Accenture in India | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438282279) |
| 18 | ML Engineer | Clean Harbors | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4423595925) |
| 19 | Adv. Data Scientist II, SIP | Invesco | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438665939) |
| 20 | Associate AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439044122) |

⚠️ **Consulting/body-shop roles flagged in this batch (skip fast unless desperate):**
EXL (#16), Accenture in India (#17). Also present in the wider 59-job pool but ranked
outside the top 20: Quanteon Solutions, ARNsofttech, Jade Global, Maganti IT Resources
LLC, Viraaj HR Solutions, AVP Vigilant Technology, VLink Inc, UST, Adept Global, Axtria -
Ingenious Insights, SourcingXPress, Happiest Minds Technologies, Teamware Solutions,
Asian Hires, Innova ESI, and EXL's second posting (Senior Manager) — all scored down via
the company-type sub-score (2/5) for being staffing/IT-services/BPO shops.

### Top 5 companies → cold outreach drafts

Drafts were created in Gmail (not sent) for the top 5 *distinct* companies from the
ranked list: **American Express, dunnhumby, Helfie.AI, S&P Global, PepsiCo**.

| Company | Role targeted | Draft subject | Recipient in draft |
|---|---|---|---|
| American Express | Analyst-Data Science | ML Engineer - Suryatej Lalam - American Express | `recruiter@americanexpress.com` (placeholder — replace with a real recruiter's address before sending) |
| dunnhumby | Applied Data Scientist | ML Engineer - Suryatej Lalam - dunnhumby | `recruiter@dunnhumby.com` (placeholder — replace before sending) |
| Helfie.AI | Machine Learning Engineer | ML Engineer - Suryatej Lalam - Helfie.AI | `talent@helfie.ai` (placeholder — unverified domain, replace before sending) |
| S&P Global | Machine Learning Engineer | ML Engineer - Suryatej Lalam - S&P Global | `recruiter@spglobal.com` (placeholder — replace before sending) |
| PepsiCo | Deputy Manager - Data Science | ML Engineer - Suryatej Lalam - PepsiCo | `talent@pepsico.com` (placeholder — replace before sending) |

**Note on labeling:** same limitation as the 2026-07-08 run — `create_label` for
`job-outreach` failed with a token/scope re-authorization error, even though reading
existing labels (`list_labels`) and creating drafts both work fine. The label still does
not exist in the mailbox. Find the 5 drafts by subject prefix `ML Engineer - Suryatej
Lalam -` in Gmail Drafts until this is resolved (re-authorize the Gmail connector with
label-management scope, then label them manually or re-run this step).

## 2026-07-13

**Search window:** last 48 hours (2026-07-11 ~04:37 IST → 2026-07-13 ~00:37 IST)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window.** All 20
ranked jobs below come from LinkedIn.

Raw emails scanned: 12 distinct LinkedIn threads in the window — 1 was a "reacted to
this post" social notification (excluded, not a job alert) and 11 were job-alert digests
or saved/viewed-job reminders. Those 11 threads yielded 69 individual job listings, which
deduped by Company + Role (and after excluding 2 Executive Assistant postings as clearly
off-target on role) came to **67 unique job postings** considered for ranking.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Research Engineer - Applied AI/ML | ixigo | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439061772) |
| 2 | Artificial Intelligence Engineer | SKV (Studiokon Ventures Private Limited) | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439000797) |
| 3 | Forward Deployed Engineer - Gen AI & Voice AI (Backend Engineer) | Blue Machines AI | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438886777) |
| 4 | AI/ML Engineer -Tech Lead | State Street | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437133714) |
| 5 | Machine Learning Engineer | Helfie.AI | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433935249) |
| 6 | Associate Data Scientist | TriNet | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437174315) |
| 7 | Data Science Associate | The Depository Trust & Clearing Corporation (DTCC) | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439046946) |
| 8 | Applied AI Engineer | Convatec | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439091242) |
| 9 | Artificial Intelligence Engineer | Blend | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4425626254) |
| 10 | Machine Learning Engineer | S&P Global | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434607893) |
| 11 | Associate AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439044122) |
| 12 | Adv. Data Scientist II, SIP | Invesco | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438665939) |
| 13 | Artificial Intelligence Engineer | Ameriprise Financial Services, LLC | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435883622) |
| 14 | Associate - AI Engineer (CTE) | Tech Economy | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438319649) |
| 15 | AI Engineer - Agentic AI & Automation | LUXASIA | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438631482) |
| 16 | Applied Scientist I | Amazon Science | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4412834723) |
| 17 | Associate AI/ML Engineer – Predictive Maintenance | Boeing | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435943294) |
| 18 | Applied AI/ML Senior Associate | JPMorganChase | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438881311) |
| 19 | MLOps Engineer (Bangalore, KA, IN, 560037) | Vestas | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438916474) |
| 20 | Applied Data Scientist — Medical AI & Model Fine Tuning | Clinvvo | Greater Bengaluru Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435976099) |

⚠️ **Consulting/body-shop/staffing roles flagged in the wider 67-job pool (skip fast,
none made the top 20):** EXL (2 postings), UST (3 postings: ML Engineer I, MLOps
Engineer, AI Engineer), "Jobs Opportunity" generic recruiter postings (3), Quanteon
Solutions, ARNsofttech, AVP Vigilant Technology, Jade Global, Maganti IT Resources,
Viraaj HR Solutions, Teamware Solutions, Asian Hires, Innova ESI, Adept Global,
SourcingXPress, Axtria - Ingenious Insights, RZR, ANSR, CloudSutra — all scored down via
the company-type sub-score (2/5) for being staffing/outsourcing/consulting shops.

### Top 5 companies → cold outreach drafts

Drafts were created in Gmail (not sent) for the top 5 *distinct* companies from the
ranked list: **ixigo, SKV (Studiokon Ventures), Blue Machines AI, State Street,
Helfie.AI**.

| Company | Role targeted | Draft subject | Recipient in draft |
|---|---|---|---|
| ixigo | Research Engineer - Applied AI/ML | ML Engineer - Suryatej - ixigo | `recruiter@ixigo.com` (placeholder — replace with a real recruiter's address before sending) |
| SKV (Studiokon Ventures) | Artificial Intelligence Engineer | ML Engineer - Suryatej - SKV (Studiokon Ventures) | `careers@studiokonventures.com` (placeholder — unverified domain, replace before sending) |
| Blue Machines AI | Forward Deployed Engineer - Gen AI & Voice AI | ML Engineer - Suryatej - Blue Machines AI | `talent@bluemachines.ai` (placeholder — replace before sending) |
| State Street | AI/ML Engineer -Tech Lead | ML Engineer - Suryatej - State Street | `recruiter@statestreet.com` (placeholder — replace before sending) |
| Helfie.AI | Machine Learning Engineer | ML Engineer - Suryatej - Helfie.AI | `talent@helfie.ai` (placeholder — replace before sending) |

**Note on labeling:** same recurring issue as 2026-07-08 — the connected Gmail
account's OAuth grant allows creating drafts (read + draft-create scopes) but
`create_label` still returns a token re-authorization error, so the `job-outreach`
label could not be created or applied this run either. Find the 5 drafts by subject
prefix `ML Engineer - Suryatej -` in Gmail Drafts. This needs a one-time
re-authorization of the Gmail connector (with label-management scope) from the
claude.ai connector settings to fix permanently.

## 2026-07-14

**Note:** this run supersedes an earlier same-day run (search window ending
01:36) — refreshed later in the day per a second trigger, so this section
reflects the latest scan rather than appending a second `## 2026-07-14` header.

**Search window:** last 48 hours (2026-07-12 10:36 → 2026-07-14 10:36)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** —
same as every prior run; this inbox does not appear to receive Naukri alerts.
All 20 ranked jobs below come from LinkedIn job alert digests and recommendation
emails.

Raw emails scanned: 11 LinkedIn threads (12 messages — one thread had 2 alert
triggers), covering job-alert digests, "jobs that match your profile"
recommendations, a saved-job "apply now" reminder, and a "similar jobs" email.
Excluded as non-job-alert content: 1 weekly-performance notification, 2
engagement emails ("X reacted to this post"), and 1 editorial newsletter email.
Yielded 62 unique job postings (deduped by Company + Role) after filtering.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Machine Learning Engineer | Opniscience | Gurgaon | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439599070) |
| 2 | Research Engineer - Applied AI/ML | ixigo | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439061772) |
| 3 | AI/ML Engineer -Tech Lead | State Street | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437133714) |
| 4 | Machine Learning Engineer | Helfie.AI | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433935249) |
| 5 | Associate Data Scientist | TriNet | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437174315) |
| 6 | Generative AI Engineer (RAG) | NextMantra AI | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437243970) |
| 7 | Data Scientist | Euromonitor International | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439147979) |
| 8 | AI Research Engineer - Applied AI | PlexTrac | Greater Bengaluru Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4417039358) |
| 9 | Applied Scientist, Traffic Quality | Amazon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4431162871) |
| 10 | Data Scientist | XCaliber Health | Bengaluru East | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439579576) |
| 11 | Data Scientist | Ecolab | Bengaluru East | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4402621132) |
| 12 | Applied Scientist II, FinAuto | Amazon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4420937427) |
| 13 | Applied Scientist I | Amazon Science | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4412834723) |
| 14 | Deputy Manager - Data Science | PepsiCo | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4390003782) |
| 15 | Analyst-Data Analytics (Python, SQL, Gen AI) | American Express | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437978853) |
| 16 | Software Development Engineer -AI | Airtel Payments Bank | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439052557) |
| 17 | AI/ML Engineer ⚠️ consulting | Blend Consulting & Training India Pvt. Ltd. | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437556949) |
| 18 | AI Graduate Engineer Trainee | Twinings | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439135741) |
| 19 | Jr ML Engineer | Baseforge Technologies | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439144232) |
| 20 | Associate - AI/ML Innovation Engineer | Amgen | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436754165) |

Only one consulting/staffing posting landed in this run's top 20: Blend
Consulting & Training India Pvt. Ltd. (#17, flagged above — skip fast). More
consulting/staffing/outsourcing postings are present in the wider 62-job pool
but ranked outside the top 20 (skip fast unless desperate): Accenture services
Pvt Ltd, Jobs Opportunity (×2 — generic recruiter-posted listings), UST,
Luxoft, Accenture in India, Maganti IT Resources, Talent500, Deloitte, Infosys
(×2), Capgemini, EXL (×2), PwC India, and Automatic Infotech.

### Top 5 companies → cold outreach drafts

Top 5 by score: **Opniscience, ixigo, State Street, Helfie.AI, TriNet.** Four
of these five (Opniscience, ixigo, State Street, Helfie.AI) are unchanged from
this morning's earlier run today and already have outreach drafts in Gmail
(created 01:40 IST) — no duplicate drafts were created for them. Only
**TriNet** is new to today's top 5, so a single new draft was created for it.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| Opniscience | Machine Learning Engineer | ML Engineer - Suryatej - Opniscience | `careers@opniscience.com` (placeholder) | already drafted this morning — skipped |
| ixigo | Research Engineer - Applied AI/ML | ML Engineer - Suryatej - ixigo | `careers@ixigo.com` (placeholder) | already drafted this morning — skipped |
| State Street | AI/ML Engineer -Tech Lead | ML Engineer - Suryatej - State Street | `recruiting@statestreet.com` (placeholder) | already drafted this morning — skipped |
| Helfie.AI | Machine Learning Engineer | ML Engineer - Suryatej - Helfie.AI | `careers@helfie.ai` (placeholder) | already drafted this morning — skipped |
| TriNet | Associate Data Scientist | ML Engineer - Suryatej - TriNet | `recruiter@trinet.com` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` Gmail label still could not be
created this run — `create_label` now fails with "MCP server Gmail requires
re-authorization (token expired)", the same unresolved issue flagged in every
prior run. Find outreach drafts by subject prefix `ML Engineer - Suryatej -`
in Gmail Drafts until the Gmail connector is re-authorized (via claude.ai
connector settings), then label them manually or re-run.


## 2026-07-15

**Search window:** last 48 hours (2026-07-13 07:10 → 2026-07-15 07:10 IST)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** —
same as every prior run; this inbox does not appear to receive Naukri alerts.
All 20 ranked jobs below come from LinkedIn job alert digests and recommendation
emails.

Raw emails scanned: 9 relevant LinkedIn threads (one thread had 2 alert
triggers with the same job card, deduped), covering job-alert digests, "jobs
that match your profile" recommendations, and a "similar jobs" email.
Excluded as non-job-alert content: 1 weekly-performance notification, 1
engagement email ("X reacted to this post"), and 1 editorial newsletter email.
Yielded 44 unique job postings (deduped by Company + Role) after filtering.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Machine Learning Engineer | Opniscience | Gurgaon | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439599070) |
| 2 | Jr ML Engineer | Baseforge Technologies | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439144232) |
| 3 | Associate Data Engineer/Scientist | Barri Financial Group | Bangalore Urban | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437214732) |
| 4 | Generative AI Engineer (RAG) | NextMantra AI | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437243970) |
| 5 | AI Research Engineer - Applied AI | PlexTrac | Greater Bengaluru Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4417039358) |
| 6 | Data Scientist | XCaliber Health | Bengaluru East | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439579576) |
| 7 | Applied Scientist, Traffic Quality | Amazon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4431162871) |
| 8 | Applied Scientist II, FinAuto | Amazon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4420937427) |
| 9 | AI Software Engineer — Remote | Pluvus | India (Remote) | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437942804) |
| 10 | AI Engineer II (Remote) | Sezzle | India (Remote) | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4378063866) |
| 11 | Associate - AI/ML Innovation Engineer | Amgen | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436754165) |
| 12 | Engineer - ML tools | Qualcomm | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4386878569) |
| 13 | Engineer I, AI Engineering | LPL Financial Global Capability Center | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4371020579) |
| 14 | AI/ML Engineer ⚠️ consulting | Blend Consulting & Training India Pvt. Ltd. | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437556949) |
| 15 | Platform Engineer | XCaliber Health | Bengaluru East | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439584280) |
| 16 | Software Engineer, AI/ML | Google | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4390913792) |
| 17 | AI Engineer - 1 | GTMfund | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439784227) |
| 18 | Applied AI Engineer | BJAK | India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437971362) |
| 19 | Machine Learning Engineer | Shuru | India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437137985) |
| 20 | Data Scientist | Euromonitor International | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439147979) |

Only one consulting/staffing posting landed in this run's top 20: Blend
Consulting & Training India Pvt. Ltd. (#14, flagged above — skip fast). More
consulting/staffing/outsourcing postings are present in the wider 44-job pool
but ranked outside the top 20 (skip fast unless desperate): PwC India
(Advisory), Luxoft, Accenture in India, IQVIA, Automatic Infotech, Capgemini,
Maganti IT Resources LLC, Deloitte, Talent500, and Infosys.

### Top 5 companies → cold outreach drafts

Top 5 by score: **Opniscience, Baseforge Technologies, Barri Financial Group,
NextMantra AI, PlexTrac.** All five are newly created drafts this run (no
prior drafts existed for these exact company + role pairs).

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| Opniscience | Machine Learning Engineer | ML Engineer - Suryatej Lalam - Opniscience | `careers@opniscience.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Baseforge Technologies | Jr ML Engineer | ML Engineer - Suryatej Lalam - Baseforge Technologies | `careers@baseforge.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Barri Financial Group | Associate Data Engineer/Scientist | ML Engineer - Suryatej Lalam - Barri Financial Group | `careers@barrifinancial.com` (placeholder — unverified, replace before sending) | new draft created this run |
| NextMantra AI | Generative AI Engineer (RAG) | ML Engineer - Suryatej Lalam - NextMantra AI | `careers@nextmantra.ai` (placeholder — unverified, replace before sending) | new draft created this run |
| PlexTrac | AI Research Engineer - Applied AI | ML Engineer - Suryatej Lalam - PlexTrac | `careers@plextrac.com` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` Gmail label still could not be
created this run — `create_label` fails with "MCP server Gmail requires
re-authorization (token expired)", the same unresolved issue flagged in every
prior run. Find outreach drafts by subject prefix `ML Engineer - Suryatej
Lalam -` in Gmail Drafts until the Gmail connector is re-authorized (via
claude.ai connector settings), then label them manually or re-run.

## 2026-07-16

**Search window:** last 48 hours (2026-07-14 02:37 → 2026-07-15 21:14 UTC)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** —
same as every prior run; this inbox does not appear to receive Naukri alerts.
All jobs below come from LinkedIn job-alert digests, "jobs that match your
profile" recommendations, and "similar jobs" emails.

Raw emails scanned: 15 threads matching the search; 11 were job-alert/job-card
content (some with 2+ job cards each), 4 were excluded as non-job-alert content
(a LinkedIn creator-tips newsletter, a "reacted to your post" notification, a
"weekly performance" notification, and one duplicate ML Ops Engineer alert
resend). Yielded 63 unique job postings (deduped by Company + Role, collapsing
several jobs that appeared in 3+ separate digest emails) after filtering.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Applied Data Scientist | dunnhumby | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437748079) |
| 2 | Agentic AI Developer | BuyBuildSell InfraTech | New Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435799678) |
| 3 | Lead, Data Scientist | Tech Economy | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439416750) |
| 4 | ML Ops Engineer | Sirion | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440051417) |
| 5 | Senior AI Engineer – EEG Cognitive Scoring Systems | Basil Health AI | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437274769) |
| 6 | Generative AI Engineer (RAG) | NextMantra AI | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437243970) |
| 7 | Machine Learning Specialist | Awign | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437259503) |
| 8 | Jr ML Engineer | Baseforge Technologies | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439144232) |
| 9 | AI Engineer II (Remote) | Sezzle | India (Remote) | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4378063866) |
| 10 | AI Software Engineer — Remote | Pluvus | India (Remote) | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437942804) |
| 11 | Associate Data Scientist - Enterprise & Reporting | Circle K | Gurgaon | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436529087) |
| 12 | Associate Data Scientist | Fluor Corporation | Gurgaon | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440048197) |
| 13 | Associate - Data Scientist | United Airlines India Knowledge Center | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437425413) |
| 14 | Data Scientist | Gartner | Gurgaon | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437053720) |
| 15 | Quantitative Data Scientist (Python), MASS, Associate | BlackRock | Gurgaon | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4422999517) |
| 16 | Junior Data Scientist | Bandhan Technologies | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439171103) |
| 17 | Senior Associate -Applied AI ML -Digital | hackajob | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439832559) |
| 18 | Software Engineer, AI/ML | Google | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4390913792) |
| 19 | AI Engineer - 1 | GTMfund | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439784227) |
| 20 | AI Research Engineer - Applied AI | PlexTrac | Greater Bengaluru Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4417039358) |

No consulting/staffing postings landed in the top 20 this run. Consulting/IT-services/
staffing/BPO postings present in the wider 63-job pool but ranked outside the top 20
(skip fast unless desperate): Bain & Company (x2 roles, Gurugram), Axtria - Ingenious
Insights, DXC Technology, GlobalLogic, VLink Inc, Tata Consultancy Services, CG-VAK
Software & Exports Ltd., CGI, Blend Consulting & Training India Pvt. Ltd., PwC India,
Accenture in India, Luxoft, r3 Consultant, IQVIA, Automatic Infotech, Morae, and
ValueMomentum.

### Top 5 companies → cold outreach drafts

Top 5 by score: **dunnhumby, Sirion, Tech Economy, NextMantra AI, Basil Health AI.**
(Six companies tied at the top score of 15 — dunnhumby, BuyBuildSell InfraTech, Tech
Economy, Sirion, Basil Health AI, and NextMantra AI — the exact-title matches to
"Data Scientist"/"MLOps Engineer" plus the clearer company profiles were prioritized
over BuyBuildSell InfraTech to fill the 5 slots.) All five are newly created drafts
this run (no prior drafts existed for these exact company + role pairs).

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| dunnhumby | Applied Data Scientist | ML Engineer - Suryatej Lalam - dunnhumby | `careers@dunnhumby.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Sirion | ML Ops Engineer | ML Engineer - Suryatej Lalam - Sirion | `careers@sirion.ai` (placeholder — unverified, replace before sending) | new draft created this run |
| Tech Economy | Lead, Data Scientist | ML Engineer - Suryatej Lalam - Tech Economy | `careers@techeconomy.co` (placeholder — unverified, replace before sending) | new draft created this run |
| NextMantra AI | Generative AI Engineer (RAG) | ML Engineer - Suryatej Lalam - NextMantra AI | `careers@nextmantra.ai` (placeholder — unverified, replace before sending) | new draft created this run |
| Basil Health AI | Senior AI Engineer – EEG Cognitive Scoring Systems | ML Engineer - Suryatej Lalam - Basil Health AI | `careers@basilhealth.ai` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` Gmail label still could not be
created this run — `create_label` fails with "MCP server Gmail requires
re-authorization (token expired)", the same unresolved issue flagged in every
prior run. Drafts themselves were created successfully (that operation does
not hit the same auth wall). Find outreach drafts by subject prefix `ML
Engineer - Suryatej Lalam -` in Gmail Drafts until the Gmail connector is
re-authorized (via claude.ai connector settings), then label them manually or
re-run.

## 2026-07-17

**Search window:** last 48 hours (2026-07-15 04:37 → 2026-07-16 12:37 UTC)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** —
same as every prior run; this inbox does not appear to receive Naukri alerts.
All jobs below come from LinkedIn job-alert digests, "jobs picked for you"
recommendations, and "similar jobs" emails.

Raw emails scanned: 13 threads matching the search; 11 were job-alert/job-card
content (two of which contained a duplicate resend of the same alert), 2 were
excluded as non-job-alert content (a LinkedIn creator-tips newsletter and a
"reacted to your post" notification). Yielded 55 unique job postings (deduped
by Company + Role, collapsing jobs that appeared in 2-3 separate digest
emails) after filtering, from 72 raw postings extracted.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | ML Ops Engineer | Sirion | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440051417) |
| 2 | Applied Data Scientist | dunnhumby | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437748079) |
| 3 | Quantitative Data Scientist (Python), MASS, Associate | BlackRock | Gurgaon | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4422999517) |
| 4 | Associate Data Scientist - Enterprise & Reporting | Circle K | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436529087) |
| 5 | AI Engineer | Honasa Consumer Ltd. | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438047826) |
| 6 | Data Scientist | Policybazaar.com | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438059953) |
| 7 | Analyst - Data Scientist Machine Learning | United Airlines India Knowledge Center | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440968123) |
| 8 | Associate - Data Scientist | United Airlines India Knowledge Center | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437425413) |
| 9 | Lead, Data Scientist | Tech Economy | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439416750) |
| 10 | Data Scientist 1 | FedEx | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4421621787) |
| 11 | Applied AI ML Associate Senior | JPMorganChase | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440319524) |
| 12 | AI/ML Engineer | Trufe | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440964174) |
| 13 | AI/ML Engineer - Tech Lead | State Street | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435352155) |
| 14 | Machine Learning Engineer | Fox Corporation | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4371494140) |
| 15 | Senior Associate -Applied AI ML -Digital | hackajob | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439832559) |
| 16 | AI Engineer | Kuku | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440217089) |
| 17 | AI/ML Engineer | Noora Health | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433827168) |
| 18 | Associate AI/ML Engineer | Optum India | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440889832) |
| 19 | Junior AI Engineer | PranaTree | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440949620) |
| 20 | Data Scientist | Societe Generale Global Solution Centre | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4381462915) |

No consulting/staffing postings landed in the top 20 this run. Consulting/IT-services/
staffing/BPO postings present in the wider 55-job pool but ranked outside the top 20
(skip fast unless desperate): Recro (x2 roles), Accenture in India (x2 roles), Bain &
Company, CodeVyasa, Fluor Corporation, Gartner, r3 Consultant, DXC Technology,
GlobalLogic, Indium, Tata Consultancy Services, VLink Inc, ValueMomentum, Axtria -
Ingenious Insights, Bandhan Technologies, CG-VAK Software & Exports Ltd., CGI,
Crescendo Global, Morae, Birlasoft, and IBM.

### Top 5 companies → cold outreach drafts

Top 5 by score: **Sirion, dunnhumby, BlackRock, Circle K, Honasa Consumer Ltd.**
(Nine postings tied at the top score of 15, spanning 8 unique companies — Sirion,
dunnhumby, BlackRock, Circle K, Honasa Consumer Ltd., Policybazaar.com, United
Airlines India Knowledge Center, and Tech Economy. Tie broken by exact-title
precision to the target role — Sirion's "ML Ops Engineer" and dunnhumby's "Applied
Data Scientist" contain literal role-fit keywords so they were ranked first; Tech
Economy's "Lead, Data Scientist" was penalized for a seniority mismatch against a
2-YOE profile; remaining ties broken alphabetically, filling out BlackRock, Circle K,
and Honasa Consumer Ltd.) All five are newly created drafts this run (no prior
drafts existed for these exact company + role pairs).

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| Sirion | ML Ops Engineer | ML Engineer - Suryatej Lalam - Sirion | `careers@sirion.ai` (placeholder — unverified, replace before sending) | new draft created this run |
| dunnhumby | Applied Data Scientist | ML Engineer - Suryatej Lalam - dunnhumby | `careers@dunnhumby.com` (placeholder — unverified, replace before sending) | new draft created this run |
| BlackRock | Quantitative Data Scientist (MASS), Associate | ML Engineer - Suryatej Lalam - BlackRock | `careers@blackrock.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Circle K | Associate Data Scientist - Enterprise & Reporting | ML Engineer - Suryatej Lalam - Circle K | `careers@circlek.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Honasa Consumer Ltd. | AI Engineer | ML Engineer - Suryatej Lalam - Honasa Consumer Ltd. | `careers@honasa.in` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` Gmail label still could not be
created this run — `create_label` fails with "MCP server Gmail requires
re-authorization (token expired)" / a 403 on upscoping, the same unresolved
issue flagged in every prior run. Drafts themselves were created successfully
(that operation does not hit the same auth wall). Find outreach drafts by
subject prefix `ML Engineer - Suryatej Lalam -` in Gmail Drafts until the
Gmail connector is re-authorized (via claude.ai connector settings), then
label them manually or re-run.

**Stray draft to delete manually:** while verifying `create_draft` still
worked after the label-creation failure, a throwaway test draft was created
with subject `ML Engineer - Suryatej Lalam - Sirion` and body `Test` (draft id
`r-7907743281550763921`). No delete-draft tool is available in this session —
please delete that one draft by hand; the real Sirion draft (with full body
text, listed above) is a separate, later-created draft and is correct.

## 2026-07-18

**Search window:** last 48 hours (2026-07-16 12:37 IST → 2026-07-18 IST)
**Sources searched:** LinkedIn job alert digest emails (`jobalerts-noreply@linkedin.com`)
and LinkedIn recommendation emails (`jobs-noreply@linkedin.com`, "New jobs similar to...")
and Naukri (`naukri.com`, subject "job alert" / "recommended jobs"). **No Naukri
job-alert emails were found in this window at all** — the connected inbox does not
appear to receive Naukri alerts currently, consistent with every prior run. All jobs
below come from LinkedIn. LinkedIn "your application was sent to X" / "application
viewed" transactional notifications were excluded — only alert-digest and
recommendation emails were parsed.

Raw emails scanned: 9 LinkedIn job-alert digest threads (`jobalerts-noreply@linkedin.com`)
plus 2 "New jobs similar to..." / "picked for you" recommendation emails
(`jobs-noreply@linkedin.com`), yielding 79 job postings extracted from HTML card
markup, reduced to 50 unique postings after deduping by Company + Role. Many postings
(Kuku, Recro, Kotak Mahindra Bank, Optum India, Trufe, Qualcomm) recurred across
multiple alert emails in the window and were merged into single entries.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Data Scientist | Policybazaar.com | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438059953) |
| 2 | AI/ML Engineer | Trufe | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440964174) |
| 3 | Machine Learning Engineer II (Data & Audience Platform Team) | Warner Bros. Discovery | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4429039909) |
| 4 | MLOps Engineer | Spydra | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4424749059) |
| 5 | AI Engineer | Honasa Consumer Ltd. | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438047826) |
| 6 | AI/ML Engineer | Noora Health | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433827168) |
| 7 | Analyst - Data Scientist Machine Learning | United Airlines India Knowledge Center | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440968123) |
| 8 | Applied Scientist I, Ads Trust | Amazon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441284756) |
| 9 | Backend + AI Engineer | Feather | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440600968) |
| 10 | Data Scientist | Kotak Mahindra Bank | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438470989) |
| 11 | Data Scientist 1, Knowledge Management | eBay | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438418977) |
| 12 | Machine Learning Engineer | Augury | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4422472372) |
| 13 | Senior Software Engineer (AI Applications) | AlphaSense | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4393960645) |
| 14 | AI / ML Engineer ⚠️ consulting | Accenture in India | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440862592) |
| 15 | AI/ML Engineer ⚠️ consulting | Recro | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440227020) |
| 16 | Associate Data Engineer/Scientist | Barri Financial Group | Bangalore (Remote) | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437692813) |
| 17 | Associate Machine Learning Engineer | Amgen | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4421621787) |
| 18 | Data Scientist 1 | FedEx | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434833080) |
| 19 | Data Scientist, Digital Products | US Pharmacopeia | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4413455175) |
| 20 | Engineer/Associate Engineer - AI Platform | Qualcomm | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4406878077) |

⚠️ **Consulting/body-shop roles flagged in top 20 (skip fast unless desperate):**
Accenture in India (#14), Recro (#15). Also present in the wider 50-job pool but
ranked outside the top 20 — skip these too: Recro (MLOps Engineer, 2nd listing),
CodeVyasa, ARNsofttech, Indium, UST, EXL, NexGen Tech Solutions, Impetus /
Impetus Technologies (GCP GenAI Engineer, x2 listings), Crescendo Global,
Soothsayer Analytics, algoleap.

### Top 5 companies → cold outreach drafts

Top 5 by score: **Policybazaar.com, Trufe, Warner Bros. Discovery, Spydra, Noora
Health.** Ranked #1-4 are unambiguous distinct companies. #5 by score was Honasa
Consumer Ltd. (AI Engineer, jobid 4438047826) — but that is the *same* posting
already drafted yesterday (2026-07-17, draft `r-1553509631058808424` to
`careers@honasa.in`), so it was skipped to avoid a duplicate outreach email and
Noora Health (#6, AI/ML Engineer) was drafted instead to keep the slate at 5
distinct, not-yet-contacted companies.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| Policybazaar.com | Data Scientist | ML Engineer - Suryatej Lalam - Policybazaar.com | `careers@policybazaar.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Trufe | AI/ML Engineer | ML Engineer - Suryatej Lalam - Trufe | `careers@trufe.ai` (placeholder — domain unverified, replace before sending) | new draft created this run |
| Warner Bros. Discovery | Machine Learning Engineer II | ML Engineer - Suryatej Lalam - Warner Bros. Discovery | `careers@wbd.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Spydra | MLOps Engineer | ML Engineer - Suryatej Lalam - Spydra | `careers@spydra.app` (placeholder — domain unverified, replace before sending) | new draft created this run |
| Noora Health | AI/ML Engineer | ML Engineer - Suryatej Lalam - Noora Health | `careers@noorahealth.org` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` Gmail label still could not be created
this run — `create_label` failed with "MCP server Gmail requires re-authorization
(token expired)", the same unresolved issue flagged in every prior run. Immediately
after, the session's Gmail connection was flagged as needing re-authorization
entirely. Draft creation itself completed successfully before that (all 5 drafts
above were created), consistent with the pattern in prior runs where drafting
works but label management does not. Find today's outreach drafts by subject
prefix `ML Engineer - Suryatej Lalam -` in Gmail Drafts until the Gmail connector
is re-authorized (via claude.ai connector settings), then label them manually or
re-run. **Action needed from user:** please re-authorize the Gmail connector — this
has now blocked label creation for 4+ consecutive daily runs.

## 2026-07-19

**Search window:** last 48 hours (2026-07-17 04:36 IST → 2026-07-18 17:30 IST)
**Sources searched:** LinkedIn job-alert digest emails (`jobalerts-noreply@linkedin.com`),
LinkedIn recommendation/saved-job-reminder emails (`jobs-noreply@linkedin.com`, "apply now
to...", "New jobs similar to..."), and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** — consistent
with every prior run, this inbox does not appear to receive Naukri alerts currently. All
jobs below come from LinkedIn. Transactional "your application was sent to X" / "your
application was viewed by X" / "reacted to this post" notifications were excluded — only
alert-digest, saved-job-reminder, and "similar jobs" recommendation emails were parsed.

Raw emails scanned: 6 LinkedIn job-alert digest threads (`jobalerts-noreply@linkedin.com`),
1 saved-job reminder (`jobs-noreply@linkedin.com`, JPMorganChase), and 1 "New jobs similar
to..." recommendation email (`jobs-noreply@linkedin.com`, Baseforge), yielding 75 job
postings extracted from the plaintext job-card markup, reduced to 55 unique postings after
deduping by Company + Role.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Machine Learning Ops Engineer | Inovalon | Gurugram, Haryana | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4362256862) |
| 2 | Quantitative Data Scientist (Python), MASS, Associate | BlackRock | Gurgaon, Haryana | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4422999517) |
| 3 | Data Scientist I | Mastercard | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438742058) |
| 4 | Analyst - Data Scientist Machine Learning | United Airlines India Knowledge Center | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440968123) |
| 5 | Senior Software Engineer (AI Applications) | AlphaSense | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4393960645) |
| 6 | Applied AI ML Associate Senior | JPMorganChase | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440319524) |
| 7 | Applied AI \| Anomaly Detection Engineer | Quantumcona | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441108269) |
| 8 | MLOps Engineer | Spydra | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434069285) |
| 9 | AI/ML Engineer | Trufe | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440964174) |
| 10 | Machine Learning Engineer II (Data & Audience Platform Team) | Warner Bros. Discovery | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4429039909) |
| 11 | AI / ML Engineer | GoodScore | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441481293) |
| 12 | AI Engineer | CME Group | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441461282) |
| 13 | AI / LLM Engineer | Kaleidofin Private Limited | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441468902) |
| 14 | Data Scientist | Nielsen | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438788959) |
| 15 | Machine Learning Scientist I - Customer Technology | Wayfair | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441607608) |
| 16 | Data Scientist | Metropolis Technologies | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441473061) |
| 17 | AI Engineer | Kuku | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440217089) |
| 18 | Data Scientist | Kotak Mahindra Bank | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438470989) |
| 19 | Data Scientist 1, Knowledge Management | eBay | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438418977) |
| 20 | Applied Scientist I, Ads Trust | Amazon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441284756) |

**No consulting/body-shop roles landed in today's top 20** — all 20 are direct product,
fintech, bank, or startup employers. Flagged consulting/staffing/outsourcing companies
present in the wider 55-job pool but ranked outside the top 20 (skip these fast): UST
(ML Engineer I), ARNsofttech (AI/ML Engineer), Innova ESI (AI Engineer), EXL (AI/ML
Engineer), NexGen Tech Solutions (AIML Engineer), CG-VAK Software & Exports Ltd.
(AI Engineer-Agentic AI/Voice Bot/LLM), Recro (MLOps Engineer), Soothsayer Analytics
(Junior AI Engineer), Trinity Life Sciences (Associate Data Scientist), Tredence Inc.
(GCP Cloud-Data Engineer), hackajob (Data Engineer), Syngene International Limited
(Associate Scientist — biology/wet-lab role, not ML despite the "Scientist" title).

### Top 5 companies → cold outreach drafts

Top 5 by score are Inovalon (#1), BlackRock (#2), United Airlines India Knowledge Center
(#4), AlphaSense (#5), and JPMorganChase (#6) — but a full re-check of existing Gmail
drafts before writing new ones found **every one of those five already has at least one
prior outreach draft** (Inovalon x2, BlackRock, United Airlines x6, AlphaSense,
JPMorganChase x7, going back to late May). Spydra (#8), Trufe (#9), Warner Bros.
Discovery (#10), Nielsen (#14), and eBay (#19) are also already drafted from prior runs.
To keep the daily slate at 5 distinct, not-yet-contacted companies, outreach was drafted
for the next 5 ranked companies with no existing draft instead: **Mastercard (#3),
Quantumcona (#7), GoodScore (#11), CME Group (#12), Kaleidofin (#13)**.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| Mastercard | Data Scientist I | ML Engineer - Suryatej Lalam - Mastercard | `careers@mastercard.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Quantumcona | Applied AI \| Anomaly Detection Engineer | ML Engineer - Suryatej Lalam - Quantumcona | `careers@quantumcona.com` (placeholder — domain unverified, replace before sending) | new draft created this run |
| GoodScore | AI / ML Engineer | ML Engineer - Suryatej Lalam - GoodScore | `careers@goodscore.in` (placeholder — domain unverified, replace before sending) | new draft created this run |
| CME Group | AI Engineer | ML Engineer - Suryatej Lalam - CME Group | `careers@cmegroup.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Kaleidofin | AI / LLM Engineer | ML Engineer - Suryatej Lalam - Kaleidofin | `careers@kaleidofin.com` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` Gmail label still could not be created this run —
`create_label` failed with "MCP server Gmail requires re-authorization (token expired)",
the same unresolved issue flagged in every prior run. All 5 drafts above were created
successfully before that error surfaced; only the labeling step is blocked. Find today's
outreach drafts by subject prefix `ML Engineer - Suryatej Lalam -` in Gmail Drafts until
the Gmail connector is re-authorized, then label them manually or re-run. **Action needed
from user:** please re-authorize the Gmail connector via claude.ai connector settings —
this has now blocked label creation for 5+ consecutive daily runs.

## 2026-07-20

**Search window:** last 48 hours (2026-07-18 04:36 IST → 2026-07-19 18:06 IST)
**Sources searched:** LinkedIn job-alert digest emails (`jobalerts-noreply@linkedin.com`),
LinkedIn "New jobs similar to..." recommendation and saved-job "apply now" reminder emails
(`jobs-noreply@linkedin.com`), and Naukri (`naukri.com`, subject "job alert" / "recommended
jobs"). **No Naukri job-alert emails were found in this window** — consistent with every
prior run, this inbox does not appear to receive Naukri alerts currently. All jobs below
come from LinkedIn.

Raw emails scanned: 5 LinkedIn job-alert digest threads, 1 "New jobs similar to SDE-II at
Amazon" recommendation email, and 1 "apply now to your saved jobs" reminder email (JPMorganChase
saved-job digest), yielding 74 job postings extracted from the plaintext job-card markup,
reduced to 60 unique postings after deduping by Company + Role.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Machine Learning Ops Engineer | Inovalon | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4362256862) |
| 2 | Quantitative Data Scientist (Python), MASS, Associate | BlackRock | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4422999517) |
| 3 | Data Scientist I | Mastercard | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438742058) |
| 4 | Applied AI ML Associate Senior | JPMorganChase | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440319524) |
| 5 | Machine Learning Software Engineer | Apple | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4414161569) |
| 6 | AI/ML Engineer - Tech Lead | State Street | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435352155) |
| 7 | Applied AI \| Anomaly Detection Engineer | Quantumcona | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441108269) |
| 8 | Associate AI/ML Engineer | Optum India | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442183263) |
| 9 | AI/Machine Learning Engineer | Siemens Energy | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441310950) |
| 10 | Applied Scientist, International Machine Learning | Amazon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433360751) |
| 11 | Machine Learning Scientist I - Customer Technology | Wayfair | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441607608) |
| 12 | Data Scientist | Societe Generale Global Solution Centre | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4422994015) |
| 13 | AI / ML Engineer | GoodScore | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441481293) |
| 14 | AI Engineer | CME Group | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441461282) |
| 15 | AI / LLM Engineer | Kaleidofin Private Limited | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441468902) |
| 16 | Data Scientist | Metropolis Technologies | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441473061) |
| 17 | Data Scientist 1 | FedEx | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4421621787) |
| 18 | AI/ML Engineer ⚠️ | CG-VAK Software & Exports Ltd. | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441719207) |
| 19 | Sr Associate — ML Ops/Data Ops, Emerging Tech, Advisory ⚠️ | PwC India | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4292873133) |
| 20 | Software Engineer (AI-native development) | Microsoft | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441989128) |

**⚠️ Consulting/body-shop flags — 2 landed inside today's top 20** (both scored high on
role fit + Gurugram location but took the company-type penalty): CG-VAK Software & Exports
Ltd. (#18, IT staffing/services vendor) and PwC India (#19, Big-4 advisory). Skip these fast
unless the role itself is compelling. Additional consulting/staffing/outsourcing companies
present in the wider 60-job pool but ranked outside the top 20 (skip these too): UST (ML
Engineer I), ToggleNow (Software Developer – AI/ML Engineer), Trinity Life Sciences
(Associate Data Scientist ×2 — life-sciences consulting, not product), True Tech
Professionals (Generative AI Engineer), CG-VAK (2nd posting — AI Engineer-Agentic
AI/Voice Bot/LLM), Bain & Company (Associate - ENR AI Engineer CoE), PwC India (2nd
posting — GenAI/Python Specialist), Accenture in India (S&C Global Network AI Analyst),
Crescendo Global (Manager-Fraud Analytics — recruiting firm), Innova ESI (AI Engineer-
Bangalore), McKinsey & Company (Knowledge Analyst - Risk Dynamics), Metyis (Data
Engineering Associate — analytics consulting), Tredence Inc. (GCP Cloud-Data Engineer).

### Top 5 companies → cold outreach drafts

Top 5 by score are Inovalon (#1), BlackRock (#2), Mastercard (#3), JPMorganChase (#4), and
Apple (#5) — but checking existing Gmail drafts first found Inovalon, BlackRock, Mastercard,
and JPMorganChase already have prior outreach drafts (going back to late May/June, several
JPMorganChase). State Street (#6), Quantumcona (#7), Optum India (#8), Amazon (#10),
Societe Generale (#12), GoodScore (#13), CME Group (#14), and Kaleidofin (#15) are also
already drafted from prior runs. To keep the daily slate at 5 distinct, not-yet-contacted
companies, outreach was drafted for the highest-ranked companies with no existing draft:
**Apple (#5), Siemens Energy (#9), Wayfair (#11), Metropolis Technologies (#16), and
Microsoft (#20)**.

**Correction made mid-run:** two drafts were initially created for DP World and Nielsen
before a closer check of Gmail drafts surfaced that Nielsen already had two prior outreach
drafts (2026-06-11 and 2026-06-21) that an earlier keyword search missed. Since DP World and
Nielsen both scored lower (11) than Metropolis Technologies (13) and Microsoft (12), those
two were swapped in as the correct 4th and 5th picks. The stray DP World and Nielsen drafts
from this run could **not** be deleted/trashed — the same Gmail re-authorization error
described below also blocks `apply_sensitive_thread_label` (trash). **Action needed from
user:** please manually delete the duplicate "ML Engineer - Suryatej Lalam - DP World" and
"ML Engineer - Suryatej Lalam - Nielsen" drafts created today (2026-07-20) from Gmail Drafts.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| Apple | Machine Learning Software Engineer | ML Engineer - Suryatej Lalam - Apple | `careers@apple.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Siemens Energy | AI/Machine Learning Engineer | ML Engineer - Suryatej Lalam - Siemens Energy | `careers@siemens-energy.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Wayfair | Machine Learning Scientist I - Customer Technology | ML Engineer - Suryatej Lalam - Wayfair | `careers@wayfair.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Metropolis Technologies | Data Scientist | ML Engineer - Suryatej Lalam - Metropolis Technologies | `careers@metropolis.io` (placeholder — domain unverified, replace before sending) | new draft created this run |
| Microsoft | Software Engineer (AI-native development) | ML Engineer - Suryatej Lalam - Microsoft | `careers@microsoft.com` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` Gmail label still could not be created this run —
`create_label` failed with "MCP server Gmail requires re-authorization (token expired)",
the same unresolved issue flagged in every prior run. All 5 (plus the 2 stray duplicate)
drafts above were created successfully before that error surfaced; only the labeling
(and thread-trash cleanup) step is blocked. Find today's outreach drafts by subject prefix
`ML Engineer - Suryatej Lalam -` in Gmail Drafts until the Gmail connector is
re-authorized, then label them manually or re-run. **Action needed from user:** please
re-authorize the Gmail connector via claude.ai connector settings — this has now blocked
label creation for 6+ consecutive daily runs.

## 2026-07-21

**Search window:** last 48 hours (2026-07-19 → 2026-07-21)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** — the
inbox has no Naukri messages at all in the last 48 hours, only LinkedIn.

Raw emails scanned: 9 distinct LinkedIn job-alert digest threads (several overlapping
across multiple saved alerts — "machine learning engineer", "applied scientist",
"mlops engineer" in Gurugram/Hyderabad/Bengaluru), yielding 48 unique job postings
(deduped by Company + Role) after filtering out non-job-alert LinkedIn emails
(application-sent confirmations, invitation notifications, "X recently posted"
engagement emails).

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Associate AI/ML Engineer | Optum India | Gurgaon | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442183263) |
| 2 | AI/Machine Learning Engineer | Siemens Energy | Gurgaon | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441310950) |
| 3 | ML Engineer - Vision | RocketFrog.ai | Noida | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441195759) |
| 4 | ML Engineer Associate | HexaKnox Innovation Labs | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439676398) |
| 5 | Junior AI Engineer | HexaKnox Innovation Labs | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439678182) |
| 6 | Specialist, AI Engineer | MSD | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441609013) |
| 7 | Associate Data Scientist | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442485487) |
| 8 | Machine Learning Software Engineer | Apple | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4414161569) |
| 9 | Data Scientist | Societe Generale Global Solution Centre | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4422994015) |
| 10 | Applied Research Scientist - AI Models & Agents | AMD | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4347336078) |
| 11 | Data Scientist | News Corp | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433883939) |
| 12 | Machine Learning Scientist | DP World | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4383739897) |
| 13 | Gen AI Data Engineer | Mobility Global | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439208879) |
| 14 | Applied Scientist, Alexa Connections | Amazon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4405894737) |
| 15 | Applied Scientist II, Alexa AI | Amazon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4384500650) |
| 16 | Applied Scientist, International Machine Learning | Amazon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433360751) |
| 17 | Data Scientist | Ecolab | Bengaluru East | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4424171731) |
| 18 | AI Associate | NewCold | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439244478) |
| 19 | AI Associate-ML | NewCold | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439247455) |
| 20 | Software Engineer (AI-native development) | Microsoft | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441989128) |

**No consulting/body-shop roles landed in today's top 20** — unusual compared to recent
days. Consulting/staffing/outsourcing companies present in the wider 48-job pool but
ranked outside the top 20 (skip these, flagged by company-type penalty): Accenture in
India (AI/ML Engineer, and S&C Global Network - AI - Auto & Industrial Analyst), PwC
India (GenAI/Python Specialist, and Senior Associate - ML Ops/Data Ops Advisory),
GlobalLogic (Generative AI Engineer, IRC279043), CG-VAK Software & Exports Ltd. (Al/ML
Engineer), Bain & Company (Associate - ENR AI Engineer CoE), McKinsey & Company
(Knowledge Analyst - Risk Dynamics), Metyis (Data Engineering Associate — analytics
consulting), ToggleNow (Software Developer – AI/ML Engineer), Trinity Life Sciences
(Associate Data Scientist, AI Engineering — life-sciences consulting, not product, per
the same classification used in the 2026-07-20 entry), and Ensemble Global (Engineer II,
AI — name pattern suggests an IT staffing vendor, unconfirmed). Also worth a skip:
Jobgenix (Associate Engineer) looks like a recruiting/job-board platform rather than a
direct employer.

### Top 5 companies → cold outreach drafts

Top 5 by score are Optum India (#1), Siemens Energy (#2), RocketFrog.ai (#3), HexaKnox
Innovation Labs (#4/#5), and MSD (#6) — but checking existing Gmail drafts first found
Optum India (drafted 2026-07-08 and 2026-06-13) and Siemens Energy (drafted yesterday,
2026-07-20) already have prior outreach. Apple (#8) and Societe Generale (#9) also
already have prior drafts (2026-07-20 and 2026-06-02 respectively). To keep the daily
slate at 5 distinct, not-yet-contacted companies, outreach was drafted for the
highest-ranked companies with no existing draft: **RocketFrog.ai (#3), HexaKnox
Innovation Labs (#4), MSD (#6), AMD (#10), and News Corp (#11)**.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| RocketFrog.ai | ML Engineer - Vision | ML Engineer - Suryatej Lalam - RocketFrog.ai | `careers@rocketfrog.ai` (placeholder — unverified, replace before sending) | new draft created this run |
| HexaKnox Innovation Labs | ML Engineer Associate | ML Engineer - Suryatej Lalam - HexaKnox Innovation Labs | `careers@hexaknox.com` (placeholder — unverified domain, replace before sending) | new draft created this run |
| MSD | Specialist, AI Engineer | ML Engineer - Suryatej Lalam - MSD | `careers@msd.com` (placeholder — unverified, replace before sending) | new draft created this run |
| AMD | Applied Research Scientist - AI Models & Agents | ML Engineer - Suryatej Lalam - AMD | `careers@amd.com` (placeholder — unverified, replace before sending) | new draft created this run |
| News Corp | Data Scientist | ML Engineer - Suryatej Lalam - News Corp | `careers@newscorp.com` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` Gmail label still could not be created this
run — `create_label` failed with "MCP server Gmail requires re-authorization (token
expired)", the same unresolved issue flagged in every prior run. All 5 drafts above were
created successfully before that error surfaced; only the labeling step is blocked.
Find today's outreach drafts by subject prefix `ML Engineer - Suryatej Lalam -` in Gmail
Drafts until the Gmail connector is re-authorized, then label them manually or re-run.
**Action needed from user:** please re-authorize the Gmail connector via claude.ai
connector settings — this has now blocked label creation for 7+ consecutive daily runs.

## 2026-07-22

**Search window:** last 48 hours (2026-07-20 → 2026-07-22)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** — the
inbox has no Naukri messages at all in the last 48 hours, only LinkedIn.

Raw emails scanned: 9 distinct LinkedIn job-alert/recommendation digest threads
(overlapping alerts for "machine learning engineer", "applied scientist", "ai engineer",
"mlops engineer" across Gurugram/Hyderabad/Bengaluru/Delhi, plus a "similar jobs" digest),
yielding 53 unique job postings (deduped by Company + Role) after filtering out
non-job-alert LinkedIn emails (application-sent confirmations, connection/invitation
notifications, "X recently posted" engagement emails, and a career-workshop promo). One
listing ("AI Engineer" at "TestCompany123Blr2023") was excluded as an obvious test/spam
posting, not a real job.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | ML Engineer - Vision | RocketFrog.ai | Noida | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441195759) |
| 2 | AI Automation Engineer | BillCut | New Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440108651) |
| 3 | AI Engineer - Agentic AI & Automation | LUXASIA | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442572669) |
| 4 | AI Engineer | dunnhumby | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442585721) |
| 5 | Data Scientist II | Mastercard | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4432371016) |
| 6 | Senior Analyst - Data Science (SQL, Python, GenAI) | American Express | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439196703) |
| 7 | Analyst-Data Science | American Express | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439988079) |
| 8 | Data Scientist | Publicis Media | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440943984) |
| 9 | AI Engineer | Ricans Solar Energy Limited | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441778821) |
| 10 | ML Engineer Associate | HexaKnox Innovation Labs | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439676398) |
| 11 | Junior AI Engineer | HexaKnox Innovation Labs | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439678182) |
| 12 | Specialist, AI Engineer | MSD | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441609013) |
| 13 | Associate Data Scientist | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442485487) |
| 14 | Senior Software Engineer/Applied AI Scientist | The Hartford India | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4421173248) |
| 15 | Sr Machine Learning Engineer | Amgen | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433330362) |
| 16 | AI ML Engineer | Deservely Technologies | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436075557) |
| 17 | Senior AI/ML Engineer | Nomiso | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439811946) |
| 18 | Applied Research Scientist - AI Models & Agents | AMD | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4347336078) |
| 19 | Applied Scientist, Alexa Connections | Amazon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4405894737) |
| 20 | Data Scientist | News Corp | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433883939) |

**Consulting/staffing/body-shop roles to skip** — present in the wider 53-job pool but
kept out of the top 20 by the company-type penalty: McKinsey & Company (Data Scientist -
Marketing & Sales), EXL (Data Science — BPO), Capgemini (Data Science), EY (two listings:
Consultant - Tech Consulting AI and Data, and RC FS-MS EY COMPLY AI Engineers-Senior),
Accenture in India (AI/ML Engineer), PwC India (Senior Associate GCP Data Engineer —
Advisory), Infosys (three listings: AI Engineers, Generative AI, GenAI/Agentic AI
Engineer, plus AWS Bedrock Developer), Birlasoft (GEN AI Developer), IQ-EQ (Engineer -
Digital & AI Solutions — fund administration/professional services), Hitachi Digital
Services (AI Engineer GDC — outsourcing/GDC), CodeVyasa (AI Specialist — dev shop),
Asian Hires (AI Consultant — staffing agency), NxtWave ("Hiring for a Client" — staffing,
not a direct employer), GlobalLogic (Generative AI Engineer). Also worth a skip: Ensemble
Global (Engineer II, AI — name pattern suggests IT staffing, unconfirmed) and Jobgenix
(Associate Engineer — looks like a recruiting/job-board platform, not a direct employer).

### Top 5 companies → cold outreach drafts

Top 5 by score are RocketFrog.ai (#1), BillCut (#2), LUXASIA (#3), dunnhumby (#4), and
Mastercard (#5) — but checking existing Gmail drafts first found RocketFrog.ai (drafted
2026-07-21), dunnhumby (drafted 2026-07-17 and 2026-07-16), Mastercard (drafted
2026-07-19), MSD (#12, drafted 2026-07-21), HexaKnox Innovation Labs (#10/#11, drafted
2026-07-21), AMD (#18, drafted 2026-07-21), and News Corp (#20, drafted 2026-07-21)
already have prior outreach. To keep the daily slate at 5 distinct, not-yet-contacted
companies, outreach was drafted for the highest-ranked companies with no existing draft:
**BillCut (#2), LUXASIA (#3), American Express (#6/#7), Publicis Media (#8), and Ricans
Solar Energy Limited (#9)**.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| BillCut | AI Automation Engineer | ML Engineer - Suryatej Lalam - BillCut | `careers@billcut.com` (placeholder — unverified, replace before sending) | new draft created this run |
| LUXASIA | AI Engineer - Agentic AI & Automation | ML Engineer - Suryatej Lalam - LUXASIA | `careers@luxasia.com` (placeholder — unverified, replace before sending) | new draft created this run |
| American Express | Senior Analyst - Data Science (SQL, Python, GenAI) | ML Engineer - Suryatej Lalam - American Express | `careers@americanexpress.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Publicis Media | Data Scientist | ML Engineer - Suryatej Lalam - Publicis Media | `careers@publicismedia.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Ricans Solar Energy Limited | AI Engineer | ML Engineer - Suryatej Lalam - Ricans Solar Energy Limited | `careers@ricanssolar.com` (placeholder — unverified domain, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` Gmail label still could not be created this
run — `create_label` failed with "MCP server Gmail requires re-authorization (token
expired)", the same unresolved issue flagged in every prior run (now 8+ consecutive daily
runs). All 5 drafts above were created successfully before that error surfaced; only the
labeling step is blocked. Find today's outreach drafts by subject prefix `ML Engineer -
Suryatej Lalam -` in Gmail Drafts until the Gmail connector is re-authorized, then label
them manually or re-run.
**Action needed from user:** please re-authorize the Gmail connector via claude.ai
connector settings — this has now blocked label creation for 8+ consecutive daily runs.

## 2026-07-23

**Search window:** last 48 hours (2026-07-21 → 2026-07-23)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** — the
inbox still has no Naukri messages in the last 48 hours, only LinkedIn.

Raw emails scanned: 11 distinct LinkedIn job-alert/recommendation digest threads
(alerts for "machine learning engineer" in Hyderabad, "mlops engineer" in Bengaluru, plus
several "jobs picked/similar to your profile" digests covering Gurugram/Hyderabad/
Bengaluru/Delhi), yielding 69 unique job postings (deduped by Company + Role) after
filtering out non-job-alert LinkedIn emails (reaction/invitation notifications and a
career-workshop promo). One listing ("AI Engineer" at "TestCompany123Blr2023") was
excluded again as an obvious test/spam posting, not a real job.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Data Scientist II | Mastercard | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4432371016) |
| 2 | Jr ML Engineer | Baseforge Technologies | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439144232) |
| 3 | AI ML Engineer | Deservely Technologies | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436075557) |
| 4 | Associate AI or ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443010380) |
| 5 | Senior AI/ML Engineer (Automation) - Senior Associate | State Street | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443099713) |
| 6 | Machine Learning Engineer | Fast Code AI | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442299303) |
| 7 | AI/ML Engineer | Trufe | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440964174) |
| 8 | Associate AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439044122) |
| 9 | Data Scientist | LSEG | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4324640971) |
| 10 | Data Scientist - AI & Automation | eBay | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440166150) |
| 11 | Applied Scientist I | Amazon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443044320) |
| 12 | Junior Algorithm Engineer | DUSQ | Dwarka | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442056703) |
| 13 | Analyst-Data Science | American Express | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439988079) |
| 14 | Senior Analyst - Data Science (SQL, Python, GenAI) | American Express | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439196703) |
| 15 | AI Engineer | dunnhumby | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442585721) |
| 16 | Sr Machine Learning Engineer | Amgen | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433330362) |
| 17 | Data Scientist I | Alegeus | Bengaluru East | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4414657280) |
| 18 | AI Automation Engineer | BillCut | New Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440108651) |
| 19 | Senior Software Engineer/Applied AI Scientist | The Hartford India | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4421173248) |
| 20 | AI Engineer | Honasa Consumer Ltd. | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440146213) |

**Consulting/staffing/body-shop roles to skip** — present in the wider 69-job pool but
kept out of the top 20 by the company-type penalty: McKinsey & Company (Data Scientist -
Marketing & Sales), EXL (Data Science — BPO), Capgemini (Data Science), EY (three
listings: Consultant - Tech Consulting AI and Data, RC FS-MS EY COMPLY AI Engineers-Senior,
and Oracle AI Developer - Staff), Infosys (four listings: AI Engineers, Generative AI,
GenAI/Agentic AI Engineer, and AWS Bedrock Developer), Deloitte (Gen AI-AI and Data
Science Engineer III), Birlasoft (GEN AI Developer), IQ-EQ (Engineer - Digital & AI
Solutions — fund administration/professional services), Hitachi Digital Services (AI
Engineer GDC — outsourcing/GDC), CodeVyasa (Artificial Intelligence Specialist — dev
shop), Nomiso (Senior AI/ML Engineer — IT services), Asian Hires (AI Consultant —
staffing agency), NxtWave ("Hiring for a Client" — staffing, not a direct employer),
Drenova Hiring Solutions (Casual AI Engineer — staffing), PwC Acceleration Center India
and PwC India (Data Engineer / GCP Data Engineer — Advisory), YMinds.AI (Data Engineer —
staffing-style listing), ThinkWise Consulting LLP (ML Engineer AI COE), Enterprise Minds
(AIML Engineer — IT services), Talentgigs (Agentic AI Engineer — staffing platform), AAA
Global (Quantitative Researcher — recruiting agency), and IQVIA (AIML Engineer — CRO/
professional services). Also worth a skip: Ensemble Global (Engineer II, AI — name
pattern suggests IT staffing, unconfirmed).

### Top 5 companies → cold outreach drafts

Top 5 by score are Mastercard (#1), Baseforge Technologies (#2), Deservely Technologies
(#3), Optum India (#4), and State Street (#5) — but checking existing Gmail drafts first
found Mastercard (drafted 2026-07-19), Baseforge Technologies (drafted 2026-07-15), Optum
India (drafted 2026-07-08 and 2026-06-13), State Street (drafted 2026-07-13 and
2026-07-14), Trufe (#7, drafted 2026-07-18), eBay (#10, drafted 2026-05-31), Amazon (#11,
drafted multiple times), American Express (#13/#14, drafted multiple times), dunnhumby
(#15, drafted multiple times), Amgen (#16, drafted multiple times), BillCut (#18, drafted
2026-06-28, 2026-06-29, 2026-07-22), and Honasa Consumer Ltd. (#20, drafted 2026-07-17)
already have prior outreach. To keep the daily slate at 5 distinct, not-yet-contacted
companies, outreach was drafted for the highest-ranked companies with no existing draft:
**Deservely Technologies (#3), Fast Code AI (#6), LSEG (#9), DUSQ (#12), and Alegeus
(#17)**.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| Deservely Technologies | AI ML Engineer | ML Engineer - Suryatej Lalam - Deservely Technologies | `careers@deservely.com` (placeholder — unverified domain, replace before sending) | new draft created this run |
| Fast Code AI | Machine Learning Engineer | ML Engineer - Suryatej Lalam - Fast Code AI | `careers@fastcode.ai` (placeholder — unverified domain, replace before sending) | new draft created this run |
| LSEG | Data Scientist | ML Engineer - Suryatej Lalam - LSEG | `careers@lseg.com` (placeholder — unverified, replace before sending) | new draft created this run |
| DUSQ | Junior Algorithm Engineer | ML Engineer - Suryatej Lalam - DUSQ | `careers@dusq.com` (placeholder — unverified domain, replace before sending) | new draft created this run |
| Alegeus | Data Scientist I | ML Engineer - Suryatej Lalam - Alegeus | `careers@alegeus.com` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` Gmail label was successfully created this run
(the "MCP server Gmail requires re-authorization" error flagged in every prior run since
2026-07-15 did not recur — the connector appears to be re-authorized now). All 5 drafts
above were created and labeled `job-outreach` successfully.

## 2026-07-24

**Search window:** last 48 hours (2026-07-22 → 2026-07-24)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** — the
inbox still has no Naukri messages in the last 48 hours, only LinkedIn.

Raw emails scanned: 23 matching threads in the search window, of which 10 were genuine
job-listing digests (single-job alerts for "Software Engineer at Microsoft", "Associate
AI/ML Engineer at Optum India" ×2, "AI Engineer at Beckman Coulter Diagnostics", "Casual
AI Engineer at Drenova Hiring Solutions", "Data Engineer at PwC Acceleration Center
India", plus "jobs picked/similar to your profile" digests covering Hyderabad/
Bengaluru/Gurugram/Delhi/Mumbai). The other 13 threads were excluded as non-job-alert
noise: "your application was sent to X" confirmations, post-reaction notifications,
connection-invitation alerts, and a "see who reached out" prompt. Parsing the 10 digests
yielded 68 unique job postings after deduping by Company + Role.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Machine Learning Engineer | Gabeo.ai | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4391708150) |
| 2 | Associate AI/ML Engineer | Optum India | Noida | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443117568) |
| 3 | Analyst-Data Science | American Express | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442673221) |
| 4 | Applied Scientist I, Amazon Shipping | Amazon Science | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441017436) |
| 5 | Machine Learning Engineer II (Data & Audience Platform Team), Hyderabad | Warner Bros. Discovery | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4429039909) |
| 6 | Sr Machine Learning Engineer | Amgen | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433330362) |
| 7 | AI/ML Engineer | Trufe | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440964174) |
| 8 | Jr ML Engineer | Baseforge Technologies | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439144232) |
| 9 | Associate Machine Learning Engineer-1 | The Goodyear Tire & Rubber Company | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4414701842) |
| 10 | Associate AI or ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443010380) |
| 11 | Senior AI/ML Engineer (Automation) - Senior Associate | State Street | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443099713) |
| 12 | Machine Learning Engineer | Incept Labs | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4393558080) |
| 13 | Machine Learning Engineer | MantriAI | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442630092) |
| 14 | Associate - Data Science / Applied AI ML | JPMorganChase | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443770736) |
| 15 | Associate AI-ML Engineer | Fortive | Bengaluru South | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443366363) |
| 16 | AI/ML Engineer | Hewlett Packard Enterprise | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443358220) |
| 17 | Data Scientist | Anko GCC | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443105307) |
| 18 | Senior Associate -Applied AI ML -Digital | JPMorganChase | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4394949495) |
| 19 | Machine Learning Engineer | Fast Code AI | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442299303) |
| 20 | AI Engineer | Honasa Consumer Ltd. | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440146213) |

**Consulting/staffing/body-shop roles to skip** — present in the wider 68-job pool but
kept out of the top 20 by the company-type penalty: Viraaj HR Solutions Private Limited
(AI ML Engineer, posted under three different locations — an HR/staffing agency posting
on a client's behalf, not a direct employer), Deloitte (two listings: Gen AI-AI and Data
Science Engineer III, Machine Learning-Lead AI and Data Science Engineer II), Nomiso
(Senior AI/ML Engineer — IT services), ThinkWise Consulting LLP (ML Engineer AI COE), EY
(Oracle AI - Oracle AI Developer - Staff), Enterprise Minds, Inc (AIML Engineer — IT
services), AAA Global (Quantitative Researcher — recruiting agency), Growify Digital (AI
Application Developer in Delhi — small digital marketing agency), Ensemble Global
(Engineer II, AI — staffing-agency name pattern), Talentgigs (Agentic AI Engineer —
staffing platform), Drenova Hiring Solutions (Casual AI Engineer — staffing), BIG
Language Solutions (Machine Learning Engineer — localization/outsourcing services),
Collabera (AI Engineer — IT staffing firm), KloudStax (Google AI/ML Engineering
(Delivery) — small IT/cloud consulting shop), Tech Economy (Specialist, Corporate
Relations – Data Insights — agency-style listing, also off-target role), Kaufman Rossin
(Ai Solutions Engineer — accounting/advisory firm), IBM (Data Engineer — enterprise
services & consulting), Capgemini (Data Engineer — IT consulting), PwC Acceleration
Center India (Data Engineer — Big-4 advisory center), YMinds.AI (keyword-stuffed Data
Engineer listing — staffing-style), and Torinit (Artificial Intelligence Engineer — small
IT services/dev shop).

### Top 5 companies → cold outreach drafts

Top 5 by score are Gabeo.ai (#1), Optum India (#2), American Express (#3), Amazon
Science (#4), and Warner Bros. Discovery (#5). Checked existing `job-outreach` Gmail
drafts first (5 on file, all created 2026-07-23 for Alegeus, DUSQ, LSEG, Fast Code AI,
and Deservely Technologies) — none of the current top 5 overlap, so all five were
drafted fresh this run. Fast Code AI re-appears at #19 in today's list but already has a
2026-07-23 draft, so it was left alone.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| Gabeo.ai | Machine Learning Engineer | ML Engineer - Suryatej Lalam - Gabeo.ai | `careers@gabeo.ai` (placeholder — unverified domain, replace before sending) | new draft created this run |
| Optum India | Associate AI/ML Engineer | ML Engineer - Suryatej Lalam - Optum India | `careers@optum.com` (placeholder — unverified, replace before sending) | new draft created this run |
| American Express | Analyst-Data Science | ML Engineer - Suryatej Lalam - American Express | `careers@americanexpress.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Amazon Science | Applied Scientist I, Amazon Shipping | ML Engineer - Suryatej Lalam - Amazon Science | `careers@amazon.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Warner Bros. Discovery | Machine Learning Engineer II | ML Engineer - Suryatej Lalam - Warner Bros. Discovery | `careers@wbd.com` (placeholder — unverified domain, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` label already existed from the 2026-07-23 run.
All 5 new drafts above were created and labeled `job-outreach` successfully (confirmed via
`list_drafts` — 10 drafts now carry the label: 5 from today, 5 from 2026-07-23).

## 2026-07-25

**Search window:** last 48 hours (2026-07-23 → 2026-07-25)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** — the
inbox still has no Naukri messages in the last 48 hours, only LinkedIn.

Raw emails scanned: 12 distinct LinkedIn job-alert/recommendation digest threads
("apply now to your saved jobs", job alerts for "applied scientist" / "machine learning
engineer" in Bengaluru, "jobs picked/similar to your profile" digests covering Gurugram/
Hyderabad/Bengaluru/Delhi), yielding 62 raw job postings. After deduping exact repeats
(same company + role posted more than once, e.g. Hewlett Packard Enterprise's "AI/ML
Engineer" and Fortive's "Associate AI-ML Engineer" each appearing twice across locations,
and Viraaj HR Solutions Private Limited's "AI ML Engineer" posted 3x across Gurugram/
Delhi/New Delhi), 59 unique jobs (deduped by Company + Role) went into ranking.
"Application confirmation" emails ("Your application was sent to X") were excluded as
noise, not job listings.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Machine Learning Scientist III- India | DISCO | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4425895357) |
| 2 | Data Scientist | Citi | Haryana, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443171368) |
| 3 | Applied Scientist I, Amazon Shipping | Amazon Science | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441017436) |
| 4 | Analyst-Data Science | American Express | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442673221) |
| 5 | Machine Learning Engineer | Gabeo.ai | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4391708150) |
| 6 | Machine Learning Engineer | S&P Global | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434607893) |
| 7 | Sr Machine Learning Engineer | Amgen | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433330362) |
| 8 | Applied Scientist I | Amazon Science | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4412834723) |
| 9 | Data Scientist | Kotak Mahindra Bank | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444292766) |
| 10 | Applied scientist 2 - Fine tuning | Microsoft | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443916118) |
| 11 | ML Engineer (Forward Deployed) | Applied Computing | Greater Bengaluru Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4432326059) |
| 12 | AI/Machine Learning Engineer | Siemens Energy | Gurgaon | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443163988) |
| 13 | Senior Associate -Applied AI ML -Digital | JPMorganChase | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4394949495) |
| 14 | Senior AI Engineer – EEG Cognitive Scoring Systems | Brainwave Science | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441037210) |
| 15 | Associate - Data Science / Applied AI ML | JPMorganChase | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443770736) |
| 16 | Associate AI/ML Engineer | Optum India | Noida | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443117568) |
| 17 | Machine Learning Engineer | Incept Labs | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4393558080) |
| 18 | Machine Learning Engineer | MantriAI | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442630092) |
| 19 | AI Engineer | OATI | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443928089) |
| 20 | Machine Learning Engineer II (Data & Audience Platform Team), Hyderabad | Warner Bros. Discovery | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4429039909) |

**Consulting/staffing/body-shop roles to skip** — present in the wider 59-job pool but
kept out of the top 20 by the company-type penalty: Viraaj HR Solutions Private Limited
(AI ML Engineer, posted 3x across Gurugram/Delhi/New Delhi — an HR/staffing agency
posting on a client's behalf, not a direct employer), Deloitte (three listings: Gen AI-AI
and Data Science Engineer III, Machine Learning-Lead AI and Data Science Engineer II, and
Data Lake - Consultant), Nomiso (Senior AI/ML Engineer — IT services), Anko GCC (Data
Scientist — Target's captive global capability center, a service-center setup rather than
a direct product org), Talentgigs (Agentic AI Engineer — staffing platform), Growify
Digital (AI Application Developer in Delhi — small digital marketing agency), PwC India
(IN_ Associate_ Data Science_ Advisory — Big-4 advisory), Capgemini (Data Engineer — IT
consulting), Promaynov Advisory Services Pvt. Ltd (Business Analyst — advisory/staffing
name pattern, also off-target role), Tech Economy (Specialist, Corporate Relations – Data
Insights — agency-style listing, also off-target role), Kaufman Rossin (Ai Solutions
Engineer — accounting/advisory firm), IBM (Data Engineer — enterprise services &
consulting), BIG Language Solutions (Machine Learning Engineer — localization/outsourcing
services), Collabera (AI Engineer — IT staffing firm), PwC Acceleration Center India
(Data Engineer- Associate- Analytics as Service - Operate — Big-4 advisory center),
KloudStax (Google AI/ML Engineering (Delivery) — small IT/cloud consulting shop), and
Torinit (Artificial Intelligence Engineer — small IT services/dev shop).

### Top 5 companies → cold outreach drafts

Top 5 by score are DISCO (#1), Citi (#2), Amazon Science (#3), American Express (#4), and
Gabeo.ai (#5). Checked existing `job-outreach` Gmail drafts first (10 on file: Warner
Bros. Discovery, Amazon Science, American Express, Optum India, and Gabeo.ai from
2026-07-24, plus Alegeus, DUSQ, LSEG, Fast Code AI, and Deservely Technologies from
2026-07-23) — Amazon Science (#3), American Express (#4), and Gabeo.ai (#5) already have
drafts, so those three were skipped. To keep the daily slate at 5 distinct, not-yet-
contacted companies, outreach was drafted for the highest-ranked companies with no
existing draft: **DISCO (#1), Citi (#2), S&P Global (#6), Amgen (#7), and Kotak Mahindra
Bank (#9)**.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| DISCO | Machine Learning Scientist III - India | ML Engineer - Suryatej Lalam - DISCO | `careers@csdisco.com` (placeholder — unverified domain, replace before sending) | new draft created this run |
| Citi | Data Scientist | ML Engineer - Suryatej Lalam - Citi | `careers@citi.com` (placeholder — unverified, replace before sending) | new draft created this run |
| S&P Global | Machine Learning Engineer | ML Engineer - Suryatej Lalam - S&P Global | `careers@spglobal.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Amgen | Sr Machine Learning Engineer | ML Engineer - Suryatej Lalam - Amgen | `careers@amgen.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Kotak Mahindra Bank | Data Scientist | ML Engineer - Suryatej Lalam - Kotak Mahindra Bank | `careers@kotak.com` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` label already existed from prior runs. All 5 new
drafts above were created and labeled `job-outreach` successfully (confirmed via
`list_labels` — the label's message count went from 10 to 15 after this run).

## 2026-07-26

**Search window:** last 48 hours (2026-07-24 → 2026-07-26)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** — the
inbox still has no Naukri messages in the last 48 hours, only LinkedIn.

Raw emails scanned: 6 distinct LinkedIn threads (10 messages total — several digests were
resent hours apart with the same subject), covering job alerts for "machine learning
engineer" in Hyderabad/Bengaluru/Gurugram, "mlops engineer" in Bengaluru, "applied
scientist" in India, plus a "saved jobs" apply-reminder digest, yielding 77 raw job
cards. After deduping exact repeats (same company + role appearing across resent digests
and cross-posted alerts, e.g. Amgen's "Associate – AI/ML Innovation Engineer" appearing
5x, Qualcomm's "Associate Engineer" 4x, and Hewlett Packard Enterprise's "AI/ML Engineer"
3x), 49 unique jobs (deduped by Company + Role) went into ranking. "Application
confirmation" emails ("Your application was sent to X") were excluded as noise, not job
listings.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | AI / ML Engineer | SecNinjaz Technologies LLP | Delhi, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444306851) |
| 2 | Data Scientist | BioBrain Insights | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443863955) |
| 3 | Data Scientist / AI Engineer / Analytics Engineer | Great Learning | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444074998) |
| 4 | Data Scientist | Aftershoot | Delhi, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444928215) |
| 5 | Data Scientist | Citi | Haryana, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443171368) |
| 6 | Machine Learning Engineer | S&P Global | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434607893) |
| 7 | AI/Machine Learning Engineer | Siemens Energy | Gurgaon | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443163988) |
| 8 | Machine Learning Engineer | Solventum | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4408285032) |
| 9 | AI / ML Data Scientist (Across levels) | Nielsen | Bengaluru East | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441586395) |
| 10 | Senior Applied Scientist | Microsoft | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444427743) |
| 11 | Applied Scientist I | Amazon Science | Bengaluru, Karnataka, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4412834723) |
| 12 | Data Scientist | Kotak Mahindra Bank | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444292766) |
| 13 | AI/ML Engineer | Hewlett Packard Enterprise | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443354325) |
| 14 | AI/ML Engineer | Optum India | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444401964) |
| 15 | Applied scientist 2 - Fine tuning | Microsoft | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443916118) |
| 16 | ML Engineer (Forward Deployed) | Applied Computing | Greater Bengaluru Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4432326059) |
| 17 | Machine Learning Scientist III- India | DISCO | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4425895357) |
| 18 | Senior Associate -Applied AI ML -Digital | JPMorganChase | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4394949495) |
| 19 | Senior AI Engineer – EEG Cognitive Scoring Systems | Brainwave Science | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441037210) |
| 20 | Data Scientist II | FedEx | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436131526) |

**Consulting/staffing/body-shop roles to skip** — present in the wider 49-job pool but
kept out of the top 20 by the company-type penalty: PwC India (two listings:
IN_Associate_AI Engineer_Financial Services_Advisory in Hyderabad, and IN_ Associate_
Data Science_ Advisory Corporate_Advisory in Bangalore — Big-4 advisory), PwC
Acceleration Center India (Data Engineer- Associate- Analytics as Service - Operate — Big-4
advisory center), Deloitte (Data Lake - Consultant), Capgemini (Data Engineer — IT
consulting), Cognizant (AI Customer Engineer — IT services), HCLTech (Machine Learning
Engineer — IT services), Dentsu Global Services (Data & AI Engineer — agency/outsourcing),
Conduent (Data Scientist I — BPO/outsourcing), ERM (Data Automation (Python) —
environmental/sustainability consulting), and Promaynov Advisory Services Pvt. Ltd
(Business Analyst — advisory/staffing name pattern, also off-target role).

### Top 5 companies → cold outreach drafts

Top 5 by score are SecNinjaz Technologies LLP (#1), BioBrain Insights (#2), Great Learning
(#3), Aftershoot (#4), and Citi (#5). Checked existing `job-outreach` Gmail drafts first
(15 on file, including Citi and S&P Global from 2026-07-25, plus Kotak Mahindra Bank,
Amgen, DISCO, Warner Bros. Discovery, Amazon Science, American Express, Optum India,
Gabeo.ai, Alegeus, DUSQ, LSEG, Fast Code AI, and Deservely Technologies from prior runs) —
Citi (#5) and S&P Global (#6) already have drafts, so those were skipped. To keep the
daily slate at 5 distinct, not-yet-contacted companies, outreach was drafted for the
highest-ranked companies with no existing draft: **SecNinjaz Technologies LLP (#1),
BioBrain Insights (#2), Great Learning (#3), Aftershoot (#4), and Siemens Energy (#7)**.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| SecNinjaz Technologies LLP | AI / ML Engineer | ML Engineer - Suryatej Lalam - SecNinjaz Technologies | `careers@secninjaz.com` (placeholder — unverified domain, replace before sending) | new draft created this run |
| BioBrain Insights | Data Scientist | ML Engineer - Suryatej Lalam - BioBrain Insights | `careers@biobraininsights.com` (placeholder — unverified domain, replace before sending) | new draft created this run |
| Great Learning | Data Scientist / AI Engineer / Analytics Engineer | ML Engineer - Suryatej Lalam - Great Learning | `careers@mygreatlearning.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Aftershoot | Data Scientist | ML Engineer - Suryatej Lalam - Aftershoot | `careers@aftershoot.co` (placeholder — unverified, replace before sending) | new draft created this run |
| Siemens Energy | AI/Machine Learning Engineer | ML Engineer - Suryatej Lalam - Siemens Energy | `careers@siemens-energy.com` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` label already existed from prior runs. All 5 new
drafts above were created and labeled `job-outreach` successfully (confirmed via
`list_labels` — the label's message count went from 15 to 20 after this run).

## 2026-07-27

**Search window:** last 48 hours (2026-07-25 → 2026-07-27)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`) and
Naukri (`naukri.com`, subject "job alert" / "recommended jobs"). **No Naukri job-alert
emails were found in this window** — the inbox still has no Naukri messages in the last
48 hours, only LinkedIn. LinkedIn "application confirmation" emails
(`jobs-noreply@linkedin.com`, "Your application to X") and connection/invitation
notifications (`notifications-noreply@linkedin.com`) were excluded as noise, not job
alerts.

Raw emails scanned: 9 LinkedIn job-alert digest messages across 6 threads (alerts for
"applied scientist" in Bengaluru, "data engineer" in Bengaluru, "mlops engineer" in
Bengaluru, and "machine learning engineer" in Hyderabad, some resent hours apart with
overlapping content), yielding 74 raw job cards. One card — a Russian-language toy/doll
listing that had clearly been spam-injected into one digest — was discarded as not a
real job posting. After deduping exact repeats (same company + role reappearing across
resent digests and cross-posted "other alerts" sections, e.g. Associate Engineer at
Qualcomm and Associate Data Scientist at TriNet each appearing 3x, Associate – AI/ML
Innovation Engineer at Amgen 2x), 49 unique jobs (deduped by Company + Role) went into
ranking. One listing had a typo in its own title ("Machine Learing Engineer" at
Leegality); treated as "Machine Learning Engineer" for role-fit scoring since the typo
is clearly the source posting's, not a different role.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | AI engineer | Tuning Research (WorkableAI) | New Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438931589) |
| 2 | Data Scientist / AI Engineer / Analytics Engineer | Great Learning | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444074998) |
| 3 | Data Scientist | Aftershoot | Bawana | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444928215) |
| 4 | Machine Learning Engineer | Leegality | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444335609) |
| 5 | Data Scientist I | MetLife | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444974240) |
| 6 | Machine Learning Engineer | S&P Global | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434607893) |
| 7 | AI/ML Data Scientist - Sales Forecasting | Philips | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435559782) |
| 8 | Associate Data Scientist | TriNet | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444947374) |
| 9 | MLOps Engineer | Vestas | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4427951750) |
| 10 | AI/ML Engineer | studyix | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441826285) |
| 11 | AI Engineer - Product and Growth | Vola Finance | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441587697) |
| 12 | Applied AI Engineer | KTR Freight Pvt Ltd | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444315856) |
| 13 | Data Scientist II | FedEx | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436131526) |
| 14 | Machine Learning Engineer | Solventum | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4408285032) |
| 15 | AI / ML Data Scientist (Across levels) | Nielsen | Bengaluru East | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441586395) |
| 16 | Machine Learning Scientist - II | Wayfair | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4429623173) |
| 17 | Machine Learning Scientist II (Search) | Wayfair | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435297949) |
| 18 | Senior Applied Scientist | Microsoft | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444427743) |
| 19 | Principal Applied AI Analyst - AI/ML | Data Scientist | First Citizens India | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4432821777) |
| 20 | AI/ML Specialist - Agentic AI & Generative AI | ZF Group | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441881999) |

**Consulting/staffing/body-shop roles to skip** — present in the wider 49-job pool but
kept out of the top 20 by the company-type penalty: SecNinjaz Technologies LLP (AI / ML
Engineer — cybersecurity consulting), BioBrain Insights (Data Scientist — boutique
analytics consultancy), UST (ML Engineer I — IT services/outsourcing), PwC India
(IN_Associate_AI Engineer_Financial Services_Advisory — Big-4 advisory), Talentgigs
(Agentic AI Engineer — staffing platform), FutureLeap Search (Applied AI Scientist —
recruiting/search firm), aikyam jobs (Associate Data Scientist posting on behalf of
Wadhwani Foundation — staffing-agency-style listing), Conduent (Data Scientist I —
BPO/outsourcing), Dentsu Global Services (Data & AI Engineer — agency/outsourcing),
HCLTech (Machine Learning Engineer — IT services), CG-VAK Software & Exports Ltd. (AI/ML
— IT services/outsourcing), Weekday (YC W21) (Graph Data Engineer — recruiting-as-a-
service platform, not a direct employer), ERM (Data Automation (Python) —
environmental/sustainability consulting), Cognizant (AI Customer Engineer — IT
services), and EY (DE-Python-AI-GDS — Big-4 advisory).

### Top 5 companies → cold outreach drafts

Top 5 by score are Tuning Research (WorkableAI) (#1), Great Learning (#2), Aftershoot
(#3), Leegality (#4), and MetLife (#5). Checked existing `job-outreach` Gmail drafts
first (20+ on file) — Great Learning and Aftershoot were already drafted on 2026-07-26,
S&P Global (#6) on 2026-07-25, and TriNet (#8) and Philips (#7) had older drafts from
2026-07-08/2026-07-14 and 2026-06-13 respectively. To keep the daily slate at 5 distinct,
not-yet-contacted companies, outreach was drafted for the highest-ranked companies with
no existing draft: **Tuning Research (WorkableAI) (#1), Leegality (#4), MetLife (#5),
Vestas (#9), and studyix (#10)**.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| Tuning Research (WorkableAI) | AI engineer | ML Engineer - Suryatej Lalam - Tuning Research (WorkableAI) | `careers@workable.ai` (placeholder — unverified domain, replace before sending) | new draft created this run |
| Leegality | Machine Learning Engineer | ML Engineer - Suryatej Lalam - Leegality | `careers@leegality.com` (placeholder — unverified, replace before sending) | new draft created this run |
| MetLife | Data Scientist I | ML Engineer - Suryatej Lalam - MetLife | `careers@metlife.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Vestas | MLOps Engineer | ML Engineer - Suryatej Lalam - Vestas | `careers@vestas.com` (placeholder — unverified, replace before sending) | new draft created this run |
| studyix | AI/ML Engineer | ML Engineer - Suryatej Lalam - studyix | `careers@studyix.com` (placeholder — unverified domain, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` label already existed from prior runs.
`label_message` failed with "Invalid id value" when called with the ID `create_draft`
returned (that ID is not a valid message ID for labeling); switching to `label_thread`
with each draft's `threadId` succeeded for all 5 new drafts.

## 2026-07-28

**Search window:** last 48 hours (2026-07-26 → 2026-07-28)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`) and
Naukri (`naukri.com`, subject "job alert" / "recommended jobs"). **No Naukri job-alert
emails were found in this window** — a direct `from:naukri.com newer_than:2d` search
returned zero results, confirming the inbox has no Naukri alerts in the last 48 hours,
only LinkedIn. LinkedIn "application confirmation" emails (`jobs-noreply@linkedin.com`,
"Your application to X"), connection/invitation notifications
(`notifications-noreply@linkedin.com`), and editorial newsletter emails
(`editors-noreply@linkedin.com`) were excluded as noise, not job alerts.

Raw emails scanned: 14 LinkedIn job-alert digest/reminder messages across 13 threads
(alerts for "ml platform engineer" in India, "ai engineer" in Hyderabad/Delhi, "machine
learning engineer" in Hyderabad/Bengaluru/Gurugram/Delhi, "applied scientist" in
Bengaluru/India, "data engineer" in Bengaluru, "mlops engineer" in Bengaluru, plus a
"jobs similar to" reminder and "New jobs from your other alerts" cross-posted sections),
yielding 79 raw job cards. One card — the same Russian-language toy/doll spam injected
into a "jobs in Disney" cross-post section as in prior runs — was discarded as not a real
job posting. After deduping exact repeats (same company + role reappearing across resent
digests and cross-posted "other alerts" sections, e.g. MLOps Engineer at Vestas and AI
Engineer - Agentic AI & Automation at LUXASIA each appearing twice, and the LPAI ML SW
Senior Engineer at Qualcomm digest resending within the same thread), 60 unique jobs
(deduped by Company + Role) went into ranking. One listing had a typo in its own title
("Machine Learing Engineer" at Leegality); treated as "Machine Learning Engineer" for
role-fit scoring since the typo is clearly the source posting's, not a different role.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | AI engineer | Tuning Research (WorkableAI) | New Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438931589) |
| 2 | Machine Learing Engineer | Leegality | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444335609) |
| 3 | AI/ML Engineer | Trufe | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440964174) |
| 4 | AI/ML Engineer | studyix | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441826285) |
| 5 | AI Engineer - Agentic AI & Automation | LUXASIA | Delhi, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445343204) |
| 6 | Machine Learning Engineer | Solventum | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445360131) |
| 7 | Associate Data Scientist - Enterprise & Reporting | Circle K | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4395998184) |
| 8 | Artificial Intelligence Researcher | HBSS India | Delhi, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444370587) |
| 9 | AI Engineer - Product and Growth | Vola Finance | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4441587697) |
| 10 | Applied AI Engineer | KTR FREIGHT PVT LTD | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444315856) |
| 11 | Machine Learning Engineer, Apple Intelligence | Apple | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4414158695) |
| 12 | Agentic AI Engineer | HP | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4440005713) |
| 13 | Applied AI/ML Engineer | Google | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439890102) |
| 14 | Generative AI Engineer | Hewlett Packard Enterprise | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433097235) |
| 15 | Applied Researcher | eBay | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4427826975) |
| 16 | Senior Applied Scientist | Microsoft | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444427743) |
| 17 | AI/ML Engineer | FICO | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442014391) |
| 18 | LPAI ML SW Senior Engineer | Qualcomm | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4397274735) |
| 19 | Data Scientist- Semantic Search-Hyd/Noida (2026) | Arrise Solutions (India) Pvt. Ltd. | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4399800152) |
| 20 | Associate – AI/ML Innovation Engineer | Amgen | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436740658) |

**Consulting/staffing/body-shop roles to skip** — present in the wider 60-job pool but
kept out of the top 20 by the company-type penalty: Deloitte (Machine Learning-AI and
Data Science Engineer III — Big-4 advisory), UST (ML Engineer I, and separately Lead I -
Software Engineering-Agentic AI, GCP — IT services/outsourcing), PwC Acceleration Center
India (Palantir AI Engineer- Senior Associate, Data Engineer-Palantir Foundry-Senior
Associate, and Operations Engineer - Palantir Foundry-Senior Associate — Big-4 advisory
delivery center), Trinity Life Sciences (Associate Data Scientist, AI Engineering — life
sciences consulting), Infosys (GEN AI Engineer, and separately Microsoft Fabric (Azure
Subscription) — IT services), aikyam jobs (Associate Data Scientist posting on behalf of
Wadhwani Foundation — staffing-agency-style listing), FutureLeap Search (Applied AI
Scientist - TTS — recruiting/search firm), EY (DE-Python-AI-GDS — Big-4 advisory),
hackajob (Quant Analytics Associate - Cards — recruiting platform, not a direct
employer), Weekday (YC W21) (Graph Data Engineer — recruiting-as-a-service platform, not
a direct employer), and CG-VAK Software & Exports Ltd. (AI/ML — IT services/outsourcing).

### Top 5 companies → cold outreach drafts

Top 5 by score are Tuning Research (WorkableAI) (#1), Leegality (#2), Trufe (#3), studyix
(#4), and LUXASIA (#5). Checked existing `job-outreach` Gmail drafts first (25+ on file)
— Tuning Research (WorkableAI), Leegality, and studyix were already drafted on
2026-07-27. To keep the daily slate at 5 distinct, not-yet-contacted companies, outreach
was drafted for the highest-ranked companies with no existing draft, walking down the
full ranked list: **Trufe (#3), LUXASIA (#5), Solventum (#6), Circle K (#7), and HBSS
India (#8)**. Confirmed via a targeted draft search (`label:job-outreach` + company name)
that none of these 5 had a prior draft before creating new ones.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| Trufe | AI/ML Engineer | ML Engineer - Suryatej Lalam - Trufe | `careers@trufe.com` (placeholder — unverified domain, replace before sending) | new draft created this run |
| LUXASIA | AI Engineer - Agentic AI & Automation | ML Engineer - Suryatej Lalam - LUXASIA | `careers@luxasia.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Solventum | Machine Learning Engineer | ML Engineer - Suryatej Lalam - Solventum | `careers@solventum.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Circle K | Associate Data Scientist - Enterprise & Reporting | ML Engineer - Suryatej Lalam - Circle K | `careers@circlek.com` (placeholder — unverified, replace before sending) | new draft created this run |
| HBSS India | Artificial Intelligence Researcher | ML Engineer - Suryatej Lalam - HBSS India | `careers@hbssindia.com` (placeholder — unverified domain, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` label already existed from prior runs and its ID
(`Label_3`) was confirmed via `list_labels`. `label_thread` with each new draft's
`threadId` (looked up via `list_drafts`) succeeded for all 5 new drafts.

## 2026-07-29

**Search window:** last 48 hours (2026-07-27 → 2026-07-29)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`) and
Naukri (`naukri.com`, subject "job alert" / "recommended jobs"). **No Naukri job-alert
emails were found in this window** — a direct `from:naukri.com newer_than:2d` search
returned zero results, confirming only LinkedIn alerts are present.

Raw emails scanned: 18 threads / 24 messages matched the search. Unlike the multi-job
digest format seen in some prior runs, every LinkedIn alert in this window was a
single-job email (subject = "Job Title at Company"). Two messages were excluded as
noise: an "editors-noreply@linkedin.com" newsletter ("network like a pro") and a
"jobs-noreply@linkedin.com" application-confirmation email ("Your application to AI/ML
Engineer at Chubb"), neither of which is a job alert. The remaining 22 job-alert emails
were resends of the same postings across separate threads/messages (PwC India ×3, Lyric
×3, Qualcomm ×2, Circle K ×2, Scoutit ×2, LUXASIA ×2). After deduping by Company + Role,
**14 unique jobs** went into ranking.

### Ranked jobs (all 14 — fewer than 20 unique postings arrived in this window)

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Associate AI/ML Engineer: Generative AI Specialist | NARBA | Noida | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4444822533/) |
| 2 | AI/ML Engineer | Scoutit | Delhi, India | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4444838361/) |
| 3 | AI Engineer - Agentic AI & Automation | LUXASIA | Delhi, India | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4445343204/) |
| 4 | LPAI ML SW Senior Engineer | Qualcomm | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4397274735/) |
| 5 | Associate Data Scientist - Enterprise & Reporting | Circle K | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4395998184/) |
| 6 | Software Engineer I, AI | Lyric | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4444880271/) |
| 7 | Machine Learning Engineer | Solventum | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4445360131/) |
| 8 | Machine Learning-AI and Data Science Engineer III | Deloitte | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4425098292/) |
| 9 | Data Analyst | Hudson Data | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4444853549/) |
| 10 | Associate Data Scientist, AI Engineering | Trinity Life Sciences | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4365330949/) |
| 11 | Data Engineer | ANZ | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4445655750/) |
| 12 | MLOps Engineer | Vestas | Chennai | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4427971581/) |
| 13 | Senior Associate - GCP Data Engineer | Equinix | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4420137897/) |
| 14 | Associate | PwC India | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4409098891/) |

**Consulting/staffing/body-shop roles to skip:** **PwC India** (#14 — Big-4 Acceleration
Center advisory delivery, generic "Associate" title with no ML/DS scope), **Deloitte**
(#8 — Big-4 advisory), and **Trinity Life Sciences** (#10 — life-sciences consulting
firm). **Hudson Data** (#9, Data Analyst) is also flagged as staffing/data-services-style
rather than a direct product employer — role fit and company type both scored low for
it. ANZ, Vestas, Solventum, Circle K, and Equinix were scored as "other corporate/GCC"
(company type = 3, not 5) since these listings read as India Global Capability
Centre/shared-services roles ("Data Engineer", "Senior Associate", generic ops titles)
rather than each company's core product engineering — not consulting/body-shop, but not
full product-company weight either.

### Top 5 companies → cold outreach drafts

Top 5 by score are NARBA (#1), Scoutit (#2), LUXASIA (#3), Qualcomm (#4), and Circle K
(#5). Checked existing `job-outreach` Gmail drafts first (35 on file after yesterday's
run) — **LUXASIA and Circle K already had drafts** from the 2026-07-28 run. To keep the
daily slate at 5 distinct, not-yet-contacted, non-consulting companies, outreach was
drafted for the highest-ranked companies with no existing draft, walking down the full
ranked list and skipping flagged consulting/GCC-ambiguous entries where a cleaner
product-company option was available: **NARBA (#1), Scoutit (#2), Qualcomm (#4), Lyric
(#6), and ANZ (#11)**. Note: two older, unlabeled drafts to Qualcomm recruiters exist
from 2026-06-15 and 2026-05-30 (predating the `job-outreach` label convention) — since
they weren't tagged `job-outreach`, Qualcomm was treated as not-yet-contacted under this
log's tracking method, consistent with how prior days only check the labeled set.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| NARBA | Associate AI/ML Engineer: Generative AI Specialist | ML Engineer - Suryatej Lalam - NARBA | `careers@narba.com` (placeholder — unverified domain, replace before sending) | new draft created this run |
| Scoutit | AI/ML Engineer | ML Engineer - Suryatej Lalam - Scoutit | `careers@scoutit.io` (placeholder — unverified domain, replace before sending) | new draft created this run |
| Qualcomm | LPAI ML SW Senior Engineer | ML Engineer - Suryatej Lalam - Qualcomm | `careers@qualcomm.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Lyric | Software Engineer I, AI | ML Engineer - Suryatej Lalam - Lyric | `careers@lyric.ai` (placeholder — unverified, replace before sending) | new draft created this run |
| ANZ | Data Engineer | ML Engineer - Suryatej Lalam - ANZ | `careers@anz.com` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` label (`Label_3`) was applied via `label_thread`
using each new draft's `threadId` (looked up via `list_drafts` after creation) —
succeeded for all 5 new drafts.

## 2026-07-30

**Search window:** last 48 hours (2026-07-28 → 2026-07-30)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** — a direct
`from:naukri.com newer_than:2d` search returned zero results.

Raw emails scanned: 16 threads / 27 messages matched the search. Unlike 2026-07-29's
single-job-per-email format, this window reverted to the multi-job digest format (each
LinkedIn alert email contains one headline job plus several more job cards below it,
separated by rule lines). Digest threads were re-parsed to pull every job card, not just
the headline one used in the email subject — this surfaced far more candidate postings
than the subject lines alone implied. One thread (Optum India, 6 messages) and one
thread (PwC India "Associate", 4 messages) and one thread (Lyric, 3 messages) were
resends of the same alert; a Scoutit posting also appeared across 2 threads. After
extracting all job cards and deduping by Company + Role, **69 unique jobs** went into
scoring.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | AI/ML Engineer – Gen AI & Data Science | M3AI PRIVATE LIMITED | Delhi, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444886100/) |
| 2 | Associate AI/ML Engineer: Generative AI Specialist | NARBA | Noida | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444822533/) |
| 3 | AI/ML Engineer | Scoutit | Delhi, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444838361/) |
| 4 | Data Scientist / Machine Learning Engineer | Azuga, Inc. | Bangalore Urban | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445110049/) |
| 5 | ML Operations Engineer | Signify | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445706151/) |
| 6 | MLOps Engineer – Python | Impact Analytics | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445960714/) |
| 7 | MLOPS ENGINEER – PYTHON | TechnoIogy@IA | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443215621/) |
| 8 | Machine Learning Engineer, Evaluation | HackerRank | Bengaluru East | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4398897010/) |
| 9 | Applied AI ML Associate Senior | JPMorganChase | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446192395/) |
| 10 | Machine Learning Engineer II (Data & Audience Platform Team) | Warner Bros. Discovery | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4429039909/) |
| 11 | Associate AI or ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443010380/) |
| 12 | AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446127766/) |
| 13 | Sr Associate Data Scientist | Amgen | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436960212/) |
| 14 | AI Developer | HighRadius | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445126566/) |
| 15 | Senior AI Engineer | Narrative Intelligence PVT. LTD. | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442392301/) |
| 16 | AI/ML Algorithm Engineer | Voltraniq Private Limited | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4442367484/) |
| 17 | Senior AI Engineer | Teradata | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4397625919/) |
| 18 | Associate AI/ML Engineer | Optum India | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446137709/) |
| 19 | Data Scientist I | Honeywell Technologies | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445679023/) |
| 20 | Machine Learning Engineer | Solventum | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445907254/) |

**Consulting/staffing/body-shop roles to skip:** none of today's top 20 are flagged —
the highest-ranked consulting-type postings this window (**Innova ESI** — IT staffing,
**Zemoso Technologies** — dev-shop/consulting studio, **L.E.K. Consulting**, **EY**,
**PwC India**, **Bain & Company**, **Accenture**, **TCS**, **Infosys**, **NTT DATA**,
**Persistent Systems**, **KPI Partners**, **Parexel**, **iXceed Solutions**,
**Intellectt Inc**, **Talentgigs**, **Jase HR Solutions**, **iThink Digital**,
**Covetus**, **Straive**, **Hudson Data**) all scored low enough (company type = 2) to
fall outside the top 20. **TechnoIogy@IA** (#7) is flagged separately: the company name
came through the LinkedIn email garbled/mis-encoded and its real identity/domain
couldn't be confirmed — treat this listing with caution and verify the actual employer
before applying. **JPMorganChase** (#9), **Warner Bros. Discovery** (#10), **Optum
India** (#11, #12, #18), **Amgen** (#13), and **Honeywell Technologies** (#19) were
scored as "other corporate/GCC" (company type = 3) — large multinational corporates
with India delivery-center-flavored roles, not body-shops but not full product-company
weight either.

### Top 5 companies → cold outreach drafts

Top 5 by score are M3AI (#1), NARBA (#2), Scoutit (#3), Azuga (#4), and Signify (#5).
Checked existing `job-outreach` Gmail drafts first (40 on file after yesterday's run) —
**NARBA, Scoutit, Warner Bros. Discovery, and Optum India already had drafts** from the
2026-07-28/07-29 runs. To keep the daily slate at 5 distinct, not-yet-contacted,
non-consulting companies, outreach was drafted for the highest-ranked companies with no
existing draft, walking down the full ranked list: **M3AI (#1), Azuga (#4), Signify
(#5), Impact Analytics (#6), and HackerRank (#8)**. TechnoIogy@IA (#7) was skipped for
outreach given the unresolved/garbled company identity noted above.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| M3AI PRIVATE LIMITED | AI/ML Engineer – Gen AI & Data Science | ML Engineer - Suryatej Lalam - M3AI PRIVATE LIMITED | `careers@m3ai.com` (placeholder — unverified domain, replace before sending) | new draft created this run |
| Azuga, Inc. | Data Scientist / Machine Learning Engineer | ML Engineer - Suryatej Lalam - Azuga, Inc. | `careers@azuga.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Signify | ML Operations Engineer | ML Engineer - Suryatej Lalam - Signify | `careers@signify.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Impact Analytics | MLOps Engineer – Python | ML Engineer - Suryatej Lalam - Impact Analytics | `careers@impactanalytics.co` (placeholder — unverified domain, replace before sending) | new draft created this run |
| HackerRank | Machine Learning Engineer, Evaluation | ML Engineer - Suryatej Lalam - HackerRank | `careers@hackerrank.com` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` label (`Label_3`) was applied via `label_thread`
using each new draft's `threadId` (looked up via `list_drafts` after creation) —
succeeded for all 5 new drafts.

## 2026-07-31

**Search window:** last 48 hours (2026-07-29 → 2026-07-31)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** — a direct
`from:naukri.com newer_than:2d` search returned zero results.

Raw emails scanned: 15 threads / 24 messages matched the search (12 distinct LinkedIn
digest emails plus a Microsoft "jobs similar to" reminder and a Disney alert; one
LinkedIn newsletter email with no job cards was excluded). Digest emails use the
multi-job-card format (a headline job plus several more cards below it, separated by
rule lines) — all cards were parsed, not just the headline job named in the subject.
The Optum India alert thread had 6 duplicate-content messages and the PwC India
"Associate" alert thread had 4; these were collapsed during Company+Role dedup. After
extracting every job card and deduping by Company + Role, **52 unique jobs** went into
scoring.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | AI Engineer (INDIA) | Trexquant Investment LP | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4317151751/) |
| 2 | AI/ML Engineer – Gen AI & Data Science | M3AI PRIVATE LIMITED | Delhi, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444886100/) |
| 3 | Sr. Lead/Sr. Engineer/Engineer – Enterprise Gen AI | Qualcomm | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4398119988/) |
| 4 | AI Engineer Apprentice | Adobe | Bengaluru East | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445799105/) |
| 5 | ML Operations Engineer | Signify | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445706151/) |
| 6 | Quantitative Researcher - Early Career (INDIA) | Trexquant Investment LP | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4317149828/) |
| 7 | Data Scientist / Machine Learning Engineer | Azuga, Inc. | Bangalore Urban | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445110049/) |
| 8 | Machine Learning Engineer | Solventum | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445907254/) |
| 9 | Machine Learning Engineer, Evaluation | HackerRank | Bengaluru East | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4398897010/) |
| 10 | Senior Software Engineer | Microsoft AI | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444995819/) |
| 11 | Senior Software Engineer - AI Data Platform | Apple | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4421796594/) |
| 12 | Senior Software Developer, AI/ML | Autodesk | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4424085309/) |
| 13 | AI Engineer | Welspun World | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445738407/) |
| 14 | IN_ Associate_ Data Science + Gen AI_ Data Analytics_ Advisory_Gurgaon | PwC India | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445467743/) ⚠️ consulting/body-shop |
| 15 | Data Scientist (Life Science) | Hiring Top MNC Company | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443242334/) ⚠️ consulting/body-shop |
| 16 | Associate- PEG (AI Solutions Engineer) | Bain & Company | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437122147/) ⚠️ consulting/body-shop |
| 17 | Applied AI ML Associate Senior | JPMorganChase | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446192395/) |
| 18 | Machine Learning & LLM Engineer | L.E.K. Consulting | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436061210/) ⚠️ consulting/body-shop |
| 19 | Machine Learning Engineer II ( Data & Audience Platform Team), Hyderabad | Warner Bros. Discovery | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4429039909/) |
| 20 | AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446127766/) |

**Consulting/staffing/body-shop roles to skip:** **PwC India** (#14), **"Hiring Top MNC
Company"** (#15 — a recruiting-agency-style masked listing; real employer unconfirmed,
treat with extra caution), **Bain & Company** (#16), and **L.E.K. Consulting** (#18) are
flagged inside today's top 20. Also scored low enough (company type = 2) to fall outside
the top 20: **EY**, **Zemoso Technologies** (dev-shop/consulting studio), **Straive**,
**Sealcube Secops**, **IQVIA**, **Parexel**, **Persistent Systems**, **KPI Partners**,
**Weekday (YC W21)** (recruiting-agency posting, not the actual employer), **Intellectt
Inc**, **Talentgigs**, **iXceed Solutions**, **Innova ESI**, and **Jase HR Solutions** —
all IT-staffing/BPO/consulting firms. **Qualcomm** (#3, Enterprise Gen AI role) scored
company type = 5 as a genuine chip/product company, but a second Qualcomm posting
("Engineer - Camera Systems (3A)") was excluded from the top 20 on role fit alone
(hardware role, off-target). **JPMorganChase** (#17), **Warner Bros. Discovery** (#19),
and **Optum India** (#20) were scored as "other corporate/GCC" (company type = 3) —
large multinational corporates with India delivery-center-flavored roles, not
body-shops but not full product-company weight either; the same treatment was applied
to **TMUS Global Solutions** and **LPL Financial Global Capability Center** (both
explicitly GCC-named) and to **Volvo Group**, **Philips**, **Ericsson**, **Welspun
World**, and **Honeywell Technologies**, which kept them out of today's top 20.

### Top 5 companies → cold outreach drafts

Top 5 by score are Trexquant Investment LP (#1), M3AI PRIVATE LIMITED (#2), Qualcomm
(#3), Adobe (#4), and Signify (#5). Checked existing `job-outreach` Gmail drafts first —
**Trexquant, M3AI, Qualcomm, Signify, Azuga, Solventum, HackerRank, Microsoft, Apple,
Warner Bros. Discovery, Optum India, LPL Financial, and Philips already had drafts**
from prior runs (Trexquant alone has 4 dating back to 2026-05-29/06-19, predating the
`job-outreach` label convention). To keep the daily slate at 5 distinct, not-yet-
contacted, non-consulting companies, outreach was drafted for the highest-ranked
companies with no existing draft, walking down the full ranked list: **Adobe (#4),
Autodesk (#12), Welspun World (#13), TMUS Global Solutions (#21), and Volvo Group
(#24)**.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| Adobe | AI Engineer Apprentice | ML Engineer - Suryatej Lalam - Adobe | `careers@adobe.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Autodesk | Senior Software Developer, AI/ML | ML Engineer - Suryatej Lalam - Autodesk | `careers@autodesk.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Welspun World | AI Engineer | ML Engineer - Suryatej Lalam - Welspun World | `careers@welspun.com` (placeholder — unverified domain, replace before sending) | new draft created this run |
| TMUS Global Solutions | Engineer AI [T500-27882] | ML Engineer - Suryatej Lalam - TMUS Global Solutions | `careers@tmusglobalsolutions.com` (placeholder — unverified domain, replace before sending) | new draft created this run |
| Volvo Group | Associate Data and AI Engineer | ML Engineer - Suryatej Lalam - Volvo Group | `careers@volvogroup.com` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` label (`Label_3`) was applied via `label_thread`
using each new draft's `threadId` (looked up via `list_drafts` after creation) —
succeeded for all 5 new drafts.

## 2026-08-01

**Search window:** last 48 hours (2026-07-30 → 2026-08-01)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** — a direct
`from:naukri.com newer_than:2d` search returned zero results.

Raw emails scanned: 8 distinct LinkedIn digest/alert threads (14 messages total — the
"Associate AI/ML Engineer at Optum India" alert had 5 duplicate-content messages in one
thread, and "Junior Applied AI Engineer at SpotDraft" had 2; both collapsed during dedup).
One LinkedIn email (`editors-noreply@linkedin.com`, "Suryatej, land your next job") was a
newsletter with no job cards and was excluded. Digest emails use the multi-job-card format
(a headline job plus several more cards below it, separated by rule lines) — all cards
were parsed from plaintext, not just the headline job named in the subject. After
extracting every job card and deduping by Company + Role, **55 unique jobs** went into
scoring.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | AI Engineer | Honasa Consumer Ltd. | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4444545191/) |
| 2 | Artificial Intelligence Engineer | Trademo | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4444557664/) |
| 3 | AI Engineer (INDIA) | Trexquant Investment LP | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4317151751/) |
| 4 | Applied Scientist, Amazon Music - Catalog Quality | Amazon Science | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4446748118/) |
| 5 | Data Scientist / Machine Learning Engineer | Azuga, Inc. | Bangalore Urban | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4445110049/) |
| 6 | Junior Applied AI Engineer | SpotDraft | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4446810058/) |
| 7 | Machine Learning Scientist - II | Wayfair | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4429623173/) |
| 8 | Applied Scientist, Forecasting | Zillow | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4419446278/) |
| 9 | Quantitative Researcher | Mathisys | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4446720540/) |
| 10 | Quantitative Researcher - Early Career (INDIA) | Trexquant Investment LP | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4317149828/) |
| 11 | Senior Analyst-Data Science (Machine Learning/AI & GenAI) | American Express | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4446421826/) |
| 12 | Jr. AI Backend Engineer | CittaAI | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4444560690/) |
| 13 | AI Solutions Engineer / AI Automation Engineer | Myfinser | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4446419296/) |
| 14 | AI Data Scientist | Amgen | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4437811464/) |
| 15 | Data Scientist | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4446869373/) |
| 16 | AI Engineer | Welspun World | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4445738407/) |
| 17 | Data Scientist (Life Science) | Hiring Top MNC Company | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4443242334/) ⚠️ consulting/body-shop |
| 18 | AI Engineer | HuntingCube | Bawana | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4446821851/) ⚠️ consulting/body-shop |
| 19 | Machine Learning & LLM Engineer | L.E.K. Consulting | Delhi | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4436061210/) ⚠️ consulting/body-shop |
| 20 | IN_ Associate_ Data Science + Gen AI_ Data Analytics_ Advisory_Gurgaon | PwC India | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/comm/jobs/view/4445467743/) ⚠️ consulting/body-shop |

**Consulting/staffing/body-shop roles to skip:** **"Hiring Top MNC Company"** (#17 — a
masked, recruiting-agency-style listing; real employer unconfirmed, treat with extra
caution), **HuntingCube** (#18 — small staffing/recruiting agency; the listed location,
Bawana, is an industrial area of Delhi, not a typical office district, another
staffing-agency tell), **L.E.K. Consulting** (#19), and **PwC India** (#20) are flagged
inside today's top 20. Also scored low enough (company type = 2) to fall outside the top
20: **Brillius Technologies** (small unverified dev/staffing shop), **Infosys** (large IT
services/outsourcing), **Bain & Company**, **EXL** (two postings — analytics BPO/
consulting), **Mercer** (HR/management consulting), **Radlabs Technologies Pvt. Ltd**
(small unverified dev shop), **Straive** (data/BPO services), **Sealcube Secops**
(security consulting), and **IQVIA** (CRO/pharma consulting). One listing, **Artificial
Intelligence Officer at Suparshva Swabs (I)** (a surgical-swabs/medical-supplies
manufacturer), looked like a possible company/role mismatch — flagged for manual
verification rather than treated as a hard skip, and it scored low enough on role fit to
land outside the top 20 anyway. Large corporates with India GCC/delivery-center-flavored
roles — **Chubb**, **Ericsson**, **Honeywell Technologies**, **Optum India** (two more
postings beyond #15), **Signify**, **Volvo Group**, **Philips** (two postings), **Target**
(two postings), **GE Vernova**, and **Moody's Corporation** — were scored as "other
corporate/GCC" (company type = 3): not body-shops, but not full product-company weight
either, which kept them out of today's top 20.

### Top 5 companies → cold outreach drafts

Top 5 by score are Honasa Consumer Ltd. (#1), Trademo (#2), Trexquant Investment LP (#3),
Amazon Science (#4), and Azuga, Inc. (#5). Checked existing `job-outreach` Gmail drafts
first — **all five already had drafts** from prior runs (Trexquant alone has 4, dating
back to 2026-05-29; Amazon Science and American Express each have 2; Honasa, Azuga,
Wayfair, Welspun World, Amgen, and Optum India each have 1). To keep the daily slate at 5
distinct, not-yet-contacted, non-consulting companies, outreach was drafted for the
highest-ranked companies with no existing draft, walking down the full ranked list:
**SpotDraft (#6), Zillow (#8), Mathisys (#9), CittaAI (#12), and Myfinser (#13)**.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| SpotDraft | Junior Applied AI Engineer | ML Engineer - Suryatej Lalam - SpotDraft | `careers@spotdraft.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Zillow | Applied Scientist, Forecasting | ML Engineer - Suryatej Lalam - Zillow | `careers@zillow.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Mathisys | Quantitative Researcher | ML Engineer - Suryatej Lalam - Mathisys | `careers@mathisys.com` (placeholder — unverified domain, replace before sending) | new draft created this run |
| CittaAI | Jr. AI Backend Engineer | ML Engineer - Suryatej Lalam - CittaAI | `careers@cittaai.com` (placeholder — unverified domain, replace before sending) | new draft created this run |
| Myfinser | AI Solutions Engineer / AI Automation Engineer | ML Engineer - Suryatej Lalam - Myfinser | `careers@myfinser.com` (placeholder — unverified domain, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` label (`Label_3`) was applied via `label_thread`
using each new draft's `threadId` (looked up via `list_drafts` after creation) —
succeeded for all 5 new drafts.

## 2026-08-02

**Search window:** last 48 hours (2026-07-31 → 2026-08-02)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** — a direct
`from:naukri.com newer_than:2d` search returned zero results.

Raw emails scanned: 8 distinct LinkedIn digest/alert/reminder threads (10 messages total
— "Associate AI or ML Engineer at Optum India" had 2 duplicate-content messages in one
thread, and "Junior Applied AI Engineer at SpotDraft" had 2; both collapsed during
dedup). One thread was a saved-job reminder ("apply now to 'AI & Automation Developer at
Vanden Recycling'") rather than a fresh digest, but it still carried job cards so was
parsed the same way. Digest emails use the multi-job-card format (a headline job plus
several more cards below it, separated by rule lines, including "New jobs from your
other alerts" sections keyed to secondary saved searches) — all cards were parsed from
plaintext, not just the headline job named in the subject. After extracting every job
card and deduping by Company + Role (LinkedIn job ID), **46 unique jobs** went into
scoring.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | AI Engineer | Honasa Consumer Ltd. | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444545191/) |
| 2 | Artificial Intelligence Engineer | Trademo | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444557664/) |
| 3 | Artificial Intelligence Engineer | a21.ai | New Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445038057/) ⚠️ verify — small/unfamiliar company name |
| 4 | AI Solutions Engineer / AI Automation Engineer | Myfinser | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446419296/) |
| 5 | Jr. AI Backend Engineer | CittaAI | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444560690/) |
| 6 | AI/ML Engineer | NationsBenefits | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444586701/) |
| 7 | Jr AI/ML Engineer | NationsBenefits | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444581854/) |
| 8 | Machine Learning Engineer | Fabric | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446967932/) ⚠️ verify — generic name, multiple companies called "Fabric" |
| 9 | Senior Machine Learning Engineer | Siemens | Gurgaon, Haryana, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445163464/) |
| 10 | Machine Learning Scientist - II | Wayfair | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4429623173/) |
| 11 | Applied Scientist, Forecasting | Zillow | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4419446278/) |
| 12 | Applied Scientist, Amazon Music - Catalog Quality | Amazon Science | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446748118/) |
| 13 | Applied AI Engineer | HackerRank | Bengaluru East | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4417204290/) |
| 14 | Data Scientist | Cloudflare | Bengaluru, Karnataka, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4425337888/) |
| 15 | Data Scientist | RapidClaims | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446986285/) |
| 16 | Associate AI or ML Engineer | Optum India | Noida | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4447097803/) |
| 17 | Junior Applied AI Engineer | SpotDraft | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446810058/) |
| 18 | Senior Analyst-Data Science (Machine Learning/AI & GenAI) | American Express | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446421826/) |
| 19 | Quantitative Researcher | Mathisys | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446720540/) |
| 20 | AI/ML Engineer | Cyfuture | Noida | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4430407175/) |

**Consulting/staffing/body-shop roles to skip:** none scored high enough to land inside
today's top 20, but several are worth flagging so they're skipped fast if seen in the
inbox: **Aadhar Stumbh IT LLP** ("Artificial Intelligence Engineer", Delhi — the "IT LLP"
naming pattern is a staffing-shop tell), **Accenture in India** ("AI / ML Engineer",
Gurugram — classic outsourcing/consulting major), **WNS** ("Data Scientist", Gurugram —
BPO/analytics outsourcing), **UST** ("ML Engineer I", Bengaluru — IT services), **Softkode
Technologies** ("Data Scientist", New Delhi — small unverified dev/staffing shop),
**Brillius Technologies** ("AI Engineer", Hyderabad — small unverified dev/staffing shop),
**Infosys** ("Junior AI Engineer", Bengaluru East — large IT services/outsourcing), and
**EXL** (two postings — "C1 - Modelling" and "C1 - Credit Risk Modeler", both Gurugram —
analytics BPO/consulting). **HuntingCube** ("AI Engineer", Bawana) is a small
staffing/recruiting agency — the listed location, Bawana, is an industrial area of Delhi
rather than a typical office district, another staffing-agency tell; it scored a
literal 12 (Delhi location = 5) but is flagged here as a skip regardless of score.
Two listings are flagged for **manual verification rather than a hard skip**: **a21.ai**
(#3) and **Fabric** (#8) — both are real-looking product/startup names but too generic
or unfamiliar to confirm from the email alone; verify the company before applying or
before sending the drafted outreach below. Large corporates with India GCC/delivery-
center-flavored roles — **Vanden Recycling**, **Nielsen**, **JPMorganChase**, **Deutsche
Bank**, **Honeywell Technologies**, **Optum India** (one more posting beyond #16, Data
Scientist in Hyderabad), **Cisco**, **GEA Group**, **NexBase**, **GE Vernova**, **Chubb**,
**Moody's Corporation**, **Take-Two Interactive**, **JB Group of Companies**, and
**Nokia** — were scored as "other corporate/GCC" or off-target role fit, which kept them
out of today's top 20.

### Top 5 companies → cold outreach drafts

Top 5 by score are Honasa Consumer Ltd. (#1), Trademo (#2), a21.ai (#3), Myfinser (#4),
and CittaAI (#5). Checked existing `job-outreach` Gmail drafts first — **Myfinser and
CittaAI already had drafts** from the 2026-08-01 run. To keep the daily slate at 5
distinct, not-yet-contacted, non-consulting companies, outreach was drafted for the
highest-ranked companies with no existing draft, walking down the full ranked list:
**Honasa Consumer Ltd. (#1), Trademo (#2), a21.ai (#3), NationsBenefits (#6/#7, one draft
for the company), and Fabric (#8)**.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| Honasa Consumer Ltd. | AI Engineer | ML Engineer - Suryatej Lalam - Honasa Consumer Ltd. | `careers@honasa.in` (placeholder — unverified, replace before sending) | new draft created this run |
| Trademo | Artificial Intelligence Engineer | ML Engineer - Suryatej Lalam - Trademo | `careers@trademo.com` (placeholder — unverified, replace before sending) | new draft created this run |
| a21.ai | Artificial Intelligence Engineer | ML Engineer - Suryatej Lalam - a21.ai | `careers@a21.ai` (placeholder — unverified domain; company identity unconfirmed, verify before sending) | new draft created this run |
| NationsBenefits | AI/ML Engineer | ML Engineer - Suryatej Lalam - NationsBenefits | `careers@nationsbenefits.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Fabric | Machine Learning Engineer | ML Engineer - Suryatej Lalam - Fabric | `careers@fabric.inc` (placeholder — unverified domain; multiple companies share this name, verify before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` label (`Label_3`) was applied via `label_thread`
using each new draft's `threadId` (looked up via `list_drafts` after creation) —
succeeded for all 5 new drafts.


## 2026-08-04

**Pipeline gap note:** the previous log entry was dated 2026-08-02 — the routine appears
to have skipped 2026-08-03 (2 days stale as of this run). This run covers a fuller
48-hour window to catch anything that would otherwise have been missed.

**Search window:** last 48 hours (2026-08-02 → 2026-08-04)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** — a direct
`from:naukri.com newer_than:2d` search returned zero results.

Raw emails scanned: 6 distinct LinkedIn threads (8 messages total — the "Applied AI ML
Associate at JPMorganChase" alert fired 3 separate digest emails within the window, all
parsed). One thread ("Suryatej, apply to Senior Machine Learning Engineer at Siemens and
more", a weekly saved-jobs reminder template) carried no job cards in its body — only a
preheader mention of the Siemens role already known from the 2026-08-02 run — so it
contributed no new listings beyond confirming that role is still open. Digest emails use
the multi-job-card format (a headline job plus several more cards below it, including
"New jobs from your other alerts" sections keyed to secondary saved searches) — all cards
were parsed from plaintext, not just the headline job named in the subject. After
extracting every job card and deduping by Company + Role (LinkedIn job ID, collapsing one
"Data Scientist, Google Ads" @ Google posting that appeared for both Gurugram and
Bengaluru), **34 unique jobs** went into scoring.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | AI Engineer, Portfolio Management Group, Associate | BlackRock | Gurgaon | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438637224/) |
| 2 | AI/ML Analyst | Citi | Haryana, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4447479954/) |
| 3 | Data Scientist, Google Ads | Google | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4447173955/) (also posted for Bengaluru, job 4447191092) |
| 4 | Senior Machine Learning Engineer | Siemens | Gurgaon | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445163464/) |
| 5 | Associate Data Scientist (Commercial) | Amgen | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4447809489/) |
| 6 | Senior AI Engineer | Teradata | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4402139915/) |
| 7 | Agentic AI Engineer | Spore N Sprouts | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4447836947/) ⚠️ verify — small/unfamiliar company name |
| 8 | Applied AI Engineer | Convatec | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439091242/) |
| 9 | Data Science Associate | The Depository Trust & Clearing Corporation (DTCC) | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439046946/) |
| 10 | Applied AI ML Associate | JPMorganChase | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4447746545/) |
| 11 | Applied AI ML Associate Senior - AI Engineer | JPMorganChase | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4447588411/) |
| 12 | Associate Engineer - AI/ML with Python | HARMAN India | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4412930013/) |
| 13 | Machine Learning Engineer - L3 | RZR | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4411227981/) |
| 14 | Data Scientist 1, Knowledge Management | eBay | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4445544077/) |
| 15 | ML Engineer I | UST | Noida | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4361810648/) ⚠️ consulting/IT services — skip fast |
| 16 | Compliance Engineering - Neon Platform - Associate | Goldman Sachs | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4379689055/) |
| 17 | Software Engineer - Modelzoo | NXP Semiconductors | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4389705912/) |
| 18 | AI Engineer, Portfolio Management Group, Associate | BlackRock | Mumbai Metropolitan Region | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438619979/) |
| 19 | Data Science Research Senior Analyst | Accenture in India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439378798/) ⚠️ consulting — skip fast |
| 20 | Data Scientist | Optum India | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4447588660/) |

**Consulting/staffing/body-shop roles to skip:** two make today's top 20 anyway (UST #15,
Accenture in India #19 — flagged above, scores earned the slot but treat as skip-fast).
Below the cutoff, worth flagging so they're skipped fast if seen in the inbox:
**Virtusa** ("GEN AI", Chennai — IT services/consulting), **IBM** ("Data Engineer-Data
Platforms-Google", Bengaluru — India roles here skew services/GBS), **Quest Global** ("AI
Engineer", Bengaluru — engineering services/consulting), **Impetus** ("GCP_GenAI_SSE",
Bengaluru — data engineering consulting shop, despite the GCP/GenAI stack match), **Bain
& Company** ("Associate – Data Ops & Estimations", Gurugram — classic consulting), and
**Firstsource** ("Senior Software Engineer", Hyderabad — BPO/outsourcing). Two listings
are recruiting/staffing agencies and were excluded from the ranked table entirely
regardless of score, same treatment as prior runs: **Talentgigs** ("Agentic AI Engineer",
Hyderabad — the name itself is a staffing-agency tell) and **HuntingCube** ("AI
Engineer", Bawana — Bawana is an industrial area of Delhi rather than a typical office
district, another staffing-agency tell; this is the same company flagged in the
2026-08-02 run). Large corporates with generic/off-target roles — **Google** ("Engineering
Analyst, Trust and Safety, YouTube", Hyderabad), **Rippling** ("Software Engineer II -
Data Catalog", Bengaluru), **Cisco** ("Data Engineer", Bengaluru), **HSBC** ("Analyst-
Data Engineering", Bengaluru), and **JPMorganChase** ("Software Engineer II - Python",
Hyderabad) — scored too low on role fit (data engineering / generic SWE, not core
ML/applied-AI) to make today's top 20.

### Top 5 companies → cold outreach drafts

Top 5 distinct companies by score, walking the ranked list: BlackRock (#1), Citi (#2),
Google (#3), Siemens (#4), Amgen (#5). Checked existing `job-outreach` Gmail drafts
first — **Citi (drafted 2026-07-25) and Amgen (drafted 2026-07-25) already had
outreach**, so both were skipped to keep the slate at 5 distinct, not-yet-contacted
companies. Continued down the ranked list, skipping Spore N Sprouts (#7, flagged above
for identity verification — didn't want to draft outreach to an unconfirmed company) in
favor of the next verified, non-consulting company with no existing draft: **BlackRock
(#1), Google (#3), Siemens (#4), Teradata (#6), and Convatec (#8)**.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| BlackRock | AI Engineer, Portfolio Management Group, Associate | ML Engineer - Suryatej Lalam - BlackRock | `careers@blackrock.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Google | Data Scientist, Google Ads | ML Engineer - Suryatej Lalam - Google | `careers@google.com` (placeholder — unverified; Google does not accept unsolicited applications at this address, replace before sending) | new draft created this run |
| Siemens | Senior Machine Learning Engineer | ML Engineer - Suryatej Lalam - Siemens | `careers@siemens.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Teradata | Senior AI Engineer | ML Engineer - Suryatej Lalam - Teradata | `careers@teradata.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Convatec | Applied AI Engineer | ML Engineer - Suryatej Lalam - Convatec | `careers@convatec.com` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` label (`Label_3`) was applied via `label_thread`
using each new draft's `threadId` (looked up via `list_drafts` after creation) —
succeeded for all 5 new drafts.

## 2026-08-05

**Search window:** last 48 hours (2026-08-03 → 2026-08-05)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`from:naukri.com newer_than:2d`). **No Naukri
job-alert emails were found in this window** — same as every prior run.

**Volume note:** only 7 distinct threads matched in the 48-hour window (one, "don't miss
your exclusive Premium events," was a LinkedIn marketing email, not a job alert). Of the
remaining 6 job-alert threads, **4 were the same digests already parsed in the 2026-08-04
run** (the "ml platform engineer," "applied scientist," and "mlops engineer" alert digests
carrying BlackRock ×2, Citi, HARMAN, UST, RZR, Virtusa, Google Trust & Safety — all dated
2026-08-03 and already scored/logged yesterday), plus the weekly "Suryatej, apply to
Senior Machine Learning Engineer at Siemens and more" reminder, which again carried no job
cards in its body (same as 2026-08-04). Re-listing those in today's ranked table would
just be yesterday's table again, so they're excluded here as duplicates rather than
re-scored. That left **2 genuinely new threads**: a "Jobs that match your profile" digest
(6 job cards, headlined by Warner Bros. Discovery) and a 4×-resent "machine learning
engineer in Gurugram" alert (which itself bundled 7 more cards across its primary and
"other alerts" sections, headlined by HYrEzy Tech Solutions). After extracting every card
from those 2 threads and deduping by Company + Role (collapsing one "Engineering Graduate
Associate" @ LSEG posting that appeared for both Hyderabad and Bengaluru), **12 unique new
jobs** went into scoring.

### Ranked Top 12 (fewer than 20 available this run — see volume note above)

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Data Scientist (Fintech / Applied ML) | HYrEzy Tech Solutions | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4447905095/) ⚠️ verify — small/unfamiliar company |
| 2 | Data Science Builder | Cars24 | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4447908498/) |
| 3 | Machine Learning Engineer II (Data & Audience Platform Team) | Warner Bros. Discovery | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4429039909/) |
| 4 | Deputy Manager - Data Science | PepsiCo | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4390003782/) |
| 5 | Artificial Intelligence Engineer | Solis Technology | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446056277/) ⚠️ verify — unfamiliar company name |
| 6 | AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446127766/) |
| 7 | Associate AI or ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4443010380/) |
| 8 | Software Engineer - AI/ML | ValGenesis | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4444923128/) |
| 9 | Engineering Graduate Associate | LSEG | Hyderabad (also posted Bengaluru, job 4447667532) | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4447655794/) |
| 10 | AI/ML Engineer | Optum India | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4448132424/) |
| 11 | Gen AI-AI and Data Science Engineer III | Deloitte | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4425075810/) ⚠️ consulting — skip fast |
| 12 | GEN AI Developer | Birlasoft | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439874927/) ⚠️ consulting/IT services — skip fast |

**Consulting/staffing/body-shop roles to skip:** two make today's list anyway (Deloitte
#11, Birlasoft #12 — flagged above, treat as skip-fast). No recruiting/staffing agencies
turned up in the 2 new threads this run.

**Already reported yesterday (excluded from the table above, not re-scored):** BlackRock
— AI Engineer, Portfolio Management Group, Associate (Gurgaon + Mumbai), Citi — AI/ML
Analyst (Haryana), HARMAN India — Associate Engineer AI/ML with Python (Bengaluru), UST —
ML Engineer I (Noida, consulting), RZR — Machine Learning Engineer L3 (Bengaluru),
Virtusa — GEN AI (Chennai, consulting), Google — Engineering Analyst, Trust and Safety,
YouTube (Hyderabad, off-target). All were already scored and logged in the 2026-08-04
entry above.

### Top 5 companies → cold outreach drafts

Only **2 of the 12 new jobs** led to a fresh outreach draft — walking the ranked list and
applying the same filters as every prior run quickly exhausted the candidates:
- **#1 HYrEzy Tech Solutions** and **#5 Solis Technology** — skipped, unfamiliar/unverified
  companies (same policy as Spore N Sprouts on 2026-08-04).
- **#3 Warner Bros. Discovery** — skipped, already has a `job-outreach` draft
  (`careers@wbd.com`, created 2026-07-24).
- **#6/#7/#10 Optum India** — skipped, already has a `job-outreach` draft
  (`careers@optum.com`, created 2026-07-24).
- **#8 ValGenesis** — skipped, already has a `job-outreach` draft (created 2026-07-27).
- **#9 LSEG** — skipped, already has a `job-outreach` draft (`careers@lseg.com`, created
  2026-07-23).
- **#11 Deloitte, #12 Birlasoft** — skipped, consulting/IT services.

That leaves only **Cars24 (#2) and PepsiCo (#4)** as valid, not-yet-contacted, non-
consulting targets from today's new listings — the slate is 2 instead of 5 this run
because the inbox simply didn't surface 5 fresh candidates that clear every filter.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| Cars24 | Data Science Builder | ML Engineer - Suryatej Lalam - Cars24 | `careers@cars24.com` (placeholder — unverified, replace before sending) | new draft created this run |
| PepsiCo | Deputy Manager - Data Science | ML Engineer - Suryatej Lalam - PepsiCo | `careers@pepsico.com` (placeholder — unverified, replace before sending) | new draft created this run |

**⚠️ PepsiCo duplicate-draft flag:** a search for existing PepsiCo outreach turned up a
prior draft to `talent@pepsico.com` (created 2026-07-12, same Deputy Manager - Data
Science / Gurugram role) that does **not** carry the `job-outreach` label, so it wasn't
caught by the label-based dedup check this run used. Both drafts now exist — recommend
deleting one (or merging) before sending to avoid double outreach to the same recruiter
pipeline.

**Note on labeling:** the `job-outreach` label (`Label_3`) was applied via `label_thread`
using each new draft's `threadId` (looked up via `list_drafts` after creation) —
succeeded for both new drafts.

## 2026-08-06

**Search window:** last 48 hours (2026-08-04 → 2026-08-06)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`, digest
subject pattern "X is hiring: Y") and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window** — same as
every prior run.

**Volume note:** 5 distinct LinkedIn job-alert digest emails matched the window (Nielsen,
Crimson Energy Experts, lululemon, American Express, and a repeat WBD "jobs picked for
you" board), each carrying 1 headline job plus a "New jobs from your other alerts"
secondary list. Also present but excluded as noise: 17 individual "your application was
sent to X" confirmation emails (not job alerts) and 1 LinkedIn Premium marketing email.
Parsing all 5 digest bodies yielded 28 unique job cards after deduping by Company + Role.

**Already reported in prior runs (excluded from today's table, not re-scored):** Warner
Bros. Discovery — Machine Learning Engineer II (same job ID, reported since 2026-07-20,
has outreach draft), Optum India — AI/ML Engineer and Associate AI or ML Engineer
(Hyderabad, same job IDs as 2026-08-05), Deloitte — Gen AI-AI and Data Science Engineer
III (same job ID as 2026-08-05, consulting), Birlasoft — GEN AI Developer (same job ID
as 2026-08-05, consulting), ValGenesis — Software Engineer - AI/ML (same job ID as
2026-08-05, has outreach draft), American Express — Analyst-Data Science (same job ID as
several prior runs, has outreach draft), FedEx — Data Scientist 1 (same job ID as
2026-07-24 run). That leaves 21 new postings, further deduped to 2 near-duplicate
Accenture "AI / ML Engineer" (Bengaluru) postings down to 1, for 18 net new candidates
below.

### Ranked Top 18

(Only 18 net-new, not-already-reported postings turned up in this window — reported as-is
rather than padding to 20.)

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Associate AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4448803708/) |
| 2 | AI Engineer | Teradata | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4448218072/) |
| 3 | AI Engineer | Teradata | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4448210227/) |
| 4 | Machine Learning Engineer 2 | Adobe | Bengaluru East | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439169182/) |
| 5 | AI / ML Engineer | GoodScore | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4448185727/) |
| 6 | Applied AI/ML Scientist [T500-28135] | lululemon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4448173947/) |
| 7 | Applied Scientist, Alexa International Tech | Amazon | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4448319209/) |
| 8 | Junior MLOps Engineer | Alegeus | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4447930211/) |
| 9 | AI / ML Data Scientist I | Nielsen | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446620362/) |
| 10 | Computer Vision Engineer | Crimson Energy Experts Pvt Ltd | Delhi, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4448265881/) ⚠️ verify — small/unfamiliar company |
| 11 | MLOps Engineer | NStarX | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4448174820/) ⚠️ verify — unfamiliar company, possible boutique AI consultancy |
| 12 | Applied AI ML Associate Senior-Data Engineer | JPMorganChase | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4448194733/) |
| 13 | Data Scientist-Artificial Intelligence | IBM | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446233811/) |
| 14 | Software Engineer | Microsoft | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4448191323/) |
| 15 | AI / ML Engineer | Accenture in India | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4448327708/) ⚠️ consulting — skip fast |
| 16 | Data Scientist | Deloitte | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4446283575/) ⚠️ consulting — skip fast |
| 17 | Machine Learning, Associate, WM Admin, Wealth Management | Morgan Stanley | Mumbai | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4448288477/) |
| 18 | Data Engineer | Accenture in India | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4448371557/) ⚠️ consulting — skip fast |

**Consulting/staffing/body-shop roles to skip:** Accenture in India (#15, #18) and
Deloitte (#16) — flagged above, treat as skip-fast. IBM (#13) is scored as "other
corporate/GCC" (company type = 3) rather than pure product, since the listing may sit
inside IBM Consulting rather than IBM's product/research org — worth a quick check before
applying, though not a hard skip.

**Unverified/small-company flags:** Crimson Energy Experts Pvt Ltd (#10) and NStarX
(#11) are unfamiliar names with no public footprint checked — verify legitimacy and
comp band before applying, same policy as HYrEzy Tech Solutions and Solis Technology in
the 2026-08-05 run.

### Top 5 companies → cold outreach drafts

Only **3 of 18** ranked jobs led to a fresh outreach draft — walking the ranked list and
checking existing Gmail drafts (`list_drafts` search, confirmed via draft recipient
addresses) exhausted the non-duplicate, non-consulting, verified candidates before
reaching 5:
- **#1 Optum India, #2/#3 Teradata, #4 Adobe, #5 GoodScore, #7 Amazon, #8 Alegeus, #9
  Nielsen, #12 JPMorganChase, #14 Microsoft** — all skipped, confirmed existing
  `job-outreach` drafts on file (`careers@optum.com`, `careers@teradata.com`,
  `careers@adobe.com`, `careers@goodscore.in`, `careers@amazon.com`,
  `careers@alegeus.com`, `careers@nielsen.com`, JPMorgan's India recruiting address, and
  `careers@microsoft.com` respectively).
- **#10 Crimson Energy Experts, #11 NStarX** — skipped, unverified/unfamiliar companies
  (see flag above).
- **#15, #16, #18 Accenture in India / Deloitte** — skipped, consulting/IT services.

That left **lululemon (#6), IBM (#13), and Morgan Stanley (#17)** as the only valid,
not-yet-contacted, non-consulting, verified targets from today's new listings — the slate
is 3 instead of 5 this run because the top of the ranked list is dominated by companies
already worked through in prior runs.

| Company | Role targeted | Draft subject | Recipient in draft | Status |
|---|---|---|---|---|
| lululemon | Applied AI/ML Scientist | ML Engineer - Suryatej Lalam - lululemon | `careers@lululemon.com` (placeholder — unverified, replace before sending) | new draft created this run |
| IBM | Data Scientist-Artificial Intelligence | ML Engineer - Suryatej Lalam - IBM | `careers@ibm.com` (placeholder — unverified, replace before sending) | new draft created this run |
| Morgan Stanley | Machine Learning, Associate, WM Admin, Wealth Management | ML Engineer - Suryatej Lalam - Morgan Stanley | `careers@morganstanley.com` (placeholder — unverified, replace before sending) | new draft created this run |

**Note on labeling:** the `job-outreach` label (`Label_3`) was applied via `label_thread`
using each new draft's `threadId` (looked up via `list_drafts` after creation) —
succeeded for all three new drafts.
