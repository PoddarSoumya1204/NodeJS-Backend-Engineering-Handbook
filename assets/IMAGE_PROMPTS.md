# 🎨 Image Generation Prompts

This handbook ships with **prompts**, not pre-rendered images, for the visual assets referenced in the README and around the repository. Run any of these through Midjourney, Flux, GPT Image, or Stable Diffusion and drop the resulting PNG into this `assets/` folder using the filename noted in each section.

| Asset | Filename | Purpose |
|---|---|---|
| Backend Architecture Diagram | `backend-architecture.png` | README system design illustration |
| Request Lifecycle Diagram | `request-lifecycle.png` | README request-flow illustration |
| Handbook Cover | `handbook-cover.png` | Repository / PDF cover art |

---

## 1. Backend Architecture Diagram — `backend-architecture.png`

**Purpose:** A clean, professional system-design illustration for the README that visually maps the architecture taught throughout the handbook.

**Prompt:**

```
A clean, modern system architecture diagram in a minimal flat-design illustration style,
suitable for a professional GitHub README. Dark background (#0B1220) or clean white
background (#FFFFFF) — dark mode preferred — with a vertical top-to-bottom flow rendered
as connected rounded-rectangle nodes joined by thin glowing directional arrows in blue
(#3B82F6) and cyan (#22D3EE) accent colors.

Vertical flow, top to bottom, centered:
1. "Client" (device/browser icon)
   ↓
2. "Load Balancer" (icon: distribution/fork symbol)
   ↓
3. "API Gateway" (icon: gateway/shield symbol)
   ↓
4. "Controllers" (icon: routing/dispatch symbol)
   ↓
5. "Services" (icon: gear/business-logic symbol)
   ↓
6. "Repositories" (icon: drawer/data-access symbol)
   ↓
7. "Database" (icon: cylinder)

Branching off to the sides of the main vertical flow, connected with thinner dashed lines,
show these supporting components as smaller labeled nodes: "Redis Cache" (lightning bolt
icon) connected near the Repository/Service level, "Authentication" (lock/shield icon)
connected near the API Gateway, "Logging" and "Monitoring" (chart/pulse icons) connected
near the Services layer, "External APIs" (globe icon) connected to Services, "Background
Jobs" (clock/queue icon) connected to Services, and "Message Queue" (stacked envelope icon)
connected between Services and Background Jobs.

Each node is a soft rounded rectangle with a subtle gradient fill, thin light-blue border,
minimal flat icon, and a clean sans-serif label directly beneath or inside it. Consistent
icon style throughout — thin-line, monochrome, modern (similar to Heroicons or Feather
icons). Generous whitespace/negative space between nodes. No 3D effects, no photorealism,
no drop shadows heavier than a subtle soft glow. Overall composition should read instantly
as "software system diagram," similar to diagrams found in AWS, Vercel, or Stripe engineering
blogs. High resolution, crisp vector-style rendering, perfectly aligned grid layout, suitable
for embedding at full width in a GitHub markdown README.
```

---

## 2. Request Lifecycle Diagram — `request-lifecycle.png`

**Purpose:** A companion illustration to the Mermaid sequence diagram in Chapter 1, showing how a single request travels through the system and back.

**Prompt:**

```
A minimal, modern infographic illustrating the lifecycle of a single HTTP request through
a backend system, rendered as a looping horizontal flow (request path on top, response path
mirrored below, like a round trip). Dark navy background (#0B1220), thin glowing blue
directional arrows (#3B82F6), flat rounded-rectangle nodes with soft gradients and minimal
line icons in a consistent style.

Top row, left to right: "Client" → "Load Balancer" → "API Gateway" → "Controller" →
"Service" → "Repository" → "Database". Bottom row (response path), right to left, mirrored
and in a slightly muted cyan tone: "Database" → "Repository" → "Service" → "Controller" →
"Client". Connect the end of the top row to the start of the bottom row with a curved
arrow to visually suggest the round trip.

Each node uses the same soft rounded-rectangle style with a subtle icon (device for Client,
fork/split icon for Load Balancer, shield for API Gateway, dispatch icon for Controller,
gear for Service, drawer for Repository, cylinder for Database) and a clean sans-serif
label. Add small annotation text near the Controller/Service/Repository nodes reading
"Every layer has one responsibility" in a subtle lighter gray caption style beneath the
diagram. No photorealism, no 3D, no clutter, no people. Clean, technical, high-end SaaS
documentation illustration style suitable for embedding in a GitHub README or technical
handbook. High resolution, sharp vector-like rendering, wide aspect ratio.
```

---

## 3. Handbook Cover — `handbook-cover.png`

**Purpose:** A cover image for the PDF and repository, resembling a professional technical handbook (O'Reilly-inspired) rather than a marketing graphic.

**Prompt:**

```
A minimal, professional technical book cover design, inspired by O'Reilly and high-end
engineering handbook aesthetics. Deep charcoal-black background (#0A0A0F) with a single
subtle accent color band (electric blue, #2563EB) running vertically down one-third of the
cover on the left or right edge. No illustration, no mascot, no photograph — purely
typographic and geometric.

Centered or left-aligned clean modern sans-serif typography (similar to Inter, Söhne, or
Neue Haas Grotesk): large title "Node.js Backend Engineering Handbook" in crisp white,
with a thin horizontal rule beneath it, followed by smaller subtitle text in muted gray:
"A Practical Guide for Building Maintainable, Scalable, Production-Ready APIs". Below that,
in the accent blue color, a small tagline: "Build Systems. Not Just APIs."

Include a very subtle geometric motif in the background at low opacity — thin interconnected
line-nodes suggesting a distributed system or circuit pattern, barely visible, purely
textural, not competing with the typography. Optionally a thin bordered rectangle frame
close to the edges of the cover, reminiscent of classic technical book covers. No gradients
that look "AI generated neon" — keep the palette restrained: black, white, one muted gray,
one accent blue. Sharp typography, generous margins, editorial print-design quality, portrait
orientation (book cover aspect ratio, e.g. 1600x2400). High resolution, print-ready quality,
flat design, no drop shadows except a very subtle one beneath the title block for depth.
```

---

## Design Notes

- **Palette:** dark background (`#050914` – `#0B1220`), primary accent blue (`#2563EB`), secondary cyan accent (`#22D3EE`), text in white/light gray.
- **Typography:** a clean geometric sans-serif (Inter, Söhne, or Neue Haas Grotesk-style) across all four assets for visual consistency.
- **Consistency:** reuse the same icon set and line weight across `backend-architecture.png` and `request-lifecycle.png` so they read as a matched pair when both appear in the README.
- Once generated, place the PNG files directly in this `assets/` folder using the exact filenames listed in the table above so the image links in [`README.md`](../README.md) resolve correctly.
