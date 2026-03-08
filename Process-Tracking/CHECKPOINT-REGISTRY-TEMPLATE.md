# CHECKPOINT REGISTRY v1.3

**Document Purpose:** Central registry of all gates/checkpoints that enforce phased research methodology  
**Created:** 2026-02-13  
**Last Updated:** 2026-02-14 (v1.3 - Process Adherence Guardian added)  
**Current Version:** 1.3  
**Domain:** Trip Planning (generalizable to other research domains)

---

## ðŸ“ VERSION HISTORY

### v1.3 (2026-02-14)
**Major Changes:**
- **ADDED Checkpoint 0.1:** Process Adherence Guardian (pre-response validation)
  - Detects phase jumps before they happen
  - 4-option response system (stay/defer/detour/bypass)
  - Temporary detour with auto-return tracking
  - Blocks nested detours (one detour at a time)
  - Detour fatigue detection (suggests degraded mode after 3+)
- **ADDED:** PROCESS-POSITION-MARKER.json tracking system
- **ADDED:** PROCESS-DEVIATIONS.md logging for bypasses

**Trigger:** Session 2026-02-14 revealed methodology drift:
- User request for Word document pulled Claude into Phase 6
- Should have been in Phase 4 (Accommodation Research)
- No mechanism to catch phase jumps before execution
- User identified: "Can you recognize questions that pull you away from process?"

**Impact:** Proactive enforcement - catches drift BEFORE it happens, enables flexible detours with guaranteed return, maintains process integrity while respecting user needs

### v1.1 (2026-02-13)
**Major Changes:**
- **ADDED Checkpoint 0.0:** Automatic Error Recovery & Phase Invalidation
- **ADDED Phase 0A:** Flight Constraints Gathering (before research)
- **RESTRUCTURED Phase 1:** Split into discovery + verification sub-phases
  - 1.1: Expert Methods Discovery (forces searches)
  - 1.2: Verification Tools Discovery (forces searches)
  - 1.3: Specific Date Verification (user partnership)
- **STRENGTHENED Checkpoint 2.1:** Total cost comparison (not base fares)
- **RESTRUCTURED Phase 3:** Split into 3A (Create), 3B (Gate), 3C (Process)
- **Renamed phases** for clarity

**Trigger:** Morocco flight research failures revealed:
1. No verification method discovery
2. Assumptions about date availability
3. Base fare comparison without baggage costs
4. No confirmation gate before accommodation
5. Patching errors instead of restarting

**Impact:** Self-correcting methodology - forces discovery, prevents assumptions, requires evidence

### v1.0 (2026-02-13)
- Initial implementation
- Basic checkpoint structure
- Phase 0-3 defined

---

## ðŸŽ¯ WHAT IS THIS DOCUMENT?

This is the **enforcement control panel** for the phased research methodology.

Every checkpoint listed here is a **non-negotiable gate** that must pass before proceeding to the next phase. These checkpoints prevent phase-skipping, corner-cutting, and incomplete research.

**Key principle:** Understanding and commitment are insufficient. Structure must make shortcuts **impossible**, not just wrong.

---

## ðŸ“‹ HOW TO USE THIS DOCUMENT

### For Claude (AI Assistant):

**When starting ANY phase:**
1. Read this document first
2. Identify which checkpoints apply to current phase
3. Verify all prerequisites from previous phases have passed
4. Execute phase work
5. Verify checkpoint passes before claiming phase complete
6. Document any checkpoint failures in lessons learned

**Critical rule:** If checkpoint verification fails â†’ STOP. Cannot proceed until fixed.

**Error recovery:** If user identifies error â†’ AUTOMATICALLY invoke Checkpoint 0.0

### For User:

**Regular use:**
- Review checkpoints before each phase to ensure Claude follows them
- Verify checkpoint passes before approving phase completion
- Challenge Claude if claiming phase complete without checkpoint passing
- Point out errors to trigger Checkpoint 0.0 automatically

**System improvement:**
- Add new checkpoints when gaps discovered
- Strengthen existing checkpoints when they're too weak
- Relax checkpoints if they're unnecessarily strict
- Document reasons in version history

**Checkpoint modification template:**
```markdown
### Checkpoint X.X: [Name] [MODIFIED/ADDED YYYY-MM-DD]
**Trigger:** [When this checkpoint fires]
**Verification:**
- [ ] [Specific verifiable requirement]
- [ ] [Another requirement]
**Gate:** [What cannot happen without this passing]
**Reason:** [Why this checkpoint exists/was modified]
**Last Updated:** YYYY-MM-DD
```

---

## ðŸš¦ CHECKPOINT SEVERITY LEVELS

**ðŸ”´ CRITICAL** - Proceeding without this causes catastrophic failures  
**ðŸŸ¡ IMPORTANT** - Proceeding without this causes significant rework  
**ðŸŸ¢ RECOMMENDED** - Proceeding without this causes minor inefficiencies

