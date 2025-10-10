# BIGP3B Dataset EEG BCI Analysis

This repository hosts a Jupyter notebook for loading, preprocessing, and analyzing the BigP3BCI dataset, focusing on P300 oddball event‑related potentials (ERPs) in an EEG brain–computer interface (BCI) paradigm.

## Contents

* `BIGP3BDataset_EEG_BCI.ipynb` – The primary notebook/pipeline:

  * Reading and filtering raw EDF files
  * Channel renaming and montage setting
  * Event detection and onset index computation
  * Epoching target vs. non‑target trials
  * ERP averaging and comparison at midline electrodes (Fz, Cz, Pz)
  * Feature extraction via windowed means and classifier pipeline

## Prerequisites

* **Python** ≥ 3.10
* **Conda** for environment management

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/BIGP3B_EEG_BCI.git
   cd BIGP3B_EEG_BCI
   ```
2. Create and activate a Conda environment:

   ```bash
   conda create -n bci_env python=3.10 -y
   conda activate bci_env
   ```
3. Install required packages:

   ```bash
   conda install -c conda-forge mne numpy scipy pandas matplotlib jupyter -y
   ```

## Usage

1. **Download the BigP3BCI data** (e.g. from PhysioNet):

   ```bash
   # example: place `C_04_SE001_CB_Train02.edf` and related files in `data/`
   ```
2. Launch Jupyter Lab or Notebook:

   ```bash
   jupyter lab
   ```
3. Open and run `BIGP3BDataset_EEG_BCI.ipynb`:

   * Step through cells to preprocess, epoch, and visualize P300 ERPs.
   * Modify parameters (e.g., epoch window, channels) as needed.

## Data Description

The BigP3BCI dataset contains single‑trial EEG recordings during an auditory oddball task. Key channels:

* **StimulusBegin** – Square pulse indicating flash onset
* **StimulusType** – Code for target vs. non‑target
* **PhaseInSequence** – Position in the stimulus sequence

Refer to the dataset documentation for full details: [https://physionet.org/content/bigp3bci/1.0.0/](https://physionet.org/content/bigp3bci/1.0.0/)

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---
*© 2025 Andy Gibson*
