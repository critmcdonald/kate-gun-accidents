# Kate's Gun Violence story

Testing various geocoding techniques.

- The first test uses [MapChi](https://rdrr.io/github/dmwelgus/MapChi/) which gets us about half the zip codes and none of the tract informaiton.
- The second test was to use [censusr](https://cran.r-project.org/web/packages/censusr/censusr.pdf) and older package that _might_ get us tract info. It's been deprecated in favor of [tidycensus](https://walkerke.github.io/tidycensus/articles/basic-usage.html), but that package doesn't appear to have the same geo coding function. I couldn't get a good request.
- [geocodio](https://geocod.io) is an online tool that gave great results, including the census information we were lookiing for. There is an [rgeocodio](https://github.com/hrbrmstr/rgeocodio) but I've yet to look at it.
- Will try [tigris]

The example I want to try:

```r
airports <- dplyr::data_frame(
  street = "700 Catalina Dr", city = "Daytona Beach", state = "FL"
)

append_geoid(airports, 'tr')
```

## Pubished notebooks

- [01-clean](https://critmcdonald.github.io/kate-gun-accidents/01-clean.html)
- [02-mapchi](https://critmcdonald.github.io/kate-gun-accidents/02-mapchi.html)
- [02-censusr](https://critmcdonald.github.io/kate-gun-accidents/02-censusr.html)
- [02-geocodio](https://critmcdonald.github.io/kate-gun-accidents/02-geocodio.html)