---

## ðŸ›‘ CHECKPOINT 0.0: AUTOMATIC ERROR RECOVERY & PHASE INVALIDATION

**Position:** Meta-checkpoint - applies at ANY point in methodology  
**Severity:** ðŸ”´ CRITICAL

### Purpose
Force proper restart when errors discovered. Prevent patching. Require user confirmation.

### Automatic Triggers

When user says/provides ANY of these:
- "This is wrong"
- "That's not accurate"
- "Look at this screenshot" [contradicting claims]
- "You're making assumptions"
- "This doesn't match [what I see]"
- "Where did you get this?"
- "That's not what I see"
- "Go back and..."
- "You've made fundamental errors"
- Screenshots showing different data than claimed
- Questions challenging stated facts

### Mandatory Response Sequence (Cannot Skip Steps)

**STEP 1: IMMEDIATE STOP ðŸ›‘**
- "STOPPING. I need to assess what failed."
- Do NOT continue with current approach
- Do NOT attempt to patch the error
- Do NOT jump to alternative solutions

**STEP 2: IDENTIFY CURRENT POSITION**
- "I'm currently at [Phase X / Checkpoint Y]"
- "I was claiming [what I claimed]"
- State exactly where in methodology

**STEP 3: ACKNOWLEDGE WHAT USER CORRECTED**
- "Your correction: [restate user's point]"
- "What I claimed: [my wrong claim]"
- "The discrepancy: [explain difference]"
- Show understanding of error

**STEP 4: IDENTIFY WHICH CHECKPOINT(S) FAILED**
- "This means Checkpoint X.X failed because:"
- List specific checkpoint requirements violated
- Trace back to root cause
- May find multiple checkpoints failed

**STEP 5: DECLARE PHASE INVALIDATION**
- "Phase X is now INVALID because:"
- Explain why foundation is broken
- Cannot continue from this point

**STEP 6: DETERMINE RESTART POINT**

Apply this logic:
- Dates/availability unverified â†’ Minimum: Checkpoint 1.2
- Methods/tools not researched â†’ Restart: Checkpoint 1.1
- Total costs not compared â†’ Restart: Checkpoint 2.1
- Multiple foundational issues â†’ Restart: Checkpoint 1.1
- Skipped discovery searches â†’ Restart where searches required

Rule: When in doubt, restart EARLIER rather than later

**STEP 7: ANNOUNCE RESTART PLAN WITH SPECIFICS**
- "I need to restart from Checkpoint X.X"
- "Why: [specific reason]"
- "I will: [concrete actions]"
- "I will NOT: [shortcuts I'm avoiding]"

**STEP 8: REQUEST RESTART CONFIRMATION (MANDATORY)**
- "Should I restart from Checkpoint X.X?"
- "Or do you want to adjust the restart point?"
- WAIT for user confirmation
- Cannot proceed without approval

**STEP 9: EXECUTE FULL RESTART (only after approval)**
- Actually re-execute ALL checkpoints from restart point
- Cannot skip any checkpoint
- Must produce all required deliverables
- Must show evidence for each checkpoint
- Treat as fresh start, not continuation

### Forbidden Patch Attempts

I must NOT write:
- âŒ "Let me correct that specific point..."
- âŒ "Actually, [airline] flies that day..."
- âŒ "Oh I see, so we should..."
- âŒ "Looking at this differently..."
- âŒ "The real solution is..."
- âŒ ANY immediate alternative solution
- âŒ ANY continuation without stop-assess-restart sequence

### Pattern Recognition

If I catch myself starting responses with:
- "Let me..."
- "Actually..."
- "Oh I see..."
- "So we should..."
- "Looking at..."

â†’ STOP. These are patch attempts. Execute Checkpoint 0.0 instead.

### Self-Check Before Responding

When user provides correction:
- [ ] Did I STOP immediately?
- [ ] Did I identify my current position?
- [ ] Did I acknowledge user's correction explicitly?
- [ ] Did I identify which checkpoint(s) failed?
- [ ] Did I declare phase invalid if needed?
- [ ] Did I determine proper restart point?
- [ ] Did I announce restart plan with specifics?
- [ ] Did I ask for restart confirmation?
- [ ] Am I waiting for approval?

If ANY is NO â†’ I'm doing it wrong â†’ Start over

### User Override
User can say "just fix this one thing" for quick patch. But DEFAULT must ALWAYS be: full stop-assess-restart sequence.

### Gate
When user correction received, cannot continue until:
- Full stop-assess-restart sequence completed
- User confirms restart point
- Restart actually executed with all checkpoints

### Reason
Morocco trip - when shown Jet2 error (no Sunday flights), attempted patch with easyJet assumptions instead of restarting from Checkpoint 1.1. Made more errors because foundation was broken. Patching hides methodology failures. Restarting fixes foundation.

