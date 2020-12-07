# Guidelines for curating ontology terms

All characteristics terms from all Atlas experiments are attempted to be mapped to ontology terms via the Zooma mapping procedure (see internal documentation how this is run). The output is a list of terms that could not be automatically mapped by Zooma because these haven't been seen before. Curators go through this list of terms and find the suitable ontology terms. The final term mappings are stored in the [zoomage_report.CURATED.tsv](https://github.com/ebi-gene-expression-group/curated-metadata) file on GitHub.

## General mapping strategy
:white_check_mark: DO try to find exact synonyms. I ask myself "would the annotation still have the same meaning if I used the ontology label instead?".

:white_check_mark: DO focus on the categories "organism part", "cell type", "disease", "cell line" as this is what people mostly search for in Expression Atlas.

:white_check_mark: DO only include terms from EFO or the ontologies named in the [zooma_ontologies.tsv](https://github.com/ebi-gene-expression-group/perl-atlas-modules/blob/master/supporting_files/zooma_ontologies.tsv) file. If you find a term that is in OLS but not in EFO or the listed ontology, it can be requested to be added in EFO.

:x: DON'T match more specific terms to more general terms. For example: "lower leg" → "leg"

:x: DON'T match general terms to more specific terms: e.g. "schizont" → "hepatic schizont"

:x: DON'T include terms that contain any other descriptors, e.g. "5 millimolar sodium sulfate" → "sodium sulfate"

:x: DON'T map terms that include reference to more than one entity: e.g. "head and thorax" → "head" | "thorax"


## How to find the terms

Look up the label in OLS EFO browser: https://www.ebi.ac.uk/ols/ontologies/efo

Sometimes a term is found in EFO but Zooma did not pick it up correctly but instead suggests a different term. Just because it didn't automatically match the term, doesn't mean it isn't in EFO with the exact label. So it still makes sense to look up these terms in OLS.

 
## Cell lines

First check if the cell line exists in the Cellosaurus database: https://web.expasy.org/cgi-bin/cellosaurus/search

If yes, continue to find the term in EFO.

For cell lines, there is often small differences that make the automatic mapping fail, like spaces or hyphens in different places:

MCF7 vs. MCF-7 vs. MCF 7

Try to look up different combinations of spacing around the letters, let the synonyms in Cellosaurus help you.

If you are not sure if a term matches with the cell line that was used in this experiment, look up the experiment and check the annotations and see if they match, e.g. both are "lung adenocarcinoma".


## Inferred cell types

For mapping inferred cell type terms to ontology terms, see the [inferred cell type curation guidelines](inferred_cell_type.md#general-style).
