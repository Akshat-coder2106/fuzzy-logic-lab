# Fuzzy Logic Lab

An interactive, browser-based workspace for exploring a **Mamdani fuzzy logic controller**. Adjust inputs and inference settings, inspect fuzzy membership and rule firing, follow calculations step by step, and run built-in verification examples.

<p align="center">
  <a href="https://akshat-coder2106.github.io/fuzzy-logic-lab/"><strong>Open the live Fuzzy Logic Lab ↗</strong></a>
</p>

## Overview

Fuzzy logic represents partial membership rather than forcing every input into a strictly true-or-false category. This lab makes the main stages of a Mamdani-style inference pipeline visible:

1. **Fuzzification** — convert crisp input values into membership degrees.
2. **Rule evaluation** — evaluate IF–THEN rule antecedents and calculate firing strengths.
3. **Implication** — apply each firing strength to its consequent membership function.
4. **Aggregation** — combine rule outputs into one fuzzy output set.
5. **Defuzzification** — convert the aggregated fuzzy set into a crisp value.

The dashboard updates its output and visualisations when you change inputs or inference settings.

## Features

- **Interactive input controls:** adjust input values with sliders or numeric fields.
- **Example models:** explore the Room Fan and Water-tank Level presets, or start from the Custom model.
- **Membership functions:** inspect input and output membership plots. The inference engine supports triangular, trapezoidal and Gaussian membership functions; numeric parameters can be changed in the parameter editor.
- **Configurable inference:** experiment with the available AND, OR, implication and aggregation operators.
- **Input fuzzifiers:** compare singleton, triangular and Gaussian fuzzification, with configurable width / standard deviation.
- **Defuzzification choices:** compare Centroid and Mean of Maxima. The Threshold option is labelled provisional in the interface.
- **Rule inspection and editing:** view rule firing strengths; add or delete rules and adjust available consequent and weight controls.
- **Step-by-step trace:** play, pause, move between steps or stages, change playback speed, and inspect formulas and intermediate state.
- **Rule-Base Doctor:** inspect a sampled completeness heatmap and rule-base diagnostic notes. Select a cell to load its inputs into the lab.
- **Control Surface:** explore a sampled input-to-output heatmap and select a sample for inspection in the lab.
- **Verification:** run five executable checks and view the Room Fan hand calculation.
- **Display options:** switch between light and dark themes and use keyboard shortcuts.

## Try the Room Fan example

The Room Fan preset starts with these values:

| Variable | Initial value |
| --- | ---: |
| Temperature | 25 °C |
| Humidity | 40% |

With the default inference settings, the reference example produces:

| Result | Value |
| --- | ---: |
| Centroid output | 59.785 |
| Mean of Maxima | 50.000 |

These values are covered by the built-in verification checks. Results can change when you modify operators, fuzzification, grid resolution, membership parameters, rules or the defuzzification method.

## How to use the lab

1. Open the [live application](https://akshat-coder2106.github.io/fuzzy-logic-lab/).
2. Choose a model from **Problem**.
3. Adjust the input sliders or enter numeric values.
4. Explore membership plots and rule firing strengths.
5. Change inference operators or the defuzzification method to compare results.
6. Use **Playback & trace** to follow the inference pipeline step by step.
7. Visit **Rule-Base Doctor**, **Control Surface** and **Verification** for further analysis.

### Keyboard shortcuts

| Shortcut | Action |
| --- | --- |
| `Space` | Play / pause the trace |
| `←` | Step backward |
| `→` | Step forward |
| `R` | Reset the trace |

Shortcuts are ignored while focus is inside an input, select or text field.

## Run locally

The application is a single HTML file and does not require a build step or package installation.

```bash
git clone https://github.com/Akshat-coder2106/fuzzy-logic-lab.git
cd fuzzy-logic-lab
```

Open `index.html` directly in a modern web browser. The core application is implemented with HTML, CSS and vanilla JavaScript.

## Deployment

The live site is published with **GitHub Pages** from the repository's `main` branch and root folder.

- Repository: https://github.com/Akshat-coder2106/fuzzy-logic-lab
- Live application: https://akshat-coder2106.github.io/fuzzy-logic-lab/

To publish a change, commit the updated `index.html` to `main`. GitHub Pages will rebuild the site.

## Implementation notes

- The Control Surface is a sampled, perspective-style **2-D heatmap projection**, not a rotatable 3-D surface.
- The Threshold defuzzification option is explicitly marked provisional.
- Rule-Base Doctor's heatmap is sampled; continuity and overlap observations are heuristic diagnostics.
- The Custom preset is a starter configuration, not a full graphical rule-authoring environment.

## License

No license file is currently included in this repository. Unless a license is added, the source remains subject to the default copyright protections.
