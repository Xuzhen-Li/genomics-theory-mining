# Weir-Cockerham FST

```
Theory: Weir-Cockerham FST estimator
Original paper (year): Weir BS, Cockerham CC. 1984.
  Estimating F-statistics for the analysis of population
  structure. Evolution 38(6):1358-1370 (1 November 1984).
  DOI 10.1111/j.1558-5646.1984.tb05657.x PMID 28563791.
  EuropePMC HTML opened (Weir BS, Cockerham CC;
  Department of Statistics, North Carolina State
  University; 01 Nov 1984; Evolution 38(6):1358-1370;
  DOI; PMID). Wiley / OUP HTML not used (prior-wave
  Cloudflare pattern). Wright 1951 / 1965 named FST,
  FIT, and FIS; 1931 already filled as the island-model
  math. 1984 is the moment estimator from allele-frequency
  variance that accounts for sample size, number of
  populations, and multiple alleles (Cockerham 1969 / 1973
  parameters extended). Distinct from filled Wright 1931
  island (the parameter FST = f(Nem), no distance decay).
  Distinct from filled Wright 1943 IBD and Kimura and
  Weiss 1964 stepping-stone. Distinct from filled Nei 1972
  genetic distance (this wave; a between-population
  identity distance, not an FST estimator).
One-sentence prediction: Population structure is summarized
  by moment estimates of FST / FIT / FIS from allele-
  frequency variance; finite samples and unequal deme
  sizes are part of the estimator, not nuisances to ignore.
Assumptions: samples are demes, not clones or cultivars;
  a vineyard block is not a deme; clone IBS is not
  coancestry; the island formula is not plugged in as the
  data function.
Which fail here: grafted cultivars are not demes. Clone
  IBD fakes FST. A wine-region PCA is not a Weir-Cockerham
  analysis. Dual domestication and human transport violate
  the island reading already filled as Wright 1931.
Modern data / statistic: Weir-Cockerham FST among wild
  V. sylvestris patches after clone + IBD filters, versus
  distance (island: no decay; IBD / stepping-stone: decay).
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset
  after clone + IBD filters. Use as structure, not as a
  published WC-FST analysis. Do not invent a grape FST
  paper.
What would falsify it: WC FST among wild patches is not
  independent of distance after clone filter (the island
  reading dies; that is the Wright 1931 job already
  filled). Treating clone IBS as FST is not the test.
What we will not claim: that Wright 1931 is this paper
  (island math, already filled). That Nei 1972 is this
  paper. That Dong 2023 reported Weir-Cockerham FST.
  That a cultivar PCA is an FST table.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
