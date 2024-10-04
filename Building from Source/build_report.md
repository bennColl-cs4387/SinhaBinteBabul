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
$ ls
scikit-learn/

sinha@Sinha MINGW64 /c/repos/Building from source (Assignments)
$ cd scikit-learn/

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

sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn (main)
$ python -m venv tutorial-env

sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn (main)
$ tutorial-env\Scripts\activate
bash: tutorial-envScriptsactivate: command not found

sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn (main)
$ source tutorial-env/Scripts/activate
(tutorial-env)
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn (main)
$ ls
asv_benchmarks/      build_tools/        CONTRIBUTING.md  examples/     meson.build     SECURITY.md  sklearn-env/
azure-pipelines.yml  CITATION.cff        COPYING          maint_tools/  pyproject.toml  setup.cfg    tutorial-env/
benchmarks/          CODE_OF_CONDUCT.md  doc/             Makefile      README.rst      sklearn/
(tutorial-env)
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn (main)
$ cd tutorial-env/
(tutorial-env)
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env (main)
$ ls
Include/  Lib/  pyvenv.cfg  Scripts/
(tutorial-env)
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env (main)
$ source tutorial-env/Scripts/activate
bash: tutorial-env/Scripts/activate: No such file or directory
(tutorial-env)
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env (main)
$ cd Scripts/
(tutorial-env)
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env/Scripts (main)
$ ls
activate  activate.bat  Activate.ps1  deactivate.bat  pip.exe*  pip3.11.exe*  pip3.exe*  python.exe*  pythonw.exe*
(tutorial-env)
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env/Scripts (main)
$ source activate
(tutorial-env)
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env/Scripts (main)
$ ls
activate  activate.bat  Activate.ps1  deactivate.bat  pip.exe*  pip3.11.exe*  pip3.exe*  python.exe*  pythonw.exe*
(tutorial-env)
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env/Scripts (main)
$ pip install wheel numpy scipy cython meson-python ninja
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
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env/Scripts (main)
$ SET DISTUTILS_USE_SDK=1
bash: SET: command not found
(tutorial-env)
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
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn/tutorial-env/Scripts (main)
$ pip install --editable . --verbose --no-build-isolation --config-settings editable-verbose=true
Using pip 24.0 from C:\repos\Building from source\scikit-learn\tutorial-env\Lib\site-packages\pip (python 3.11)
Obtaining file:///C:/repos/Building%20from%20source/scikit-learn/tutorial-env/Scripts
ERROR: file:///C:/repos/Building%20from%20source/scikit-learn/tutorial-env/Scripts does not appear to be a Python project: neither 'setup.py' nor 'pyproject.toml' found.

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
Using pip 24.0 from C:\repos\Building from source\scikit-learn\tutorial-env\Lib\site-packages\pip (python 3.11)
Obtaining file:///C:/repos/Building%20from%20source/scikit-learn
  Running command Checking if build backend supports build_editable
  Checking if build backend supports build_editable ... done
  Running command Preparing editable metadata (pyproject.toml)
  + meson setup C:\repos\Building from source\scikit-learn C:\repos\Building from source\scikit-learn\build\cp311 -Dbuildtype=release -Db_ndebug=if-release -Db_vscrt=md --native-file=C:\repos\Building from source\scikit-learn\build\cp311\meson-python-native-file.ini
  The Meson build system
  Version: 1.5.2
  Source dir: C:\repos\Building from source\scikit-learn
  Build dir: C:\repos\Building from source\scikit-learn\build\cp311
  Build type: native build
  Project name: scikit-learn
  Project version: 1.6.dev0
  Activating VS 17.11.4
  C compiler for the host machine: cl (msvc 19.41.34120 "Microsoft (R) C/C++ Optimizing Compiler Version 19.41.34120 for x64")
  C linker for the host machine: link link 14.41.34120.0
  C++ compiler for the host machine: cl (msvc 19.41.34120 "Microsoft (R) C/C++ Optimizing Compiler Version 19.41.34120 for x64")
  C++ linker for the host machine: link link 14.41.34120.0
  Cython compiler for the host machine: cython (cython 3.0.11)
  Host machine cpu family: x86_64
  Host machine cpu: x86_64
  Compiler for C supports arguments -Wno-unused-but-set-variable: NO
  Compiler for C supports arguments -Wno-unused-function: NO
  Compiler for C supports arguments -Wno-conversion: NO
  Compiler for C supports arguments -Wno-misleading-indentation: NO
  Library m found: NO
  Program python found: YES (C:\repos\Building from source\scikit-learn\tutorial-env\Scripts\python.exe)
  Run-time dependency OpenMP for c found: YES 2.0
  Run-time dependency python found: YES 3.11
  Build targets in project: 111

  scikit-learn 1.6.dev0

    User defined options
      Native files: C:\repos\Building from source\scikit-learn\build\cp311\meson-python-native-file.ini
      buildtype   : release
      b_ndebug    : if-release
      b_vscrt     : md

  Found ninja.EXE-1.11.1.git.kitware.jobserver-1 at "C:\repos\Building from source\scikit-learn\tutorial-env\Scripts\ninja.EXE"
  + meson compile
  [1/251] Generating sklearn/write_built_with_meson_file with a custom command
  [2/251] Copying file sklearn/__init__.py
  [3/251] Copying file sklearn/utils/__init__.py
  [4/251] Copying file sklearn/_loss/_loss.pxd
  [5/251] Copying file sklearn/utils/_openmp_helpers.pxd
  [6/251] Copying file sklearn/utils/_cython_blas.pxd
  [7/251] Copying file sklearn/utils/_heap.pxd
  [8/251] Copying file sklearn/utils/_random.pxd
  [9/251] Generating sklearn/_loss/_loss_pyx with a custom command
  [10/251] Generating sklearn/utils/_seq_dataset_pxd with a custom command
  [11/251] Generating sklearn/utils/_weight_vector_pxd with a custom command
  [12/251] Generating sklearn/metrics/_dist_metrics_pxd with a custom command
  [13/251] Copying file sklearn/utils/_sorting.pxd
  [14/251] Copying file sklearn/utils/_vector_sentinel.pxd
  [15/251] Copying file sklearn/utils/_typedefs.pxd
  [16/251] Copying file sklearn/metrics/__init__.py
  [17/251] Generating sklearn/metrics/_pairwise_distances_reduction/_datasets_pair_pxd with a custom command
  [18/251] Generating sklearn/metrics/_pairwise_distances_reduction/_base_pxd with a custom command
  [19/251] Generating sklearn/metrics/_pairwise_distances_reduction/_middle_term_computer_pxd with a custom command
  [20/251] Copying file sklearn/metrics/_pairwise_distances_reduction/_classmode.pxd
  [21/251] Copying file sklearn/metrics/_pairwise_distances_reduction/__init__.py
  [22/251] Compiling C++ object sklearn/utils/murmurhash.cp311-win_amd64.pyd.p/src_MurmurHash3.cpp.obj
  [23/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/__check_build/_check_build.pyx"
  [24/251] Compiling C object sklearn/__check_build/_check_build.cp311-win_amd64.pyd.p/meson-generated_sklearn___check_build__check_build.pyx.c.obj
  [25/251] Linking target sklearn/__check_build/_check_build.cp311-win_amd64.pyd
     Creating library sklearn\__check_build\_check_build.cp311-win_amd64.lib and object sklearn\__check_build\_check_build.cp311-win_amd64.exp

  [26/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/_isotonic.pyx"
  [27/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/utils/_openmp_helpers.pyx"
  [28/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/utils/murmurhash.pyx"
  [29/251] Compiling C object sklearn/utils/_openmp_helpers.cp311-win_amd64.pyd.p/meson-generated_sklearn_utils__openmp_helpers.pyx.c.obj
  [30/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/utils/_fast_dict.pyx"
  [31/251] Linking target sklearn/utils/_openmp_helpers.cp311-win_amd64.pyd
     Creating library sklearn\utils\_openmp_helpers.cp311-win_amd64.lib and object sklearn\utils\_openmp_helpers.cp311-win_amd64.exp

  [32/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/utils/arrayfuncs.pyx"
  [33/251] Compiling C object sklearn/_isotonic.cp311-win_amd64.pyd.p/meson-generated_sklearn__isotonic.pyx.c.obj
  [34/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/utils/_cython_blas.pyx"
  [35/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/utils/_random.pyx"
  [36/251] Linking target sklearn/_isotonic.cp311-win_amd64.pyd
     Creating library sklearn\_isotonic.cp311-win_amd64.lib and object sklearn\_isotonic.cp311-win_amd64.exp
  [37/251] Compiling C object sklearn/utils/murmurhash.cp311-win_amd64.pyd.p/meson-generated_sklearn_utils_murmurhash.pyx.c.obj
  ..\..\sklearn\utils\src/MurmurHash3.h(16): warning C4142: 'uint32_t': benign redefinition of type
  C:\Program Files (x86)\Microsoft Visual Studio\2022\BuildTools\VC\Tools\MSVC\14.41.34120\include\stdint.h(24): note: see declaration of 'uint32_t'
  [38/251] Linking target sklearn/utils/murmurhash.cp311-win_amd64.pyd
     Creating library sklearn\utils\murmurhash.cp311-win_amd64.lib and object sklearn\utils\murmurhash.cp311-win_amd64.exp

  [39/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/utils/sparsefuncs_fast.pyx"
  [40/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/utils/_typedefs.pyx"
  [41/251] Compiling C object sklearn/utils/arrayfuncs.cp311-win_amd64.pyd.p/meson-generated_sklearn_utils_arrayfuncs.pyx.c.obj
  [42/251] Linking target sklearn/utils/arrayfuncs.cp311-win_amd64.pyd
     Creating library sklearn\utils\arrayfuncs.cp311-win_amd64.lib and object sklearn\utils\arrayfuncs.cp311-win_amd64.exp
  [43/251] Compiling C++ object sklearn/utils/_fast_dict.cp311-win_amd64.pyd.p/meson-generated_sklearn_utils__fast_dict.pyx.cpp.obj
  sklearn/utils/_fast_dict.cp311-win_amd64.pyd.p/sklearn/utils/_fast_dict.pyx.cpp(26950): warning C4551: function call missing argument list
  [44/251] Linking target sklearn/utils/_fast_dict.cp311-win_amd64.pyd
     Creating library sklearn\utils\_fast_dict.cp311-win_amd64.lib and object sklearn\utils\_fast_dict.cp311-win_amd64.exp

  [45/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/utils/_heap.pyx"
  [46/251] Compiling C object sklearn/utils/_random.cp311-win_amd64.pyd.p/meson-generated_sklearn_utils__random.pyx.c.obj
  [47/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/utils/_sorting.pyx"
  [48/251] Linking target sklearn/utils/_random.cp311-win_amd64.pyd
     Creating library sklearn\utils\_random.cp311-win_amd64.lib and object sklearn\utils\_random.cp311-win_amd64.exp
  [49/251] Compiling C object sklearn/utils/_heap.cp311-win_amd64.pyd.p/meson-generated_sklearn_utils__heap.pyx.c.obj
  [50/251] Linking target sklearn/utils/_heap.cp311-win_amd64.pyd
     Creating library sklearn\utils\_heap.cp311-win_amd64.lib and object sklearn\utils\_heap.cp311-win_amd64.exp
  [51/251] Compiling C object sklearn/utils/_typedefs.cp311-win_amd64.pyd.p/meson-generated_sklearn_utils__typedefs.pyx.c.obj
  [52/251] Compiling C object sklearn/utils/_sorting.cp311-win_amd64.pyd.p/meson-generated_sklearn_utils__sorting.pyx.c.obj
  [53/251] Generating sklearn/utils/_seq_dataset_pyx with a custom command
  [54/251] Linking target sklearn/utils/_typedefs.cp311-win_amd64.pyd
     Creating library sklearn\utils\_typedefs.cp311-win_amd64.lib and object sklearn\utils\_typedefs.cp311-win_amd64.exp

  [55/251] Linking target sklearn/utils/_sorting.cp311-win_amd64.pyd
     Creating library sklearn\utils\_sorting.cp311-win_amd64.lib and object sklearn\utils\_sorting.cp311-win_amd64.exp

  [56/251] Generating sklearn/metrics/_dist_metrics_pyx with a custom command
  [57/251] Generating sklearn/utils/_weight_vector_pyx with a custom command
  [58/251] Generating sklearn/metrics/_pairwise_distances_reduction/_datasets_pair_pyx with a custom command
  [59/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/utils/_vector_sentinel.pyx"
  [60/251] Compiling C object sklearn/utils/_cython_blas.cp311-win_amd64.pyd.p/meson-generated_sklearn_utils__cython_blas.pyx.c.obj
  [61/251] Linking target sklearn/utils/_cython_blas.cp311-win_amd64.pyd
     Creating library sklearn\utils\_cython_blas.cp311-win_amd64.lib and object sklearn\utils\_cython_blas.cp311-win_amd64.exp

  [62/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/utils/_isfinite.pyx"
  [63/251] Compiling C++ object sklearn/utils/_vector_sentinel.cp311-win_amd64.pyd.p/meson-generated_sklearn_utils__vector_sentinel.pyx.cpp.obj
  sklearn/utils/_vector_sentinel.cp311-win_amd64.pyd.p/sklearn/utils/_vector_sentinel.pyx.cpp(15416): warning C4551: function call missing argument list
  [64/251] Generating sklearn/metrics/_pairwise_distances_reduction/_base_pyx with a custom command
  [65/251] Linking target sklearn/utils/_vector_sentinel.cp311-win_amd64.pyd
     Creating library sklearn\utils\_vector_sentinel.cp311-win_amd64.lib and object sklearn\utils\_vector_sentinel.cp311-win_amd64.exp

  [66/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/metrics/_pairwise_fast.pyx"
  [67/251] Generating sklearn/metrics/_pairwise_distances_reduction/_middle_term_computer_pyx with a custom command
  [68/251] Compiling Cython source sklearn/utils/_seq_dataset.pyx
  [69/251] Compiling C object sklearn/utils/_isfinite.cp311-win_amd64.pyd.p/meson-generated_sklearn_utils__isfinite.pyx.c.obj
  [70/251] Compiling Cython source sklearn/_loss/_loss.pyx
  [71/251] Compiling Cython source sklearn/utils/_weight_vector.pyx
  [72/251] Linking target sklearn/utils/_isfinite.cp311-win_amd64.pyd
     Creating library sklearn\utils\_isfinite.cp311-win_amd64.lib and object sklearn\utils\_isfinite.cp311-win_amd64.exp

  [73/251] Compiling C object sklearn/utils/sparsefuncs_fast.cp311-win_amd64.pyd.p/meson-generated_sklearn_utils_sparsefuncs_fast.pyx.c.obj
  [74/251] Linking target sklearn/utils/sparsefuncs_fast.cp311-win_amd64.pyd
     Creating library sklearn\utils\sparsefuncs_fast.cp311-win_amd64.lib and object sklearn\utils\sparsefuncs_fast.cp311-win_amd64.exp

  [75/251] Compiling Cython source sklearn/metrics/_pairwise_distances_reduction/_datasets_pair.pyx
  [76/251] Compiling C object sklearn/metrics/_pairwise_fast.cp311-win_amd64.pyd.p/meson-generated_sklearn_metrics__pairwise_fast.pyx.c.obj
  [77/251] Generating sklearn/metrics/_pairwise_distances_reduction/_argkmin_pxd with a custom command
  [78/251] Linking target sklearn/metrics/_pairwise_fast.cp311-win_amd64.pyd
     Creating library sklearn\metrics\_pairwise_fast.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_fast.cp311-win_amd64.exp
  [79/251] Compiling C object sklearn/utils/_weight_vector.cp311-win_amd64.pyd.p/meson-generated_sklearn_utils__weight_vector.pyx.c.obj
  [80/251] Linking target sklearn/utils/_weight_vector.cp311-win_amd64.pyd
     Creating library sklearn\utils\_weight_vector.cp311-win_amd64.lib and object sklearn\utils\_weight_vector.cp311-win_amd64.exp

  [81/251] Generating sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors_pxd with a custom command
  [82/251] Generating sklearn/metrics/_pairwise_distances_reduction/_argkmin_pyx with a custom command
  [83/251] Compiling C object sklearn/utils/_seq_dataset.cp311-win_amd64.pyd.p/meson-generated_sklearn_utils__seq_dataset.pyx.c.obj
  [84/251] Generating sklearn/metrics/_pairwise_distances_reduction/_argkmin_classmode_pyx with a custom command
  [85/251] Linking target sklearn/utils/_seq_dataset.cp311-win_amd64.pyd
     Creating library sklearn\utils\_seq_dataset.cp311-win_amd64.lib and object sklearn\utils\_seq_dataset.cp311-win_amd64.exp

  [86/251] Generating sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors_pyx with a custom command
  [87/251] Compiling Cython source sklearn/metrics/_pairwise_distances_reduction/_base.pyx
  [88/251] Generating sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors_classmode_pyx with a custom command
  [89/251] Compiling Cython source sklearn/metrics/_dist_metrics.pyx
  warning: sklearn\metrics\_dist_metrics.pyx:846:44: Assigning to 'float64_t *' from 'const float64_t *' discards const qualifier
  warning: sklearn\metrics\_dist_metrics.pyx:909:40: Assigning to 'float64_t *' from 'const float64_t *' discards const qualifier
  warning: sklearn\metrics\_dist_metrics.pyx:3426:44: Assigning to 'float32_t *' from 'const float32_t *' discards const qualifier
  warning: sklearn\metrics\_dist_metrics.pyx:3489:40: Assigning to 'float32_t *' from 'const float32_t *' discards const qualifier

  [90/251] Compiling C++ object sklearn/metrics/_pairwise_distances_reduction/_datasets_pair.cp311-win_amd64.pyd.p/meson-generated_sklearn_metrics__pairwise_distances_reduction__datasets_pair.pyx.cpp.obj
  sklearn/metrics/_pairwise_distances_reduction/_datasets_pair.cp311-win_amd64.pyd.p/sklearn/metrics/_pairwise_distances_reduction/_datasets_pair.pyx.cpp(43425): warning C4551: function call missing argument list
  [91/251] Linking target sklearn/metrics/_pairwise_distances_reduction/_datasets_pair.cp311-win_amd64.pyd
     Creating library sklearn\metrics\_pairwise_distances_reduction\_datasets_pair.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_distances_reduction\_datasets_pair.cp311-win_amd64.exp

  [92/251] Compiling Cython source sklearn/metrics/_pairwise_distances_reduction/_middle_term_computer.pyx
  [93/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/metrics/cluster/_expected_mutual_info_fast.pyx"
  [94/251] Compiling C++ object sklearn/metrics/_pairwise_distances_reduction/_base.cp311-win_amd64.pyd.p/meson-generated_sklearn_metrics__pairwise_distances_reduction__base.pyx.cpp.obj
  sklearn/metrics/_pairwise_distances_reduction/_base.cp311-win_amd64.pyd.p/sklearn/metrics/_pairwise_distances_reduction/_base.pyx.cpp(32606): warning C4551: function call missing argument list
  [95/251] Compiling Cython source sklearn/metrics/_pairwise_distances_reduction/_argkmin.pyx
  [96/251] Compiling Cython source sklearn/metrics/_pairwise_distances_reduction/_argkmin_classmode.pyx
  [97/251] Linking target sklearn/metrics/_pairwise_distances_reduction/_base.cp311-win_amd64.pyd
     Creating library sklearn\metrics\_pairwise_distances_reduction\_base.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_distances_reduction\_base.cp311-win_amd64.exp

  [98/251] Compiling Cython source sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors_classmode.pyx
  [99/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/cluster/_dbscan_inner.pyx"
  [100/251] Compiling C object sklearn/metrics/cluster/_expected_mutual_info_fast.cp311-win_amd64.pyd.p/meson-generated_sklearn_metrics_cluster__expected_mutual_info_fast.pyx.c.obj
  sklearn/metrics/cluster/_expected_mutual_info_fast.cp311-win_amd64.pyd.p/sklearn/metrics/cluster/_expected_mutual_info_fast.pyx.c(18720): warning C4244: 'function': conversion from 'Py_ssize_t' to 'double', possible loss of data
  sklearn/metrics/cluster/_expected_mutual_info_fast.cp311-win_amd64.pyd.p/sklearn/metrics/cluster/_expected_mutual_info_fast.pyx.c(18720): warning C4244: 'function': conversion from 'Py_ssize_t' to 'double', possible loss of data
  sklearn/metrics/cluster/_expected_mutual_info_fast.cp311-win_amd64.pyd.p/sklearn/metrics/cluster/_expected_mutual_info_fast.pyx.c(18720): warning C4244: 'function': conversion from 'Py_ssize_t' to 'double', possible loss of data
  [101/251] Linking target sklearn/metrics/cluster/_expected_mutual_info_fast.cp311-win_amd64.pyd
     Creating library sklearn\metrics\cluster\_expected_mutual_info_fast.cp311-win_amd64.lib and object sklearn\metrics\cluster\_expected_mutual_info_fast.cp311-win_amd64.exp
  [102/251] Compiling Cython source sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors.pyx
  [103/251] Compiling C++ object sklearn/metrics/_pairwise_distances_reduction/_middle_term_computer.cp311-win_amd64.pyd.p/meson-generated_sklearn_metrics__pairwise_distances_reduction__middle_term_computer.pyx.cpp.obj
  sklearn/metrics/_pairwise_distances_reduction/_middle_term_computer.cp311-win_amd64.pyd.p/sklearn/metrics/_pairwise_distances_reduction/_middle_term_computer.pyx.cpp(42045): warning C4551: function call missing argument list
  [104/251] Linking target sklearn/metrics/_pairwise_distances_reduction/_middle_term_computer.cp311-win_amd64.pyd
     Creating library sklearn\metrics\_pairwise_distances_reduction\_middle_term_computer.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_distances_reduction\_middle_term_computer.cp311-win_amd64.exp

  [105/251] Compiling C++ object sklearn/metrics/_pairwise_distances_reduction/_argkmin_classmode.cp311-win_amd64.pyd.p/meson-generated_sklearn_metrics__pairwise_distances_reduction__argkmin_classmode.pyx.cpp.obj
  cl : Command line warning D9002 : ignoring unknown option '-fno-sized-deallocation'
  sklearn/metrics/_pairwise_distances_reduction/_argkmin_classmode.cp311-win_amd64.pyd.p/sklearn/metrics/_pairwise_distances_reduction/_argkmin_classmode.pyx.cpp(29323): warning C4551: function call missing argument list
  [106/251] Linking target sklearn/metrics/_pairwise_distances_reduction/_argkmin_classmode.cp311-win_amd64.pyd
     Creating library sklearn\metrics\_pairwise_distances_reduction\_argkmin_classmode.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_distances_reduction\_argkmin_classmode.cp311-win_amd64.exp
  [107/251] Compiling C++ object sklearn/metrics/_pairwise_distances_reduction/_argkmin.cp311-win_amd64.pyd.p/meson-generated_sklearn_metrics__pairwise_distances_reduction__argkmin.pyx.cpp.obj
  sklearn/metrics/_pairwise_distances_reduction/_argkmin.cp311-win_amd64.pyd.p/sklearn/metrics/_pairwise_distances_reduction/_argkmin.pyx.cpp(35870): warning C4551: function call missing argument list
  [108/251] Linking target sklearn/metrics/_pairwise_distances_reduction/_argkmin.cp311-win_amd64.pyd
     Creating library sklearn\metrics\_pairwise_distances_reduction\_argkmin.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_distances_reduction\_argkmin.cp311-win_amd64.exp

  [109/251] Compiling C++ object sklearn/cluster/_dbscan_inner.cp311-win_amd64.pyd.p/meson-generated_sklearn_cluster__dbscan_inner.pyx.cpp.obj
  sklearn/cluster/_dbscan_inner.cp311-win_amd64.pyd.p/sklearn/cluster/_dbscan_inner.pyx.cpp(23107): warning C4551: function call missing argument list
  [110/251] Compiling C object sklearn/metrics/_dist_metrics.cp311-win_amd64.pyd.p/meson-generated_sklearn_metrics__dist_metrics.pyx.c.obj
  sklearn/metrics/_dist_metrics.cp311-win_amd64.pyd.p/sklearn/metrics/_dist_metrics.pyx.c(29538): warning C4090: '=': different 'const' qualifiers
  sklearn/metrics/_dist_metrics.cp311-win_amd64.pyd.p/sklearn/metrics/_dist_metrics.pyx.c(30323): warning C4090: '=': different 'const' qualifiers
  sklearn/metrics/_dist_metrics.cp311-win_amd64.pyd.p/sklearn/metrics/_dist_metrics.pyx.c(49162): warning C4090: '=': different 'const' qualifiers
  sklearn/metrics/_dist_metrics.cp311-win_amd64.pyd.p/sklearn/metrics/_dist_metrics.pyx.c(49947): warning C4090: '=': different 'const' qualifiers
  [111/251] Linking target sklearn/cluster/_dbscan_inner.cp311-win_amd64.pyd
     Creating library sklearn\cluster\_dbscan_inner.cp311-win_amd64.lib and object sklearn\cluster\_dbscan_inner.cp311-win_amd64.exp

  [112/251] Linking target sklearn/metrics/_dist_metrics.cp311-win_amd64.pyd
     Creating library sklearn\metrics\_dist_metrics.cp311-win_amd64.lib and object sklearn\metrics\_dist_metrics.cp311-win_amd64.exp

  [113/251] Compiling C++ object sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors_classmode.cp311-win_amd64.pyd.p/meson-generated_sklearn_metrics__pairwise_distances_reduction__radius_neighbors_classmode.pyx.cpp.obj
  sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors_classmode.cp311-win_amd64.pyd.p/sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors_classmode.pyx.cpp(32619): warning C4551: function call missing argument list
  [114/251] Linking target sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors_classmode.cp311-win_amd64.pyd
     Creating library sklearn\metrics\_pairwise_distances_reduction\_radius_neighbors_classmode.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_distances_reduction\_radius_neighbors_classmode.cp311-win_amd64.exp
  [115/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/cluster/_hierarchical_fast.pyx"
  [116/251] Compiling C++ object sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors.cp311-win_amd64.pyd.p/meson-generated_sklearn_metrics__pairwise_distances_reduction__radius_neighbors.pyx.cpp.obj
  sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors.cp311-win_amd64.pyd.p/sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors.pyx.cpp(38873): warning C4551: function call missing argument list
  [117/251] Linking target sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors.cp311-win_amd64.pyd
     Creating library sklearn\metrics\_pairwise_distances_reduction\_radius_neighbors.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_distances_reduction\_radius_neighbors.cp311-win_amd64.exp

  [118/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/cluster/_k_means_common.pyx"
  [119/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/cluster/_k_means_lloyd.pyx"
  [120/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/cluster/_k_means_elkan.pyx"
  [121/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/cluster/_k_means_minibatch.pyx"
  [122/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/cluster/_hdbscan/_linkage.pyx"
  [123/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/cluster/_hdbscan/_reachability.pyx"
  [124/251] Compiling C++ object sklearn/cluster/_hierarchical_fast.cp311-win_amd64.pyd.p/meson-generated_sklearn_cluster__hierarchical_fast.pyx.cpp.obj
  sklearn/cluster/_hierarchical_fast.cp311-win_amd64.pyd.p/sklearn/cluster/_hierarchical_fast.pyx.cpp(23677): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/cluster/_hierarchical_fast.cp311-win_amd64.pyd.p/sklearn/cluster/_hierarchical_fast.pyx.cpp(23688): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/cluster/_hierarchical_fast.cp311-win_amd64.pyd.p/sklearn/cluster/_hierarchical_fast.pyx.cpp(23712): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/cluster/_hierarchical_fast.cp311-win_amd64.pyd.p/sklearn/cluster/_hierarchical_fast.pyx.cpp(24838): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/cluster/_hierarchical_fast.cp311-win_amd64.pyd.p/sklearn/cluster/_hierarchical_fast.pyx.cpp(24849): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/cluster/_hierarchical_fast.cp311-win_amd64.pyd.p/sklearn/cluster/_hierarchical_fast.pyx.cpp(33802): warning C4551: function call missing argument list
  [125/251] Linking target sklearn/cluster/_hierarchical_fast.cp311-win_amd64.pyd
     Creating library sklearn\cluster\_hierarchical_fast.cp311-win_amd64.lib and object sklearn\cluster\_hierarchical_fast.cp311-win_amd64.exp

  [126/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/cluster/_hdbscan/_tree.pyx"
  [127/251] Compiling C object sklearn/cluster/_k_means_lloyd.cp311-win_amd64.pyd.p/meson-generated_sklearn_cluster__k_means_lloyd.pyx.c.obj
  [128/251] Linking target sklearn/cluster/_k_means_lloyd.cp311-win_amd64.pyd
     Creating library sklearn\cluster\_k_means_lloyd.cp311-win_amd64.lib and object sklearn\cluster\_k_means_lloyd.cp311-win_amd64.exp

  [129/251] Compiling C object sklearn/cluster/_k_means_minibatch.cp311-win_amd64.pyd.p/meson-generated_sklearn_cluster__k_means_minibatch.pyx.c.obj
  [130/251] Linking target sklearn/cluster/_k_means_minibatch.cp311-win_amd64.pyd
     Creating library sklearn\cluster\_k_means_minibatch.cp311-win_amd64.lib and object sklearn\cluster\_k_means_minibatch.cp311-win_amd64.exp

  [131/251] Compiling C object sklearn/cluster/_hdbscan/_linkage.cp311-win_amd64.pyd.p/meson-generated_sklearn_cluster__hdbscan__linkage.pyx.c.obj
  [132/251] Compiling C object sklearn/cluster/_k_means_common.cp311-win_amd64.pyd.p/meson-generated_sklearn_cluster__k_means_common.pyx.c.obj
  [133/251] Linking target sklearn/cluster/_hdbscan/_linkage.cp311-win_amd64.pyd
     Creating library sklearn\cluster\_hdbscan\_linkage.cp311-win_amd64.lib and object sklearn\cluster\_hdbscan\_linkage.cp311-win_amd64.exp

  [134/251] Linking target sklearn/cluster/_k_means_common.cp311-win_amd64.pyd
     Creating library sklearn\cluster\_k_means_common.cp311-win_amd64.lib and object sklearn\cluster\_k_means_common.cp311-win_amd64.exp

  [135/251] Compiling C object sklearn/cluster/_k_means_elkan.cp311-win_amd64.pyd.p/meson-generated_sklearn_cluster__k_means_elkan.pyx.c.obj
  [136/251] Compiling C object sklearn/cluster/_hdbscan/_reachability.cp311-win_amd64.pyd.p/meson-generated_sklearn_cluster__hdbscan__reachability.pyx.c.obj
  [137/251] Linking target sklearn/cluster/_k_means_elkan.cp311-win_amd64.pyd
     Creating library sklearn\cluster\_k_means_elkan.cp311-win_amd64.lib and object sklearn\cluster\_k_means_elkan.cp311-win_amd64.exp
  [138/251] Linking target sklearn/cluster/_hdbscan/_reachability.cp311-win_amd64.pyd
     Creating library sklearn\cluster\_hdbscan\_reachability.cp311-win_amd64.lib and object sklearn\cluster\_hdbscan\_reachability.cp311-win_amd64.exp

  [139/251] Compiling C object sklearn/cluster/_hdbscan/_tree.cp311-win_amd64.pyd.p/meson-generated_sklearn_cluster__hdbscan__tree.pyx.c.obj
  [140/251] Linking target sklearn/cluster/_hdbscan/_tree.cp311-win_amd64.pyd
     Creating library sklearn\cluster\_hdbscan\_tree.cp311-win_amd64.lib and object sklearn\cluster\_hdbscan\_tree.cp311-win_amd64.exp

  [141/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/decomposition/_cdnmf_fast.pyx"
  [142/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/decomposition/_online_lda_fast.pyx"
  [143/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/datasets/_svmlight_format_fast.pyx"
  [144/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/ensemble/_hist_gradient_boosting/_gradient_boosting.pyx"
  [145/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/ensemble/_hist_gradient_boosting/histogram.pyx"
  [146/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/ensemble/_gradient_boosting.pyx"
  [147/251] Compiling C object sklearn/decomposition/_cdnmf_fast.cp311-win_amd64.pyd.p/meson-generated_sklearn_decomposition__cdnmf_fast.pyx.c.obj
  [148/251] Compiling C object sklearn/decomposition/_online_lda_fast.cp311-win_amd64.pyd.p/meson-generated_sklearn_decomposition__online_lda_fast.pyx.c.obj
  [149/251] Linking target sklearn/decomposition/_cdnmf_fast.cp311-win_amd64.pyd
     Creating library sklearn\decomposition\_cdnmf_fast.cp311-win_amd64.lib and object sklearn\decomposition\_cdnmf_fast.cp311-win_amd64.exp

  [150/251] Linking target sklearn/decomposition/_online_lda_fast.cp311-win_amd64.pyd
     Creating library sklearn\decomposition\_online_lda_fast.cp311-win_amd64.lib and object sklearn\decomposition\_online_lda_fast.cp311-win_amd64.exp

  [151/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/ensemble/_hist_gradient_boosting/_binning.pyx"
  [152/251] Compiling C object sklearn/ensemble/_hist_gradient_boosting/_gradient_boosting.cp311-win_amd64.pyd.p/meson-generated_sklearn_ensemble__hist_gradient_boosting__gradient_boosting.pyx.c.obj
  [153/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/ensemble/_hist_gradient_boosting/splitting.pyx"
  [154/251] Linking target sklearn/ensemble/_hist_gradient_boosting/_gradient_boosting.cp311-win_amd64.pyd
     Creating library sklearn\ensemble\_hist_gradient_boosting\_gradient_boosting.cp311-win_amd64.lib and object sklearn\ensemble\_hist_gradient_boosting\_gradient_boosting.cp311-win_amd64.exp

  [155/251] Compiling C object sklearn/ensemble/_gradient_boosting.cp311-win_amd64.pyd.p/meson-generated_sklearn_ensemble__gradient_boosting.pyx.c.obj
  [156/251] Compiling C object sklearn/ensemble/_hist_gradient_boosting/histogram.cp311-win_amd64.pyd.p/meson-generated_sklearn_ensemble__hist_gradient_boosting_histogram.pyx.c.obj
  [157/251] Linking target sklearn/ensemble/_gradient_boosting.cp311-win_amd64.pyd
     Creating library sklearn\ensemble\_gradient_boosting.cp311-win_amd64.lib and object sklearn\ensemble\_gradient_boosting.cp311-win_amd64.exp
  [158/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/ensemble/_hist_gradient_boosting/_predictor.pyx"
  [159/251] Linking target sklearn/ensemble/_hist_gradient_boosting/histogram.cp311-win_amd64.pyd
     Creating library sklearn\ensemble\_hist_gradient_boosting\histogram.cp311-win_amd64.lib and object sklearn\ensemble\_hist_gradient_boosting\histogram.cp311-win_amd64.exp
  [160/251] Compiling C object sklearn/ensemble/_hist_gradient_boosting/_binning.cp311-win_amd64.pyd.p/meson-generated_sklearn_ensemble__hist_gradient_boosting__binning.pyx.c.obj
  [161/251] Linking target sklearn/ensemble/_hist_gradient_boosting/_binning.cp311-win_amd64.pyd
     Creating library sklearn\ensemble\_hist_gradient_boosting\_binning.cp311-win_amd64.lib and object sklearn\ensemble\_hist_gradient_boosting\_binning.cp311-win_amd64.exp

  [162/251] Copying file sklearn/linear_model/__init__.py
  [163/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/ensemble/_hist_gradient_boosting/common.pyx"
  [164/251] Compiling C object sklearn/ensemble/_hist_gradient_boosting/_predictor.cp311-win_amd64.pyd.p/meson-generated_sklearn_ensemble__hist_gradient_boosting__predictor.pyx.c.obj
  [165/251] Linking target sklearn/ensemble/_hist_gradient_boosting/_predictor.cp311-win_amd64.pyd
     Creating library sklearn\ensemble\_hist_gradient_boosting\_predictor.cp311-win_amd64.lib and object sklearn\ensemble\_hist_gradient_boosting\_predictor.cp311-win_amd64.exp

  [166/251] Compiling C object sklearn/datasets/_svmlight_format_fast.cp311-win_amd64.pyd.p/meson-generated_sklearn_datasets__svmlight_format_fast.pyx.c.obj
  [167/251] Generating sklearn/linear_model/_sgd_fast_pyx with a custom command
  [168/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/ensemble/_hist_gradient_boosting/_bitset.pyx"
  [169/251] Linking target sklearn/datasets/_svmlight_format_fast.cp311-win_amd64.pyd
     Creating library sklearn\datasets\_svmlight_format_fast.cp311-win_amd64.lib and object sklearn\datasets\_svmlight_format_fast.cp311-win_amd64.exp

  [170/251] Compiling C object sklearn/ensemble/_hist_gradient_boosting/splitting.cp311-win_amd64.pyd.p/meson-generated_sklearn_ensemble__hist_gradient_boosting_splitting.pyx.c.obj
  [171/251] Generating sklearn/linear_model/_sag_fast_pyx with a custom command
  [172/251] Linking target sklearn/ensemble/_hist_gradient_boosting/splitting.cp311-win_amd64.pyd
     Creating library sklearn\ensemble\_hist_gradient_boosting\splitting.cp311-win_amd64.lib and object sklearn\ensemble\_hist_gradient_boosting\splitting.cp311-win_amd64.exp

  [173/251] Generating sklearn/neighbors/_binary_tree_pxi with a custom command
  [174/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/feature_extraction/_hashing_fast.pyx"
  [175/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/manifold/_utils.pyx"
  [176/251] Compiling C object sklearn/ensemble/_hist_gradient_boosting/_bitset.cp311-win_amd64.pyd.p/meson-generated_sklearn_ensemble__hist_gradient_boosting__bitset.pyx.c.obj
  [177/251] Linking target sklearn/ensemble/_hist_gradient_boosting/_bitset.cp311-win_amd64.pyd
     Creating library sklearn\ensemble\_hist_gradient_boosting\_bitset.cp311-win_amd64.lib and object sklearn\ensemble\_hist_gradient_boosting\_bitset.cp311-win_amd64.exp

  [178/251] Compiling C object sklearn/ensemble/_hist_gradient_boosting/common.cp311-win_amd64.pyd.p/meson-generated_sklearn_ensemble__hist_gradient_boosting_common.pyx.c.obj
  [179/251] Linking target sklearn/ensemble/_hist_gradient_boosting/common.cp311-win_amd64.pyd
     Creating library sklearn\ensemble\_hist_gradient_boosting\common.cp311-win_amd64.lib and object sklearn\ensemble\_hist_gradient_boosting\common.cp311-win_amd64.exp

  [180/251] Copying file sklearn/neighbors/__init__.py
  [181/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/linear_model/_cd_fast.pyx"
  [182/251] Compiling C object sklearn/_loss/_loss.cp311-win_amd64.pyd.p/meson-generated_sklearn__loss__loss.pyx.c.obj
  [183/251] Copying file sklearn/neighbors/_partition_nodes.pxd
  [184/251] Linking target sklearn/_loss/_loss.cp311-win_amd64.pyd
     Creating library sklearn\_loss\_loss.cp311-win_amd64.lib and object sklearn\_loss\_loss.cp311-win_amd64.exp

  [185/251] Compiling C object sklearn/manifold/_utils.cp311-win_amd64.pyd.p/meson-generated_sklearn_manifold__utils.pyx.c.obj
  sklearn/manifold/_utils.cp311-win_amd64.pyd.p/sklearn/manifold/_utils.pyx.c(20845): warning C4305: '=': truncation from 'double' to 'float'
  sklearn/manifold/_utils.cp311-win_amd64.pyd.p/sklearn/manifold/_utils.pyx.c(20854): warning C4305: '=': truncation from 'double' to 'float'
  [186/251] Linking target sklearn/manifold/_utils.cp311-win_amd64.pyd
     Creating library sklearn\manifold\_utils.cp311-win_amd64.lib and object sklearn\manifold\_utils.cp311-win_amd64.exp
  [187/251] Generating sklearn/neighbors/_ball_tree_pyx with a custom command
  [188/251] Compiling C++ object sklearn/feature_extraction/_hashing_fast.cp311-win_amd64.pyd.p/meson-generated_sklearn_feature_extraction__hashing_fast.pyx.cpp.obj
  [189/251] Linking target sklearn/feature_extraction/_hashing_fast.cp311-win_amd64.pyd
     Creating library sklearn\feature_extraction\_hashing_fast.cp311-win_amd64.lib and object sklearn\feature_extraction\_hashing_fast.cp311-win_amd64.exp

  [190/251] Generating sklearn/neighbors/_kd_tree_pyx with a custom command
  [191/251] Compiling Cython source sklearn/linear_model/_sgd_fast.pyx
  [192/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/manifold/_barnes_hut_tsne.pyx"
  [193/251] Compiling Cython source sklearn/linear_model/_sag_fast.pyx
  [194/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/neighbors/_partition_nodes.pyx"
  [195/251] Compiling C++ object sklearn/neighbors/_partition_nodes.cp311-win_amd64.pyd.p/meson-generated_sklearn_neighbors__partition_nodes.pyx.cpp.obj
  [196/251] Compiling C object sklearn/manifold/_barnes_hut_tsne.cp311-win_amd64.pyd.p/meson-generated_sklearn_manifold__barnes_hut_tsne.pyx.c.obj
  sklearn/manifold/_barnes_hut_tsne.cp311-win_amd64.pyd.p/sklearn/manifold/_barnes_hut_tsne.pyx.c(22163): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 1 has type 'Py_ssize_t'
  sklearn/manifold/_barnes_hut_tsne.cp311-win_amd64.pyd.p/sklearn/manifold/_barnes_hut_tsne.pyx.c(22163): note: consider using '%lli' in the format string
  sklearn/manifold/_barnes_hut_tsne.cp311-win_amd64.pyd.p/sklearn/manifold/_barnes_hut_tsne.pyx.c(22163): note: consider using '%Ii' in the format string
  sklearn/manifold/_barnes_hut_tsne.cp311-win_amd64.pyd.p/sklearn/manifold/_barnes_hut_tsne.pyx.c(22163): note: consider using '%I64i' in the format string
  [197/251] Linking target sklearn/neighbors/_partition_nodes.cp311-win_amd64.pyd
     Creating library sklearn\neighbors\_partition_nodes.cp311-win_amd64.lib and object sklearn\neighbors\_partition_nodes.cp311-win_amd64.exp

  [198/251] Linking target sklearn/manifold/_barnes_hut_tsne.cp311-win_amd64.pyd
     Creating library sklearn\manifold\_barnes_hut_tsne.cp311-win_amd64.lib and object sklearn\manifold\_barnes_hut_tsne.cp311-win_amd64.exp

  [199/251] Compiling C object sklearn/linear_model/_sgd_fast.cp311-win_amd64.pyd.p/meson-generated_sklearn_linear_model__sgd_fast.pyx.c.obj
  [200/251] Compiling C object sklearn/linear_model/_cd_fast.cp311-win_amd64.pyd.p/meson-generated_sklearn_linear_model__cd_fast.pyx.c.obj
  [201/251] Linking target sklearn/linear_model/_sgd_fast.cp311-win_amd64.pyd
     Creating library sklearn\linear_model\_sgd_fast.cp311-win_amd64.lib and object sklearn\linear_model\_sgd_fast.cp311-win_amd64.exp
  [202/251] Linking target sklearn/linear_model/_cd_fast.cp311-win_amd64.pyd
     Creating library sklearn\linear_model\_cd_fast.cp311-win_amd64.lib and object sklearn\linear_model\_cd_fast.cp311-win_amd64.exp

  [203/251] Compiling C object sklearn/linear_model/_sag_fast.cp311-win_amd64.pyd.p/meson-generated_sklearn_linear_model__sag_fast.pyx.c.obj
  [204/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/preprocessing/_csr_polynomial_expansion.pyx"
  [205/251] Linking target sklearn/linear_model/_sag_fast.cp311-win_amd64.pyd
     Creating library sklearn\linear_model\_sag_fast.cp311-win_amd64.lib and object sklearn\linear_model\_sag_fast.cp311-win_amd64.exp

  [206/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/preprocessing/_target_encoder_fast.pyx"
  [207/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/neighbors/_quad_tree.pyx"
  [208/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/svm/_newrand.pyx"
  [209/251] Compiling C++ object sklearn/svm/liblibsvm-skl.a.p/src_libsvm_libsvm_template.cpp.obj
  C:\repos\Building from source\scikit-learn\sklearn\svm\src\libsvm\../newrand/newrand.h(40): warning C4146: unary minus operator applied to unsigned type, result still unsigned
  C:\repos\Building from source\scikit-learn\sklearn\svm\src\libsvm\svm.cpp(1881): warning C4805: '|=': unsafe mix of type 'int' and type 'bool' in operation
  C:\repos\Building from source\scikit-learn\sklearn\svm\src\libsvm\svm.cpp(3157): warning C4244: 'initializing': conversion from 'double' to 'int', possible loss of data
  C:\repos\Building from source\scikit-learn\sklearn\svm\src\libsvm\svm.cpp(1881): warning C4805: '|=': unsafe mix of type 'int' and type 'bool' in operation
  C:\repos\Building from source\scikit-learn\sklearn\svm\src\libsvm\svm.cpp(3157): warning C4244: 'initializing': conversion from 'double' to 'int', possible loss of data
  [210/251] Compiling C++ object sklearn/svm/libliblinear-skl.a.p/src_liblinear_linear.cpp.obj
  C:\repos\Building from source\scikit-learn\sklearn\svm\src\liblinear\../newrand/newrand.h(40): warning C4146: unary minus operator applied to unsigned type, result still unsigned
  [211/251] Compiling C++ object sklearn/svm/libliblinear-skl.a.p/src_liblinear_tron.cpp.obj
  [212/251] Linking static target sklearn/svm/libliblinear-skl.a
  [213/251] Linking static target sklearn/svm/liblibsvm-skl.a
  [214/251] Compiling Cython source sklearn/neighbors/_ball_tree.pyx
  warning: sklearn\neighbors\_binary_tree.pxi:1092:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:1958:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:2053:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:2222:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:2345:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:2402:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:2403:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:2728:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:3594:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:3689:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:3858:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:3981:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:4038:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:4039:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_ball_tree.pyx:105:9: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier

  warning: sklearn\neighbors\_ball_tree.pyx:107:9: Assigning to 'float64_t *' from 'const float64_t *' discards const qualifier

  warning: sklearn\neighbors\_ball_tree.pyx:308:9: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier

  warning: sklearn\neighbors\_ball_tree.pyx:310:9: Assigning to 'float32_t *' from 'const float32_t *' discards const qualifier

  [215/251] Compiling C++ object sklearn/svm/_newrand.cp311-win_amd64.pyd.p/meson-generated_sklearn_svm__newrand.pyx.cpp.obj
  ..\..\sklearn\svm\src\newrand\newrand.h(40): warning C4146: unary minus operator applied to unsigned type, result still unsigned
  [216/251] Linking target sklearn/svm/_newrand.cp311-win_amd64.pyd
     Creating library sklearn\svm\_newrand.cp311-win_amd64.lib and object sklearn\svm\_newrand.cp311-win_amd64.exp
  [217/251] Compiling Cython source sklearn/neighbors/_kd_tree.pyx
  warning: sklearn\neighbors\_binary_tree.pxi:1092:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:1958:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:2053:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:2222:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:2345:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:2402:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:2403:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:2728:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:3594:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:3689:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:3858:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:3981:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:4038:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_binary_tree.pxi:4039:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
  warning: sklearn\neighbors\_kd_tree.pyx:74:9: Assigning to 'float64_t *' from 'const float64_t *' discards const qualifier
  warning: sklearn\neighbors\_kd_tree.pyx:75:9: Assigning to 'float64_t *' from 'const float64_t *' discards const qualifier
  warning: sklearn\neighbors\_kd_tree.pyx:342:9: Assigning to 'float32_t *' from 'const float32_t *' discards const qualifier
  warning: sklearn\neighbors\_kd_tree.pyx:343:9: Assigning to 'float32_t *' from 'const float32_t *' discards const qualifier
  [218/251] Compiling C object sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/meson-generated_sklearn_neighbors__quad_tree.pyx.c.obj
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25472): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 1 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25472): note: consider using '%lli' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25472): note: consider using '%Ii' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25472): note: consider using '%I64i' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 1 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): note: consider using '%lli' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): note: consider using '%Ii' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): note: consider using '%I64i' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 2 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): note: consider using '%lli' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): note: consider using '%Ii' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): note: consider using '%I64i' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25683): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 1 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25683): note: consider using '%lli' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25683): note: consider using '%Ii' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25683): note: consider using '%I64i' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 1 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): note: consider using '%lli' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): note: consider using '%Ii' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): note: consider using '%I64i' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 2 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): note: consider using '%lli' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): note: consider using '%Ii' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): note: consider using '%I64i' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 4 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): note: consider using '%lli' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): note: consider using '%Ii' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): note: consider using '%I64i' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 11 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): note: consider using '%lli' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): note: consider using '%Ii' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): note: consider using '%I64i' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 3 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): note: consider using '%lli' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): note: consider using '%Ii' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): note: consider using '%I64i' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 8 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): note: consider using '%lli' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): note: consider using '%Ii' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): note: consider using '%I64i' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28020): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 1 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28020): note: consider using '%lli' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28020): note: consider using '%Ii' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28020): note: consider using '%I64i' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28139): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 1 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28139): note: consider using '%lli' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28139): note: consider using '%Ii' in the format string
  sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28139): note: consider using '%I64i' in the format string
  [219/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/svm/_libsvm.pyx"
  [220/251] Linking target sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd
     Creating library sklearn\neighbors\_quad_tree.cp311-win_amd64.lib and object sklearn\neighbors\_quad_tree.cp311-win_amd64.exp
  [221/251] Compiling C object sklearn/preprocessing/_csr_polynomial_expansion.cp311-win_amd64.pyd.p/meson-generated_sklearn_preprocessing__csr_polynomial_expansion.pyx.c.obj
  [222/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/svm/_libsvm_sparse.pyx"
  [223/251] Linking target sklearn/preprocessing/_csr_polynomial_expansion.cp311-win_amd64.pyd
     Creating library sklearn\preprocessing\_csr_polynomial_expansion.cp311-win_amd64.lib and object sklearn\preprocessing\_csr_polynomial_expansion.cp311-win_amd64.exp

  [224/251] Compiling C++ object sklearn/preprocessing/_target_encoder_fast.cp311-win_amd64.pyd.p/meson-generated_sklearn_preprocessing__target_encoder_fast.pyx.cpp.obj
  sklearn/preprocessing/_target_encoder_fast.cp311-win_amd64.pyd.p/sklearn/preprocessing/_target_encoder_fast.pyx.cpp(39805): warning C4551: function call missing argument list
  [225/251] Linking target sklearn/preprocessing/_target_encoder_fast.cp311-win_amd64.pyd
     Creating library sklearn\preprocessing\_target_encoder_fast.cp311-win_amd64.lib and object sklearn\preprocessing\_target_encoder_fast.cp311-win_amd64.exp
  [226/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/svm/_liblinear.pyx"
  [227/251] Compiling C object sklearn/svm/_libsvm_sparse.cp311-win_amd64.pyd.p/meson-generated_sklearn_svm__libsvm_sparse.pyx.c.obj
  [228/251] Linking target sklearn/svm/_libsvm_sparse.cp311-win_amd64.pyd
     Creating library sklearn\svm\_libsvm_sparse.cp311-win_amd64.lib and object sklearn\svm\_libsvm_sparse.cp311-win_amd64.exp

  [229/251] Compiling C object sklearn/svm/_liblinear.cp311-win_amd64.pyd.p/meson-generated_sklearn_svm__liblinear.pyx.c.obj
  [230/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/tree/_partitioner.pyx"
  [231/251] Compiling C object sklearn/svm/_libsvm.cp311-win_amd64.pyd.p/meson-generated_sklearn_svm__libsvm.pyx.c.obj
  [232/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/tree/_splitter.pyx"
  [233/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/tree/_criterion.pyx"
  [234/251] Linking target sklearn/svm/_libsvm.cp311-win_amd64.pyd
     Creating library sklearn\svm\_libsvm.cp311-win_amd64.lib and object sklearn\svm\_libsvm.cp311-win_amd64.exp
  [235/251] Linking target sklearn/svm/_liblinear.cp311-win_amd64.pyd
     Creating library sklearn\svm\_liblinear.cp311-win_amd64.lib and object sklearn\svm\_liblinear.cp311-win_amd64.exp
  [236/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/tree/_utils.pyx"
  [237/251] Compiling Cython source "C:/repos/Building from source/scikit-learn/sklearn/tree/_tree.pyx"
  [238/251] Compiling C object sklearn/tree/_partitioner.cp311-win_amd64.pyd.p/meson-generated_sklearn_tree__partitioner.pyx.c.obj
  sklearn/tree/_partitioner.cp311-win_amd64.pyd.p/sklearn/tree/_partitioner.pyx.c(24489): warning C4244: 'function': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to 'double', possible loss of data
  sklearn/tree/_partitioner.cp311-win_amd64.pyd.p/sklearn/tree/_partitioner.pyx.c(24489): warning C4244: 'function': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to 'double', possible loss of data
  sklearn/tree/_partitioner.cp311-win_amd64.pyd.p/sklearn/tree/_partitioner.pyx.c(26110): warning C4244: 'function': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to 'double', possible loss of data
  sklearn/tree/_partitioner.cp311-win_amd64.pyd.p/sklearn/tree/_partitioner.pyx.c(30951): warning C4305: '=': truncation from 'double' to '__pyx_t_7sklearn_5utils_9_typedefs_float32_t'
  [239/251] Linking target sklearn/tree/_partitioner.cp311-win_amd64.pyd
     Creating library sklearn\tree\_partitioner.cp311-win_amd64.lib and object sklearn\tree\_partitioner.cp311-win_amd64.exp

  [240/251] Compiling C object sklearn/tree/_criterion.cp311-win_amd64.pyd.p/meson-generated_sklearn_tree__criterion.pyx.c.obj
  [241/251] Compiling C object sklearn/tree/_splitter.cp311-win_amd64.pyd.p/meson-generated_sklearn_tree__splitter.pyx.c.obj
  [242/251] Linking target sklearn/tree/_criterion.cp311-win_amd64.pyd
     Creating library sklearn\tree\_criterion.cp311-win_amd64.lib and object sklearn\tree\_criterion.cp311-win_amd64.exp

  [243/251] Linking target sklearn/tree/_splitter.cp311-win_amd64.pyd
     Creating library sklearn\tree\_splitter.cp311-win_amd64.lib and object sklearn\tree\_splitter.cp311-win_amd64.exp

  [244/251] Compiling C object sklearn/tree/_utils.cp311-win_amd64.pyd.p/meson-generated_sklearn_tree__utils.pyx.c.obj
  [245/251] Linking target sklearn/tree/_utils.cp311-win_amd64.pyd
     Creating library sklearn\tree\_utils.cp311-win_amd64.lib and object sklearn\tree\_utils.cp311-win_amd64.exp
  [246/251] Compiling C object sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/meson-generated_sklearn_neighbors__ball_tree.pyx.c.obj
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(24810): warning C4244: 'function': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to 'double', possible loss of data
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(32767): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(40182): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(40735): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(40979): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(41262): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(41271): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(41641): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(42252): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(42655): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(42665): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(46580): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(54004): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(54557): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(54801): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(55084): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(55093): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(55463): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(56074): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(56477): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(56487): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(58364): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(58387): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(59739): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(59762): warning C4090: '=': different 'const' qualifiers
  [247/251] Compiling C object sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/meson-generated_sklearn_neighbors__kd_tree.pyx.c.obj
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(24678): warning C4244: 'function': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to 'double', possible loss of data
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(32635): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(40050): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(40603): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(40847): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(41130): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(41139): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(41509): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(42120): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(42523): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(42533): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(46448): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(53872): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(54425): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(54669): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(54952): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(54961): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(55331): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(55942): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(56345): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(56355): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(58229): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(58241): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(60038): warning C4090: '=': different 'const' qualifiers
  sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(60050): warning C4090: '=': different 'const' qualifiers
  [248/251] Linking target sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd
     Creating library sklearn\neighbors\_ball_tree.cp311-win_amd64.lib and object sklearn\neighbors\_ball_tree.cp311-win_amd64.exp

  [249/251] Linking target sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd
     Creating library sklearn\neighbors\_kd_tree.cp311-win_amd64.lib and object sklearn\neighbors\_kd_tree.cp311-win_amd64.exp
  [250/251] Compiling C++ object sklearn/tree/_tree.cp311-win_amd64.pyd.p/meson-generated_sklearn_tree__tree.pyx.cpp.obj
  sklearn/tree/_tree.cp311-win_amd64.pyd.p/sklearn/tree/_tree.pyx.cpp(28907): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/tree/_tree.cp311-win_amd64.pyd.p/sklearn/tree/_tree.pyx.cpp(33179): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
  sklearn/tree/_tree.cp311-win_amd64.pyd.p/sklearn/tree/_tree.pyx.cpp(55049): warning C4551: function call missing argument list
  sklearn/tree/_tree.cp311-win_amd64.pyd.p/sklearn/tree/_tree.pyx.cpp(55964): warning C4551: function call missing argument list
  [251/251] Linking target sklearn/tree/_tree.cp311-win_amd64.pyd
     Creating library sklearn\tree\_tree.cp311-win_amd64.lib and object sklearn\tree\_tree.cp311-win_amd64.exp

  Activating VS 17.11.4
  INFO: automatically activated MSVC compiler environment
  INFO: autodetecting backend as ninja
  INFO: calculating backend command to run: "C:\repos\Building from source\scikit-learn\tutorial-env\Scripts\ninja.EXE"
  Preparing editable metadata (pyproject.toml) ... done
Requirement already satisfied: numpy>=1.19.5 in c:\repos\building from source\scikit-learn\tutorial-env\lib\site-packages (from scikit-learn==1.6.dev0) (2.1.1)
Requirement already satisfied: scipy>=1.6.0 in c:\repos\building from source\scikit-learn\tutorial-env\lib\site-packages (from scikit-learn==1.6.dev0) (1.14.1)
Collecting joblib>=1.2.0 (from scikit-learn==1.6.dev0)
  Obtaining dependency information for joblib>=1.2.0 from https://files.pythonhosted.org/packages/91/29/df4b9b42f2be0b623cbd5e2140cafcaa2bef0759a00b7b70104dcfe2fb51/joblib-1.4.2-py3-none-any.whl.metadata
  Downloading joblib-1.4.2-py3-none-any.whl.metadata (5.4 kB)
Collecting threadpoolctl>=3.1.0 (from scikit-learn==1.6.dev0)
  Obtaining dependency information for threadpoolctl>=3.1.0 from https://files.pythonhosted.org/packages/4b/2c/ffbf7a134b9ab11a67b0cf0726453cedd9c5043a4fe7a35d1cefa9a1bcfb/threadpoolctl-3.5.0-py3-none-any.whl.metadata
  Downloading threadpoolctl-3.5.0-py3-none-any.whl.metadata (13 kB)
Downloading joblib-1.4.2-py3-none-any.whl (301 kB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 301.8/301.8 kB 2.7 MB/s eta 0:00:00
Downloading threadpoolctl-3.5.0-py3-none-any.whl (18 kB)
Building wheels for collected packages: scikit-learn
  Running command Building editable for scikit-learn (pyproject.toml)
  Building editable for scikit-learn (pyproject.toml) ... done
  Created wheel for scikit-learn: filename=scikit_learn-1.6.dev0-cp311-cp311-win_amd64.whl size=10603 sha256=ebb548164888349acbe1cadab0683115ee30b3056e3148b9c2fb26560cabb46f
  Stored in directory: C:\Users\sinha\AppData\Local\Temp\pip-ephem-wheel-cache-z30ferwk\wheels\51\22\ab\06f080299d1c53aa75b294f930a36a83b62429ed85b72baa9a
Successfully built scikit-learn
Installing collected packages: threadpoolctl, joblib, scikit-learn
Successfully installed joblib-1.4.2 scikit-learn-1.6.dev0 threadpoolctl-3.5.0

[notice] A new release of pip is available: 24.0 -> 24.2
[notice] To update, run: python.exe -m pip install --upgrade pip
(tutorial-env)
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn (main)
$ python -c "import sklearn; sklearn.show_versions()"
meson-python: building scikit-learn: meson compile
Activating VS 17.11.4
INFO: automatically activated MSVC compiler environment
INFO: autodetecting backend as ninja
INFO: calculating backend command to run: "C:\repos\Building from source\scikit-learn\tutorial-env\Scripts\ninja.EXE"
[9/177] Compiling C++ object sklearn/utils/_vector_sentine...meson-generated_sklearn_utils__vector_sentinel.pyx.cpp.obj
sklearn/utils/_vector_sentinel.cp311-win_amd64.pyd.p/sklearn/utils/_vector_sentinel.pyx.cpp(15416): warning C4551: function call missing argument list
[12/177] Linking target sklearn/utils/_weight_vector.cp311-win_amd64.pyd
   Creating library sklearn\utils\_weight_vector.cp311-win_amd64.lib and object sklearn\utils\_weight_vector.cp311-win_amd64.exp
[13/177] Compiling Cython source sklearn/metrics/_dist_metrics.pyx
warning: sklearn\metrics\_dist_metrics.pyx:846:44: Assigning to 'float64_t *' from 'const float64_t *' discards const qualifier
warning: sklearn\metrics\_dist_metrics.pyx:909:40: Assigning to 'float64_t *' from 'const float64_t *' discards const qualifier
warning: sklearn\metrics\_dist_metrics.pyx:3426:44: Assigning to 'float32_t *' from 'const float32_t *' discards const qualifier
warning: sklearn\metrics\_dist_metrics.pyx:3489:40: Assigning to 'float32_t *' from 'const float32_t *' discards const qualifier
[14/177] Linking target sklearn/utils/_vector_sentinel.cp311-win_amd64.pyd
   Creating library sklearn\utils\_vector_sentinel.cp311-win_amd64.lib and object sklearn\utils\_vector_sentinel.cp311-win_amd64.exp
[15/177] Linking target sklearn/utils/_seq_dataset.cp311-win_amd64.pyd
   Creating library sklearn\utils\_seq_dataset.cp311-win_amd64.lib and object sklearn\utils\_seq_dataset.cp311-win_amd64.exp
[17/177] Compiling C++ object sklearn/utils/_fast_dict.cp3...pyd.p/meson-generated_sklearn_utils__fast_dict.pyx.cpp.obj
sklearn/utils/_fast_dict.cp311-win_amd64.pyd.p/sklearn/utils/_fast_dict.pyx.cpp(26950): warning C4551: function call missing argument list
[18/177] Linking target sklearn/utils/_fast_dict.cp311-win_amd64.pyd
   Creating library sklearn\utils\_fast_dict.cp311-win_amd64.lib and object sklearn\utils\_fast_dict.cp311-win_amd64.exp
[19/177] Linking target sklearn/utils/_isfinite.cp311-win_amd64.pyd
   Creating library sklearn\utils\_isfinite.cp311-win_amd64.lib and object sklearn\utils\_isfinite.cp311-win_amd64.exp
[21/177] Linking target sklearn/utils/arrayfuncs.cp311-win_amd64.pyd
   Creating library sklearn\utils\arrayfuncs.cp311-win_amd64.lib and object sklearn\utils\arrayfuncs.cp311-win_amd64.exp
[23/177] Linking target sklearn/utils/_cython_blas.cp311-win_amd64.pyd
   Creating library sklearn\utils\_cython_blas.cp311-win_amd64.lib and object sklearn\utils\_cython_blas.cp311-win_amd64.exp
[27/177] Compiling C object sklearn/metrics/_dist_metrics.....p/meson-generated_sklearn_metrics__dist_metrics.pyx.c.obj
sklearn/metrics/_dist_metrics.cp311-win_amd64.pyd.p/sklearn/metrics/_dist_metrics.pyx.c(29538): warning C4090: '=': different 'const' qualifiers
sklearn/metrics/_dist_metrics.cp311-win_amd64.pyd.p/sklearn/metrics/_dist_metrics.pyx.c(30323): warning C4090: '=': different 'const' qualifiers
sklearn/metrics/_dist_metrics.cp311-win_amd64.pyd.p/sklearn/metrics/_dist_metrics.pyx.c(49162): warning C4090: '=': different 'const' qualifiers
sklearn/metrics/_dist_metrics.cp311-win_amd64.pyd.p/sklearn/metrics/_dist_metrics.pyx.c(49947): warning C4090: '=': different 'const' qualifiers
[29/177] Linking target sklearn/metrics/_dist_metrics.cp311-win_amd64.pyd
   Creating library sklearn\metrics\_dist_metrics.cp311-win_amd64.lib and object sklearn\metrics\_dist_metrics.cp311-win_amd64.exp
[33/177] Linking target sklearn/metrics/_pairwise_fast.cp311-win_amd64.pyd
   Creating library sklearn\metrics\_pairwise_fast.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_fast.cp311-win_amd64.exp
[35/177] Linking target sklearn/utils/sparsefuncs_fast.cp311-win_amd64.pyd
   Creating library sklearn\utils\sparsefuncs_fast.cp311-win_amd64.lib and object sklearn\utils\sparsefuncs_fast.cp311-win_amd64.exp
[37/177] Compiling C++ object sklearn/metrics/_pairwise_di...s__pairwise_distances_reduction__datasets_pair.pyx.cpp.obj
sklearn/metrics/_pairwise_distances_reduction/_datasets_pair.cp311-win_amd64.pyd.p/sklearn/metrics/_pairwise_distances_reduction/_datasets_pair.pyx.cpp(43425): warning C4551: function call missing argument list
[38/177] Compiling C++ object sklearn/metrics/_pairwise_di...rn_metrics__pairwise_distances_reduction__base.pyx.cpp.obj
sklearn/metrics/_pairwise_distances_reduction/_base.cp311-win_amd64.pyd.p/sklearn/metrics/_pairwise_distances_reduction/_base.pyx.cpp(32606): warning C4551: function call missing argument list
[40/177] Linking target sklearn/metrics/_pairwise_distances_reduction/_datasets_pair.cp311-win_amd64.pyd
   Creating library sklearn\metrics\_pairwise_distances_reduction\_datasets_pair.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_distances_reduction\_datasets_pair.cp311-win_amd64.exp
[41/177] Linking target sklearn/metrics/_pairwise_distances_reduction/_base.cp311-win_amd64.pyd
   Creating library sklearn\metrics\_pairwise_distances_reduction\_base.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_distances_reduction\_base.cp311-win_amd64.exp
[42/177] Compiling C++ object sklearn/metrics/_pairwise_di...metrics__pairwise_distances_reduction__argkmin.pyx.cpp.obj
sklearn/metrics/_pairwise_distances_reduction/_argkmin.cp311-win_amd64.pyd.p/sklearn/metrics/_pairwise_distances_reduction/_argkmin.pyx.cpp(35870): warning C4551: function call missing argument list
[43/177] Compiling C++ object sklearn/metrics/_pairwise_di...wise_distances_reduction__middle_term_computer.pyx.cpp.obj
sklearn/metrics/_pairwise_distances_reduction/_middle_term_computer.cp311-win_amd64.pyd.p/sklearn/metrics/_pairwise_distances_reduction/_middle_term_computer.pyx.cpp(42045): warning C4551: function call missing argument list
[44/177] Linking target sklearn/metrics/_pairwise_distances_reduction/_argkmin.cp311-win_amd64.pyd
   Creating library sklearn\metrics\_pairwise_distances_reduction\_argkmin.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_distances_reduction\_argkmin.cp311-win_amd64.exp
[45/177] Linking target sklearn/metrics/_pairwise_distances_reduction/_middle_term_computer.cp311-win_amd64.pyd
   Creating library sklearn\metrics\_pairwise_distances_reduction\_middle_term_computer.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_distances_reduction\_middle_term_computer.cp311-win_amd64.exp
[47/177] Compiling C++ object sklearn/metrics/_pairwise_di...airwise_distances_reduction__argkmin_classmode.pyx.cpp.obj
cl : Command line warning D9002 : ignoring unknown option '-fno-sized-deallocation'
sklearn/metrics/_pairwise_distances_reduction/_argkmin_classmode.cp311-win_amd64.pyd.p/sklearn/metrics/_pairwise_distances_reduction/_argkmin_classmode.pyx.cpp(29323): warning C4551: function call missing argument list
[49/177] Linking target sklearn/metrics/_pairwise_distances_reduction/_argkmin_classmode.cp311-win_amd64.pyd
   Creating library sklearn\metrics\_pairwise_distances_reduction\_argkmin_classmode.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_distances_reduction\_argkmin_classmode.cp311-win_amd64.exp
[50/177] Compiling C++ object sklearn/metrics/_pairwise_di...pairwise_distances_reduction__radius_neighbors.pyx.cpp.obj
sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors.cp311-win_amd64.pyd.p/sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors.pyx.cpp(38873): warning C4551: function call missing argument list
[52/177] Linking target sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors.cp311-win_amd64.pyd
   Creating library sklearn\metrics\_pairwise_distances_reduction\_radius_neighbors.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_distances_reduction\_radius_neighbors.cp311-win_amd64.exp
[57/177] Compiling C object sklearn/metrics/cluster/_expec...learn_metrics_cluster__expected_mutual_info_fast.pyx.c.obj
sklearn/metrics/cluster/_expected_mutual_info_fast.cp311-win_amd64.pyd.p/sklearn/metrics/cluster/_expected_mutual_info_fast.pyx.c(18720): warning C4244: 'function': conversion from 'Py_ssize_t' to 'double', possible loss of data
sklearn/metrics/cluster/_expected_mutual_info_fast.cp311-win_amd64.pyd.p/sklearn/metrics/cluster/_expected_mutual_info_fast.pyx.c(18720): warning C4244: 'function': conversion from 'Py_ssize_t' to 'double', possible loss of data
sklearn/metrics/cluster/_expected_mutual_info_fast.cp311-win_amd64.pyd.p/sklearn/metrics/cluster/_expected_mutual_info_fast.pyx.c(18720): warning C4244: 'function': conversion from 'Py_ssize_t' to 'double', possible loss of data
[58/177] Compiling C++ object sklearn/cluster/_dbscan_inne.../meson-generated_sklearn_cluster__dbscan_inner.pyx.cpp.obj
sklearn/cluster/_dbscan_inner.cp311-win_amd64.pyd.p/sklearn/cluster/_dbscan_inner.pyx.cpp(23107): warning C4551: function call missing argument list
[59/177] Compiling C++ object sklearn/metrics/_pairwise_di...istances_reduction__radius_neighbors_classmode.pyx.cpp.obj
sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors_classmode.cp311-win_amd64.pyd.p/sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors_classmode.pyx.cpp(32619): warning C4551: function call missing argument list
[60/177] Linking target sklearn/metrics/cluster/_expected_mutual_info_fast.cp311-win_amd64.pyd
   Creating library sklearn\metrics\cluster\_expected_mutual_info_fast.cp311-win_amd64.lib and object sklearn\metrics\cluster\_expected_mutual_info_fast.cp311-win_amd64.exp
[61/177] Linking target sklearn/cluster/_dbscan_inner.cp311-win_amd64.pyd
   Creating library sklearn\cluster\_dbscan_inner.cp311-win_amd64.lib and object sklearn\cluster\_dbscan_inner.cp311-win_amd64.exp
[62/177] Linking target sklearn/metrics/_pairwise_distances_reduction/_radius_neighbors_classmode.cp311-win_amd64.pyd
   Creating library sklearn\metrics\_pairwise_distances_reduction\_radius_neighbors_classmode.cp311-win_amd64.lib and object sklearn\metrics\_pairwise_distances_reduction\_radius_neighbors_classmode.cp311-win_amd64.exp
[64/177] Compiling C++ object sklearn/cluster/_hierarchica...n-generated_sklearn_cluster__hierarchical_fast.pyx.cpp.obj
sklearn/cluster/_hierarchical_fast.cp311-win_amd64.pyd.p/sklearn/cluster/_hierarchical_fast.pyx.cpp(23677): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/cluster/_hierarchical_fast.cp311-win_amd64.pyd.p/sklearn/cluster/_hierarchical_fast.pyx.cpp(23688): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/cluster/_hierarchical_fast.cp311-win_amd64.pyd.p/sklearn/cluster/_hierarchical_fast.pyx.cpp(23712): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/cluster/_hierarchical_fast.cp311-win_amd64.pyd.p/sklearn/cluster/_hierarchical_fast.pyx.cpp(24838): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/cluster/_hierarchical_fast.cp311-win_amd64.pyd.p/sklearn/cluster/_hierarchical_fast.pyx.cpp(24849): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/cluster/_hierarchical_fast.cp311-win_amd64.pyd.p/sklearn/cluster/_hierarchical_fast.pyx.cpp(33802): warning C4551: function call missing argument list
[65/177] Linking target sklearn/cluster/_hierarchical_fast.cp311-win_amd64.pyd
   Creating library sklearn\cluster\_hierarchical_fast.cp311-win_amd64.lib and object sklearn\cluster\_hierarchical_fast.cp311-win_amd64.exp
[68/177] Linking target sklearn/cluster/_k_means_lloyd.cp311-win_amd64.pyd
   Creating library sklearn\cluster\_k_means_lloyd.cp311-win_amd64.lib and object sklearn\cluster\_k_means_lloyd.cp311-win_amd64.exp
[72/177] Linking target sklearn/cluster/_k_means_elkan.cp311-win_amd64.pyd
   Creating library sklearn\cluster\_k_means_elkan.cp311-win_amd64.lib and object sklearn\cluster\_k_means_elkan.cp311-win_amd64.exp
[73/177] Linking target sklearn/cluster/_k_means_common.cp311-win_amd64.pyd
   Creating library sklearn\cluster\_k_means_common.cp311-win_amd64.lib and object sklearn\cluster\_k_means_common.cp311-win_amd64.exp
[74/177] Linking target sklearn/cluster/_k_means_minibatch.cp311-win_amd64.pyd
   Creating library sklearn\cluster\_k_means_minibatch.cp311-win_amd64.lib and object sklearn\cluster\_k_means_minibatch.cp311-win_amd64.exp
[76/177] Linking target sklearn/cluster/_hdbscan/_linkage.cp311-win_amd64.pyd
   Creating library sklearn\cluster\_hdbscan\_linkage.cp311-win_amd64.lib and object sklearn\cluster\_hdbscan\_linkage.cp311-win_amd64.exp
[85/177] Linking target sklearn/cluster/_hdbscan/_reachability.cp311-win_amd64.pyd
   Creating library sklearn\cluster\_hdbscan\_reachability.cp311-win_amd64.lib and object sklearn\cluster\_hdbscan\_reachability.cp311-win_amd64.exp
[88/177] Linking target sklearn/decomposition/_online_lda_fast.cp311-win_amd64.pyd
   Creating library sklearn\decomposition\_online_lda_fast.cp311-win_amd64.lib and object sklearn\decomposition\_online_lda_fast.cp311-win_amd64.exp
[92/177] Linking target sklearn/decomposition/_cdnmf_fast.cp311-win_amd64.pyd
   Creating library sklearn\decomposition\_cdnmf_fast.cp311-win_amd64.lib and object sklearn\decomposition\_cdnmf_fast.cp311-win_amd64.exp
[93/177] Linking target sklearn/ensemble/_hist_gradient_boosting/_gradient_boosting.cp311-win_amd64.pyd
   Creating library sklearn\ensemble\_hist_gradient_boosting\_gradient_boosting.cp311-win_amd64.lib and object sklearn\ensemble\_hist_gradient_boosting\_gradient_boosting.cp311-win_amd64.exp
[95/177] Linking target sklearn/cluster/_hdbscan/_tree.cp311-win_amd64.pyd
   Creating library sklearn\cluster\_hdbscan\_tree.cp311-win_amd64.lib and object sklearn\cluster\_hdbscan\_tree.cp311-win_amd64.exp
[98/177] Linking target sklearn/ensemble/_hist_gradient_boosting/histogram.cp311-win_amd64.pyd
   Creating library sklearn\ensemble\_hist_gradient_boosting\histogram.cp311-win_amd64.lib and object sklearn\ensemble\_hist_gradient_boosting\histogram.cp311-win_amd64.exp
[99/177] Linking target sklearn/ensemble/_gradient_boosting.cp311-win_amd64.pyd
   Creating library sklearn\ensemble\_gradient_boosting.cp311-win_amd64.lib and object sklearn\ensemble\_gradient_boosting.cp311-win_amd64.exp
[103/177] Linking target sklearn/ensemble/_hist_gradient_boosting/splitting.cp311-win_amd64.pyd
   Creating library sklearn\ensemble\_hist_gradient_boosting\splitting.cp311-win_amd64.lib and object sklearn\ensemble\_hist_gradient_boosting\splitting.cp311-win_amd64.exp
[107/177] Linking target sklearn/datasets/_svmlight_format_fast.cp311-win_amd64.pyd
   Creating library sklearn\datasets\_svmlight_format_fast.cp311-win_amd64.lib and object sklearn\datasets\_svmlight_format_fast.cp311-win_amd64.exp
[108/177] Linking target sklearn/ensemble/_hist_gradient_boosting/_binning.cp311-win_amd64.pyd
   Creating library sklearn\ensemble\_hist_gradient_boosting\_binning.cp311-win_amd64.lib and object sklearn\ensemble\_hist_gradient_boosting\_binning.cp311-win_amd64.exp
[112/177] Linking target sklearn/ensemble/_hist_gradient_boosting/_predictor.cp311-win_amd64.pyd
   Creating library sklearn\ensemble\_hist_gradient_boosting\_predictor.cp311-win_amd64.lib and object sklearn\ensemble\_hist_gradient_boosting\_predictor.cp311-win_amd64.exp
[115/177] Linking target sklearn/ensemble/_hist_gradient_boosting/_bitset.cp311-win_amd64.pyd
   Creating library sklearn\ensemble\_hist_gradient_boosting\_bitset.cp311-win_amd64.lib and object sklearn\ensemble\_hist_gradient_boosting\_bitset.cp311-win_amd64.exp
[118/177] Linking target sklearn/ensemble/_hist_gradient_boosting/common.cp311-win_amd64.pyd
   Creating library sklearn\ensemble\_hist_gradient_boosting\common.cp311-win_amd64.lib and object sklearn\ensemble\_hist_gradient_boosting\common.cp311-win_amd64.exp
[120/177] Linking target sklearn/feature_extraction/_hashing_fast.cp311-win_amd64.pyd
   Creating library sklearn\feature_extraction\_hashing_fast.cp311-win_amd64.lib and object sklearn\feature_extraction\_hashing_fast.cp311-win_amd64.exp
[126/177] Linking target sklearn/linear_model/_sgd_fast.cp311-win_amd64.pyd
   Creating library sklearn\linear_model\_sgd_fast.cp311-win_amd64.lib and object sklearn\linear_model\_sgd_fast.cp311-win_amd64.exp
[127/177] Compiling C object sklearn/manifold/_utils.cp311...64.pyd.p/meson-generated_sklearn_manifold__utils.pyx.c.obj
sklearn/manifold/_utils.cp311-win_amd64.pyd.p/sklearn/manifold/_utils.pyx.c(20845): warning C4305: '=': truncation from 'double' to 'float'
sklearn/manifold/_utils.cp311-win_amd64.pyd.p/sklearn/manifold/_utils.pyx.c(20854): warning C4305: '=': truncation from 'double' to 'float'
[128/177] Linking target sklearn/manifold/_utils.cp311-win_amd64.pyd
   Creating library sklearn\manifold\_utils.cp311-win_amd64.lib and object sklearn\manifold\_utils.cp311-win_amd64.exp
[129/177] Compiling C object sklearn/manifold/_barnes_hut_...eson-generated_sklearn_manifold__barnes_hut_tsne.pyx.c.obj
sklearn/manifold/_barnes_hut_tsne.cp311-win_amd64.pyd.p/sklearn/manifold/_barnes_hut_tsne.pyx.c(22163): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 1 has type 'Py_ssize_t'
sklearn/manifold/_barnes_hut_tsne.cp311-win_amd64.pyd.p/sklearn/manifold/_barnes_hut_tsne.pyx.c(22163): note: consider using '%lli' in the format string
sklearn/manifold/_barnes_hut_tsne.cp311-win_amd64.pyd.p/sklearn/manifold/_barnes_hut_tsne.pyx.c(22163): note: consider using '%Ii' in the format string
sklearn/manifold/_barnes_hut_tsne.cp311-win_amd64.pyd.p/sklearn/manifold/_barnes_hut_tsne.pyx.c(22163): note: consider using '%I64i' in the format string
[131/177] Linking target sklearn/manifold/_barnes_hut_tsne.cp311-win_amd64.pyd
   Creating library sklearn\manifold\_barnes_hut_tsne.cp311-win_amd64.lib and object sklearn\manifold\_barnes_hut_tsne.cp311-win_amd64.exp
[133/177] Linking target sklearn/linear_model/_sag_fast.cp311-win_amd64.pyd
   Creating library sklearn\linear_model\_sag_fast.cp311-win_amd64.lib and object sklearn\linear_model\_sag_fast.cp311-win_amd64.exp
[134/177] Linking target sklearn/linear_model/_cd_fast.cp311-win_amd64.pyd
   Creating library sklearn\linear_model\_cd_fast.cp311-win_amd64.lib and object sklearn\linear_model\_cd_fast.cp311-win_amd64.exp
[136/177] Linking target sklearn/neighbors/_partition_nodes.cp311-win_amd64.pyd
   Creating library sklearn\neighbors\_partition_nodes.cp311-win_amd64.lib and object sklearn\neighbors\_partition_nodes.cp311-win_amd64.exp
[138/177] Linking target sklearn/_loss/_loss.cp311-win_amd64.pyd
   Creating library sklearn\_loss\_loss.cp311-win_amd64.lib and object sklearn\_loss\_loss.cp311-win_amd64.exp
[139/177] Compiling Cython source sklearn/neighbors/_ball_tree.pyx
warning: sklearn\neighbors\_binary_tree.pxi:1092:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:1958:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:2053:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:2222:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:2345:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:2402:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:2403:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:2728:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:3594:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:3689:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:3858:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:3981:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:4038:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:4039:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_ball_tree.pyx:105:9: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_ball_tree.pyx:107:9: Assigning to 'float64_t *' from 'const float64_t *' discards const qualifier
warning: sklearn\neighbors\_ball_tree.pyx:308:9: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_ball_tree.pyx:310:9: Assigning to 'float32_t *' from 'const float32_t *' discards const qualifier
[140/177] Compiling Cython source sklearn/neighbors/_kd_tree.pyx
warning: sklearn\neighbors\_binary_tree.pxi:1092:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:1958:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:2053:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:2222:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:2345:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:2402:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:2403:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:2728:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:3594:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:3689:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:3858:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:3981:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:4038:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_binary_tree.pxi:4039:13: Assigning to 'intp_t *' from 'const intp_t *' discards const qualifier
warning: sklearn\neighbors\_kd_tree.pyx:74:9: Assigning to 'float64_t *' from 'const float64_t *' discards const qualifier
warning: sklearn\neighbors\_kd_tree.pyx:75:9: Assigning to 'float64_t *' from 'const float64_t *' discards const qualifier
warning: sklearn\neighbors\_kd_tree.pyx:342:9: Assigning to 'float32_t *' from 'const float32_t *' discards const qualifier
warning: sklearn\neighbors\_kd_tree.pyx:343:9: Assigning to 'float32_t *' from 'const float32_t *' discards const qualifier
[148/177] Compiling C object sklearn/neighbors/_quad_tree....d.p/meson-generated_sklearn_neighbors__quad_tree.pyx.c.obj
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25472): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 1 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25472): note: consider using '%lli' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25472): note: consider using '%Ii' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25472): note: consider using '%I64i' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 1 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): note: consider using '%lli' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): note: consider using '%Ii' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): note: consider using '%I64i' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 2 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): note: consider using '%lli' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): note: consider using '%Ii' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25586): note: consider using '%I64i' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25683): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 1 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25683): note: consider using '%lli' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25683): note: consider using '%Ii' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(25683): note: consider using '%I64i' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 1 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): note: consider using '%lli' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): note: consider using '%Ii' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): note: consider using '%I64i' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 2 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): note: consider using '%lli' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): note: consider using '%Ii' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26270): note: consider using '%I64i' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 4 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): note: consider using '%lli' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): note: consider using '%Ii' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): note: consider using '%I64i' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 11 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): note: consider using '%lli' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): note: consider using '%Ii' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26765): note: consider using '%I64i' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 3 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): note: consider using '%lli' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): note: consider using '%Ii' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): note: consider using '%I64i' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 8 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): note: consider using '%lli' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): note: consider using '%Ii' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(26793): note: consider using '%I64i' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28020): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 1 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28020): note: consider using '%lli' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28020): note: consider using '%Ii' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28020): note: consider using '%I64i' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28139): warning C4477: 'printf' : format string '%li' requires an argument of type 'long', but variadic argument 1 has type '__pyx_t_7sklearn_5utils_9_typedefs_intp_t'
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28139): note: consider using '%lli' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28139): note: consider using '%Ii' in the format string
sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_quad_tree.pyx.c(28139): note: consider using '%I64i' in the format string
[149/177] Linking target sklearn/svm/_liblinear.cp311-win_amd64.pyd
   Creating library sklearn\svm\_liblinear.cp311-win_amd64.lib and object sklearn\svm\_liblinear.cp311-win_amd64.exp
