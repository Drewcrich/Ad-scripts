# 🎬 AI Guide for Creating PrimeBite Scripts

**Purpose:** Everything a fresh AI needs to create high-quality Sora 2 video scripts for PrimeBite Fishing app.

---

## 🎯 Your Mission

Create entertaining fishing content that:
1. **Entertains first** (content-first, not advertisements)
2. **Integrates PrimeBite naturally** (as part of the story)
3. **Includes AI transparency** (builds trust)
4. **Follows all critical rules** (documented below)

---

## 🚨 CRITICAL RULES (Never Skip These)

1. **CLIP DURATIONS: ONLY 10s OR 15s** - Sora 2 cannot generate 12s, 13s, 14s, 20s, or any other duration
2. **ALWAYS include background music** in every prompt (epic, upbeat, chill, soft, action)
3. **DIALOGUE LIMITS** - Max 25-30 words for 10s clips, 35-45 words for 15s clips (2.5-3 words/sec)
4. **KEEP PROMPTS SHORT** - Remove unnecessary details (clothing, extra actions) for better generation
5. **AVOID COMPLEX PHYSICS** - No "line screaming out", minimize simultaneous actions (fighting + reeling)
6. **Fish on deck only** - never show fish in water (Sora struggles with this)
7. **Small crowds** - maximum 2-3 people (large groups look fake)
8. **Add AI transparency** to all realistic UGC videos (mandatory final clip or text overlay)
9. **Use "PASTE FROM HERE" markers** in all Sora prompts for clarity
10. **Character diversity** - vary age, gender, appearance across scripts
11. **Water continuity** - Specify "calm water" across clips to maintain consistency
12. **Emphasize "bite windows" and "bite ratings"** in dialogue (not just "real data")

---

## ❌ Common Mistakes to Avoid

1. ❌ Using 12s, 13s, 14s, or 20s durations (MOST COMMON)
2. ❌ Forgetting background music (CRITICAL)
3. ❌ Too much dialogue (>30 words in 10s clips causes audio hallucination)
4. ❌ Over-detailed prompts (remove lighting, expressions, UGC feel notes - keep it simple, let Sora fill in details)
5. ❌ Complex physics (avoid "line screaming", "bent HARD", simultaneous actions)
6. ❌ Casting actions (difficult for Sora - use reeling or static holding instead)
7. ❌ Showing fish in water (looks fake)
8. ❌ Generic dialogue ("real data" instead of "bite windows")
9. ❌ Skipping AI transparency (builds distrust)
10. ❌ Long storyboard scene descriptions (causes failures - keep to 1-2 sentences)

---

## ✅ What Sora 2 Does Well

- Natural human interactions (2-3 people max)
- Direct-to-camera dialogue with gestures
- Stationary or slow-moving subjects
- Fish on deck, in net, or being held
- Beautiful water shots, golden hour lighting
- POV perspectives (first-person)
- Background music + dialogue simultaneously
- Simple actions: reeling, holding rod, talking

---

## ❌ What Sora 2 Struggles With

