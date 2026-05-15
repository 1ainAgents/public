# 1ain — Nano Banana Visual Prompts
**Project:** 1ain Personal Master Agent  
**Generated:** 2026-05-14  
**Usage:** Paste each prompt block directly into Nano Banana. Prompts are self-contained — no prior context needed.

---

## HOW TO USE THIS FILE

Each prompt block is labelled with:
- **TYPE** — diagram type and best render format
- **PRIORITY** — HIGH / MEDIUM / LOW (suggested build order)
- **SIZE** — recommended canvas dimensions
- **PROMPT** — the full text to paste into Nano Banana

Start with the HIGH priority prompts. Each builds your visual vocabulary for the project.

---

## SECTION 1 — SYSTEM ARCHITECTURE

---

### DIAGRAM 1A — System Overview (Hub & Spoke)
**TYPE:** Architecture diagram — hub and spoke topology  
**PRIORITY:** HIGH  
**SIZE:** 1600 × 1000px landscape  

**PROMPT:**
```
Technical architecture diagram, hub-and-spoke topology, clean engineering aesthetic.

Central hub: large amber/gold hexagonal node labelled "1ain — Personal Master Agent". 
Glowing softly. This is the gatekeeper and single point of control.

Surrounding the hub inside a dashed rectangular boundary labelled 
"Hostinger VPS / Docker / UFW Firewall":
- Left side: two stacked blue nodes — "Soul Template (5 .md files)" and "Memory (memory.json)" — 
  connected to 1ain hub with solid blue lines labelled "loads identity" and "persists sessions"
- Right side: one coral/orange node outside the VPS boundary labelled 
  "Private Git Repo (git-crypt encrypted)" connected with a bidirectional line labelled "git sync / DR"

Above the VPS boundary: purple node labelled "Subject — Single User" 
connected downward to 1ain with a solid line passing through a badge labelled "Telegram"

Below the VPS boundary, two grayed/dimmed dashed-border nodes connected to 1ain 
with dashed lines (indicating future phases):
- Left: "Hermes — Work Ops Agent (Phase 2)" — 60% opacity
- Right: "Future Agents — Phase 3+" — 30% opacity

Small external dashed node top-right: "Anthropic Claude API" connected to 1ain 
with a thin dashed line labelled "LLM reasoning"

Color palette: dark navy background (#0f0f0e), amber (#ef9f27) for 1ain hub, 
blue (#185fa5) for knowledge components, purple (#534ab7) for subject, 
coral (#993c1d) for external storage, gray (#888780) for future/inactive nodes.

Style: precision engineering schematic, sharp edges, subtle grid background, 
thin connecting lines with arrowheads, monospace font for labels, 
professional infrastructure diagram aesthetic. No decorative elements.

Legend bottom-left: "Solid = Phase 1 Active  |  Dashed = Future Phases  |  
All sub-agents route through 1ain — never direct to subject"
```

---

### DIAGRAM 1B — VPS Internal Stack
**TYPE:** Structural / containment diagram — vertical layers  
**PRIORITY:** HIGH  
**SIZE:** 900 × 1200px portrait  

