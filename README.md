# Code for the paper "The Potential Role of a Hydrogen Network in Europe"

[![DOI](https://zenodo.org/badge/513162844.svg)](https://zenodo.org/badge/latestdoi/513162844)


This repository contains the code and manuscript accompanying the paper "The Potential Role of a Hydrogen Network in Europe".

## Abstract

Electricity transmission expansion has suffered many delays in Europe in recent
decades, despite its significance for integrating renewable electricity. A
hydrogen network reusing the existing gas network could not only help to supply
demand for low-emission fuels, but could also balance variations in wind and
solar energy across the continent and thus avoid power grid expansion. We pursue
this idea by varying the allowed expansion of electricity and hydrogen grids in
net-zero CO2 scenarios for a sector-coupled European energy system. With 181
regions and 3-hourly time series, we capture transmission bottlenecks, the
variability of demand and renewable supply, and potentials for retrofitting gas
pipelines and developing geological hydrogen storage. We find that a hydrogen
network connecting regions with low-cost and abundant renewable potentials to
demand centers, electrofuel production and cavern storage sites reduces system
costs by up to  26 bn€/a (3.4%). Between 64% and
69% of this network could reuse natural gas pipelines. While the expansion of
both networks together can achieve the largest cost savings of
9.9%, the expansion of neither appears as essential in a net-zero
system as long as higher costs can be accepted and flexibility options are
enabled to manage grid bottlenecks.

## Repository Structure

- `configs` contains configuration files for PyPSA-Eur and PyPSA-Eur-Sec for different scenarios.
- `notebooks` contains the Jupyter notebooks used for the evaluation of results.
- `paper` contains the `.tex` files for the paper.
- `workflows` contains the PyPSA-Eur, PyPSA-Eur, and technology-data workflows.

## Installation and Usage

Clone the repository including its submodules:

```sh
git clone --recurse-submodules git@github.com:fneum/spatial-sector
```

Install the necessary dependencies using `conda` or `mamba`:

```sh
mamba env create -f workflows/pypsa-eur/envs/environment.yaml
```

Navigate into the main Snakemake workflow directory of PyPSA-Eur-Sec:

```sh
cd workflows/pypsa-eur-sec
```

To run the scenarios of a particular configuration file (e.g. `configs/config.main.yaml`), run:

```sh
snakemake -call --configfile ../../configs/config.main.yaml plot_summary
```

This call requires a high-performance computing environment.

Please follow the documentation of [PyPSA-Eur](https://pypsa-eur.readthedocs.io) for more details.

## License

MIT