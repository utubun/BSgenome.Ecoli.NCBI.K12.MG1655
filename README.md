
# BSgenome.Ecoli.NCBI.K12.MG1655

<!-- badges: start -->
[![Lifecycle: stable](https://img.shields.io/badge/lifecycle-stable-brightgreen.svg)](https://lifecycle.r-lib.org/articles/stages.html#stable)
<!-- badges: end -->

The package provides a full genome assembly of *E. coli* str. K12, substr. MG1655. Data source [NCBI](https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/000/005/845/GCF_000005845.2_ASM584v2/) 

## Installation

You can install the development version of BSgenome.Ecoli.NCBI.K12.MG1655 from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("utubun/BSgenome.Ecoli.NCBI.K12.MG1655")
```

## Example

Load *E.coli* genome, and assign it to the variable `genome`:

``` r
library(BSgenome.Ecoli.NCBI.K12.MG1655)

genome <- BSgenome.Ecoli.NCBI.K12.MG1655
```

Get the information about the genome:

``` r
sprintf(
  'Genome:\t%s\nName:\t%s\nOrganism:\t%s\nProvider:\t%s\nReleased:\t%s',
  sapply(c(bsgenomeName, commonName, organism, provider, releaseDate), \(f) {f(genome)})
)
```

List the methods available for the genome:

``` r
methods(class = class(genome))
```

## More examples

``` r
vignette("GenomeSearching", package="BSgenome")
```
