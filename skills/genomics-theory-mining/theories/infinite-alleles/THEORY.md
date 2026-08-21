# Infinite-alleles

```
Theory: Infinite-alleles model
Original paper (year): Kimura M, Crow JF. 1964. The number
  of alleles that can be maintained in a finite population.
  Genetics 49(4):725-738. DOI 10.1093/genetics/49.4.725
  PMID 14156929 PMC1210609.
One-sentence prediction: Each mutation creates a new allele,
  so identity-by-state is identity-by-descent; the effective
  number of alleles is 4Ne u + 1 under neutrality.
Assumptions: an astronomically large allelic state space;
  back-mutation / recurrent mutation negligible; a finite
  sexual population with a meaningful Ne.
Which fail here: SNP chips ascertain a finite, recurrent
  state space (mostly biallelic). Same-site SNPs and TE
  family insertions are recurrent. A cultivar collection
  is not one Ne. Identity-by-state among clones is not
  identity-by-descent in the Kimura-Crow sense.
Modern data / statistic: recurrent same-site or same-element
  events, and IBS versus IBD, on cultivar chips or WGS
  after clone filters.
Datasets: Carrier et al. 2012 PLoS ONE 7(3):e32973 (recurrent
  TE insertions in Pinot noir). Vondras et al. 2019 BMC
  Genomics 20:972 (TE plus methylation-driven transitions
  among Zinfandel clones). Dong et al. 2023 Science (WGS;
  they already used IBS to collapse clone genotypes).
  Do not invent a grape chip-ascertainment paper.
What would falsify it: identity-by-state on Vitis chips
  (or WGS SNPs) behaves as infinite-alleles after clones
  are filtered — recurrent SNPs and ascertainment are
  rare enough not to matter.
What we will not claim: that infinite-alleles is the same
  job as infinite-sites (that note is already filled).
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
