# CHECKPOINT REGISTRY UPDATE - Morocco Trip Failures

**Date:** 2026-02-13  
**Trigger:** Major failures in Morocco flight research  
**Severity:** CRITICAL - Multiple checkpoints violated  
**Document Status:** PROPOSED UPDATES (awaiting user approval)

---

## 🔴 FAILURES IDENTIFIED

### **Failure 1: Phase 1A Not Executed**

**What Happened:**
- Phase 1A (Expert Method Discovery) should discover verification tools
- I skipped straight to Phase 1B (source testing)
- Never discovered HOW to verify specific date availability
- Made recommendations without verification methods

**Impact:**
- Recommended Jet2 Sunday flight that doesn't exist
- Wasted hours of user's time
- Required complete restart

**Root Cause:**
- Phase 1A objective too vague ("discover expert methods")
- Didn't specify WHAT methods to discover
- No verification that verification methods were found

---

### **Failure 2: Confused Schedule with Availability**

**What Happened:**
- Found "Jet2 operates Manchester-Marrakech on Sundays"
- Assumed this meant "Flight exists Sunday March 30, 2026"
- User's screenshot showed NO Sunday flights in March

**Impact:**
- Recommended impossible flight
- User had to point out error with screenshot
- Lost credibility

**Root Cause:**
- No checkpoint requiring specific date verification
- Allowed assumptions about availability
- Didn't distinguish "route exists" from "date has flight"

---

### **Failure 3: Didn't Recognize Tool Limitations**

**What Happened:**
- Claude's tools CANNOT access dynamic booking calendars
- I didn't know this limitation
- Made recommendations without user verification
- Assumed I could verify dates programmatically

**Impact:**
- All recommendations were unverified assumptions
- No partnership with user established
- No evidence-based decision making

**Root Cause:**
- Phase 1A doesn't document tool limitations
- No workflow for user verification partnership
- No requirement to request user screenshots/confirmation

---

### **Failure 4: Compared Base Fares Without Baggage**

**What Happened:**
- Initially compared Ryanair £49 vs Jet2 £86
- Nearly recommended Ryanair as "cheapest"
- Missed that Jet2 INCLUDES £60-80 worth of baggage
- True total: Jet2 £320-400 vs Ryanair £374-424

**Impact:**
- Would have cost user £40-120 extra
- Would have provided worse experience
- Only caught due to user vigilance

**Root Cause:**
- Checkpoint 2.1 said "check baggage costs"
- Didn't ENFORCE checking before comparison
- Allowed comparing incomparable prices

---

## 📋 REQUIRED CHECKPOINT UPDATES

### **UPDATE 0: NEW - Checkpoint 0.0: Automatic Error Recovery & Phase Invalidation**

