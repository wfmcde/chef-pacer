# Chef Pacer

A single-threaded culinary itinerary runner and kitchen pacer designed for mobile use right at the stove or grill. Modeled after modular itinerary engines, it structures recipes into sequential checkpoints with sensory exit criteria, cadence timers, and audio cues.

**Live Application:** [https://wfmcde.github.io/chef-pacer/](https://wfmcde.github.io/chef-pacer/)

---

## Features

- **Single-Threaded Step Runner:** Displays only the active kitchen task in high-visibility typography to prevent losing your place during active prep.
- **Sensory Exit Criteria:** Clear visual, tactile, and aromatic benchmarks for each phase rather than ambiguous timing guidelines.
- **Integrated Cadence Timers:** Native in-browser Web Audio chimes via Tone.js with real-time extension controls (+3 min adjustments).
- **Dynamic Category Filtering:** Instant protein and style filtering (All, Pork, Seafood, etc.) on the central hub.
- **Zero-Build Architecture:** Pure HTML, Tailwind CSS (CDN), and vanilla JavaScript. Deploys instantly to GitHub Pages with no build steps or dependencies.

---

## Repository Structure

```text
chef-pacer/
├── index.html                           # Main Hub & Dynamic Recipe Directory
├── grilled-pork-chops-pesto.html        # Two-zone grilled chops & pesto ravioli
├── braised-pork-chops-sugo.html         # Dutch oven braised pork chops & rigatoni
├── shrimp-scallop-heirloom-pasta.html   # Flash-seared seafood & heirloom tomato pasta
└── README.md                            # Documentation & data schema
Adding a New Recipe
Create the Recipe File: Duplicate an existing recipe template (e.g., grilled-pork-chops-pesto.html), rename it (e.g., cast-iron-ribeye.html), and update the checklist array and step objects.

Register in index.html: Add an entry to the recipes array in index.html:
{
  title: "Cast-Iron Ribeye & Charred Asparagus",
  category: "Steak",
  tag: "Skillet & Veg",
  desc: "High-heat baste with butter and garlic, carryover rest timing, and flash-charred asparagus.",
  time: "Est. 20 min",
  legs: "4 Legs",
  file: "cast-iron-ribeye.html"
}
