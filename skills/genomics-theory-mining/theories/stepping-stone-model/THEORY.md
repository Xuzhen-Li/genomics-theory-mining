# Stepping-stone model

```
Theory: Stepping-stone model
Original paper (year): Kimura M, Weiss GH. 1964. The stepping stone
  model of population structure and the decrease of genetic
  correlation with distance. Genetics 49(4):561-576.
  DOI 10.1093/genetics/49.4.561 PMID 17248204 PMC1210594.
  (Kimura 1953 Annual Report of the National Institute of Genetics
  Japan 3:62-63 is a one-page note; 1964 is the paper. Weiss and
  Kimura 1965 J Appl Probab 2:129-149 is later math.)
  Distinct from filled IBD: Wright 1943 is continuous isolation by
  distance. Stepping-stone is discrete neighbor-only migration.
One-sentence prediction: In a lattice of demes that exchange
  migrants only with neighbors, genetic correlation declines with
  the number of steps between demes (and with dimension).
Assumptions: a lattice of demes; migration only to neighbors;
  correlation is a function of steps, not Euclidean distance as
  such; samples are demes, not clones or cultivars.
Which fail here: a cultivar PCA is not a lattice. Humans and
  rivers move vines farther than one step. Grafted clones are
  not demes.
Modern data / statistic: genetic correlation versus step-count
  and versus Euclidean distance among wild V. sylvestris patches
  after clone / pedigree filters.
Dataset: Dong Y et al. 2023. Science. DOI 10.1126/science.add8655
  PMID 36862793. 3525-accession WGS; use wild sylvestris only
  after clone / pedigree filter.
What would falsify it: correlation among wild patches is not
  higher along neighbor-connected habitat (river / corridor)
  than at equal Euclidean distance, or the decay is no steeper
  than Wright 1943 continuous IBD.
What we will not claim: that a wine-region PCA is a stepping-
  stone lattice. That this note replaces Wright 1943 IBD
  (different job: discrete neighbor steps vs continuous
  distance).
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
