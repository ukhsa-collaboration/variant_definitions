
# Standardised Variant Definitions

This is a repository containing the up-to-date lineage definitions for variants of concern (VOC) and variants of interest (VUI) as curated by Public Health England. They are provided in order to facilitate standardised VOC and VUI calling across sequencing sites and bioinformatics pipelines and are the same definitions used internally at Public Health England. The mutations have been chosen to aid rapid and sensitive identification from sequence data: these are typically only a subset of the total set of mutations found in a variant. 

Variant definitions are subject to change at any time. The latest release can be downloaded under the releases tab. A <a href="CHANGELOG.md">CHANGELOG</a> is available. For email notifications when this repository is updated, please use the GitHub "Watch" functionality at the top right of this page.

## Variant List

| Label                  | Lineages              | Description                             |
| ---------------------- | --------------------- | --------------------------------------- |
| <a href="variant_yaml/denture-daughter.yml">VOC-20DEC-01</a> | PANGO: <a href="https://cov-lineages.org/global_report_B.1.1.7.html">B.1.1.7</a>, nextstrain: <a href="https://nextstrain.org/sars-cov-2/">N501Y.V1</a> | This variant became widespread in the UK in the Winter of 2021 and is characterised by increased transmissibility. |
| <a href="variant_yaml/carnival-shimmy.yml">VOC-20DEC-02</a> | PANGO: <a href="https://cov-lineages.org/global_report_B.1.351.html">B.1.351</a>, nextstrain: <a href="https://nextstrain.org/sars-cov-2/">N501Y.V2</a> | This variant became widespread in countries in Southern Africa at the end of 2020 and has now been exported to a number of other countries including the UK |
| <a href="variant_yaml/unloved-crouton.yml">VOC-21FEB-02</a> | PANGO: <a href="https://cov-lineages.org/global_report_B.1.1.7.html">B.1.1.7</a> | This variant is a cluster of B.1.1.7 (VOC202012/01) that contains E484K and is associated with the Bristol area |
| <a href="variant_yaml/slinky-antennae.yml">VOC-21JAN-02</a> | PANGO: <a href="https://cov-lineages.org/global_report_P.1.html">P.1</a> | This variant was first identified in Japan in travellers from Brazil and is associated with Manaus in the Amazonas region assoicated with a severe second wave of COVID-19 |
| <a href="variant_yaml/cheesy-styling.yml">VUI-21FEB-01</a> | PANGO: <a href="https://cov-lineages.org/global_report_A.23.1.html">A.23.1</a> | This variant is a cluster within clade A.23.1 containing E484K observed in Liverpool |
| <a href="variant_yaml/glorious-saucy.yml">VUI-21FEB-03</a> | PANGO: <a href="https://cov-lineages.org/global_report_B.1.525.html">B.1.525</a> | This variant is a cluster of E484K containing genomes |
| <a href="variant_yaml/animating-thermos.yml">VUI-21FEB-04</a> | PANGO: B.1.1.318 | This variant is a cluster of E484K containing genomes |
| <a href="variant_yaml/marbling-doodle.yml">VUI-21JAN-01</a> | PANGO: P.2 | This variant became widespread in Rio de Janeiro, Brazil and imported cases have been reported in a number of other countries including the UK |
| <a href="variant_yaml/cornstalk-handprint.yml">VUI-21MAR-01</a> | PANGO: B.1.324.1 | First detected in the UK in a traveller from Antigua. |
| <a href="variant_yaml/mushroom-android.yml">VUI-21MAR-02</a> | PANGO: P.3 | This variant appeared to be closely associated with the Phillipines and widely divergent from anything else upon discovery. |
| <a href="variant_yaml/habitable-pasty.yml">VUI-21APR-01</a> | PANGO: B.1.617.1 | This variant is reported to be circulating in India and has been exported to other countries. |
| <a href="variant_yaml/empathy-serve.yml">VOC-21APR-02</a> | PANGO: B.1.617.2 | This variant is reported to be circulating in India and has been exported to other countries. |
| <a href="variant_yaml/spherical-trial.yml">VUI-21APR-03</a> | PANGO: B.1.617.3 | This variant is reported to be circulating in India and has been exported to other countries. |
| <a href="variant_yaml/harbor-sprite.yml">E484K</a> | PANGO: Multiple | Catch-all definition to identify sequences with the E484K spike variant |
| <a href="variant_yaml/dandelion-marshy.yml">VUI-21MAY-01</a> | PANGO: AV.1 | This variant has been observed in a growing cluster in the UK |