[151/177] Linking target sklearn/neighbors/_quad_tree.cp311-win_amd64.pyd
   Creating library sklearn\neighbors\_quad_tree.cp311-win_amd64.lib and object sklearn\neighbors\_quad_tree.cp311-win_amd64.exp
[154/177] Linking target sklearn/preprocessing/_csr_polynomial_expansion.cp311-win_amd64.pyd
   Creating library sklearn\preprocessing\_csr_polynomial_expansion.cp311-win_amd64.lib and object sklearn\preprocessing\_csr_polynomial_expansion.cp311-win_amd64.exp
[156/177] Linking target sklearn/tree/_splitter.cp311-win_amd64.pyd
   Creating library sklearn\tree\_splitter.cp311-win_amd64.lib and object sklearn\tree\_splitter.cp311-win_amd64.exp
[159/177] Linking target sklearn/svm/_libsvm.cp311-win_amd64.pyd
   Creating library sklearn\svm\_libsvm.cp311-win_amd64.lib and object sklearn\svm\_libsvm.cp311-win_amd64.exp
[160/177] Compiling C++ object sklearn/preprocessing/_targ...ted_sklearn_preprocessing__target_encoder_fast.pyx.cpp.obj
sklearn/preprocessing/_target_encoder_fast.cp311-win_amd64.pyd.p/sklearn/preprocessing/_target_encoder_fast.pyx.cpp(39805): warning C4551: function call missing argument list
[161/177] Linking target sklearn/svm/_libsvm_sparse.cp311-win_amd64.pyd
   Creating library sklearn\svm\_libsvm_sparse.cp311-win_amd64.lib and object sklearn\svm\_libsvm_sparse.cp311-win_amd64.exp
