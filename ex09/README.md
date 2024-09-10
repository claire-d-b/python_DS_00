# en gros le setup.py il va regarder le sous fichier init et deduire qu'il s'agit d'un module

# ensuite il va créer un tgz avec le nom du dossier local

# si t'installes pas le tgz il reconnaitra pas l'import si le fichier local porte un autre nom

# First, we create a directory and give it a package name, preferably related to

# its operation. Then we put the classes and the required functions in it.

# Finally we create an **init**.py file inside the directory, to let Python

# know that the directory is a package.

pip install --upgrade setuptools wheel

# Generate Distribution Archive

# This command will create a dist/ directory containing a .tar.gz file,

# which is your distribution archive.

python setup.py sdist
pip install ./dist/ft_package-0.0.1.tar.gz

# Generate Wheel Distribution

# This command will create a dist/ directory containing a .whl file,

# which is your wheel distribution archive.

python setup.py bdist_wheel
pip install ./dist/ft_package-0.0.1-py3-none-any.whl

# Difference between both : standard source distribution archive sdist

# (cross-platform, Python compiles the code during installation) VS

# binary distribution format called a wheel (faster installation,

# platform specific, skips the build step and directly unpacks the pre-built files)

pip list
pip install .
pip show -v ft_package

deactivate
