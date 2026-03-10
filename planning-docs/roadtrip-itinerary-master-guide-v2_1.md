# Morocco Road Trip - Complete Research & Booking Guide

**Master Planning Document | Version 2.0 | February 2026**

*This guide provides Claude with a comprehensive methodology for researching and presenting travel options, plus a final booking strategy guide for the user.*

---

## ðŸŽ¯ OVERVIEW: The Complete Research Process

**Goal:** Provide Phil & Steph with detailed, decision-ready information across all budget tiers so they can select a Morocco trip within their Â£2,800-3,800 budget.

**Trip Parameters:**
- **Duration:** 11 nights (March 31 - April 11, 2026)
- **Travelers:** 2 people (Phil & Steph)
- **Budget:** Â£2,800 - Â£3,800 total
- **Style:** Self-drive with mix of accommodation tiers
- **Priorities:** Nature-focused, recovery days, authentic experiences

**Key Principle:** Data access methods change over time (APIs close, websites block scrapers, new tools emerge). Therefore, Claude must FIRST investigate what's currently possible before starting the main research.


---

## 🚨 CRITICAL: DATE VERIFICATION PROTOCOL (MANDATORY)

**⚠️ BEFORE STATING ANY CHECK-IN/CHECK-OUT DATE, EXECUTE THIS PROTOCOL**

### Why This Exists
Date errors in travel booking = expensive mistakes (non-refundable bookings, wrong dates, wasted money). This protocol prevents:
- Reading section headings instead of itinerary table
- Assuming dates from memory
- Confusing arrival dates with stay dates
- Day-date mismatches

### MANDATORY 6-STEP VERIFICATION PROCESS

#### **STEP 1: Locate in Itinerary Table**
```
ACTION: Open master file, find ITINERARY TABLE (NOT section headings)
LOCATION: Day-by-day itinerary table in master document
REQUIREMENT: Read ONLY from this table
```

#### **STEP 2: Extract Arrival Date**
```
RULE: Find first row where location appears in "Location" column
EXTRACT: Date + Day from table
NOTE: Arrow (→) means ARRIVAL that day
```

Example:
```
| **Apr 3** | **Fri** | → Agdz | ... |
ARRIVAL: Friday, April 3, 2026
```

#### **STEP 3: Extract Departure Date**
```
RULE: Find first row where DIFFERENT location appears AFTER target location
EXTRACT: That date = checkout date
```

Example:
```
Agdz appears: Apr 3, Apr 4
Next location: | **Apr 5** | **Sun** | → Taroudant | ... |
DEPARTURE: Sunday, April 5, 2026
```

#### **STEP 4: Calculate Nights**
```
FORMULA: Count nights between arrival and departure
METHOD: Count days you sleep AT that location
VERIFY: Must match "Nights X-Y" designation
```

Example:
```
Arrival: Apr 3 → Sleep Apr 3
Stay: Apr 4 → Sleep Apr 4  
Departure: Apr 5 → Leave (don't sleep)
NIGHTS: 2
```

#### **STEP 5: Verify Day-Date Correlation**
```
REQUIREMENT: Confirm day-of-week matches date
METHOD: Use trip anchor date or 2026 calendar
ANCHOR: March 30, 2026 = Monday (known)
```

Morocco Trip 2026 Calendar:
```
Mar 30 (Mon) | Mar 31 (Tue) | Apr 1 (Wed) | Apr 2 (Thu)
Apr 3 (Fri)  | Apr 4 (Sat)  | Apr 5 (Sun) | Apr 6 (Mon)
Apr 7 (Tue)  | Apr 8 (Wed)  | Apr 9 (Thu)
```

#### **STEP 6: State Booking Dates**
```
MANDATORY FORMAT:
✅ Check-in: [Day], [Month] [Date], 2026
✅ Check-out: [Day], [Month] [Date], 2026  
✅ Nights: [X] nights (sleep [dates])
```

### Verification Template (Show in Response)

**Before stating booking dates, Claude MUST show:**

```
DATE VERIFICATION FOR [LOCATION]:

From itinerary table:
[Quote relevant rows]

Arrival: [Day], [Date] (→ symbol confirms arrival)
Departure: [Day], [Date] (next location)
Nights: [X] (sleep [dates])
Day-date check: ✅ Verified against 2026 calendar

CONFIRMED BOOKING DATES:
Check-in: [Day], [Month] [Date], 2026
Check-out: [Day], [Month] [Date], 2026
Nights: [X] nights
```