**PROMPT:**
```
Vertical technical stack diagram showing the internal architecture of a VPS server.
Clean cross-section style, like an engineering cutaway drawing.

From top to bottom, stacked rectangular layers with labels:

LAYER 1 (outermost, thin border): "Ubuntu 22.04 LTS — Host OS"
Color: very dark gray, minimal styling

LAYER 2 (inside layer 1): "UFW Firewall" 
Color: dark red/rust, thin border. Small icon of a shield or firewall symbol left side.
Annotation: "Port 443 only — no SSH from internet"

LAYER 3 (inside layer 2): "Docker Engine"
Color: dark blue. Docker whale logo or simple container icon left side.

LAYER 4 (inside layer 3, the main focus): Large amber-bordered container 
labelled "1ain Container (Python 3.11)"
Inside this container, three sub-sections side by side:
  - Left third: blue section "Soul Loader — reads .md files on startup"
  - Middle third: amber section "Agent Core — Claude API + session logic"  
  - Right third: green section "Memory Store — reads/writes memory.json"

Below the container, two small external connection indicators:
- Left: "Telegram API (polling)" with bidirectional arrow
- Right: "Anthropic Claude API" with outbound arrow

LAYER 5 (at the very bottom, outside the VPS): 
Two storage indicators side by side:
- "VPS Filesystem — soul/ data/ logs/ app/" (local)
- "GitHub Private Repo (git-crypt)" (cloud, dashed border)

Connected with thin lines showing data flow direction.

Style: technical blueprint aesthetic, dark background (#0d0d0b), 
amber (#ba7517) for 1ain components, blue (#185fa5) for data/knowledge,
green (#3b6d11) for memory/persistence, red (#993c1d) for security layers.
Clean sans-serif labels, precise alignment, grid lines in background at 20% opacity.
Professional infrastructure documentation style.
```

---

### DIAGRAM 1C — Git / Disaster Recovery Architecture
**TYPE:** Flow diagram — backup and recovery paths  
**PRIORITY:** MEDIUM  
**SIZE:** 1400 × 800px landscape  

**PROMPT:**
```
Technical flow diagram showing a Git-based disaster recovery architecture for a personal AI agent.

Three main zones arranged left to right:

ZONE 1 — VPS (left, green border):
- Box: "1ain Running Container"
- Box below: "/opt/1ain/ filesystem" with sub-items: soul/*.md, data/memory.json, logs/
- Dashed box: ".env (git-crypt encrypted)"

ZONE 2 — GitHub (centre, coral/orange border):
- Box: "Private Repository"
- Sub-items: "soul template files", "app/ Python code", 
  "docker-compose.yml", ".env.gpg (encrypted)"
- Label: "Single source of truth"

ZONE 3 — Engineer/DR (right, purple border):
- Box: "git-crypt key (password manager)"
- Box: "Any fresh VPS"
- Box: "< 2 hours full restore"

Bidirectional arrows between Zone 1 and Zone 2 labelled:
- "git pull (startup)" going left
- "git push via /soulsync command" going right

Arrow from Zone 2 to Zone 3 labelled "git clone + decrypt + docker compose up"

At the top, a timeline showing the DR procedure as numbered steps:
1. Provision new VPS (15 min)
2. Install Docker (10 min)
3. git clone private repo (2 min)
4. git-crypt unlock with key (1 min)
5. docker compose up (5 min)
6. Verify SC-008 acceptance test (20 min)
Total: < 2 hours

Style: clean technical diagram, dark background, color-coded zones with subtle fills,
precise arrows with operation labels, monospace font for commands,
professional DevOps/infrastructure style.
```

---

## SECTION 2 — SOUL TEMPLATE SYSTEM

---

### DIAGRAM 2A — Soul Template Ecosystem
**TYPE:** Knowledge map / entity relationship  
**PRIORITY:** HIGH  
**SIZE:** 1600 × 1000px landscape  

