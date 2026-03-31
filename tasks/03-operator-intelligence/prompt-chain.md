# Socratic Research Prompts: Phase 5A-5B — Operator Intelligence Profiles

> **Topic:** Company-level intelligence on every significant DC operator active or entering Norway — their strategic position (money, customers, land, power), corporate strategy, execution model, and how each maps to a tailored Metier + Norconsult value proposition.
> **Depends on:** 1A (context brief), 1C (9 customer personas), 1E (risk taxonomy), 2B (regulatory landscape), 3B (GTM strategy)
> **Feeds into:** 3D (action plan), 4A (service design), 4B (pricing), 4C (objection handling)

---

## 🟢 5A. Operator Strategic Position Mapping

**Run after Phase 1-2 core prompts.** This is the company-level intelligence that the existing persona-level analysis (1C) doesn't provide. It answers: which specific operators have what, need what, and are reachable by Metier.

**⚠️ CROSS-REFERENCE:** Existing operator research is stored in this Notion database — do NOT duplicate: https://www.notion.so/32d64f44828381f09c19cb3495d16d96?v=32d64f4482838132b519000ce3417478. Check what's already been researched before running these prompts. Only research operators and data points not already captured there.

**✅ Prompt 5A.1: Operator-by-Operator Strategic Position Assessment**

