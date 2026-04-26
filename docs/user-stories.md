# User Stories

These stories are written for the rental-only MVP. Each story includes acceptance criteria and a short INVEST check so the scope stays small, testable, and ready for implementation.

## Story 1: Broker login with Google

**User story**

As a broker, I want to log in with my Google account so that I can access my rental listings without needing to remember a separate password.

**Acceptance criteria**

- Broker can start login with Google Sign-In
- Broker can complete Google authentication and log in successfully
- First-time broker is routed to profile setup after successful login
- Returning broker lands on the broker dashboard after successful login
- Failed or cancelled Google authentication shows a clear error state

**INVEST check**

- `Independent`: authentication can be built and tested separately from listing management
- `Negotiable`: Google provider details and session handling can change without changing the story goal
- `Valuable`: it unlocks secure broker-only access
- `Estimable`: the flow is small and clear
- `Small`: covers only login, not full onboarding
- `Testable`: success and failure paths are explicit

## Story 2: Broker profile setup

**User story**

As a broker, I want to create my public profile with name, photo, phone, WhatsApp number, and service area so that renters trust the listings and can contact me.

**Acceptance criteria**

- Broker can add or edit name, profile photo, phone number, WhatsApp number, and service area
- Required fields are validated before save
- Saved profile details appear on the public broker page
- Broker can update profile details later

**INVEST check**

- `Independent`: profile setup does not depend on creating listings
- `Negotiable`: exact profile fields can evolve while keeping the same outcome
- `Valuable`: creates a trustworthy public identity
- `Estimable`: the fields and behaviors are well defined
- `Small`: limited to profile data only
- `Testable`: save, validation, and display states are observable

## Story 3: Create rental listing

**User story**

As a broker, I want to create a rental listing with property details so that renters can understand the property without calling me first.

**Acceptance criteria**

- Broker can create a listing with title, area, society, property type, rent, deposit, brokerage, furnishing, availability, and description
- Property type options include `1 RK`, `1 BHK`, `2 BHK`, `3 BHK`, `4 BHK`, studio, penthouse, room, PG, shop, and office
- Furnishing options include `Unfurnished`, `Semi-furnished`, and `Furnished`
- Required fields must be completed before publish
- New listing is visible in the broker dashboard after save

**INVEST check**

- `Independent`: listing creation can be delivered before media upload or public filters
- `Negotiable`: field ordering and labels can still be refined
- `Valuable`: this is the core inventory-creation action
- `Estimable`: inputs are concrete and bounded
- `Small`: focuses on listing creation only
- `Testable`: required-field, save, and option-list behavior can be verified

## Story 4: Upload listing photos and videos

**User story**

As a broker, I want to upload property photos and videos so that renters can see the actual rental before contacting me.

**Acceptance criteria**

- Broker can upload multiple images to a listing
- Broker can upload at least one video to a listing
- Broker can remove uploaded media before publishing
- Uploaded media is shown in the listing preview after save

**INVEST check**

- `Independent`: media upload extends a listing without changing base listing creation
- `Negotiable`: upload limits and ordering rules can be adjusted later
- `Valuable`: visual proof increases trust and lead quality
- `Estimable`: image/video upload scope is bounded
- `Small`: limited to media attach and remove actions
- `Testable`: upload, display, and remove behavior are observable

## Story 5: Publish and share broker page

**User story**

As a broker, I want a public broker page with a shareable link so that I can send one link on WhatsApp and Facebook groups instead of posting many statuses.

**Acceptance criteria**

- Broker has a public page URL after profile setup
- Active listings appear on the public page
- Broker can copy or share the page link
- Inactive listings do not appear on the public page

**INVEST check**

- `Independent`: public page delivery does not require renter accounts
- `Negotiable`: final URL pattern and sharing UI can change
- `Valuable`: this is the main distribution mechanism for the MVP
- `Estimable`: the page behavior is simple and visible
- `Small`: focuses on public page publishing and sharing
- `Testable`: visibility and share behavior can be verified

## Story 6: Renter filters listings

**User story**

As a renter, I want to filter a broker's listings by area, price, property type, brokerage, and furnishing so that I can quickly find relevant rental options.

**Acceptance criteria**

- Renter can filter listings by area or locality
- Renter can filter listings by price or budget
- Renter can filter listings by property type, including `1 BHK`, `2 BHK`, `3 BHK`, `4 BHK`, and penthouse
- Renter can filter listings by brokerage
- Renter can filter listings by furnishing: `Unfurnished`, `Semi-furnished`, and `Furnished`
- Filtered results update correctly on the public broker page

**INVEST check**

- `Independent`: browsing filters can be implemented after listings exist
- `Negotiable`: filter UI can be chips, dropdowns, or sections
- `Valuable`: it reduces renter effort and broker back-and-forth
- `Estimable`: each filter field maps to known listing data
- `Small`: focused on filtering only, not detailed search ranking
- `Testable`: each filter has a clear expected result set

## Story 7: Renter views listing details

**User story**

As a renter, I want to open a listing detail page so that I can review full property information, photos, videos, and charges before contacting the broker.

**Acceptance criteria**

- Renter can open a listing detail page from the public broker page
- Listing detail page shows title, area, society, property type, rent, deposit, brokerage, furnishing, availability, description, photos, and videos
- Page works without renter login
- Listing detail page has visible call and WhatsApp actions

**INVEST check**

- `Independent`: detail view stands on top of listing data without needing lead capture
- `Negotiable`: layout can evolve without changing the story outcome
- `Valuable`: gives renters enough detail to make contact decisions
- `Estimable`: the fields and media to display are known
- `Small`: limited to viewing one listing
- `Testable`: field presence and link behavior can be checked

## Story 8: Renter contacts broker directly

**User story**

As a renter, I want to call or WhatsApp the broker from a listing so that I can take immediate action on a rental I like.

**Acceptance criteria**

- Listing detail page includes a working `Call Broker` action
- Listing detail page includes a working `WhatsApp Broker` action
- WhatsApp action opens a prefilled message with basic listing context
- Contact actions are visible on mobile without scrolling excessively

**INVEST check**

- `Independent`: direct contact can be delivered without a full lead-management system
- `Negotiable`: prefilled message text can change later
- `Valuable`: this is the conversion point of the MVP
- `Estimable`: the actions are straightforward links or intents
- `Small`: limited to direct contact behavior
- `Testable`: call and WhatsApp actions can be validated

## Story 9: Broker hides inactive listing

**User story**

As a broker, I want to hide an inactive listing so that renters only see currently available rental options.

**Acceptance criteria**

- Broker can mark a listing as inactive from the dashboard
- Inactive listing stays visible in the broker dashboard
- Inactive listing is removed from the public broker page
- Broker can reactivate the listing later

**INVEST check**

- `Independent`: status control is separate from create and edit flows
- `Negotiable`: the UI can be a toggle, menu, or button
- `Valuable`: keeps public inventory current
- `Estimable`: the status behavior is simple
- `Small`: focused on active versus inactive visibility
- `Testable`: dashboard and public-page visibility can be confirmed
