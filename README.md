# VOT Corpora

This package collects a number of small VOT corpora from different sources:

* Baese-Berk & Goldrick (2009) experiment 1 measured voice onset time for
  monosyllabic words with word-initial voiceless stops. Some words had voiced
  minimal pair, while others did not. Words were read in isolation with other
  monosyllabic fillers that did not have initial stops. Experiment 1a only had
  /p/-initial words, and Experiment 1b had /t/ and /k/.  Supported by National
  Institutes of Health Grant DC0079772

* Goldrick, Vaughn, & Murphy (2013), experiment 1 is analogous to Baese-Berk &
  Goldrick (2009) but with voiced stops.  Supported by National Science
  Foundation Grant BCS0846147

* Lev-Ari, S., & Peperkamp, S. (2013). English-French bilinguals (English L1)
  read 16 sentences, 10 of which contained one word each starting with /p/, /t/,
  and /k/. (Items are the English sentences from Fowler, Sramkoc, Ostrya,
  Rowlanda, & Halle, 2008). A subset of the talkers also conducted interviews,
  from which VOTs of all word-initial voiceless stops were measured.

* Buckeye (Nelson, N. & Wedel, A., _e-pub ahead of print_). VOTs
  automatically annotated from word-initial voice and voiceless stops in the
  Buckeye Corpus of conversational speech by Andy Wedel and Noah Nelson.  Age is
  coded as old (40+) or young (under 40).  Includes stop length and local speech
  rate information, but no pre-voiced tokens.

The first two are from isolated word list reading, the third from sentences and
conversational speech and the fourth from conversational speech. All are from
English monolinguals except for the Lev-Ari data, which is from L1 English, L2
French speakers who live in France and speak French primarily. The Buckeye,
Lev-Ari, and Goldrick et al. (2013) have speaker sex coded, and Buckeye and
Lev-Ari have age (Buckeye only as older/younger than 40).

__The only corpus that has both voiced and voiceless stops for each talker is the
Buckeye data.__

# Installation

```r
devtools::install_github("kleinschmidt/votcorpora")
```

# Usage

``` r
library(votcorpora)
vot
#> # A tibble: 14,262 x 14
#>    sour… subj… phon…   vot prev… word  sex     age age_… bili… spee… stop…
#>    <chr> <chr> <fct> <dbl> <lgl> <chr> <chr> <dbl> <chr> <lgl> <dbl> <dbl>
#>  1 leva… la_1  k      52.0 NA    keep… f      47.0 o     T        NA    NA
#>  2 leva… la_1  k      42.0 NA    cove… f      47.0 o     T        NA    NA
#>  3 leva… la_1  k      75.0 NA    carr… f      47.0 o     T        NA    NA
#>  4 leva… la_1  k      54.0 NA    cavi… f      47.0 o     T        NA    NA
#>  5 leva… la_1  k      57.0 NA    kate  f      47.0 o     T        NA    NA
#>  6 leva… la_1  k      58.0 NA    car   f      47.0 o     T        NA    NA
#>  7 leva… la_1  k      50.0 NA    comf… f      47.0 o     T        NA    NA
#>  8 leva… la_1  k      54.0 NA    Kayla f      47.0 o     T        NA    NA
#>  9 leva… la_1  k      61.0 NA    call… f      47.0 o     T        NA    NA
#> 10 leva… la_1  k      55.0 NA    caug… f      47.0 o     T        NA    NA
#> # ... with 14,252 more rows, and 2 more variables: voicing <fctr>,
#> #   place <fctr>
```

See the vignette for more details.

## Citation

This package contains citation information.  To get this within R:

``` r
citation("votcorpora")
#> 
#>   Goldrick, M., Vaughn, C., & Murphy, A. (2013). The effects of
#>   lexical neighbors on stop consonant articulation. The Journal of
#>   the Acoustical Society of America, 134(2), EL172-7.
#>   https://doi.org/10.1121/1.4812821
#> 
#>   Baese-Berk, M., & Goldrick, M. (2009). Mechanisms of interaction
#>   in speech production. Language and Cognitive Processes, 24(4),
#>   527–554. https://doi.org/10.1080/01690960802299378
#> 
#>   Nelson, N. R., & Wedel, A. (2017). The phonetic specificity of
#>   competition: Contrastive hyperarticulation of voice onset time
#>   in conversational English. Journal of Phonetics, e-pub, 1–20.
#>   https://doi.org/10.1016/j.wocn.2017.01.008
#> 
#>   Lev-Ari, S., & Peperkamp, S. (2013). Low inhibitory skill leads
#>   to non-native perception and production in bilinguals’ native
#>   language. Journal of Phonetics, 41(5), 320–331.
#>   https://doi.org/10.1016/j.wocn.2013.06.002
#> 
#> To see these entries in BibTeX format, use 'print(<citation>,
#> bibtex=TRUE)', 'toBibtex(.)', or set
#> 'options(citation.bibtex.max=999)'.
```
