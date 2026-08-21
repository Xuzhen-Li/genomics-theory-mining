# Slatkin conditional-frequency gene flow

```
Theory: Slatkin conditional average frequency (gene-flow
  estimator)
Original paper (year): Slatkin M. 1981. Estimating levels of
  gene flow in natural populations. Genetics 99(2):323-335
  (1 October 1981). DOI 10.1093/genetics/99.2.323
  PMID 17249120 PMCID PMC1214504. EuropePMC HTML opened
  (https://europepmc.org/article/MED/17249120): Slatkin M,
  Department of Zoology, NJ-15, University of Washington,
  Seattle, Washington 98195; 01 Oct 1981; Genetics
  99(2):323-335; DOI; PMID; PMC; abstract. Simulation of
  selection, mutation, and drift in a geographically
  subdivided population (infinite-alleles mutation; both
  advantageous and deleterious mutants). The average
  frequency of an allele conditioned on the number of local
  populations it appears in (the conditional average
  frequency) is approximately independent of selection
  intensity and mutation rate, but depends strongly on the
  overall level of gene flow. That justifies using the
  conditional average frequency as a rough estimate of
  gene flow. Data from 16 species: large differences among
  taxa; some species apparently high gene flow, salamanders
  low. Distinct from filled Slatkin 1985 (private-allele
  frequency as log Nm; the later lock). Distinct from
  filled Slatkin 1993 (pairwise M from FST). Distinct from
  filled Slatkin 1973 / 1975 two-locus (clines). Distinct
  from filled Slatkin and Maruyama 1975 (this wave; drift
  flattening a cline). Distinct from filled Wright 1931
  (island FST = f(Nem) as theory, not this occupancy
  estimator). Slatkin 1987 Science remains a review.
One-sentence prediction: Allele frequency given occupancy
  (how many demes carry the allele) estimates gene flow
  and is nearly independent of selection and mutation.
Assumptions: local populations are sexual demes, not
  clones; occupancy is not a cultivar name-list; private
  or rare alleles are not clone-private SNPs; dual
  domestication is not one subdivided species.
Which fail here: clones fake occupancy and private alleles.
  A nursery block is not a deme. Human transport is not
  the paper's gene flow. Dual domestication is two origins.
  SNP chips are biallelic, not infinite-alleles.
Modern data / statistic: whether wild-patch conditional
  average frequencies estimate Nm after clone + IBD
  filters, versus clone-private SNPs or two origins.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset
  after clone + IBD filters. Use as the occupancy contrast,
  not as a published Slatkin-1981 analysis. Do not invent
  a grape conditional-frequency paper.
What would falsify it: conditional frequencies do not
  estimate gene flow after clone filter (clone-private
  SNPs, or two origins). Private-allele log Nm remains
  the 1985 job; pairwise M remains 1993; island FST
  remains Wright 1931.
What we will not claim: that Slatkin 1985 is this paper
  (already filled). That Slatkin 1993 is this paper. That
  Slatkin 1987 is the source (review). That Dong 2023
  estimated conditional-frequency Nm. That a cultivar
  private SNP is an occupancy allele.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