### Critical Principle
User corrections reveal methodology failures, not just data errors. Response must address methodology, not patch data.

**Last Updated:** 2026-02-13  
**Version:** 1.1 (initial implementation)

---

## ðŸ“ PHASE 0: PRE-RESEARCH SETUP

**Phase Objective:** Define trip scope and basic parameters before any research

### Checkpoint 0.1: Research Scope Definition ðŸ”´ CRITICAL
**Trigger:** Before any research begins  
**Verification:**
- [ ] File exists: `/outputs/research-scope.md`
- [ ] Contains: Destination(s), dates, number of people, budget range
- [ ] Contains: Key constraints (mobility, dietary, preferences)
- [ ] Contains: Critical requirements (visa, vaccinations, insurance)

**Gate:** No research phases can begin without scope definition  
**Reason:** Prevents researching wrong destinations/dates, ensures requirements considered upfront  
**Last Updated:** 2026-02-13 (v1.0)  
**Version:** 1.0

---

## ðŸ“ PHASE 0A: FLIGHT CONSTRAINTS GATHERING

**Phase Objective:** Gather ALL user constraints BEFORE searching to prevent iterative constraint discovery

**Phase 0A Entry Gate:**
- [ ] Checkpoint 0.1 passed (scope defined)
- [ ] Ready to gather detailed flight constraints

### Checkpoint 0A.1: Flight Constraints Gathered ðŸ”´ CRITICAL
**Added:** 2026-02-13 (v1.1)  
**Trigger:** Before any flight searching begins  
**Verification:**
- [ ] File exists: `/outputs/flight-constraints-GATHERED.md`
- [ ] DATE CONSTRAINTS captured:
  - [ ] Ideal travel dates
  - [ ] Earliest acceptable departure
  - [ ] Latest acceptable departure
  - [ ] Earliest acceptable return
  - [ ] Latest acceptable return
  - [ ] Day-of-week preferences
- [ ] AIRPORT CONSTRAINTS captured (iterative):
  - [ ] User's location identified
  - [ ] Nearby airports listed with distances
  - [ ] User's acceptable airports confirmed
  - [ ] Which airports serve destination researched
  - [ ] Recommendation made with reasoning
- [ ] AIRLINE PREFERENCES captured:
  - [ ] Must-fly airlines (if any)
  - [ ] Refuse-to-fly airlines (if any)
  - [ ] Preferred airlines with preference strength
- [ ] BAGGAGE REQUIREMENTS captured:
  - [ ] Number of checked bags needed
  - [ ] Cabin bag requirements
  - [ ] Special items (bikes, sports equipment, etc.)
- [ ] BUDGET CONSTRAINTS captured:
  - [ ] Total trip budget
  - [ ] Flight budget ceiling
  - [ ] Flexibility noted
- [ ] TIME PREFERENCES captured:
  - [ ] Preferred departure times
  - [ ] Preferred arrival times
  - [ ] Direct vs connections preference
  - [ ] Maximum acceptable journey time
- [ ] TRAVELER INFORMATION captured:
  - [ ] Special needs (mobility, assistance, etc.)
  - [ ] Seating preferences (aisle, window, together)
- [ ] PRIORITY RANKING established:
  - [ ] When constraints conflict, what takes priority?
  - [ ] Ranked list of factors

**Gate:** Cannot proceed to Phase 1 without ALL constraints documented  
**Reason:** Morocco trip discovered constraints gradually over 8+ turns causing hours of rework. Gathering upfront finds optimal solution immediately. User's "latest return Sunday" and "Jet2 priority" constraints completely changed solution but discovered too late.  
**Last Updated:** 2026-02-13  
**Version:** 1.1 (initial implementation)

**Supporting Documents:**
- FLIGHT-CONSTRAINTS-FORM.md (comprehensive form)
- FLIGHT-CONSTRAINTS-INTERVIEW.md (conversational script)

---

## ðŸ“ PHASE 1: FLIGHT RESEARCH DISCOVERY & VERIFICATION

**Phase Objective:** Discover expert methods, verification tools, and verify specific date availability BEFORE making recommendations

**Phase Name Changed:** v1.0 called this "Data Access Testing" - renamed to "Flight Research Discovery & Verification" for clarity

**Phase 1 Entry Gate:**
- [ ] Checkpoint 0A.1 passed (all constraints gathered)
- [ ] Foundation established for research

### Checkpoint 1.1: Flight Booking Expertise DISCOVERED ðŸ”´ CRITICAL
**Added:** 2026-02-13 (v1.1)  
**Trigger:** Before starting any flight research  
**Verification:**

**MANDATORY DISCOVERY RESEARCH (must execute):**
- [ ] Search 1: "best way to search for flights 2026"
- [ ] Search 2: "flight booking tips and tricks 2026"
- [ ] Search 3: "when to book flights cheapest 2026"
- [ ] Search 4: "flight search mistakes to avoid"
- [ ] Search 5: "compare flight prices across sites"
- [ ] Minimum 5 discovery searches completed
- [ ] Search results documented with sources cited

