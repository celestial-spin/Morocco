# Morocco Road Trip - Complete Research & Booking Guide

**Master Planning Document | Version 3.0 | February 2026**

*This guide provides Claude with a comprehensive methodology for researching travel options when direct API access is unavailable. It includes preliminary investigation procedures, data gathering strategies, and a final user booking guide.*

---

## 🎯 MISSION STATEMENT

**Primary Goal:** Provide Phil & Steph with the maximum possible information to select and book a Morocco trip within their £2,800-3,800 budget.

**The Challenge:** Most travel platforms don't offer public APIs and block automated access. Claude must work within these constraints to gather the best available data.

**Trip Parameters:**
- **Duration:** 11 nights (March 31 - April 11, 2026)
- **Travelers:** 2 people (Phil & Steph)
- **Budget:** £2,800 - £3,800 total (all costs)
- **Style:** Self-drive with mix of accommodation tiers
- **Priorities:** Nature-focused, recovery days, authentic experiences

---

## 📋 THE THREE-PHASE APPROACH

### Phase 1: PRELIMINARY INVESTIGATION
Determine what data sources and methods work RIGHT NOW (methods change over time)

### Phase 2: COMPREHENSIVE DATA GATHERING  
Extract maximum information using all working methods

### Phase 3: USER BOOKING GUIDE
Provide step-by-step instructions for Phil to get live prices and book

---

## 🔍 PHASE 1: PRELIMINARY INVESTIGATION

**Critical Principle:** Never assume a data source works. Test everything first.

### 1.1 Test Flight Data Access

**Objective:** Find which flight aggregators provide accessible pricing data

```bash
# Test Sequence:

1. SKYSCANNER
   web_search: "Skyscanner Manchester Marrakech March April 2026"
   → Get URL from results
   → web_fetch: [URL from search results]
   → Check: Can we parse HTML? Are prices visible?
   → Result: [DOCUMENT: Working/Blocked/Partial]

2. GOOGLE FLIGHTS
   web_search: "Google Flights Manchester Marrakech"
   → Try fetching the URL
   → Check: Accessible data?
   
3. KAYAK
   web_search: "Kayak Manchester Marrakech flights"
   → Try fetching
   
4. MOMONDO / CHEAPFLIGHTS
   → Same process

5. API ACCESS CHECK
   web_search: "Skyscanner API public access 2026"
   web_search: "free flight API 2026"
   → Check: New APIs? Partnership programs?
```

**Document Findings:**
```markdown
### Flight Data Access Report (February 12, 2026)

**WORKING SOURCES:**
- Skyscanner: ✅ Can fetch route pages, shows recent searches (4-day window)
  - Data available: Price ranges, airlines, general date ranges
  - Limitation: Not live pricing for specific dates
  - Example: £39-85 range visible for March/April

**BLOCKED SOURCES:**
- [List any blocked sites]

**API STATUS:**
- Skyscanner API: Requires partnership (not public)
- [Other findings]

**BEST METHOD FOR USER:**
- [Recommendation based on findings]
```

### 1.2 Test Accommodation Data Access

```bash
# Test Sequence:

1. BOOKING.COM
   web_search: "[Hotel Name] Marrakech booking.com"
   → Get hotel URL
   → web_fetch: [Hotel page URL]
   → Check: Can we see prices? Room details?
   → Result: [DOCUMENT]

2. KAYAK HOTELS
   web_search: "[Hotel Name] Kayak price"
   → Try fetching
   → Check: Price data accessible?

3. HOTELS.COM / EXPEDIA / TRAVELOCITY
   → Same process for each

4. DIRECT HOTEL WEBSITES
   web_search: "[Hotel Name] official website"
   → Fetch direct site
   → Check: Pricing visible? Booking available?

5. API CHECK
   web_search: "Booking.com API public 2026"
   web_search: "hotel API free access 2026"
```

**Document Findings:**
```markdown
### Accommodation Data Access Report (February 12, 2026)

**WORKING SOURCES:**
- KAYAK: ✅ Partial (shows some pricing in search results)
- Direct hotel websites: ✅ Most work, show packages/rates
- Booking.com: ❌ Blocked (JavaScript check)

**DATA AVAILABLE:**
- Price ranges (approximate)
- Room features and descriptions
- Direct booking links

**LIMITATION:**
- Cannot get live availability for specific dates
- Prices shown may not be current

**BEST METHOD FOR USER:**
- Use aggregator links we provide
- Check multiple sources for each hotel
```