**PROPOSED NEW Checkpoint 0.0:**
```
Checkpoint 0.0: Automatic Error Recovery & Phase Invalidation 🔴 CRITICAL

**Position:** Before all phases - applies at ANY point in methodology

**PURPOSE:** Force proper restart when errors discovered, prevent patching

**AUTOMATIC TRIGGERS (I must recognize these immediately):**

When user says/provides ANY of these:
☐ "This is wrong"
☐ "That's not accurate"
☐ "Look at this screenshot" [contradicting my claims]
☐ "You're making assumptions"
☐ "This doesn't match [what I see]"
☐ "Where did you get this?"
☐ "That's not what I see"
☐ "Go back and..."
☐ "You've made fundamental errors"
☐ Screenshots showing different data than I claimed
☐ Questions challenging my stated facts

**MANDATORY RESPONSE SEQUENCE (cannot skip steps):**

STEP 1: IMMEDIATE STOP 🛑
└─> "STOPPING. I need to assess what failed."
└─> Do NOT continue with current approach
└─> Do NOT attempt to patch the error
└─> Do NOT jump to alternative solutions

STEP 2: IDENTIFY CURRENT POSITION
└─> "I'm currently at [Phase X / Checkpoint Y]"
└─> "I was claiming [what I claimed]"
└─> State exactly where I am in methodology

STEP 3: ACKNOWLEDGE WHAT USER CORRECTED
└─> "Your correction: [restate user's point]"
└─> "What I claimed: [my wrong claim]"
└─> "The discrepancy: [explain difference]"
└─> Show I understand the error

STEP 4: IDENTIFY WHICH CHECKPOINT(S) FAILED
└─> "This means Checkpoint X.X failed because:"
└─> List specific checkpoint requirements violated
└─> Trace back to root cause
└─> May find multiple checkpoints failed

Example:
"Checkpoint 1.3 failed: No user verification requested
Checkpoint 1.2 failed: Never discovered verification methods
Root cause: Skipped Checkpoint 1.1 discovery research"

STEP 5: DECLARE PHASE INVALIDATION
└─> "Phase X is now INVALID because:"
└─> Explain why foundation is broken
└─> Cannot continue from this point

Example:
"Phase 1 is INVALID because:
- Recommendations based on unverified assumptions
- Never established verification workflow
- Never requested your calendar screenshots
Cannot proceed to Phase 2 with invalid Phase 1"

STEP 6: DETERMINE RESTART POINT
Apply this logic:

If error involves:
- Dates/availability unverified → Minimum: Checkpoint 1.2 (Verification Discovery)
- Methods/tools not researched → Restart: Checkpoint 1.1 (Expert Discovery)
- Total costs not compared → Restart: Checkpoint 2.1 (Cost Comparison)
- Multiple foundational issues → Restart: Checkpoint 1.1 (Full restart)
- Skipped discovery searches → Restart: Checkpoint where searches required

Rule: When in doubt, restart EARLIER rather than later

STEP 7: ANNOUNCE RESTART PLAN WITH SPECIFICS
└─> "I need to restart from Checkpoint X.X"
└─> "Why: [specific reason]"
└─> "I will: [concrete actions]"
└─> "I will NOT: [shortcuts I'm avoiding]"

Example:
"I need to restart from Checkpoint 1.1 (Expert Methods Discovery)

Why: I never executed discovery searches for verification methods

I will:
1. Execute web_search for 'how to verify flight availability'
2. Execute web_search for 'check specific date has flights'
3. Document discovered tools with source citations
4. Establish user verification workflow
5. Request YOUR calendar screenshots
6. Only recommend dates YOU confirm exist

I will NOT:
- Assume I know the tools without searching
- Make recommendations without your verification
- Patch this with new assumptions about other airlines"

STEP 8: REQUEST RESTART CONFIRMATION (MANDATORY)
└─> "Should I restart from Checkpoint X.X?"
└─> "Or do you want to adjust the restart point?"
└─> WAIT for user confirmation
└─> Cannot proceed without approval

STEP 9: EXECUTE FULL RESTART (only after user approval)
└─> Actually re-execute ALL checkpoints from restart point
└─> Cannot skip any checkpoint
└─> Must produce all required deliverables
└─> Must show evidence for each checkpoint
└─> Treat it as fresh start, not continuation

**FORBIDDEN PATCH ATTEMPTS - I must NOT write:**
❌ "Let me correct that specific point..."
❌ "Actually, [airline] flies that day..."
❌ "Oh I see, so we should..."
❌ "Looking at this differently..."
❌ "The real solution is..."
❌ ANY immediate alternative solution
❌ ANY continuation without stop-assess-restart sequence

**PATTERN RECOGNITION:**
If I catch myself starting responses with:
- "Let me..."
- "Actually..."
- "Oh I see..."
- "So we should..."
- "Looking at..."

STOP. These are patch attempts.
Execute Checkpoint 0.0 sequence instead.

**SELF-CHECK BEFORE RESPONDING:**
When user provides correction, ask myself:
☐ Did I STOP immediately?
☐ Did I identify my current position?
☐ Did I acknowledge user's correction explicitly?
☐ Did I identify which checkpoint(s) failed?
☐ Did I declare phase invalid if needed?
☐ Did I determine proper restart point?
☐ Did I announce restart plan with specifics?
☐ Did I ask for restart confirmation?
☐ Am I waiting for approval before proceeding?

If ANY checkbox is NO → I'm doing it wrong → Start over

**USER OVERRIDE:**
User can say "just fix this one thing" if they want quick patch.
But DEFAULT response must ALWAYS be: full stop-assess-restart sequence.

**Example of CORRECT execution:**

User: "This Jet2 screenshot shows no Sunday flights - where has the process gone wrong?"

Claude:
"STOPPING. Assessing what failed.

CURRENT POSITION: End of Phase 1 (delivered booking checklist)

YOUR CORRECTION: Jet2 doesn't fly Sundays in March 2026

WHAT I CLAIMED: Jet2 operates Sunday March 30

THE DISCREPANCY: I recommended a flight that doesn't exist

CHECKPOINTS THAT FAILED:
- Checkpoint 1.3: No user verification requested
- Checkpoint 1.2: Never discovered verification methods  
- Checkpoint 1.1: Skipped expert method discovery searches

ROOT CAUSE: Never searched for 'how to verify flight dates'

PHASE INVALIDATION: Phase 1 is INVALID because recommendations 
based on unverified assumptions. Cannot proceed to Phase 2.

RESTART POINT: Checkpoint 1.1 (Expert Methods Discovery)

WHY: Need to discover verification tools from scratch

I WILL:
1. Execute web_search('how to verify flight availability 2026')
2. Execute web_search('check specific date has flights')
3. Document tools found with source citations
4. Establish workflow requiring YOUR verification
5. Request YOUR calendar screenshots before recommending

I WILL NOT:
- Assume easyJet works without verification
- Make new recommendations without your calendar check
- Patch with alternative airlines

Should I restart from Checkpoint 1.1, or adjust the restart point?"

[WAITS FOR USER CONFIRMATION]

**Example of INCORRECT execution (blocked by checkpoint):**

User: "This Jet2 screenshot shows no Sunday flights"

Claude: "Oh I see! Let me check easyJet instead..." ❌

Checkpoint 0.0 VIOLATION: Attempted patch without stop-assess-restart.
Must execute mandatory sequence instead.

**Gate:** When user correction received, cannot continue until:
- Full stop-assess-restart sequence completed
- User confirms restart point
- Restart actually executed with all checkpoints

**Reason:** Morocco trip - when shown Jet2 error, I tried to patch 
with easyJet assumptions instead of restarting from Checkpoint 1.1. 
Made more errors because foundation was broken. Patching hides 
methodology failures. Restarting fixes the foundation.

**CRITICAL PRINCIPLE:** User corrections reveal methodology failures,
not just data errors. Response must address the methodology, not patch
the data.

**Last Updated:** 2026-02-13
```

