# Phase 1 Build

This document turns the repo planning into a practical Phase 1 execution plan.

## Phase 1 goal

Ship the first complete broker-to-renter loop:

1. broker signs in
2. broker sets up profile
3. broker creates and publishes listings
4. broker shares broker page or individual listing
5. renter opens the public page
6. renter views details and contacts broker

If those six steps work cleanly on mobile, Phase 1 is successful.

## What Phase 1 includes

- Google Sign-In for broker
- first-time routing to profile setup
- broker profile setup
- create rental listing
- upload photos and optional video
- save draft
- broker dashboard
- active/inactive listing control
- public broker page
- public listing detail page
- share broker page link
- share individual listing link
- renter filters
- call broker and WhatsApp broker actions

## What Phase 1 does not include

- renter login
- OTP login
- payments
- CRM
- admin moderation workflows
- map search
- advanced analytics
- draft completeness scoring

## Build principle

Build in the same order the product is experienced.

Do not start with polishing filters or visual details before the broker can publish and share one live listing.

## Recommended build order

### Stage 0: Foundation

This is technical setup work before feature implementation:

- choose app stack
- set up project scaffold
- set up database schema
- set up auth provider for Google Sign-In
- set up file storage for images and videos
- set up deployment and environment variables

Deliverable:

- app runs locally
- auth, database, and storage connections are working

### Stage 1: Broker access

Build issues:

- `#1` Broker login with Google Sign-In
- `#2` Broker profile setup

Deliverable:

- broker can sign in
- first-time broker lands on profile setup
- returning broker lands on dashboard

### Stage 2: Broker inventory creation

Build issues:

- `#3` Create rental listing
- `#4` Upload listing photos and videos
- `#9` Broker hides inactive listing

Deliverable:

- broker can create listing
- broker can save draft
- broker can publish listing
- broker can hide and reactivate listing

## Stage 3: Public inventory

Build issues:

- `#5` Publish and share broker and listing pages
- `#7` Renter views listing details

Deliverable:

- broker page has a public URL
- listing has a public URL
- shared listing link opens directly on listing detail page

### Stage 4: Contact conversion

Build issues:

- `#8` Renter contacts broker directly

Deliverable:

- renter can call broker
- renter can open WhatsApp with listing context

### Stage 5: Discovery and narrowing

Build issues:

- `#6` Renter filters listings

Deliverable:

- renter can filter by area, budget, type, brokerage, and furnishing
- missing rent/brokerage listings are excluded when those filters are applied

### Stage 6: Launch pass

This is the launch-readiness pass after all core flows exist:

- mobile responsiveness pass
- slower-network sanity check
- empty-state check
- missing-data fallback check
- share-link verification
- call/WhatsApp verification

Deliverable:

- a broker can realistically use it with live listings

## Why this order

This order follows the shortest path to value:

- without sign-in and profile, there is no broker identity
- without listing creation, there is nothing to share
- without public pages, there is nothing for renters to open
- without contact actions, there is no conversion
- filters help conversion quality, but they are not the first blocker

## Dependency map

- `#2` depends on `#1`
- `#3` depends on `#1` and enough of `#2` to know the broker identity
- `#4` depends on `#3`
- `#9` depends on `#3`
- `#5` depends on `#2`, `#3`, and `#9`
- `#7` depends on `#5`
- `#8` depends on `#7`
- `#6` depends on `#5`

## Demo checkpoints

### Checkpoint A

After Stage 1:

- sign in with Google
- complete profile
- land on empty dashboard

### Checkpoint B

After Stage 2:

- create one listing
- upload media
- save draft
- publish
- hide and reactivate listing

### Checkpoint C

After Stage 3 and 4:

- share broker page
- share listing page
- open shared link in logged-out state
- call or WhatsApp broker

### Checkpoint D

After Stage 5:

- filter live inventory
- confirm missing-value behavior for rent and brokerage

## Phase 1 launch definition

Phase 1 is ready to launch when all of the following are true:

- broker can sign in with Google
- broker can complete profile setup
- broker can create, draft, publish, hide, and share listings
- renter can open broker page without login
- renter can open listing detail without login
- renter can call or WhatsApp broker
- filters work on mobile
- optional rent and brokerage fields gracefully show `Ask broker`

## Practical risk notes

### Video upload

Video is in the current Phase 1 scope, but it is the biggest media-risk item.

If implementation timeline slips:

- keep image upload mandatory for launch
- keep video support behind a soft rollout if needed

That is a fallback only, not the default product decision.

### Filters

Filters should ship in Phase 1, but they should stay simple.

Do not add:

- map-based filters
- saved searches
- smart ranking

## Suggested engineering rhythm

- finish one stage fully before moving to the next
- keep every stage demoable
- test on mobile after every major stage
- use the repo docs as the source of truth if chat context gets lost

## Source documents for implementation

If implementation starts later, rebuild context from:

- `README.md`
- `docs/PRD.md`
- `docs/user-stories.md`
- `docs/wireframes.md`
- `docs/high-fidelity-ui-spec.md`
- this file