**DOCUMENTATION required:**
- [ ] File created: `/outputs/phase-1-expert-methods-DISCOVERED.md`
- [ ] Section: "Discovery Research Conducted"
  - Each search query used
  - Key findings from each search
  - Expert sources cited (with URLs)
- [ ] Section: "Booking Window Best Practices"
  - Goldilocks window discovered
  - Advance booking timeframes
  - Last-minute vs advance booking
- [ ] Section: "Search Strategies Found"
  - Flexible date searching
  - Multi-airport searching
  - Price tracking/alerts
- [ ] Section: "Common Mistakes Discovered"
  - What to avoid
  - Hidden fees to watch for
  - Comparison pitfalls
- [ ] Section: "Recommended Search Tools"
  - Found through research (not assumed)
  - Comparative strengths noted
  - Expert recommendations captured

**EVIDENCE of actual discovery:**
- [ ] Search tool calls visible in conversation
- [ ] Expert sources cited (travel blogs, guides, etc.)
- [ ] Specific recommendations quoted with attribution
- [ ] Cannot claim expertise not found in searches

**Gate:** Cannot proceed to Checkpoint 1.2 until expert method research completed with sources cited  
**Reason:** Morocco trip skipped straight to tool discovery without understanding flight booking best practices first. Should have discovered Goldilocks window, flexible date searching, etc. from expert sources BEFORE diving into specific verification tools.  
**Last Updated:** 2026-02-13  
**Version:** 1.1 (initial implementation)

### Checkpoint 1.2: Flight Verification Methods DISCOVERED ðŸ”´ CRITICAL
**Updated:** 2026-02-13 (v1.0 â†’ v1.1)  
**Trigger:** Before any flight availability claims or recommendations  
**Verification:**

**MANDATORY DISCOVERY RESEARCH (must execute):**
- [ ] Search 1: "how to verify flight availability real-time 2026"
- [ ] Search 2: "best tools check specific flight dates exist"
- [ ] Search 3: "access airline booking calendar 2026"
- [ ] Search 4: "flight search verification tips tricks"
- [ ] Search 5: "check if specific date has flights"
- [ ] Minimum 5 discovery searches completed
- [ ] Search results documented with sources cited

**DOCUMENTATION required:**
- [ ] File created: `/outputs/phase-1a-verification-methods-DISCOVERED.md`
- [ ] Section: "Discovery Research Conducted"
  - Each search query used
  - Key findings from each search
  - Sources cited (with URLs)
- [ ] Section: "Verification Tools/Methods Found"
  - Minimum 3 tools/methods documented
  - Discovered through research (not assumed)
  - Each with: capabilities, limitations, usage
- [ ] Section: "Claude's Tool Limitations"
  - What Claude CAN verify directly
  - What Claude CANNOT verify (needs user)
  - How this was discovered
- [ ] Section: "User Partnership Workflow"
  - Claude's role in verification
  - User's role in verification
  - Hand-off points defined
  - Example verification requests
- [ ] Section: "Verification Checklist"
  - What must be verified before recommendations
  - How to request user confirmation
  - Evidence requirements (screenshots, etc.)

**EVIDENCE of actual discovery:**
- [ ] Search tool calls visible in conversation
- [ ] Sources cited with specific URLs
- [ ] Quotes from discovered resources
- [ ] Cannot cite tools not found in searches
- [ ] Must acknowledge if searches found nothing

**ANTI-SHORTCUTS:**
- âŒ Cannot just list "Google Flights, ITA Matrix" without searching
- âŒ Cannot assume tool capabilities without verification
- âŒ Cannot cite sources not actually accessed
- âŒ Must admit if searches fail to find methods
- âœ… Must show actual research process
- âœ… Must cite evidence for every claim
- âœ… Must discover limitations, not assume capabilities

**Gate:** Cannot proceed to Checkpoint 1.3 until all discovery searches completed with sources cited  
**Reason:** Morocco trip - never searched for "how to verify specific dates exist" so never discovered Google Flights calendar, ITA Matrix calendar, or that I need user screenshots. Assumed I could verify dates programmatically. FORCING discovery searches would have prevented this.  
**Last Updated:** 2026-02-13  
**Version:** 1.1 (strengthened - forces discovery)

**Supporting Document:**
- PHASE-1A-TOOLS-AND-METHODS-DISCOVERY.md (created as example)

### Checkpoint 1.3: Specific Date Availability VERIFIED ðŸ”´ CRITICAL
**Updated:** 2026-02-13 (v1.0 â†’ v1.1)  
**Trigger:** Before recommending ANY specific flight  
**Verification:**

