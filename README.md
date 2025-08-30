# Basic Skills

This repository focuses on basic skills required for scientific research, including script writing, basic usage of GitHub, and Linux Powershell commands for server usage.

## Table of Contents
- [Basic Skills](#basic-skills)
  - [Script Writing](#script-writing)
  - [Github Usage](#github-usage)
  - [Linux Powershell](#linux-powershell)
  - [VPN](#vpn)
  - [Pytorch](#pytorch)
  - [Paper Reading](#paper-reading)

---

## Script Writing

Scripts are mainly used for processing data, including convert data into a specific format, add or change a key for every element in the json file. In brief, scripts can automatically complete large volumes of repetitive tasks. Here I mainly introduce two python libraries: `os` and `json`. Examples of script code are in `Script` folder.

`os` allows interaction with the operating system, such as file management.  
```python
os.listdir(".")  # list files in the current directory
```

```python
with open (json_path, 'r', encoding='utf-8') as f: # open the json file in read mode with utf-8
    data = json.load(f) # load and parse the json content into a Python dictionary(or list)
```

```python
with open (json_path, 'w', encoding='utf-8') as f: # open the json file in writing mode with utf-8
    json.dump(content, file_path, indent=4) # write content into file
```

---

## Github Usage
Suppose I have a folder required to upload to github repository, here is a complete process.
1. Open the terminal and enter the local folder
```bash
cd path/my_project
```

2. If the folder is not a github repository, initialize it
```bash
git init
```

3. Add remote repository address
```bash
git remote add origin https://github.com/username/repo.git
```

4. Add all files in the folder
```bash
git add .
```

5. Submit code with a comment
```bash
git commit -m "comment"
```

6. Check and create new branch
```bash
git checkout -b <name>
git branch -M <name>
```

7. Push code
```bash
git push -u origin branch
```

8. Update before push
```bash
git pull origin main --rebase
```

---

## Linux Powershell
The following are some basic commands.
### Folder
Enter a folder
```bash
cd \path
```

Return to the previous folder
```bash
cd ..
```

List all files in current folder
```bash
ls
```

Send a folder from one remote server to another
```bash
rsync -avzP -e "ssh -p port" /path/to/original/file username@ip:/path/to/new/address
```

Send a folder from windows local to a linux server
```cmd
scp -P port -r /path/to/local/file username@ip:/path/to/new/address
```

### Environment Creation
Create a new environment
```bash
conda create -n name python=
```

Activate an environment
```bash
conda activate name
```

Deactivate current environment
```bash
conda deactivate
```

Remove an environment
```bash
conda env remove -n name
```

List all environments
```bash
conda env list
```

Install all need libraries in `requirements.txt`
```bash
pip install -r requirements.txt
```

Generate `requirements.txt`
```bash
pipreqs ./ --encoding=utf-8 --force
```

Get entire environment
```bash
pip freeze > requirements_full.txt
```

### GPU Usage
Monitor the usage of GPU
```bash
pip install gpustat
gpustat
```

Specify the GPU
```bash
export CUDA_VISIBLE_DEVICES=0, 1
```

## VPN
Allocate port
```bash
proxy
```

Open another terminal and run the command
```bash
clash
```

## Pytorch
`pytorch.ipynb` is based on official documentation and some video tutorials. The dataset used can be downloaded from `https://download.pytorch.org/tutorial/hymenoptera_data.zip`

## Paper Reading
`paper` folder contains papers and notes read during summer practice.
