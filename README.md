# eb_cray
EasyBuild configs for the Cray platform

## Installing EasyBuild

Find detailed instructions at  http://easybuild.readthedocs.io/en/latest/Installation.html. 

 1. Set EASYBUILD_PREFIX

```
export EASYBUILD_PREFIX=$HOME/easybuild
```

 2. Download and install the code 
```
curl -O https://raw.githubusercontent.com/easybuilders/easybuild-framework/develop/easybuild/scripts/bootstrap_eb.py
python bootstrap_eb.py $EASYBUILD_PREFIX
```

 3. Put this in your .bashrc
```
export EASYBUILD_MODULES_TOOL=EnvironmentModulesC
export EASYBUILD_MODULE_SYNTAX=Tcl
export EASYBUILD_PREFIX=$HOME/easybuild
export EASYBUILD_OPTARCH=broadwell
module use $EASYBUILD_PREFIX/modules/all
module load EasyBuild
```
## Creating an easybuild config


