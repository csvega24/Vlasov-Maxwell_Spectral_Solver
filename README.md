<p align="center">
    <img src="https://raw.githubusercontent.com/uwplasma/SPECTRAX/refs/heads/main/docs/SPECTRAX_logo.png" align="center" width="30%">
</p>
<!-- <p align="center"><h3 align="center">SPECTRAX</h1></p> -->
<p align="center">
	<em><code>❯ spectrax: Hermite-Fourier Vlasov equation solver in JAX to simulate plasmas</code></em>
</p>
<p align="center">
	<img src="https://img.shields.io/github/license/uwplasma/SPECTRAX?style=default&logo=opensourceinitiative&logoColor=white&color=0080ff" alt="license">
	<img src="https://img.shields.io/github/last-commit/uwplasma/SPECTRAX?style=default&logo=git&logoColor=white&color=0080ff" alt="last-commit">
	<img src="https://img.shields.io/github/languages/top/uwplasma/SPECTRAX?style=default&color=0080ff" alt="repo-top-language">
	<a href="https://github.com/uwplasma/SPECTRAX/actions/workflows/build_test.yml">
		<img src="https://github.com/uwplasma/SPECTRAX/actions/workflows/build_test.yml/badge.svg" alt="Build Status">
	</a>
	<a href="https://codecov.io/gh/uwplasma/SPECTRAX">
		<img src="https://codecov.io/gh/uwplasma/SPECTRAX/branch/main/graph/badge.svg" alt="Coverage">
	</a>
	<a href="https://spectrax.readthedocs.io/en/latest/?badge=latest">
		<img src="https://readthedocs.org/projects/spectrax/badge/?version=latest" alt="Documentation Status">
	</a>

</p>
<p align="center"><!-- default option, no dependency badges. -->
</p>
<p align="center">
	<!-- default option, no dependency badges. -->
</p>
<br>


##  Table of Contents

