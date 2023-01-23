---
title: Sgkit is awesome
keywords:
- markdown
- publishing
- manubot
lang: en-US
date-meta: '2023-01-23'
author-meta:
- Tom White
- Jane Roe
header-includes: |
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta property="og:type" content="article" />
  <meta name="dc.title" content="Sgkit is awesome" />
  <meta name="citation_title" content="Sgkit is awesome" />
  <meta property="og:title" content="Sgkit is awesome" />
  <meta property="twitter:title" content="Sgkit is awesome" />
  <meta name="dc.date" content="2023-01-23" />
  <meta name="citation_publication_date" content="2023-01-23" />
  <meta property="article:published_time" content="2023-01-23" />
  <meta name="dc.modified" content="2023-01-23T17:21:51+00:00" />
  <meta property="article:modified_time" content="2023-01-23T17:21:51+00:00" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="Tom White" />
  <meta name="citation_author_institution" content="TWC" />
  <meta name="citation_author_orcid" content="XXXX-XXXX-XXXX-XXXX" />
  <meta name="twitter:creator" content="@tom_e_white" />
  <meta name="citation_author" content="Jane Roe" />
  <meta name="citation_author_institution" content="Department of Something, University of Whatever" />
  <meta name="citation_author_institution" content="Department of Whatever, University of Something" />
  <meta name="citation_author_orcid" content="XXXX-XXXX-XXXX-XXXX" />
  <link rel="canonical" href="https://tomwhite.github.io/manubot-test/" />
  <meta property="og:url" content="https://tomwhite.github.io/manubot-test/" />
  <meta property="twitter:url" content="https://tomwhite.github.io/manubot-test/" />
  <meta name="citation_fulltext_html_url" content="https://tomwhite.github.io/manubot-test/" />
  <meta name="citation_pdf_url" content="https://tomwhite.github.io/manubot-test/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://tomwhite.github.io/manubot-test/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://tomwhite.github.io/manubot-test/v/aa933ae5e52d1d687e235084c1440d3a29cc2b83/" />
  <meta name="manubot_html_url_versioned" content="https://tomwhite.github.io/manubot-test/v/aa933ae5e52d1d687e235084c1440d3a29cc2b83/" />
  <meta name="manubot_pdf_url_versioned" content="https://tomwhite.github.io/manubot-test/v/aa933ae5e52d1d687e235084c1440d3a29cc2b83/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...






<small><em>
This manuscript
([permalink](https://tomwhite.github.io/manubot-test/v/aa933ae5e52d1d687e235084c1440d3a29cc2b83/))
was automatically generated
from [tomwhite/manubot-test@aa933ae](https://github.com/tomwhite/manubot-test/tree/aa933ae5e52d1d687e235084c1440d3a29cc2b83)
on January 23, 2023.
</em></small>



## Authors



+ **Tom White**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [Tom White](https://github.com/Tom White)
    · ![Twitter icon](images/twitter.svg){.inline_icon width=16 height=16}
    [tom_e_white](https://twitter.com/tom_e_white)
    <br>
  <small>
     TWC
     · Funded by Grant XXXXXXXX
  </small>

+ **Jane Roe**
  ^[✉](#correspondence)^<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [janeroe](https://github.com/janeroe)
    <br>
  <small>
     Department of Something, University of Whatever; Department of Whatever, University of Something
  </small>


::: {#correspondence}
✉ — Correspondence possible via [GitHub Issues](https://github.com/tomwhite/manubot-test/issues)
or email to
Jane Roe \<jane.roe@whatever.edu\>.


:::


## Abstract {.page_break_before}




## Popgen

### Audience

[TODO]

### Overview of sgkit's API methods

Sgkit provides a number of methods for computing statistics in population genetics. Before running the methods, the dataset is usually divided into windows along the genome, using the `window_by_*` functions, which tell sgkit to produce per-window statistics. For example, `window_by_position` creates windows that are a fixed number of base pairs, while `window_by_interval` creates windows corresponding to arbitrary user-defined intervals.

It's common in population genetics to group samples into populations, which in sgkit are referred to as _cohorts_. There are two types of statistics: one-way statistics where there is a single statistic for each cohort, and multi-way statistics where there is a statistic between each pair, triple, etc of cohorts. [TODO: do we need to say how cohorts are defined?]

The methods for one-way statistics include `diversity` for computing mean genetic diversity, `Tajimas_D` for computing Tajima’s D, and `Garud_H` for computing the H1, H12, H123 and H2/H1 statistics defined in [@doi:10.1371/journal.pgen.1005004].

The methods for multi-way statistics include `divergence` and `Fst` for computing mean genetic divergence and F[ST] (respectively) between pairs of cohorts, and `pbs` for computing the population branching statistic between cohort triples.

### Example

We converted phased Ag1000G hypotype data in Zarr format [@https://www.malariagen.net/data/ag1000g-phase-2-ar1] to sgkit's Zarr format using the `read_scikit_allel_vcfzarr` function. The data contained 1,164 samples at 39,604,636 sites, and was [TODO] MB on disk before conversion, and Y MB after conversion to sgkit's Zarr format. Data for the X chromosome was discarded since it was not available for all samples. The conversion took [TODO] minutes Y seconds, including a postprocessing `rechunk` step to ensure that the data was suitably chunked for the subsequent analysis.

## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>