**PROMPT:**
```
Knowledge ecosystem diagram showing the Soul Template profiling system for an AI agent.

Central element: large hexagonal node labelled "soul_master.md — Master Profile"
Amber/gold color, slightly glowing, central position.

Six satellite nodes connected to the master with solid lines:

Connected satellites (solid lines = Phase 1 complete):
1. Blue node top-left: "soul_cognitive.md — Reasoning Modes" 
   Subtitle: "top-down primary, systems thinker, complexity management"
2. Purple node top-right: "soul_expertise.md — Domain Topology"
   Subtitle: "Expert: network arch, Linux, security | Proficient: ELK, AI, crypto"
3. Green node right: "soul_values.md — Core Values & Philosophy"
   Subtitle: "precision, reusability, production-grade, autonomy"
4. Coral node bottom-right: "soul_interaction.md — Communication Profile"
   Subtitle: "CRITICAL: cannot code — AI-driven always. Expert peer posture."
5. Teal node bottom-left: "soul_hermes_vision.md — Architecture Vision"
   Subtitle: "1ain as hub/gatekeeper, Hermes Phase 2, multi-agent OS"

Outer ring — feeding INTO the master (dashed lines = ongoing input):
- Five small source nodes arranged in an arc on the left:
  "HST-S001: BGP/Alerta thread (Claude)" — HIGH weight
  "HST-S002: Web3/VC Bridge thread (GPT-4o)" — HIGH weight
  "HST-S003: Network Vision thread (Gemini)" — HIGH weight
  "HST-S004: Agent Bridge thread (Grok)" — LOW weight
  "HST-S005: SRX/ELK Pipeline thread (Perplexity)" — MEDIUM weight
  Each labelled with source LLM and weight.

Bottom of diagram: "Debrief Instrument — hermes_soul_template_v1.md"
Arrow pointing up into the source nodes labelled "multi-LLM profiling pipeline"

Small annotations:
- "14 hardened cross-thread signals"
- "5 seed threads complete — ongoing"
- "v0.1-SEED — production pending"

Style: dark background, interconnected knowledge graph aesthetic,
glowing nodes with soft halos, amber for master, varied colors per satellite,
thin connecting lines with subtle animations implied (static but dynamic-feeling),
reminiscent of a neural network or knowledge graph visualization.
Clean, technical, slightly futuristic.
```

---

### DIAGRAM 2B — Soul Template Debrief Pipeline
**TYPE:** Sequence / process flow diagram  
**PRIORITY:** MEDIUM  
**SIZE:** 1600 × 700px landscape  

**PROMPT:**
```
Horizontal left-to-right process flow diagram showing the soul template profiling workflow.

7 stages as connected rectangular nodes with arrows between them:

STAGE 1 (purple): "Existing Chat Thread"
Sub-label: "Any LLM — any topic"
Small icons: Claude, GPT, Gemini, Grok, Perplexity logos (or stylized initials)

STAGE 2 (blue arrow →): "Debrief Instrument Pasted"
Sub-label: "hermes_soul_template_v1.md"
"10-part structured debrief"

STAGE 3 (amber): "LLM Analyses the Thread"
Sub-label: "Cognitive profile, expertise map, values, decisions, comms fingerprint"
"Output formatted for AI ingestion"

STAGE 4 (teal): "Structured Output Generated"
Sub-label: "DEBRIEF_ID: HST-NNNN"
"THREAD_UID: LLM_CODE-TITLE-DATE"
"RE-ENGAGEMENT FLAG + metadata"

STAGE 5 (green): "Cross-Thread Synthesis"
Sub-label: "soul_master.md updated"
"Hardened signals extracted"
"Open questions flagged"

STAGE 6 (coral): "soul_*.md Files Updated"
Sub-label: "6 sub-profile files"
"Version bumped"

STAGE 7 (amber glow): "1ain Loads Identity"
Sub-label: "On startup: git pull"
"Soul template injected as system context"

Below the main flow, a feedback loop arrow from Stage 7 back to Stage 1 
labelled "every conversation adds signal"

Style: clean process flow, dark background, numbered stages, 
professional workflow/pipeline aesthetic, 
each stage box has a small icon or symbol in the top corner.
```

---

## SECTION 3 — DATA FLOW

---

### DIAGRAM 3A — Message Lifecycle (Data Flow)
**TYPE:** Sequence diagram / data flow  
**PRIORITY:** HIGH  
**SIZE:** 1400 × 900px landscape  