```
For every significant data center operator currently active, announced, or credibly planning to develop in Norway, build a strategic position assessment. This is not about persona types — it's about specific companies.

For EACH operator, research and document:

1. CAPITAL POSITION ("Money")
   - Who owns them? (PE fund, public company, sovereign wealth, hyperscaler balance sheet, family office, utility parent)
   - What is their funding structure? (Equity committed, debt capacity, project finance, REIT structure)
   - What CAPEX have they committed or announced for Norway specifically?
   - What is their capital deployment timeline pressure? (Fund lifecycle, GPU delivery schedules, tenant commitments)
   - How does their capital structure affect their risk tolerance and decision speed?

2. DEMAND POSITION ("Customers")
   - Do they have pre-committed tenants/customers for their Norwegian capacity? Who?
   - Are they building speculative capacity or build-to-suit?
   - What is their customer concentration risk — one anchor tenant vs. diversified portfolio?
   - For hyperscalers: is this for their own workloads? Which workloads — cloud, AI training, AI inference, enterprise?
   - How does their demand position affect their urgency and willingness to pay for advisory?

3. SITE POSITION ("Land") & POWERED LAND ACQUISITION STRATEGIES
   - What sites have they secured in Norway? Where exactly?
   - What is the zoning status of each site? (Reguleringsplan approved? In process? Not started?)
   - What is the site's physical readiness? (Greenfield, brownfield, existing facility, industrial park)
   - Do they have optionality on additional land for expansion?
   - What municipal and community dynamics affect their site? (Supportive kommune? Opposition? Environmental sensitivities?)
   - HOW did they acquire their site(s)? Map the different powered land acquisition strategies in Norway:
     a. Industrial sites in decline selling to DC operators (e.g., legacy smelters, paper mills, industrial parks with existing grid connections) — which sites have been repurposed? Which are available?
     b. Utility-owned land with grid access being offered to DC developers
     c. Municipal land being zoned for DC through proactive kommune strategies
     d. Greenfield sites near substations or transmission lines
     e. Mine/tunnel conversions (Lefdal model)
     f. Co-location with industrial parks (Mo Industripark model)
   - What is the "powered land" premium — how much more valuable is a site with existing grid infrastructure vs. a greenfield site that needs new grid connection?
   - Which municipalities or industrial landowners are actively marketing sites to DC operators?

4. POWER POSITION ("Grid")
   - What grid capacity have they reserved with Statnett? (MW reserved, grid connection point, voltage level)
   - What is the status of their grid connection? (Reservation only? NVE concession applied? Granted? Physical infrastructure under construction?)
   - What is the realistic timeline from current status to energized connection?
   - What grid infrastructure needs to be built? (New substation? Transmission line? Who is responsible — the operator, the grid company, or both?)
   - What is their power sourcing strategy? (Grid only? On-site generation? PPA? Renewable certificates?)

5. FIBER & CONNECTIVITY POSITION
   - What is the fiber connectivity at their site(s)? Number of diverse fiber paths, proximity to internet exchanges, subsea cable access
   - Is connectivity a constraint or an advantage for this operator?

6. ORGANIZATIONAL READINESS — LOCAL & INTERNATIONAL
   - How large is their Norwegian team? Who leads it?
   - Do they have in-house project management / construction management capability in Norway?
   - Which external advisors / consultants are they already working with?
   - What is their track record of building data centers? (First build? Experienced multi-site operator?)
   - INTERNATIONAL ORGANIZATION: What does their global/regional organization look like?
     a. Where is their DC development HQ? (US, UK, Dublin, Singapore, Stockholm?)
     b. How is their construction/development function organized globally? (Central team that deploys to regions? Regional autonomy? Matrix?)
     c. Who makes the decision to engage a local advisor — the Norwegian team or the global/regional HQ?
     d. What global delivery standards, templates, and processes do they impose on local builds?
     e. What international consultants/contractors do they bring with them? (Mitchell McDermott, Hill International, Turner & Townsend, Linesight, Jacobs, AECOM?)
     f. How does their international organization create friction with Norwegian execution realities? (Global standards vs. local codes, international contract templates vs. NS frameworks, global procurement vs. Norwegian contractor market)
     g. Where does the local team have autonomy vs. where must they follow the global playbook?

OPERATORS TO PROFILE (research each — if an operator has no credible Norwegian activity, note that and skip):

**Hyperscalers building in Norway:**
- Google (Gromstul/Skien — confirmed, 240 MW Phase 1, €600M invested)
- Microsoft / Azure (Norwegian plans — confirmed? Rumored? What's known?)
- Meta (Norwegian plans — any evidence?)
- Amazon / AWS (Norwegian plans — any evidence?)
- Apple (Norwegian plans — any evidence?)
- TikTok / Bytedance (Green Mountain Hamar — what's the current status and expansion plans?)
- Oracle (Norwegian plans — any evidence?)

**Colocation / Wholesale Providers:**
- Bulk Infrastructure (N01 Støleheia — what's the full campus roadmap? Additional sites?)
- Green Mountain (Rjukan, Ytre Enebakk, Hamar — multi-site program status)
- Stack Infrastructure (formerly DigiPlex) (Norwegian portfolio and expansion plans)
- Lefdal Mine Data Center (current status, expansion potential, ownership)

**Sovereign / Enterprise Cloud:**
- Evroc (Swedish HQ but Nordic strategy — any Norwegian sites planned?)
- Telenor (data hall/Tier-3 projects — is this expanding or one-off?)

**Utility / Energy-Company Backed:**
- Any Norwegian energy companies (Statkraft, Hafslund, Lyse, BKK, etc.) announced DC development or "power-to-data" strategies? Research evidence.

**Capital-Led / Developer-Backed ("Finansgutta"):**
- Odin Green DC / Colonor (Kilemoen — status, funding, timeline)
- Any PE funds or infrastructure investors with announced Norwegian DC investments?
- Any SPVs or development companies that have secured Statnett grid reservations?

**Real-Estate / Industrial Park Pivots:**
- Mo Industripark / Arctic Circle Data Center (status, expansion)
- Any industrial parks or real-estate developers with DC development plans?

**AI/HPC Specialists:**
- Any dedicated AI/HPC operators planning Norwegian facilities? (Applied Digital, CoreWeave, Lambda, Cerebras — any Norwegian activity?)

**Other / Emerging:**
- Any other operators on Statnett's grid reservation list that haven't been covered above?
- Any operators announced via NVE concession applications?

EVIDENCE REQUIREMENT: Do not make anything up. Every finding, claim, or data point must be backed by a direct quote from a credible source, with a direct link (URL) to that source. If you cannot find evidence for a claim, state that explicitly — "no public evidence found" is a valid and important finding. The absence of public information about an operator's Norwegian plans IS data.
```

