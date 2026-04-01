# Project Context: Accountant Ability Landing Page Revamp

You are acting as an expert Front-End Web Developer and UX/UI Designer. You are working on the landing page for "Accountant Ability," a B2B SaaS product for CPA firms. 

**Product Overview:**
Accountant Ability uses agentic AI to read chaotic, unstructured tax documents (like complex K-1s and W-2s) and automatically pushes the extracted data natively into legacy tax software (like Lacerte) via API. It eliminates manual data entry for accountants. 

**Reference Material:** Please refer to the `pitch_deck.pdf` slideshow in the project directory for deeper context on the value proposition, tone, and specific pain points (manual data entry, offshore outsourcing, margin compression) we are solving.

## The Task
I want to insert a new HTML/CSS section into `index.html` directly between the `.hero` section and the `.pricing` section. 

This new section will be an **Interactive UI Simulation** that visually demonstrates how the product works. It should not use actual backend logic, but rather use HTML/CSS animations to create a high-fidelity mock-up of the user journey.

### Section Requirements:

**1. Layout & Styling:**
* Use the existing vanilla CSS style (Tailwind-inspired color palette: `#0f172a`, `#0369a1`, `#e0f2fe`, etc.).
* The section should have a clean white or very light gray background (`#f8fafc`) to contrast with the blue hero section.
* Add a section title like: `<h2>How It Works: From Chaos to Completed Return in Seconds</h2>`.

**2. The UI Simulation (3-Step Animation Sequence):**
Create a flexbox/grid layout that simulates a software dashboard showing three distinct steps. Use CSS animations (keyframes, transitions, delays) to make it feel like the software is actively processing data as the user looks at it.

* **Step 1: Document Intake (The Chaos)**
  * Design a visual "Dropzone" or upload UI.
  * Show a mock PDF icon representing a messy, 50-page tax document (W-2s, 1099s, K-1s) dropping into the system. 
* **Step 2: Agentic AI Processing (The Magic)**
  * Design a simulated processing state. 
  * Show a skeleton loader or scanning animation moving over the document. 
  * Use brief text callouts that appear dynamically: *"Extracting non-standard K-1..."*, *"Validating schema..."*, *"No templates required."*
* **Step 3: The "Last-Mile" Delivery (The Payload)**
  * Show the final result: A clean data payload securely passing through an API bridge into a mock legacy system (label it "Lacerte / Legacy Tax Software"). 
  * Include a prominent "Success" checkmark and a stat like *"2 Hours of Manual Entry Saved."*

**3. Code Constraints:**
* Keep it contained within the single `index.html` file.
* Do not use external libraries (no React, no external animation libraries like GSAP). Rely entirely on modern Vanilla CSS (`@keyframes`, flexbox, grid, transforms) to keep the page lightweight.
* Ensure the simulation is responsive (stack vertically on mobile, display side-by-side or as a pipeline on desktop).

Please output the complete, updated `index.html` file with this new section fully integrated.