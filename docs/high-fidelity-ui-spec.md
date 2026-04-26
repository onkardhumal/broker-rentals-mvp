# High-Fidelity UI Spec

This document turns the low-fidelity wireframes into a stronger product direction that is realistic for an Indian rental audience and concrete enough for design or implementation.

## Product feel

The product should feel:

- trustworthy, not flashy
- fast, local, and practical
- optimized for WhatsApp-driven sharing
- clear enough for first-time brokers who are not comfortable with complex dashboards

The renter should feel:

- "I can scan this quickly"
- "I can trust this broker enough to call or WhatsApp"
- "I understand rent, deposit, brokerage, furnishing, and locality without guessing"

The broker should feel:

- "I can upload and share listings in minutes"
- "I do not need technical knowledge"
- "This looks more professional than posting statuses"

## Visual direction

Use a bright, clean, mobile-first design with a local-services feel rather than a luxury real-estate feel.

### Color system

- Primary: deep teal `#0F766E`
- Primary dark: `#115E59`
- Accent: warm amber `#D97706`
- Surface: soft off-white `#FCFBF7`
- Card: white `#FFFFFF`
- Border: `#E7E5E4`
- Text primary: `#1C1917`
- Text secondary: `#57534E`
- Success: `#15803D`
- Danger: `#B91C1C`

### Typography

- Headings: `Poppins`
- Body: `Inter`
- Numbers/prices can use slightly bolder `Inter Semi Bold`

Suggested scale:

- Page title: 28
- Section title: 20
- Card title: 18
- Body: 14 to 16
- Meta labels: 12 to 13

### Shape and depth

- Radius: 14 for cards, 12 for inputs, 999 for pills/chips
- Shadows: very light, mostly used on cards and sticky action bars
- Borders: thin and soft, avoid harsh separators

### Icon style

- Clean outline icons
- Use icons only where they improve scanning: location, rupee, phone, WhatsApp, image, video, edit, share

## Layout system

- Mobile-first canvas width: 390 to 430
- Primary content width: full mobile width with 16px side padding
- Vertical rhythm: 8px grid
- Section spacing: 16 to 24px

## Shared interaction rules

- Primary CTA is always filled
- Secondary CTA is outlined
- Destructive actions are text or subtle outlined red
- WhatsApp action should often be visually stronger than a generic secondary action
- Sticky footer CTAs are recommended on renter-facing detail screens

## Shared components

### Broker card header

Used on public broker page and listing detail.

Contains:

- profile photo
- broker/business name
- service localities
- short trust line like `Families + Bachelors`
- `Call` and `WhatsApp` actions

### Listing card

Contains:

- media thumbnail
- property type + locality
- rent or `Ask broker`
- deposit
- brokerage or `Ask broker`
- furnishing
- society
- `View details`

Card order matters:

1. property type + locality
2. rent
3. deposit + brokerage
4. furnishing + society

### Filter chips

- rounded pills
- inactive: light border, white fill
- active: primary fill with white text
- should be easy to tap one-handed

### Data rows

Used for rent, deposit, brokerage, furnishing, availability.

- label on top or left
- value bold enough to scan
- if missing, show `Ask broker`

## Screen 1: Broker sign-in

Goal: remove friction and communicate value quickly.

### Structure

- Logo or wordmark
- one-line promise
- visual panel with property thumbnails or abstract property collage
- `Continue with Google`
- terms text

### High-fidelity behavior

- page uses large whitespace and one strong CTA
- background can use a subtle warm gradient from off-white to pale mint
- CTA should span most of the width

### Copy suggestion

Title:
`Create one rental page. Share everywhere.`

Subtitle:
`For brokers, agents, and local connectors who work through WhatsApp and Facebook groups.`

## Screen 2: Broker profile setup

Goal: complete trust-building basics without feeling like a long onboarding form.

### Step 1

- profile photo uploader at top
- name
- phone number
- WhatsApp number
- service areas

### Step 2

- short intro
- preferred contact
- preview public page

### High-fidelity behavior

- use progress indicator with `Step 1 of 2`
- inputs should be large and forgiving
- area input can later evolve to tag chips, but plain text is enough for MVP