**✅ Prompt 5A.2: Operator Strategy → Execution Model → Consulting Needs**

```
Now take the strategic position data from the previous prompt and analyze what it means for each operator's execution approach and consulting needs.

For EACH operator profiled:

1. CORPORATE STRATEGY IN NORWAY
   - What is this operator trying to achieve in Norway specifically? (Market entry? Capacity expansion? Cost optimization? AI infrastructure? Data sovereignty compliance?)
   - What is their timeline pressure? (GP fund deployment deadline? GPU delivery schedule? Tenant commitment date? Public announcement to deliver on?)
   - How does Norway fit in their broader portfolio? (Only market? One of several Nordic sites? Part of a European rollout?)

2. EXECUTION MODEL
   - How are they building? (Self-perform? EPCM? Turnkey/EPC? Design-build? Hybrid?)
   - Who is their design consultant? (International DC specialist? Local engineering firm? In-house?)
   - Who is their PM/advisory partner? (In-house? International firm like Mitchell McDermott or Hill? Local firm? Nobody yet?)
   - What contract model are they using with contractors? (NS 8405? NS 8407? FIDIC? Samspill? Do they even know about NS standards?)
   - How does their execution model create specific gaps that Metier could fill?

3. WHERE ARE THEY IN THE LIFECYCLE RIGHT NOW?
   - Map each operator to the project lifecycle phases from Prompt 1B
   - Which phase are they currently in? Which phase are they about to enter?
   - What are the critical decisions and risks they face in the NEXT 6-12 months?

4. THEIR SPECIFIC PAIN POINTS (given their strategic position)
   - A fully resourced operator (money + customers + land + power) has different pains than one missing a piece
   - An operator with a grid reservation but no concession for the substation has a specific timeline risk
   - An operator building their first Norwegian facility has localization pains; a multi-site operator has program management pains
   - Map each operator's position to the risk taxonomy from Prompt 1E — which risks are they most exposed to?

5. WHICH OF THE 9 CUSTOMER PERSONAS DO THEY BELONG TO?
   - Assign each operator to their primary persona (1-9)
   - Note where an operator spans multiple personas (e.g., a utility company backing a development SPV is both Persona 4 and Persona 1)

EVIDENCE REQUIREMENT: Do not make anything up. Every finding, claim, or data point must be backed by a direct quote from a credible source, with a direct link (URL) to that source. If you cannot find evidence for a claim, state that explicitly.
```

---

## 🟢 5B. Tailored Value Propositions & Relationship Strategy

**Run after 5A.** Converts operator intelligence into specific sales strategy per operator.

**✅ Prompt 5B.1: Tailored Metier + Norconsult Value Proposition per Operator**

