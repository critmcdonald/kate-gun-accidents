# Kate's Gun Violence story

Testing various geocoding techniques.

The first test uses [MapChi]() which gets us about half the zip codes and none of the tract informaiton.

The next test will be using [censusr](https://cran.r-project.org/web/packages/censusr/censusr.pdf) and older package that _might_ get us tract info. It's been deprecated in favor of [tidycensus](), but that package doesn't appear to have the same geo coding function.

The example I want to try:

```r
airports <- dplyr::data_frame(
  street = "700 Catalina Dr", city = "Daytona Beach", state = "FL"
)

append_geoid(airports, 'tr')
```

## Pubished notebooks

- [01-clean](https://critmcdonald.github.io/kate-gun-accidents/01-clean.html)
- [02-mapchi-test](https://critmcdonald.github.io/kate-gun-accidents/02-mapchi-test.html)
