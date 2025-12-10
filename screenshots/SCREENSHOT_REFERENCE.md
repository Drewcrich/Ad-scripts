# PrimeBite App Screenshot Reference

This document catalogs the available app screenshots and provides guidance on which screenshots to use for different script types and overlay placements.

## Available Screenshots

### 1. Today Tab - General Species (Bite Windows Card)
**Best for:** Most UGC videos showing bite windows
**Key Elements:**
- Day Rating (e.g., "2.4/5 Fair")
- Target Species selector (General, Freshwater, Offshore)
- Bite Windows list with times and ratings:
  - Minor periods (moonrise/moonset)
  - Major periods (moon overhead/underfoot)
  - Each shows time range and rating (e.g., "Major — 2.7/5 Good from 9:20 AM – 11:20 AM")
- Sunrise/Sunset times
- Moon phase percentage
- Explanation text about Major/Minor periods

**When to use:**
- Scripts mentioning "bite window" or "timing chart"
- Videos showing "checking the window before going out"
- Educational content about when fish are active
- Testimonial videos showing the app predicted correctly

**Overlay placement:** Top-right corner, ~25-30% of screen width
**Timing:** Show during mentions of timing, windows, or checking the app

---

### 2. Today Tab - Offshore Species (24-Hour Activity Timeline)
**Best for:** Videos showing activity patterns throughout the day
**Key Elements:**
- 24-Hour Activity Timeline graph
- Activity percentage visualization (0-100%)
- Peaks labeled with percentages (e.g., "42%" at 10 AM)
- Sunrise/Sunset vertical lines
- "Now" indicator showing current time
- Status bar showing "Major in progress • until 11:50 PM"
- Legend for Sunrise (yellow), Sunset (pink), Now (teal)

**When to use:**
- Videos explaining activity patterns
- Content showing "this is when they're most active"
- Educational content about fishing timing
- When you want to show visual data rather than just times

**Overlay placement:** Can be larger, center or top-right
**Timing:** Show when explaining activity patterns or optimal times

---

### 3. Logbook Tab - Log a Catch Form
**Best for:** Videos about tracking catches or using the app to log results
**Key Elements:**
- "Log a Catch" form
- Current Conditions (auto-filled): Moon phase, Sunrise, Sunset, Location
- Input fields: Species, Waterbody, Gear, Bait/Lure, Weight, Notes
- "Add Photo" and "Location Added" options
- "Save Catch" button

**When to use:**
- Videos about logging successful catches
- Content showing "I caught this and logged it"
- Follow-up videos after showing a catch
- Educational content about tracking fishing data

**Overlay placement:** Center or top-right
**Timing:** Show when mentioning logging catches or tracking results

---

### 4. Today Tab - Expanded Technical Details
**Best for:** Educational content explaining how the app works
**Key Elements:**
- Location information (Champaign, IL example)
- Day Rating with expanded "Why this rating" section
- Technical Details showing:
  - Step 1: Calculate today's total lift (Base lift, Phase lift, Overlap lift)
  - Step 2: Convert lift to rating (formula shown)
  - Explanation of why rating is "Fair"
- Target Species selector

**When to use:**
- Educational videos explaining the science behind PrimeBite
- Content for viewers who want to understand the methodology
- Videos emphasizing the app's accuracy and research-backed approach
- When you want to show transparency and technical credibility

**Overlay placement:** Center or full-screen for readability
**Timing:** Show when explaining how ratings are calculated

---

### 5. Research & Sources Page
**Best for:** Educational content about the app's scientific backing
**Key Elements:**
- "What PrimeBite Does" explanation
- "Why Trust It" section (cited sources, transparent math, validated data)
- "How to Read Bite Ratings" guide
- Quick Examples:
  - Moon Overhead: "Walleye trips are ~10-12% more successful"
  - Full/New Moon Nights: "Muskellunge show up to 28% relative lift"
  - Low-Light Bonus: Walleye and pike gain extra points
  - Weather Effects: Pike benefit from moderate wind, walleye sensitive to precipitation
- "Why Location Matters" explanation
- Complete list of source papers with publication details and access links

**When to use:**
- Educational videos about the science behind PrimeBite
- Content building trust and credibility
- Videos explaining why the app works
- When emphasizing research-backed methodology
- AI transparency clips when mentioning "all our sources" or "peer-reviewed research"

**Overlay placement:** Center or full-screen for readability
**Timing:** Show when explaining the science or building credibility

---

### 6. Technical Appendix
**Best for:** Deep-dive educational content showing the mathematical methodology
**Key Elements:**
- **Inputs Section:**
  - Location data (lat, lon, timezone from GPS)
  - Ephemerides (sunrise/sunset, moonrise/set, moon fraction, illumination)
  - Weather parameters (species-specific: wind speed, precipitation chance, pressure trend)