### Common Errors to Avoid

❌ **Reading section headings** → ✅ Read itinerary table  
❌ **Assuming from memory** → ✅ Execute protocol every time  
❌ **Confusing → with stay** → ✅ Arrow = arriving, not departing  
❌ **Off-by-one errors** → ✅ Count nights slept, not days visited  
❌ **Wrong day-date** → ✅ Verify against calendar

### Enforcement

**Execute this protocol:**
- Before every booking date statement
- Before updating master file with dates
- When user asks about dates
- Every single time, no exceptions

**If Claude states dates without showing verification → Call it out immediately**

---

## ðŸ“Š PHASE 1: PRELIMINARY INVESTIGATION (Do This First!)

**Purpose:** Determine the best available data sources and access methods RIGHT NOW.

### Step 1.1: Test Current Data Access Methods

**For FLIGHTS:**
```
1. Test Skyscanner page fetching:
   - Try: web_fetch on https://www.skyscanner.net/routes/[origin]/[dest]/
   - Check: Does it return price data or is it blocked?

2. Search for API access:
   - Query: "Skyscanner API public access 2026"
   - Query: "flight price API free public 2026"
   - Check: Are there new free APIs? Partnership requirements?

3. Test alternative aggregators:
   - Google Flights: Can we fetch the page?
   - Kayak: Can we fetch the page?
   - Momondo: Can we fetch the page?

4. Document findings:
   - Which sites provide accessible data?
   - What format (HTML we can parse, JSON, XML)?
   - What limitations (recent searches only, no live pricing)?
```

**For ACCOMMODATION:**
```
1. Test hotel aggregator access:
   - Booking.com: Try fetching a hotel page
   - KAYAK hotels: Try fetching search results  
   - Hotels.com: Try fetching
   - Expedia: Try fetching

2. Test direct hotel websites:
   - Pick 2-3 known hotels
   - Try fetching their websites
   - Check: Can we get pricing info?

3. Search for API access:
   - Query: "Booking.com API public access 2026"
   - Query: "hotel booking API free 2026"
   - Check: Partnership requirements? Cost?

4. Document findings:
   - Which sources work?
   - Which provide actual pricing?
   - Which only show features/reviews?
```

**For CAR HIRE:**
```
1. Test car rental sites:
   - Try: Rentalcars.com search page
   - Try: Kayak car rental page
   - Try: Direct sites (Hertz, Europcar, Budget)

2. Search for API access:
   - Query: "car rental API public 2026"
   - Query: "Hertz API free access"

3. Document findings:
   - What's accessible?
   - What data can we extract?
```

### Step 1.2: Document Investigation Results

**Create a findings summary:**
```markdown
## Data Access Status Report (Date: [YYYY-MM-DD])

### Flights
- **Working:** [List sites/methods that work]
- **Blocked:** [List sites that block access]
- **Data Quality:** [What we can get: ranges/exact prices/availability]
- **Limitations:** [e.g., "Recent searches only, not live pricing"]

### Accommodation  
- **Working:** [...]
- **Blocked:** [...]
- **Data Quality:** [...]
- **Limitations:** [...]

### Car Hire
- **Working:** [...]
- **Blocked:** [...]
- **Data Quality:** [...]
- **Limitations:** [...]

### Recommended Approach
Based on current access, here's how we'll proceed:
1. [Method for flights]
2. [Method for accommodation]
3. [Method for car hire]
```

---

## ðŸ“‹ PHASE 2: COMPREHENSIVE RESEARCH (After Investigation)

**Now that you know what's accessible, gather maximum information using the best available methods.**

### RESEARCH WORKFLOW

#### A. FLIGHTS (All UK Airports â†’ Marrakech)

**Airports to Research:**
1. Manchester (MAN) - Primary (closest to Nottingham, most flights)
2. Birmingham (BHX) - Secondary (closer to Nottingham, fewer flights)
3. East Midlands (EMA) - Tertiary (closest but check if directs exist)
4. Luton (LTN) - Backup (easyJet hub)

**For Each Airport, Gather:**

1. **Availability:**
   - Direct flights available?
   - Flight frequency (flights per week)
   - Airlines operating route
   - Average flight time

