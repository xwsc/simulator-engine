# 🎬 SIMULATOR ENGINE (v1.2) — Director-Style SillyTavern Preset

A Chat Completion preset for **SillyTavern** that flips standard roleplay on its head: you don't play a single character—you act as the **Director**, an invisible voice giving stage directions while the AI simulates a self-consistent living world and every character in it, including `{{user}}` as a fully realized, autonomous NPC.

---

## ⚙️ How It Works

* **Director-to-Character Proxy:** Your inputs are treated as stage directions or intent, never literal dialogue. The AI authors the actual words and actions filtered through each character's personality, flaws, and current emotional state.
* **Passive Progression:** You can send an empty message (`Continue`) to let time pass and allow NPCs to act on their own drives without direct user intervention.
* **Character Autonomy & Veto:** Characters can flatly refuse, ignore, or oppose your cues if they violate their established psychology or boundaries—no softening or forced compliance.
* **Micro-Causality & State Persistence:** Enforces physical friction across beats (freeing occupied hands, removing outer layers, lingering cold/fatigue/residue, and unprompted subconscious habits).
* **Anti-Passivity Cap:** Hard limit of 2 consecutive reactive beats; on beat 3, characters must initiate an action, question, or contradiction.
* **Cognitive Bounds & Perception:** Characters only act on knowledge they personally possess, respecting line-of-sight, hearing distance, and physical constraints.
* **Dynamic Tone & Anti-Resolution:** Calibrates conflict tolerance to the scene register. Dramatic scenes resist premature closure and sit in tension; domestic/fluff scenes allow warmth to land without manufactured drama.
* **Prose Economy & Anti-Slop:** Bans common AI cliché phrases, rule-of-three lists, abstract emotion summaries, and caps repeated phrases/gestures at 2 uses per session.

---

## 🎛️ Modes & Optional Toggles

All modules can be toggled directly inside SillyTavern's **Prompt Manager**:

* **Normal Mode *(Default Active)*:** 5–6 beats (~300–500 words). Ends on an active hook to hand momentum back to the Director.
* **Chapter Mode *(Optional)*:** 12–18 continuous beats (~800–1,200 words). Pushes past natural breaks for long-form scene progression.
* **Scene Anchor *(Optional)*:** Appends a collapsible `💎 Scene Anchor` block tracking time, location, active thread, mood, and per-character `[LOOK]`, `[POS]`, `[ACT]`, `[EMO]`, and `[FOCUS]`.
* **Obligations Tracker *(Optional)*:** Hidden XML tracker logging active promises, lies, debts, and consequences (auto-pruned to ≤6 active items).
* **Story Strings *(Optional)*:** Generates 4–6 hidden future narrative threads (`expected`, `unlikely`, `random`, `chaotic`, `carryover`) that trigger only if a scene stagnates for 4+ turns.
* **Colored Dialogue & Internal Thoughts *(Optional)*:** Assigns distinct dark-theme pastel `<font>` colors per speaker (white for `{{user}}`) and pairs outward action with private italicized monologue.
* **NSFW / Smut Toggle *(Optional)*:** Explicit, consequence-aware intimacy rules with real-time sensory tracking and experience continuity.

---

## 📊 Token Footprint & Built-in Regex

* **Core Engine (No Toggles):** ~2,450 – 2,970 tokens
* **Full Engine (All Toggles Active):** ~3,300 – 4,000 tokens
* **Automatic Token Saver:** This preset includes bundled **Regex Scripts** that automatically strip old `Scene Anchors`, `Obligations`, `Story Strings`, and `<font>` tags from the prompt context beyond the last 4 messages while keeping them fully visible in your chat UI.

---

## 📝 Changelog

### v1.2
* Consolidated 15+ fragmented modules into 8 tight, imperative prompt blocks (~30% token reduction).
* Added `<character_profile>` XML tags for cleaner separation between `{{user}}` and `{{char}}`.
* Added **Micro-Causality & State Persistence**, **Anti-Passivity** beat caps, and a **Motif Cap**.
* Upgraded `Scene Anchor` to 5 per-character tracking fields, added auto-pruning to `Obligations`, and added **Selection Pressure** to `Story Strings`.
* Split **Internal Thoughts** into an independent toggle.

---

*Inspired by Writer's Block and Stab's SillyTavern presets. Feedback and model compatibility notes are always welcome!*
