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
