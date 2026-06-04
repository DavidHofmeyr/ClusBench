# ClusBench

A repository of synthetic data sets for benchmarking clustering methods.
The data were derived from data sets primarily used for classification. A
modified Kernel Density Estimate (KDE) which uses local statistics computed
from nearest neighbours was fit to each underlying data set, and then ten
samples, each of size 5000, were generated from each fitted distribution.
In addition, when class proportions were unbalanced, an additional ten
data sets of size 5000, but in which the class priors were set equal for
all classes, were generated. The suffix "_original" means class priors
match the class proportions in the underlying data set and "_equal" refers
to the modified, uniform class priors. Finally, data sets which were unreasonably
difficult to cluster were then removed. This means that some data sets will
only have an "_equal" variant, while others may only have an "_original" variant.

See DATA_PROVENANCE for resources.

## Installing the R package
To install and load the package from within R:
```{r}
install.packages("https://github.com/DavidHofmeyr/ClusBench/raw/refs/heads/master/ClusBench_0.1.0.tar.gz",
  type = "source", repos = NULL)
library(ClusBench)
help(ClusBench)
```

The main functions in the package are `{r} get_data`

## More
A paper will be uploaded soon to ArXiV with more details on the data and the package. Please cite the paper (once available) if using the package and/or repository.
