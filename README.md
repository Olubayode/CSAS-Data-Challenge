# CSAS-Data-Challenge

# CSAS Bayesian Analysis for Bat Speed and Swing Length

## Installation and Dependencies

### Installing the Dependencies

To install the dependencies to run the notebook provided in this repository, follow these steps after you have [anaconda](https://www.anaconda.com/products/individual#Downloads) install on your computer: 

1. **Clone the Repository:**
   - Open your command prompt and navigate to the directory where you want to clone the repository:
     ```bash
     cd path/to/your/directory
     ```
   - Clone the repository by running:
     ```bash
     git clone https://github.com/Olubayode/CSAS-Data-Challenge.git
     ```

   The cloned repository will contain the following major files:
   - `CausalModel.ipynb` (Jupyter Notebook for the analysis)
   - `environment.yml` (environment specification file)
   - `statcast_pitch_swing_data_20240402_20240630.arrow` (dataset file)

2. **Set Up the Environment:**
   - Open the Anaconda Command Prompt and navigate to the cloned folder:
     ```bash
     cd path/to/CSAS-Data-Challenge
     ```
   - Create the conda environment by running:
     ```bash
     conda env create -f environment.yml
     ```

3. **Activate the Environment:**
   - Activate the newly created environment by running:
     ```bash
     activate stat-rethink2-pymc_v4_env
     ```
   - **Note:** The environment setup process may take some time depending on your system.

4. **Register the Environment for Jupyter Notebooks:**
   - Register your environment as a valid notebook kernel by running:
     ```bash
     python -m ipykernel install --user --name stat-rethink2-pymc4 --display-name "Python 3.10 (CSAS Data Challenge)"
     ```

   #### Explanation of Your Command:
   1. `--name stat-rethink2-pymc4`:
      - Internally registers the kernel with the name `stat-rethink2-pymc4`. This is how Jupyter identifies the kernel behind the scenes.
   2. `--display-name "Python 3.10 (CSAS Data Challenge)"`:
      - This is the name that will appear in the Jupyter interface, so you can easily recognize and select the kernel when working on your project.


   This command will successfully create a new kernel for your Jupyter notebooks with:
   - Internal name: `stat-rethink2-pymc4`
   - Display name: `Python 3.10 (CSAS Data Challenge)`


5. **Start Jupyter Notebooks or Jupyter Lab:**
   - Start a notebook interface by running:
     ```bash
     jupyter notebook
     ```
     Or use the more modern Jupyter Lab interface:
     ```bash
     jupyter lab
     ```
   - Make sure you run these commands from the root directory of the cloned repository.

6. **Install Additional Python Packages:**
   - Once the Jupyter Lab or Notebook interface opens, install the following additional dependencies:
     ```bash
     pip install polars
     pip install pyarrow
     ```
   - These packages are necessary to access the datasets provided in the repository.

---

## Overview

### Project Topic

Explore how batter mechanics (bat speed and swing length), pitch characteristics (release speed and movement), and game context (inning, outs, and balls) influence the likelihood of fouling off 2-strike pitches.

### My Objective

The goal of this analysis is to explore how batter mechanics (bat speed and swing length), pitch characteristics (release speed and movement), and game context (inning, outs, and balls) influence the likelihood of fouling off 2-strike pitches. It’s a crucial topic for advancing our understanding of player performance and decision-making in high-pressure situations. Fouling off 2-strike pitches is a critical skill in baseball, as it enables the batter to extend at-bats, tire pitchers, and increase the chances of favorable outcomes and for pitchers, it helps to control the Zone and set up strikeouts. By identifying the factors that contribute to fouling off such pitches, teams can improve coaching strategies, player development, and game tactics.

Furthermore, this study could serve as a foundation for building a survival mechanism model, which explores how batters sustain themselves in the game by fouling off multiple pitches with two strikes. Such a model could analyze the factors contributing to prolonged at-bats and provide insights into the physical and mental attributes of successful batters. This analysis is limited to the first aspect and the second part can be explored further.

### Description

For this data challenge, the goal is to use new baseball data on bat speed and swing length to analyze some aspect of the pitcher/batter interaction. The dataset includes pitch-level data from Baseball Savant for 346,250 Major League Baseball plate appearances from 4/2/2024 to 6/30/2024, which includes:
- Relevant Statcast data 
- Bat speed and swing length on pitches with a swing tracked.

### Potential Analysis Topics

- **Batter-Specific Plate Discipline:**
  - Can bat speed and swing length be used to measure plate discipline?
  - Are faster swingers more patient?
  - How are bat speed or swing length related to a hitter’s ability to foul off 2-strike pitches or protect the plate?

- **Pitcher and Batter Behavior:**
  - Do pitchers "dictate" swings, or do batters influence pitcher behavior?
  - Are swing lengths longer against certain pitchers? Is this due to pitch velocity or spin rate?
  - Do pitchers change pitch location or type against batters with higher/lower bat speed?

- **Game Context:**
  - How are batter mechanics influenced by situations such as count, base runners, or outs?

### Data

The data is provided in two formats:

1. **CSV Format:**
   - The file contains data up to June 30, 2024, and is available in a shared folder. Due to its size, you may need to download and work on it locally.

2. **Apache Arrow Format:**
   - A columnar, in-memory format designed for fast analytics and interoperability between systems. Example codes for loading this data in Python, Julia, and R are available on [GitHub](https://github.com/CSAS-Data-Challenge/2025) and [Kaggle](https://www.kaggle.com/competitions/csas-2025-data-challenge/data).

And here is the [Glossary](https://baseballsavant.mlb.com/visuals/swing-take?playerId=545361) for the data

---


### Additional Resources

For more information about Bayesian analysis and how PyMC works, check out the [Statistical Rethinking materials](https://github.com/pymc-devs/pymc-resources/tree/main/Rethinking_2).

---

## License

**CSAS Bayesian Analysis for Bat Speed and Swing Length** © 2025 by Ebenezer Olubayode is licensed under the [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](https://creativecommons.org/licenses/by-nc-nd/4.0/).