## File format definition

Each variant is stored one-per-file in the `variant_yaml` directory. Each file should be syntactically correct YAML. The file should be named according to its `unique-id` (unique identifer) with the suffix `.yml`.

You can check that files are correct using the `yaml-validator.py` script.

| Top-level block              | Required | Type         | Description                                                  |
| ---------------------------- | -------- | ------------ | ------------------------------------------------------------ |
| unique-id                    | yes      | text         | A unique identifier for this definition file, should never change. |
| phe-label                    | yes      | text         | The official Public Health England description for this variant, may change over time (e.g. upgrade VUI to VOC) |
| alternate-names              | no       | list of text | Synonyms for this variant for ease of referencing            |
| belongs-to-lineage           | no       | list of dict | Lineage descriptions for commonly used lineage naming schemes e.g. PANGO and nextstrain |
| description                  | yes      | text         | Description of the variant                                   |
| information-sources          | no       | list of URLs | Useful references (not exhaustive) to official information sources about the discovery and monitoring of this reference |
| acknowledgements             | no       | list of text | Acknowledgements to people or institutions involved in creating this definition |
| curators                     | no       | list of text | List of individuals responsible for maintaining this definition file |
| **variants** block           | yes      | list of dict | List of mutations (SNPs, insertions and deletions) defining this variant |
| amino-acid-change            | no       | text         | amino acid change, relative to coordinates of gene, e.g. N501Y |
| codon-change                 | yes      | text         | codon change encoded as reference codon - alternate codon e.g. "AAT-TAT" |
| protein-codon-position       | yes      | text         | codon position for `codon-change` according to protein annotation (not gene) |
| gene                         | no       | text         | the gene corresponding to annotations in change and codon-change |
| one-based-reference-position | yes      | integer      | the start position of the mutation, 1 based encoded - all mutations are encoded relatively to SARS-CoV-2 reference genome NC_045512.2 |
| reference-base               | yes      | text         | The base or bases (for deletions) in reference corresponding with one-based-reference-position |
| predicted-effect             | no       | text         | synonymous, non-synonymous, no-effect (e.g. upstream stop) |
| protein                      | no       | text         | the mature protein product (used for amino-acid-change, codon-change and protein-codon-position) |
| type                         | yes      | text         | SNP, MNP, insertion, deletion |
| variant-base                 | yes      | text         | The mutated base or bases (for insertions) in the variant at one-based-reference-genome, encoded as per VCF |
| **calling-definition** block | no       | dict         | A set of dictionary labels defining 1 or more calling definitions |
| mutations-required           | yes      | integer      | number of mutations (SNPs or MNPs) required to call the mutation |
| indels-required              | yes      | integer      | number of insertions or deletions from the variant definition required |
| allowed-wildtype             | yes      | integer      | how many wild-type (reference) calls are permitted to satisfy this calling definition |
|                              |          |              |                                                              |

## Contact

For further information, help or assistance contact PHE Genomics Cell at <covid19genomics@phe.gov.uk>

## Contributors

 - Matt Bull (PHW)
 - Meera Chand (PHE)
 - Tom Connor (PHW)
 - Nick Ellaby (PHE)
 - Natalie Groves (PHE)
 - Katri Jalava (PHE)
 - Nick Loman (University of Birmingham/PHE)
 - Richard Myers (PHE)
 - Sam Nicholls (University of Birmingham/PHE)
 - Ulf Schaefer (PHE)


