# eb_cray
EasyBuild configs for the Cray platform

## Installing EasyBuild

```
EASYBUILD_PREFIX=$HOME/easybuild
curl -O https://raw.githubusercontent.com/easybuilders/easybuild-framework/develop/easybuild/scripts/bootstrap_eb.py
python bootstrap_eb.py $EASYBUILD_PREFIX
module use $EASYBUILD_PREFIX/modules/all
module load EasyBuild
```


