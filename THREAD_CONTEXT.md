# Thread Context

This file is the persistent handoff document for this workspace.

Any new thread working in `C:\_dev\Koine-ProductDemonstration` should read this file first to recover project context, current status, and constraints.

## Current Status

- Project output is a single self-contained `index.html`.
- The page is an interactive technical briefing for adaptive sports program directors and equipment managers.
- `index.html` was previously corrupted to all zero bytes and was restored from the last committed version on March 10, 2026.
- A backup of the corrupted file exists as `index.html.zero-backup`.
- The `assets/` folder currently contains:
  - `position 1.png`
  - `position 2.png`
  - `position 3.png`
  - `prototype image.png`
  - `trike_diagram_profile.png`
- All current asset images are `702x496` PNG files.
- The restored HTML currently still contains placeholder regions that may need to be replaced with the actual local assets.
- `index.html` now includes a developer-only screenshot mode toggled with `Shift + Alt + D`.
- Screenshot mode opens all expandable cards and details sections and hides the floating "Open All Details" button for cleaner long-page captures.
- In screenshot mode, the Rider Adaptability section hides the live configuration slider and shows all three seating-position cards at once.
- Local assets are now integrated into the page:
  - hero image uses `assets/prototype image.png`
  - design overview uses `assets/trike_diagram_profile.png`
  - rider configuration uses `assets/position 1.png`, `assets/position 2.png`, and `assets/position 3.png`
- Image render areas are now width-driven with the native `702x496` aspect ratio.
- In normal mode, the active rider-position image now appears directly under the Rider Adaptability heading, with the slider controls below it.
- The bike title is now `KOINE RAINIER`, and the hero image appears directly above that title.

## Project Goal

Build a single interactive webpage that can also be exported as one long screenshot.

Audience:
- adaptive sports program directors
- equipment managers

Use case:
- evaluation of a new adaptive mountain bike prototype for possible pilot program purchase

Primary communication goal:
- clear operational evaluation
- technical briefing tone
- no hype

Questions the page should answer quickly:
- Who can ride this bike?
- How easy is it to adjust between riders?
- How difficult is maintenance?
- How does it compare to existing adaptive bikes?
- Does it fit into our fleet?

## Required Output Constraints

- Single HTML file only
- Runs locally
- Prints cleanly to PDF
- Loads quickly
- No external dependencies
- HTML, CSS, and minimal vanilla JavaScript only
- Use clear visual hierarchy
- Avoid long paragraphs
- Use large sections, expandable panels, interactive diagrams, and comparison tables

## Original Base Prompt

