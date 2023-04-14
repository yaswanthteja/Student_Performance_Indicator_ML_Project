## End To End Ml Project : Student Perfomance Index 

This is a end to end machine learning project which predicts the student performance index based on the given data.


### End To End #ml #project With Deployment-PART 1
GitHub And Code Set Up


Prerequisites:
1. #pythonprogramming
2. #modular #programming
3. #machinelearning
4. #deeplearning
5. #githubactions



Step1 :

- setup the github repository
  - creating new virtual environment
  - setup.py
  - requirements.txt
- Src folder and bulid the package


1. Create a GitHub Repository 'ml project'

2. Create a local repository 'ml project' and open it in code editor like VS Code

3. Create  virtual environment  by using this 

conda create -p venv python==3.8 -y

and Activate an environment 'venv' 
by using 

conda activate venv/

4. Create a 'README.md' file in 'ml project' folder

5. Sync the GitHub and Local Repositories and push the code to GitHub Repo using #githubactions .

6. Create '.gitignore' file in #python in GitHub directly with Python template.

7. Git Pull to make sure code is in sync between GitHub Repo and Base Repo

8. Create 'setup.py' file in 'ml project' folder. With the setup.py we will be able to build our entire machine learning application as a package and even deploy.
add this to setup.py

```
from setuptools import find_packages,setup
from typing import List

HYPEN_E_DOT='-e .'
def get_requirements(file_path:str)->List[str]:
    '''
    this function will return the list of requirements
    '''
    requirements=[]
    with open(file_path) as file_obj:
        requirements=file_obj.readlines()
        requirements=[req.replace("\n","") for req in requirements]

        if HYPEN_E_DOT in requirements:
            requirements.remove(HYPEN_E_DOT)
    
    return requirements

setup(
name='Student_Performance_Index',
version='0.0.1',
author='Yaswanth Teja',
author_email='yaswanthteja02@gmail.com',
packages=find_packages(),
install_requires=get_requirements('requirements.txt')

)
```
9. Create 'requirements.txt' file and add required libraries after that add -e . at last in the requirements.txt

10. Create 'src' folder in 'ml project' folder
in that src folder create a  __init__.py file

11. In terminal, execute the following
  pip install -r requirements.txt

12. 'mlproject.egg-info' indicated that your package is getting installed.

13. push all the files to #github .



## Files in "ml project" folders:
```
1. mlproject.egg-info                            --automatically created this file structure 
     |-dependency_links.txt
     |-PKG-INFO
     |-requires.txt
     |-SOURCES.txt
     |-top_level.txt

2. src 
     |- __init__.py
3. venv
4. .gitignore
6. README.md
7. requirements.txt
8. setup.py
```