```
Using the operator intelligence from the previous prompts, design a TAILORED value proposition for Metier + Norconsult for each significant operator.

This is NOT the generic persona-level positioning from 1C.2 — this is company-specific. For EACH operator:

1. THE HOOK — What is the single most compelling thing we can say to THIS operator that would get us a meeting? Based on their specific strategic position, current phase, and pain points.
   - For an operator struggling with grid connection execution: lead with Norconsult's NVE concession and substation EPCM track record
   - For an operator entering Norway for the first time: lead with Norwegian execution risk awareness (the 1G "what you don't know you don't know" narrative)
   - For an operator scaling to multi-site: lead with program governance and contractor market management (3E)
   - For an operator in pre-FID: lead with the rush-to-FID risk and the Norwegian Execution Readiness Assessment (1D)

2. THE VALUE PROPOSITION — What specific combination of Metier + Norconsult services addresses THIS operator's needs? Not our full catalog — the 3-4 services most relevant to where they are right now.

3. THE ENTRY POINT — What is the realistic first engagement?
   - What would we propose as a first piece of work?
   - What scope, duration, team composition, and approximate fee?
   - What deliverable does the operator get that solves an immediate problem?
   - How does this first engagement position us for follow-on work?

4. THE RELATIONSHIP MAP
   - Who is our existing contact (if any) at this operator? Through Metier or Norconsult?
   - Who is the decision-maker we need to reach?
   - What is the path from current contact to decision-maker?
   - What external referrals or introductions could help? (Other clients, Norconsult contacts, industry events)

5. THE COMPETITIVE SITUATION
   - Who else is advising this operator or likely pitching to them?
   - What is our competitive angle against the incumbent or likely competitor?
   - Where do we win and where do we need to partner or concede?

6. OPPORTUNITY SIZING
   - What is the estimated total consulting/advisory spend for this operator over the next 3 years in Norway?
   - What is Metier + Norconsult's realistic addressable share of that spend?
   - What is the estimated revenue opportunity (NOK) — low / base / high scenario?

For operators where we have EXISTING relationships (Bulk, Green Mountain, Google, Stack/Digiplex, Lefdal Mine, Telenor, TikTok/Bytedance via Norconsult), note the relationship status and how to expand from current scope.

For operators where we have NO relationship, design the cold-start approach.

EVIDENCE REQUIREMENT: Do not make anything up. Every finding, claim, or data point must be backed by a direct quote from a credible source, with a direct link (URL) to that source. Where you estimate opportunity sizes, state your assumptions explicitly and flag them as estimates.
```

**✅ Prompt 5B.2: Operator Priority Matrix & Account Plan**

```
Now synthesize the operator profiles into a priority matrix and account plan.

1. PRIORITY MATRIX
   Plot each operator on a 2x2 matrix:
   - X-axis: ATTRACTIVENESS (total opportunity size × growth trajectory × strategic reference value × margin potential)
   - Y-axis: ACCESSIBILITY (existing relationship strength × current phase match to our capabilities × competitive intensity × speed to first engagement)

   Quadrant 1 (High Attractiveness, High Accessibility): PRIORITY ACCOUNTS — pursue immediately
   Quadrant 2 (High Attractiveness, Low Accessibility): STRATEGIC TARGETS — invest in relationship building
   Quadrant 3 (Low Attractiveness, High Accessibility): OPPORTUNISTIC — serve if they come to us
   Quadrant 4 (Low Attractiveness, Low Accessibility): DEPRIORITIZE — not worth the effort now

2. TOP 5 PRIORITY ACCOUNTS
   For the top 5 operators in Quadrant 1, create a one-page account plan:
   - Current relationship status
   - Target decision-maker
   - Hook and value proposition
   - Proposed first engagement
   - 90-day action plan to advance the relationship
   - Revenue target (Year 1)
   - Success metrics

3. STRATEGIC TARGETS
   For operators in Quadrant 2, define the investment strategy:
   - What needs to change to make them accessible? (Capability building, partnership, reference, event presence)
   - What is the realistic timeline to first engagement?
   - What "air cover" activities (thought leadership, conference presence, referral relationships) should we run?

4. TOTAL ADDRESSABLE OPPORTUNITY
   Sum the opportunity sizing across all profiled operators:
   - Total Norwegian DC consulting market estimate (NOK/year)
   - Metier + Norconsult's realistic addressable market
   - Revenue projection: Year 1 / Year 2 / Year 3 (low / base / high scenarios)
   - Key assumptions and risks to the projection

EVIDENCE REQUIREMENT: Do not make anything up. Every finding must be backed by evidence. For market sizing and revenue estimates, state all assumptions explicitly. Use ranges rather than false precision.
```
