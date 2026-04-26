# Wireframes

These are low-fidelity, mobile-first wireframes for the broker rentals MVP. They are written for Indian usage patterns first: Android-heavy traffic, WhatsApp sharing, one-handed browsing, locality-first discovery, visible pricing, visible brokerage, and fast direct contact.

## UX assumptions for Indian users

- Most brokers and renters will first open the app or links on a phone, not desktop
- Many users will come from WhatsApp chats, statuses, and Facebook groups
- Locality and society matter more than long descriptions
- Rent, deposit, brokerage, furnishing, and availability should be visible early
- Trust signals matter: broker name, profile photo, locality served, phone, WhatsApp
- Users may not want long forms, so broker data entry should be short and structured
- Media is important, but pages should still work on slower mobile internet

## UX principles

- Show key rental facts above the fold
- Use familiar Indian rental language: `1 RK`, `1 BHK`, `2 BHK`, `3 BHK`, `4 BHK`, `Semi-furnished`, `Brokerage`
- Make WhatsApp and Call actions persistent and obvious
- Keep filters lightweight and easy to reset
- Reduce typing by using selectable property-type and furnishing options
- Route first-time brokers straight into profile setup after Google sign-in

## Screen 1: Broker sign-in

Relevant issue: `#1`

```text
+--------------------------------------------------+
| Broker Rentals                                   |
| Find tenants faster. Share one clean listing page|
|                                                  |
|  [ Illustration / property collage ]             |
|                                                  |
|  For brokers, agents, and local connectors       |
|                                                  |
|  [ Continue with Google ]                        |
|                                                  |
|  By continuing, you agree to Terms / Privacy     |
|                                                  |
|  Already shared your link before? Sign in again  |
+--------------------------------------------------+
```

**UX note**

- One primary action only
- Avoid extra fields on first screen
- Keep copy simple and trust-building

## Screen 2: First-time broker profile setup

Relevant issue: `#2`

```text
+--------------------------------------------------+
| Set up your broker profile               Step 1/2|
| This will appear on your public page            |
|                                                  |
|  Profile photo                                  |
|  [ Upload photo ]                               |
|                                                  |
|  Full name                                      |
|  [______________________________]               |
|                                                  |
|  Phone number                                   |
|  [______________________________]               |
|                                                  |
|  WhatsApp number                                |
|  [______________________________]               |
|                                                  |
|  Areas you serve                                |
|  [ Eg. Wakad, Baner, Hinjewadi ]                |
|                                                  |
|  [ Continue ]                                   |
+--------------------------------------------------+
```

```text
+--------------------------------------------------+
| Set up your broker profile               Step 2/2|
|                                                  |
|  Short intro                                     |
|  [ Rentals in West Pune / Bachelor / Family ]   |
|                                                  |
|  Preferred contact                               |
|  ( ) WhatsApp first                              |
|  ( ) Call first                                  |
|                                                  |
|  [ Preview page ]                                |
|  [ Finish setup ]                                |
+--------------------------------------------------+
```

**UX note**

- Ask only for what improves trust and contactability
- Split into 2 small steps instead of one long form

## Screen 3: Broker dashboard

Relevant issues: `#2`, `#3`, `#4`, `#5`, `#9`

```text
+--------------------------------------------------+
| Hi, Rahul                                        |
| Your public page: broker.app/rahul-123          |
| [ Copy link ] [ Share ]                          |
|                                                  |
|  Listings summary                                |
|  Active 12   Inactive 3                          |
|                                                  |
|  [ + Add listing ]                               |
|                                                  |
|  Your listings                                   |
|  ----------------------------------------------  |
|  2 BHK | Baner | 28,000 | Active                 |
|  [ Edit ] [ Hide ] [ Share ]                     |
|                                                  |
|  1 RK | Wakad | 11,000 | Active                  |
|  [ Edit ] [ Hide ] [ Share ]                     |
|                                                  |
|  3 BHK | Hinjewadi | 40,000 | Inactive           |
|  [ Edit ] [ Activate ]                           |
+--------------------------------------------------+
```

**UX note**

- Share link stays near the top because sharing is the broker's daily behavior
- Share on each listing card means the broker can send a direct public link to that exact property, and the viewer lands on the listing-detail experience rather than the full dashboard
- Listing cards show the minimum decision info: type, locality, price, status

## Screen 4: Add listing - basics

Relevant issue: `#3`

```text
+--------------------------------------------------+
| Add rental listing                      Step 1/2 |
|                                                  |
|  Property type                                   |
|  [1 RK] [1 BHK] [2 BHK] [3 BHK]                  |
|  [4 BHK] [Studio] [Penthouse] [Room]             |
|                                                  |
|  Locality / Area                                 |
|  [______________________________]               |
|                                                  |
|  Society / Building                              |
|  [______________________________]               |
|                                                  |
|  Rent (Optional)                                 |
|  [______________________________]               |
|                                                  |
|  Deposit                                          |
|  [______________________________]               |
|                                                  |
|  Brokerage (Optional)                            |
|  [______________________________]               |
|                                                  |
|  [ Continue ]                                     |
+--------------------------------------------------+
```

**UX note**

- Use selection chips for property type to reduce typing
- Put locality and price early because they are the most searched fields
- Rent and brokerage stay optional in MVP, but if left blank the public UI should display `Ask broker`

## Screen 5: Add listing - furnishing, media, publish

Relevant issues: `#3`, `#4`

