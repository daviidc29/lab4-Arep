# lab4-Arep - Embeddings Lab — Text Preprocessing & Token/Position Embeddings (Chapter 2, Build a Large Language Model (From Scratch))

## One Paragraph of project description goes here
This repository contains a runnable Jupyter notebook embeddings.ipynb that follows the Chapter 2 workflow from Sebastian Raschka’s Build a Large Language Model: loading a text corpus (the-verdict.txt), tokenizing it into IDs, building overlapping input/target training samples using max_length and stride, and creating token/positional embeddings with PyTorch. It also includes a small experiment that varies max_length and stride to show how overlap changes the number of samples and why overlapping windows help language models learn smoother context transitions

## Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes

### Prerequisites
What things you need to install the software and how to install them

- **Python 3.10+**
  - Check version:
    ```bash
    python --version
    ```
- **pip** 
  - Check pip:
    ```bash
    pip --version
    ```
- **Jupyter Notebook**
  - Install:
    ```bash
    pip install notebook
    ```
- **PyTorch**
  - Install:
    ```bash
    pip install torch
    ```
- **tiktoken** 
  - Install:
    ```bash
    pip install tiktoken
    ```

### Installing

- **Step 1 — Clone this repository**
  ```bash
  git clone https://github.com/daviidc29/lab4-Arep
  cd lab4-Arep
``

- **Step 2 — (Recommended) Create and activate a virtual environment**

  * Windows (PowerShell):

    ```bash
    python -m venv .venv
    .\.venv\Scripts\Activate.ps1
    ```
  * macOS / Linux:

    ```bash
    python3 -m venv .venv
    source .venv/bin/activate
    ```

* **Step 3 — Install dependencies**

  ```bash
  pip install --upgrade pip
  pip install notebook torch tiktoken
  ```


* **Step 4 — Verify required files are present**
  You should have:

  * embeddings.ipynb
  * the-verdict.txt

* **Step 5 — Run the notebook**

  ```bash
  jupyter notebook
  ```

  Then open embeddings.ipynb and run Kernel to Restart & Run All

![alt text](img/image.png)

![alt text](img/image-1.png)

* **Demo — Confirm the dataset windowing experiment works**
  In embeddings.ipynb, run the experiment cell that changes max_length and stride. You should see printed outputs like:

  * the number of generated samples for each configuration
  * a short explanation of why overlapping windows are useful

## Running the tests


This project does not include a formal automated test suite. The tests are the notebook’s end-to-end execution checks 


* **End-to-end notebook run**

  * What it tests: verifies text loading, tokenization, dataset window creation, DataLoader batching, and embedding generation all execute successfully
  * Why it matters: ensures the pipeline is reproducible and outputs are generated as expected for grading


```bash
jupyter notebook
```

Open embeddings.ipynb to Kernel to Restart & Run All to confirm no error cells.


No coding style tests are included because the deliverable is a single notebook intended for educational exploration


```bash
pip install black
black .
```

* **Local machine** (recommended for submission)
* **Google Colab / Kaggle Notebooks** (upload embeddings.ipynb and the-verdict.txt)
* **JupyterHub** (school/lab environment)

If using a hosted notebook environment, ensure both files are in the same working directory so the notebook can load the-verdict.txt

## Built With

Dropwizard - The web framework used
Maven - Dependency Management
ROME - Used to generate RSS Feeds

* **Python** — runtime
* **Jupyter Notebook** — notebook execution environment
* **PyTorch** — tensors, dataset utilities, and nn.Embedding
* **tiktoken (optional)** — tokenizer support (notebook includes a fallback)

## Versioning

We use SemVer for versioning. For the versions available, see the tags on this repository.

Version: 0.1.0 (educational notebook deliverable)

## Authors

Billie Thompson - Initial work - PurpleBooth
See also the list of contributors who participated in this project.

* David Santiago Catro — notebook implementation, explanations, and experiment (based on the book’s Chapter 2 workflow)

## License

This project is licensed under the MIT License 

## Acknowledgments

Hat tip to anyone whose code was used
Inspiration
etc

* Sebastian Raschka — *Build a Large Language Model (From Scratch)* (Chapter 2 workflow inspiration)
* The provided text corpus the-verdict.txt
* PyTorch community resources for embedding and dataset patterns