[162/177] Linking target sklearn/preprocessing/_target_encoder_fast.cp311-win_amd64.pyd
   Creating library sklearn\preprocessing\_target_encoder_fast.cp311-win_amd64.lib and object sklearn\preprocessing\_target_encoder_fast.cp311-win_amd64.exp
[164/177] Compiling C object sklearn/neighbors/_ball_tree....d.p/meson-generated_sklearn_neighbors__ball_tree.pyx.c.obj
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(24810): warning C4244: 'function': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to 'double', possible loss of data
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(32767): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(40182): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(40735): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(40979): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(41262): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(41271): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(41641): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(42252): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(42655): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(42665): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(46580): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(54004): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(54557): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(54801): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(55084): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(55093): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(55463): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(56074): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(56477): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(56487): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(58364): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(58387): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(59739): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_ball_tree.pyx.c(59762): warning C4090: '=': different 'const' qualifiers
[165/177] Linking target sklearn/neighbors/_ball_tree.cp311-win_amd64.pyd
   Creating library sklearn\neighbors\_ball_tree.cp311-win_amd64.lib and object sklearn\neighbors\_ball_tree.cp311-win_amd64.exp
[166/177] Compiling C object sklearn/neighbors/_kd_tree.cp...pyd.p/meson-generated_sklearn_neighbors__kd_tree.pyx.c.obj
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(24678): warning C4244: 'function': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to 'double', possible loss of data
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(32635): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(40050): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(40603): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(40847): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(41130): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(41139): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(41509): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(42120): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(42523): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(42533): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(46448): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(53872): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(54425): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(54669): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(54952): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(54961): warning C4244: '=': conversion from 'const __pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(55331): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(55942): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(56345): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(56355): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(58229): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(58241): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(60038): warning C4090: '=': different 'const' qualifiers
sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd.p/sklearn/neighbors/_kd_tree.pyx.c(60050): warning C4090: '=': different 'const' qualifiers
[168/177] Linking target sklearn/neighbors/_kd_tree.cp311-win_amd64.pyd
   Creating library sklearn\neighbors\_kd_tree.cp311-win_amd64.lib and object sklearn\neighbors\_kd_tree.cp311-win_amd64.exp
