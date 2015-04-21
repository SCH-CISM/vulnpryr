[![Travis-CI Build Status](https://travis-ci.org/SCH-CISM/vulnpryr.png?branch=master)](https://travis-ci.org/SCH-CISM/vulnpryr)[![Coverage Status](https://coveralls.io/repos/SCH-CISM/vulnpryr/badge.svg?branch=master)](https://coveralls.io/r/SCH-CISM/vulnpryr?branch=master)

vulnpryr
=========

Vulnerability Pryer - An implementation of [VulnPryer](https://github.com/SCH-CISM/VulnPryer) in R.

#Installation
`
devtools:github("SCH-CISM\vulnpryr")
`

#Usage

```
library(vulnpryr)

#Load vulnerability fact table
vulndb_file <- ".\vulnerability_facts.csv"
vulnpryr::load_vulndb(vulndb_file)

#Rescore a vulnerability
vulnpryer(cve_id = "CVE-2014-0013", cvss_base = 5)
```

Weightings can be overridden by specifying manual values in the function call.

`
vulnpryer(cve_id = "CVE-2014-0013", cvss_base = 5, msp_factor = 2, network_vector_factor = 3)
`

#Acknowledgements
VulnPryer would not exist without the inspiration and assistance of the following individuals 
and organizations:
- [@alexcpsec](https://twitter.com/alexcpsec) and 
[@kylemaxwell](https://twitter.com/alexcpsec) for the 
[combine](https://github.com/mlsecproject/combine) project. VulnPryer has cribbed heavily from 
that design pattern, including a crude aping of naming metaphors. :grin:
- [Risk Based Security](https://vulndb.cyberriskanalytics.com/) (RBS) 
for providing the VulnDB product and for the support in getting this project 
off the ground.
- [Risk I/O](https://www.risk.io/) for providing the inspiration 
on this project and their continued support of the community.
- [RedSeal](https://www.redsealnetworks.com) for providing the analysis platform for network 
security posture review and analysis.
