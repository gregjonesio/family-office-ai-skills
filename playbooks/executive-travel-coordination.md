# Playbook: Executive Travel Coordination

How a family office plans, briefs, and tracks principal and executive travel — maintaining current traveler profiles and documents, coordinating security and ground logistics, managing private aviation, and consolidating everything into one trip sheet — so a trip runs smoothly and the principal arrives prepared. Read-only, human-in-the-loop, non-advisory: AI organizes and drafts; people book, confirm, and decide.

> **Fictionalized and illustrative.** This is a generalized operating pattern. It does not describe any actual family office, principal, itinerary, or travel arrangement. Nothing here books, confirms, or pays for travel, and none of it is legal, tax, security, or insurance advice. Every AI output described is an unverified draft requiring human review.

---

## Objective

Deliver well-organized, low-risk travel: a single authoritative itinerary, valid documents in hand, security and ground logistics arranged, meetings briefed, and contingencies anticipated — so the principal's time on the ground is productive and nothing logistical or document-related is left to chance.

## Operating Problem

Executive travel concentrates many small, time-sensitive details — flights or private lift, ground transport, lodging, meeting logistics, documents, time zones, and contingencies — where a single dropped item derails a day or, worse, strands the principal. Three details cause most of the pain. **Documents**: passports must usually be valid six months beyond travel, and visas can take weeks, so an expired document discovered at the airport is a self-inflicted failure. **Propagation**: an itinerary that changes but doesn't reach the driver, the host, or security creates a missed connection or an exposure. **Security**: an over-shared schedule is itself a risk for a high-profile principal. A lean office assembles each trip by hand, re-keying the same details across an itinerary, a brief, and a calendar; the discipline a mature office imposes is a current traveler profile, a single source-of-truth trip sheet, and a security-conscious distribution.

## Typical Trigger

A confirmed or proposed trip — a principal's meeting commitment, a family event, or a recurring travel pattern — that needs to be turned into a planned, briefed, and contingency-ready itinerary.

## Frequency

On demand as trips arise, often clustered around recurring commitments and seasons; profile and document maintenance runs continuously in the background.

## Primary Stakeholders

- **Executive assistant (owner)** — plans the trip, books arrangements, and maintains the single source-of-truth itinerary.
- **Principal / executive traveler** — the subject; makes the final calls on schedule and preferences.
- **Chief of staff** — aligns the trip's meetings and priorities.
- **Security / executive protection** — advance work, route and venue vetting, and check-in protocols where the principal's profile warrants it.
- **Flight department or charter provider** — crew, aircraft, permits, and FBO coordination for private lift.
- **Ground providers and local hosts / fixers** — drivers and on-the-ground contacts named on the trip sheet.

## Required Inputs

- Trip purpose, dates, and destinations
- The traveler profile: document status (passport expiry, visas, trusted-traveler enrollments), seat and lodging preferences, dietary and medical needs, loyalty programs
- Meeting commitments and desired outcomes on the ground
- Documents the trip requires — itineraries, confirmations, visas, and any travel documents (provided manually)
- For private aviation: aircraft availability, crew duty-time constraints, FBO and catering, and international permit or customs requirements
- Prior-trip notes for recurring destinations

Travel documents, identifiers, and detailed schedules are sensitive; provide them manually, keep them out of unapproved tools, and limit distribution.

## AI-Assisted Activities

- Assemble a structured per-meeting brief for the trip's commitments with [Meeting Prep Pack](../skills/meeting-prep-pack/) — attendees, agenda, and desired outcomes.
- Produce plain-English reads of itineraries, confirmations, and travel documents with [Document Digest](../skills/document-digest/), surfacing key times, addresses, gate and FBO details, and document requirements.
- Surface the trip, its dates, document-expiry checks, and open logistics in the [Principal Weekly Brief](../skills/principal-weekly-brief/).
- Capture post-trip follow-ups with [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/).

AI organizes, drafts, and reminds. It does not book, confirm, pay for, or change any arrangement, and it renders no security or travel-risk judgment.

## Human Responsibilities

- Maintain the traveler profile and proactively track document expiries and visa lead times — well ahead, not at booking.
- Book and confirm all arrangements directly with providers.
- Verify every time, address, gate, and document against the actual confirmation — never rely on a remembered or AI-restated detail.
- Propagate every itinerary change to the driver, host, security, and flight department.
- Make the calls on routing and contingencies, and handle any security, medical, or travel-risk judgment with qualified providers.

