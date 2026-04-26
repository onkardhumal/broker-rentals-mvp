# GitHub Backlog

Suggested project name: `Broker Rentals MVP`

## Epic 1: Foundation

- Create app repository structure
- Set up staging and production environments
- Define data models for `Broker`, `Listing`, `ListingMedia`, and optional `LeadRequest`
- Set up analytics events
- Add app shell and navigation

## Epic 2: Broker Login and Profile

- Broker login with `Google Sign-In`
- First-time broker routing to profile setup
- Broker onboarding flow
- Create and edit broker profile
- Add broker photo or logo upload
- Generate public broker page URL

## Epic 3: Listing Management

- Create new rental listing
- Edit listing
- View all listings in broker dashboard
- Publish or unpublish listing
- Delete listing
- Duplicate listing
- Add validation for required fields
- Future: show draft completeness state before publishing

## Epic 4: Media Upload

- Upload multiple images for a listing
- Upload one property video or short clip
- Remove uploaded media
- Reorder images
- Optimize media for mobile upload

## Epic 5: Public Broker Page

- Build broker public page
- Show all active rental listings
- Add filters for `area`, `budget`, `room type`, `brokerage`, and `furnishing`
- Add listing cards
- Add empty state for no matching listings

## Epic 6: Listing Detail

- Build listing detail page
- Show image and video gallery
- Show rent, deposit, brokerage, furnishing, availability, locality, and society
- Add `Call Broker` action
- Add `WhatsApp Broker` action
- Add shareable single-listing link

## Epic 7: Lead Flow

- Prefilled WhatsApp inquiry message
- Direct call button behavior
- Optional `Request Visit` or `Request Callback`
- Store lead requests if form is included

## Epic 8: Sharing and Growth

- Share broker page link
- Share individual listing link
- Add link preview metadata for WhatsApp and Facebook
- Add copy-link action
- Add share action inside broker dashboard

## Epic 9: QA and Launch

- Mobile responsiveness testing
- Loading, error, and empty states
- Basic SEO checks
- Performance pass for slower mobile internet
- Demo seed data
- Launch checklist for first five brokers

## Labels

- `mvp`
- `must-have`
- `good-to-have`
- `frontend`
- `backend`
- `design`
- `qa`
- `blocked`
