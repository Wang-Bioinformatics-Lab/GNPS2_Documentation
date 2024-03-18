
Modifinder is a tool for site localization of structural modifications using MS/MS data. 

## Data Input
**Universal Spectrum Identifiers:** The Universal Spectrum Identifiers(USI) for both known and unknown compounds should be provided as they encompass the peak information used in the alignment step.
**SMILES:** ModiFinder is designed to accept molecular structures in SMILES notation. Providing the SMILES for the unknown compound is optional and is used to generate additional results that are particularly useful for evaluating and visualizing ModiFinder's performance with compounds whose structures are already known.

**ppm:** This input determines the error tolerance of ModiFinder in ppm. This error tolerance is used both in the alignment step and when annotating the peaks with substructures.

**Adduct:** This input determines the Adduct used.

* There are examples provided in the examples tab, you can select any example and click on the update button to see the result.

## Visualization Output

**Stats Table:** This table contains general information about the pair, detailing aspects like the mass difference and the count of both total and shifted peaks observed in the alignment. In the case that SMILES2 is provided, an evaluation score is also provided. This evaluation score evaluates the ModiFinder performance against ground truth.

**Prediction:** This image shows a heatmap representation of the structure, where atoms with a higher likelihood of being the modification site are highlighted in shades of red, while those less likely to be modified appear in cooler blue tones.

**Modification Highlight:** If SMILES2 is provided, an image indicating the true modification and the modification site is displayed.

**Peaks:** This visualization displays the alignment of peaks, with the peaks of the known compound positioned at the top and those of the modified compound at the bottom. Peaks that are both matched and shifted are indicated in red, while matched but unshifted peaks are highlighted in blue. Peaks that do not have a match are represented in gray. Clicking on a matched and shifted peak will highlight that peak and its corresponding match.

## Refinement of MS/MS substructure annotation

By selecting a peak associated with the known compound, all the potential substructures assigned to that peak by ModiFinder will be shown. Users have the ability to manually filter these substructures, incorporating specialist domain knowledge into the filtering process.
