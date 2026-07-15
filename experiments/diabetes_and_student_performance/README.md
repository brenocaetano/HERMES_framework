# HERMES — Diabetes and Student Performance Experiments

This repository contains notebooks with experimental implementations of the HERMES pipeline applied to the **Diabetes 130-US Hospitals** and **Student Performance** datasets.

## Requirements

- Python version specified in `python-version.txt`
- `pip`
- Internet access, when required to obtain the datasets
- Local files `utils.py` and `phyil.py`

The `requirements.txt` file contains the dependencies and package versions required to run experiments for both datasets: **Diabetes** and **Student Performance**.

## Installation

1. Install the Python version specified in `python-version.txt`.

2. Open a terminal in the project directory.

3. Install the dependencies:

```bash
python -m pip install -r requirements.txt
```

## Execution

Open the notebook for the dataset you want to run in an IDE or environment compatible with Jupyter Notebook, such as Jupyter Notebook, JupyterLab, VS Code, Google Colab, or PyCharm.

Run the cells in the order in which they appear in the notebook.

## Expected Structure

```text
hermes-project/
├── README.md
├── python-version.txt
├── requirements.txt
├── hermes_diabetes_fix-2.ipynb
├── hermes_student_performance.ipynb
└── utils.py
└── phyil.py
```

## Outputs

The results of each experiment are saved in separate directories:

| Dataset | Output directory |
|---|---|
| Diabetes | `diabetes_binary_hermes/` |
| Student Performance | `student_performance_5objs/` |