2. **Pricing Information:**
   - Recent price ranges for March/April departures
   - Price for 2 people return
   - Baggage costs (if available)
   - Best day of week to fly

3. **Practical Details:**
   - Distance from Nottingham (driving time)
   - Airport parking costs (if driving)
   - Train connections (if not driving)
   - On-time performance/delays

4. **Booking Links:**
   - Direct airline booking pages
   - Comparison sites (Skyscanner, Google Flights, etc.)
   - Format: Clear clickable URLs

**Present as:**
```markdown
### Option 1: Manchester (MAN) - RECOMMENDED
**Availability:** Daily directs with easyJet, Ryanair, TUI (18 flights/week)
**Recent Pricing:** Â£45-85/person = Â£90-170 for 2 people return
**Flight Time:** 3h 40m direct
**Baggage:** Â£15-35/bag each way (check at booking)
**Distance:** 90 min drive from Nottingham
**Delays:** 22% delayed (avg 114min), avoid afternoon departures
**Best Days:** Monday/Tuesday typically 10-20% cheaper
**Booking Links:**
- Direct: [Airline URLs]
- Compare: [Skyscanner URL] | [Google Flights URL]
```

#### B. CAR HIRE (10 days: March 31 - April 11)

**Companies to Research:**
- Hertz (international, reliable)
- Budget (international, good value)
- Europcar (international)
- Green Motion (eco, discount codes available)
- LOCAL COMPANIES: Research warnings

**For Each Company, Gather:**

1. **Pricing:**
   - Base rate for 10 days
   - Insurance options & costs
   - Full/zero excess insurance cost
   - Fuel policy
   - **Total estimated cost** (all-in)

2. **Features:**
   - Unlimited mileage?
   - Additional driver cost
   - GPS/child seat costs
   - Airport pickup location
   - Drop-off flexibility

3. **Warnings:**
   - Scam reports (like ADDCAR)
   - Common upselling tactics
   - Deposit amounts
   - Credit card requirements

4. **Discount Codes:**
   - Current promotion codes
   - Validity dates
   - Restrictions

**Present as:**
```markdown
### Recommended: Hertz/Budget/Europcar (International Brands)
**Base Rate:** Â£250-350 for 10 days (economy car)
**Full Insurance:** +Â£100-200 (ESSENTIAL - get zero excess)
**Total Estimate:** Â£350-550 all-in
**Pickup:** Marrakech Menara Airport - Terminal 2 arrivals
**Requirements:** Credit card (NOT debit), full UK license, passport
**CRITICAL:** Pre-book full insurance online (cheaper than desk)
**Booking:** [Direct links for each]

### âš ï¸ AVOID: ADDCAR
**Why:** Parking lot scam, wrong vehicles, aggressive tactics
[Details of warnings]

### Alternative: Green Motion (15% discount available)
**Code:** MARRAKECH15 (valid until March 30, 2026)
**Estimate:** Â£300-450 with full insurance
**Rating:** 6-6.6/10 (mixed reviews, "card not working" scam reported)
**Booking:** https://greenmotion.com/locations/morocco/marrakech-airport
```

#### C. ACCOMMODATION (For Each Location)

**Locations:**
1. Marrakech (2 nights) - arrival splurge
2. Todra Gorge (2 nights) - confirmed: Kasbah Amazir
3. Merzouga Desert (1 night) - luxury camp
4. Agdz (2 nights) - oasis
5. Taroudant (2 nights) - authentic town
6. Agadir (2-3 nights) - beach recovery with gym

**For Each Location, Provide 3-4 Options Across Budget Tiers:**

**Budget Tier (Â£40-70/night):**
- Hotel name
- Exact/estimated price for dates
- Key features (breakfast included? pool? location?)
- Booking link
- Review rating

**Mid-Range (Â£70-120/night):**
- Same details

**Luxury (Â£120+/night):**
- Same details

**Information to Gather for Each Hotel:**

1. **Pricing:**
   - Rate per night for 2 people
   - Total for stay at this location
   - What's included (breakfast? dinner? activities?)
   - Booking.com vs. direct website comparison
   - Cancellation policy

2. **Essential Features:**
   - Room type/size
   - Private bathroom?
   - Air conditioning? (essential in Morocco)
   - WiFi quality
   - Parking available?

