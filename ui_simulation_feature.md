# Project Context: Accountant Ability Landing Page Revamp

You are acting as an expert Front-End Web Developer and UX/UI Designer. You are working on the landing page for "Accountant Ability," a B2B SaaS product that automates tax document entry for CPA firms using agentic AI.

**Reference Material:** Please refer to the `Big Bang Round 2.pdf` slideshow in the project directory for deeper context on the value proposition and tone.

## The Task
I want to insert a new HTML/CSS/JS section into `index.html` directly between the `.hero` section and the `.pricing` section. 

This new section will be an **Interactive UI Simulation** that lets the user test-drive the software directly on the landing page. It must use Vanilla JavaScript to manage state transitions and Vanilla CSS for high-quality animations.

### Section Requirements:

**1. Layout & Styling:**
* Use the existing vanilla CSS style (Tailwind-inspired color palette: `#0f172a`, `#0369a1`, `#e0f2fe`, etc.).
* The section should have a clean white background and a header like: `<h2>Experience the Workflow: From Chaos to Completed Return in Seconds</h2>`.
* The simulation container should look like a sleek, modern SaaS dashboard (rounded corners, soft drop shadows, clean borders).

**2. The Interactive Flow (4 States):**

* **State 1: Selection (The Trigger)**
  * Display a simple upload UI with 3 distinct document options the user can click on (e.g., "Complex K-1 (Multi-State)", "Messy W-2", "Scanned 1099-B").
  * Prompt the user: "Select a document to process."
  * **Action:** When the user clicks one of the documents, transition to State 2.

* **State 2: Processing (The Magic - CSS Animations)**
  * Hide the selection screen and show a dynamic loading state.
  * Use CSS animations (like a scanning laser over a blurred document, or glowing skeleton loaders).
  * **Crucial:** Use JavaScript to cycle through these specific text labels every ~800ms to simulate the agentic AI doing the heavy lifting:
    1. *"Analyzing document structure..."*
    2. *"Extracting relevant data..."*
    3. *"Redacting PII..."*
    4. *"Parsing into tax schema..."*
    5. *"Connecting to legacy tax prep tool API..."*
  * **Action:** After the final label, automatically transition to State 3.

* **State 3: API Confirmation (The Bridge)**
  * Show a brief (1.5-second) success screen simulating the connection to the tax prep tool. 
  * Include a green checkmark and text like: *"Payload successfully delivered to Lacerte/Tax Tool."*
  * **Action:** Automatically transition to State 4.

* **State 4: The Final Output (The Value Prop)**
  * Show a mock "Ready to File" tax form UI populated with clean, structured data.
  * Include a prominent "Success" metric, such as: *"1.5 Hours of Manual Entry Saved."*
  * Include a "Reset Demo" button to allow the user to try another document, which returns them to State 1.

**3. Code Constraints:**
* Keep all code contained within the single `index.html` file (embed the CSS in `<style>` and JS in `<script>`).
* **Do not use external libraries** (no React, Vue, or GSAP). Rely entirely on Vanilla JS and CSS (`@keyframes`, flexbox, grid, transitions).
* Ensure the simulation is fully responsive and looks great on both mobile and desktop.

Please output the complete, updated `index.html` file with this new interactive section fully integrated.