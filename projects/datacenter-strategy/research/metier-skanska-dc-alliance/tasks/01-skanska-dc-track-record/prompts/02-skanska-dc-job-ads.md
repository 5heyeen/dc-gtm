# Prompt 02: skanska-dc-job-ads

> **Prompt:** What do Skanska's Nordic job ads on finn.no, LinkedIn, and Skanska's own career pages reveal about current DC-specific hiring? Search "datasenter" OR "data center" on Skanska Norway, Skanska Sverige, Skanska Suomi career pages and Nordic job boards. For each role capture (a) title, (b) required competencies and years of experience, (c) project named if any, (d) location, (e) posting date. Pay special attention to MEP, commissioning, procurement, and senior project-director roles, which signal which capabilities Skanska is building vs. subcontracting.

---

## Method note and access limitations

Direct WebFetch requests to finn.no's Skanska employer profile (`finn.no/job/employer/company/62`), to `skanska.se/om-skanska/jobba-hos-oss/lediga-jobb/`, to `group.skanska.com/careers/find-your-job/`, and to the Skanska Finland data-center page all returned HTTP 403 (the sites block automated fetching). As a result, the job-ad detail that would normally be extracted per ad (required years of experience, full competencies, posting date) is **not directly retrievable** via this agent. Findings below therefore rely on (i) search-engine titles and snippets for Skanska's Nordic job boards and (ii) Skanska's own press releases announcing named DC projects. Where an ad's internal text cannot be quoted verbatim, the item is moved to **Unverified Observations**.

---

## Norway

