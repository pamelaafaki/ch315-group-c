# Project handoff — 9 October 2026

The simulation website is unavailable. The user will return with the remaining data.

## Task

Complete `GroupC_Block2_project.ipynb` using the instructions in `/Users/chiarabifuclo/Desktop/Project.pdf`. Continue in this single project notebook; leave the previous assignment notebook unchanged. Do not invent numerical results.

## Writing preferences

- Match the simple, clear style of question 1 in the previous assignment.
- Write at third-year EPFL chemical engineering level, with concise explanations and no unnecessary repetition.
- Use question numbering 1–7 matching the project PDF; item 8 is report organisation.
- Use “Results for question X:” and omit “Discussion.” labels.
- Use readable Unicode units and CO₂/N₂ subscripts in prose and tables, avoiding visible dollar signs. Use properly delimited LaTeX for equations.
- Explain what properties mean; separate values, units and meanings where appropriate.
- Give explicit answers to qualitative questions, with limitations grounded in the data.

## Received data

- UTSA-80 pore analysis: Desktop/544.csv, copied to `UTSA-80_pore_analysis.csv` in this folder. Density 0.678215 g/cm³; ASA 3114.62 Å²/cell; POAV 9619.78 Å³/cell; porosity 0.66798.
- NOTT-300 pore analysis: Desktop/533.csv, copied to `NOTT-300_pore_analysis.csv`. Density 1.03926 g/cm³; ASA 453.452 Å²/cell; POAV 1297.11 Å³/cell; porosity 0.48999.
- Both use a 1.525 Å probe and 100,000 volume samples. Assignment specifies 10,000 samples. Preserve the actual settings in reporting.
- Desktop/871.csv was labelled IRMOF-1 but uses a 1.655 Å probe, has no ASA and reports density 0.886275 g/cm³. Copied to `IRMOF-1_export_to_check.csv`. User explicitly asked to IGNORE this file for now while checking. Do not use it in calculations.

## Next steps

Receive confirmed IRMOF-1 pore data and CO₂/N₂ simulation exports for all assigned materials at 25 °C (298.15 K). Confirm the full assigned material list.

Complete Henry coefficients and affinity ranking; pure-component isotherms; binary IAST at adsorption and desorption conditions; working capacity; CO₂/N₂ selectivity; working-capacity/selectivity plot and ranking; final conclusions.

Adsorption: 1 bar, 15% CO₂ / 85% N₂. Desorption: 0.2 bar, same temperature. Clearly state and confirm the assumed desorption gas composition: using the feed composition at both pressures is an equilibrium screening assumption, not a prediction of actual cycle composition.

Working capacity must use binary IAST loadings. Selectivity uses binary loadings at adsorption conditions. Check IAST reference pressures against the available isotherm range; do not silently extrapolate. Do not reuse previous 300 K CO₂/CH₄ data for this 298.15 K CO₂/N₂ project.

The notebook has question 1 results for UTSA-80 and NOTT-300, verified import/porosity code, explanations/placeholders for questions 2–6, and a drafted question 7 on equilibrium screening limits and process-level indicators (purity, recovery, productivity, energy). Code cells were run successfully.

## Additional data received

ZIF-8: Desktop/718.csv copied to `ZIF-8_pore_export.csv`. Probe radius 1.525 Å; 10,000 volume samples; density 0.909567 g/cm³; POAV 2189.3 Å³/cell; porosity 0.4391. ASA is absent: request full pore-analysis export. Included available properties in question 1 without inventing ASA. Porosity cross-check tolerance is 1e-4 to accommodate four-decimal exported volume fractions.

## Replacement ZIF-8 and additional pore data

New ZIF-8 source: Desktop/zif-pore analysis.csv, stored as ZIF-8_pore_analysis.csv. Supersedes ALL values from 718.csv; old export unused. Density 0.909567, ASA 787.421, POAV 2488.25, porosity 0.49906.
Mg-MOF source: Desktop/mgmof-pore analysis.csv, stored as Mg-MOF_pore_analysis.csv. Exact framework name requires confirmation; do not assume Mg-MOF-74 without confirmation. Density 0.886275, ASA 222.828, POAV 837.198, porosity 0.61368.
UTSA-20 screenshot transcribed into UTSA-20_pore_screenshot.csv: density 0.882399, ASA 1307.51, POAV 3575.36, porosity 0.62907, probe radius 1.525 Å. Unitcell volume and sample settings not reliably visible; not inferred. All four required properties are available. IRMOF-1 still missing corrected export.

## Isotherm exports received

Ten user files copied unchanged to received_isotherms/. mgmof-co2/n2, nott300-co2/n2, utsa20-co2/n2, utsa80-n2, utsa8-co2 and zif-co2 all contain Henry coefficients and isotherms from 0.2 to 10.2 bar, at reported 298 K (not 298.15 K). zif-n2.csv has neither Henry coefficient nor isotherm: replacement needed. Confirm whether utsa8-co2.csv is UTSA-80, exact Mg-MOF identity and whether IRMOF-1 belongs in final list. IRMOF-1 exports not supplied. Do not assume these identities.

## Confirmed material identities (latest instructions)

User confirmed utsa8-co2.csv is UTSA-80 CO₂. IRMOF-1 is NOT assigned; no IRMOF-1 data are needed. Mg-MOF is Mg-MOF-74, identified by supplied Desktop/Mg-MOF-74 (2).cif; stored in structures/Mg-MOF-74.cif. Calculated CIF cell volume matches pore export (~1364.22 Å³). Final five materials: UTSA-80, UTSA-20, NOTT-300, Mg-MOF-74, ZIF-8. ZIF-8 N₂ remains unavailable; user suspects small pores prevented simulation, but failure cause not confirmed. Do not set N₂ uptake to zero or calculate infinite selectivity without evidence.

ZIF-8 N₂ export checked: is_porous=False, POAV=0, estimated saturation=0, Input_volpo radius 1.655 Å. aiida-lsmo workflow source confirms Widom/GCMC skipped when no accessible volume. Missing data arise from geometric screening, not generic simulation failure; no replacement required to document limitation. Do not report measured KH=0, actual flat isotherm or finite mixture selectivity. Added explanation to question 2.

## Project completed

Notebook completed with seven executed code cells, saved tables and three plots. pyIAST 1.4.3 installed only in /tmp/block2-project-deps for execution; users need pyiast in their notebook environment. Four complete materials ranked NOTT-300 > Mg-MOF-74 > UTSA-20 > UTSA-80. WC: 2.786, 1.020, 0.490, 0.198 mmol/g; selectivity: 30.02, 27.10, 10.10, 5.19. Independent analytical piecewise-linear IAST calculation matched pyIAST in all eight states within 1e-6 relative tolerance. ZIF-8 unranked with documented geometric screening limitation. Same feed composition assumed at desorption; no high-pressure extrapolation, but low-pressure origin interpolation is required and explicitly discussed. All exports report 298 K.