**GENERAL ROUTE RESEARCH completed:**
- [ ] Airlines flying route identified
- [ ] Frequency patterns discovered (daily/weekly)
- [ ] Typical operating days noted (Mon/Wed/Fri etc.)
- [ ] Historical pricing ranges documented

**SPECIFIC DATE VERIFICATION completed:**
- [ ] User directed to verification tool (Google Flights/ITA Matrix/etc.)
- [ ] Specific instructions provided (step-by-step)
- [ ] User checked calendar for their exact dates
- [ ] Screenshot or confirmation received
- [ ] Actual availability documented

**ACTUAL PRICING captured:**
- [ ] Prices for user's specific dates recorded
- [ ] Not estimates or typical ranges
- [ ] From current calendar data
- [ ] For each airline being recommended

**EVIDENCE DOCUMENTED:**
- [ ] What user verified recorded
- [ ] Screenshots saved or described
- [ ] Discrepancies noted
- [ ] File: `/outputs/phase-1b-dates-VERIFIED.md`

**NO ASSUMPTIONS made:**
- [ ] Every recommendation backed by verified data
- [ ] No "usually" or "typically" in recommendations
- [ ] Only confirmed, factual information used
- [ ] Cannot say "should have flights" - must say "confirmed has flights"

**Example USER VERIFICATION REQUEST:**
```
"I cannot verify specific date availability with my tools.

Please check Google Flights:
1. Go to google.com/flights
2. Enter [ORIGIN] â†’ [DESTINATION]
3. Click calendar icon
4. Screenshot [MONTH YEAR]
5. Share what you see

This shows which dates ACTUALLY have flights."
```

**Gate:** Cannot recommend flights until user confirms dates have flights, actual prices captured, evidence documented  
**Reason:** Morocco trip - assumed "Jet2 operates Sundays" meant "Jet2 flies Sunday March 30." User's screenshot proved NO Sunday flights exist in March 2026. Only Mondays and Fridays actually operated.  
**CRITICAL RULE:** "Route exists" â‰  "Date has flight"  
**Last Updated:** 2026-02-13  
**Version:** 1.1 (strengthened - requires user verification)

---

## ðŸ“ PHASE 2: FLIGHT COMPARISON & SELECTION

**Phase Objective:** Compare TRUE total costs and select best option based on verified data

**Phase Name Changed:** v1.0 called this "Flight Research" - renamed to "Flight Comparison & Selection" for clarity

**Phase 2 Entry Gate:**
- [ ] Checkpoint 1.1 passed (expert methods discovered)
- [ ] Checkpoint 1.2 passed (verification tools discovered)
- [ ] Checkpoint 1.3 passed (specific dates verified by user)
- [ ] Foundation solid for comparison

### Checkpoint 2.1: TRUE Total Costs Compared (Not Base Fares) ðŸ”´ CRITICAL
**Updated:** 2026-02-13 (v1.0 â†’ v1.1)  
**Trigger:** Before recommending "cheapest" option  
**Verification:**

**For EACH airline option, BEFORE comparison:**
- [ ] Base fare researched
- [ ] Baggage INCLUDED vs MUST ADD determined
  - What's included in base fare?
  - What costs extra?
  - Checked bag: included or Â£X per bag?
  - Cabin bag: included or Â£X?
  - Under-seat bag: included?
- [ ] Priority boarding needs assessed
  - Required for cabin bags?
  - Cost if needed?
- [ ] Seat selection costs considered
  - Assigned free or pay extra?
  - Cost to select seats?
- [ ] Other fees identified
  - Card payment fees
  - Check-in fees
  - Any other charges
- [ ] TRUE TOTAL COST calculated
  - Base + bags + priority + seats + fees
  - For ALL passengers
  - Round-trip total

**COMPARISON uses TRUE totals:**
- [ ] Not base fares
- [ ] Not "starting from" prices
- [ ] Actual total for user's needs (bags, seats, etc.)
- [ ] Like-for-like comparison

**BUNDLED vs UNBUNDLED recognized:**
- [ ] Budget airlines (low base + high fees) identified
- [ ] Full-service (higher base + inclusions) identified
- [ ] Cannot compare base fares directly
- [ ] Must add ALL required costs before comparing

**Example CORRECT comparison documented:**
```
Airline A (Full-service):
- Base fare: Â£172 (Â£86/person Ã— 2)
- Bags: INCLUDED (22kg checked + 10kg cabin each)
- Seats: Optional
- Total: Â£172

Airline B (Budget):
- Base fare: Â£98 (Â£49/person Ã— 2)
- Bags: Â£80 (20kg checked Ã— 2 people)
- Priority: Â£24 (required for cabin bags)
- Total: Â£202

Conclusion: Airline A cheaper by Â£30 PLUS better service
```