3. **Location-Specific Features:**
   - **Marrakech:** Pool? Rooftop terrace? Alcohol license? (RARE in Medina)
   - **Todra Gorge:** Pool? Bar? River views? Proximity to gorge?
   - **Desert Camp:** En-suite bathroom? Hot water? Activities included?
   - **Agdz:** Pool? Gardens? Hammam? Restaurant on-site?
   - **Taroudant:** Traditional riad? Pool? Medina location?
   - **Agadir:** GYM WITH FREE WEIGHTS/DUMBBELLS (ESSENTIAL), Beach access? Pool?

4. **Reviews & Reputation:**
   - Overall rating (9.0+ excellent, 8.0-8.9 very good, 7.0-7.9 good)
   - Number of reviews
   - Recent review themes
   - Awards/rankings (TripAdvisor, Booking.com)

5. **Booking Links:**
   - Direct hotel website
   - Booking.com
   - Other aggregators (if different prices)

**Present as:**
```markdown
## MARRAKECH (2 nights - Arrival Splurge)

### LUXURY: Riad Kheirredine â­â­â­â­â­
**Price:** Â£140-180/night = **Â£280-360 total**
**Rating:** 9.7/10 (3,829 reviews) - #1 Riad Africa, #5 Worldwide
**Key Features:**
- âœ… Alcohol license (RARE in Medina - wine/beer/spirits menu)
- 3 pools: 1 heated rooftop, 2 courtyard
- Multiple roof terraces with Atlas Mountain views
- Spa with hammam
- Breakfast included (rooftop or room service)
- Adults-focused, romantic
**Room Types:**
- 8 suites, all with AC, luxury bathrooms
- Some with terraces/sitting areas
**Location:** 10min walk to Jemaa el-Fnaa, Medina
**Parking:** Nearby paid parking Â£5/day, porter service
**Special:** Direct booking saves 10% vs Booking.com
**Cancellation:** Free up to 7 days before
**Booking Links:**
- Direct: https://www.riadkheirredine.com/
- Booking.com: https://www.booking.com/hotel/ma/riad-kheirredine.html
- KAYAK: $211/night (check current rate)

### MID-RANGE: Riad Brummell
**Price:** Â£100-120/night = **Â£200-240 total**
[Full details as above]

### BUDGET: Dar Darma
**Price:** Â£90-100/night = **Â£180-200 total**
[Full details as above]
```

---

## ðŸ“Š PHASE 3: BUDGET SUMMARY & OPTIONS

**After gathering all data, create:**

### Budget Matrix

```markdown
## COST BREAKDOWN SCENARIOS

### Scenario 1: BUDGET CONSCIOUS (Â£2,800 target)
- Flights: Manchester Â£90-170 (2 people return)
- Car hire: Budget/Europcar Â£400 (full insurance)
- Accommodation: Mix of budget/mid
  - Marrakech (2n): Â£180-200 (budget)
  - Todra (2n): Â£120 (Kasbah Amazir confirmed)
  - Desert (1n): Â£240 (mid-range camp)
  - Agdz (2n): Â£180 (mid-range)
  - Taroudant (2n): Â£160 (budget)
  - Agadir (3n): Â£300 (budget with gym)
- Food & activities: Â£800-1,000
**TOTAL: Â£2,470-2,930**

### Scenario 2: BALANCED (Â£3,200 target)
[Mix of mid-range and one luxury splurge]
**TOTAL: Â£3,000-3,400**

### Scenario 3: COMFORTABLE (Â£3,600 target)
[Mostly mid-range with luxury elements]
**TOTAL: Â£3,400-3,800**

### MIX & MATCH GUIDE
"Want to add luxury desert camp? (+Â£150) Offset by choosing budget in Taroudant (-Â£100)"
```

---

## ðŸ“– PHASE 4: USER BOOKING STRATEGY GUIDE

**This section is PROVIDED TO THE USER at the end of research.**

---

# ðŸŽ¯ YOUR BOOKING STRATEGY GUIDE

**How to Turn This Research Into Actual Bookings**

Phil & Steph, you now have comprehensive research showing options across all budget tiers. Here's exactly how to check live prices and make bookings:

## â° TIMING & ORDER

