# Setting Up an Old Python Virtual Environment on Linux & Jupyter Notebook

## Overview

This guide provides step-by-step instructions for installing an older version of Python (Python 3.8), setting up a virtual environment on a Linux system, and installing Jupyter Notebook.

## How to Install a Specific Python Version

### 1. Add the Deadsnakes PPA Repository

The Deadsnakes PPA provides older versions of Python for Ubuntu-based systems.

```sh
sudo add-apt-repository ppa:deadsnakes/ppa -y
```

### 2. Update Package Lists

Run the following commands to update your system's package lists:

```sh
sudo apt-get update
sudo apt update
```

### 3. Install Python 3.8 and Required Packages

Use the following command to install Python 3.8 along with `venv` and `distutils`:

```sh
sudo apt install python3.8 python3.8-venv python3.8-distutils -y
```

### 4. Verify Python Installation

Check if Python 3.8 is installed correctly by running:

```sh
python3.8 --version
```

Expected output:

```
Python 3.8.X
```

## How to Create a Virtual Environment

### 1. Create a Directory for Python 3.8 Projects

```sh
mkdir python3.8 && cd python3.8
```

### 2. Create a Virtual Environment

To create a virtual environment using Python 3.8, run:

```sh
python3.8 -m venv myenv
```

Replace `myenv` with your preferred environment name.

## How to Activate and Deactivate the Virtual Environment

### 1. Activate the Virtual Environment

To activate the virtual environment, use:

```sh
source myenv/bin/activate
```

Your terminal prompt should now show `(myenv)`, indicating that the virtual environment is active.

### 2. Check the Active Python Version

To check which Python version is currently being used:

```sh
python --version
```

### 3. Deactivate the Virtual Environment

To exit the virtual environment, simply run:

```sh
deactivate
```

## How to Install Jupyter Notebook

### 1. Install Jupyter Notebook

To install Jupyter Notebook, run the following command:

```sh
sudo pip install -U jupyter-book
```

### 2. Build a Jupyter Book

After installation, you can build a Jupyter Book using:

```sh
jupyter-book build [filepath]
```

Replace `[filepath]` with the directory or file path of your Jupyter Book.

## Troubleshooting

- If `python3.8` is not found, ensure the installation was successful by running:

  ```sh
  which python3.8
  ```

- If the `venv` module is missing, reinstall it using:

  ```sh
  sudo apt install python3.8-venv -y
  ```

- To check the active Python version at any time, use:

  ```sh
  python --version
  ```

## Conclusion

By following these steps, you can install an older version of Python, create a virtual environment, and set up Jupyter Notebook for your development needs on a Linux system.