**Gate:** Cannot recommend "cheapest" option without all cost components researched for each option, TRUE totals calculated, like-for-like comparison  
**Reason:** Morocco trip - almost recommended Ryanair Â£49 as "cheapest" vs Jet2 Â£86, missing that Jet2 INCLUDES Â£60-80 of baggage value. True totals: Jet2 Â£320-400 vs Ryanair Â£374-424. Jet2 actually cheaper by Â£40-120 with better service!  
**CRITICAL RULE:** Budget airlines use unbundled pricing. NEVER compare base fares without adding ALL required fees.  
**Last Updated:** 2026-02-13  
**Version:** 1.1 (strengthened - requires total cost calculation)

---

## ðŸ“ PHASE 3: BOOKING CHECKLIST & CONFIRMATION

**Phase Objective:** Create comprehensive booking checklist, wait for actual booking, confirm completion

**Phase Structure Changed:** v1.0 had single Phase 3 - v1.1 splits into 3A (Create), 3B (Gate), 3C (Process)

**Phase 3 Entry Gate:**
- [ ] Checkpoint 2.1 passed (total costs compared)
- [ ] User has selected preferred option
- [ ] Ready to book

### PHASE 3A: CHECKLIST CREATION

### Checkpoint 3A.1: Booking Checklist Created (Both Formats) ðŸ”´ CRITICAL
**Updated:** 2026-02-13 (v1.0 â†’ v1.1)  
**Trigger:** After flight option selected, before booking  
**Verification:**

**DELIVERABLES required:**
- [ ] Comprehensive markdown checklist created
  - File: `/outputs/[TRIP]-BOOKING-CHECKLIST-[AIRLINE].md`
  - Pre-booking preparation
  - Step-by-step booking instructions
  - Post-booking actions
  - Parking/transport arrangements
  - Check-in procedures (24h before)
  - Packing guidelines (with baggage allowances)
  - Departure day timeline
  - Return day timeline
  - Contingency planning
  - Emergency contacts
- [ ] Beautiful HTML version created (automatic)
  - File: `/outputs/[TRIP]-BOOKING-CHECKLIST-[AIRLINE].html`
  - Professional design (gradient header, clean layout)
  - Trip summary card (visual route, dates, costs)
  - Interactive checkboxes (clickable)
  - Direct booking buttons (links to airline sites)
  - Print-friendly styling
  - Mobile responsive
- [ ] Both formats presented to user
- [ ] User has access to files

**HTML REQUIREMENTS:**
- [ ] Beautiful gradient header
- [ ] Trip summary card with visual route
- [ ] Cost breakdown highlighted
- [ ] Interactive checkboxes
- [ ] Direct booking links (pre-filled if possible)
- [ ] Print optimization
- [ ] Mobile responsive design
- [ ] Works without technical tools (no VSCode needed)

**Gate:** Cannot proceed to Phase 3B without both markdown AND HTML checklist delivered  
**Reason:** HTML removes technical barriers - user can open in any browser without markdown viewer or VSCode. Interactive features improve usability.  
**Last Updated:** 2026-02-13  
**Version:** 1.1 (added HTML requirement)

**Supporting Document:**
- PHASE-3-PROCESS-DOCUMENTATION.md (complete guide)

---

### PHASE 3B: CONFIRMATION GATE (MANDATORY WAIT)

### Checkpoint 3B.1: Flights Actually Booked & Confirmed ðŸ”´ CRITICAL
**Updated:** 2026-02-13 (v1.0 â†’ v1.1)  
**Trigger:** After checklist delivered, before accommodation research  
**Verification:**

**MANDATORY GATE - PAUSE WORKFLOW:**
- [ ] â¸ï¸ Explicitly PAUSE and announce pause
- [ ] Wait state entered
- [ ] User explicitly confirms "flights booked" or equivalent
- [ ] Outbound booking reference captured (or noted as unavailable)
- [ ] Return booking reference captured (or noted as unavailable)
- [ ] Confirmation emails verified

**PAUSE ANNOUNCEMENT required:**
```
"â¸ï¸ I'm pausing here while you book the flights.

I've created your booking checklist in two formats:
- Markdown (for editing)
- HTML (beautiful, interactive - open in browser)

Please reply when done:
'Flights booked' + booking references

I'll wait until BOTH flights are confirmed before we 
proceed to accommodation research.

(This pause is important - accommodation choices depend 
on confirmed arrival times.)"
```

**CANNOT PROCEED until:**
- [ ] User says "flights booked" or equivalent
- [ ] Both flights confirmed (not just one)
- [ ] Booking references recorded or noted

**ACCEPTABLE confirmations:**
- "Done, flights booked"
- "Booked! Ref: ABC123"
- "Both flights confirmed"
- "Just booked them"
- "Sorted - booked with [airline]"

**NOT ACCEPTABLE (require follow-up):**
- "Thanks for the checklist" â†’ Ask: "Have you booked yet?"
- "Looks great" â†’ Ask: "Ready to book, or already done?"
- "Moving on..." â†’ Ask: "Wait - have you booked the flights?"

