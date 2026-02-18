# Updated Master Guide - What's Changed

**Document:** roadtrip-itinerary-master-guide-v2.md  
**Date:** February 12, 2026  
**Changes:** Added comprehensive data-gathering methodology with preliminary investigation phase

---

## 🎯 KEY IMPROVEMENTS

### 1. **PHASE 1: Preliminary Investigation (NEW)**

**What It Is:**
Before Claude starts ANY research, it must first investigate what data sources are currently available. This accounts for the fact that APIs close, websites block scrapers, and access methods change over time.

**How It Works:**
```
Step 1: Test current access to flight aggregators
- Try fetching Skyscanner pages
- Try Google Flights, KAYAK, etc.
- Document what works and what doesn't

Step 2: Search for API availability
- "Skyscanner API public access 2026"
- "flight price API free 2026"
- Check if anything new has opened up

Step 3: Test accommodation sites
- Try Booking.com, KAYAK, Hotels.com
- Check direct hotel websites
- Document data quality (features only? pricing too?)

Step 4: Test car hire sites
- Try Rentalcars.com, direct sites
- Check for API access

Step 5: Create "Data Access Status Report"
- What works RIGHT NOW
- What data quality we can get
- What our limitations are
- Recommended approach based on findings
```

**Why This Matters:**
Our February 2026 testing showed:
- ✅ Skyscanner pages: WORK (can fetch recent searches)
- ❌ Booking.com: BLOCKED (JavaScript/robot detection)
- ✅ KAYAK hotels: WORK (can extract pricing)
- ❌ Public APIs: NONE AVAILABLE (all require partnerships)

**But these could change!** In 6 months:
- Skyscanner might block us too
- Booking.com might open access
- New free APIs might emerge
- Alternative aggregators might appear

**Therefore:** Claude must TEST first, not assume.

---

### 2. **PHASE 2: Comprehensive Research (IMPROVED)**

**What Changed:**
Much more detailed instructions on EXACTLY what information to gather for each category.

#### For Flights:
- Not just "recent prices" but: availability, frequency, airlines, flight times, delays, best days, baggage costs, booking links
- Presented in consistent format for easy comparison
- All practical details (distance from home, parking, on-time performance)

#### For Car Hire:
- Base rate + insurance + fees = TOTAL cost (not just base)
- Specific warnings (ADDCAR scam)
- Discount codes with validity dates
- Deposit requirements, credit card needs

#### For Accommodation:
- **3-4 options per location** across budget tiers
- **Complete information for each:**
  - Exact pricing (or best estimate available)
  - What's included (breakfast? dinner? activities?)
  - Location-specific features (alcohol license for Marrakech, gym for Agadir)
  - Review ratings with context
  - Both direct and aggregator booking links
  - Cancellation policies
- **Presented consistently** so user can compare

---

### 3. **PHASE 3: Budget Summary (NEW)**

**What It Is:**
After gathering all options, Claude creates 3 complete scenarios:

**Scenario 1: Budget Conscious** (£2,800 target)
- Specific choices from the options researched
- Budget tier accommodation mostly
- Total breakdown showing it fits budget

**Scenario 2: Balanced** (£3,200 target)
- Mix of mid-range with one luxury splurge
- Realistic middle ground

**Scenario 3: Comfortable** (£3,600 target)
- Mostly mid-range with luxury elements
- Upper end of budget range

**Plus: Mix & Match Guide**
"Want luxury desert camp? (+£150) Offset by choosing budget in Taroudant (-£100)"

**Why This Helps:**
User can see complete trips at different budget levels, not just individual hotel prices. Makes decision-making much easier.

---

### 4. **PHASE 4: User Booking Strategy Guide (NEW)**

**This is the game-changer.** A complete step-by-step guide that we give TO THE USER at the end of the research.

**It Includes:**

#### A. Timing & Order
- Book flights first, then car hire, then accommodation
- WHY this order (car times depend on flights, etc.)

#### B. Step-by-Step Flight Booking
```
1. Where to go (Skyscanner URL)
2. What to enter (exact dates, airports)
3. How to compare (check Google Flights too)
4. Decision criteria (total cost including bags, times, reviews)
5. Where to book (direct with airline usually cheapest)
6. Time estimate: 45 minutes total
```

#### C. Step-by-Step Car Hire Booking
```
1. Rentalcars.com for comparison (with exact filters to use)
2. Check direct with Europcar
3. Try discount code with Green Motion
4. Critical checks list (insurance, mileage, fuel policy, credit card)
5. Decision criteria
6. Time estimate: 45 minutes total
```

#### D. Step-by-Step Accommodation Booking
```
1. Book confirmed choices first (Kasbah Amazir)
2. Book limited availability next (desert camp)
3. Book everywhere else with FREE CANCELLATION
4. Calculate remaining budget
5. Fine-tune choices based on actual budget
6. Special section: How to verify Agadir gym has free weights BEFORE booking
7. Time estimate: 2-3 hours spread over a week
```

#### E. Budget Tracking Spreadsheet Template
Shows user how to track estimated vs. actual costs as they book.

#### F. Common Mistakes to Avoid
- Forgetting baggage costs
- Not getting full car insurance
- Not verifying gym equipment
- Booking non-refundable when unsure

#### G. Booking Timeline
When to do each step (flights today, car hire within 48hrs, etc.)

#### H. Essential Websites List
All the booking URLs in one place