- **Skanska Norway career portal (live, DC-specific ads not indexed in snippets).** The Skanska Norway openings page is public at `skanska.no/hvem-vi-er/jobb-i-skanska/ledige-stillinger/`, per search: *"Ledige stillinger | www.skanska.no"* — [Source](https://www.skanska.no/hvem-vi-er/jobb-i-skanska/ledige-stillinger/). Snippet text did not surface any ad containing the string "datasenter" or "data center" in the indexed listings retrieved.
- **One Skanska Norway finn.no ad visible in search: project engineer, Skedsmokorset (not DC-specific).** *"Prosjektingeniør – Team automatisk overvåking og sensorikk · Skedsmokorset · Skanska"* — [Source](https://www.finn.no/job/ad/457543550). No datacenter reference in the title/snippet.
- **Named Norwegian DC project is active and staffing-relevant (Gromstul / Skien, Telemark).** *"Skanska has signed a contract with WS Computing AS for preparatory groundwork and foundations for a new hyperscale data center at Gromstul in Skien municipality, Norway"* — [Source](https://group.skanska.com/media/press-releases-articles/278070/Skanska-prepares-for-new-data-center-in-Telemark,-Norway,-for-NOK-1.1-billion,-about-SEK-1.1-billion). A follow-on contract was also signed: *"Skanska signs additional contract to build a data center in Telemark, Norway, for NOK 569M"* — [Source](https://group.skanska.com/media/press-releases-articles/284876/Skanska-signs-additional-contract-to-build-a-data-center-in-Telemark,-Norway,-for-NOK-569M,-about-SEK-560M).

## Sweden

- **Skanska Sweden openings page is live, but DC-specific ads did not surface in indexed snippets.** *"Hitta lediga jobb hos Skanska | skanska.se"* — [Source](https://www.skanska.se/om-skanska/jobba-hos-oss/lediga-jobb/). No "datacenter"/"datacenter" titles appeared among the indexed results retrieved via WebSearch.
- **LinkedIn Sweden indexes generic "Skanska Projektledare" roles, none tagged data-center in snippet.** *"5 jobb som matchar Skanska Projektledare i Sverige"* — [Source](https://se.linkedin.com/jobs/skanska-projektledare-jobs).
- **Indeed Sweden shows ~50+ Skanska openings nationally, none DC-tagged in snippet text.** *"50+ jobb som Skanska, anställning 7 februari 2026"* — [Source](https://se.indeed.com/q-skanska-jobb.html).

## Finland

- **Skanska Finland has a dedicated data-center positioning page and an announced EUR 95M project.** *"Skanska signed a contract with a technology company to build a data center facility in Finland worth EUR 95M, about SEK 1.1 billion. Construction will start during the fall 2025 and will be completed by the fall in 2026"* — [Source](https://www.prnewswire.com/news-releases/skanska-builds-data-center-in-finland-for-eur-95m-about-sek-1-1-billion-302546147.html). The Skanska Finland English-language data-center landing page exists: *"Your trusted international and local partner in data center construction | www.skanska.fi"* — [Source](https://www.skanska.fi/tietoa-skanskasta/about-skanska-in-english/data-centers/).
- **Finland-side DC management talent identifiable on LinkedIn, but roles are not shown as open ads.** *"Timo Markkanen - Project Development Director at Skanska Talonrakennus Oy"* — [Source](https://www.linkedin.com/in/timo-markkanen-96256180/). *"Maiju Tarkiainen - Skanska"* — [Source](https://www.linkedin.com/in/maiju-tarkiainen-18a78345/). *"Teemu Makkonen - IT Service Manager - Skanska"* — [Source](https://www.linkedin.com/in/teemu-makkonen-a18b0588/). *"Mikko Borg - Contract Manager - Skanska Finland"* — [Source](https://www.linkedin.com/in/mikko-borg/).

## Denmark

- No Skanska Denmark DC-specific job ads surfaced in search. Skanska's Danish construction unit was not returned in any of the queries for "datacenter", "data center", MEP, commissioning, procurement, or project director. See **Unverified Observations**.

---

## Inferred Findings

**Inferred: Skanska is staffing DC work through its existing general-contracting organization (project managers, procurement, engineering leads) rather than running a visibly separate DC-branded hiring campaign in the Nordics.**
- **Based on:**
  - *"Skanska has signed a contract with WS Computing AS for preparatory groundwork and foundations for a new hyperscale data center at Gromstul in Skien municipality, Norway"* — [Source](https://group.skanska.com/media/press-releases-articles/278070/Skanska-prepares-for-new-data-center-in-Telemark,-Norway,-for-NOK-1.1-billion,-about-SEK-1.1-billion)
  - *"Prosjektingeniør – Team automatisk overvåking og sensorikk · Skedsmokorset · Skanska"* — [Source](https://www.finn.no/job/ad/457543550) (the only Skanska Norway finn.no ad title retrieved; generic engineering, no DC label)
- **Reasoning:** Despite two active Norwegian DC contracts (Gromstul Phase 1 and additional NOK 569M package) and a EUR 95M Finnish DC contract, the finn.no and skanska.se search snippets retrieved do not show any publicly indexed job ads carrying "datasenter"/"data center" in their titles. The most plausible reading is that Skanska fills DC roles from its standing pool of civil/structural project managers under generic titles, rather than advertising DC-flagged vacancies externally.

**Inferred: MEP, commissioning, and hyperscale procurement competencies for the Nordic DC pipeline are likely being supplied by specialist subcontractors and by Skanska's internal cross-border resources, not by Nordic-market external hires.**
- **Based on:**
  - *"Skanska signed a contract with a technology company to build a data center facility in Finland worth EUR 95M, about SEK 1.1 billion"* — [Source](https://www.prnewswire.com/news-releases/skanska-builds-data-center-in-finland-for-eur-95m-about-sek-1-1-billion-302546147.html)
  - *"There are currently two experienced MEP QA/QC Manager positions available for a large-scale data centre project team in Norway"* (industry aggregator, not Skanska-branded) — [Source](https://www.careerstructure.com/jobs/data-centre/in-norway)
- **Reasoning:** The live Norwegian DC MEP QA/QC openings appear on generalist DC job boards (not Skanska career sites), and no Skanska Nordic career snippet retrieved contains the words "MEP", "commissioning", or "ibruktakelse". Combined with Skanska's scale, the most likely pattern is that MEP/commissioning trades sit with subcontractors while Skanska holds GC, civil/structural, schedule, and procurement leadership in-house.

---

## Unverified Observations

- Posting dates, exact required years of experience, and full competency lists for individual Skanska Nordic DC ads could not be captured because finn.no, skanska.se, skanska.fi, and group.skanska.com all returned HTTP 403 to WebFetch during this run.
- Whether Skanska Norway's live openings list currently contains any role explicitly tied to the Gromstul/Skien DC project (e.g., "Prosjektleder datasenter Skien") is not verifiable from the search snippets retrieved; the Skanska Norway openings URL is live but its ad titles were not returned in snippet form.
- Whether Skanska Sweden is hiring a dedicated DC project director or commissioning manager for any named Swedish hyperscale site is not verifiable from snippets retrieved.
- Whether Skanska Denmark has any DC-flagged vacancies is not verifiable; no Danish-language Skanska DC search results were returned.
- The status (open vs. filled) of the LinkedIn-profiled Skanska Finland DC-relevant individuals (Markkanen, Tarkiainen, Makkonen, Borg) cannot be inferred from profile URLs alone and is not an "ad."

---

## Sources

- https://www.finn.no/job/employer/company/62
- https://www.finn.no/job/ad/457543550
- https://www.skanska.no/hvem-vi-er/jobb-i-skanska/ledige-stillinger/
- https://www.skanska.se/om-skanska/jobba-hos-oss/lediga-jobb/
- https://se.linkedin.com/jobs/skanska-projektledare-jobs
- https://se.indeed.com/q-skanska-jobb.html
- https://www.skanska.fi/tietoa-skanskasta/about-skanska-in-english/data-centers/
- https://www.prnewswire.com/news-releases/skanska-builds-data-center-in-finland-for-eur-95m-about-sek-1-1-billion-302546147.html
- https://group.skanska.com/media/press-releases-articles/278070/Skanska-prepares-for-new-data-center-in-Telemark,-Norway,-for-NOK-1.1-billion,-about-SEK-1.1-billion
- https://group.skanska.com/media/press-releases-articles/284876/Skanska-signs-additional-contract-to-build-a-data-center-in-Telemark,-Norway,-for-NOK-569M,-about-SEK-560M
- https://group.skanska.com/careers/find-your-job/
- https://www.careerstructure.com/jobs/data-centre/in-norway
- https://www.linkedin.com/in/timo-markkanen-96256180/
- https://www.linkedin.com/in/maiju-tarkiainen-18a78345/
- https://www.linkedin.com/in/teemu-makkonen-a18b0588/
- https://www.linkedin.com/in/mikko-borg/