**PROMPT:**
```
Sequence/swimlane diagram showing the complete lifecycle of a user message through the 1ain system.

Four swimlanes (horizontal bands) from top to bottom:
1. SUBJECT — purple band
2. TELEGRAM CLOUD — gray band  
3. 1ain CONTAINER (VPS) — amber band, slightly wider
4. EXTERNAL SERVICES — blue/dark band

Message flow (numbered steps with arrows between swimlanes):

1. Subject types message in Telegram app → [arrow down to Telegram Cloud]
2. Telegram stores message, polling detects it → [arrow down to 1ain Container]
3. User ID whitelist check → if unknown: SILENT REJECT + LOG (red branch, exits right)
4. soul_master.md loaded as identity context (internal to 1ain)
5. memory.json loaded for session history (internal to 1ain)
6. Full prompt assembled: soul context + memory + user message (internal to 1ain)
7. Request sent to Anthropic Claude API → [arrow down to External Services]
8. Claude generates response → [arrow up back to 1ain Container]
9. Response formatted and checked (internal to 1ain)
10. Response sent via Telegram API → [arrow up to Telegram Cloud]
11. Message delivered to Subject → [arrow up to Subject]
12. Session memory updated, optionally saved (internal to 1ain)

Special command branches (shown as side branches from step 3):
- /status → immediate status response
- /clear → clear session memory  
- /save → persist memory to disk
- /soulsync → git pull + reload soul files + git push

Style: clean sequence diagram, dark background, 
color-coded swimlanes with subtle fills,
numbered step bubbles on arrows, 
branching paths clearly shown with different line colors,
professional technical documentation style.
Small clock icon showing "typical response < 3 seconds"
```

---

### DIAGRAM 3B — Security Perimeter (Threat Model)
**TYPE:** Concentric rings / security architecture  
**PRIORITY:** MEDIUM  
**SIZE:** 1000 × 1000px square  

**PROMPT:**
```
Concentric rings security architecture diagram, like an onion or fortress cross-section.

Centre (innermost): Small amber hexagon — "Soul Template + Memory — Identity core"
Label: "Never leaves VPS. Never in logs. git-crypt encrypted in repo."

Ring 1 around centre: "1ain Application Container"
Label: "Python 3.11. Non-root user. Isolated filesystem."

Ring 2: "Docker Engine"
Label: "Container isolation. No host network access."

Ring 3: "UFW Firewall"
Label: "Outbound only: Telegram API, Anthropic API. No inbound ports."
Color: rust/red band indicating security boundary

Ring 4: "Hostinger VPS"
Label: "SSH key auth. Fail2ban. Ubuntu 22.04 LTS. Private network."

Ring 5 (outermost, dashed): "Internet / External"
Color: dark, slightly threatening aesthetic
Sub-labels at cardinal points: 
  - "Telegram API (polling — no inbound)" 
  - "Anthropic Claude API (HTTPS)" 
  - "GitHub (deploy key, git-crypt)" 
  - "All other traffic: BLOCKED"

One thin arrow from outer ring to Ring 3 labelled "rejected" with an X symbol.
One thin green arrow from Ring 3 outward labelled "outbound only, encrypted"

Style: concentric rings cross-section, dark background, 
each ring a different shade/color indicating security tier,
rings get lighter and more accessible toward the outside,
innermost ring glows amber indicating the protected identity core,
military/cybersecurity aesthetic — precise, serious, technical.
```

---

## SECTION 4 — ROADMAP & VISION

---

### DIAGRAM 4A — Phase Roadmap (Timeline)
**TYPE:** Horizontal timeline / Gantt-style  
**PRIORITY:** HIGH  
**SIZE:** 1800 × 600px landscape  

