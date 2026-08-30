# Write an empty metadata template to local file

The fields are those defined by the Dublin Core Metadata Initiative
(DCMI), defined at
<https://www.dublincore.org/specifications/dublin-core/dcmi-terms/>. The
template produced by this function is in `json` format which can be
manually edited to provide metadata for a deposit.

## Usage

``` r
deposits_metadata_template(filename = NULL)
```

## Arguments

- filename:

  Name or full path to local file where template is to be written. This
  file will be created. If a file of that name already exists, it must
  first be deleted. The file extension '.json' will be automatically
  appended.

## Value

(Invisibly) `TRUE` if local file successfully created; otherwise
`FALSE`.

## See also

Other meta:
[`dcmi_terms()`](https://docs.ropensci.org/deposits/reference/dcmi_terms.md),
[`figshare_categories()`](https://docs.ropensci.org/deposits/reference/figshare_categories.md)

## Examples

``` r
filename <- tempfile (fileext = ".json")
deposits_metadata_template (filename)
#> Edit the file [/tmp/RtmpnTxfh9/file5ab73d63f24.json] and remove everything except the metadata fields you require.
#> The filename may be then passed as the 'metadata' argument to a 'deposits' client.
# then edit that file to complete metadata
```
