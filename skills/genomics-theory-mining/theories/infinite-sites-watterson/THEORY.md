# Infinite-sites / Watterson

```
Theory: Infinite-sites model and theta from segregating sites
Original paper (year): Kimura M. 1969. The number of heterozygous
  nucleotide sites maintained in a finite population due to steady
  flux of mutations. Genetics 61(4):893-903.
  DOI 10.1093/genetics/61.4.893.
  Estimator: Watterson GA. 1975. On the number of segregating sites
  in genetical models without recombination. Theor Popul Biol
  7(2):256-276. DOI 10.1016/0040-5809(75)90020-9 PMID 1145509.
One-sentence prediction: Each mutation hits a new site, so the number
  of segregating sites estimates 4Ne mu (theta_W) and should match
  pairwise diversity (pi) under neutrality.
Assumptions: infinite sites; no recurrent mutation; no recombination
  in the Watterson 1975 derivation; Wright-Fisher sample of unrelated
  gametes.
Which fail here: TE insertions hit the same families repeatedly.
  Gene conversion and hemizygosity create apparent recurrent SNPs.
  Clone samples are not a random sexual sample.
Modern data / statistic: pi versus theta_W, and recurrent TE insertion
  counts, on clone and cultivar WGS.
Datasets: Carrier et al. 2012 PLoS ONE 7(3):e32973 (147 mobile-element
  insertion events in Pinot noir; TE rate exceeded SNP/indel in the
  scored interval). Vondras et al. 2019 BMC Genomics 20:972 (thousands
  of TE insertions among Zinfandel clones).
What would falsify it: recurrent same-site or same-element events are
  rare enough that pi still equals theta_W after clones are filtered.
What we will not claim: that every TE insertion invalidates Watterson
  on fourfold SNPs. State the site class.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