### Validation behavior

- inline errors under fields
- do not use modal errors

## Screen 3: Broker dashboard

Goal: help the broker do three things quickly:

1. add listing
2. share broker page
3. share or manage a specific listing

### Structure

- welcome header
- public page block with `Copy link` and `Share page`
- active/inactive counters
- prominent `+ Add listing`
- listing stack

### Listing row behavior

Each listing row should show:

- property type
- locality
- rent or `Ask broker`
- status badge
- quick actions: `Edit`, `Hide`, `Share`

### Share behavior

- `Share` on top block = share broker page
- `Share` on listing row = share listing detail URL

This matches your understanding and is the right product behavior.

### Visual notes

- broker page block can use a tinted primary background with white text
- listing rows should be white cards on a soft surface background
- status badges:
  - active = green tint
  - inactive = neutral gray tint

## Screen 4: Add listing - basics

Goal: keep property entry quick, structured, and mobile-friendly.

### Required fields

- property type
- locality/area
- society/building
- deposit

### Optional in MVP

- rent
- brokerage

If optional values are blank, the public view should show `Ask broker`.

### High-fidelity form behavior

- property type as wrapped chips
- numeric inputs use number keyboard
- helper text for optional fields

Example helper copy:

- `Rent (Optional)`
- `Brokerage (Optional)`

## Screen 5: Add listing - furnishing, media, publish

Goal: finish the listing without overwhelming the broker.

### Sections

- furnishing selector
- availability
- description
- photo upload
- video upload
- save draft / publish

### Draft behavior

For MVP:

- simple `Save draft`
- draft stays private

Later:

- add `draft completeness` like `4/6 fields completed`
- show what is missing before publish

### Visual notes

- media upload blocks should look tappable, like soft dashed cards
- uploaded media should show as small preview tiles

## Screen 6: Public broker page

Goal: help renters scan inventory fast and contact the broker directly.

### Above-the-fold priority

1. broker identity
2. call / WhatsApp
3. filters
4. first 1-2 listings

### High-fidelity layout

- sticky header with broker name after scroll
- filters shown as horizontal chips
- listings in stacked cards
- `Share page` can be smaller than contact actions

### Public trust pattern

Show:

- broker name
- profile image
- areas served
- short intro
- phone/WhatsApp actions

Do not show:

- cluttered analytics
- too many badges
- complex meta information

## Screen 7: Filter sheet

Goal: keep filtering lightweight and mobile-native.

### Filter groups

- area
- budget
- property type
- furnishing
- brokerage

### Behavior

- opens as bottom sheet
- `Reset` at top right
- bottom CTA says `Show X listings`

### Important rule

If rent or brokerage is blank on a listing, and the renter applies that respective filter, that listing should drop out of results.

## Screen 8: Listing detail page

Goal: convert interest into contact.

### Priority order

1. gallery
2. property type + locality
3. rent
4. deposit
5. brokerage
6. furnishing
7. availability
8. society
9. description
10. broker block
11. sticky contact actions

### CTA behavior

- sticky bottom bar with:
  - `Call Broker`
  - `WhatsApp Broker`

### Missing info handling

- if rent missing: show `Ask broker`
- if brokerage missing: show `Ask broker`

## Screen 9: Empty state

Goal: avoid dead ends.

### Content

- message that no listings match filters
- `Clear filters`
- still show `Call broker` and `WhatsApp broker`

This is important for Indian rental behavior because many renters will still ask whether something similar is available.

## Recommended content style

Use short, plain, local-service language:

- `Rent`
- `Deposit`
- `Brokerage`
- `Furnishing`
- `Immediate`
- `Ask broker`

Avoid:

- overly premium real-estate jargon
- long marketing copy

## States to design

Before coding, these states should all be visually considered:

- sign-in default
- sign-in error
- profile validation error
- dashboard empty state
- listing draft state
- media upload progress
- public page no results
- listing detail with missing rent
- listing detail with missing brokerage

## Mapping to implementation

This document plus the lower-fidelity wireframes should be enough to:

- create final Figma screens later
- build the first responsive UI
- keep product decisions consistent when context is reloaded
