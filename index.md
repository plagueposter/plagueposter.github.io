## Introduction

* Unclear whether the second plague pandemic was driven by rat fleas or human ectoparasites [1, 2]
* Mathematical models can help identify the underlying biological mechanisms
* Dean et al.’s [3] conclusion that these epidemics were driven by human ectoparasites relies on strong assumptions [4]

## Methods

* Particle MCMC [5] + biologically informed priors on all model parameters
* Use ternary plots to summarize results
* Incorporate information from Third Pandemic plague epidemics with known transmission modes
* Validate with simulation studies

## Combined transmission model

![model](https://github.com/plagueposter/plagueposter.github.io/blob/master/images/propose.png)

* Direct human-to-human transmission (pneumonic plague)
* Indirect human-to-human transmission (bubonic plague) via human ectoparasites
* Transmission (bubonic plague) via rat fleas
* Bubonic cases →secondary pneumonic cases

## Biologically informed priors

![prior](https://github.com/plagueposter/plagueposter.github.io/blob/master/images/prior_data2.png)

* Represents uncertainty in our knowledge about the biology
* Use biologically informed priors on all model parameters
* Why? Overly specific parametric assumptions → overly confident conclusions [6]

## Results

![prior](https://github.com/plagueposter/plagueposter.github.io/blob/master/images/combres.png)

(Top) Fits of combined model to mortality data from the Second Pandemic epidemics. For each posterior sample, a filtered trajectory is calculated using 500 particles. Solid lines represent median trajectories. Shaded regions represent equi-tailed 95% credible intervals. Numbers on top right represent goodness of fit. (Bottom) Relative contribution of each transmission route. Proportion of total incidence caused by pneumonic plague (PP), (human) ectoparasite plague (EP), and rat-flea plague (RP) is calculated for each filtered trajectory; this summary is mapped onto a ternary plot. Shaded areas represent 95% highest posterior density regions.

## Simulation studies

#### Case 1: correctly identifies the true mechanism and rules out other mechanisms (5/18)

![prior](https://github.com/plagueposter/plagueposter.github.io/blob/master/images/g1.png)

#### Case 2: unclear results but does not rule out the true mechanism (12/18)

![prior](https://github.com/plagueposter/plagueposter.github.io/blob/master/images/g2.png)

#### Case 3: rules out the true mechanism (1/18)

![prior](https://github.com/plagueposter/plagueposter.github.io/blob/master/images/g3.png)

## Conclusions and open questions

* Our models take many sources of uncertainty into account and still make meaningful conclusions
* Need to consider combined transmission
* Large uncertainty about transmission remains
* neglected: seasonal patterns in plague epidemics (e.g., two epidemic peaks in Moscow, 1772)

## Acknowledgements

We thank (#MacTheobio)[https://twitter.com/hashtag/mactheobio?f=tweets&vertical=default] lab for useful comments, Aaron King for discussions on particle filtering, Katharine Dean for the mortality time series, the Natural Science and Engineering Research Council of Canada (NSERC) for funding, and SHARCNET for computational resources.

## Reference

1. Drancourt, M., Houhamdi, L., & Raoult, D. (2006). Yersinia pestis as a telluric, human ectoparasite-borne organism. The Lancet infectious diseases, 6(4), 234-241.
2. Hufthammer, A. K., & Walløe, L. (2013). Rats cannot have been intermediate hosts for Yersinia pestis during medieval plague epidemics in Northern Europe. Journal of Archaeological Science, 40(4), 1752-1759.
3. Dean, K. R., Krauer, F., Walløe, L., Lingjærde, O. C., Bramanti, B., Stenseth, N. C., & Schmid, B. V. (2018). Human ectoparasites and the spread of plague in Europe during the Second Pandemic. PNAS, 115(6), 1304-1309.
4. Park, S. W., Dushoff, J., Earn, D. J., Poinar, H., & Bolker, B. M. (2018). Human ectoparasite transmission of the plague during the Second Pandemic is only weakly supported by proposed mathematical models. PNAS, 115(34), E7892-E7893.
5. King, A. A., Nguyen, D., & Ionides, E. L. (2015). Statistical inference for partially observed Markov processes via the R package pomp. arXiv preprint arXiv:1509.00503.
6. Elderd, B. D., Dukic, V. M., & Dwyer, G. (2006). Uncertainty in predictions of disease spread and public health responses to bioterrorism and emerging diseases. PNAS, 103(42), 15693-15697.
7. Tieh, T. H., Landauer, E., Miyagawa, F., Kobayashi, G., & Okayasu, G. (1948). Primary pneumonic plague in Mukden, 1946, and report of 39 cases with 3 recoveries. The Journal of infectious diseases, 82(1), 52-58.
8. Perry, R. D., & Fetherston, J. D. (1997). Yersinia pestis--etiologic agent of plague. Clinical microbiology reviews, 10(1), 35-66.
9. Kool, J. L., & Weinstein, R. A. (2005). Risk of person-to-person transmission of pneumonic plague. Clinical Infectious Diseases, 40(8), 1166-1172.
10. Gani, R., & Leach, S. (2004). Epidemiologic determinants for modeling pneumonic plague outbreaks. Emerging infectious diseases, 10(4), 608.

