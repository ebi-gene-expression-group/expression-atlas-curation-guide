# What experiments can be included in Expression Atlas?


## General rules 

To be included in Expression Atlas or Single Cell Expression Atlas each experiment must meet all of the following criteria:

* Experiment measures gene or protein expression
* Raw data are available
* All samples within the dataset belong to a single species
* Samples come from non-bacterial species
* The species genome is available through Ensembl
* Annotations for microarray probes are available
* Sufficient sample annotation is provided


## Experiment type specific rules

Depending on the experiment type a few more conditions must be met for inclusion.

For **differential** (bulk) experiments: 
* The experiment must have at least 2 experimental groups, with 3 biological replicates each 
* The experiment must have a clear control/reference group
* The experiment is not a two-colour microarray study

For **baseline** (bulk) experiments: 

* The experiment design does not involve any perturbations 
* The experiment should have at least 3 experimental groups with 3 biological replicates each

For **single cell** experiments:

* The experiment must be of a type supported by the Atlas pipelines, currently we can re-analyse the following single cell library protocols
  ```
  Smart-seq2
  Smart-like
  Drop-seq
  Seq-Well
  10xV2 (3 prime and 5 prime)
  10xV3 (3 prime)
  ```
* The experiment cannot contain a mix of different library construction protocols (with few exceptions, e.g. 10xV2 and 10xV3)


## Soft criteria

Additionally, we employ several “softer” guidelines to determine whether or not an experiment is eligible for inclusion into Expression Atlas:

* The experiment addresses a relevant biological question (is not technical or proof of principle study)
* Experimental metadata are of high quality and confidence
* The experimental design is not too complex (e.g. not too many factors) and allows for straightforward one-to-one comparisons


## Note

If an experiment is judged to be of particular interest and its inclusion in Expression Atlas is highly valuable for the community, 
we may decide to include it even if it fails some of the above guidelines. We also actively collaborate with several specialized initiatives
such as the Gramene consortium and OpenTargets and prioritize experiments that are of special interest to our partners.