### 1.3 Test Car Hire Data Access

```bash
# Test Sequence:

1. RENTAL AGGREGATORS
   web_search: "Rentalcars.com Marrakech airport"
   web_search: "Kayak car rental Marrakech"
   → Try fetching
   
2. DIRECT COMPANIES
   web_search: "Hertz Marrakech airport car rental"
   web_search: "Europcar Morocco"
   web_search: "Budget Marrakech"
   → Check: Can we access pages? See rates?

3. API CHECK
   web_search: "car rental API public free 2026"
```

**Document Findings:**
```markdown
### Car Hire Data Access Report (February 12, 2026)

**WORKING SOURCES:**
- [List what works]

**DATA AVAILABLE:**
- [What can we extract]

**SCAM WARNINGS:**
- ADDCAR: Known scam (document evidence found)

**BEST METHOD FOR USER:**
- [Recommendation]
```

### 1.4 Create Master Data Access Summary

After completing all tests, create a single reference document:

```markdown
## CURRENT DATA ACCESS STATUS (Updated: February 12, 2026)

### What Claude CAN Provide:
1. Flights: Recent price ranges, airlines, booking links
2. Accommodation: Hotel shortlist with features, approximate pricing, booking links  
3. Car Hire: Company comparison, price ranges, warnings, booking links

### What Claude CANNOT Provide:
1. Live pricing for user's exact dates (March 31 - April 11)
2. Real-time availability
3. Exact final costs (fees, taxes vary)

### Why This Matters:
User will need to spend 30-60 minutes checking live prices using the links and information provided.

### Strategy:
Claude provides comprehensive research + booking guide
User executes final price checks and booking
```

---

## 📊 PHASE 2: COMPREHENSIVE DATA GATHERING

**Now that we know what works, extract MAXIMUM information from each source**

### 2.1 FLIGHTS - Comprehensive Research

**Goal:** Give user enough info to make informed decisions about which airport and airline to use

#### Step 2.1.1: Search All Airport Options

```bash
# For each viable airport (Manchester, Birmingham, Luton):

1. Recent Price Data
   web_search: "[Airport] Marrakech flights March April 2026"
   → Extract: Price ranges, airlines operating route
   
2. Route Details  
   web_fetch: [Skyscanner route page if accessible]
   → Extract: 
     - Flight frequency (flights per week)
     - Direct vs connection
     - Flight duration
     - Airlines operating
     - Seasonal pricing trends
     
3. Airline Quality
   web_search: "[Airline] reliability delays 2026"
   → Check: Known issues? Delay statistics?
```

#### Step 2.1.2: Create Flight Comparison Table

**Deliverable Format:**
```markdown
## FLIGHT OPTIONS (2 people return, March 31 - April 11, 2026)

### Option 1: Manchester (MAN) → Marrakech (RAK)
**Recent Price Range:** £39-85 per person = **£78-170 for 2 people**

**Airlines Operating:**
- easyJet: Daily direct (3h 40m)
- Ryanair: Daily direct (3h 40m)  
- TUI: Weekly direct
- Jet2: Weekly direct

**Pros:**
- Most flight options (14+ per week)
- Maximum flexibility for date changes
- Frequent departures reduce stress if you miss one

**Cons:**
- 90min drive from Nottingham
- Higher parking costs

**Baggage Costs:**
- Checked bag: £15-35 each way per bag
- Estimate: +£60-140 for 2 bags return

**Booking Links:**
- Skyscanner: [specific URL]
- Direct easyJet: [URL]
- Direct Ryanair: [URL]

**ESTIMATED TOTAL: £138-310 (flights + bags for 2 people)**

---

### Option 2: Birmingham (BHX) → Marrakech
[Same detailed breakdown]

---

### Option 3: Luton (LTN) → Marrakech  
[Same detailed breakdown]

---

### RECOMMENDATION:
**Primary:** Manchester (most flexibility, best for March 31 departure)
**Backup:** Birmingham (if significantly cheaper when you check live)
**Avoid:** Luton (only 2x/week, furthest from Nottingham)
```

