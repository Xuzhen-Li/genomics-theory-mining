# McClintock TE (Vitis extra)

```
Theory: Mobile loci generate new mutable alleles
Original paper (year): McClintock B. 1950. The origin and behavior of
  mutable loci in maize. Proc Natl Acad Sci USA 36(6):344-355.
  DOI 10.1073/pnas.36.6.344.
One-sentence prediction: Chromosome-breakage-associated mobile elements
  (Ac/Ds in maize) change position and create new unstable alleles.
Assumptions: the mutability is caused by transposition, not by a
  static SNP; the element can be recovered at the new site.
Which fail here: scoring only SNPs on a 12X panel hides the TE clock.
  Methylation both silences TEs and raises C-to-T in the same repeats
  (Vondras 2019), so "repeat SNPs" are not independent of TEs.
Modern data / statistic: clone-private TE insertion rate versus SNP
  rate in the same cultivar.
Lead test: Carrier et al. 2012 PLoS ONE 7(3):e32973. In Pinot noir,
  insertion polymorphism from mobile elements was the largest scored
  mutational class (147 events; 35.2 / Mb).
Companion: Vondras et al. 2019 (TE insertions plus methylation-driven
  transitions). Zhou et al. 2019 (SVs, including TE-associated, accrue
  as heterozygotes in clones).
What would falsify it: in a genome-wide, method-fair census, clone
  polymorphism is SNP-dominated and TE insertions are negligible.
What we will not claim: that every berry-color sport is a TE
  (Carbonell-Bejerano 2017 is a rearrangement, not a TE proof).
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