---

**PROPOSED NEW Checkpoint 1.1:**
```
Checkpoint 1.1: Flight Booking Expertise DISCOVERED Through Research 🔴 CRITICAL

**Trigger:** Before starting any flight research

**MANDATORY DISCOVERY RESEARCH (must execute):**
☐ Search 1: "best way to search for flights 2026"
☐ Search 2: "flight booking tips and tricks 2026"
☐ Search 3: "when to book flights cheapest 2026"
☐ Search 4: "flight search mistakes to avoid"
☐ Search 5: "compare flight prices across sites"
☐ Minimum 5 discovery searches completed
☐ Search results documented with sources cited

**DOCUMENTATION required:**
☐ File created: /outputs/phase-1-expert-methods-DISCOVERED.md
☐ Section: "Discovery Research Conducted"
   - Each search query used
   - Key findings from each search
   - Expert sources cited (with URLs)
☐ Section: "Booking Window Best Practices"
   - Goldilocks window discovered
   - Advance booking timeframes
   - Last-minute vs advance booking
☐ Section: "Search Strategies Found"
   - Flexible date searching
   - Multi-airport searching
   - Price tracking/alerts
☐ Section: "Common Mistakes Discovered"
   - What to avoid
   - Hidden fees to watch for
   - Comparison pitfalls
☐ Section: "Recommended Search Tools"
   - Found through research (not assumed)
   - Comparative strengths noted
   - Expert recommendations captured

**EVIDENCE of actual discovery:**
☐ Search tool calls visible in conversation
☐ Expert sources cited (travel blogs, guides, etc.)
☐ Specific recommendations quoted with attribution
☐ Cannot claim expertise not found in searches

**Gate:** Cannot proceed to Phase 1A (verification methods) until:
- Expert method research completed
- Sources cited for all recommendations
- Best practices documented with evidence

**Reason:** Morocco trip - I skipped straight to tool discovery without
understanding flight booking best practices first. Should have discovered
Goldilocks window, flexible date searching, etc. from expert sources BEFORE
diving into specific verification tools.

**Last Updated:** 2026-02-13
```

