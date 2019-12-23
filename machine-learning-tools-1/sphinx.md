# Sphinx

## Getting started with Sphinx 
- Install Sphinx :
    <code> pip install Sphinx </code>
- Create Project Documentation directory
mkdir $ProjectDirectory/docs
cd $ProjectDirectory/docs
    
- Setup Sphinx
    ```  sphinx-quickstart  ```
    >Separate source and build directories (y/n) [n]: y
    > Project name: My Project
    > Author name(s): Ganesh Kedari
    > Project release []: 0.1
    > Project language [en]: en

    Check the responce in Console 
    ```
    Creating file .\source\conf.py.
    Creating file .\source\index.rst.
    Creating file .\Makefile.
    Creating file .\make.bat.
    Finished: An initial directory structure has been created.
    ```

- Edit conf.py    
Configure path to root directory
```
    import os
    import sys
    sys.path.insert(0, os.path.abspath('../..'))
```

- Open the index.rst and change the content
- make html
- Documenation will be generated in $ProjectDirectory/docs/build directory
