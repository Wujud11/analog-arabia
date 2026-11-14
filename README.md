# Analog Arabia: a mission-fit atlas of Mars and Moon test sites in the Arabian Peninsula

**NASA Space Apps Challenge 2026** · Challenge: Identify Earth Locations That Analog the Permanent Moon Base Locations and Mars · Saudi Arabia

## Summary
NASA mostly tests rovers, instruments and crews at a few famous analog sites. The Arabian Peninsula has sites that fit specific tests at least as well, yet they rarely appear on analog shortlists. Analog Arabia lets a user pick a mission type (rover test, habitat trial, astrobiology, orbital instrument, unexplored) and ranks eight candidate sites by fit, next to three famous analogs (Atacama, Devon Island, Kilauea) rated on the same criteria. The Arabian sites lead on habitat, orbital-instrument and rover tests; Atacama leads on astrobiology. Each site card shows sourced facts, its Mars or Moon twin, field constraints, live NASA satellite imagery, and NASA POWER climate.

## How to run it
Open `index.html` in any modern browser. It needs no build step, server or API key.
To publish it, enable **GitHub Pages** for this repo (Settings → Pages → Deploy from branch → `main` / root). The live NASA data loads on the published page.

## NASA data used
| Dataset | How it is used |
| --- | --- |
| NASA POWER climatology API (power.larc.nasa.gov) | Live precipitation, surface skin temperature, air temperature, solar radiation and wind for every site; feeds the measured climate criterion in the score |
| NASA GIBS: MODIS Terra Corrected Reflectance (True Color) | Live satellite view of each site |
| NASA GIBS: ASTER GDEM Color Shaded Relief | Terrain view of each site |
| NASA Earth Observatory: White and Black Volcanoes of Saudi Arabia (Landsat 9) | Harrat Khaybar geology |
| NASA Earth Observatory: Harrat Khaybar Volcanic Field (ISS016-E-34524) | Tuff cones and evidence of a wetter past |
| NASA: lava field southeast of Medina (iss071e235550) | Harrat Rahat imagery |
| NASA Earth Observatory: A Long-Ago Lake Amid the Dunes | Jubbah paleolake |
| NASA Worldview | A per-site link to explore the imagery |
| NASA Moon Trek (LRO WAC mosaic) and Mars Trek (Viking MDIM 2.1 colour mosaic) | A tile of the paired Moon or Mars target for every site |
| NASA mission pages: LRO, Apollo 11, Perseverance, Curiosity, Opportunity, InSight | Target coordinates and why each target matches |

Other references (peer-reviewed papers, USGS and IUGS) are linked on each site card in the app.

## Moon and Mars targets
Every Earth site is paired with a named Moon or Mars target: Umm Jirsan with the Mare Tranquillitatis pit, Jubbah with Jezero crater, Rub' al Khali with Gale crater's Bagnold Dunes, Lunayyir with Cerberus Fossae, Al Wahbah with Meridiani Planum, and so on. No Arabian site reproduces the lunar south pole's permanent cold and shadow; the sites match lunar lava tubes and mare basalt instead, which are candidate places for a sheltered base.

## Methodology: weighted multi-criteria decision analysis (MCDA)
Score = Σ(weight × criterion) ÷ Σ(weight × 5) × 100 over nine criteria, with one weight set per mission.
- **Measured live from NASA POWER:** Mars-like climate = 0.7 × dryness + 0.3 × sunlight (dryness from annual precipitation PRECTOTCORR; sunlight from ALLSKY_SFC_SW_DWN). Surface skin temperature (TS), air temperature and wind are shown for every site.
- **From the scientific literature:** Mars likeness, Moon likeness, rover terrain, shelter, past water, orbital calibration, access and novelty, rated 0–5 from the sources cited on each site card.
- **Planned, not yet in the score:** SRTM/NASADEM terrain roughness and EMIT surface minerals.

Coordinates come from the Smithsonian Global Volcanism Program, published papers and NASA pages.

## Use of AI
The project was built by one participant directing AI agents (Claude, by Anthropic): a research agent, a build agent, a writing agent, and an independent "judge" agent that fact-checked the work. The participant chose the challenge and the regional angle and made the final decisions. No AI-generated images are used.

## Team
- (Your name): Team Owner
