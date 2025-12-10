# PrimeBite Research Document for Sora 2 Video Prompts

**Last Updated:** 2025-11-03 · Research v1.4

This document contains all species-specific information, weather preferences, moon phase data, and sources needed for generating Sora 2 video prompts about fishing conditions.

---

## Table of Contents

1. [General Profile (Baseline)](#general-profile)
2. [Species-Specific Profiles](#species-specific-profiles)
   - [Walleye](#walleye)
   - [Muskellunge (Muskie)](#muskellunge)
   - [Northern Pike](#northern-pike)
   - [Yellowfin Tuna](#yellowfin-tuna)
   - [Mahi-mahi](#mahi-mahi)
   - [Black Marlin](#black-marlin)
   - [Bigeye Tuna](#bigeye-tuna)
3. [Weather Conditions](#weather-conditions)
4. [Moon Phases & Solunar Windows](#moon-phases--solunar-windows)
5. [Sources & Citations](#sources--citations)

---

## General Profile (Baseline)

**What it is:** A balanced baseline profile that works reasonably well for most freshwater predatory fish when species-specific data isn't available.

### When Fish Are More Likely to Bite

- **Moon Position (Majors/Minors):** YES - Uses overhead/underfoot (majors) and moonrise/moonset (minors)
- **Best Moon Phases:** New moon and Full moon (peaks at new/full, moderate boost at gibbous phases)
- **Best Times of Day:** 
  - Major periods: ~2-hour windows when moon is overhead/underfoot
  - Minor periods: ~1-hour windows at moonrise/moonset
  - No specific time-of-day bias (works all day)
- **Best Seasons:** Year-round (no seasonal multipliers - 1.0 for all months)

### Weather Preferences

- **Wind:** No weather effects in baseline (windPenalty: 0)
- **Precipitation:** No weather effects in baseline (precipPenalty: 0)
- **Barometric Pressure:** No weather effects in baseline (pressureBonus: 0)

### Moon Phase Details

- **Phase Model:** Standard solunar theory
- **Phase Weight:** 1.0 (moderate moon sensitivity)
- **Majors/Minors:** Enabled
- **Base Scores:** Major: 7.5, Minor: 5.5 (on 0-10 scale, but uses 1-5 rating system)

### Key Characteristics

- Uses traditional solunar theory (new/full moon peaks)
- No species-specific time-of-day preferences
- No weather adjustments
- Conservative baseline for general fishing

---

## Species-Specific Profiles

### Walleye

**Evidence Tier:** A (Strong evidence)

#### When Walleye Are More Likely to Bite

- **Moon Position (Majors/Minors):** YES - Strongest during overhead/underfoot periods
  - ~10-12% more likely to be successful when moon is overhead/underfoot
- **Best Moon Phases:** **Gibbous phases (waxing/waning gibbous)** perform best; quarter phases lowest
- **Best Times of Day:** **Dawn and Dusk** (low-light preference)
  - Low-light boost peaks at sunrise/sunset, fades over ~120 minutes
  - Dawn/dusk and lower solar radiation improve success

#### Weather Preferences

- **Wind:** Generic penalty model - penalty per 5 mph over 10 mph
- **Precipitation:** Penalty when precipitation chance > 70% (penalty: 0.76)
- **Barometric Pressure:** Bonus for falling pressure (pressureBonus: 0.15)

#### Moon Phase Details

- **Phase Model:** Standard (peaks at new/full, but gibbous strongest in research)
- **Phase Weight:** 1.52 (high sensitivity)
- **Majors/Minors:** Enabled
- **Base Scores:** Major: 4.18, Minor: 3.04 (on 0-10 scale)
- **Overlap Windows:** ±25 minutes (inner), ±55 minutes (outer) around sunrise/sunset

#### Best Conditions Summary

- **Time:** Dawn or dusk (within 2 hours of sunrise/sunset)
- **Moon:** Gibbous phases with moon overhead/underfoot
- **Weather:** Calm conditions, falling barometric pressure, low precipitation
- **Season:** Peak months: March (1.1x), April (1.15x), May (1.3x), June (1.15x), September (1.15x)

#### Research Source

Shaw et al. (2021). Lunar and crepuscular timing of walleye angling success. PLOS ONE.
- Single-lake creel dataset (Escanaba Lake, 2003-2015)
- Effects small but robust after controls

---

### Muskellunge (Muskie)

**Evidence Tier:** A (Strong evidence)

#### When Muskie Are More Likely to Bite

- **Moon Position (Majors/Minors):** YES - Uses overhead/underfoot and moonrise/moonset
- **Best Moon Phases:** **Full moon and New moon** (strongest peaks)
- **Best Times of Day:** **Night** (effects strengthen significantly at night)
  - Predicted maximum relative effect ≈ 28% at night overall
  - ≈ 5% overall effect during day
  - Night bias: +0.57 boost at night

#### Weather Preferences

- **Wind:** Generic penalty model - penalty per 5 mph over 10 mph
- **Precipitation:** Penalty when precipitation chance > 70%
- **Barometric Pressure:** Bonus for falling pressure

#### Moon Phase Details

- **Phase Model:** Standard (peaks at new/full)
- **Phase Weight:** 1.33 (moderate-high sensitivity)
- **Majors/Minors:** Enabled
- **Base Scores:** Major: 3.99, Minor: 2.85 (on 0-10 scale)
- **Overlap Windows:** ±30 minutes (inner), ±60 minutes (outer) around sunrise/sunset

#### Best Conditions Summary

- **Time:** Night (before 6 AM or after 6 PM)
- **Moon:** Full or new moon with moon overhead/underfoot
- **Weather:** Calm conditions, falling barometric pressure
- **Season:** Peak months: March (1.2x), April (1.4x), May (1.3x), June (1.2x)

#### Research Source

Vinson & Angradi (2014). Musky madness: Do anglers catch more muskies during a full moon? PLOS ONE.
- Large North American dataset (341,959 catches)
- Effort confounding discussed (anglers fish more near full/new moons)

---

### Northern Pike

**Evidence Tier:** A (Strong evidence)

#### When Pike Are More Likely to Bite

- **Moon Position (Majors/Minors):** YES - Uses overhead/underfoot and moonrise/moonset
- **Best Moon Phases:** Full/New moons (modest signal)
- **Best Times of Day:** **Dusk** (strongest tendency regardless of phase)
  - Dusk-only boost: +0.38 near sunset (triangular peak within ±90 minutes)
  - Dusk increased CPUE in research
  - Night bias: +0.38 at night

#### Weather Preferences

- **Wind:** **POSITIVE MODEL** (unique to pike)
  - Boost at 8-15 mph (peak around 12 mph)
  - Penalty only when wind > 20 mph
  - Wind speed was positively correlated with CPUE
- **Precipitation:** Penalty when precipitation chance > 70%
- **Barometric Pressure:** **NO pressure bonus** (unlike other species)

#### Moon Phase Details

- **Phase Model:** Standard (peaks at new/full, but modest effect)
- **Phase Weight:** 1.045 (lower sensitivity)
- **Majors/Minors:** Enabled
- **Base Scores:** Major: 3.8, Minor: 2.66 (on 0-10 scale)
- **Overlap Windows:** ±35 minutes (inner), ±65 minutes (outer) around sunrise/sunset

#### Best Conditions Summary

- **Time:** Dusk (within 90 minutes of sunset) or night
- **Moon:** Full or new moon with moon overhead/underfoot
- **Weather:** **Moderate wind (8-15 mph is beneficial)**, low precipitation
- **Season:** Peak months: March (1.2x), April (1.3x), May (1.2x), June (1.1x)

#### Research Source

Kuparinen et al. (2010). Abiotic and fishing-related correlates of angling catch rates in pike (Esox lucius). Fisheries Research.
- European waterbodies
- GLM model explained ~19.2% deviance (most variation is environmental)
- Cooler water also helpful

---

### Yellowfin Tuna

**Evidence Tier:** A (Strong evidence)

#### When Yellowfin Tuna Are More Likely to Bite

- **Moon Position (Majors/Minors):** **NO** - Phase-only pattern (majors/minors disabled)
- **Best Moon Phases:** **New moon → First Quarter** (consistent peak in tournament data)
- **Best Times of Day:** No specific time-of-day bias

#### Weather Preferences

- **Wind:** Generic penalty model - penalty per 5 mph over 10 mph
- **Precipitation:** Penalty when precipitation chance > 70%
- **Barometric Pressure:** Bonus for falling pressure

#### Moon Phase Details

- **Phase Model:** Yellowfin-mahi (ramp from new to first quarter)
- **Phase Weight:** 1.33
- **Majors/Minors:** **Disabled** (phase-only scoring)
- **Base Scores:** Same for all periods (phase-only)

#### Best Conditions Summary

- **Time:** Any time of day
- **Moon:** New moon transitioning to first quarter
- **Weather:** Calm conditions, falling barometric pressure
- **Season:** Year-round (no seasonal multipliers)

#### Research Source

Lowry et al. (2007). Relationship between lunar phase and catch rates of yellowfin tuna in eastern Australia. Fisheries Research.
- 145 tournaments (381 days) in Australia
- Periodic regression found consistent peak from new to first quarter
- No position effect reported for overhead/underfoot

---

### Mahi-mahi

**Evidence Tier:** A (Strong evidence)

#### When Mahi-mahi Are More Likely to Bite

- **Moon Position (Majors/Minors):** **NO** - Phase-only pattern (majors/minors disabled)
- **Best Moon Phases:** **New moon → First Quarter** (same pattern as yellowfin)
- **Best Times of Day:** Night availability boost (+0.285)

#### Weather Preferences

- **Wind:** Generic penalty model - penalty per 5 mph over 10 mph
- **Precipitation:** Penalty when precipitation chance > 70%
- **Barometric Pressure:** Bonus for falling pressure

#### Moon Phase Details

- **Phase Model:** Yellowfin-mahi (ramp from new to first quarter)
- **Phase Weight:** 1.33
- **Majors/Minors:** **Disabled** (phase-only scoring)
- **Base Scores:** Same for all periods (phase-only)

#### Best Conditions Summary

- **Time:** Night preferred (night availability boost)
- **Moon:** New moon transitioning to first quarter
- **Weather:** Calm conditions, falling barometric pressure
- **Season:** Year-round (no seasonal multipliers)

#### Research Source

Lowry et al. (2007). Relationship between lunar phase and catch rates of yellowfin tuna in eastern Australia. Fisheries Research.
- Same dataset as yellowfin tuna
- Consistent phase pattern

---

### Black Marlin

**Evidence Tier:** A (Strong evidence)

#### When Black Marlin Are More Likely to Bite

- **Moon Position (Majors/Minors):** **NO** - Phase-only pattern (majors/minors disabled)
- **Best Moon Phases:** **Full moon → Last Quarter** (NSW dataset pattern)
- **Best Times of Day:** No specific time-of-day bias

#### Weather Preferences

- **Wind:** Generic penalty model - penalty per 5 mph over 10 mph
- **Precipitation:** Penalty when precipitation chance > 70%
- **Barometric Pressure:** Bonus for falling pressure

#### Moon Phase Details

- **Phase Model:** Black-marlin-quarters or NSW variant
- **Phase Weight:** 1.235
- **Majors/Minors:** **Disabled** (phase-only scoring)
- **Base Scores:** Same for all periods (phase-only)

#### Best Conditions Summary

- **Time:** Any time of day
- **Moon:** Full moon transitioning to last quarter
- **Weather:** Calm conditions, falling barometric pressure
- **Season:** Peak months: March (1.1x), April (1.2x), May (1.2x), June (1.1x) - GBR spring-early summer aggregation

#### Research Source

Lowry et al. (2007). Relationship between lunar phase and catch rates of yellowfin tuna in eastern Australia. Fisheries Research.
- Tournament dataset
- Species-specific pattern (blue/striped marlin showed no significant lunar trend)

---

### Bigeye Tuna

**Evidence Tier:** A (Strong evidence)

#### When Bigeye Tuna Are More Likely to Bite

- **Moon Position (Majors/Minors):** **NO** - Phase-only pattern (majors/minors disabled)
- **Best Moon Phases:** **Full moon** (sharp peak in longline CPUE data)
- **Best Times of Day:** Night availability boost (+0.38) - deep-water feeding patterns

#### Weather Preferences

- **Wind:** Generic penalty model - penalty per 5 mph over 10 mph
- **Precipitation:** Penalty when precipitation chance > 70%
- **Barometric Pressure:** Bonus for falling pressure

#### Moon Phase Details

- **Phase Model:** Bigeye-full (sharp peak near full moon)
- **Phase Weight:** 1.425 (high sensitivity)
- **Majors/Minors:** **Disabled** (phase-only scoring)
- **Base Scores:** Same for all periods (phase-only)

#### Best Conditions Summary

- **Time:** Night preferred (night availability boost for deep-water feeding)
- **Moon:** Full moon
- **Weather:** Calm conditions, falling barometric pressure
- **Season:** Year-round (no seasonal multipliers)

#### Research Source

Jatmiko et al. (2016). Influence of lunar phase on bigeye tuna catch in the Eastern Indian Ocean. ILMU KELAUTAN.
- Longline observer data
- Significant CPUE differences among phases; full highest
- ANOVA + Tukey test showed significance

---

## Weather Conditions

### Wind Effects by Species

1. **Northern Pike:** POSITIVE MODEL (unique)
   - 8-15 mph: Boost (peak around 12 mph)
   - > 20 mph: Penalty
   - Wind creates surface chop that helps pike hunting

2. **All Other Species:** GENERIC PENALTY MODEL
   - ≤ 10 mph: No effect
   - > 10 mph: Penalty per 5 mph increment
   - Example: 15 mph = -1 penalty, 20 mph = -2 penalty

3. **General Profile:** No wind effects

### Precipitation Effects

- **All Species (except General):** Penalty when precipitation chance > 70%
- **General Profile:** No precipitation effects

### Barometric Pressure Effects

- **Most Species:** Bonus for falling pressure (indicates approaching weather front)
- **Northern Pike:** NO pressure bonus (unlike other species)
- **General Profile:** No pressure effects

---

## Moon Phases & Solunar Windows

### Moon Phases Explained

- **New Moon:** 0% illumination - Moon between Earth and Sun
- **Waxing Crescent:** 1-49% illumination (growing)
- **First Quarter:** 50% illumination
- **Waxing Gibbous:** 51-99% illumination (growing toward full)
- **Full Moon:** 100% illumination
- **Waning Gibbous:** 99-51% illumination (shrinking from full)
- **Last Quarter:** 50% illumination
- **Waning Crescent:** 49-1% illumination (shrinking toward new)

### Solunar Windows

**Major Windows:**
- When moon is **overhead** (highest point in sky) or **underfoot** (lowest point, opposite side of Earth)
- Duration: ~2 hours (±60 minutes around peak)
- Strongest bite periods for freshwater species

**Minor Windows:**
- When moon is **rising** or **setting** (crossing horizon)
- Duration: ~1 hour (±30 minutes around horizon crossing)
- Secondary bite periods

### Phase Models by Species

1. **Standard Model:** Peaks at new/full moons
   - Used by: General, Walleye, Muskie, Pike
   - Formula: strength = max(0, 1 − 4 × |fraction − 0.5|²)

2. **Yellowfin-Mahi Model:** Ramp from new to first quarter
   - Used by: Yellowfin Tuna, Mahi-mahi

3. **Black Marlin Model:** Peak from full to last quarter
   - Used by: Black Marlin

4. **Bigeye-Full Model:** Sharp peak at full moon
   - Used by: Bigeye Tuna

---

## Sources & Citations

### Peer-Reviewed Research Papers

1. **Shaw, S.L. et al. (2021).** Lunar and crepuscular timing of walleye angling success. PLOS ONE.
   - URL: https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0257882
   - Key Finding: ~10-12% higher success with overhead/underfoot; gibbous strongest; dawn/dusk positive
   - Dataset: Escanaba Lake creel data (2003-2015)

2. **Vinson, M.R. & Angradi, T.R. (2014).** Musky madness: Do anglers catch more muskies during a full moon? PLOS ONE.
   - URL: https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0098046
   - Key Finding: Full/new peaks; ~28% at night overall; ~5% overall; effort confounding discussed
   - Dataset: 341,959 catches across North America

3. **Kuparinen, A. et al. (2010).** Abiotic and fishing-related correlates of angling catch rates in pike (Esox lucius). Fisheries Research.
   - URL: https://www.agrar.hu-berlin.de/de/institut/departments/dntw/jp_bfm/publ_html/kuparinen-et-al-2010/@@download/file/kuparinenetal_fishres_2010.pdf
   - Key Finding: Dusk positive; wind positive; modest lunar phase; ~19.2% deviance explained
   - Dataset: European waterbodies, GLM analysis

4. **Lowry, M. et al. (2007).** Relationship between lunar phase and catch rates of yellowfin tuna in eastern Australia. Fisheries Research.
   - URL: https://www.sciencedirect.com/science/article/abs/pii/S0165783607001634
   - Key Finding: New→first quarter peak for yellowfin/mahi; black marlin differs; position effects not supported
   - Dataset: 145 tournaments (381 days) in Australia

5. **Jatmiko, I. et al. (2016).** Influence of lunar phase on bigeye tuna catch in the Eastern Indian Ocean. ILMU KELAUTAN.
   - URL: https://ejournal.undip.ac.id/index.php/ijms/article/view/10245
   - Key Finding: Full-moon peak; significant CPUE differences among phases
   - Dataset: Longline observer data, Eastern Indian Ocean

### Methods References

6. **Maunder, M.N. & Punt, A.E. (2004).** Standardizing catch and effort data: a review of recent approaches. Fisheries Research.
   - URL: https://www.sciencedirect.com/science/article/abs/pii/S0165783604001638
   - Key Note: CPUE standardization best practices and interpretation

### Context References

7. **NOAA Tidal Currents Tutorial**
   - URL: https://oceanservice.noaa.gov/education/tutorial_currents/02tidal1.html

8. **NOAA: Why fishermen monitor currents**
   - URL: https://oceanservice.noaa.gov/education/tutorial_tides/tides09_monitor.html

---

## Quick Reference: Best Conditions by Species

| Species | Best Moon Phase | Best Time of Day | Majors/Minors? | Best Weather |
|---------|----------------|------------------|----------------|--------------|
| **General** | New/Full | Any | Yes | N/A (no weather effects) |
| **Walleye** | Gibbous | Dawn/Dusk | Yes | Calm, falling pressure |
| **Muskie** | Full/New | Night | Yes | Calm, falling pressure |
| **Pike** | Full/New | Dusk/Night | Yes | **Moderate wind (8-15 mph)** |
| **Yellowfin** | New→1st Q | Any | No | Calm, falling pressure |
| **Mahi** | New→1st Q | Night | No | Calm, falling pressure |
| **Black Marlin** | Full→Last Q | Any | No | Calm, falling pressure |
| **Bigeye** | Full | Night | No | Calm, falling pressure |

---

**Document Version:** 1.4  
**Last Updated:** 2025-11-03  
**Source:** PrimeBite Research Hub (docs/RESEARCH_HUB.md)

