# My Bali — Social, Trip and Evidence-Linked Experience Flows

**Status:** System-design foundation derived from founder direction (2026-11-02). This is a conceptual data and workflow model, not a final technical architecture or implementation specification.

## 1. Core separation

Keep these entities separate even when they are presented together in the interface:

- **Media asset:** uploaded photo or video, with ownership, rights declaration, processing state, storage reference, and moderation state.
- **Social post:** user-authored caption and media, post type, audience, publication state, and edit history.
- **Trip Plan:** a plan for a future or hypothetical trip, including intended dates, itinerary items, accommodation ideas, interests, notes, and estimated budget.
- **Trip Experience:** a record or story about something that has already happened. It may be user-authored, provider-confirmed, or linked to eligible system evidence.
- **Transaction / booking:** the commercial record with its own status and source of truth.
- **Experience evidence:** references to relevant system events or provider confirmations. This must not be confused with user-generated text.
- **Story / Status:** a temporary content publication with its own audience and expiry/archive rules; it is not automatically a Feed post.

A single media asset may be reused in multiple permitted surfaces, but permissions, visibility, deletion, and moderation must remain consistent and traceable.

## 2. Suggested publication types

1. **General post** — ordinary permitted photo/video and caption; no Trip relation required.
2. **Trip Plan post** — a plan shared from the Trip area; clearly marked as planned, not completed.
3. **Experience Post** — a story about an actual experience, optionally linked to evidence.
4. **Business post** — content published by an approved provider profile and linked to its business/product/service page.
5. **Story / Status** — temporary publication; may reference a general post, Trip Plan, or Experience Post without duplicating or changing the source record.

These are logical content types. Final labels and UI composition remain subject to founder review.

## 3. Trip Plan lifecycle

Possible states:

- Draft / private.
- Shared with selected audience.
- Publicly shared.
- In progress (only if the owner chooses to mark the trip as underway).
- Completed by the owner (self-declared; not automatically verified).
- Archived or deleted according to retention rules.

Trip Plan items may be places, accommodation, activities, restaurants, transport, dates, route order, estimated cost, and notes. A plan may be copied or adapted by another user only as a new plan, not by altering the original owner's record.

A Trip Plan is not a booking, provider confirmation, payment, attendance record, or proof of future intent. Estimated prices must be labeled as estimates with source/freshness context where available.

## 4. Evidence-linked Experience Post lifecycle

A possible flow:

1. A qualifying transaction or provider-confirmed activity reaches an eligible state.
2. My Bali offers the user an optional **Share experience** action.
3. The user chooses media, caption, audience, and whether to show the linked provider/activity.
4. The system creates a post that references the underlying activity record.
5. System-sourced facts are displayed separately from user-authored content.
6. If a source fact is disputed, an authorized correction workflow creates an auditable change; it does not silently overwrite the historical event.
7. The user can hide/unpublish the social post without deleting a legally or operationally required transaction record.

Evidence labels must describe exactly what was verified. Examples: **Order completed in My Bali**, **Booking completed**, or **Provider confirmed visit**. Do not use **verified visit** if only payment was recorded. GPS alone is not sufficient proof.

## 5. Editing and audit rules

- Users may edit their own ordinary caption/media within policy; meaningful changes may retain edit history.
- Users cannot directly alter system-generated provider, booking, payment, time, fulfillment, or evidence fields.
- Authorized staff/provider corrections require role-based access, a reason, timestamp, actor identity, and an audit record.
- Disputes must allow the affected user/provider to submit context and supporting evidence.
- The public post should show only the minimum facts necessary; internal transaction IDs and sensitive details stay private.
- Removing a public post does not automatically erase the underlying transaction, dispute, or legally required audit record. Retention and deletion rules must be defined transparently.

## 6. Copyright, licensing and content moderation

A social-media-like workflow does not make third-party content free to reuse. Product safeguards should include:

- A clear upload declaration that the user created the content or has the necessary rights/permission.
- No assumption that credit, cropping, filters, short duration, or non-commercial use automatically grants permission.
- A licensed or platform-cleared music/media catalogue if users can add music; otherwise limit audio choices to content users have rights to use.
- A report flow for copyright owners/rightsholders and a documented review/takedown process.
- A way for uploaders to appeal or submit evidence of authorization.
- Proportionate repeat-infringer rules and account enforcement.
- Moderation for other policy violations, privacy, harassment, impersonation, and unsafe content.

Automated matching may assist review later, but it should not be treated as a perfect legal decision-maker. My Bali cannot promise zero copyright complaints. Applicable Indonesian law and any other relevant jurisdiction must be reviewed before launch.

## 7. Privacy and audience controls

Visibility should be explicit and separate for profile, individual post, Trip Plan, saved places/interests, and Story/Status. Possible audience levels are private, selected audience/followers, and public. Defaults, age restrictions, location precision, retention, and deletion behavior remain open policy decisions.

Do not publish private itinerary details, exact accommodation room information, private addresses, payment credentials, or sensitive transaction data by default. Sharing a plan must be a deliberate action.

## 8. Integration boundaries

The social layer may link to provider pages, product listings, menus, offers, transport options, bookings, and transaction records. A social post must not itself be treated as an order or booking. Each commercial workflow retains its own confirmation, payment, cancellation, fulfillment, and dispute states.

## 9. Decisions still required

This document does not decide the final feed algorithm, story duration, default privacy, exact evidence thresholds, copyright response deadlines, music licensing vendor, backend, database, media storage provider, or final app navigation. These require product, legal, operational, and technical design.