**PROMPT:**
```
Horizontal project roadmap timeline showing 4 phases of an AI agent build.

Layout: left-to-right timeline with 4 phase blocks. 
A single horizontal line runs through all blocks at the mid-height.
Circular milestone markers on the line at phase transitions.

PHASE 1 — "1ain Core" (amber/gold, leftmost, largest — it's current)
Block label: "Phase 1 — NOW"
Contents listed inside:
• Telegram interface
• Soul template identity
• Claude API reasoning  
• Memory persistence
• Private Git repo + DR
• VPS · Docker · Firewall
Status badge: "▶ IN PROGRESS" in green

PHASE 1b — "Tool Integrations" (green, second block)
Block label: "Phase 1b — NEXT"
Contents:
• MCP server activated
• Gmail / Calendar / Drive
• /soulsync automated
• 1ain trusted daily
Status badge: "⏳ PENDING"

PHASE 2 — "Hermes Agent" (blue, third block)
Block label: "Phase 2 — DEFERRED"
Contents:
• Task ops specialist agent
• Work projects / productivity
• Blue sky thinking capture
• Skills / resource library
• Separate isolated repo
• Routes through 1ain only
Status badge: "⏳ TRIGGER: Phase 1 complete"

PHASE 3+ — "Multi-Agent OS" (gray, rightmost, faded)
Block label: "Phase 3+ — VISION"
Contents:
• Finance / Web3 agent
• Research agent
• Knowledge base RAG
• Potential replication
Status badge: "◌ BLUE SKY"

Trigger annotations between phases:
Between P1→P1b: "SC-007: used daily without second-guessing"
Between P1b→P2: "1ain fully trusted and stable"
Between P2→P3: "Hermes delivering value"

Style: professional product roadmap, dark background,
color progression left-to-right from amber to gray showing urgency/certainty,
clean typography, amber glow on Phase 1 block indicating active,
later phases progressively more transparent/faded.
```

---

### DIAGRAM 4B — Multi-Agent Future Vision
**TYPE:** Conceptual architecture / isometric  
**PRIORITY:** MEDIUM  
**SIZE:** 1600 × 1000px landscape  

**PROMPT:**
```
Isometric conceptual architecture diagram showing the future multi-agent AI OS vision.

Isometric 3D perspective, floating nodes connected by glowing lines.

Central elevated platform: Large amber hexagonal platform labelled "1ain"
Subtitle: "Personal AI Operating System"
Glowing amber, highest elevation — the orchestrator above all others.

Six lower platform nodes surrounding 1ain, connected with glowing lines from below:

1. Blue platform: "Hermes — Task Ops Agent"
   Sub-nodes: Work projects, Tasks, Blue sky, Skills library
   
2. Green platform: "Finance Agent" (Phase 3+, slightly dimmed)
   Sub-nodes: Crypto, Portfolio, Markets
   
3. Purple platform: "Research Agent" (Phase 3+, dimmed)
   Sub-nodes: Web search, RAG, Documents
   
4. Coral platform: "Personal Admin" (Phase 3+, dimmed)
   Sub-nodes: Calendar, Email, Tasks
   
5. Teal platform: "Web3 Agent" (Phase 3+, dimmed)
   Sub-nodes: Blockchain, DeFi, Identity
   
6. Gray placeholder platform: "Agent N" — "Extensible" (very dimmed, dashed border)

Above 1ain, a single upward connection to: 
"Subject — You" — small glowing purple node at apex

All sub-agent connections route THROUGH 1ain. 
No direct connections between sub-agents or to Subject.
This hub-and-spoke constraint is visually obvious in the geometry.

Floating data streams: thin glowing lines showing data flowing from sub-agents 
upward through 1ain then upward to Subject.

Background: deep space / dark navy with subtle star field or grid pattern.
Style: futuristic but technical, isometric engineering aesthetic,
subtle glows, amber as the dominant accent color for 1ain,
each sub-agent a distinct color. Professional, not cartoonish.
```

---

## SECTION 5 — 1ain AVATAR / IDENTITY

Three distinct concept directions. Build all three, then choose.

---

### AVATAR A — The Sentinel (Recommended for Telegram bot icon)
**TYPE:** Logo / identity mark — geometric badge  
**PRIORITY:** HIGH  
**SIZE:** 512 × 512px square (for Telegram profile picture use)  

