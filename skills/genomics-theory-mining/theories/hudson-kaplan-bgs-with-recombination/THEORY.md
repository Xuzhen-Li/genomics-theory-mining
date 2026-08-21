# Hudson-Kaplan BGS with recombination

```
Theory: Hudson-Kaplan background selection with
  recombination
Original paper (year): Hudson RR, Kaplan NL. 1995.
  Deleterious background selection with recombination.
  Genetics 141(4):1605-1617 (1 December 1995).
  DOI 10.1093/genetics/141.4.1605 PMID 8601498
  PMCID PMC1206891. EuropePMC HTML opened
  (https://europepmc.org/article/MED/8601498):
  Hudson RR, Department of Ecology and Evolutionary
  Biology, University of California, Irvine 92717,
  USA; Kaplan NL; 01 Dec 1995; Genetics 141(4):1605-
  1617; DOI; PMID; PMC; abstract. An analytic
  expression for expected nucleotide diversity at a
  neutral locus in a region with deleterious mutation
  and recombination. Predictions for the entire third
  chromosome of D. melanogaster: consistent with low
  variation near the centromeres; low variation near
  the tips is not predicted with then-available
  deleterious-mutation and selection estimates, unless
  selection coefficients are considerably smaller.
  Distinct from filled Charlesworth, Morgan and
  Charlesworth 1993 (BGS original; no/low-
  recombination formulas, not this analytic-with-
  recombination result). Distinct from filled
  Charlesworth 1994 (this wave; weakly selected
  substitution rates, not the recombination formula
  for pi). Distinct from filled Kaplan, Hudson and
  Langley 1989 (coalescent hitchhiking reduction of
  polymorphic sites; not BGS). Distinct from filled
  Nordborg 1996 (this wave; arbitrary-map extension).
One-sentence prediction: Expected nucleotide diversity
  at a neutral locus has an analytic BGS form when
  deleterious mutation and recombination both act;
  low-recombination (centromere-like) regions are
  the strong prediction.
Assumptions: a sexual recombination map with linked
  deleterious mutation; a chip skeleton is not that
  map; samples are not clones; a vineyard is not a
  Drosophila third chromosome.
Which fail here: clone IBD fakes a diversity trough
  in low-recombination bins. A SNP chip is not a
  Vitis map. Dual domestication is two origins.
  Human transport is not Drosophila recombination.
Modern data / statistic: whether wild-sample
  nucleotide diversity after clone + IBD filters
  follows the Hudson-Kaplan BGS function of local
  recombination and deleterious mutation on a real
  Vitis map, versus clone IBS or two origins.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Use as the BGS-
  with-recombination contrast, not as a published
  grape Hudson-Kaplan analysis. Do not invent a
  grape BGS-with-recombination paper. No locked
  grape recombination-map paper; the map is a
  requirement, as in the 1993 BGS note.
What would falsify it: diversity is not the Hudson-
  Kaplan BGS function after clone filter (flat, or
  clone IBS, or two origins). Neutral-diversity BGS
  remains Charlesworth 1993. Coalescent hitchhiking
  remains Kaplan 1989. Weakly-selected BGS remains
  Charlesworth 1994.
What we will not claim: that Charlesworth 1993 is
  this paper (already filled). That Kaplan 1989 is
  this paper. That Dong 2023 fitted a Hudson-Kaplan
  BGS curve. That a chip skeleton is the map.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
