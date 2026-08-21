# Slatkin private-allele gene flow

```
Theory: Slatkin private-allele estimator of gene flow
Original paper (year): Slatkin M. 1985. Rare alleles as
  indicators of gene flow. Evolution 39(1):53-65
  (1 January 1985). DOI 10.1111/j.1558-5646.1985.tb04079.x
  PMID 28563643. EuropePMC HTML opened (Slatkin M,
  Department of Zoology, NJ-15, University of Washington,
  Seattle; 01 Jan 1985; Evolution 39(1):53-65; DOI; PMID;
  abstract). Log of the average number of migrants exchanged
  between local populations, Nm, is approximately linearly
  related to the log of the average frequency of private
  alleles, p(1); the relation is relatively insensitive to
  other parameters except Nm and the number of individuals
  sampled. Applied to 16 species, estimated Nm ranged from
  much greater than 1 to less than 0.1, confirming the
  qualitative analysis of Slatkin 1981. Distinct from filled
  Wright 1931 island (FST = f(Nem) as the parameter, not a
  private-allele estimator). Distinct from filled Wright
  1943 IBD and filled Kimura and Weiss 1964 stepping-stone.
  Distinct from filled Weir and Cockerham 1984 (moment FST).
  Slatkin 1987 Science 236:787-792 (PMID 3576198) is a
  review of direct and indirect gene-flow methods; red line;
  not the source. Slatkin 1981 is the qualitative precursor,
  not used as the source (same Muller-1964 / Felsenstein-1974
  split).
One-sentence prediction: The rarer the private alleles in
  a set of local samples, the larger Nm; private alleles
  that are common imply little gene flow.
Assumptions: samples are local sexual populations, not
  clones or cultivars; a private allele is not a clone-
  private SNP or a nursery sport; sample size is scored
  (the paper's correction); a vineyard block is not a
  local population.
Which fail here: grafted cultivars are not demes. Clone
  IBD fakes private alleles. Humans and nurseries move
  vines farther than local migration. Dual domestication
  is not one subdivided species with a single Nm.
Modern data / statistic: private-allele frequency among
  wild V. sylvestris patches after clone + IBD filters,
  converted to Nm, versus an island / IBD / stepping-stone
  reading.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset
  after clone + IBD filters. Use as structure, not as a
  published private-allele analysis. Do not invent a grape
  gene-flow paper.
What would falsify it: private-allele Nm among wild patches
  is not a migration estimate after clone filter (clone-
  private SNPs treated as private alleles are not the test).
  FST independent of distance is the Wright 1931 job;
  continuous IBD slope is the Wright 1943 job.
What we will not claim: that Slatkin 1987 is the source
  (review). That Slatkin 1981 is this paper. That Wright
  1931 or Weir-Cockerham 1984 is this paper. That Dong
  2023 estimated Nm from private alleles. That a cultivar
  private SNP is a migrant.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