**PROMPT:**
```
Precision engineering badge / logo mark. Dark background. Amber/gold colourway.

Outer shape: Regular hexagon (flat-top orientation), amber stroke, very dark amber fill.
Stroke weight: 2.5px, sharp edges, no rounding.

Inside the hexagon, concentric inner hexagon (same centre, 65% scale), 
amber stroke only, no fill, stroke weight: 1px.

At the very centre: A stylised numeral "1" in a precision serif/engineering style:
- Strong vertical stem, stroke-weight 8px
- Top-left diagonal serif stroke (like a classic Roman I), stroke-weight 5px  
- Bottom horizontal crossbar, stroke-weight 5px
- The "1" is amber-200 (light gold) for maximum contrast against dark fill

Four small filled amber circles (radius 4px) at the midpoints of the inner hexagon's 
four cardinal edges (top, right, bottom, left) — like circuit connection nodes.

Six short tick marks radiating outward from each outer hexagon vertex, 
length 10px, amber-600 color, indicating precision measurement markings.

Below the hexagon:
Text "1ain" — font: geometric sans-serif, font-weight 600, amber color, 
letter-spacing 0.15em, font-size roughly 1/4 of the hexagon width.
Text "PERSONAL AGENT" — same font, much smaller, lighter amber, 
very wide letter-spacing (0.25em), below "1ain".

Color palette (dark theme — this is a dark background icon):
Background: #1a1a17 (near-black warm dark)
Outer hex fill: #412402 (dark amber)
Outer hex stroke: #EF9F27 (bright amber)  
Inner hex stroke: #ba7517 (mid amber)
"1" numeral: #FAC775 (light gold)
Circuit nodes: #EF9F27 (bright amber)
Tick marks: #ba7517 (mid amber)
"1ain" text: #FAC775 (light gold)
"PERSONAL AGENT" text: #ba7517 (mid amber)

Overall feel: premium technical badge, like a precision instrument nameplate.
Clean, authoritative, engineered. Not decorative. Works at 32px icon size.
```

---

### AVATAR B — The Circuit Mind (Dark/Cyber variant)
**TYPE:** Logo / identity mark — cyberpunk circuit aesthetic  
**PRIORITY:** MEDIUM  
**SIZE:** 512 × 512px square  

**PROMPT:**
```
Abstract circuit-board head / AI consciousness logo. Dark cyberpunk aesthetic.

Circular outer ring, thin stroke, amber-gold color, 
with four tick marks at 12/3/6/9 o'clock positions.

Inside the circle: Abstract human head profile made entirely from circuit board traces.
The profile faces right (or straight ahead). Highly stylised, minimalist — 
recognisable as a head only from the outline. 

The head is constructed from:
- Sharp angular lines (PCB trace style — 45° angles only, no curves)
- Small junction nodes (filled circles) at trace intersections
- A glowing "eye" — single bright amber circle mid-head
- From the "eye", radiating trace lines outward across the head — like thoughts/signals

Below the head, descending trace lines that transform into:
"1" — formed from circuit traces, same angular PCB aesthetic

The entire interior of the circle uses amber traces on very dark background.

Text below circle:
"1ain" in a monospace/technical font, amber color
"PERSONAL MASTER AGENT" very small, amber-600, wide letter-spacing

Background: #0d0d0b (near-black)
Amber traces: #EF9F27 (#ba7517 for secondary traces)
Glow effect on the eye node: subtle amber bloom
Node circles: filled #EF9F27

Style: cyberpunk/hacker aesthetic meets precision engineering.
Think: Blade Runner + circuit schematic. Technical, intelligent, slightly mysterious.
Suitable as a dark-mode app icon or Telegram bot profile picture.
```

---

### AVATAR C — The Minimal Mark (Abstract geometric)
**TYPE:** Logo / identity mark — pure geometric minimalism  
**PRIORITY:** MEDIUM  
**SIZE:** 512 × 512px square  

