# EM Python

Jupyter notebooks for learning electromagnetism using Python.

## Prerequisites

Install Python, pip, and Jupyter before setting up the project.

### Windows

1. Download and install Python from [python.org](https://www.python.org/downloads/) — make sure to check **"Add Python to PATH"** during setup.
2. pip is bundled with Python. Verify with:
   ```powershell
   python --version
   pip --version
   ```
3. Install Jupyter:
   ```powershell
   pip install jupyter jupyterlab
   ```

### Arch Linux

```bash
sudo pacman -S python python-pip
pip install jupyterlab
```

Or install Jupyter system-wide:
```bash
sudo pacman -S jupyter-notebook
```

## Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Parven05/EM-Python
cd EM-Python
```

### 2. Create a Virtual Environment and Install Dependencies

**Linux / macOS**
```bash
python -m venv .venv
source .venv/bin/activate
which python
pip install vpython ipykernel setuptools
python -m ipykernel install --user --name=EMT_env --display-name "Python (EMT)"
```

**Windows**
```powershell
python -m venv .venv
.venv\Scripts\activate
where python
pip install vpython ipykernel setuptools
python -m ipykernel install --user --name=EMT_env --display-name "Python (EMT)"
```

### 3. Verify the Setup

```bash
jupyter kernelspec list
```

**Linux / macOS** — expected output:
```
Available kernels:
  python3    /home/user/dev/EM-Python/.venv/share/jupyter/kernels/python3
  emt_env    /home/user/.local/share/jupyter/kernels/emt_env
```

**Windows** — expected output:
```
Available kernels:
  python3    C:\Users\user\dev\EM-Python\.venv\share\jupyter\kernels\python3
  emt_env    C:\Users\user\AppData\Roaming\jupyter\kernels\emt_env
```

## Usage

```bash
jupyter-lab
```

<img width="1679" height="1062" alt="jupyter" src="https://github.com/user-attachments/assets/4f4ee901-444b-4796-8f2d-bce4907442ec" />
Select the kernel named **Python (EMT)**, and start coding.

## Troubleshooting

If something goes wrong, remove the kernel and virtual environment, then redo the setup steps.

**Linux / macOS**
```bash
jupyter kernelspec uninstall emt_env
rm -rf .venv
```

**Windows**
```powershell
jupyter kernelspec uninstall emt_env
Remove-Item -Recurse -Force .venv
```