#### Step 2.1.3: Add Booking Strategy

```markdown
### HOW TO BOOK FLIGHTS:

**Best Time to Book:** NOW (6 weeks ahead is optimal window)

**Process:**
1. Check all three links above on same day
2. Use private/incognito browser (avoid price tracking)
3. Compare total cost including bags
4. Monday departures often 10-20% cheaper than weekends
5. Book directly with airline (not aggregator) for easier changes

**Price Alerts:**
Set up at: [Skyscanner alert link], [Google Flights alert link]
```

---

### 2.2 CAR HIRE - Comprehensive Research

#### Step 2.2.1: Company Comparison Research

```bash
# Research each major company:

1. Safety & Reputation
   web_search: "Hertz Marrakech airport reviews 2025 2026"
   web_search: "Budget Morocco car rental reviews"
   web_search: "Europcar Marrakech scam complaints"
   → Document: Reputation, known issues, ratings

2. Pricing Structure
   web_search: "Marrakech car rental 10 days full insurance cost"
   → Extract: Typical price ranges for similar rentals
   
3. Insurance Requirements
   web_search: "Morocco car rental insurance requirements CDW"
   → Document: What's mandatory, what's recommended
   
4. Scam Warnings
   web_search: "Morocco car rental scams ADDCAR"
   → Document: Companies to avoid, common tactics
```

#### Step 2.2.2: Create Car Hire Guide

**Deliverable Format:**
```markdown
## CAR HIRE (10 days: March 31 - April 11, 2026)

### Price Range Estimate: £350-550 (with full insurance)

---

### ✅ RECOMMENDED COMPANIES

**1. HERTZ**
- **Reputation:** 6.5/10 average rating
- **Insurance:** CDW + Theft Protection included, recommend Super CDW
- **Excess:** £1,200-1,500 standard, £0 with Super CDW
- **Price Estimate:** £400-500 (10 days, compact car, full insurance)
- **Pros:** International brand, reliable, airport desk
- **Cons:** Can be pricier than locals
- **Booking:** [Direct Hertz link], [Via Rentalcars.com]

**2. EUROPCAR**
- **Reputation:** 7.0/10 average rating
- **Similar structure to Hertz**
- [Full details]

**3. BUDGET**
- [Full details]

**4. GREEN MOTION**
- **Discount Code:** MARRAKECH15 (15% off, valid until March 30, 2026)
- **Reputation:** 6.6/10 (mixed reviews)
- **Warning:** Some reports of "card not working" scam to upsell insurance
- **Price Estimate:** £300-400 with discount
- **Use if:** You're comfortable being firm about pre-booked insurance
- [Full details]

---

### ❌ COMPANIES TO AVOID

**ADDCAR - CONFIRMED SCAM**
Evidence gathered:
- No actual airport location (shed in parking lot)
- Cancels bookings if >2hrs late (no refund)
- Wrong vehicles delivered (booked SUV, get sedan)
- Expired insurance papers
- Aggressive upselling tactics

**DO NOT BOOK** regardless of price.

---

### 🛡️ INSURANCE REQUIREMENTS

**What You MUST Have:**
1. **CDW (Collision Damage Waiver):** Mandatory, reduces excess
2. **Theft Protection:** Mandatory

**Standard Excess with Basic CDW:** £1,200-£3,000

**What You SHOULD Add:**
3. **Super CDW / Zero Excess:** Reduces excess to £0
   - **Critical:** Pre-book online, cheaper than desk
   - Cost: Usually £8-15/day extra = £80-150 total
   - **Worth it:** Morocco driving chaotic, reduces risk

**NEVER:**
- Accept basic CDW only
- Buy insurance at desk (2-3x more expensive)
- Skip photographing all damage before leaving

---

### 📝 BOOKING PROCESS

**Step-by-step:**
1. **Search on aggregator first:** Use Rentalcars.com or Kayak
2. **Compare 3-4 companies:** Note prices with FULL insurance
3. **Check direct websites:** Sometimes cheaper booking direct
4. **Pre-book Super CDW/Zero Excess:** Do this online, not at desk
5. **Read insurance terms:** Know what excess remains
6. **Save confirmation:** Print or download, bring to desk

**At Pickup:**
1. **Inspect car thoroughly:** Photo every scratch, dent, mark
2. **Video walk-around:** With rental agent visible
3. **Check insurance papers:** Ensure not expired, correct coverage
4. **Refuse any upsells:** You already have full coverage
5. **Fuel policy:** Most are "full to full" - note fuel level

**Morocco Driving Essentials:**
- Drive on RIGHT
- Valid UK license + International Driving Permit (get from Post Office, ~£5.50)
- Never go below 1/4 tank (rural stations sparse)
- Speed cameras common, high fines
- City traffic chaotic (horns = communication, not aggression)

---

### BOOKING LINKS

**Comparison Sites:**
- Rentalcars.com: [search URL for Marrakech Airport, March 31-April 11]
- Kayak: [search URL]

**Direct Companies:**
- Hertz Morocco: [URL]
- Europcar Morocco: [URL]  
- Budget Morocco: [URL]
- Green Motion (with code): [URL]

**ESTIMATED BUDGET ALLOCATION: £400-500** (mid-range with full insurance)
```

