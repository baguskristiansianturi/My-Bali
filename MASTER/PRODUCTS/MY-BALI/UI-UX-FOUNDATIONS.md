# My Bali — UI/UX and Service Experience Foundations

**Status:** Initial design-planning foundation derived from founder discussions. Not a visual specification or approved screen design.  
**Product principle:** Local-first, Bali-focused, trusted ecosystem.

## 1. Experience principles
1. Design first for people who live in Bali and use services repeatedly.
2. Make trust visible and understandable; do not rely on vague badges.
3. Show who actually provides and fulfills a service.
4. Show accurate location, service area, price, availability, and update context.
5. Keep the experience simple for residents while supporting Indonesian and international users.
6. Make service-specific workflows fit their real-world operations; do not force every category into one generic checkout.
7. Prefer controlled, high-quality growth over uncontrolled listing volume.
8. Never fabricate reviews, activity, availability, popularity, verification, or transaction proof.

## 2. One platform, service-family entry points
Working service names:
- My Bali Food
- My Bali Shopping
- My Bali Kurir
- My Bali Taxi
- My Bali Spa
- My Bali Trip
- My Bali Stay
- My Bali Rental
- My Bali Activity
- My Bali Event
- My Bali Service
- My Bali Lifestyle
- My Bali Property (later evaluation)

These are entry points inside one app, not separate accounts or necessarily separate apps. Shared navigation and identity should coexist with category-specific forms and workflows.

## 3. Local-first home and navigation
The home experience should prioritize useful Bali-local services and nearby/available options, not only tourist attractions. Potential primary entry points include Food, Shopping, Kurir, Taxi, Spa, and Discover. Trip, Stay, Activity, and attractions remain discoverable without dominating the resident-first experience.

Location permission should be requested contextually and explained. Users must be able to search by area or enter locations manually. Never imply precise location access if permission is unavailable.

## 4. Provider discovery cards and profile pages
A provider card should help users quickly understand:
- Provider name and category.
- Verification state and what it means.
- Real location or service area.
- Price or price range, including whether it is provider-listed or estimated.
- Availability/opening information and last update where relevant.
- Relevant quality indicators and review count only when genuine.
- Whether fulfillment is direct, vendor-managed, or through an authorized partner.

A full provider page may show business identity, operator/authority, location/map, products/services, price, hours, availability, media, update history, offers, policies, and in-platform contact/booking actions.

Do not expose a provider's personal phone number as a public directory field by default. Keep communication in My Bali where the transaction or safety workflow requires it.

## 5. Provider onboarding and trust states
The onboarding UI should explain each step and why it is required. Possible states:
- Draft / registration incomplete.
- Submitted / under review.
- Verified / approved for specified categories.
- Limited / additional evidence required or some features restricted.
- Suspended / temporarily unavailable pending review.
- Rejected / not approved, with reason and appeal route where appropriate.

Verification labels must state what was checked (for example identity, authority, or location) rather than implying a universal guarantee of quality. Verification can expire or require re-checks.

The system should support document capture, business/location details, category-specific evidence, real photos, service areas, and site-review scheduling where appropriate. Sensitive documents must not be displayed publicly.

## 6. Transport UX: independent driver and vendor-managed operator
Users must be able to distinguish:
- Independent/freelance driver.
- Vendor-managed driver.
- Established transport operator/company.

Show the relevant operator, driver identity, actual vehicle, plate/vehicle match status, service class, estimated pickup time, estimated fare/offer, and applicable protection/limitations. Do not present a freelance provider as equivalent to a vendor-managed service.

Vendor profiles should show their declared service territory, service types, verification state, and operational responsibility. Where multiple vendors cover an area, users should see eligible options ranked by relevance, pickup time, service suitability, quality, and price. Do not make ranking a hidden pay-to-win system.

Driver substitutions and vehicle substitutions require a controlled, visible update and user approval where applicable.

## 7. Courier request flow
Potential user flow:
1. Select pickup and destination.
2. Describe item, size/category, urgency, and any handling needs.
3. Add optional photo and declared value where required.
4. Enter an offered price or request/counteroffer according to the chosen model.
5. Review independent versus vendor-managed options and restrictions.
6. Confirm driver/operator and vehicle.
7. Track pickup, transit, and delivery status.
8. Recipient confirms handover with code or equivalent proof.
9. Review the completed delivery and raise an issue if necessary.

Sensitive/high-value goods need category restrictions, enhanced verification, handling instructions, and actual insurance terms if offered. Do not imply coverage where none exists.

## 8. Food, shopping, and local commerce UX
Food should support menu/variants, availability, pickup, delivery, order status, and merchant confirmation.

Shopping should prioritize real Bali-based stores and eligible new goods. Store location and product origin must be clear. The platform should not resemble an unrestricted second-hand classifieds marketplace. Product categories that are undecided or high-risk should remain unavailable until policy approval.

For Bali-local eligible orders, show instant/same-day options only when real capacity exists. For orders after a buyer leaves Bali, show actual shipping origin, service, and estimated delivery window.

## 9. Offers, reservations, QR, and transaction status
Support walk-in businesses as well as reservation businesses. A time-limited offer may use a claim-and-redeem flow:
- Viewed.
- Claimed.
- Scheduled / reservation requested.
- Confirmed (where provider confirmation is required).
- Checked in.
- Redeemed.
- Payment completed.
- Fulfilled / closed.
- Expired, cancelled, refunded, or disputed as applicable.

