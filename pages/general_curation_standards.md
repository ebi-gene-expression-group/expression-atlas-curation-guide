
# General curation standards

* [Plant experiments](#Plant-experiments)
* [Human cell line experiments](#Human-cell-line-experiments)
* [Mouse experiments](#Mouse-experiments)
* [Human disease experiments](#Human-disease-experiments)


## Plant experiments
<span style="color: rgb(0,0,0);"><u><span style="font-size: 14.0px;">Required metadata</span></u><span style="font-size: 14.0px;">:</span> The minimum information required to describe the properties of the source material used in a plant genomics experiment is the following:</span>

*   <span style="color: rgb(0,0,0);">organism > NCBITaxon term that should be also in EFO</span>
*   <span style="color: rgb(0,0,0);">ecotype > EFO or cultivar > EFO</span>
*   <span style="color: rgb(0,0,0);">age > number + unit[time unit] > EFO</span>
*   <span style="color: rgb(0,0,0);">developmental stage > EFO</span>
*   <span style="color: rgb(0,0,0);">organism part > PO term that should be also in EFO</span>  

<span style="color: rgb(0,0,0);">**Ecotype:** Columbia (Col-0) is the most popular ecotype of Arabidopsis thaliana and has been widely used for various studies in the molecular and genetic fields (Meyerowitz 1989). Other frequently used ecotypes are Landsberg erecta (Ler) and Wassilewskija (Ws-0). Sometimes it is not easy to know if something like _cop-1_ is a genotype (_cop1_ mutant?) or an ecotype. You can check the ecotype in this web page: <span style="color: rgb(0,0,0);">[https://www.arabidopsis.org](https://www.arabidopsis.org/). </span></span><span style="color: rgb(0,0,0);">For example, Col-0 as 'genetic background' should be curated as Characteristics [ecotype] -> Col-0</span>

<span style="color: rgb(0,0,0);">For cultivated plants (mainly food crop or cash crop like cut flowers), use cultivar as their variation is due to selective cultivation (breeding) by humans. For Arabidopsis, use ecotype.</span>

<span style="color: rgb(0,0,0);">**Age** (EFO_0000246): is a temporal measurement of the time period elapsed since an identifiable point in the life cycle of an organism. If a developmental stage is specified, the identifiable point would be the beginning of that stage. Otherwise the identifiable point must be specified such as planting (e.g. 3 days post planting). In plant biology there are different ways of describing the 'moment' the sample is taken: DAP (day after pollination) and DPA (day post anthesis). It could be considered as ‘sampling time point’ </span>

**Developmental stage** (EFO_0000399): For a complete review of ‘developmental stage’ in Arabidopsis see [ Growth Stage–Based Phenotypic Analysis of Arabidopsis: A Model for High Throughput Functional Genomics in Plants](http://europepmc.org/abstract/MED/11449047)  
A common term in plant biology is seedling that is a developmental stage, see [seedling developmental stage](http://www.ebi.ac.uk/ols/ontologies/po/terms?iri=http%3A%2F%2Fpurl.obolibrary.org%2Fobo%2FPO_0007131)

Characteristics [organism part] -> 4-day old seedling should be curated as: 

<pre>    Characteristics [age] -> 4; Unit [time unit] -> day  
    Characteristics [developmental stage] -> seedling  
    Characteristics [organism part] -> whole organism</pre>

<span style="color: rgb(0,0,0);">**Organism part**. Check if the term used is in EFO. For example, 'root tip tissue' should be 'root tip' and 'embryo' should be **plant embryo**</span>

<span style="color: rgb(0,0,0);"></span>

<span style="color: rgb(0,0,0);"><u>Optional metadata</u>: According to the study design, the following information is required in order to describe the plant sample:</span>

*   <span style="color: rgb(0,0,0);">genotype</span>
*   <span style="color: rgb(0,0,0);">phenotype</span>
*   <span style="color: rgb(0,0,0);">compound > CHEBI term that should be also in EFO</span>
*   <span style="color: rgb(0,0,0);">infect > NCBITaxon term that should be also in EFO</span>
*   <span style="color: rgb(0,0,0);">growth condition</span>  
    <span style="color: rgb(0,0,0);">  
    </span>

**Genotype design**<span style="color: rgb(0,0,0);"> (EFO_ 0001748) is a study design type that compares genotype, haplotype, or other individual genetic characteristics. The sample attribute is genotype (EFO_0000513). In plant biology, there are two main types of plant material in a genotype design experiment:</span>

1.  <span style="color: rgb(0,0,0);">Mutant plants. Mutant plants could be identified by the 'mutant name’ typically associated with the ‘mutated gene name’, for example, _spl7_ mutant. </span>
2.  <span style="color: rgb(0,0,0);">Transgenic plants. Transgenic plants could be identified with the ‘promoter name’ and the ‘gene name’, for example _35S::PdGA20ox1_ or _DX15::PdGA20ox1_</span>

<span style="color: rgb(0,0,0);">The term **phenotype** (EFO_0000651), as the detectable outward manifestations of a specific genotype, allows describing in more detail the plant sample studied. </span>

<span style="color: rgb(0,0,0);">**Genetic modification design** (EFO_0001758), that is, a design type where an organism(s) has had genetic material removed, rearranged, mutagenized or added, such as knock out. The sample attribute is **genetic modification** (EFO_0000510). There are two main strategies to study the biological function of a gene or set of genes in plant functional genomics:</span>

1.  <span style="color: rgb(0,0,0);">Loss of function strategy (decreasing gene expression levels) to obtain gene knock out (EFO_0000506, MI_0788) or gene knock down (MI_0789) </span>
2.  <span style="color: rgb(0,0,0);">Gain of function strategy (increasing gene expression levels), for example, overexpression of a gene in a transgenic plant </span>

<span style="color: rgb(0,0,0);">**Compound treatment design** (EFO_0001755), where the response to administration of a compound or chemical (including biological compounds such as hormones) is assayed. The sample attribute is **compound** (is not in EFO). The most similar term in EFO is chemical compound (CHEBI_37577) and compound based treatment (EFO_0000369). </span>

<span style="color: rgb(0,0,0);">**Pathogenicity design** (EFO_0001761), where an infective agent such as a bacterium, virus, protozoan, fungus etc. infects a host organism(s) and the infective agent is assayed. The sample attribute is **infection** (EFO_0000544). </span><span style="color: rgb(0,0,0);">For example, Characteristics [infect] -> Xanthomonas oryzae pv. Oryzae</span>

**Stimulus or stress design**<span style="color: rgb(0,0,0);"> (EFO_0001762), where the response of an organism(s) to the stress or stimulus is studied, e.g. osmotic stress, heat shock, radiation exposure, etc. Instead of using the general term 'stimulus' use the following ones:</span>

1.  <span style="color: rgb(0,0,0);">environmental stress (EFO_0000470) > use as value terms from <span style="color: rgb(0,0,0);">the </span>**Plant Environment Ontology**<span style="color: rgb(0,0,0);"> (EO) includes a set of plant treatments (EO_0001001) </span></span>
2.  <span style="color: rgb(0,0,0);">irradiate (EFO_0000554) > number + unit[irradiation unit] > Gray</span>
3.  <span style="color: rgb(0,0,0);">temperature (EFO_0001702) > number + unit[temperature unit] > degree celsius</span>

**What to do when NCBITaxon, PO, CHEBI terms are not in EFO?**

1.  Create a ticket in the Pivotal project ‘AE2/Atlas Curation’ called ‘Terms to be added to EFO - weekXX_yearXXXX’
2.  Just add as description "The following terms needs to be added to EFO" and tag the ticket with the "efo" label
3.  Include each term that needs to be added + their ontology ID and the accession number of the experiment in which the term was used to annotate the samples.
4.  Assign the ticket to Laura Huerta to centralise all ontology requests.

## Human cell line experiments

Cell line experiments are the ones involving immortalized cell lines and naturally immortal cell lines (e.g. stem cell lines). This category does not include primary cell lines and plant cell lines. 

<u>Required metadata</u>:

*   organism > NCBITaxon term that should be also in EFO
*   cell line > should be in EFO. The cell line term that you use to annotate your samples must be exactly the term used in EFO
*   disease > EFO
*   organism part > UBERON term that should be also in EFO
*   cell type > CL term that should be also in EFO - no longer mandatory as many cancer cell types aren't applicable

Comments:

*   disease > this term captures the disease(s) that the individual from which the cell line originated was suffering from.

Special cases:

*   biosource provider > company name. Can be added as a characteristics if the cell line is a primary cell line that is commercially available but does not have a specific cell line name (e.g. Human aortic endothelial cells (HAECs) in [E-MTAB-6605](https://www.ebi.ac.uk/arrayexpress/experiments/E-MTAB-6605))


**What to do when a cell line is not in EFO?**

1.  Create a a ticket in the Pivotal project ‘AE2/Atlas Curation’ called ‘Cell lines to be added to EFO – weekXX_yearXXXX’
2.  Upload a spreadsheet to that Pivotal ticket with one cell line per row and the following information per columns:

*   cell line
*   cell type > CL (should be also in EFO)
*   organism part > UBERON (should be also in EFO)
*   organism > NCBITaxon (should be also in EFO)
*   sex > EFO
*   disease > EFO
*   definition > e.g. human leukemia cell line established from the bone marrow of a 57-year-old woman with plasma cell leukemia (IgA1kappa) at diagnosis in 1987 (DSMZ catalog number ACC 541)
*   synonyms > - definition citation

Tips:

*   Google search the cell line name and the words "cell line" e.g. "AMO-1 cell line". Results from cell line repositories such as Cellosaurus, ATCC, DSMZ, Sigma-Aldrich or ECACC General Cell Collection are good references to find the information.

*   Add the catalog number at the end of the definition in brackets: e.g. (DDSMZ catalog number ACC 583), (ATCC CRL-2780), (Sigma catalog number 04072103), (ECACC catalog number 86012804)

*   Check Cellosaurus ([http://web.expasy.org/cellosaurus/](http://web.expasy.org/cellosaurus/)) for synonyms

*   The definition citation should be just the URL of the webpage where you found the information.

*   Sometimes all that comes back is some research papers -- if this is all you find put the PubMed ID in the definition citation column.

*   If you use more that one term per column separate them using two vertical lines, e.g. A-549||A 549||NCI-A549||hA549

**What to do when a disease is not in EFO?**

1.  Create a ticket in the Pivotal project ‘AE2/Atlas Curation’ called ‘Terms to be added to EFO - weekXX_yearXXXX’
2.  Just add as description "The following terms needs to be added to EFO" and tag the ticket with the "efo" label
3.  Include each disease that needs to be added + accession number of the experiment in which the term was used to annotate the samples and the following information:
    1.  Definition
    2.  Parent term


## Mouse experiments

<u>Required metadata</u>:

*   organism > NCBITaxon that should be also in EFO)
*   strain > EFO
*   age > number + unit[time unit] > EFO || developmental stage > EFO
*   sex > EFO
*   organism part > UBERON (should be also in EFO)
*   genotype
*   disease > EFO  

<u>Optional metadata</u>:

*   individual
*   cell type > CL (should be also in EFO)
*   phenotype
*   growth condition
*   sampling site


## Human disease experiments

<u>Required metadata</u>:

*   organism > NCBITaxon that should be also in EFO)
*   individual (if applicable)
*   age > number + unit[time unit] > EFO || developmental stage > EFO
*   sex > EFO
*   organism part > UBERON (should be also in EFO)
*   disease > EFO

<u>Optional metadata:</u>

*   ethnic group

Please tag these experiments as 'atlas curation' and 'OpenTargets' in the Pivotal project 'AE2/Atlas Curation' so we can easily find them.

We send data on human disease experiments to OpenTargets to be included in their platform. OpenTargets platform presents associations between genes and diseases in an attempt to help researchers develop drug targets. They are currently interested in all our human disease experiments, but especially in comparisons between **diseased and normal primary tissue**. For this type of comparison, they display a "transcript activity" indicating whether the gene shows increased or decreased activity in the disease when compared with normal tissue. They only want to display this information for "disease vs normal", in **primary tissues**. In cancer experiments, the tissue should be the main affected tissue of the cancer - for example, the comparison "breast carcinoma vs normal" would be allowed if the organism part was "breast". It would not be allowed if the organism part was e.g. "lymph node" (see [ E-GEOD-44408](http://www.ebi.ac.uk/gxa/experiments/E-GEOD-44408/Results)). In this case we can still load the experiment but OpenTargets do not want to display the "transcript activity" for genes for this comparison, as it is not about the original tissue of the cancer. For non-cancer diseases, any tissue is OK as long as it's from real patients and the comparison is disease vs normal. Also not allowed are comparisons on cell lines or other "non-primary" tissue, comparisons about treatments e.g. "response to chemotherapy vs no response to chemotherapy", etc.

To handle this on Expression Atlas, we decided to add a new attribute to the experiment XML configuration, in the contrast element, called cttv_primary. When you (or Conan) run gxa_generateConfigurationForExperiment.pl, this attribute will always be given a zero, e.g.

```
<contrast id="g1_g2" cttv_primary="0">
```

If your comparison is comparing **disease vs normal** in **primary tissue** of the disease origin, please change this to a 1, e.g.:

```
<contrast id="g1_g2" cttv_primary="1">
```

This will then be picked up by the code that collects data to send to OpenTargets, enabling the "transcript activity" to be defined for the differentially expressed gene(s) in this comparison on the OpenTargets website.


