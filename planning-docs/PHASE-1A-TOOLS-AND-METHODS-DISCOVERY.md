# PHASE 1A: FLIGHT VERIFICATION TOOLS & METHODS DISCOVERY

**Purpose:** Discover expert methods and tools for verifying ACTUAL flight availability on SPECIFIC dates  
**Critical:** This phase MUST complete BEFORE making any flight recommendations  
**Created:** 2026-02-13 (AFTER failure on Morocco trip)  
**Version:** 1.0

---

## 🔴 WHY THIS PHASE EXISTS

**The Problem:** 
- Generic sources show "Airline X flies route Y"  
- Schedule databases show "Flight operates Sundays"
- BUT this doesn't mean the flight exists on YOUR specific date

**The Failure:**
- I recommended Jet2 Sunday March 30, 2026
- Based on "Jet2 operates Manchester-Marrakech on Sundays"
- User's screenshot showed: NO Sunday flights in March 2026
- Only Monday and Friday flights actually exist

**The Lesson:**
**"Route exists" ≠ "Flight exists on YOUR date"**

---

## 🎯 PHASE 1A OBJECTIVES

**Must Discover:**
1. ✅ Tools that show ACTUAL calendar availability
2. ✅ Methods to verify specific dates have flights
3. ✅ Ways to check real-time pricing
4. ✅ Techniques to confirm flight numbers exist
5. ✅ Approaches to validate airline schedules

**Must Answer:**
- Which tools can Claude use directly vs require user?
- What are the limitations of each tool?
- How to verify when tools can't access calendars?
- What's the verification workflow?

---

## 📊 DISCOVERED TOOLS & METHODS

### **1. GOOGLE FLIGHTS (Primary Recommendation)**

**What It Does:**
- Shows ACTUAL calendar of available flights
- Displays real prices for specific dates
- Calendar view with green = cheapest days
- Date grid shows combinations
- Price graph shows trends

**Strengths:**
- ✅ Visual calendar with actual availability
- ✅ Shows which days have NO flights (blank)
- ✅ Real-time pricing
- ✅ Can see up to 12 months ahead
- ✅ Free, no login required
- ✅ Mobile and desktop

**Limitations:**
- ❌ Can't always access via web_fetch (dynamic content)
- ❌ Prices are estimates (may vary slightly)
- ❌ Shows aggregated results (may miss some airlines)

**How Claude Should Use:**
```
1. Direct user to: google.com/flights
2. User enters: Origin, Destination
3. User clicks calendar icon
4. User screenshots calendar showing:
   - Which dates have flights (prices shown)
   - Which dates have NO flights (blank)
   - Actual prices for their dates
5. User shares screenshot with Claude
6. Claude analyzes ACTUAL availability
```

**Best For:**
- Verifying which days have flights
- Checking if specific date exists
- Comparing prices across dates
- Finding cheapest days

---

### **2. ITA MATRIX (Advanced Verification)**

**What It Does:**
- Most powerful flight search engine
- Backend for Google Flights, Kayak, Orbitz
- Calendar of lowest fares
- Specific flight number search
- Fare class verification

**Strengths:**
- ✅ "Calendar of lowest fares" feature
- ✅ Can search specific flight numbers
- ✅ Shows fare classes (economy/business)
- ✅ Extension codes for complex searches
- ✅ Can verify fuel surcharges/taxes
- ✅ More detailed than Google Flights

**Limitations:**
- ❌ Cannot book through it (research only)
- ❌ More complex interface
- ❌ Claude cannot access directly
- ❌ Requires user to check

**How To Use:**
```
1. Go to: matrix.itasoftware.com
2. Enter origin, destination
3. Select "See calendar of lowest fares"
4. Set departure date (shows month ahead)
5. For round-trip: set trip length range
6. Results show which dates have flights
7. Can filter by specific airlines
```

