# r-conda

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/betatim/r-conda/master?urlpath=rstudio)

> R and RStudio in repo2docker without waiting for packages to compile!

Jupyter+R: [![Binder](http://mybinder.org/badge_logo.svg)](http://mybinder.org/v2/gh/binder-examples/r-conda/master?filepath=index.ipynb)

RStudio: [![Binder](http://mybinder.org/badge_logo.svg)](http://mybinder.org/v2/gh/binder-examples/r-conda/master?urlpath=rstudio)

Binder supports using R and RStudio, with libraries pinned to a specific versions.

Install R itself and your required R packages via conda packages. Installing conda packages is faster than
installing CRAN packages. This is because CRAN packages need compiling during the install process and conda
packages do not.

For some R packages there is no corresponding conda-forge package yet, in that case take a look at https://github.com/binder-examples/r. Note that these two approaches cannot be combined, so you cannot install R packages via Conda and via an `install.R` file at the same time. You can check if a required R package is available on the Conda Forge website at https://conda-forge.org/feedstocks/ by searching for `r-PACKAGENAME`. You can install R packges from other sources using a `postBuild` script.

Both [RStudio](https://www.rstudio.com/) and [IRKernel](https://irkernel.github.io/)
are installed by default, so you can use either the Jupyter notebook interface or
the RStudio interface.