**Recommended Booking Order:**
1. **Flights FIRST** (6 weeks before = good timing, prices stable)
2. **Car Hire SECOND** (within 24hrs of flights - you'll know exact times)
3. **Accommodation THIRD** (most can be booked 2-4 weeks out, some flexible cancellation)

**Why This Order:**
- Flights determine your exact arrival/departure times
- Car pickup/drop times depend on flight times
- Some accommodation has free cancellation, giving you flexibility

---

## âœˆï¸ STEP 1: BOOK FLIGHTS

### What You Have From Research:
- Airport comparison with pros/cons
- Recent price ranges
- Best airlines/days
- Direct booking links

### What You Need To Do:

**A. Check Live Prices (15-20 minutes):**

1. **Go to Skyscanner:**
   - URL: https://www.skyscanner.net/
   - Enter: Your chosen airport â†’ Marrakech (RAK)
   - Dates: March 31, 2026 (out) | April 11, 2026 (return)
   - Passengers: 2 adults
   - Click "Search Flights"

2. **Check Google Flights (comparison):**
   - URL: https://www.google.com/travel/flights
   - Enter same details
   - Look for: Different airlines/times

3. **Check Direct with Airlines (often cheaper):**
   - easyJet: https://www.easyjet.com/
   - Ryanair: https://www.ryanair.com/
   - Enter same route/dates

**B. Compare Total Costs:**
```
Flight Price + Baggage (Â£15-35/bag each way) = Total Cost

Example:
Ryanair: Â£43/person base + Â£25 bags each = Â£68/person = Â£136 total
easyJet: Â£55/person base + Â£20 bags each = Â£75/person = Â£150 total
```

**C. Decision Criteria:**
- âœ… Cheapest total price (inc. bags)
- âœ… Convenient times (not 6am or midnight)
- âœ… Avoid afternoon departures if possible (more delays)
- âœ… Check customer reviews (avoid ultra-budget if concerning)

**D. Book:**
- Directly with airline usually cheapest
- Save confirmation immediately
- Note exact flight times for car booking

**â±ï¸ Time Estimate: 30 minutes research + 15 minutes booking**

---

## ðŸš— STEP 2: BOOK CAR HIRE

### What You Have From Research:
- Recommended companies (Hertz/Budget/Europcar)
- Companies to avoid (ADDCAR)
- Expected pricing with full insurance
- Discount codes (Green Motion: MARRAKECH15)

### What You Need To Do:

**A. Get Quotes (20 minutes):**

1. **Rentalcars.com (Aggregator - Easy Comparison):**
   - URL: https://www.rentalcars.com/
   - Enter:
     - Pickup: Marrakech Menara Airport
     - Date: March 31, 2026
     - Time: [Your flight arrival + 1 hour]
     - Drop-off: Same location
     - Date: April 11, 2026
     - Time: [Your flight departure - 2 hours]
   - Filter:
     - âœ… "Full to Full" fuel policy
     - âœ… Unlimited mileage
     - âœ… Show "Fully inclusive" or "Zero Excess" insurance

2. **Direct with Europcar:**
   - URL: https://www.europcar.com/
   - Enter same details
   - Add "Super Cover" or "Premium Protection" (zero excess)
   - Compare total price to Rentalcars.com

3. **Green Motion (with discount code):**
   - URL: https://greenmotion.com/locations/morocco/marrakech-airport
   - Use code: MARRAKECH15 at checkout
   - Compare total

**B. Critical Checks:**
```
âœ… Insurance is FULL/ZERO EXCESS (not basic CDW)
âœ… Unlimited mileage included
âœ… Price includes airport pickup fee
âœ… Additional driver fee if needed
âœ… Fuel policy (Full to Full is fairest)
âœ… Deposit amount (you need this available on credit card)
âœ… MUST be credit card (not debit) - Check your card
```

**C. Decision Criteria:**
- Choose established international brand (Hertz/Budget/Europcar)
- Full insurance is non-negotiable (saves hassle)
- Read reviews specifically for Marrakech airport location
- Total price including ALL fees/insurance

**D. Book:**
- Take screenshot of confirmation
- Save voucher/booking number
- Print or save to phone
- Check: "What to bring to pickup" section

**â±ï¸ Time Estimate: 30 minutes comparison + 15 minutes booking**

---

## ðŸ¨ STEP 3: BOOK ACCOMMODATION

**Recommended: Book in stages (flexibility)**

### Stage 1: Book CONFIRMED locations first

**Already Decided:**
- Todra Gorge: Kasbah Amazir (confirmed choice)

**Check Live Price:**
1. Go to Booking.com
2. Search "Kasbah Amazir Todra"
3. Dates: April 2-4, 2026 (2 nights)
4. 2 adults, 1 room
5. Check: Price, availability, breakfast included?
6. **Alternative:** Email direct: [find email on their website]
   - Often 10-15% cheaper than Booking.com
   - More flexibility

**Book it.**

### Stage 2: Book locations with LIMITED options

**Desert Camp (limited availability):**
- From research, you have 3-4 luxury camp options
- These book up fast
- Check each one:
  - Email/WhatsApp (often required for camps)
  - Request: Price for March 31, 2026 (1 night, 2 people)
  - What's included? (dinner, breakfast, camel trek, etc.)
- Compare and book

### Stage 3: Book flexible-cancellation first

**Strategy:** Book everywhere with free cancellation, finalize later

**For Marrakech, Agdz, Taroudant, Agadir:**

1. **Check Booking.com for each:**
   - Search hotel name from research
   - Enter your dates
   - Filter: "Free Cancellation"
   - Look for: "Cancel up to [X] days before for free refund"

2. **Book your TOP CHOICE with free cancellation**
   - Secures the room
   - Gives you time to research alternatives
   - No risk if you change mind

### Stage 4: Fine-tune based on budget

**After Steps 1-3, Calculate Remaining Budget:**

```
Total Budget: Â£3,200 (your target)
- Flights: Â£XXX (actual booked)
- Car: Â£XXX (actual booked)
- Desert: Â£XXX (actual booked)
- Todra: Â£120 (booked)
- Food/activities buffer: Â£900
= Remaining for other accommodation: Â£XXX

Split across 7 nights (Marrakech 2, Agdz 2, Taroudant 2, Agadir 3)
= Â£XX/night average you can afford
```

**Now Make Final Choices:**
- Want to splurge on luxury Marrakech riad? Choose budget in Taroudant.
- Want the nicer Agdz oasis? Go mid-range in Agadir.
- Over budget? Cancel free-cancellation bookings, choose cheaper options.

### AGADIR SPECIAL REQUIREMENT: Gym with Free Weights

**From research, you have 2-3 options.**

**BEFORE booking, verify gym facilities:**

1. **Email the hotel directly:**
   ```
   Subject: Gym Facilities Enquiry

   Hello,

   I'm looking to book [dates] and I have a specific requirement
   for the gym facilities. Could you please confirm:

   1. Do you have free weights/dumbbells available?
   2. What weight range? (e.g., 5kg - 30kg dumbbells)
   3. Are there barbells/squat rack or just dumbbells?
   4. What are the gym opening hours?

   This is essential for my booking decision.

   Thank you,
   Phil
   ```

2. **Wait for confirmation before booking**
   - Don't assume "gym" means free weights
   - Many hotels only have cardio machines

3. **Alternative:** Call hotel directly (faster response)

---

## ðŸ“Š FINAL BUDGET TRACKING

**Create a Simple Spreadsheet:**

```
Item | Estimated | Actual Booked | Difference
-----|-----------|---------------|------------
Flights | Â£170 | Â£156 | -Â£14 âœ…
Car Hire | Â£450 | Â£418 | -Â£32 âœ…
Marrakech (2n) | Â£200 | [pending] | 
Todra (2n) | Â£120 | Â£115 | -Â£5 âœ…
Desert (1n) | Â£240 | [pending] |
Agdz (2n) | Â£180 | [pending] |
Taroudant (2n) | Â£160 | [pending] |
Agadir (3n) | Â£360 | [pending] |
Food/Activities | Â£1,000 | n/a |
-----|-----------|---------------|------------
TOTAL | Â£2,880 | [running total] |
```

**Adjust as you go:**
- Come in under budget somewhere? Upgrade elsewhere.
- Over budget? Swap a mid-range for budget option.

---

## ðŸš¨ COMMON BOOKING MISTAKES TO AVOID

### Flights:
- âŒ Forgetting baggage costs (add Â£50-100 total)
- âŒ Booking without checking airline reviews (some budget carriers have issues)
- âŒ Ignoring flight times (3am arrival = tired first day)

### Car Hire:
- âŒ **Not getting full insurance** = Biggest mistake, can cost Â£1,000+ if damage
- âŒ Accepting basic CDW with Â£1,200 excess
- âŒ Not reading fuel policy (some charge premium for fuel)
- âŒ Forgetting you need CREDIT card (debit not accepted)
- âŒ Booking with ADDCAR or unknown local companies

### Accommodation:
- âŒ Not checking what's included (breakfast can be Â£10-20/person/day)
- âŒ Booking non-refundable when unsure
- âŒ Not verifying gym equipment before booking (your Agadir requirement)
- âŒ Assuming "Medina location" means easy car access (some require walking)

---

## â° RECOMMENDED BOOKING TIMELINE

**Today (6 weeks before trip):**
- âœ… Book flights (price is stable at 6 weeks, good timing)

**Within 48 hours:**
- âœ… Book car hire (you now know exact flight times)

**This Week:**
- âœ… Book desert camp (limited availability)
- âœ… Book Kasbah Amazir (confirmed choice)

**Next Week:**
- âœ… Book remaining accommodation with free cancellation
- âœ… Verify Agadir gym facilities via email/call

**2-3 Weeks Before Trip:**
- âœ… Finalize accommodation (cancel any free-cancellation bookings you're not using)
- âœ… Switch to better options if found

**1 Week Before:**
- âœ… Print/save all confirmations
- âœ… Check-in online for flights
- âœ… Review car hire pickup instructions

---

## ðŸ”— ESSENTIAL BOOKING WEBSITES

**Flight Comparison:**
- Skyscanner: https://www.skyscanner.net/
- Google Flights: https://www.google.com/travel/flights
- Direct Airlines: easyJet, Ryanair, TUI (from research links)

**Car Hire:**
- Rentalcars.com: https://www.rentalcars.com/
- Europcar Direct: https://www.europcar.com/
- Green Motion: https://greenmotion.com/

**Accommodation:**
- Booking.com: https://www.booking.com/
- Direct hotel websites (usually 10% cheaper, from research links)
- Email contacts (for camps and riads)

**Trip Planning:**
- Google Maps: Route planning, download offline maps
- XE Currency: https://www.xe.com/ (GBP to MAD rates)

---

## ðŸ’¡ MONEY-SAVING TIPS

1. **Book Direct with Hotels:**
   - Email: "What's your best rate for [dates]?"
   - Often 10-15% cheaper than Booking.com
   - Better room allocation

2. **Package Deal Check:**
   - Some airlines offer flight+hotel packages
   - Sometimes cheaper than separate booking
   - Less flexibility, but worth checking

3. **Credit Card Benefits:**
   - Some cards include car hire insurance (check yours)
   - Travel insurance included? (check)
   - Foreign transaction fees? (use fee-free card)

4. **Accommodation Breakfast:**
   - Â£10-20/person/day if not included
   - 11 nights = Â£220-440 total
   - Book places with breakfast included when possible

---

## âœ… FINAL CHECKLIST BEFORE YOU START BOOKING

```
â–¡ Passport valid until October 2026 minimum
â–¡ Credit card with sufficient limit for deposits (Â£1,500+)
â–¡ Travel insurance arranged? (consider)
â–¡ Decided on airport (Manchester recommended)
â–¡ Reviewed all accommodation options in research
â–¡ Understand full insurance is essential for car
â–¡ Budget spreadsheet ready to track spending
â–¡ Email drafted for Agadir gym verification
â–¡ Flight times work for you (not too early/late)
â–¡ Comfortable with total budget (Â£2,800-3,800)
â–¡ Partner agrees with plan and budget
```

---

## ðŸŽ¯ YOUR MISSION: Turn Research Into Reality

**Total Time Investment:**
- **Flights:** 45 minutes (compare + book)
- **Car Hire:** 45 minutes (compare + book)
- **Accommodation:** 2-3 hours (spread over a week)
- **Total:** ~4 hours to book entire trip

**You've got this!** The research is done. Now it's just methodical clicking through the sites, comparing prices, and booking. Take it one step at a time.

**Questions?** Refer back to the research document for specific hotel details, features, and links.

**Bon voyage! ðŸ‡²ðŸ‡¦**

---