[169/177] Compiling C object sklearn/tree/_partitioner.cp3....pyd.p/meson-generated_sklearn_tree__partitioner.pyx.c.obj
sklearn/tree/_partitioner.cp311-win_amd64.pyd.p/sklearn/tree/_partitioner.pyx.c(24489): warning C4244: 'function': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to 'double', possible loss of data
sklearn/tree/_partitioner.cp311-win_amd64.pyd.p/sklearn/tree/_partitioner.pyx.c(24489): warning C4244: 'function': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to 'double', possible loss of data
sklearn/tree/_partitioner.cp311-win_amd64.pyd.p/sklearn/tree/_partitioner.pyx.c(26110): warning C4244: 'function': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to 'double', possible loss of data
sklearn/tree/_partitioner.cp311-win_amd64.pyd.p/sklearn/tree/_partitioner.pyx.c(30951): warning C4305: '=': truncation from 'double' to '__pyx_t_7sklearn_5utils_9_typedefs_float32_t'
[170/177] Linking target sklearn/tree/_partitioner.cp311-win_amd64.pyd
   Creating library sklearn\tree\_partitioner.cp311-win_amd64.lib and object sklearn\tree\_partitioner.cp311-win_amd64.exp
[173/177] Linking target sklearn/tree/_criterion.cp311-win_amd64.pyd
   Creating library sklearn\tree\_criterion.cp311-win_amd64.lib and object sklearn\tree\_criterion.cp311-win_amd64.exp
