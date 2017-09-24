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

 4. Install toolchains for Cray, Intel and GNU compilers

In the ec_cray directory
```
eb --toolchain-name=dummy easyconfigs/CrayIntel-2017.06.eb
eb --toolchain-name=dummy easyconfigs/CrayCCE-2017.06.eb
eb --toolchain-name=dummy easyconfigs/CrayGNU-2017.06.eb
```

## Creating an easybuild config

 1. Find a suitable configuration file (.eb file) and use it as a template
 2. Adapt toolchain and other settings in .eb file, as required

## Building 

```
eb package-pkgversion-toolchain-toolchainversion.eb --robot
```

E.g.,  
```
eb gnuplot-4.6.0-CrayGNU-1.4.10.eb --robot
```