---

### 2.3 ACCOMMODATION - Comprehensive Research

**This is the most time-intensive section - do it properly**

#### Step 2.3.1: Research Each Location Systematically

**For EACH location (Marrakech, Todra Gorge, Merzouga, Agdz, Taroudant, Agadir):**

```bash
# Research Process:

1. IDENTIFY TOP OPTIONS (3-4 per location)
   web_search: "best [location] hotels riad [budget tier] Morocco"
   web_search: "[location] accommodation pool terrace 2026"
   → Create shortlist of 3-4 properties per location

2. GATHER DETAILED INFO FOR EACH PROPERTY
   For each property:
   
   a) Basic Details
      web_search: "[Property Name] [Location] official website"
      web_search: "[Property Name] Tripadvisor reviews"
      
   b) Pricing Research
      web_search: "[Property Name] price per night 2026"
      web_search: "[Property Name] Booking.com"
      web_search: "[Property Name] KAYAK price"
      → Extract: Price ranges, what's included
      
   c) Key Features
      web_search: "[Property Name] pool alcohol license breakfast"
      → Document: All relevant features
      
   d) Reviews & Warnings
      web_search: "[Property Name] reviews complaints problems"
      → Check: Any red flags? Consistent issues?
      
   e) Direct Contact
      web_search: "[Property Name] email phone booking"
      → Provide: Direct booking options

3. ORGANIZE FINDINGS
   Create detailed profile for each property
```

#### Step 2.3.2: Property Profile Template

**Use this template for EVERY property researched:**

```markdown
### [PROPERTY NAME] | [Location] | [Budget Tier: Budget/Mid/Upper-Mid/Luxury]

**Price Estimate:** £[low]-[high] per night (based on [source and date])

**What's Included:**
- ✅ Breakfast: [Included/Not included/Optional at £X]
- ✅ Dinner: [Available/Not available/Price if known]
- ✅ Pool: [Yes/No - details if yes]
- ✅ Alcohol: [Licensed bar/Restaurant wine list/None/Unknown]
- ✅ Terrace: [Rooftop/Garden/None]
- ✅ Parking: [Free/Paid £X/Nearby/None]
- ✅ Wifi: [Free/Paid/None]
- ✅ AC: [Yes/No/Some rooms]

**Special Features:**
- [Any unique amenities: hammam, spa, cooking class, etc.]

**Room Types:**
- [List available room categories if known]

**Location Context:**
- Distance to main attractions: [X]
- Distance to restaurants: [X]
- Accessibility: [Easy/Difficult - explain]

**Reviews Summary:**
- Tripadvisor: [Rating]/10 ([X] reviews)
- Booking.com: [Rating]/10 ([X] reviews)
- Google: [Rating]/5 ([X] reviews)
- **Consistent Praise:** [What guests love]
- **Consistent Complaints:** [Any recurring issues]

**Booking Options:**
- **Direct:** [Website URL] - [any direct booking benefits]
- **Booking.com:** [URL]
- **KAYAK:** [URL]
- **Phone:** [Number if available]
- **Email:** [Email if available]

**Notes:**
- [Any important info: minimum stay, adults only, specific policies, etc.]

**Source Quality:** [Where data came from, how recent, reliability]
```

#### Step 2.3.3: Location-Specific Research Priorities