**Advanced Features:**
- Routing codes: `UA` (United only), `~AA` (exclude American)
- Extension codes: `minconnect 20:00` (overnight layover)
- Aircraft search: `aircraft t:787` (specific plane)
- Fare class: `F BC=M` (specific booking class)

**Best For:**
- Complex itineraries
- Specific flight number verification
- Award travel planning
- Checking fare classes

**After Finding Flight:**
- Use BookWithMatrix.com to book
- Or manually recreate on airline website
- Or use travel agent with ITA details

---

### **3. SKYSCANNER**

**What It Does:**
- Flight comparison across airlines
- "Whole month" and "Cheapest month" views
- Price alerts
- Flexible date searching

**Strengths:**
- ✅ Month view shows cheapest dates
- ✅ Can search "whole year" for best month
- ✅ Price alerts (track specific routes)
- ✅ Shows multiple airlines
- ✅ Direct booking links

**Limitations:**
- ❌ Calendar not as detailed as Google Flights
- ❌ Dynamic content hard for Claude to fetch
- ❌ Sometimes shows cached prices

**How To Use:**
```
1. Go to: skyscanner.com
2. Enter route
3. Click "Whole month" or "Cheapest month"
4. See grid of prices by date
5. Blank cells = no flights that date
```

**Best For:**
- Finding cheapest month overall
- Comparing across full year
- Setting price alerts
- Finding alternative airports

---

### **4. EXPERTFLYER**

**What It Does:**
- Real-time award seat availability
- Upgrade seat tracking
- Flight alerts
- Detailed seat maps

**Strengths:**
- ✅ Shows real-time availability
- ✅ Award seat tracking
- ✅ Set alerts for specific flights
- ✅ Detailed fare class info
- ✅ Seat map visualization

**Limitations:**
- ❌ Requires paid subscription (~$10/month)
- ❌ More for award travel/frequent flyers
- ❌ Not needed for basic booking

**Best For:**
- Award travel
- Upgrade availability
- Frequent flyer planning
- Monitoring specific flights

---

### **5. AIRLINE DIRECT WEBSITES**

**What It Does:**
- Official airline booking calendar
- Actual inventory in real-time
- Most accurate for that airline

**Strengths:**
- ✅ Shows airline's ACTUAL calendar
- ✅ Real-time availability
- ✅ Official pricing
- ✅ Can book directly
- ✅ Most authoritative source