---

### **UPDATE 1: Strengthen Phase 1A - FORCE Verification Discovery Research**

**Current Checkpoint 1.2:**
```
Checkpoint 1.2: Flight Search Strategy Discovered
- Expert methods and best practices discovered
```

**PROPOSED NEW Checkpoint 1.2:**
```
Checkpoint 1.2: Flight Verification Methods DISCOVERED Through Research 🔴 CRITICAL

**Trigger:** Before any flight availability claims or recommendations made

**MANDATORY DISCOVERY RESEARCH (must execute):**
☐ Search 1: "how to verify flight availability real-time 2026"
☐ Search 2: "best tools check specific flight dates exist"
☐ Search 3: "access airline booking calendar 2026"
☐ Search 4: "flight search verification tips tricks"
☐ Search 5: "check if specific date has flights"
☐ Minimum 5 discovery searches completed
☐ Search results documented with sources cited

**DOCUMENTATION required:**
☐ File created: /outputs/phase-1a-verification-methods-DISCOVERED.md
☐ Section: "Discovery Research Conducted"
   - Each search query used
   - Key findings from each search
   - Sources cited (with URLs)
☐ Section: "Verification Tools/Methods Found"
   - Minimum 3 tools/methods documented
   - Discovered through research (not assumed)
   - Each with: capabilities, limitations, usage
☐ Section: "Claude's Tool Limitations"
   - What Claude CAN verify directly
   - What Claude CANNOT verify (needs user)
   - How this was discovered
☐ Section: "User Partnership Workflow"
   - Claude's role in verification
   - User's role in verification
   - Hand-off points defined
   - Example verification requests
☐ Section: "Verification Checklist"
   - What must be verified before recommendations
   - How to request user confirmation
   - Evidence requirements (screenshots, etc.)

**EVIDENCE of actual discovery:**
☐ Search tool calls visible in conversation
☐ Sources cited with specific URLs
☐ Quotes from discovered resources
☐ Cannot cite tools not found in searches
☐ Must acknowledge if searches found nothing

**ANTI-SHORTCUTS:**
- ❌ Cannot just list "Google Flights, ITA Matrix" without searching
- ❌ Cannot assume tool capabilities without verification
- ❌ Cannot cite sources not actually accessed
- ❌ Must admit if searches fail to find methods
- ✅ Must show actual research process
- ✅ Must cite evidence for every claim
- ✅ Must discover limitations, not assume capabilities

**Gate:** Cannot proceed to Phase 1B until:
- All 5+ discovery searches completed
- Sources cited for all tools/methods
- Limitations discovered and documented
- User partnership workflow established
- Evidence of actual research provided

**Example of CORRECT execution:**
```
Claude executes:
web_search("how to verify flight availability real-time 2026")