## Review Gates

1. **Document gate** — a person confirms passports, visas, and entry requirements are valid and current — applying the six-month passport rule and visa lead times — well before departure, not at the airport.
2. **Plan gate (single source of truth)** — the owner reconciles the trip sheet against the actual bookings and confirmations so one authoritative itinerary governs; superseded versions are retired.
3. **Propagation gate** — a person confirms the current itinerary has reached every party who acts on it — driver, host, security, and crew.
4. **Brief-and-discretion gate** — the owner confirms meeting briefs are accurate and the principal's preferences reflected, and that schedule detail is distributed only to those who need it.

## Outputs

- A consolidated trip sheet and itinerary (draft)
- Per-meeting prep for on-the-ground commitments (draft)
- Plain-English digests of confirmations and documents (draft)
- A post-trip follow-up list (draft)

## Risks

- **Dropped or wrong detail** — a misremembered address or time derails a day; every detail is verified against the confirmation.
- **Stale information** — itineraries change; the plan is checked against current bookings, not a prior version.
- **Confidentiality and physical security** — travel patterns and documents are sensitive; use approved environments and limit distribution. See [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md) and [threat-model.md](../docs/threat-model.md).
- **Authority boundary** — the AI never books, confirms, or pays; those remain human actions with providers.

## Common Failure Points

- **Expired document at the airport.** A passport inside the six-month window or a missing visa surfaces too late to fix. *Control:* proactive document-expiry tracking on the traveler profile and the document gate well ahead of departure.
- **Itinerary change not propagated.** The schedule shifts but the driver, host, or crew works from an old version. *Control:* a single source-of-truth trip sheet and a propagation gate confirming the current version reached everyone.
- **Over-shared schedule.** Detailed movements distributed too widely create a security exposure for a high-profile principal. *Control:* need-to-know distribution and the discretion gate.
- **No contingency.** A delay, cancellation, or medical issue with no fallback strands the principal. *Control:* pre-identified alternates and ground contacts on the trip sheet, and a check-in protocol where security warrants.
- **Private-lift surprises.** Crew duty-time limits, an international permit, or a customs/APIS requirement grounds the aircraft. *Control:* the flight department confirms crew legality, permits, and FBO arrangements as part of planning, not at the ramp.
- **Stale traveler profile.** Preferences, loyalty numbers, or medical needs are out of date and re-gathered each trip. *Control:* a maintained profile updated as things change.

## Metrics

- Trips with a complete, verified trip sheet and valid documents before departure (target: every trip)
- Review-gate completion rate (target: 100%)
- Document expiries caught proactively vs. at booking or travel
- Logistical exceptions on the ground (target: trend toward zero)
- Assembly time saved per trip (directional)

Figures are directional, not audited. See [measurement-framework.md](../docs/measurement-framework.md).

## Related Skills

- [Meeting Prep Pack](../skills/meeting-prep-pack/)
- [Document Digest](../skills/document-digest/)
- [Principal Weekly Brief](../skills/principal-weekly-brief/)
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)

## Related Blueprints

- [Weekly Principal Briefing System](../blueprints/weekly-principal-briefing-system.md) — where the trip surfaces in the weekly view.

## Related Case Studies

- [Weekly Principal Brief](../case-studies/weekly-principal-brief.md)

## Related Governance Documents

- [Privacy and Confidentiality](../docs/privacy-and-confidentiality.md)
- [Threat Model](../docs/threat-model.md)
- [Connectors and Context Access](../docs/connectors-and-context.md)
- [Measurement Framework](../docs/measurement-framework.md)

## Evolution Path

1. **Ad hoc** — each trip assembled from scratch, details re-keyed across documents, document status checked at booking.
2. **Profiled** — a maintained traveler profile with proactive document-expiry tracking and standing preferences removes repeated rework and the airport surprise. This discipline stands independent of AI.
3. **Source-of-truth trip sheet** — one authoritative itinerary with ground contacts, security protocols, and contingencies, distributed on a need-to-know basis.
4. **AI-assisted** — the prep pack and document digest assemble briefs and surface key details; approved, read-only retrieval of calendar commitments can seed the itinerary — a governed data-access change, not new authority.

No stage lets the AI book, confirm, pay for, or change travel, or render security judgment. Those stay human.

---

*This playbook is an illustrative operating pattern, not security, travel, insurance, legal, or tax advice, and not a live integration. It books, confirms, and pays for nothing. Every output described is an unverified draft requiring human review.*
