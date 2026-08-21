# Braverman hitchhiking SFS

```
Theory: Braverman hitchhiking site-frequency spectrum
Original paper (year): Braverman JM, Hudson RR, Kaplan NL,
  Langley CH, Stephan W. 1995. The hitchhiking effect on
  the site frequency spectrum of DNA polymorphisms.
  Genetics 140(2):783-796 (1 June 1995).
  DOI 10.1093/genetics/140.2.783 PMID 7498754
  PMCID PMC1206652. EuropePMC HTML opened (Braverman JM,
  Center for Population Biology, University of California,
  Davis; Hudson RR; Kaplan NL; Langley CH; Stephan W;
  01 Jun 1995; Genetics 140(2):783-796; DOI; PMID; PMC;
  abstract). Simple hitchhiking (directional selection on
  rare advantageous mutants sweeping linked neutrals)
  predicts a skew toward rare variants. Coalescent
  simulations of recurrent hitchhiking show (1) expected
  Tajima D is large and negative, (2) Tajima's test has
  reasonable power for realistic parameters, and (3) some
  Drosophila datasets with reduced diversity but no SFS
  skew are very unlikely under simple hitchhiking; that
  model is then not a sufficient explanation. Distinct
  from filled Tajima 1989 (the D statistic as a neutrality
  test; this paper is the hitchhiking prediction for D).
  Distinct from filled Kaplan, Hudson and Langley 1989
  (this wave; reduction in the number of sites, not the
  SFS / D prediction). Distinct from filled Fay and Wu
  2000 H (derived high-frequency excess). Distinct from
  filled Maynard Smith and Haigh 1974.
One-sentence prediction: Simple recurrent hitchhiking
  leaves a large negative Tajima D (excess of rare
  variants) at linked sites; reduced diversity without
  that skew is not simple hitchhiking.
Assumptions: a random sample of sequences; rare variants
  are not clone-private SNPs; a cultivar panel is not
  that sample; chips are not forced-biallelic loci;
  demography is not a confounder that mimics D.
Which fail here: a cultivar panel is not a random sample.
  Clone IBD and clone-private SNPs fake rare variants.
  Dual domestication is not one equilibrium population.
  SNP chips are biallelic.
Modern data / statistic: Tajima D (and the SFS) at
  candidate domestication loci on Dong-class WGS after
  clone + IBD filters, versus the large-negative-D
  hitchhiking prediction. Kaplan site-count and Fay-Wu H
  remain other jobs.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Color / sex / flavor
  peaks. Use as the SFS contrast, not as a published
  Braverman analysis. Do not invent a grape hitchhiking-SFS
  paper.
What would falsify it: candidate loci do not show large
  negative D after clone + IBD filters (simple hitchhiking
  dies; BGS or demography remain other readings). Treating
  clone-private SNPs as rare sweep variants is not the
  test. One-sample Tajima as a generic test is the 1989
  job; site-count reduction is the Kaplan job.
What we will not claim: that Tajima 1989 is this paper
  (already filled). That Kaplan 1989 is this paper. That
  Fay and Wu 2000 is this paper. That Dong 2023 computed
  a Braverman SFS. That a nursery sport is a rare variant
  from a sweep.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