**MARRAKECH (2 nights - arrival splurge):**
- Focus: Riads with pools, rooftop terraces
- Budget: Upper-mid to luxury (£100-180/night)
- **Critical feature:** Alcohol license (rare in Medina)
- Research 4 options across price range

**TODRA GORGE (2 nights):**
- Focus: Kasbahs/auberges with character
- Budget: Mid-range (£40-80/night)  
- **Critical features:** Bar/alcohol, views, good food
- Research 3-4 options

**MERZOUGA DESERT (1 night - luxury camp):**
- Focus: Luxury camps with private bathrooms
- Budget: Luxury (£100-180 per person)
- **Critical features:** En-suite, hot water, quality experience
- **Warning:** Verify exact camp name (scams exist)
- Research 3-4 camps

**AGDZ (2 nights - oasis):**
- Focus: Small lodges/kasbahs with pools
- Budget: Mid to upper-mid (£60-110/night)
- **Critical features:** Pool, garden/oasis, excellent food
- Research 3-4 options

**TAROUDANT (2 nights - walled city):**
- Focus: Hotels/riads with pools
- Budget: Mid-range (£50-100/night)
- **Critical features:** Pool (hot in this region), walkable to walls
- Research 3-4 options

**AGADIR (2-3 nights - beach recovery):**
- Focus: Beachfront hotels with gyms
- Budget: Mid to upper-mid (£100-150/night)
- **CRITICAL FEATURE:** Gym with free weights/dumbbells (Phil's requirement)
- **Must verify:** Actually has dumbbells, not just cardio
- Research 3-4 options, verify gym facilities

#### Step 2.3.4: Create Comprehensive Accommodation Guide

**Deliverable Format:**

```markdown
## ACCOMMODATION OPTIONS (11 nights total)

### Budget Allocation Strategies

**Strategy A: Balanced Mix** (~£1,400 total)
- Marrakech: 2 nights × £140 = £280 (luxury)
- Todra: 2 nights × £50 = £100 (budget-mid)
- Merzouga: 1 night × £140 pp = £280 (luxury camp)
- Agdz: 2 nights × £95 = £190 (upper-mid)
- Taroudant: 2 nights × £70 = £140 (mid)
- Agadir: 2 nights × £130 = £260 (upper-mid beach)

**Strategy B: Splurge Smart** (~£1,600 total)
- [Different allocation]

**Strategy C: Value Focus** (~£1,100 total)
- [Budget-conscious allocation]

---

### 📍 MARRAKECH (2 nights: March 31 - April 2)

#### Option 1: Riad Kheirredine ⭐⭐⭐⭐⭐ LUXURY
[Full property profile using template above]

#### Option 2: Riad Brummell ⭐⭐⭐⭐ UPPER-MID
[Full property profile]

#### Option 3: Riad Les Yeux Bleus ⭐⭐⭐⭐ MID
[Full property profile]

#### Option 4: Dar Darma ⭐⭐⭐ BUDGET-MID
[Full property profile]

**Marrakech Summary:**
- **Recommended:** Riad Kheirredine (if budget allows) - #1 in Africa
- **Best Value:** Riad Les Yeux Bleus
- **Budget Pick:** Dar Darma

---

### 📍 TODRA GORGE (2 nights: April 2-4)

[Same format - 3-4 options with full profiles]

**Todra Summary:**
- **Confirmed Choice:** Kasbah Amazir (has bar, great location)
- [Other options]

---

[Continue for each location...]

---

### ACCOMMODATION BOOKING STRATEGY

**Timing:**
- Book NOW for March 31 trip (6 weeks is good timing)
- Most places allow free cancellation 24-48hrs before
- Some may require deposits

**Booking Process:**
1. **Check all options for each location** using links provided
2. **Compare prices** on Booking.com vs direct website
3. **Benefits of direct booking:** Often 10% cheaper, better rooms, perks
4. **Read cancellation policy:** Flexible vs non-refundable
5. **Contact via email:** Can sometimes negotiate, ask questions
6. **Book mix of tiers:** Based on which budget strategy you choose

**Email Template for Direct Booking:**
```
Subject: Accommodation Inquiry - March 31 - April 2, 2026 (2 guests)

Dear [Property Name],

We are planning a stay at your property from [date] to [date] for 2 guests (couple).

Questions:
1. Do you have availability for these dates?
2. What is your best available rate for a [room type]?
3. Is breakfast included?
4. What is your cancellation policy?
5. [Any specific questions: alcohol, parking, etc.]

We are booking multiple properties across Morocco and would love to stay with you.

Many thanks,
Phil & Steph
```

**ESTIMATED ACCOMMODATION TOTAL: £1,100-1,600** (depending on strategy)
```

---

### 2.4 ADDITIONAL COSTS RESEARCH

Don't forget these in the budget!

```bash
# Research:

1. FUEL COSTS
   web_search: "Morocco fuel prices 2026"
   web_search: "Marrakech Agadir drive fuel cost"
   → Estimate: ~1,500km total @ £1.30/L = £150-200

2. ROAD TOLLS
   web_search: "Morocco motorway tolls A7 A3 cost"
   → Estimate: £20-40

3. PARKING
   web_search: "Marrakech medina parking cost"
   → Estimate: £5-10/day when needed

4. FOOD & ACTIVITIES
   Based on user profile (likes nice meals but not extravagant):
   → Estimate: £50-80/day for 2 people = £550-880

5. CONTINGENCY
   → Recommend: £100-200 buffer
```

---

## 📖 PHASE 3: USER BOOKING GUIDE

**This is what Phil uses to actually book the trip**

### 3.1 Create Step-by-Step Booking Checklist

```markdown
# YOUR MOROCCO TRIP BOOKING GUIDE

## ✅ PRE-BOOKING CHECKLIST

**Documents Needed:**
- [ ] Passports (valid for 6+ months after April 11)
- [ ] International Driving Permit (get from Post Office, £5.50)
- [ ] Credit cards with no foreign transaction fees
- [ ] Travel insurance documents

**Timing Strategy:**
- **Book now:** Flights + Car (6 weeks ahead = optimal)
- **Book now:** Accommodation (March 31 is soon, availability limited)
- **Set price alerts:** For flights (in case price drops)

---

## 📅 BOOKING SEQUENCE (Recommended Order)

### STEP 1: BOOK FLIGHTS (Do First - Most Time-Sensitive)

**Why first:** Prices change frequently, availability crucial for your dates

**Process:**
1. Open incognito browser (avoid price tracking cookies)
2. Check ALL THREE airport options using links below:
   - [ ] Manchester to Marrakech: [Skyscanner link], [easyJet link], [Ryanair link]
   - [ ] Birmingham to Marrakech: [Links]
   - [ ] Luton to Marrakech: [Links]

3. Compare TOTAL cost (flights + bags)
4. Choose best option based on: price + convenience + flexibility
5. **Book directly with airline** (not through aggregator)
6. **Add bags during booking** (cheaper than later)
7. **Save confirmation** to secure folder
8. **Add to calendar** with flight numbers

**Target Budget:** £200-350 for 2 people return (flights + bags)

---

### STEP 2: BOOK CAR HIRE (Do Second)

**Why second:** Lock in good rate, ensure availability

**Process:**
1. Go to comparison sites:
   - [ ] Rentalcars.com: [link with dates]
   - [ ] Kayak: [link]

2. Filter for:
   - Pickup: Marrakech Airport
   - Dates: March 31 (arrival time) - April 11 (departure time)
   - Car type: Compact or Economy
   - Transmission: Automatic (recommended) or Manual
   - **Insurance: FULL / Zero excess / Super CDW**

3. Compare top 3 options:
   - [ ] Hertz with full insurance: £____
   - [ ] Europcar with full insurance: £____
   - [ ] Budget with full insurance: £____

4. Check direct website of cheapest option (sometimes cheaper)
   - [ ] Direct website price: £____

5. **CRITICAL:** Verify insurance includes:
   - ✅ CDW (Collision Damage Waiver)
   - ✅ Theft Protection
   - ✅ Zero excess OR Super CDW
   - ✅ Coverage amount adequate

6. Book best option
7. Print confirmation (bring to airport)
8. Note pickup instructions (Marrakech Airport, Terminal 1)

**Target Budget:** £400-500

---

### STEP 3: BOOK ACCOMMODATION (Do Third - Location by Location)

**Why this order:** Flights and car are fixed costs; accommodation has flexibility

**Process for EACH location:**

#### MARRAKECH (2 nights: March 31 - April 2)

1. Check all 4 options I researched:
   - [ ] Riad Kheirredine: [Booking.com link] [Direct website link]
   - [ ] Riad Brummell: [Links]
   - [ ] Riad Les Yeux Bleus: [Links]
   - [ ] Dar Darma: [Links]

2. For each, note:
   - Price for March 31-April 2 (2 nights, 2 guests): £____
   - Breakfast included? Y/N
   - Free cancellation until: [date]
   - Room type available: ________

3. Decision Matrix:
   ```
   Property          | Price  | Value Score | Choice
   ------------------|--------|-------------|--------
   Kheirredine       | £___   | ___/10     | [ ]
   Brummell          | £___   | ___/10     | [ ]
   Les Yeux Bleus    | £___   | ___/10     | [ ]
   Dar Darma         | £___   | ___/10     | [ ]
   ```

4. Book your choice:
   - [ ] Direct website (check first - often 10% cheaper)
   - [ ] OR Booking.com
   - [ ] Save confirmation
   - [ ] Add to calendar
   - [ ] Email property: Arrival time + any special requests

**Repeat this process for:**
- [ ] Todra Gorge (2 nights: April 2-4)
- [ ] Merzouga Desert (1 night: April 4-5)
- [ ] Agdz (2 nights: April 5-7)
- [ ] Taroudant (2 nights: April 7-9)
- [ ] Agadir (2 nights: April 9-11)

**Target Total:** £1,100-1,600 depending on tier choices

---

### STEP 4: BUDGET CHECK

After booking transport + accommodation, calculate total:

```
ITEM                  | BUDGETED  | ACTUAL    | REMAINING
----------------------|-----------|-----------|----------
Flights (2 people)    | £300      | £____     | 
Car hire (10 days)    | £450      | £____     |
Marrakech (2 nights)  | £___      | £____     |
Todra (2 nights)      | £___      | £____     |
Merzouga (1 night)    | £___      | £____     |
Agdz (2 nights)       | £___      | £____     |
Taroudant (2 nights)  | £___      | £____     |
Agadir (2 nights)     | £___      | £____     |
----------------------|-----------|-----------|----------
SUBTOTAL              | £2,100    | £____     | £____
----------------------|-----------|-----------|----------
Fuel                  | £175      |           |
Tolls                 | £30       |           |
Parking               | £50       |           |
Food (11 days)        | £650      |           |
Activities            | £100      |           |
Contingency           | £150      |           |
----------------------|-----------|-----------|----------
TOTAL BUDGET          | £3,255    | £____     | £____
----------------------|-----------|-----------|----------
YOUR BUDGET RANGE     | £2,800-3,800        |
WITHIN BUDGET?        | [ ] YES  [ ] NO     |
```

**If over budget:**
- Swap luxury accommodation for mid-tier options
- Reduce Agadir from 3 to 2 nights
- Choose budget airline with hand luggage only

**If under budget:**
- Upgrade one or two accommodations
- Add activities (hot air balloon, cooking class, etc.)
- Extend Agadir for extra beach time

---

### STEP 5: PREPARE FOR TRAVEL

**2 Weeks Before:**
- [ ] Get International Driving Permit from Post Office
- [ ] Inform credit card companies (travel to Morocco March 31-April 11)
- [ ] Download offline maps (Google Maps / Maps.me)
- [ ] Research restaurants at each location
- [ ] Book any activities (hot air balloon, etc.)
- [ ] Check weather forecast
- [ ] Pack according to forecast

**1 Week Before:**
- [ ] Check in online for flights (if available)
- [ ] Print all confirmations (flight, car, hotels)
- [ ] Create digital backup folder with all confirmations
- [ ] Organize by date
- [ ] Screenshot car rental confirmation
- [ ] Note hotel addresses + phone numbers
- [ ] Download Google Translate (French/Arabic)

**Day Before:**
- [ ] Charge all devices
- [ ] Pack printouts in hand luggage
- [ ] Set airport parking if driving
- [ ] Confirm ride to airport if not driving

---

## 💡 MONEY-SAVING TIPS

1. **Direct Booking:** Often 10% cheaper than aggregators for hotels
2. **Lunch vs Dinner:** Eat main meal at lunch (cheaper, same quality)
3. **Local Restaurants:** Ask hotel staff for recommendations
4. **Fuel Strategy:** Fill up in cities (cheaper than rural areas)
5. **Cash:** Get dirhams from ATMs (better rate than exchange booths)
6. **Haggling:** Expected in souks, not in restaurants
7. **Water:** Buy large bottles at shops, not hotel minibar
8. **SIM Card:** Get local SIM at airport (data much cheaper than roaming)

---

## 📞 EMERGENCY CONTACTS

**Save these in phone:**
- UK Embassy Rabat: +212 537 63 33 33
- Police (Morocco): 19
- Ambulance: 15
- Car rental company 24hr: [from booking]
- Travel insurance emergency: [from policy]
- Credit card lost/stolen: [from card]

---

## 🗺️ NAVIGATION TIPS

**Apps to Download:**
- Maps.me (offline maps - essential for remote areas)
- Google Maps (good for cities)
- Google Translate (camera function for menus)
- XE Currency (exchange rates)

**Driving Tips:**
- Download offline maps for entire route
- Save each hotel address in Google Maps favorites
- Pin restaurants / gas stations along route
- Check distance markers on highway (toll costs)

---

## ✅ FINAL CHECKLIST

**Booked:**
- [ ] Flights (Manchester/Birmingham/Luton → Marrakech)
- [ ] Car hire (Marrakech Airport, full insurance)
- [ ] Marrakech accommodation (2 nights)
- [ ] Todra Gorge accommodation (2 nights)
- [ ] Merzouga camp (1 night)
- [ ] Agdz accommodation (2 nights)
- [ ] Taroudant accommodation (2 nights)
- [ ] Agadir accommodation (2 nights)

**Obtained:**
- [ ] International Driving Permit
- [ ] Travel insurance
- [ ] Local currency plan (ATM on arrival)

**Prepared:**
- [ ] All confirmations printed
- [ ] Offline maps downloaded
- [ ] Credit cards notified
- [ ] Emergency contacts saved
- [ ] Packing list completed

---

**YOU'RE READY FOR MOROCCO! 🇲🇦**

```

---

## 🎓 APPENDIX: TROUBLESHOOTING

### If Flights Too Expensive

**Alternative strategies:**
1. Check flying day before/after (March 30 or April 1 departure)
2. Consider: Manchester → Agadir instead (then drive to Marrakech)
3. Check: Gatwick or other London airports if willing to drive further
4. Look at: Flight + hotel packages (sometimes cheaper)

### If Car Hire Too Expensive

**Alternative strategies:**
1. Skip Europcar/Hertz, try Budget or Green Motion with discount code
2. Reduce car type to smallest category
3. Manual transmission (cheaper than automatic)
4. Check: Picking up from city center vs airport
5. **DO NOT:** Skip full insurance to save money (false economy)

### If Accommodation Unavailable

**Backup plan:**
1. Use filters: Set price range, sort by rating
2. Look for: "Free cancellation" options (book now, decide later)
3. Check: Airbnb for any locations (not in guide but valid option)
4. Contact properties directly: Sometimes have availability not shown online
5. Be flexible: Swap location order if needed

### If Total Over Budget

**Cut costs here (in order):**
1. Reduce Agadir from 3 → 2 nights (saves £100-150)
2. Swap one luxury stay for mid-tier (saves £60-100)
3. Choose budget airline with hand luggage only (saves £60-140)
4. Skip desert camp, use hotel in Merzouga (saves £100-200)
5. Pack lunches from breakfast buffets (saves £100-150)

**DON'T cut:**
- Car insurance (false economy, high risk)
- Fuel budget (remote areas, safety issue)
- Contingency fund (you'll need it)

---

## 📚 FURTHER RESOURCES

**Morocco Travel:**
- Lonely Planet Morocco: [Link]
- Visit Morocco official: [Link]
- Morocco travel forums: [Links]

**Route Planning:**
- Google Maps: [Morocco map link]
- Rome2rio: [Morocco travel options]

**Reviews:**
- Tripadvisor Morocco: [Link]
- Booking.com Morocco: [Link]

**Driving:**
- Morocco road rules: [Official link]
- Toll calculator: [If available]

---

**END OF GUIDE**

*This guide will be updated as data access methods change. Last updated: February 12, 2026*