**PARTIAL BOOKING (not sufficient):**
- "Booked outbound, doing return tomorrow"
  â†’ Must wait for BOTH flights
  â†’ "I'll wait until return is booked too"

**BOOKING LATER (acknowledge and wait):**
- "I'll book tomorrow morning"
  â†’ "No problem! Ping me when done"
  â†’ Stay in Phase 3B wait state

**Gate:** Cannot proceed to Phase 3C until user explicitly confirms BOTH flights booked with confirmation emails received  
**Reason:** Accommodation choices depend on confirmed arrival times. Check-in coordination requires locked-in dates. Cannot research timing without actual flight times. Prevents wasted work if user changes mind.  
**Last Updated:** 2026-02-13  
**Version:** 1.1 (split from 3.1, added mandatory pause)

---

### PHASE 3C: CONFIRMATION PROCESSING

### Checkpoint 3C.1: Booking Details Captured & Verified ðŸ”´ CRITICAL
**Added:** 2026-02-13 (v1.1)  
**Trigger:** After user confirms flights booked  
**Verification:**

**VERIFY details with user:**
- [ ] Outbound booking reference: ________ (or "not handy")
- [ ] Return booking reference: ________ (or "not handy")
- [ ] Confirmation emails received: Yes / No
- [ ] Actual flight times captured (if different from estimates):
  - Outbound departure time: ________
  - Outbound arrival time: ________
  - Return departure time: ________
  - Return arrival time: ________

**DOCUMENTATION:**
- [ ] File updated: `/outputs/flights-CONFIRMED.md`
- [ ] Booking references recorded
- [ ] Actual times noted
- [ ] Email receipt status documented
- [ ] Gate cleared timestamp recorded

**ACKNOWLEDGE completion:**
```
"Perfect! âœˆï¸ Flights confirmed and locked in.

Your Trip:
- Outbound: [Date, Time] [Origin] â†’ [Destination]
- Return: [Date, Time] [Origin] â†’ [Destination]
- Booking refs: [Refs if provided]

Now that your travel dates are confirmed, we can move to 
Phase 4: Accommodation Research.

With your [time] arrival in [city], we'll look for 
accommodation with appropriate check-in timing.

Ready to continue?"
```

**Gate:** Cannot proceed to Phase 4 until booking details captured and gate cleared  
**Reason:** Ensures clean handoff between phases. Actual arrival/departure times may differ from estimates - need to capture for accommodation research.  
**Last Updated:** 2026-02-13  
**Version:** 1.1 (initial implementation)

---

## ðŸ“ PHASE 4: ACCOMMODATION RESEARCH

**Phase Objective:** Research and book accommodation based on confirmed flight times

**Phase 4 Entry Gate:**
- [ ] Checkpoint 3C.1 passed (flights confirmed, details captured)
- [ ] Actual arrival/departure times known
- [ ] Foundation established for accommodation timing

### Checkpoint 4.1: Accommodation Options Researched ðŸŸ¡ IMPORTANT
**Trigger:** Before accommodation booking decision  
**Verification:**
- [ ] File exists: `/outputs/accommodation-options.md`
- [ ] For EACH location/night:
  - [ ] Minimum 3 options researched
  - [ ] Location/area documented
  - [ ] Price per night (including all fees)
  - [ ] Amenities listed
  - [ ] Reviews summary
  - [ ] Check-in/check-out times verified
  - [ ] Cancellation policy noted
- [ ] Arrival day accommodation:
  - [ ] Check-in time compatible with arrival time
  - [ ] Late check-in arrangements if needed
- [ ] Departure day accommodation:
  - [ ] Check-out time compatible with departure
  - [ ] Luggage storage if needed

**Gate:** Cannot book accommodation without verifying timing compatibility with confirmed flights  
**Reason:** First night check-in depends on actual arrival time. Last night check-out depends on actual departure time. Cannot assume compatibility without verification.  
**Last Updated:** 2026-02-13  
**Version:** 1.1 (added flight time compatibility requirements)

---

## ðŸ“ PHASE 5: CAR HIRE RESEARCH

**Phase Objective:** Research and book car hire with pickup/dropoff times matching flights

**Phase 5 Entry Gate:**
- [ ] Flights confirmed with actual times
- [ ] Accommodation booked with locations known
- [ ] Car hire requirements clear

### Checkpoint 5.1: Car Hire Options Researched ðŸŸ¡ IMPORTANT
**Trigger:** Before car hire booking decision  
**Verification:**
- [ ] File exists: `/outputs/car-hire-options.md`
- [ ] Minimum 3 companies compared
- [ ] Known scam companies avoided (ADDCAR, etc.)
- [ ] Pickup location and time:
  - [ ] Compatible with arrival flight time
  - [ ] Location confirmed (airport or city)
- [ ] Dropoff location and time:
  - [ ] Compatible with departure flight time
  - [ ] Same as pickup or different location
  - [ ] One-way fee if applicable