**PROMPT:**
```
Ultra-minimal geometric logo mark. Clean, timeless, works at any size.

The entire mark is constructed from just three elements:

ELEMENT 1: A perfect circle, outline only (stroke, no fill), amber color, 
occupying roughly 70% of the canvas.

ELEMENT 2: Inside the circle, a bold vertical line — the numeral "1" stripped to its
absolute minimum. No serifs, no crossbar. Just a single strong vertical stroke, 
centered, occupying 50% of the circle's height. 
Stroke width: 12px. Color: amber.

ELEMENT 3: A single arc — a partial circle (roughly 270°, missing the bottom-right arc segment) 
positioned outside the main circle, concentric with it, 
as if the circle is "opening" or "reaching outward" on one side.
This creates a feeling of connectivity and reach.
Stroke color: amber, stroke-width 3px, slightly lighter amber than the inner "1".

Below the mark:
"1ain" in a clean geometric sans-serif, medium weight, amber.
Tracking: 0.2em.

Color options (provide two versions side by side):
Version A — dark: black background, amber mark (#EF9F27)
Version B — light: white background, amber mark (#ba7517)

Style: Swiss design / Bauhaus influence. Extreme reduction. 
Every element is functional — nothing decorative.
The kind of logo that looks equally good at 16px favicon size and 2m banner size.
Think: Dieter Rams, not neon cyberpunk.
```

---

## SECTION 6 — SUPPORTING VISUALS

---

### DIAGRAM 6A — Soul Template File Structure
**TYPE:** File tree / document hierarchy  
**PRIORITY:** LOW  
**SIZE:** 800 × 1000px portrait  

**PROMPT:**
```
Clean technical file tree diagram showing the soul template document structure.

Title at top: "Soul Template — Identity Architecture"

File tree structure with visual hierarchy:

📁 /opt/1ain/ (root folder, amber)
├── 📁 soul/  (blue folder — identity layer)
│   ├── 📄 soul_master.md      ← "Master consolidated profile (hub)"
│   ├── 📄 soul_cognitive.md   ← "Reasoning modes, mental models"
│   ├── 📄 soul_expertise.md   ← "Domain topology, skill inventory"
│   ├── 📄 soul_values.md      ← "Core values, philosophy"
│   ├── 📄 soul_interaction.md ← "Communication fingerprint, constraints"
│   └── 📄 soul_hermes_vision.md ← "Architecture vision, future state"
├── 📁 data/  (green folder — runtime state)
│   └── 📄 memory.json         ← "Session memory, conversation history"
├── 📁 logs/  (gray folder — observability)
│   └── 📄 1ain.log            ← "Structured log, rejected users logged"
├── 📁 app/   (teal folder — application code)
│   ├── 📄 agent.py            ← "Main application — 650 lines"
│   ├── 📄 requirements.txt    ← "Python dependencies"
│   ├── 📄 Dockerfile          ← "Container definition"
│   └── 📄 docker-compose.yml  ← "Service orchestration"
└── 📄 .env  🔒               ← "Secrets — git-crypt encrypted"

On the right side of the diagram, a small column showing what 1ain does with each layer:
soul/ → "Loaded as identity context on every conversation"
data/ → "Read + written during session, /save command persists"
logs/ → "Written continuously, never synced to Git"
app/  → "Source of truth in Git, deployed via docker compose"
.env  → "Encrypted in Git, decrypted on VPS only"

At bottom: 
"Git repo contains: soul/ + app/ + .env (encrypted) — NOT data/ or logs/"

Style: dark terminal/IDE aesthetic, monospace font throughout,
color-coded folder icons, file type icons, 
subtle syntax highlighting colors for the annotation comments.
Like a high-quality code editor file tree screenshot.
```

---

### DIAGRAM 6B — Binary Questions Decision Log
**TYPE:** Decision log / resolved questions table  
**PRIORITY:** LOW  
**SIZE:** 1200 × 700px landscape  

