# Installation and Setup

## Installation

The package can be installed by enabling the [“ropensci”
r-universe](https://ropensci.r-universe.dev), and using
[`install.packages()`](https://rdrr.io/r/utils/install.packages.html):

``` r

options (repos = c (
    ropensci = "https://ropensci.r-universe.dev",
    CRAN = "https://cloud.r-project.org"
))
install.packages ("deposits")
```

Alternatively, the package can be installed directly from GitHub with
the following command:

``` r

remotes::install_github ("ropenscilabs/deposits")
```

The package can then be loaded for use with:

``` r

library (deposits)
```

## Setup: API Tokens

All services require users to create an account and then to generate API
(“Application Programming Interface”) tokens. Click on the following
links to generate tokens, also listed as sequences of menu items used to
reach token settings:

- [zenodo/account/settings/applications/tokens/new](https://zenodo.org/account/settings/applications/tokens/new/)
- [zenodo-sandbox/account/settings/applications/tokens/new](https://sandbox.zenodo.org/account/settings/applications/tokens/new/),
- [figshare/account/applications](https://figshare.com/account/applications).

It is not necessary to create or register applications on any of these
services; this package uses personal tokens only. The tokens need to be
stored as local environment variables the names of which must include
the names of the respective services, as defined by the “name” column
returned from `deposits_service()`, as shown above. This can be done as
in the following example:

``` r

Sys.setenv ("ZENODO_SANDBOX_TOKEN" = "<my-token")
```

Alternatively, these tokens can be stored in a `~/.Renviron` file, where
they will be automatically loaded into every R session.