```text
+--------------------------------------------------+
| Add rental listing                      Step 2/2 |
|                                                  |
|  Furnishing                                      |
|  ( ) Unfurnished                                 |
|  ( ) Semi-furnished                              |
|  ( ) Furnished                                   |
|                                                  |
|  Availability                                    |
|  [ Immediate / From date ]                       |
|                                                  |
|  Description                                     |
|  [__________________________________________]    |
|                                                  |
|  Upload photos                                   |
|  [ + Add photos ]                                |
|                                                  |
|  Upload video                                    |
|  [ + Add video ]                                 |
|                                                  |
|  [ Save draft ]      [ Publish listing ]         |
+--------------------------------------------------+
```

**UX note**

- Keep one video optional in MVP
- Save draft is useful because brokers often collect details in pieces
- A richer `draft completeness` state can come later, but it is not required for MVP

## Screen 6: Public broker page

Relevant issues: `#5`, `#6`

```text
+--------------------------------------------------+
| [ Photo ] Rahul Properties                       |
| Baner, Wakad, Hinjewadi                          |
| WhatsApp first | Families + Bachelors            |
| [ Call ] [ WhatsApp ] [ Share page ]             |
|                                                  |
|  Filters                                         |
|  [ Area ] [ Budget ] [ Type ] [ Furnishing ]     |
|                                                  |
|  18 properties available                         |
|                                                  |
|  ----------------------------------------------  |
|  [ 3 photos ]   2 BHK in Baner                   |
|  Rent 28,000 | Deposit 70,000                    |
|  Brokerage 1 month | Semi-furnished              |
|  Society: Park View                              |
|  [ View details ]                                |
|                                                  |
|  ----------------------------------------------  |
|  [ 2 photos ]   1 RK in Wakad                    |
|  Rent 11,000 | Deposit 25,000                    |
|  Brokerage 5,000 | Unfurnished                   |
|  [ View details ]                                |
+--------------------------------------------------+
```

**UX note**

- Contact buttons appear before listings because many renters contact quickly
- Cards surface brokerage and furnishing without forcing another tap

## Screen 7: Filter bottom sheet

Relevant issue: `#6`

```text
+--------------------------------------------------+
| Filter listings                            Reset |
|                                                  |
|  Area                                            |
|  [ Baner ] [ Wakad ] [ Hinjewadi ]               |
|                                                  |
|  Budget                                          |
|  [ Min ] -----------slider----------- [ Max ]    |
|                                                  |
|  Type                                            |
|  [1 RK] [1 BHK] [2 BHK] [3 BHK] [4 BHK]          |
|  [Penthouse] [Room] [PG]                         |
|                                                  |
|  Furnishing                                      |
|  [ Unfurnished ] [ Semi-furnished ] [ Furnished ]|
|                                                  |
|  Brokerage                                       |
|  [ No pref ] [ Under 5k ] [ 1 month ]            |
|                                                  |
|  [ Show 7 listings ]                             |
+--------------------------------------------------+
```

**UX note**

- Bottom sheet feels natural on mobile and keeps context
- Show result count on CTA to reduce uncertainty

## Screen 8: Listing detail page

Relevant issues: `#7`, `#8`

```text
+--------------------------------------------------+
| < Back                                            |
| [ Photo carousel / video thumbnail ]             |
|                                                  |
|  2 BHK in Baner                                  |
|  Rent 28,000 / month                             |
|  Deposit 70,000                                  |
|  Brokerage 1 month                               |
|  Semi-furnished                                  |
|                                                  |
|  Society                                          |
|  Park View Residency                              |
|                                                  |
|  Availability                                     |
|  Immediate                                        |
|                                                  |
|  Description                                      |
|  Family preferred. Near metro. Good ventilation. |
|                                                  |
|  Broker                                           |
|  [ Photo ] Rahul Properties                       |
|                                                  |
|  [ Call Broker ]   [ WhatsApp Broker ]            |
+--------------------------------------------------+
```

**UX note**

- Core facts are stacked in a rent-first order
- Sticky contact CTA is recommended in implementation

## Screen 9: No results state

Relevant issue: `#6`

```text
+--------------------------------------------------+
| No matching listings                              |
| Try changing budget, type, or furnishing filter   |
|                                                    |
| [ Clear filters ]                                  |
| [ Call broker ] [ WhatsApp broker ]                |
+--------------------------------------------------+
```

**UX note**

- Empty states should still keep the renter close to contact
- In Indian rental behavior, many renters will ask "anything else available?"

## Mapping to issues

- `#1` Broker login with Google Sign-In: Screen 1
- `#2` Broker profile setup: Screen 2
- `#3` Create rental listing: Screens 4 and 5
- `#4` Upload listing photos and videos: Screen 5
- `#5` Publish and share broker page: Screens 3 and 6
- `#6` Renter filters listings: Screens 6, 7, and 9
- `#7` Renter views listing details: Screen 8
- `#8` Renter contacts broker directly: Screens 6 and 8
- `#9` Broker hides inactive listing: Screen 3

## Research-based decisions behind these wireframes

- `Google Sign-In first`: lowers friction and avoids OTP cost for MVP
- `Profile after login`: keeps the first screen light and reduces abandonment
- `Locality-first cards`: Indian renters usually narrow by area before finer details
- `Brokerage visible early`: hidden charges break trust quickly
- `WhatsApp before form`: direct messaging is a default behavior for this audience
- `Chips over typing`: many repeated rental formats can be tapped faster than typed
- `Short broker dashboard`: brokers care about shareability and inventory status, not analytics first
