# Nei-Li nucleotide diversity

```
Theory: Nei-Li nucleotide diversity (pi)
Original paper (year): Nei M, Li WH. 1979. Mathematical model
  for studying genetic variation in terms of restriction
  endonucleases. Proc Natl Acad Sci USA 76(10):5269-5273
  (15 October 1979; EuropePMC 01 Oct 1979).
  DOI 10.1073/pnas.76.10.5269 PMID 291943 PMCID PMC413122.
  EuropePMC HTML opened (https://europepmc.org/article/MED/291943):
  Nei M, Li WH; 01 Oct 1979; PNAS 76(10):5269-5273; DOI; PMID;
  PMC; abstract. A mathematical model for evolutionary change
  of restriction sites in mitochondrial DNA; formulas for the
  number of nucleotide substitutions between two populations
  or species; a measure called nucleotide diversity is proposed
  for polymorphism at the nucleotide level. Seed-lock PDF
  (https://europepmc.org/articles/PMC413122?pdf=render):
  Center for Demographic and Population Genetics, University
  of Texas Health Science Center, Houston, Texas 77025;
  communicated by Motoo Kimura, 1 August 1979. Nucleotide
  diversity pi is the average number of nucleotide differences
  per site between two randomly chosen DNA sequences
  (pi = sum_i sum_j x_i x_j r_ij). When populations are
  closely related, intrapopulational pi is subtracted:
  net nucleotide differences delta = pi_XY - (pi_X + pi_Y)/2.
  Distinct from filled Nei 1972 (allele-frequency distance D
  from gene identity; not nucleotide pi). Distinct from filled
  Nei 1973 (GST = DST/HT). Distinct from filled Nei 1978
  (small-sample unbiased H and D). Distinct from filled
  Tajima 1989 (D as pi versus theta_W; not the definition of
  pi). Distinct from filled Watterson 1975 (theta from S).
  Distinct from filled Kimura 1969 infinite-sites. Distinct
  from filled Tajima and Nei 1984 (pairwise substitution
  distance). Distinct from filled Kimura 1980 K80.
One-sentence prediction: Polymorphism at the nucleotide level
  is pi, the mean pairwise difference per site; net divergence
  subtracts within-population pi.
Assumptions: homologous nucleotide sequences, not chip
  genotypes; sequences are not clone copies; dual
  domestication is not one pairwise split; a cultivar name-
  list is not a population; somatic clone age is not
  evolutionary time.
Which fail here: clones fake pairwise identity and therefore
  fake pi. A nursery block is not a Nei-Li population. Dual
  domestication is two origins. SNP chips are not restriction-
  site sequences. Grafted clones skip the germline clock.
Modern data / statistic: whether wild-sample pi after clone
  + IBD filters is a Nei-Li average pairwise nucleotide
  difference (and whether net delta subtracts within-group
  pi), versus clone IBS or two origins.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset
  after clone + IBD filters. Use as the nucleotide-diversity
  contrast, not as a published Nei-Li-1979 analysis. Do not
  invent a grape nucleotide-diversity paper.
What would falsify it: wild-sample pi is not a Nei-Li
  pairwise-difference estimate after clone filter (clone
  IBS, or two origins). Allele-frequency D remains Nei 1972.
  GST remains Nei 1973. Unbiased H/D remains Nei 1978.
  Tajima D remains 1989. Theta from S remains Watterson 1975.
What we will not claim: that Nei 1972 / 1973 / 1978 is this
  paper (already filled). That Tajima 1989 is this paper.
  That Dong 2023 computed Nei-Li pi. That clone IBS is
  nucleotide diversity.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
