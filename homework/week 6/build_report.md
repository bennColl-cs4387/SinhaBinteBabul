# LOG OF BUILDING SCIKIT-LEARN FROM SOURCE

I have been able to build the project from source by utilizing the [Installing the developement version of scikit-learn](https://scikit-learn.org/stable/developers/advanced_installation.html#compiler-windows). Initially, I encountered a few errors and had to restart the installation process several times. After troubleshooting online and trying different CLI guidelines, I realized partway through the process that the article was intended for use with 'cmd' or 'conda' only, while I had been using Git Bash. As a result, I had to modify some commands accordingly. This log doesn't contain the tests to be run on the modules of my choice. I will log it in a different markdown.

### Step 1: First, I cloned the scikit-learn repo to my local repo.
```bash
sinha@Sinha MINGW64 /c/repos/Building from source (Assignments)
$ git clone git@github.com:scikit-learn/scikit-learn.git
Cloning into 'scikit-learn'...
remote: Enumerating objects: 251415, done.
remote: Counting objects: 100% (321/321), done.
remote: Compressing objects: 100% (239/239), done.
remote: Total 251415 (delta 176), reused 166 (delta 82), pack-reused 251094 (from 1)
Receiving objects: 100% (251415/251415), 159.81 MiB | 4.67 MiB/s, done.
Resolving deltas: 100% (195355/195355), done.
Updating files: 100% (1600/1600), done.

sinha@Sinha MINGW64 /c/repos/Building from source (Assignments)
$ cd scikit-learn/
```


### Step 2: Next, since I already have Python 3.11 installed in my device, I tried creating a build/virtual environment and activating it. My understanding for this part is that it is essential to build the dependencies in venv to avoid disrupting other Python programs already installed on the system. Creating and activating this process failed initially.
```bash
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn (main)
$ python3 -m venv sklearn-env

sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn (main)
$ source sklearn-env/bin/activate
bash: sklearn-env/bin/activate: No such file or directory

sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn (main)
$ python3 -m venv sklearn-env
source sklearn-env/bin/activate
pip install wheel numpy scipy cython meson-python ninja
bash: sklearn-env/bin/activate: No such file or directory
Requirement already satisfied: wheel in c:\users\sinha\appdata\local\packages\pythonsoftwarefoundation.python.3.11_qbz5n2kfra8p0\localcache\local-packages\python311\site-packages (0.43.0)
Requirement already satisfied: numpy in c:\users\sinha\appdata\local\packages\pythonsoftwarefoundation.python.3.11_qbz5n2kfra8p0\localcache\local-packages\python311\site-packages (1.26.4)
Requirement already satisfied: scipy in c:\users\sinha\appdata\local\packages\pythonsoftwarefoundation.python.3.11_qbz5n2kfra8p0\localcache\local-packages\python311\site-packages (1.14.0)
Requirement already satisfied: cython in c:\users\sinha\appdata\local\packages\pythonsoftwarefoundation.python.3.11_qbz5n2kfra8p0\localcache\local-packages\python311\site-packages (3.0.11)
Requirement already satisfied: meson-python in c:\users\sinha\appdata\local\packages\pythonsoftwarefoundation.python.3.11_qbz5n2kfra8p0\localcache\local-packages\python311\site-packages (0.16.0)
Requirement already satisfied: ninja in c:\users\sinha\appdata\local\packages\pythonsoftwarefoundation.python.3.11_qbz5n2kfra8p0\localcache\local-packages\python311\site-packages (1.11.1.1)
Requirement already satisfied: meson>=0.63.3 in c:\users\sinha\appdata\local\packages\pythonsoftwarefoundation.python.3.11_qbz5n2kfra8p0\localcache\local-packages\python311\site-packages (from meson-python) (1.5.2)
Requirement already satisfied: packaging>=19.0 in c:\users\sinha\appdata\local\packages\pythonsoftwarefoundation.python.3.11_qbz5n2kfra8p0\localcache\local-packages\python311\site-packages (from meson-python) (23.2)
Requirement already satisfied: pyproject-metadata>=0.7.1 in c:\users\sinha\appdata\local\packages\pythonsoftwarefoundation.python.3.11_qbz5n2kfra8p0\localcache\local-packages\python311\site-packages (from meson-python) (0.8.0)
```

### Step 2 (continued): I referred to another article [Creating Virtual Environments](https://docs.python.org/3/tutorial/venv.html). First try, it failed. After that I realized since I am using Git Bash I have to use forward slash instead of backward slash. The commands in the article are for cmd. I was able to successfully activate the virtual environment.

```bash
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn (main)
$ tutorial-env\Scripts\activate
bash: tutorial-envScriptsactivate: command not found
```
```bash
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn (main)
$ source tutorial-env/Scripts/activate
(tutorial-env)
```

### Step 3: Installing the required dependencies
```
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env/Scripts (main)
$ pip install wheel numpy scipy cython meson-python ninja
```

Successfull installation
```
Collecting wheel
  Downloading wheel-0.44.0-py3-none-any.whl.metadata (2.3 kB)
Collecting numpy
  Downloading numpy-2.1.1-cp311-cp311-win_amd64.whl.metadata (59 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 59.7/59.7 kB 526.6 kB/s eta 0:00:00
Collecting scipy
  Downloading scipy-1.14.1-cp311-cp311-win_amd64.whl.metadata (60 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 60.8/60.8 kB 3.2 MB/s eta 0:00:00
Collecting cython
  Using cached Cython-3.0.11-cp311-cp311-win_amd64.whl.metadata (3.2 kB)
Collecting meson-python
  Using cached meson_python-0.16.0-py3-none-any.whl.metadata (4.1 kB)
Collecting ninja
  Using cached ninja-1.11.1.1-py2.py3-none-win_amd64.whl.metadata (5.4 kB)
Collecting meson>=0.63.3 (from meson-python)
  Using cached meson-1.5.2-py3-none-any.whl.metadata (1.8 kB)
Collecting packaging>=19.0 (from meson-python)
  Using cached packaging-24.1-py3-none-any.whl.metadata (3.2 kB)
Collecting pyproject-metadata>=0.7.1 (from meson-python)
  Using cached pyproject_metadata-0.8.0-py3-none-any.whl.metadata (3.0 kB)
Downloading wheel-0.44.0-py3-none-any.whl (67 kB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 67.1/67.1 kB ? eta 0:00:00
Downloading numpy-2.1.1-cp311-cp311-win_amd64.whl (12.9 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 12.9/12.9 MB 6.7 MB/s eta 0:00:00
Downloading scipy-1.14.1-cp311-cp311-win_amd64.whl (44.8 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 44.8/44.8 MB 5.1 MB/s eta 0:00:00
Using cached Cython-3.0.11-cp311-cp311-win_amd64.whl (2.8 MB)
Using cached meson_python-0.16.0-py3-none-any.whl (26 kB)
Using cached ninja-1.11.1.1-py2.py3-none-win_amd64.whl (312 kB)
Using cached meson-1.5.2-py3-none-any.whl (968 kB)
Using cached packaging-24.1-py3-none-any.whl (53 kB)
Using cached pyproject_metadata-0.8.0-py3-none-any.whl (7.5 kB)
Installing collected packages: ninja, wheel, packaging, numpy, meson, cython, scipy, pyproject-metadata, meson-python
Successfully installed cython-3.0.11 meson-1.5.2 meson-python-0.16.0 ninja-1.11.1.1 numpy-2.1.1 packaging-24.1 pyproject-metadata-0.8.0 scipy-1.14.1 wheel-0.44.0

[notice] A new release of pip is available: 24.0 -> 24.2
[notice] To update, run: python.exe -m pip install --upgrade pip
(tutorial-env)
```

### Step 4: It involved installing a compiler for my Windows system. According to the article, I downloaded Visual Studio Build Tools with Developement Enviroment for C++. It was a simple installation.


### Step 5: After the installation, I tried configuring the build environment but failed initially 

```
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env/Scripts (main)
$ SET DISTUTILS_USE_SDK=1
"C:\Program Files (x86)\Microsoft Visual Studio\2022\BuildTools\VC\Auxiliary\Build\vcvarsall.bat" x64
bash: SET: command not found
**********************************************************************
** Visual Studio 2022 Developer Command Prompt v17.11.4
** Copyright (c) 2022 Microsoft Corporation
**********************************************************************
[vcvarsall.bat] Environment initialized for: 'x64'
(tutorial-env)

sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env/Scripts (main)
$ pip install --editable . --verbose --no-build-isolation --config-settings editable-verbose=true
Using pip 24.0 from C:\repos\Building from source\scikit-learn\tutorial-env\Lib\site-packages\pip (python 3.11)
Obtaining file:///C:/repos/Building%20from%20source/scikit-learn/tutorial-env/Scripts
ERROR: file:///C:/repos/Building%20from%20source/scikit-learn/tutorial-env/Scripts does not appear to be a Python project: neither 'setup.py' nor 'pyproject.toml' found.

[notice] A new release of pip is available: 24.0 -> 24.2
[notice] To update, run: python.exe -m pip install --upgrade pip
(tutorial-env)
```

### Step 5 (continued): Since one of the errors said that 'bash command not found', I searched online to find the equivant to 'bash' for Git Bash CLI. Found out its 'export' in this case.
```
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env/Scripts (main)
$ export DISTUTILS_USE_SDK=1
(tutorial-env)
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env/Scripts (main)
$ "C:\Program Files (x86)\Microsoft Visual Studio\2022\BuildTools\VC\Auxiliary\Build\vcvarsall.bat" x64
**********************************************************************
** Visual Studio 2022 Developer Command Prompt v17.11.4
** Copyright (c) 2022 Microsoft Corporation
**********************************************************************
[vcvarsall.bat] Environment initialized for: 'x64'
(tutorial-env)
```

### Step 6: Finally, building the project with 'pip'. Initial try : FAILED
```bash
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env/Scripts (main)
$ pip install --editable . --verbose --no-build-isolation --config-settings editable-verbose=true
Using pip 24.0 from C:\repos\Building from source\scikit-learn\tutorial-env\Lib\site-packages\pip (python 3.11)
Obtaining file:///C:/repos/Building%20from%20source/scikit-learn/tutorial-env/Scripts
ERROR: file:///C:/repos/Building%20from%20source/scikit-learn/tutorial-env/Scripts does not appear to be a Python project: neither 'setup.py' nor 'pyproject.toml' found.
```

### Step 6 (continued): Since the error indicated that it couldn't find the 'setup.py' and 'pyproject.toml' files, I manually located them in the project folders and realized I needed to move two directories up to the scikit-learn directory, as I was still in the virtual environment directory. After navigating back to the correct location, I ran the build commands again, and it finally worked.
```
[notice] A new release of pip is available: 24.0 -> 24.2
[notice] To update, run: python.exe -m pip install --upgrade pip
(tutorial-env)
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env/Scripts (main)
$ cd ..
(tutorial-env)
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env (main)
$ cd ..
(tutorial-env)
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn (main)
$ pip install --editable . --verbose --no-build-isolation --config-settings editable-verbose=true
```

Next, the build process happens....
```
Using pip 24.0 from C:\repos\Building from source\scikit-learn\tutorial-env\Lib\site-packages\pip (python 3.11)
Obtaining file:///C:/repos/Building%20from%20source/scikit-learn
  Running command Checking if build backend supports build_editable
  Checking if build backend supports ....(continued)
```

### Step 7: Checking that the installed scikit-learn has a version number ending with .dev0:
```
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn (main)
$ python -c "import sklearn; sklearn.show_versions()"
```

More build happens...
```
meson-python: building scikit-learn: meson compile
Activating VS 17.11.4
INFO: automatically activated MSVC compiler environment
INFO: autodetecting backend as ninja
INFO: calculating backend command to run: "C:\repos\Building from source\scikit-learn\tutorial-env\Scripts\ninja.EXE"
[9/177] Compiling C++ object sklearn/utils/_vector_sentine...meson-generated_sklearn_utils__vector_sentinel.pyx.cpp.obj
.
.
.
.
sklearn/tree/_tree.cp311-win_amd64.pyd.p/sklearn/tree/_tree.pyx.cpp(55049): warning C4551: function call missing argument list
sklearn/tree/_tree.cp311-win_amd64.pyd.p/sklearn/tree/_tree.pyx.cpp(55964): warning C4551: function call missing argument list
[177/177] Linking target sklearn/tree/_tree.cp311-win_amd64.pyd
   Creating library sklearn\tree\_tree.cp311-win_amd64.lib and object sklearn\tree\_tree.cp311-win_amd64.exp

System:
    python: 3.11.9 (tags/v3.11.9:de54cf5, Apr  2 2024, 10:12:12) [MSC v.1938 64 bit (AMD64)]
executable: C:\repos\Building from source\scikit-learn\tutorial-env\Scripts\python.exe
   machine: Windows-10-10.0.22631-SP0

Python dependencies:
      sklearn: 1.6.dev0
          pip: 24.0
   setuptools: 65.5.0
        numpy: 2.1.1
        scipy: 1.14.1
       Cython: 3.0.11
       pandas: None
   matplotlib: None
       joblib: 1.4.2
threadpoolctl: 3.5.0

Built with OpenMP: True

threadpoolctl info:
       user_api: blas
   internal_api: openblas
    num_threads: 8
         prefix: libscipy_openblas
       filepath: C:\repos\Building from source\scikit-learn\tutorial-env\Lib\site-packages\numpy.libs\libscipy_openblas64_-c16e4918366c6bc1f1cd71e28ca36fc0.dll
        version: 0.3.27
threading_layer: pthreads
   architecture: SkylakeX

       user_api: blas
   internal_api: openblas
    num_threads: 8
         prefix: libscipy_openblas
       filepath: C:\repos\Building from source\scikit-learn\tutorial-env\Lib\site-packages\scipy.libs\libscipy_openblas-5b1ec8b915dfb81d11cebc0788069d2d.dll
        version: 0.3.27.dev
threading_layer: pthreads
   architecture: SkylakeX

       user_api: openmp
   internal_api: openmp
    num_threads: 8
         prefix: vcomp
       filepath: C:\Windows\System32\vcomp140.dll
        version: None
(tutorial-env)
```
The check confirmed that indeed the dev version was built. I deactivated the venv environment and decided to run tests on different modules later. So I will reactivate the virtual environment again when I do it.
