# HERMES — Diabetes and Student Performance Experiments

This repository contains notebooks with experimental implementations of the HERMES pipeline applied to the **Diabetes 130-US Hospitals** and **Student Performance** datasets. 

The project is structured into two independent directories, ensuring that each dataset has its own isolated environment, helper scripts, and requirement files.

## Requirements

For each dataset environment, you will need:
- Python version specified in the respective `python-version.txt`
- `pip`
- Internet access, when required to obtain the datasets
- Local helper scripts: `utils.py`, `phyil.py`, and `damicore.py`

Each folder contains its own `requirements.txt` file with the dependencies and package versions required to run the experiments.

## Installation

Since the environments are separated, you must navigate to the specific directory of the dataset you want to test before installing the dependencies.

1. Open a terminal in the root directory of the project.
2. Navigate to the desired folder (`diabetes` or `student_performance`):
   ```bash
   cd diabetes
   # or
   # cd student_performance
