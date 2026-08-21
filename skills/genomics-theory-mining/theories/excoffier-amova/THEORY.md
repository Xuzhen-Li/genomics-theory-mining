# Excoffier AMOVA

```
Theory: Excoffier AMOVA (hierarchical molecular variance and
  phi-statistics)
Original paper (year): Excoffier L, Smouse PE, Quattro JM.
  1992. Analysis of molecular variance inferred from metric
  distances among DNA haplotypes: application to human
  mitochondrial DNA restriction data. Genetics 131(2):479-491
  (1 June 1992). DOI 10.1093/genetics/131.2.479 PMID 1644282
  PMCID PMC1205020. EuropePMC HTML opened
  (https://europepmc.org/article/MED/1644282): Excoffier L,
  Center for Theoretical and Applied Genetics (CTAG), Cook
  College, Rutgers University, New Brunswick, New Jersey
  08903-0231; Smouse PE; Quattro JM; 01 Jun 1992; Genetics
  131(2):479-491; DOI; PMID; PMC; abstract. DNA haplotype
  divergence is put into an analysis-of-variance format from
  a matrix of squared distances among all pairs of haplotypes.
  AMOVA estimates variance components and F-statistic analogs
  (phi-statistics) for haplotypic diversity at hierarchical
  levels of subdivision. Alternative input matrices (data
  types / evolutionary assumptions) leave the analysis
  structure unchanged. Significance of variance components
  and phi-statistics is tested by permutation, dropping the
  normality assumption that is conventional for ANOVA but
  inappropriate for molecular data. Human mtDNA: subdivisions
  resolve better when some molecular difference among
  haplotypes is used; at the intraspecific level, exact
  phylogeny or a nonlinear restriction-to-nucleotide map does
  not much change inferred structure. Distinct from filled
  Weir and Cockerham 1984 (moment FST from allele-frequency
  variance; not haplotype-distance hierarchy). Distinct from
  filled Nei 1972 distance. Distinct from filled Wright 1931
  island formula as data.
One-sentence prediction: Hierarchical molecular variance
  among haplotypes is captured by phi-statistics; permutation
  tests whether a named hierarchy explains haplotypic
  distances.
Assumptions: haplotypes are from a sexual sample, not clone
  copies; the named hierarchy is biological, not a nursery
  catalogue; dual domestication is not one nested design;
  mtDNA-style haplotypes are not SNP-chip genotypes treated
  as clones.
Which fail here: clone IBD fakes haplotypes. Dual
  domestication is two origins, not one nested hierarchy. A
  vineyard is not a deme. Cultivar groups are human
  catalogues.
Modern data / statistic: whether wild / cultivar haplotype
  distances after clone + IBD filters support an AMOVA
  hierarchy (phi among named groups), versus two
  domestication centres or clone copies.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Use as the hierarchy
  contrast, not as a published grape AMOVA. Do not invent a
  grape AMOVA paper.
What would falsify it: the named hierarchy does not explain
  haplotypic distances after clone filter (two origins, or
  clone copies). Treating cultivar names as demes is not the
  test. Weir-Cockerham 1984 remains the moment-FST job; Nei
  1972 remains genetic distance.
What we will not claim: that Weir and Cockerham 1984 is this
  paper (already filled). That Nei 1972 is this paper. That
  Dong 2023 ran AMOVA. That a cultivar name is a haplotype
  deme.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
