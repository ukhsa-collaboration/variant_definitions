# Changelog

## 1.4 - 2024-01-23

### Added
- `nutrient-magnesium`: Added definition for V-23DEC-01 (JN.1)

## 1.3 - 2023-08-23

### Added
- `poppy-deed`: Added definition for V-23AUG-01 (BA.2.86)

## 1.2 - 2023-08-07

### Added
- `wispy-subscript`: Added definition for V-23JUL-01 (EG.5.1)

## 1.1.1 - 2022-06-22

### Changed
- `imagines-viewable`: Increased `wildtype-allowed` for `low-qc` definition from 0 to 1 in line with probable definition
- `handler-hypnosis`: Increased `wildtype-allowed` for `low-qc` definition from 0 to 1 in line with probable definition

## 1.1 - 2023-05-19

### Added
- `handler-hypnosis`: Added definition for V-23APR-01 (XBB.1.16)

### Changed
- Corrected description in `vertical-sworn`  

## 1.0 - 2023-01-26

### Added
- `legroom-finished`: Added definition for V-22SEP-01 (BA.4.6)
- `monologue-underling`: Added definition for V-22OCT-01 (BQ.1)
- `edge-talon`: Added definition for V-22OCT-02 (XBB)
- `gaming-talon`: Added definition for V-22DEC-01 (CH.1.1)
- `vertical-sworn`: Added definition for V-23JAN-01 (XBB.1.5)

### Changed
- Updated MNP notation in yaml files. The full codon will now be included in `reference-base` and `variant-base` for 
any MNPs in the `variants` section of the yaml. Unchanged nucleotides will be written as `N` in the `variant-base` 
field to indicate that a wildtype call is not required to assign the mutation as present.
- `animating-thermos.yml`: removed T21I from mutations required
- `carnival-shimmy.yml`: removed N501Y from mutations required and alternate probable mutations
- `habitable-pasty.yml`: mutations required for probable call increased from 5 to 6
- This repository will now be maintained for all signals currently monitored by UKHSA.

## 0.11 - 2022-08-01

### Added
- `pampered-imagining`: Added definition for V-22JUL-01 (BA.2.75)

### Changed
- Skipped two minor versions for internal consistency to 0.11

## 0.8 - 2022-05-10

### Added
- `umbrella-embark`: Added definition for V-22APR-01 (XD)
- `outmost-resubmit`: Added definition for V-22APR-02 (XE)
- `radiator-ditto`: Added definition for V-22APR-03 (BA.4)
- `dipped-bubbling`: Added definition for V-22APR-03 (BA.5)

### Changed
- Updated definitions for pentagon-refining (VOC-21NOV-01) and imagines-viewable (VOC-22JAN-01)
- Added definitions for generic Omicron call (`plausible-scanner`) now required for VOC-21NOV-01, VOC-22JAN-01, V-22APR-03 and V-22APR-04
- `statistic-cadillac`: Added definition for BA.3 for monitoring purposes (not a declared variant)
- Renamed variants to new nomenclature (V instead of VUI)

## 0.7 - 2022-02-03

### Added
- `imagines-viewable`:  Definition for VUI-22JAN-01 (BA.2)

### Changed
- `pentagon-refining`: Reduced overlapping mutations to increase specificity vs VUI-22JAN-01 (BA.2)

## 0.6.1 - 2021-12-01

### Changed
- Fixed numbering for deletion at 21986
- Fixed nomenclature issue with MNP S371L
- Updated PHE name to VOC

## 0.6 - 2021-11-27

### Added
- `pentagon-refining`: New definition for Omicron (B.1.1.529)
- `curtain-oasis`: Definition for VUI-21OCT-01 (AY.4.2)

## 0.5.1 - 2021-07-29

### Changed
- `empathy-serve`: removed 4 mutations for broader variant definition

## 0.5 - 2021-07-29

### Added
- `kelp-lesser`: added VUI-21JUL-01 (B.1.621)
- New field: `who-label` with thanks to Theo Sanderson (WTSI)

## 0.4.1 - 2021-07-06
### Added
- `perfume-sprint`: added VUI-21JUN-01 (lambda/C.37)

## 0.4 - 2021-05-21
### Added
- `paragraph-footwork`: added VUI-21MAY-02 (C.36.3)

### Changed
- added `low-qc` for marbling-doodle

### Changed

## 0.3.5 - 2021-05-21
### Changed
- Fixed duplicate `variant` block

## 0.3.4 - 2021-05-21
### Added
- `dandelion-marshy`: added VUI-21MAY-01 (AV.1)

## 0.3.3 - 2021-05-07

### Added
- `harbor-sprite`: E484K mutation definition

### Changed
- `empathy-serve`: updated PHE label to VOC-21APR-02 to reflect VOC status

## 0.3.2 - 2021-04-29
### Added
- `empathy-serve`: new definition (VUI-21APR-02)
- `spherical-trial`: new definition (VUI-21APR-03)

### Changed
- `habitable-pasty`: reflects B.1.617.1, removed mutations 21895 and 22022
 
## 0.3.1

### Changed
- `glorious-saucy`: remove invariant base

## 0.3 - 2021-04-19

### Added
- `habitable-pasty`: new definition (VUI-21APR-01)
### Changed
- `animating-thermos`: removed positions 3852 and 24382
- `cornstalk-handprint`: fixed erroneous mutations at 28272

## 0.2.2 - 2021-03-17
### Changed
- `cornstalk-handprint`: removed `probable` definition, there is no probable definition for this variant

## 0.2.1 - 2021-03-16

### Added
- `cornstalk-handprint`: new definition (VUI-21MAR-01)
- `mushroom-android`: new definition (VUI-21MAR-02)
### Changed
- renamed variants according to updated PHE nomenclature (VOC/VUI-YYMMM-NN)

## 0.1.2 - 2021-03-07
### Changed
- `glorious-saucy`: fix incorrect variant base

## 0.1.1 - 2021-03-05
### Changed
- `slinky-antennae`: Fix amino acid definition for nsp12 mutation incorporating slippage annotation

## 0.1.0 - 2021-03-04
### Added
- Release of initial draft definition files

