# Rousset IBD from pairwise FST

```
Theory: Rousset isolation by distance (pairwise FST/(1-FST)
  versus distance)
Original paper (year): Rousset F. 1997. Genetic differentiation
  and estimation of gene flow from F-statistics under isolation
  by distance. Genetics 145(4):1219-1228 (1 April 1997).
  DOI 10.1093/genetics/145.4.1219 PMID 9093870
  PMCID PMC1207888. EuropePMC HTML opened
  (https://europepmc.org/article/MED/9093870): Rousset F,
  Laboratoire Genetique et Environnement, Universite de
  Montpellier II, France; 01 Apr 1997; Genetics 145(4):1219-1228;
  DOI; PMID; PMC; abstract. Isolation-by-distance models as a
  basis for estimating demographic parameters from subdivision.
  Results for F-statistics in one-dimensional models and
  coalescence times in two-dimensional models; earlier
  two-dimensional F and one-dimensional coalescence results
  made more precise. Method: regress pairwise FST/(1-FST)
  estimates on geographic distance for linear habitats, or on
  logarithm of distance for two-dimensional habitats. The
  regression estimates the product of population density and
  the second moment of parental axial dispersal distance. In
  two cases with direct estimates available, the method is more
  satisfactory than previous indirect methods. Distinct from
  filled Wright 1943 (continuous-space similarity decay; not
  this pairwise FST regression). Distinct from filled Slatkin
  1993 (pairwise M = (1/FST-1)/4 versus distance). Distinct
  from filled Weir and Cockerham 1984 (moment estimator, not
  an IBD regression). Distinct from filled Kimura and Weiss
  1964 stepping-stone.
One-sentence prediction: Pairwise FST/(1-FST) rises with
  distance (linear habitats) or log distance (2D); the slope
  estimates density times dispersal second moment.
Assumptions: a sexual array of subpopulations, not clones;
  dispersal is the paper's kernel, not human / nursery
  transport; a vineyard is not a subpopulation; dual
  domestication is not one habitat; chips are not forced-
  biallelic loci that fake FST.
Which fail here: humans and nurseries move vines farther than
  Rousset dispersal. Clone IBD fakes FST. Dual domestication
  is two origins, not one isolation-by-distance habitat. A
  wine-region PCA is not a Rousset transect.
Modern data / statistic: whether wild-patch pairwise
  FST/(1-FST) versus distance (or log distance) is a Rousset
  density-dispersal slope after clone + IBD filters, versus
  two domestication centres or transport.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset
  after clone + IBD filters. Use as geography, not as a
  published Rousset analysis. Do not invent a grape IBD
  paper.
What would falsify it: wild-patch FST/(1-FST) is not a
  Rousset slope after clone filter (swamped by transport, or
  two origins). Treating clone IBS as FST is not the test.
  Wright 1943 remains continuous IBD; Slatkin 1993 remains
  pairwise M; Weir-Cockerham 1984 remains the estimator.
What we will not claim: that Wright 1943 is this paper
  (already filled). That Slatkin 1993 is this paper. That
  Weir and Cockerham 1984 is this paper. That Dong 2023
  fitted a Rousset regression. That a cultivar name is a
  subpopulation.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