**Limitations:**
- ❌ Dynamic calendars (Claude can't fetch)
- ❌ Must check each airline separately
- ❌ Some only show 6-11 months ahead

**How Claude Should Use:**
```
For EACH recommended airline:
1. Direct user to airline website
2. User navigates to flight booking
3. User enters route
4. User opens calendar view
5. User screenshots the calendar
6. User shares what they see

Claude then analyzes actual availability
```

**Examples:**
- Jet2: jet2.com/flights
- easyJet: easyjet.com/en/flights
- Ryanair: ryanair.com/gb/en
- British Airways: ba.com

**Best For:**
- Final verification before booking
- Checking specific airline schedule
- Seeing ALL available dates for that airline
- Confirming exact departure times

---

### **6. FLIGHTAWARE / FLIGHTSTATS**

**What It Does:**
- Track existing flights in real-time
- Historical flight data
- On-time performance

**Strengths:**
- ✅ Shows if flight number exists
- ✅ Historical on-time data
- ✅ Real-time tracking

**Limitations:**
- ❌ Only tracks flights TODAY
- ❌ Not for future booking
- ❌ Doesn't show availability

**Best For:**
- Tracking flight after booking
- Checking on-time performance
- Verifying flight number exists
- Real-time status

**NOT For:**
- Checking future availability
- Booking flights
- Price comparison

---

## 🔧 VERIFICATION WORKFLOW (Claude + User Partnership)

### **THE CRITICAL PRINCIPLE:**

**Claude's tools CANNOT access dynamic booking calendars.**

Therefore, flight verification REQUIRES partnership with user:

**Claude's Role:**
1. Research which airlines fly the route
2. Discover general schedules (days of week)
3. Find historical pricing patterns
4. Identify best booking tools
5. Direct user to specific verification steps

**User's Role:**
1. Access airline/aggregator calendars
2. Screenshot actual availability
3. Share what they see with Claude
4. Verify specific dates exist
5. Confirm actual prices

---

### **STEP-BY-STEP VERIFICATION PROCESS:**

**Step 1: Claude Researches Route (Phase 1A)**
```
Claude discovers:
- Which airlines fly Manchester → Marrakech
- General frequency (daily, 3x/week, etc.)
- Typical operating days (Mon/Wed/Fri, etc.)
- Historical price ranges
- Best search tools
```

**Step 2: Claude Directs User to Verification (Phase 1B)**
```
Claude says:
"I've found that easyJet, Ryanair, and Jet2 fly this route.
Now I need YOU to verify which actually have flights on YOUR dates.

Please:
1. Go to Google Flights: google.com/flights
2. Enter: Manchester (MAN) → Marrakech (RAK)
3. Click the calendar icon
4. Screenshot March 2026 calendar
5. Share what you see

This shows which dates have ACTUAL flights."
```

**Step 3: User Provides Screenshot**
```
User shares screenshot showing:
- March 2: easyJet £44
- March 3: Jet2 £3 (marked cheapest)
- March 9: easyJet £68
- March 30: BLANK (no flight)
- March 31: easyJet £58
```

**Step 4: Claude Analyzes REAL Data**
```
Claude NOW KNOWS:
✅ March 30 Sunday: NO FLIGHTS EXIST
✅ March 31 Monday: easyJet £58 AVAILABLE
❌ Cannot recommend Sunday (no flights)
✅ Can recommend Monday with confidence
```

**Step 5: Make Evidence-Based Recommendations**
```
Claude recommends based on VERIFIED data only.
No assumptions. No "probably" or "usually".
Only dates user confirmed exist.
```

---

### **VERIFICATION CHECKLIST:**

Before recommending ANY flight, Claude must verify:

☐ **Route Verification:**
   - Airlines confirmed to fly this route
   - Frequency discovered (daily/weekly)
   - Operating days identified

☐ **Date Availability:**
   - User checked calendar for specific dates
   - Screenshot or confirmation provided
   - Prices noted for user's dates

☐ **Airline-Specific Check:**
   - If recommending specific airline (e.g., Jet2)
   - User verified that airline flies user's date
   - Actual price for that airline confirmed

☐ **Return Flight Verification:**
   - Both outbound AND return verified
   - Not just assumed symmetrical

☐ **No Assumptions Made:**
   - Every recommendation backed by verified data
   - No "usually" or "typically" statements
   - Only factual, confirmed information

---

## 🚫 WHAT CLAUDE CANNOT DO (Tool Limitations)

**Claude CANNOT:**
- ❌ Access interactive booking calendars
- ❌ See real-time airline inventory
- ❌ Verify if specific date has flights
- ❌ Check exact current pricing
- ❌ Access JavaScript-loaded content
- ❌ Screenshot airline calendars

**Claude CAN:**
- ✅ Research which airlines fly route
- ✅ Find historical patterns
- ✅ Discover general schedules
- ✅ Recommend verification tools
- ✅ Direct user to check specific things
- ✅ Analyze data user provides

---

## ✅ UPDATED PHASE 1B REQUIREMENTS

**Phase 1B (Data Source Testing) must now include:**

### **For EACH Airline Being Recommended:**

1. **Schedule Pattern Research**
   - What days does airline fly this route?
   - How frequently? (daily, 3x/week, etc.)
   - Are there seasonal variations?

2. **User Verification Required**
   - Direct user to verification tool
   - Specific instructions on what to check
   - Request screenshot or confirmation

3. **Actual Data Capture**
   - User confirms date exists
   - User provides actual price
   - User screenshots calendar

4. **Evidence Documentation**
   - Record what user verified
   - Note any discrepancies
   - Update recommendations based on facts

### **Example Dialogue:**

**BAD (Old Way - Assumptions):**
```
Claude: "Jet2 operates Sundays on this route, so Sunday March 30 
should be available around £86/person."

[WRONG - Made assumption without verification]
```

**GOOD (New Way - Verification):**
```
Claude: "Based on schedule data, Jet2 typically flies this route 
on certain days. However, I cannot verify specific date availability.

Please check Google Flights for March 2026:
1. Go to google.com/flights
2. Enter MAN → RAK
3. Click calendar
4. Screenshot March dates
5. Share what you see

This will show which dates actually have Jet2 flights."

User: [shares screenshot showing no Sunday flights]

Claude: "Thank you! The calendar shows Jet2 does NOT fly Sundays 
in March 2026. They only fly Mondays (£165) and Fridays (£68-259).

Given your constraint of latest Tuesday departure, easyJet Monday 
March 31 is your best verified option."

[RIGHT - Made recommendation based on verified data]
```

---

## 📋 PHASE 1A COMPLETION CRITERIA

**Phase 1A is complete when:**

✅ **Tools Discovered:**
   - Primary verification tools identified
   - Limitations understood
   - User partnership workflow defined

✅ **Methods Documented:**
   - Step-by-step verification process
   - Checklist created
   - Examples provided

✅ **Workflow Established:**
   - Claude's role clear
   - User's role clear
   - Hand-off points defined

✅ **Checkpoint Updated:**
   - Phase 1B requirements strengthened
   - Verification mandatory before recommendations
   - No assumptions allowed

---

## 🎓 KEY LEARNINGS FROM MOROCCO FAILURE

**Error 1: Skipped Phase 1A Entirely**
- Went straight to recommendations
- Didn't discover verification methods
- Assumed research alone was sufficient

**Error 2: Confused Schedule with Availability**
- "Jet2 flies Sundays" (general schedule)
- ≠ "Jet2 flies Sunday March 30" (specific availability)

**Error 3: Didn't Recognize Tool Limitations**
- Assumed Claude could verify dates
- Didn't request user verification
- Made recommendations without evidence

**Error 4: No Verification Workflow**
- No checklist for what to verify
- No user partnership process
- No evidence requirements

---

## 🔄 METHODOLOGY UPDATES REQUIRED

**Update Checkpoint 1.2 (Phase 1A):**
```
OLD: "Expert methods and best practices discovered"

NEW: "Expert methods AND verification tools discovered:
      ☐ Verification tools identified (Google Flights, ITA Matrix, etc.)
      ☐ Tool limitations documented
      ☐ User partnership workflow established
      ☐ Verification checklist created"
```

**Update Checkpoint 1.3 (Phase 1B):**
```
OLD: "All discovered sources tested, strategies validated"

NEW: "All discovered sources tested AND specific dates verified:
      ☐ General route research completed
      ☐ User directed to verification tool
      ☐ User confirmed specific dates exist
      ☐ Actual prices captured for user's dates
      ☐ Evidence documented before recommendations
      ☐ NO assumptions about availability"
```

**Add New Requirement:**
```
GATE: Cannot proceed to Phase 2 (Recommendations) until:
      - User has verified dates exist
      - Actual availability confirmed
      - Prices captured
      - Evidence documented
```

---

## ✅ PHASE 1A DELIVERABLES

**This document provides:**
1. ✅ Discovery of verification tools
2. ✅ Understanding of tool limitations
3. ✅ User partnership workflow
4. ✅ Verification checklist
5. ✅ Example dialogues
6. ✅ Methodology updates required

**Next Step:**
- Update Checkpoint Registry
- Implement Phase 1B verification requirements
- RESTART Morocco flight research with proper verification

---

**END OF PHASE 1A DISCOVERY DOCUMENT**

Version: 1.0  
Created: 2026-02-13  
Purpose: Prevent future availability assumption errors