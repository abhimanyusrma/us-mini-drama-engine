# TROUBLESHOOTING & EDGE CASES LOG V1.0

This document tracks visual, structural, and technical fixes for the automated VideoExpress workflow. If the browser agent encounters an error or produces a low-quality output, reference these fixes immediately.

## 1. VISUAL GLITCHES & CHARACTER DRIFT

### Symptom: Character faces or outfits change drastically between shots.
- **Fix:** Enforce the "Seed + Reference" lock. Instruct the agent to copy the **Seed Number** of the character’s very first approved generated image. For all subsequent shot prompts, force the agent to append: `[Insert base prompt], maintaining exact facial structures and clothing from Seed: [Seed Number], matching the style of Video 1.`
- **Alternative Fix:** Simplify clothing. Complex patterns (stripes, logos) cause AI drift. Force the agent to write wardrobe prompts using solid, simple colors (e.g., "wearing a solid navy blue blazer and white undershirt").

### Symptom: Characters look like they belong in a generic global soap opera instead of a US drama.
- **Fix:** Aggressive cultural prompt injection. Force the agent to add specific US styling modifiers: "Contemporary American street fashion, sharp cinematic contrast, styled like an HBO drama series, authentic US location styling."

## 2. TIMELINE & PACING ISSUES

### Symptom: The video feels sluggish or characters stare blankly at the start/end of clips.
- **Fix:** Boost the trim velocity. The standard 40 px/s trim leaves too much "dead air" for fast-paced US shorts. Instruct the browser agent to manually adjust the timeline zoom and execute the Cut + Delete tool at **55 px/s** or **60 px/s**. The dialogue should clip the absolute first frame of mouth movement.

### Symptom: The twist happens too late, causing viewers to swipe away early.
- **Fix:** Truncate Stage 2. If the video timeline runs past 50 seconds, instruct the agent to delete the two least critical context shots in the middle of the timeline, slide the remaining clips together, and force a punchier 40–45 second export.

## 3. BROWSER AGENT & UI ERRORS

### Symptom: The agent gets stuck in a loop or states it "cannot find the timeline button."
- **Fix:** Refresh and map. VideoExpress updates its web UI periodically. If a button element changes, tell the agent: `Pause automation. Take a screenshot of the current page, analyze the layout, locate the new selector for the [Timeline/Export/Generate] button, and proceed with the new coordinate/element path.`

### Symptom: Parallel rendering cap hit (VideoExpress limits simultaneous renders).
- **Fix:** Queue management. When VideoExpress throws a "Maximum parallel generations reached" pop-up, instruct the agent to pause for 15 seconds, check the status of the top 3 rendering bars, and only hit the "Generate" button for the next clip once an active slot clears.