**PROMPT:**
```
Clean decision log table / visual showing resolved architectural questions.

Title: "1ain — Architectural Decisions"
Subtitle: "Binary questions resolved during design phase"

Table with 3 columns: ID | Question | Decision + Implication

Row 1 (green — resolved): 
BQ-001 | "Is this infrastructure personal/private or professional?" 
| "PERSONAL & PRIVATE — full autonomy. No compliance constraints. 
  Build exactly what's needed."

Row 2 (green — resolved):
BQ-002 | "Can you code? Will this change?"
| "CANNOT CODE — AI-driven always, permanently. 
  Every deliverable: copy-paste ready, numbered steps, verify+fail path."

Row 3 (green — resolved):
BQ-003 | "Single user or multi-user?"
| "SINGLE USER — personal agent. 
  Simple whitelist auth. No user management complexity."

Row 4 (green — resolved):
BQ-004 | "Python delegated or owned?"
| "AI-DELEGATED — all Python generated by AI. 
  Subject reads, verifies, does not write."

Row 5 (amber — open):
BQ-005 | "Monday.com — professional or personal?"
| "OPEN — relevant to Hermes Phase 2 scope"

Row 6 (amber — open):
BQ-006 | "Hermes Phase 2 — task ops only, personal only, or both?"
| "OPEN — non-blocking, defer to Phase 2 design"

Below the table, two highlighted constraint boxes:

Red box: "C-010 — PERMANENT NON-NEGOTIABLE"
Text: "1ain Git repo is PERMANENTLY SEPARATE from all sub-agent repos. 
No sub-agent has read or write access to the 1ain repo — ever."

Amber box: "SC-007 — Human Acceptance Test"  
Text: "Subject trusts 1ain enough to use daily without second-guessing. 
This is the trigger for Phase 1b and eventually Phase 2."

Style: clean product/engineering decision log,
dark background, color-coded rows (green = resolved, amber = open),
professional table formatting, monospace for constraint IDs,
sans-serif for text content.
```

---

## APPENDIX — STYLE NOTES FOR ALL DIAGRAMS

When generating any diagram for this project, apply these global style principles:

**Color Palette (consistent across all outputs):**
- 1ain / Primary agent: amber/gold (#EF9F27, #ba7517, #FAC775)
- Knowledge / Soul / Data: blue (#185fa5, #e6f1fb)
- Subject / Human: purple (#534ab7, #eeedfe)
- Infrastructure / Storage: teal (#0F6E56, #E1F5EE) or coral (#993c1d)
- Memory / Persistence: green (#3b6d11, #eaf3de)
- Future / Inactive: gray (#888780, #f1efe8)
- Security / Firewall: rust/red (#a32d2d)
- Background: near-black warm dark (#0f0f0e or #1a1a17)

**Typography:**
- Labels: clean geometric sans-serif (Inter, DM Sans, or similar)
- Code / IDs / paths: monospace (JetBrains Mono, Fira Code)
- All labels: sentence case (not ALL CAPS except badge labels)

**General Aesthetic:**
- Engineering precision, not decoration
- Dark backgrounds preferred (subject is a visual engineer who works at night)
- Thin strokes (0.5–1.5px), sharp edges
- Subtle grid or dot pattern backgrounds at 10–15% opacity
- Arrowheads: small, clean, open chevron style
- No drop shadows, no heavy gradients, no glassmorphism
- Think: Cisco network diagram meets dark IDE theme

**What to avoid:**
- Bright white backgrounds
- Bubble/rounded-everything UX aesthetic
- Icons that are too small to read
- Over-coloring (max 3–4 distinct colors per diagram)
- Decorative elements that don't carry information

---
*Prompt file version: 1.0 | Project: 1ain | Date: 2026-05-14*
*Reference files: 1ain_SoR.md, 1ain_HLD.md, 1ain_LLD.md, soul_master.md*