#### I. Money-Saving Tips
- Book direct with hotels (10-15% cheaper)
- Check credit card benefits
- Consider breakfast included (saves £220-440 total)

#### J. Final Checklist
Everything to verify before starting to book.

---

## 🎯 HOW TO USE THIS GUIDE

### For Claude:

**Step 1:** When asked to research Morocco trip (or any roadtrip):
```
1. Read roadtrip-itinerary-master-guide-v2.md
2. Start with PHASE 1: Preliminary Investigation
3. Test current data access methods
4. Document findings
5. Proceed to PHASE 2 with best available methods
6. Create PHASE 3 budget scenarios
7. Provide user with PHASE 4 booking guide
```

**Step 2:** Use the detailed templates for presenting information:
- Flights: Use the "Option 1: Manchester" format
- Car Hire: Use the "Recommended: Hertz/Budget" format
- Accommodation: Use the "LUXURY: Riad Kheirredine" format

**Step 3:** Don't just dump data - structure it for DECISION-MAKING:
- Group by budget tier
- Show total costs, not just per-night
- Include all practical details
- Provide clear booking links

### For Users (Phil & Steph):

**You get TWO documents at the end:**

**Document 1: Research Results**
- All flight options with recent pricing
- All car hire options with warnings
- 3-4 accommodation options per location across budget tiers
- Complete details for each (features, pricing, links)
- 3 budget scenarios (budget/balanced/comfortable)

**Document 2: Your Booking Strategy Guide**
- Exact steps to check live prices (30-60 mins)
- Exact steps to book everything (4 hours total)
- Common mistakes to avoid
- Timeline of when to do what
- Money-saving tips
- Final checklist

---

## 📊 EXAMPLE OUTPUT STRUCTURE

After Claude completes research, user receives:

```
📄 MOROCCO-TRIP-RESEARCH-RESULTS.md
├─ Data Access Status Report
│  └─ What worked, what didn't, our limitations
├─ ✈️ FLIGHTS (All UK Airports)
│  ├─ Option 1: Manchester (RECOMMENDED)
│  ├─ Option 2: Birmingham
│  └─ Option 3: Luton
├─ 🚗 CAR HIRE
│  ├─ Recommended: International Brands
│  ├─ Alternative: Green Motion
│  └─ ⚠️ AVOID: ADDCAR (scam warnings)
├─ 🏨 ACCOMMODATION
│  ├─ Marrakech (2 nights)
│  │  ├─ Luxury: Riad Kheirredine [full details]
│  │  ├─ Mid: Riad Brummell [full details]
│  │  └─ Budget: Dar Darma [full details]
│  ├─ Todra Gorge (2 nights)
│  │  └─ Confirmed: Kasbah Amazir [full details]
│  ├─ Merzouga Desert (1 night)
│  │  ├─ Luxury: Desert Luxury Camp [full details]
│  │  └─ Mid: Tiziri Camp [full details]
│  ├─ Agdz (2 nights)
│  │  ├─ Mid: Kasbah Azul [full details]
│  │  └─ Budget: Lodge Hara [full details]
│  ├─ Taroudant (2 nights)
│  │  └─ [3-4 options across tiers]
│  └─ Agadir (3 nights - GYM REQUIRED)
│     ├─ Agadir Beach Club [verified gym details]
│     └─ Robinson Agadir [gym details]
└─ 💰 BUDGET SCENARIOS
   ├─ Scenario 1: Budget (£2,800)
   ├─ Scenario 2: Balanced (£3,200)
   └─ Scenario 3: Comfortable (£3,600)

📄 YOUR-BOOKING-STRATEGY-GUIDE.md
├─ ⏰ Timing & Order
├─ ✈️ How to Book Flights (Step-by-step)
├─ 🚗 How to Book Car Hire (Step-by-step)
├─ 🏨 How to Book Accommodation (Step-by-step)
├─ 📊 Budget Tracking Template
├─ 🚨 Common Mistakes to Avoid
├─ ⏰ Booking Timeline
├─ 🔗 Essential Websites
├─ 💡 Money-Saving Tips
└─ ✅ Final Checklist
```

---

## ✅ QUALITY STANDARDS

**Every piece of information must include:**

1. **Source transparency:**
   - "From Skyscanner search results (Feb 12, 2026)"
   - "KAYAK pricing: $211/night"
   - "Cannot access live Booking.com prices (blocked)"

2. **Limitations clearly stated:**
   - "Recent searches only, not your exact dates"
   - "Estimated based on similar March 2026 dates"
   - "You'll need to verify live prices"

3. **Actionable format:**
   - Not: "Hotels range from budget to luxury"
   - But: "Budget: Dar Darma £90/night | Mid: Riad Brummell £110/night | Luxury: Riad Kheirredine £160/night"

4. **Complete for decision-making:**
   - Not just price, but what's included
   - Not just features, but booking links
   - Not just options, but recommendations with reasoning

---

## 🔄 VERSION HISTORY

**v1.0** (Original guide)
- Generic roadtrip planning methodology
- No specific data-gathering instructions
- Assumed Claude could access whatever needed

**v2.0** (This version)
- ✅ Preliminary investigation phase added
- ✅ Detailed data-gathering templates
- ✅ Budget scenario creation
- ✅ Complete user booking strategy guide
- ✅ Accounts for changing data access methods
- ✅ Much more actionable and specific

---

**This guide transforms Claude from "here's some information" to "here's everything you need to make decisions and book your trip."**

The user goes from research paralysis to clear action steps.