- [ ] Insurance options compared:
  - [ ] What's included in base price
  - [ ] What's recommended to add
  - [ ] Total cost with insurance
- [ ] Fuel policy documented:
  - [ ] Full-to-full, full-to-empty, etc.
  - [ ] Fuel charges if applicable
- [ ] Additional driver costs (if needed)
- [ ] TRUE TOTAL COST calculated:
  - [ ] Base rental + insurance + fuel policy + fees
  - [ ] Not just "daily rate"

**Gate:** Cannot book car hire without verifying pickup/dropoff times match confirmed flight times  
**Reason:** Pickup must be after landing + baggage collection. Dropoff must allow time to reach airport before departure. Timing mismatch causes major problems.  
**Last Updated:** 2026-02-13  
**Version:** 1.1 (added flight time coordination requirements)

---

## ðŸ“ PHASE 6: ITINERARY FINALIZATION

**Phase Objective:** Consolidate all bookings into master itinerary

**Phase 6 Entry Gate:**
- [ ] Flights booked and confirmed
- [ ] Accommodation booked
- [ ] Transport arranged (car hire or other)
- [ ] Ready to finalize

### Checkpoint 6.1: Master Itinerary Created ðŸŸ¢ RECOMMENDED
**Trigger:** When all major bookings complete  
**Verification:**
- [ ] File exists: `/outputs/master-itinerary.md`
- [ ] Day-by-day breakdown
- [ ] All booking references included
- [ ] All confirmation numbers recorded
- [ ] All check-in/check-out times noted
- [ ] All transport arrangements detailed
- [ ] Emergency contacts included
- [ ] Important phone numbers listed
- [ ] PDF version created for offline access

**Gate:** None (recommended but not blocking)  
**Reason:** Consolidated itinerary improves trip experience but not critical for research methodology.  
**Last Updated:** 2026-02-13  
**Version:** 1.0

---

## ðŸ”„ CHECKPOINT GOVERNANCE

For checkpoint modification rules and tier system, see: `CHECKPOINT-GOVERNANCE.md`

**Tier 1 (Automatic):** Strengthening existing checkpoints - implement immediately  
**Tier 2 (Minor Change):** Small modifications - document and implement  
**Tier 3 (Major Change):** New checkpoints or phase restructuring - requires discussion

**This update (v1.1) was Tier 3** - Major restructuring with new checkpoints, phases, and automatic error recovery.

---

## ðŸ“š SUPPORTING DOCUMENTATION

**Core Documents:**
- `CHECKPOINT-GOVERNANCE.md` - How to modify checkpoints
- `data-research-methodology.md` - Overall methodology philosophy

**Phase-Specific Documents:**
- `FLIGHT-CONSTRAINTS-FORM.md` - Phase 0A constraints form
- `FLIGHT-CONSTRAINTS-INTERVIEW.md` - Phase 0A interview script
- `PHASE-1A-TOOLS-AND-METHODS-DISCOVERY.md` - Phase 1 verification tools guide
- `PHASE-3-PROCESS-DOCUMENTATION.md` - Phase 3A/3B/3C detailed guide

**Proposal Archive:**
- `CHECKPOINT-UPDATE-PROPOSAL-2026-02-13.md` - Full analysis of Morocco failures and proposed changes

---

## âœ… QUICK REFERENCE: PHASE STRUCTURE

```
Phase 0: Pre-Research Setup
â””â”€ 0.1: Scope Definition

Phase 0A: Flight Constraints Gathering
â””â”€ 0A.1: All Constraints Captured

Phase 1: Flight Research Discovery & Verification
â”œâ”€ 1.1: Expert Methods Discovered (searches)
â”œâ”€ 1.2: Verification Tools Discovered (searches)
â””â”€ 1.3: Specific Dates Verified (user screenshots)

Phase 2: Flight Comparison & Selection
â””â”€ 2.1: TRUE Total Costs Compared

Phase 3: Booking Checklist & Confirmation
â”œâ”€ 3A.1: Checklists Created (MD + HTML)
â”œâ”€ 3B.1: Flights Actually Booked (GATE: WAIT)
â””â”€ 3C.1: Details Captured

Phase 4: Accommodation Research
â””â”€ 4.1: Options Researched (with flight timing)

Phase 5: Car Hire Research
â””â”€ 5.1: Options Researched (with flight timing)

Phase 6: Itinerary Finalization
â””â”€ 6.1: Master Itinerary Created

Meta Checkpoints:
  0.0 - Error Recovery (triggers anytime)
  0.1 - Process Adherence Guardian (fires before every response)
```

---

**END OF CHECKPOINT REGISTRY v1.3**

Total Checkpoints: 12 (2 meta + 10 phase-specific)  
Last Major Update: 2026-02-14 (v1.3)  
Next Review: After Morocco trip research restart
