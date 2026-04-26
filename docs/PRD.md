# PRD

## Product

Working title: `Broker Rentals MVP`

One-line summary: a mobile-first tool that lets a broker create a personal rental listings page, upload photos and videos, and share one link on WhatsApp, Facebook groups, and direct chats.

## Users

- `Broker/Agent`: creates a profile, uploads listings, and shares the page
- `Renter`: browses listings and contacts the broker directly

## Authentication

- Broker login only
- No renter login in MVP
- Recommended authentication: `mobile number + OTP`

## Problem

- Small brokers post many scattered statuses every day
- Renters get incomplete details across chats and groups
- Brokers repeat the same information many times
- Inventory is hard to organize by area, budget, and room type
- Existing portals are often too heavy for local WhatsApp-first brokers

## Goal

Help a broker publish a clean rental listings page in minutes and help renters find relevant properties fast without needing an account.

## MVP scope

- Broker signup/login
- Broker profile setup
- Add, edit, hide, and delete rental listings
- Photo and video upload
- Public broker page with filters
- Public listing detail page
- Call broker and WhatsApp broker actions
- Optional lightweight `Request Visit` or `Request Callback`

## Out of scope

- Sale properties
- Flatmates product
- Renter login
- Payments or subscriptions
- In-app chat
- Multi-broker marketplace discovery
- Advanced CRM
- Map-based search
- AI recommendations

## Broker requirements

- Sign in using mobile OTP
- Create public profile with name, phone, WhatsApp number, photo/logo, and service area
- Add rental listings with images, videos, and property details
- Share broker page link
- Share individual listing link
- Hide inactive listings quickly

## Renter requirements

- Open shared link without login
- Browse listings from one broker
- Filter by area, price, room type, society, and brokerage
- View photos, videos, and full rental details
- Call broker directly
- Message broker on WhatsApp directly

## Listing fields

- Listing title
- Area or locality
- Society or building name
- Property type: `1 RK`, `1 BHK`, `2 BHK`, room, PG, shop, office, and similar rental categories
- Rent amount
- Deposit
- Brokerage or charges
- Furnishing
- Availability
- Size if available
- Floor if relevant
- Short description
- Photos
- Videos
- Contact number
- Preferred contact mode

## Core screens

- Broker login
- Broker onboarding or profile setup
- Broker dashboard
- Add or edit listing
- Public broker page
- Public listing detail page
- Optional request visit or callback form

## Primary user flow

1. Broker signs in with mobile OTP
2. Broker sets up profile
3. Broker adds first rental listing
4. Broker uploads photos and videos
5. Broker publishes listing
6. Broker shares broker-page link or single-listing link
7. Renter opens link, filters listings, and contacts broker

## Functional requirements

- Each broker gets a public shareable page
- Each listing gets its own public URL
- Public pages must be mobile-friendly
- Listing filters must work without login
- Call and WhatsApp actions must be clearly visible
- Media uploads should work well from mobile devices
- Broker must be able to edit or deactivate listings at any time

## Non-functional requirements

- Mobile-first design
- Fast loading on average mobile internet
- Simple onboarding
- Trustworthy UI
- Basic SEO and link-preview support for public pages
- Secure OTP-based authentication
- Basic media compression for upload speed

## Success metrics

- Broker signups
- Profile completion rate
- Time to first listing
- Listings created per broker
- Broker page shares
- Listing page views
- Call button clicks
- WhatsApp button clicks
- Repeat usage by brokers

## Product bet

If local brokers can create a clean rental listings page in minutes, they will prefer sharing one organized link over posting many scattered statuses, and renters will convert faster because the information is already structured.
