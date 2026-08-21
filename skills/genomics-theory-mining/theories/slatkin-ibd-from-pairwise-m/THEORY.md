# Slatkin IBD from pairwise M

```
Theory: Slatkin isolation by distance from pairwise M
Original paper (year): Slatkin M. 1993. Isolation by
  distance in equilibrium and non-equilibrium populations.
  Evolution 47(1):264-279 (1 February 1993).
  DOI 10.1111/j.1558-5646.1993.tb01215.x PMID 28568097.
  EuropePMC HTML opened (Slatkin M, Department of
  Integrative Biology, University of California, Berkeley;
  01 Feb 1993; Evolution 47(1):264-279; DOI; PMID;
  abstract). For allele-frequency data a useful pairwise
  gene-flow measure is M = (1/FST - 1)/4, the estimated
  island-model Nm at equilibrium; for sequences, replace
  FST by NST. Analytic theory gives a simple relationship
  between M and geographic distance in both equilibrium and
  non-equilibrium populations, approximately independent of
  mutation rate when that rate is small. Simulations show
  IBD can be detected with reasonable samples and that some
  non-equilibrium patterns can be distinguished. Applied to
  gull and pocket-gopher allozymes. Distinct from filled
  Wright 1943 IBD (continuous isolation by distance as the
  process; no pairwise-M diagnostic). 1993 is the FST-based
  estimator of that pattern, the same split as filled Weir-
  Cockerham 1984 versus filled Wright 1931 island math.
  Distinct from filled Kimura and Weiss 1964 stepping-stone
  and from filled Slatkin 1985 private alleles (this wave;
  a different gene-flow estimator). Distinct from filled
  serial founder (Ramachandran et al. 2005).
One-sentence prediction: Pairwise M declines with geographic
  distance under restricted dispersal, in both equilibrium
  and some non-equilibrium histories; a flat M-distance
  plot is not that pattern.
Assumptions: pairs are demes, not clones or cultivars; FST
  is not clone IBS; a vineyard is not a pair of demes;
  dual domestication is not one expanding range; mutation
  is small relative to migration.
Which fail here: grafted cultivars are not demes. Clone
  IBD fakes FST and therefore M. Humans and rivers move
  vines farther than restricted dispersal. Dual
  domestication is two origins, not one IBD surface.
Modern data / statistic: pairwise M among wild
  V. sylvestris patches after clone + IBD filters, versus
  geographic distance (IBD: decline; island: flat).
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset
  after clone + IBD filters. Use as geography, not as a
  published Slatkin-M analysis. Do not invent a grape
  isolation-by-distance estimator paper.
What would falsify it: M among wild patches is not a
  function of distance after clone filter (the restricted-
  dispersal reading dies). Treating clone IBS as FST is
  not the test. Wright 1943 remains the continuous-space
  original; this note is the pairwise-M diagnostic.
What we will not claim: that Wright 1943 is this paper
  (already filled). That Slatkin 1985 is this paper.
  That Ramachandran 2005 is this paper. That Dong 2023
  reported pairwise M. That a wine-region PCA is an
  M-distance plot.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