- Fish in water (looks fake - AVOID)
- Large crowds (8-10+ people)
- Complex fish jumps mid-fight
- Over-detailed prompts (too many details overwhelm Sora and cause generation failures)
- **Casting actions** (rod motion, lure splash - difficult to generate cleanly)
- **Invisible line physics** ("line screaming out" - Sora can't see fishing line)
- **Complex rod bending** ("bent HARD in deep curve" - too much detail causes issues)
- **Simultaneous actions** (fighting + reeling at same time)
- **Too much dialogue** (>3.5 words/sec causes audio hallucination)

---

## 🛠️ Solutions & Best Practices

**For fish:** Keep on deck, in net, or held briefly  
**For crowds:** Maximum 2-3 people  
**For continuity:** Specify water conditions ("calm water") across clips  
**For prompts:** Keep short and focused (3-5 sentences for clips)  
**For casting:** Use reeling or static rod holding instead  
**For physics:** Simplify to "rod bent" or "holding rod" - avoid detailed physics  
**For dialogue:** Count words! 10s = max 30 words, 15s = max 45 words  
**For clothing/details:** Remove unless critical - let Sora decide

---

## ⚠️ CRITICAL: Keep Prompts Simple (Over-Detailing Breaks Sora)

**Problem:** Too many details overwhelm Sora and cause generation failures or poor quality.

**Solution:** Include ONLY the essentials. Let Sora fill in the rest naturally.

### ❌ BAD Example (Over-Detailed):
```
Vertical selfie video filmed on a phone. Same fisherman, now on a boat in bright mid-day sun. Calm water visible in background. He's holding a nice walleye with both hands, fish clearly visible. He looks amazed and excited. It should feel like authentic TikTok UGC: slight phone shake, natural bright lighting, phone-mic audio.

He speaks with excitement and disbelief: "[dialogue]"

Keep his delivery excited but still genuine—he's sharing a real discovery, not hyping anything. Upbeat background music plays (lower volume so his voice is clear). Include subtle water sounds. Leave clean space in the upper-right corner so I can add a screenshot overlay later.
```

### ✅ GOOD Example (Simplified):
```
Vertical selfie video filmed on a phone. Same fisherman on a boat, holding a walleye with both hands.

He speaks: "[dialogue]"

Upbeat background music plays (lower volume so his voice is clear). Leave clean space in the upper-right corner for overlay.
```

### What to Remove:
- ❌ Lighting details ("bright mid-day sun", "golden morning light")
- ❌ Background descriptions ("calm water visible in background")
- ❌ Facial expressions ("looks amazed and excited")
- ❌ UGC feel notes ("slight phone shake", "natural lighting", "phone-mic audio")
- ❌ Delivery instructions ("Keep his delivery excited but still genuine")
- ❌ Ambient sound details ("Include subtle water sounds")
- ❌ Redundant descriptions ("fish clearly visible")

### What to Keep:
- ✅ Format ("Vertical selfie video filmed on a phone")
- ✅ Character ("Same fisherman")
- ✅ Location ("on a boat")
- ✅ Essential action ("holding a walleye")
- ✅ Dialogue
- ✅ Background music (required)
- ✅ Overlay space note (needed for CapCut)

**Rule of Thumb:** If Sora can infer it from context, don't specify it. Less is more.  

---

## 🎵 Background Music (MANDATORY)

**Always include music in your prompts:**

**For action/cinematic:**
- "Epic cinematic music plays in the background"
- "Action music with building intensity"

**For UGC content:**
- "Upbeat background music plays throughout"
- "Chill fishing music in background"

**For educational:**
- "Soft background music"

**Audio Balance:** Always specify "music volume is lower so voice is clear" when combining dialogue + music.

---

## 📋 Lean Script Template

Use this structure for ALL scripts:

```markdown
# Script XXX – [Title]

**Species:** [Species]  
**Style:** UGC Epic Moment / UGC Educational / Cinematic  
**Platforms:** TikTok, YouTube Shorts, Instagram Reels  
**Total Length:** [XX seconds] ([Xs + Xs + Xs])

---

## Clip 1 – [Name] ([Duration])

**📋 PASTE FROM HERE ↓**

Vertical selfie video filmed on a phone. A mid-30s fisherman on a boat.

He speaks: "[dialogue here - max 30 words for 10s, 45 words for 15s]"

Upbeat background music plays (lower volume so his voice is clear). Leave clean space in top-right corner for overlay.

**↑ TO HERE 📋**

**Duration:** [10s or 15s] | **Orientation:** Portrait

**Character Note:** Create character in Sora 2. Save/reference for other clips.

---

## Clip 2 – [Name] ([Duration])

**📋 PASTE FROM HERE ↓**

[Same structure as Clip 1]

**↑ TO HERE 📋**

**Duration:** [10s or 15s] | **Orientation:** Portrait

**Character Note:** Use same character from Clip 1.

---

## Clip 3 – AI Disclosure & CTA ([Duration])

**📋 PASTE FROM HERE ↓**

Vertical selfie video filmed on a phone. Same fisherman on a boat.

He speaks: "Quick note: This video is AI-generated, but PrimeBite's predictions are 100% real. [Brief CTA - max 30 words total]"

Soft background music plays (lower volume so his voice is clear). Leave clean space in top-right corner for overlay.

**↑ TO HERE 📋**

**Duration:** 10 seconds | **Orientation:** Portrait

---

## CapCut Instructions

**Clip 1 (0-Xs):**
- At [X]s: Add Today Tab bite-window screenshot (top-right corner)
- Size: 30-35% of screen width
- Show from [X]s to [X]s with fade in/out (0.3s)

**Clip 2 (X-Xs):**
- [Overlay/text instructions with specific timings]

**Clip 3 (X-Xs):**
- At [X]s: Add text center-bottom: "🤖 AI-Generated Video"
- At [X]s: Add text: "✅ PrimeBite Predictions = 100% Real"
- At [X]s: Add text: "📱 Download PrimeBite"

**Stitching:**
1. Import all clips into CapCut in order
2. Add 0.2s crossfade transitions between clips
3. Add screenshot overlays and text as specified
4. Adjust audio levels (dialogue clear over music)
5. Export vertical 9:16, 1080x1920 resolution

---

## Title/Caption

**Primary:** "[Attention-grabbing title with emoji] #species #fishing"

**Alternative:** "[Backup option]"

---

## Hashtags

`#species #fishing #fishingtiktok #fishinglife #fishingtips #bigfish #fishingapp #bitetime #solunar`

---

---

<details>
<summary>📊 Analytics & Testing Notes (Click to expand)</summary>

## Testing Focus

This script tests:
1. [Element being tested]
2. [Another element]

**Hypothesis:** [What you expect and why]

## Performance Tracking

**Log in analytics/shorts-log.csv:**
- script_id: Script_XXX_[name]
- video_length_s: [XX]
- hook_line: "[First line]"

**Success Metrics:**
- Target retention: 60%+ ([XX]s+ avg watch time)
- Compare to: [Similar script reference]

## Why This Script

**Based on analytics:**
- ✅ [Pattern from data]
- ✅ [Another pattern]

**New elements:**
- 🆕 [New thing being tested]

</details>
```

---

## 🐟 Species Available in App

**Freshwater:**
- Walleye
- Muskie (Muskellunge)
- Northern Pike

**Saltwater:**
- Yellowfin Tuna
- Bigeye Tuna
- Mahi Mahi (Dolphinfish)
- Black Marlin

❌ **Don't use:** Bass, Crappie, or any other species not listed

---

## 🎨 Content Mix Strategy

- **70% UGC** (Concept 07) - Proven format, drives trust
- **30% Cinematic** (Concept 06) - Diversifies content, tests new format

**UGC (User-Generated Content):**
- Vertical selfie video filmed on phone
- Raw, authentic feel
- Character talking to camera
- Natural lighting, phone shake
- Educational tips, testimonials, epic moments

**Cinematic:**
- POV action sequences
- Dramatic fishing moments
- Multiple scenes stitched
- Epic music, intense visuals

---

## 📊 How to Use Analytics

**Before creating a script:**

1. **Read `analytics/shorts-log.csv`**
2. **Identify top 3 performers** by:
   - `avg_view_duration_s` (retention)
   - `views_total` (reach)
   - Calculate retention: (avg_view_duration_s / video_length_s) × 100
3. **Read those top scripts** to understand:
   - Structure (clip count, length)
   - Tone (calm, energetic, excited)
   - Content type (tip, story, epic moment)
   - Hook lines (what grabs attention)
4. **Create new script** using insights from what works

**Target metrics:**
- **60%+ retention** is excellent
- **40-60%** is good
- **<40%** needs improvement

---

## 🎯 Quick Workflow

```
User: "Create Script [NUMBER]"

You:
1. Read this AI_GUIDE.md (you're reading it now ✅)
2. Read analytics/shorts-log.csv (see what's working)
3. Read top 3 performing scripts (learn patterns)
4. Create Script [NUMBER] using lean template above
5. Follow all critical rules (durations, dialogue limits, music, etc.)
6. Count dialogue words (10s = max 30, 15s = max 45)
7. Keep prompts short and simple
8. Include AI transparency clip
```

---

## 💡 Pro Tips

1. **Count dialogue words** - 10s clips: max 30 words, 15s clips: max 45 words
2. **Avoid complex physics** - No "line screaming", "rod bent HARD", simultaneous actions
3. **Simplify actions** - "Rod bent" not "casting", "holding rod" not "fighting + reeling"
4. **Water continuity** - Specify "calm water" across clips
5. **Remove unnecessary details** - Don't specify clothing, lighting, expressions, or UGC feel notes. Let Sora fill in details naturally.
6. **Use reeling instead of casting** - Easier for Sora to generate
7. **Keep prompts focused** - 3-5 sentences max per clip
8. **Always include music** - Dramatically improves engagement
9. **AI transparency builds trust** - Always include disclosure

---

## 🔗 Additional Resources

**For moon phase science:** Read `RESEARCH_HUB.md`  
**For app screenshots:** Check `screenshots/SCREENSHOT_REFERENCE.md`  
**For concept details:** Read `concepts/Concept_06_Cinematic_Fishing_Moments.md` or `Concept_07_UGC_Fisherman_Testimonial.md`  

---

**🎬 You're ready to create amazing fishing content! 🎣**