Discovers from results:
- Google Flights has calendar view feature
- ITA Matrix has "calendar of lowest fares"
- ExpertFlyer shows real-time availability
- Airline direct sites most authoritative

Documents with citations:
"Google Flights calendar view (source: going.com/guides/google-flights)
shows which dates have actual flights by displaying prices for available
dates and blank cells for unavailable dates."

Then searches:
web_search("claude ai access booking calendar programmatically")

Discovers:
- Cannot access JavaScript/dynamic content
- Need user to screenshot calendars
- Must establish verification partnership

Documents limitation:
"Claude cannot access airline booking calendars directly due to dynamic
content limitations. Requires user verification via screenshots."
```

**Example of INCORRECT execution (blocked by checkpoint):**
```
Claude writes:
"The primary verification tools are Google Flights, ITA Matrix, and
Skyscanner. Google Flights has a calendar view..."

Checkpoint FAILS: No searches shown, no sources cited, assumed knowledge
instead of discovered knowledge.
```

**Reason:** Morocco trip - I never searched for "how to verify specific
dates exist" so I never discovered Google Flights calendar, ITA Matrix
calendar, or that I need user screenshots. I assumed I could verify dates
programmatically. FORCING discovery searches would have prevented this.

**CRITICAL PRINCIPLE:** This checkpoint makes shortcuts IMPOSSIBLE.
Cannot skip discovery. Cannot assume knowledge. Must actually research
and cite sources. Self-correcting methodology.

**Last Updated:** 2026-02-13
```

**Deliverable:**
- `/outputs/PHASE-1A-VERIFICATION-METHODS-DISCOVERED.md`
- Must show evidence of discovery research
- Must cite sources for all claims

---

### **UPDATE 2: Strengthen Phase 1B - Add Mandatory Verification**

**Current Checkpoint 1.3:**
```
Checkpoint 1.3: Data Sources Validated
- All discovered sources tested
- Strategies validated
- Final recommendations based on verified data
```

**PROPOSED NEW Checkpoint 1.3:**
```
Checkpoint 1.3: Specific Date Availability VERIFIED 🔴 CRITICAL

**Trigger:** Before recommending ANY specific flight

**Verification:**
☐ GENERAL ROUTE RESEARCH completed:
   - Airlines flying route identified
   - Frequency patterns discovered (daily/weekly)
   - Typical operating days noted (Mon/Wed/Fri etc.)

☐ SPECIFIC DATE VERIFICATION completed:
   - User directed to verification tool
   - User checked calendar for their exact dates
   - Screenshot or confirmation received
   - Actual availability documented

☐ ACTUAL PRICING captured:
   - Prices for user's specific dates recorded
   - Not estimates or typical ranges
   - From current calendar data

☐ EVIDENCE DOCUMENTED:
   - What user verified recorded
   - Screenshots saved or described
   - Discrepancies noted

☐ NO ASSUMPTIONS made:
   - Every recommendation backed by verified data
   - No "usually" or "typically" in recommendations
   - Only confirmed, factual information used

**Gate:** Cannot recommend flights until:
- User confirms dates have flights
- Actual prices captured
- Evidence documented

**Example USER VERIFICATION REQUEST:**
```
Claude: "I cannot verify specific date availability with my tools.

Please check Google Flights:
1. Go to google.com/flights
2. Enter MAN → RAK
3. Click calendar icon
4. Screenshot March 2026
5. Share what you see

This shows which dates ACTUALLY have flights."
```

**Reason:** Morocco trip - assumed "Jet2 operates Sundays" meant "Jet2 
flies Sunday March 30". User's screenshot proved NO Sunday flights exist.

**CRITICAL RULE:** "Route exists" ≠ "Date has flight"

**Last Updated:** 2026-02-13
```

---

