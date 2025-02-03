# Running a Jupyter Notebook in a Virtual Environment (For Non-Technical Users)

## Introduction

If you have a Jupyter Notebook file that you need to run but are unsure about the technical setup, this guide will help. A virtual environment is an isolated space where you can install the necessary tools without affecting other programs on your computer.

### Why Use a Virtual Environment?
- Prevents conflicts with existing Python installations.
- Keeps your setup clean and organized.
- Ensures that required dependencies are installed correctly.

---

## Activating the Virtual Environment

Once a virtual environment has been created, you need to activate it before running Jupyter Notebook.

### **Windows**
```sh
my_env\Scripts\activate
```

### **macOS/Linux**
```sh
source my_env/bin/activate
```

Once activated, you will see `(my_env)` appear before your terminal prompt, indicating that you are inside the virtual environment.

---

## Running a Jupyter Notebook

With the virtual environment activated, you can now launch Jupyter Notebook:
```sh
jupyter notebook
```
This will open a browser window where you can navigate to and open your `.ipynb` file.

To run the code inside a cell, click inside it and press `Shift + Enter`.

---

## Deactivating the Virtual Environment

Once you are finished using Jupyter Notebook, you should deactivate the virtual environment to return to your normal system setup.

### **Deactivate the Virtual Environment**
```sh
deactivate
```
This ensures that your system environment is restored, preventing conflicts with other Python projects.

### **Alternative: Closing the Terminal**
Simply closing the terminal window will also deactivate the environment automatically.

---

## Extra Tips & Troubleshooting

- **How to check installed packages:** Run `pip list` to see what is installed inside the virtual environment.
- **Resolving common errors:** If `jupyter notebook` is not recognized, ensure the virtual environment is activated before running the command.
- **Saving dependencies:** If you need to save installed packages for future use, run:
  ```sh
  pip freeze > requirements.txt
  ```
  This will create a file listing all installed packages, which can be reinstalled later using `pip install -r requirements.txt`.

