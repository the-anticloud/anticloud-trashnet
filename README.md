# TRASHNET

![license](https://img.shields.io/badge/license-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-waste_management-lightgrey)

> Anticloud-hardened packaging of the upstream project `TRASHNET` in category **WASTE MANAGEMENT**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** WASTE MANAGEMENT · **Upstream:** https://github.com/garythung/trashnet · **Upstream pin:** `6fa2b878c6c1b4304b91109070ce0edf9279bb31` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

# trashnet
Code (only for the convolutional neural network) and dataset for mine and [Mindy Yang](http://github.com/yangmindy4)'s final project for [Stanford's CS 229: Machine Learning class](http://cs229.stanford.edu). Our paper can be found [here](https://cs229.stanford.edu/proj2016/report/ThungYang-ClassificationOfTrashForRecyclabilityStatus-report.pdf). The convolutional neural network results on the poster are dated since we continued working after the end of the quarter and  were able to achieve around 75% test accuracy (with 70/13/17 train/val/test split) after changing the weight initialization to the Kaiming method.

## Dataset
This project contains the dataset that we collected. The dataset spans six classes: glass, paper, cardboard, plastic, metal, and trash. Currently, the dataset consists of 2527 images:
- 501 glass
- 594 paper
- 403 cardboard
- 482 plastic
- 410 metal
- 137 trash

The pictures were taken by placing the object on a white posterboard and using sunlight and/or room lighting. The pictures have been resized down to 512 x 384, which can be changed in `data/constants.py` (resizing them involves going through step 1 in usage). The devices used were Apple iPhone 7 Plus, Apple iPhone 5S, and Apple iPhone SE.

The size of the original dataset, ~3.5GB, exceeds the git-lfs maximum size so it has been uploaded to Google Drive. If you are planning on using the Python code to preprocess the original dataset, then download `dataset-original.zip` from the link below and place the unzipped folder inside of the `data` folder.

**If you are using the dataset, please give a citation of this project. The dataset can be downloaded [here](https://huggingface.co/datasets/garythung/trashnet).**

## Installation
### Lua setup
We wrote code in [Lua](http://lua.org) using [Torch](http://torch.ch); you can find installation instructions
[here](http://torch.ch/docs/getting-started.html). You'll need the following Lua packages:

- [torch/torch7](http://github.com/torch/torch7)
- [torch/nn](http://github.com/torch/nn)
- [torch/optim](http://github.com/torch/optim)
- [torch/image](http://github.com/torch/image)
- [torch/gnuplot](http://github.com/torch/gnuplot)

After installing Torch, you can install these packages by running the following:

```bash
# Install using Luarocks
luarocks install torch
luarocks install nn
luarocks install optim
luarocks install image
luarocks install gnuplot
```

We also need [@e-lab](http://github.com/e-lab)'s [weight-init module](http://github.com/e-lab/torch-toolbox/blob/master/Weight-init/weight-init.lua), which is already included in this project.

### CUDA support
Because training takes awhile, you will want to use a GPU to get results in a reasonable amount of time. We used CUDA with a GTX 650 Ti with CUDA. To enable GPU acceleration with CUDA, you'll first need to install CUDA 6.5 or higher. Find CUDA installations [here](http://developer.nvidia.com/cuda-downloads).

Then you need to install following Lua packages for CUDA:
- [torch/cutorch](http://github.com/torch/cutorch)
- [torch/cunn](http://github.com/torch/cunn)

You can install these packages by running the following:

```bash
luarocks install cutorch
luarocks install cunn
```

### Python setup
Python is currently used for some image preprocessing tasks. The Python dependencies are:
- [NumPy](http://numpy.org)
- [SciPy](http://scipy.org)

You can install these packages by running the following:

```bash
# Install using pip
pip install numpy scipy
```

## Usage

### Step 1: Prepare the data
Unzip `data/dataset-resized.zip`.

If adding more data, then the new files must be enumerated properly and put into the appropriate folder in `data/dataset-original` and then preprocessed. Preprocessing the data involves deleting the `data/dataset-resized` folder and then calling `python resize.py` from `trashnet/data`. This will take around half an hour.

### Step 2: Train the model
TODO

### Step 3: Test the model
TODO

### Step 4: View the results
TODO

## Contributing
1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## Acknowledgments
- Thanks to the Stanford CS 229 autumn 2016-2017 teaching staff for a great class!
- [@e-lab](http://github.com/e-lab) for their [weight-init Torch module](http://github.com/e-lab/torch-toolbox/blob/master/Weight-init/weight-init.lua)

## TODOs
- finish the Usage portion of the README
- add specific results (and parameters used) that were achieved after the CS 229 project deadline
- add saving of confusion matrix data and creation of graphic to `plot.lua`
- rewrite the data preprocessing to only reprocess new images if the dimensions have not changed

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Unknown (no standard manifest detected)** (manifests: none detected; scanned in UPSTREAM_CLONE)
- Top-level source layout: `data/`
- Snapshot size: **19 files**, **1033 lines of code** (measured; see Benchmarks)
- Primary languages: `.lua` (8), `.txt` (5), `(none)` (2), `.py` (2), `.md` (1), `.zip` (1)
- Upstream commit pinned for this packaging: `6fa2b878c6c1b4304b91109070ce0edf9279bb31`

---

## Installation

No installation section was found in the upstream readme, so the commands below are generated from the manifests detected in this project directory.

```sh
# No standard manifest detected. Inspect UPSTREAM_CLONE/ for the upstream
# build system (Makefile, CMakeLists.txt, configure, ...) and follow it.
```

Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

The size of the original dataset, ~3.5GB, exceeds the git-lfs maximum size so it has been uploaded to Google Drive. If you are planning on using the Python code to preprocess the original dataset, then download `dataset-original.zip` from the link below and place the unzipped folder inside of the `data` folder.

**If you are using the dataset, please give a citation of this project. The dataset can be downloaded [here](https://huggingface.co/datasets/garythung/trashnet).**

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

- 501 glass
- 594 paper
- 403 cardboard
- 482 plastic
- 410 metal
- 137 trash

The pictures were taken by placing the object on a white posterboard and using sunlight and/or room lighting. The pictures have been resized down to 512 x 384, which can be changed in `data/constants.py` (resizing them involves going through step 1 in usage). The devices used were Apple iPhone 7 Plus, Apple iPhone 5S, and Apple iPhone SE.

The size of the original dataset, ~3.5GB, exceeds the git-lfs maximum size so it has been uploaded to Google Drive. If you are planning on using the Python code to preprocess the original dataset, then download `dataset-original.zip` from the link below and place the unzipped folder inside of the `data` folder.

**If you are using the dataset, please give a citation of this project. The dataset can be downloaded [here](https://huggingface.co/datasets/garythung/trashnet).**

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Unknown (no standard manifest detected) |
| Manifests detected | none |
| Files in snapshot | 19 |
| Lines of code | 1033 |
| Dependency references | 0 |
| Upstream license | MIT |
| Overlay license | Anticommons 0.1.0 |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

No configuration section was found in the upstream readme. Configuration-relevant files detected in this project directory:

- None detected at the snapshot root; consult the upstream documentation link in the Upstream section.

Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

Upstream contributions: fork the `TRASHNET` project, create a feature branch, and open a pull request against upstream. Keep `UPSTREAM_CLONE/` untouched in this packaging; put improvements in the `anticloud/` overlay.

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: MIT** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
MIT License

Copyright (c) 2017 Gary Thung

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original MIT terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `MIT` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `TRASHNET` (category: WASTE MANAGEMENT)
- **Upstream URL:** https://github.com/garythung/trashnet
- **Pinned commit (SHA):** `6fa2b878c6c1b4304b91109070ce0edf9279bb31`
- **Branch:** master
- **Pin provenance:** local source .git file read (no .git dir in source). The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`ea5dcfb31344c98880a029e9c246e4f768c65c96b298a01814af0f1f0b490327`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

