# Kimura 1962 fixation probability

```
Theory: Kimura 1962 probability of fixation
Original paper (year): Kimura M. 1962. On the
  probability of fixation of mutant genes in a
  population. Genetics 47:713-719 (June 1962;
  EuropePMC 01 Jun 1962).
  DOI 10.1093/genetics/47.6.713 PMID 14456043
  PMCID PMC1210364. EuropePMC HTML opened
  (https://europepmc.org/article/MED/14456043):
  KIMURA M; 01 Jun 1962; Genetics 47:713-719;
  DOI; PMID; PMC; no abstract there. Seed-lock
  PDF (https://europepmc.org/articles/PMC1210364?pdf=render):
  MOTOO KIMURA, University of Wisconsin, Madison,
  Wisconsin; on leave from the National Institute
  of Genetics, Mishima-shi, Japan; received
  29 January 1962; paper number 391 of NIG;
  Genetics 47:713-719 June 1962. General formula
  for the ultimate fixation probability u(p) from
  the Kolmogorov backward equation, as a function
  of initial frequency p and of the mean M and
  variance V of the gene-frequency change per
  generation. For genic selection,
  u(p) = (1 - exp(-4Nsp)) / (1 - exp(-4Ns));
  for a rare mutant p = 1/(2N) and small s,
  u is about 2s / (1 - exp(-4Ns)); for large N
  and positive s this is about 2s (Haldane 1927);
  as s -> 0, u = 1/(2N). Also treats random
  fluctuation of selection intensity and
  quasi-fixation. Distinct from filled Kimura
  1968 (neutral substitution rate equals mutation
  rate; not the fixation probability). Distinct
  from filled Kimura and Ohta 1969 (4Ne mean time
  to fixation excluding loss). Distinct from
  filled Kimura 1955 (forward drift diffusion /
  heterozygosity decay). Distinct from filled
  Kimura 1969 infinite-sites. Distinct from
  filled Haldane 1927 (mutation-selection
  equilibrium q, and the 2s remark reused here
  as a limit). Kimura 1957 Ann Math Stat is the
  earlier dominance extension; 1962 is the
  general M,V formula and is the lock.
One-sentence prediction: The chance a mutant
  reaches fixation is set by its starting
  frequency and by the mean and variance of
  gene-frequency change; a rare advantageous
  mutant has u about 2s in a large population,
  and a neutral has u = 1/(2N).
Assumptions: a finite sexual (or equivalent)
  population with a meaningful N; a cultivar
  panel is not that N; clone-private SNPs are
  not substitutions on their way to fixation;
  grafted cuttings skip the walk.
Which fail here: a cultivar collection is not
  N. Grafted clones skip the fixation walk.
  Dual domestication is two origins. Human
  choice is not the paper's u. Clone-private
  SNPs are not mutants heading to fixation.
Modern data / statistic: whether a rare
  variant's fixation chance after clone + IBD
  filters is Kimura-1962 u (about 2s or 1/(2N)),
  versus clone age or two origins.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild versus
  cultivar N contrast after clone + IBD
  filters. Vondras 2019 / Roach 2018 as
  clone-clock companions (somatic age is not
  the fixation walk). Use as the fixation-
  probability contrast, not as a published
  grape u analysis. Do not invent a grape
  fixation-probability paper.
What would falsify it: fixation chance is
  not Kimura-1962 u after clone filter (clone
  age, or two origins). Neutral substitution
  rate remains Kimura 1968. Time to fixation
  remains Kimura-Ohta 1969. Drift diffusion
  remains Kimura 1955.
What we will not claim: that Kimura 1968 is
  this paper (already filled). That Kimura
  and Ohta 1969 is this paper. That Kimura
  1955 is this paper. That Dong 2023 estimated
  u. That clone age is a fixation walk.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