- **Solunar Windows:**
  - Majors: Moon altitude sampled every 5 minutes, ±60 minutes around transit
  - Minors: Horizon crossing detection, ±30 minutes window
- **Phase Weighting:**
  - Standard model strength formula: `max(0, 1 - 4 × |fraction – 0.5|²)`
  - Scaled by species phaseWeight
  - Offshore species use custom curves
- **Lift-Based Rating System:**
  - L_total formula: `L_total = L_base + L_phase + L_overlap + L_time + L_dusk + L_weather`
  - L_seasonal formula: `L_seasonal = L_total x seasonalMultiplier`
  - Rating formula: `Rating = 1 + 4 x (L_seasonal / L_REF)`
  - L_REF = 0.28 (theoretical maximum lift for exceptional conditions)
- **Species Modifiers Table:**
  - Shows species-specific modifiers (low-light bias, night bias, dusk boost, wind model, phase weight, phase model)
  - Includes source citations for each modifier (e.g., "Shaw 2021", "Kuparinen 2010")
- **Validation Notes:**
  - Timings cross-checked against public solunar tables (±1-2 min)
  - Spot checks with historical catch logs
  - Offshore phase curves validated with tournament and longline datasets
  - Location accuracy verified across multiple latitudes/longitudes

**When to use:**
- AI transparency clips when emphasizing "exactly how we calculate everything"
- Educational content explaining the mathematical methodology
- When viewers question the app's accuracy or want to see "the math"
- Scripts that mention "technical details" or "transparent calculations"
- Trust-building moments when emphasizing scientific rigor

**Overlay placement:** Center or full-screen for readability (formulas and tables need space)
**Timing:** Show during mentions of "how we calculate," "the math behind it," "technical details," or "exactly how we get our bite ratings"

---

### 7. Weather Tab - Current Conditions & Forecast
**Best for:** Videos mentioning weather conditions or weather impact on fishing
**Key Elements:**
- Current temperature and conditions (e.g., "43°F Foggy")
- Current Conditions details: Wind, Humidity, Cloud Cover, UV Index, Pressure, Precipitation, Visibility
- "Fishing Impact" section (e.g., "Moderate wind helps Pike activity")
- Hourly forecast with temperature and wind
- Daily forecast option

**When to use:**
- Videos mentioning weather conditions
- Content about how weather affects fishing
- Educational videos about weather factors
- When weather is a key part of the fishing story

**Overlay placement:** Top-right or center
**Timing:** Show when discussing weather conditions or their impact

---

## Screenshot Selection Guide by Script Type

### UGC Talking-Head (Scripts 001, 005)
**Recommended:** Screenshot #1 (Today Tab - Bite Windows)
- Simple, clear bite window display
- Easy to read in small overlay
- Directly relevant to "checking the window" narrative

### UGC Story/Before-After (Script 002)
**Recommended:** Screenshot #1 (Today Tab - Bite Windows)
- Shows the "before" - what they should have checked
- Can show specific window that worked

### UGC Testimonial (Script 003)
**Recommended:** Screenshot #1 (Today Tab - Bite Windows)
- Shows the window that "was right"
- Proves the app's accuracy

### UGC Tip + Payoff (Script 004)
**Recommended:** Screenshot #1 (Today Tab - Bite Windows)
- Shows the "timing chart" mentioned in the tip
- Can appear during both setup and payoff clips

---

## Overlay Best Practices

### Size & Position
- **Standard overlay:** 25-30% of screen width, top-right corner
- **Larger overlay (for graphs/details):** 40-50% of screen width, center or top
- **Full-screen (for educational):** Use sparingly, only when explaining complex concepts

### Timing
- **Fade in/out:** 0.2-0.3 seconds
- **Show duration:** 
  - Quick reference: 2-3 seconds
  - Detailed explanation: 5-8 seconds
  - Educational content: 8-12 seconds

### When to Show
- When fisherman mentions "checking the window"
- When explaining timing or bite windows
- When showing proof/app accuracy
- During payoff moments showing results
- When mentioning specific times or ratings

### What to Highlight
- **For quick references:** Just the bite windows list
- **For proof/testimonials:** Specific window time and rating
- **For educational:** Full card with explanation text
- **For activity patterns:** The 24-hour timeline graph

---

## Notes

- All screenshots should be cropped to remove iOS status bar (time, battery, etc.) when used as overlays
- For bite window overlays, crop to just show the black card with times and ratings
- Maintain aspect ratio when resizing
- Ensure text remains readable at overlay size
- Consider adding subtle border or shadow for visibility over video

---

## Future Screenshots to Consider

If creating new content, consider capturing:
- Screenshot with specific species selected (e.g., Walleye) showing species-specific windows
- Screenshot showing a "Good" or "Excellent" day rating for contrast
- Screenshot of a logged catch to show the tracking feature
- Screenshot showing different locations to emphasize location-specific calculations

