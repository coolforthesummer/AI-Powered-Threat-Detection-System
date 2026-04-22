# File and Folder Guide

This file explains what each file and folder in this project is used for.


## File Purpose

### `README.md`

Use this file as the project entry point.

Purpose:



### `FILE_GUIDE.md`

Use this file as a quick reference for what each file and folder is for.

Purpose:


### `Documents/project_aim.md`

Use this file for the full project roadmap.

Purpose:



### `Documents/Phase 1/Phase1.md`

Use this file for Phase 1 planning and research details.

Purpose:



### `Documents/Phase 2/Phase2.md`

Use this file for Phase 2 data collection and preprocessing planning.

Purpose:


## Folders

As the project moves from documentation into implementation, these folders should be added.

### `data/raw/`


Purpose:

- stores the untouched source dataset,
- keeps original files separate from cleaned data.

Important:

- do not edit files in this folder,
- do not usually commit large raw dataset files to git.

### `data/processed/`

Use this folder for cleaned and transformed data.



### `data/samples/`

Use this folder for small sample files.


### `scripts/`

Use this folder for Python preprocessing or utility scripts.



Example files:

- `preprocess.py`
- `split_data.py`

### `notebooks/`

Use this folder for Jupyter notebooks.


### `docs/`

Use this folder for phase planning.


## Recommended Branch Usage

### `document` branch

Use this branch for writing and updating documentation files.



### `code` branch

Use this branch for implementation work.



## Overall

- planning phase goes in `docs/`,
- implementation goes in `code` branch,
- raw dataset goes in `data/raw/`,
- cleaned dataset goes in `data/processed/`,
- experiments go in `notebooks/`,
- reusable code goes in `scripts/`.
