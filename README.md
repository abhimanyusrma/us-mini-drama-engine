# US Short-Form Drama Engine 🎬 🇺🇸

This is a proprietary, closed-loop workflow framework designed to generate high-retention, 9:16 vertical mini-dramas for the US YouTube Shorts, Instagram Reels, and TikTok markets. It leverages a browser automation agent to execute asset generation, pacing structures, and timeline edits cost-effectively inside VideoExpress.ai.

## 🚀 Quick Start Workflow (Under 3 Minutes)

1. **Sign In:** Open your browser and log into [VideoExpress.ai](https://videoexpress.ai).
2. **Launch Agent Workspace:** Open a web-browsing capable agent window:
   - **ChatGPT Desktop App:** Ensure `Settings` -> `General` -> `Permissions` -> `Full Access` is enabled.
   - **Claude:** Use the Chrome browser interface or Claude Desktop with automation enabled.
3. **Trigger the Engine:** Copy the text block inside `US_SYSTEM_PROMPT.md` from this repository and paste it into your AI agent chat.
4. **Input the Variables:** When the agent responds, provide it with your creative parameters:
   - **Topic:** (e.g., *A corporate assistant exposes that her boss stole her project pitch during a live board meeting*)
   - **Target Aesthetic:** (e.g., *Grit-cinematic, high-contrast, modern New York office setting*)
5. **Production:** Wait for the agent to construct the script, generate consistent visual frames, perform the timeline assembly, execute aggressive dead-air trimming, and output the final video.

## 📊 US Optimization Parameters (Engine Rules)

Unlike standard global workflows, this engine hardcodes specific constraints optimized strictly for US viewer retention mechanics:
- **1.5-Second Visual Hook:** Eliminates preamble shots. Forces instant emotional or physical stakes.
- **5-Word Dialogue Limit:** Enforces rapid-fire pacing suitable for fast-skimming American mobile audiences.
- **50 px/s Aggressive Trim:** Slices trailing and leading dead frames out of video assets for relentless pacing.
- **Geographic Anchoring:** Automates the inclusion of recognizable US backdrops within the generation prompt layers.

## 📁 Repository Structure

- `US_SYSTEM_PROMPT.md` - The initial lightweight trigger prompt fed to the LLM agent.
- `CORE_PLAYBOOK.md` - The underlying ruleset defining narrative beats, visual routing, and editor specifications.
- `TROUBLESHOOTING.md` - Operational log for system overrides and visual consistency corrections.

