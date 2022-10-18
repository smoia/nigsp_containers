NiGSP - containers
==================

Former-Singularity-now-Apptainer containers to run NiGSP related things, e.g. preprocessing.

When building them, if the `/tmp` directory isn't doing great (cause maybe allocated space isn't much, or there's no access), declare a temporary folder where their unsquashed sif image can be stored (sif images can be big, unsquashed they become huge, like 2-3x):

```shell
export APPTAINER_TMPDIR=/path/to/build/tmp/dir
apptainer build image.sif image.def
```

Remember to check that the chosen folder is empty and temporary building file are removed after building is over.

