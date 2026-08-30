# Retrieve a token for a specified deposits service.

Tokens should be stored as local environment variables, optionally
defined in a `~/.Renviron` file, and should contain the name of the
desired deposits service.

## Usage

``` r
get_deposits_token(service = NULL, sandbox = FALSE)
```

## Arguments

- service:

  Name of desired service; must be a value in the "name" column of
  [deposits_services](https://docs.ropensci.org/deposits/reference/deposits_services.md).

- sandbox:

  If `TRUE`, retrieve token for sandbox, rather than actual API.

## Value

API token for nominated service.

## Examples

``` r
if (FALSE) { # \dontrun{
token <- get_deposits_token (service = "figshare")
} # }
```
