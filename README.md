# wild-etal_2020_ColoradoNexus
Repository for Wild et al. (2020) paper on Colorado Basin (Argentina) Energy-Water-Land Nexus Planning Study

## Contents
- [Abstract](#abstract)
- [Code Reference](#code-reference)
- [Journal Reference](#journal-reference)
- [Data Reference](#data-reference)
- [Reproduce My Experiement](#reproduce-my-experiement)

<br />

## Abstract
Integrated energy-water-land (EWL) planning has the potential to promote synergies and avoid conflicts in ways that sector-specific planning approaches cannot. Many of the most important decisions that influence emerging EWL nexus conflicts and synergies are implemented by decision makers at regional (e.g., large river basin, electricity grid) and sub-regional (e.g., river sub-basin, irrigation district) scales. However, actual implementation of integrated planning practices at these scales has been relatively limited. Indeed, simply collecting and visualizing data and interconnections across multiple sectors and sub-regions in a single, internally consistent modeling platform is a unique endeavor in many regions. This study introduces and applies a novel approach to linking together multiple sub-regions, and their constituent EWL systems, in a single platform to characterize and visualize EWL resource use, EWL system linkages within and among sub-regions, and the EWL nexus implications of future policies and investments. This integrated sub-regional planning methodology is applied in the Colorado River Basin in southern Argentina, a water-stressed and drought-stricken basin that is facing increasing demands for water-intensive agricultural and fossil fuel commodities. Guided by stakeholders, this study seeks to inform basin planning activities by characterizing and visualizing (1) the current state of EWL resources in the basin, (2) the linkages between sectors, and (3) the EWL nexus implications of planned future agricultural development activities in the basin. Results demonstrate that water scarcity, driven in part by human system demands that have historically reached 60% of total surface water supply, poses a substantial constraint to economic development in the basin. The Colorado basin has the potential to serve as a testbed for crafting novel and generalizable sub-regional EWL planning approaches capable of informing the regional EWL planning dialogue globally.

[Back to Contents](#contents)

<br />

## Code Reference
<!-- for each minted software release for all code involved.  If you have modified a codebase that is outside of a formal release, and the modifications are not planned on being merged back into a version, fork the parent repository and add a `.<shortname>` to the version number of the parent and conduct your own name.  For example, `v1.2.5.hydro`.-->
metis [![GitHub tag](https://img.shields.io/github/v/tag/JGCRI/metis)](https://www.github.com/JGCRI/metis/tree/wild_et_al_2020_ColoradoNexus)

GCAM [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3897519.svg)](https://doi.org/10.5281/zenodo.3897519)

<!--
#### Example:

Wild, T.B. (2020). Colorado Nexus Repository. Github. https://github.com/FeralFlows/wild-etal_2020_ColoradoNexus.git
-->

[Back to Contents](#contents)

<br />


## Journal Reference
Journal reference will be updated after acceptance.

[Back to Contents](#contents)

<br />

## Data reference

### Input Data

The input data in this study is at sub-regional level within the Colorado basin. For more details, please check the CSV files within the /metis_input directory.

  1. Supply capacity for water and electricity (gas, refined liquid oil, and hydropower).
  2. Demand for multipal sectors (see table below).
  3. Stream network connectivity matrix.

| Demand Sector | Class | Supply Sector |
|---|---|---|
| Agritculture | Fruit trees, pasture, cereals, specialty, and vegetables | Water |
| Municipal | N/A | Water |
| Electricity | Diesel fuel, gas, and hydropower | Water |
| Livestock | Vacas, vaquillonas, novillos, terneros, and toros | Water |
| Residential | N/A | Electricity |
| Commercial | N/A | Electricity |
| industrial | N/A | Electricity |
| Export | N/A | Electricity, agriculture, and livestock |
| Other | N/A | Electricity |

<!--
#### Example:

Human, I.M. (2020). My dataset name [Data set]. DataHub. https://doi.org/some-doi-number


### Output Data
Reference for each minted data source for your output data.
-->

[Back to Contents](#contents)

<br />

## Contributing Models
| Model | Version | Repository Link/DOI |
|-------|---------|---------------------|
| metis | v1.0.0 | www.github.com/JGCRI/metis/tree/wild_et_al_2020_ColoradoNexus |
| GCAM | v5.1.3LAC | https://doi.org/10.5281/zenodo.3897519 |

[Back to Contents](#contents)

<br />

## Reproduce My Experiement

### Install Metis

1. Clone and install metis to your desired location from www.github.com/JGCRI/metis. This Metis GitHub repository has detailed installation instructions.

```
git clone https://github.com/JGCRI/metis.git
```

2. Checkout the metis model version used to run this publication's experiments. The git "tag" that points to the version/commit of metis used to run this publication's experiments is "wild_et_al_2020_ColoradoNexus". Nevigate into the cloned metis folder and run the following command to checkout the 'tagged' metis version.

```
git checkout tags/wild_et_al_2020_ColoradoNexus
```

3. To use the 'tagged' metis version associated with this paper, go to cloned metis folder, open metis.Rproj, select Build -> Document. Then select Build -> Install and Restart. If you previously installed metis, reload metis.

```
devtools::unload("metis")
library(metis)
```

### Reproduce the I/O Experiment

1. Clone reproducible repository into your desired location.

```
git clone https://github.com/FeralFlows/wild-etal_2020_ColoradoNexus.git
```

2. To run the I/O experiment, run the metis.masterX_io_colorado.R script.

3. To produce the figures, run the colorado_FinalMaps.R script within the /figures directory.

[Back to Contents](#contents)