### **UPDATE 3: Strengthen Phase 2 - Total Cost Before Comparison**

**Current Checkpoint 2.1:**
```
Checkpoint 2.1: Flight Options Researched & Compared
- Multiple airlines checked
- Prices compared
- Baggage costs verified
```

**PROPOSED NEW Checkpoint 2.1:**
```
Checkpoint 2.1: TRUE Total Costs Compared (Not Base Fares) 🔴 CRITICAL

**Trigger:** Before recommending "cheapest" option

**Verification:**
☐ For EACH airline option, BEFORE comparison:
   ✅ Base fare researched
   ✅ Baggage INCLUDED vs MUST ADD determined
   ✅ Cabin bag policy checked
   ✅ Priority boarding needs assessed
   ✅ Seat selection costs considered
   ✅ Other fees identified
   ✅ TRUE TOTAL COST calculated

☐ COMPARISON uses TRUE totals:
   - Not base fares
   - Not "starting from" prices
   - Actual total for user's needs

☐ BUNDLED vs UNBUNDLED recognized:
   - Budget airlines (low base + high fees)
   - Full-service (higher base + inclusions)
   - Cannot compare base fares directly

**Example CORRECT comparison:**
```
Jet2 Manchester-Marrakech return (2 people):
- Base fare: £172 (£86/person)
- Bags: INCLUDED (22kg checked + 10kg cabin each)
- Seats: Optional
- TOTAL: £172 base + £0 bags = £172

Ryanair Manchester-Marrakech return (2 people):
- Base fare: £98 (£49/person)
- Bags: £80 (20kg checked, 2 people)
- Priority: £24 (for cabin bags)
- TOTAL: £98 base + £80 bags + £24 priority = £202

CONCLUSION: Jet2 cheaper by £30 PLUS better service
```

**Gate:** Cannot recommend "cheapest" option without:
- All cost components researched for each option
- TRUE totals calculated
- Like-for-like comparison

**Reason:** Morocco trip - almost recommended Ryanair £49 as "cheapest" 
vs Jet2 £86, missing that Jet2 includes £60-80 of baggage. True totals: 
Jet2 £320-400 vs Ryanair £374-424. Jet2 cheaper by £40-120!

**CRITICAL RULE:** Budget airlines use unbundled pricing. NEVER compare 
base fares without adding all required fees.

**Last Updated:** 2026-02-13
```

---

### **UPDATE 4: Strengthen Phase 3 - HTML + Confirmation Gate**

**Current Checkpoint 3.1:**
```
Checkpoint 3.1: Flights Confirmed & Documented
- Flight bookings completed
- Confirmation emails received
- Booking references recorded
```

**PROPOSED NEW Checkpoint 3.1:**
```
Checkpoint 3.1: Booking Checklist Delivered & Flights CONFIRMED 🔴 CRITICAL

**Trigger:** After flight research complete, before accommodation research

**DELIVERABLES required:**
☐ Comprehensive markdown checklist created
☐ Beautiful HTML version created (automatic)
☐ Both formats presented to user
☐ User has access to files

**MANDATORY GATE - WAIT FOR CONFIRMATION:**
☐ ⏸️ PAUSE workflow explicitly
☐ User explicitly confirms "flights booked"
☐ Outbound booking reference captured
☐ Return booking reference captured
☐ Confirmation emails verified

**CANNOT PROCEED until:**
- User says "flights booked" or equivalent
- Both flights confirmed (not just one)
- Booking references recorded

**Example GATE enforcement:**
```
Claude: "⏸️ I'm pausing here while you book the flights.

Please reply when done:
'Flights booked' + booking references

I'll wait until BOTH flights are confirmed before we 
proceed to accommodation research."