```text
You are generating a single interactive webpage that will also be exported as one long screenshot. The webpage will be sent to adaptive sports program directors and equipment managers who are evaluating a new adaptive mountain bike prototype for potential pilot program purchase.

The goal is clear operational evaluation, not marketing hype. Write with a technical briefing tone.

Avoid startup buzzwords and exaggerated claims.

The page should help a program director answer these questions quickly:

- Who can ride this bike?
- How easy is it to adjust between riders?
- How difficult is maintenance?
- How does it compare to existing adaptive bikes?
- Does it fit into our fleet?

The webpage must be interactive but lightweight, using only HTML, CSS, and minimal vanilla JavaScript.

The final output should be a single HTML file that:

- runs locally
- prints cleanly to PDF
- uses clear visual hierarchy
- loads quickly
- contains no external dependencies

Use large sections, expandable panels, interactive diagrams, and comparison tables.

Do not produce long paragraphs.

PAGE STRUCTURE

1. HERO SECTION
- Title: Bike name placeholder
- Subtitle: "An adaptive electric trail trike designed for riders traditionally excluded from adaptive mountain biking."
- Include a large image placeholder: [Prototype Image Placeholder]
- Show key metrics:
  - Weight: < 70 lbs
  - Range: 40-80 miles
  - Target Price: $5k-$7.5k
- Include subtle hover animation
- Include a scroll cue indicator

2. QUICK OVERVIEW (INTERACTIVE FEATURE GRID)
- Grid of expandable cards:
  - Rider Adaptability
  - Fleet Operation
  - Maintenance Simplicity
  - Cost Accessibility
  - Trail Performance

3. DESIGN OVERVIEW
- Diagram placeholder of the trike
- Interactive callouts with hover tooltips
- Example callouts:
  - Front Wheel Pair
  - Fat Rear Tire
  - Rear Hub Motor
  - Rigid Frame

4. RIDER ADAPTABILITY (INTERACTIVE SLIDER)
- Slider cycles through three rider setups:
  - Position 1: 90-degree seated with foot pegs
  - Position 2: 45-degree forward position with foot pads
  - Position 3: Long-sitting configuration with adjustable leg supports
- Each configuration updates:
  - a simple diagram placeholder
  - bullet points explaining the adjustment
- Static adjustment list:
  - Backrest height (removable)
  - Seat dump
  - Seat width
  - Strap placement
  - Seat fore/aft
  - Seat height
- Rider limits:
  - Max rider height: 6'2"
  - Max rider weight: 220 lbs
- Volunteer adjustment time: 20-30 minutes

5. PROGRAM OPERATIONS
- Interactive metric tiles:
  - Bike Weight: < 70 lbs
  - Unload Time: < 5 minutes
  - Setup Time: Typically < 10 minutes
  - Transport Compatibility: Fits existing transport solutions
  - Volunteer Requirement: Single volunteer handling

6. MAINTENANCE AND DURABILITY
- Collapsible sections:
  - Frame Materials
  - Component Strategy
  - Fastener Standardization
  - Routine Maintenance

7. PERFORMANCE SPECIFICATIONS
- Visual specification table with:
  - Configuration: Tadpole trike
  - Motor: 2000W rear hub motor
  - Top speed: 20 mph
  - Range: 40-80 miles
  - Max grade: 20%
  - Wheels: Front 26 x 2.4, Rear 26 x 4.5 fat tire
  - Rigid frame architecture

8. COMPARISON TABLE (INTERACTIVE)
- Columns:
  - Feature
  - This Bike
  - Typical Adaptive MTB
  - NotAWheelchair - The Rig
- Rows:
  - Target Rider Groups
  - Price
  - Adjustability
  - Motor Power
  - Range
  - Maintenance Complexity
  - Volunteer Setup Time
  - Fleet Adaptability
- Sticky column headers
- Hover row highlighting
- Toggle switch: Show Only Key Differences

9. PROTOTYPE STATUS
- Timeline milestones:
  - Prototype Generation: Gen-1
  - Field Testing Completed: California, Utah, Washington, British Columbia
  - Current Validation Focus: Testing across broader disability populations
  - Production Timeline: ~1 year estimated
  - Early demo units produced domestically

10. PILOT PROGRAM OPPORTUNITY
- CTA panel explaining pilot interest and validation goals

11. CONTACT SECTION
- Placeholders for:
  - Name
  - Organization
  - Email
  - Website

INTERACTION REQUIREMENTS
- Expandable sections
- Hover tooltips
- Interactive rider configuration slider
- Sticky comparison table
- Hover highlighting
- Clickable feature cards
- Subtle and professional animations only

DESIGN REQUIREMENTS
- Clean readable layout
- Large section headers
- Readable body text
- Clear spacing
- Palette should evoke:
  - outdoor recreation
  - engineering reliability
  - accessibility
- Example palette:
  - dark forest green
  - neutral gray
  - white background
- Must export cleanly to PDF using browser print

OUTPUT FORMAT
- Single complete HTML file
- Embedded CSS
- Embedded JavaScript
- No external frameworks
- No CDN dependencies
```

## Working Notes

- If a future thread needs to resume work, read `index.html`, this file, and `assets/` first.
- Prefer preserving the current technical briefing tone over redesigning the concept.
- If image placeholders are still present, the next likely task is integrating the actual local PNG assets into the page.
- If major edits are made, update this file with:
  - what changed
  - what remains
  - any known risks or open decisions

## Update Log

### 2026-03-10

- Restored `index.html` from the last committed git version after the working copy became all zero bytes.
- Added this persistent handoff file for cross-thread continuity.
- Added a developer-only screenshot mode shortcut to `index.html` for clean long screenshots.
- Updated screenshot mode so Rider Adaptability uses three visible seating cards instead of the single slider view.
- Replaced the main placeholder render areas with the local PNG assets and updated the rider slider to swap real seating-position images.