[175/177] Linking target sklearn/tree/_utils.cp311-win_amd64.pyd
   Creating library sklearn\tree\_utils.cp311-win_amd64.lib and object sklearn\tree\_utils.cp311-win_amd64.exp
[176/177] Compiling C++ object sklearn/tree/_tree.cp311-win_amd64.pyd.p/meson-generated_sklearn_tree__tree.pyx.cpp.obj
sklearn/tree/_tree.cp311-win_amd64.pyd.p/sklearn/tree/_tree.pyx.cpp(28907): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
sklearn/tree/_tree.cp311-win_amd64.pyd.p/sklearn/tree/_tree.pyx.cpp(33179): warning C4244: '=': conversion from '__pyx_t_7sklearn_5utils_9_typedefs_intp_t' to '__pyx_t_7sklearn_5utils_9_typedefs_float64_t', possible loss of data
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
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn (main)
$ history > command_history.txt
(tutorial-env)
sinha@Sinha MINGW64 /c/repos/Building from source/scikit-learn (main)
$ ls
asv_benchmarks/      build_tools/         CONTRIBUTING.md  maint_tools/    README.rst   sklearn-env/
azure-pipelines.yml  CITATION.cff         COPYING          Makefile        SECURITY.md  tutorial-env/
benchmarks/          CODE_OF_CONDUCT.md   doc/             meson.build     setup.cfg
build/               command_history.txt  examples/        pyproject.toml  sklearn/