A claim is not a completed transaction. QR credentials must be secure, time/condition-bound where needed, resistant to duplicate redemption, and usable under defined connectivity-failure procedures. Deposit requirements should be configurable by offer and risk, not universally required.

## 10. Pricing display
Always distinguish:
- Provider-listed price.
- System-generated estimate.
- Provider-confirmed quote.
- Final payable amount.

Show what is included and excluded: taxes, fees, delivery, waiting time, surcharges, optional upgrades, and cancellation conditions. Provider updates should carry a timestamp or clear freshness indicator.

The intended pricing principle is equal provider pricing for local and foreign users except where an official/legal rule requires a difference. Any exception must be explained and grounded.

## 11. Communication and transaction integrity
Use in-platform chat or structured contact for bookings, delivery coordination, and service questions. Detect likely attempts to move protected transactions off-platform, including phone numbers or external payment instructions, but allow legitimate operational, safety, and emergency communication.

Warnings should explain the risk and offer a safe in-app alternative. Avoid blunt blocking that prevents a recipient from coordinating a delivery or a customer from resolving a genuine issue.

## 12. Trust, reviews, reputation, and levels
Trust indicators should be evidence-based and explainable. Distinguish provider verification from service quality and from transaction protection.

Reviews should be tied to eligible experiences where possible, with a fair response and dispute process. User and provider reputation should consider context, confirmed events, and repeated behavior—not a single complaint or raw spending alone.

Levels and achievements may support identity and social sharing, but public visibility should be user-controlled. Internal safety signals and private dispute records must never be exposed as public status.

## 13. Error, empty, and exception states
Design explicit states for:
- No provider available in the selected area.
- No driver currently available.
- Provider not yet verified.
- Price or availability needs confirmation.
- Same-day service unavailable.
- Booking awaiting provider confirmation.
- Payment pending or failed.
- QR invalid, expired, or already redeemed.
- Delivery handover failed.
- Cancellation, refund, complaint, or appeal in progress.

Offer safe alternatives and explain what the user can do next. Never display invented availability or pretend a request was accepted when it was not.

## 14. Accessibility, language, and localization
Plan for Indonesian and English from the start, with a path to additional languages if justified. Currency display should be clear and conversion estimates must not be confused with the provider's actual payable currency. Use readable typography, clear contrast, accessible touch targets, plain language, and mobile-first responsive layouts.

## 15. Open UI/UX decisions
- Final primary navigation and home ordering.
- User and provider profile privacy settings.
- Verification labels and evidence details.
- Driver/vendor comparison and matching explanation.
- Price offer/counteroffer interface.
- In-person payment and QR redemption.
- Chat moderation and emergency contact handling.
- Product categories and prohibited listings.
- Accessibility, language, and currency scope.
- Exact level, achievement, and reputation presentation.

## 16. Social-first home and navigation

**Founder direction captured (2026-11-02):** The primary My Bali experience is social-media-first. Do not design the homepage as a directory, service dashboard, or travel booking catalogue. The social feed is the central home experience; the Bali business and service ecosystem is discoverable through and connected to it.

### Main experience areas

- **Feed / Home:** a mixed photo-and-video feed. Content may include general posts, Trip content, verified business updates, destination content, food, local life, and clearly labeled promotions. General posts do not need to be Trip-related.
- **Trip:** a dedicated travel area. **Bali Plan** is a sub-area for intended travel plans and itineraries; **Trip Experience** is for experiences that have happened. Do not merge planned and completed states.
- **Stories / Status:** temporary posts, separate from the persistent feed. A user can share a Trip Plan or ordinary update to Stories without automatically publishing it to the main feed. Cross-posting is an explicit user choice.
- **Explore:** discovery/search for people, providers, products, destinations, services, and public Trip Plans.
- **Shopping and service flows:** dedicated catalog and task-specific journeys, using patterns appropriate to the category rather than copying another platform's exact visual design.

Users should be able to browse public content and details as guests. Ask for login only when the user takes an account-bound action; after login, preserve the intended action and return the user to it. Final navigation labels, order, and desktop layout remain open until prototype review.

### Trip planning and visibility

A Bali Plan may contain intended dates, places, accommodation, activities, restaurants, route order, notes, and estimated budget. The owner chooses whether the whole plan is private, followers-only, or public, and may control visibility of selected interests/saved places separately. A plan can be shared to Feed, Stories/Status, or a chosen audience. Sharing a plan never implies a confirmed reservation or completed visit.

### Evidence-linked Experience Post

When a supported My Bali transaction or provider-confirmed activity reaches an eligible state, offer the user an option to publish an Experience Post. Keep system-sourced facts visually distinct from the user's caption and media. The user may choose whether to publish; publication must not expose payment credentials, sensitive receipt details, private addresses, or unnecessary transaction identifiers.

System-sourced facts must not be silently editable. If a source record is wrong, provide a correction/dispute route and preserve the audit history. User-authored caption/media may have normal edit controls, with edit history where needed by policy. Never label a payment alone as proof of a physical visit.

### Design references, not copies

Use familiar interaction patterns as references: Instagram for social feed and Stories behavior, Zalora for fashion shopping discovery, Traveloka for transport search/selection, and Shopee for guest browsing with login at meaningful action boundaries. These are behavioral references only. My Bali must have its own visual identity, content hierarchy, wording, iconography, and original interface design.

