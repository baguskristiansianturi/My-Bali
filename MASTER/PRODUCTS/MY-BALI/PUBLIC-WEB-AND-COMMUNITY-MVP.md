# My Bali — Public Web, Account and Community MVP

**Status:** Prototype scope approved for iterative founder testing. This is not a production authentication, publishing, or moderation specification.

## 1. One product, two access channels
My Bali is one platform available through a public website and, later, installable/native mobile applications. Public web pages should remain usable without an app download. A shared backend and identity system should eventually serve web and mobile clients.

## 2. Guest-first public browsing
Unauthenticated visitors can:
- Open the public homepage and browse categories.
- Search and view publicly indexed product, provider, and destination pages.
- Read public descriptions, location, prices, photos, and relevant policies when those data are available.
- Open shared links from search engines without being forced to install an app.

Authentication should be requested at a meaningful action boundary (for example, creating a post, saving a favorite, following a provider, submitting a booking, or writing an eligible review), not merely because a visitor opened a detail page. Public pages should have crawlable URLs, distinct titles/descriptions, canonical URLs, structured data where appropriate, and share previews. Do not expose private profile or transaction data to search engines.

## 3. Website and mobile application
- Responsive web is the public discovery and account channel for desktop and mobile browsers.
- Native mobile apps may later offer installation and device-native capabilities.
- PWA installation can be evaluated as an intermediate option; it is not a substitute for all native functionality.
- Both clients should eventually use the same backend, account identity, provider data, and transaction records.

## 4. Initial user account prototype
The first test flow covers profile creation, dashboard entry, and basic profile editing. The founder's requested basic profile fields are display name, age, country, and optional area. Age collection should be reviewed for necessity, minimum-age policy, privacy, and legal requirements before production. Location should be optional and user-controlled; allow manual area selection as well as consent-based device location in a later implementation.

## 5. Initial social publishing prototype
The first community iteration allows a signed-in demo profile to:
- Write a text post.
- Attach one image.
- Preview the image before publishing.
- See their own posts in a personal feed.
- Delete their own post.

Deletion in the prototype removes the local browser copy. Production deletion must define server-side deletion, backups/retention, moderation evidence, abuse reports, and legal retention exceptions. The initial prototype should not invent community activity, likes, comments, followers, or reviews.

## 6. Prototype versus production
The GitHub Pages prototype uses browser-local storage for the demo profile and posts. This is device/browser-specific and is not secure authentication, cloud storage, multi-user synchronization, or public social publishing. Do not enter real passwords, sensitive documents, or private personal data. Uploaded photos are compressed in the browser and remain local to that browser.

Production requires a backend, secure authentication/session management, authorization, database, object storage, upload validation and malware/content checks, moderation/reporting, rate limits, privacy controls, audit logs, backups, and account/data deletion workflows.

## 7. Retail category boundaries
The initial curated shopping direction is limited to:
- Bali souvenirs and crafts, including eligible locally made products such as carvings, ornaments, and gifts.
- Fashion, including Bali-made and international brands, provided the seller is a genuine, verifiable business with an actual business presence in Bali.

Not in the initial shopping marketplace:
- Electronics.
- Vehicle sales.
- Land/property sales.
- Open classifieds or unrestricted peer-to-peer listings.

An independent classified-ad format may be evaluated separately in the future. It is not part of the initial marketplace and must not dilute provider verification or category quality.

## 8. Geographic directory
Providers and destination managers submit their own actual address, coordinates, service area, and region. The system groups listings by verified/declared administrative area and may calculate distance from a user's chosen area or consent-based device location. Manual area selection must remain available. Never infer a business's exact location from a name or show precise user location without consent.

## 9. Iterative founder review
Build small, testable increments. Each iteration should:
1. Have a clear user journey and acceptance criteria.
2. Preserve existing approved pages and responsive behavior.
3. Be tested on a mobile browser and desktop viewport.
4. Record limitations honestly.
5. Include a commit reference and deployed Pages URL after successful deployment.

## 10. Open production decisions
- Backend and hosting architecture.
- Secure login methods, account recovery, and cross-device identity.
- Minimum age, age collection necessity, privacy and retention.
- Public feed policy, post visibility, and whether user posts are public by default.
- Image limits, storage, deletion, reporting, moderation, appeals, and prohibited content.
- SEO indexation policy for product/provider/destination pages.
- PWA versus native app timing.
