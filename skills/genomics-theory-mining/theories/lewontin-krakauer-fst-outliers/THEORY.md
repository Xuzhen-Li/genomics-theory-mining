# Lewontin-Krakauer FST outliers

```
Theory: Lewontin-Krakauer test (F heterogeneity among loci)
Original paper (year): Lewontin RC, Krakauer J. 1973. Distribution
  of gene frequency as a test of the theory of the selective
  neutrality of polymorphisms. Genetics 74(1):175-195 (1 May 1973).
  DOI 10.1093/genetics/74.1.175 PMID 4711903 PMCID PMC1212935.
  EuropePMC HTML opened (Lewontin RC, Krakauer J; 01 May 1973;
  Genetics 74(1):175-195; DOI; PMID; PMC; abstract). PMC HTML
  opened (Department of Theoretical Biology / Department of
  Biology, University of Chicago; received 14 February 1972;
  revision requested 16 January 1973). Breeding structure should
  affect all loci the same way; significant heterogeneity among
  loci in apparent inbreeding coefficients
  F = s(p)^2 / p(1-p) is evidence for selection. Human polymorphic
  genes showed highly significant heterogeneity in F worldwide;
  temporal variation in Dacus oleae did not. Distinct from filled
  Wright 1931 island (FST as a function of Nem, no locus test).
  Distinct from filled Wright 1943 IBD and filled Weir and
  Cockerham 1984 (the moment estimator, not a heterogeneity
  test). Distinct from filled Kimura 1968 (the neutral null).
  Beaumont and Nichols 1996 is a later method; not used.
One-sentence prediction: Loci that share a breeding structure
  share F; a locus whose F is an outlier relative to the others
  is a candidate for selection.
Assumptions: samples are demes, not clones or cultivars; F is
  not clone IBS; chips are not forced-biallelic loci; dual
  domestication is not one breeding structure; a vineyard is
  not a deme.
Which fail here: grafted cultivars are not demes. Clone IBD
  fakes F. SNP chips are biallelic. Dual domestication and
  human transport violate a single shared breeding structure.
  A wine-region PCA is not a Lewontin-Krakauer table.
Modern data / statistic: heterogeneity of locus F (or FST)
  among wild V. sylvestris patches after clone + IBD filters,
  versus a single shared breeding-structure null.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset after
  clone + IBD filters. Use as structure, not as a published
  Lewontin-Krakauer analysis. Do not invent a grape FST-outlier
  paper.
What would falsify it: F among wild-patch loci is not
  heterogeneous after clone + IBD filters (the selection
  reading dies). Treating clone IBS as F is not the test.
  Island / IBD / WC-estimator jobs remain other notes.
What we will not claim: that Wright 1931 or 1943 is this
  paper. That Weir-Cockerham 1984 is this paper. That
  Beaumont and Nichols 1996 is the source. That Dong 2023
  ran a Lewontin-Krakauer test. That a cultivar PCA is an
  F-outlier table.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