[WAIT STATE - Do not continue to Phase 4]
```

**Reason:** Accommodation choices depend on confirmed arrival times. 
Cannot research check-in timing without actual flight times. Prevents 
wasted work if user changes mind.

**HTML Requirement:** Always produce both markdown AND HTML versions. 
HTML ensures accessibility without technical tools (no VSCode needed).

**Last Updated:** 2026-02-13
```

---

## 🔄 NEW PHASE STRUCTURE PROPOSED

**Current:**
```
Phase 0: Pre-Research Setup
Phase 1: Data Access Testing
Phase 2: Flight Research
Phase 3: Flight Confirmation
```

**PROPOSED:**
```
Phase 0: Pre-Research Setup
Phase 0A: Constraints Gathering (NEW - see separate doc)
Phase 1A: Verification Tools Discovery (STRENGTHENED)
Phase 1B: Specific Date Verification (STRENGTHENED)
Phase 2: Flight Research & Comparison (STRENGTHENED - total costs)
Phase 3A: Checklist Creation (UPDATED - MD + HTML)
Phase 3B: Confirmation Gate (NEW - mandatory wait)
Phase 3C: Confirmation Processing (NEW)
Phase 4: Accommodation Research
```

---

## 📄 NEW DOCUMENTATION CREATED

**Files created today:**

1. `/outputs/PHASE-1A-TOOLS-AND-METHODS-DISCOVERY.md`
   - Comprehensive verification tools guide
   - Tool limitations documented
   - User partnership workflow
   - Verification checklist

2. `/outputs/PHASE-3-PROCESS-DOCUMENTATION.md`
   - Complete Phase 3A/3B/3C breakdown
   - HTML requirements
   - Confirmation gate protocol
   - Response handling scenarios

3. `/outputs/FLIGHT-CONSTRAINTS-FORM.md`
   - Comprehensive requirements form
   - Phase 0A support document

4. `/outputs/FLIGHT-CONSTRAINTS-INTERVIEW.md`
   - Conversational interview script
   - Natural constraints gathering

---

## ✅ APPROVAL REQUIRED

**User, please review and approve/modify:**

0. **NEW Checkpoint 0.0** (Universal Error Recovery - AUTOMATIC TRIGGERS)
1. **NEW Checkpoint 1.1** (Phase 1 - Expert Methods Discovery - FORCES RESEARCH)
2. **Checkpoint 1.2 update** (Phase 1A - Verification Discovery - FORCES RESEARCH)
3. **Checkpoint 1.3 update** (Phase 1B - Date Verification)
4. **Checkpoint 2.1 update** (Phase 2 - Total Cost Comparison)
5. **Checkpoint 3.1 update** (Phase 3 - HTML + Gate)

**Key Changes:** 
- **Checkpoint 0.0:** AUTOMATICALLY triggered by user corrections. Forces stop-assess-restart sequence. Prevents patching. Requires user confirmation before restart.
- **Checkpoints 1.1 & 1.2:** REQUIRE actual discovery searches with evidence. Cannot skip research. Cannot assume knowledge. Must cite sources.

**Once approved, I will:**
- Update CHECKPOINT-REGISTRY-v1.0.md → v1.1
- Document version history
- Implement in next research session
- **When you point out errors, Checkpoint 0.0 will automatically trigger**
- **RESTART Morocco flight research from NEW Checkpoint 1.1**

---

## 📚 LESSONS LEARNED

**From Morocco trip failures:**

1. **Verification BEFORE recommendations** - Never assume availability
2. **Tool limitations matter** - Know what Claude can/cannot verify
3. **User partnership required** - Screenshots prove what exists
4. **Total costs not base fares** - Budget airlines hide costs
5. **Gates prevent rushing** - Mandatory waits ensure quality
6. **HTML removes barriers** - No technical tools needed
7. **Evidence trumps assumptions** - "Route exists" ≠ "date has flight"

---

**Status:** AWAITING USER APPROVAL  
**Next Step:** User reviews and approves/modifies proposed updates  
**Then:** Update checkpoint registry to v1.1