- [ Overview](#-overview)
- [ Features](#-features)
- [ Project Structure](#-project-structure)
  - [ Project Index](#-project-index)
- [ Getting Started](#-getting-started)
  - [ Prerequisites](#-prerequisites)
  - [ Installation](#-installation)
  - [ Usage](#-usage)
  - [ Testing](#-testing)
- [ Project Roadmap](#-project-roadmap)
- [ Contributing](#-contributing)
- [ License](#-license)
- [ Acknowledgments](#-acknowledgments)

---

##  Overview

SPECTRAX is an open-source project in Python that uses JAX to speedup simulations, leading to a simple to use, fast and concise code. It can be imported in a Python script using the **spectrax** package, or run directly in the command line as `spectrax`. To install it, use

   ```sh
   pip install spectrax
   ```

Alternatively, you can install the Python dependencies `jax`, `jax_tqdm` and `matplotlib`, and run the [example script](example_script.py) in the repository after downloading it as

   ```sh
   git clone https://github.com/uwplasma/SPECTRAX
   python example_script.py
   ```

This allows SPECTRAX to be run without any installation.

The project can be downloaded in its [GitHub repository](https://github.com/uwplasma/SPECTRAX)
</code>

---

##  Features

SPECTRAX can run in CPUs, GPUs and TPUs, has autodifferentiation and just-in-time compilation capabilities, is based on rigorous testing, uses CI/CD via GitHub actions and has detailed documentation.

Currently, it evolves particles using the non-relativisic Lorentz force $\mathbf F = q (\mathbf E + \mathbf v \times \mathbf B)$, and evolves the electric $\mathbf E$ and magnetic $\mathbf B$ field using Maxwell's equations.

Plenty of examples are provided in the `examples` folder, and the documentation can be found in [Read the Docs](https://spectrax.readthedocs.io/).

---

##  Project Structure

```sh
└── SPECTRAX/
    ├── LICENSE
    ├── docs
    ├── examples
    │   ├── 1D_two-stream.py
    │   ├── 1D_landau_damping.py
    │   └── 2D_orszag_tang.py
    ├── spectrax
    │   ├── file1.py
    │   ├── file2.py
    │   └── file3.py
    └── tests
        └── test1.py
```

---
##  Getting Started

###  Prerequisites

- **Programming Language:** Python

Besides Python, SPECTRAX has minimum requirements. These are stated in [requirements.txt](requirements.txt), and consist of the Python libraries `jax`, `jax_tqdm` and `matplotlib`.

###  Installation

Install SPECTRAX using one of the following methods:

**Using PyPi:**

1. Install SPECTRAX from anywhere in the terminal:
```sh
pip install spectrax
```

**Build from source:**

1. Clone the SPECTRAX repository:
```sh
git clone https://github.com/uwplasma/SPECTRAX
```

2. Navigate to the project directory:
```sh
cd SPECTRAX
```

3. Install the project dependencies:

```sh
pip install -r /path/to/requirements.txt
```

4. Install SPECTRAX:

```sh
pip install -e .
```

###  Usage
To run a simple case of SPECTRAX, you can simply call `spectrax` from the terminal
```sh
spectrax
```

This runs SPECTRAX using standard input parameters of the two stream instability. To change input parameters, use a TOML file similar to the [example input](example_input.toml) present in the repository as

```sh
spectrax example_input.toml
```

Additionally, it can be run inside a script, as shown in the [example script](example_script.py) file
```sh
python example_script.py
```

There, you can find most of the input parameters needed to run many test cases, as well as resolution parameters.
The `spectrax` package has a single function `simulation()` that takes as arguments a dictionary input_parameters, the number of grid points, number of pseudoelectrons, total number of time steps, and the field solver to use.

In the [example script](example_script.py) file we write as inline comments the meaning of each input parameter.

###  Testing
Run the test suite using the following command:
```sh
pytest .
```

---
##  Project Roadmap

- [X] **`Task 1`**: <strike>Task 1.</strike>
- [ ] **`Task 2`**: Task 2.
- [ ] **`Task 3`**: Task 3.

---

##  Contributing

- **💬 [Join the Discussions](https://github.com/uwplasma/SPECTRAX/discussions)**: Share your insights, provide feedback, or ask questions.
- **🐛 [Report Issues](https://github.com/uwplasma/SPECTRAX/issues)**: Submit bugs found or log feature requests for the `SPECTRAX` project.
- **💡 [Submit Pull Requests](https://github.com/uwplasma/SPECTRAX/blob/main/CONTRIBUTING.md)**: Review open PRs, and submit your own PRs.

<details closed>
<summary>Contributing Guidelines</summary>

1. **Fork the Repository**: Start by forking the project repository to your github account.
2. **Clone Locally**: Clone the forked repository to your local machine using a git client.
   ```sh
   git clone https://github.com/uwplasma/SPECTRAX
   ```
3. **Create a New Branch**: Always work on a new branch, giving it a descriptive name.
   ```sh
   git checkout -b new-feature-x
   ```
4. **Make Your Changes**: Develop and test your changes locally.
5. **Commit Your Changes**: Commit with a clear message describing your updates.
   ```sh
   git commit -m 'Implemented new feature x.'
   ```
6. **Push to github**: Push the changes to your forked repository.
   ```sh
   git push origin new-feature-x
   ```
7. **Submit a Pull Request**: Create a PR against the original project repository. Clearly describe the changes and their motivations.
8. **Review**: Once your PR is reviewed and approved, it will be merged into the main branch. Congratulations on your contribution!
</details>

<details closed>
<summary>Contributor Graph</summary>
<br>
<p align="left">
   <a href="https://github.com{/uwplasma/SPECTRAX/}graphs/contributors">
      <img src="https://contrib.rocks/image?repo=uwplasma/SPECTRAX">
   </a>
</p>
</details>

---

##  License

This project is protected under the MIT License. For more details, refer to the [LICENSE](LICENSE) file.

---

##  Acknowledgments

- We acknowledge the help of the whole [UWPlasma](https://rogerio.physics.wisc.edu/) plasma group.

---
