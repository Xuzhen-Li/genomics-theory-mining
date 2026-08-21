# Nei unbiased distance

```
Theory: Nei 1978 unbiased heterozygosity and genetic
  distance
Original paper (year): Nei M. 1978. Estimation of average
  heterozygosity and genetic distance from a small number
  of individuals. Genetics 89(3):583-590 (1 July 1978).
  DOI 10.1093/genetics/89.3.583 PMID 17248844
  PMCID PMC1213855. EuropePMC HTML opened
  (https://europepmc.org/article/MED/17248844): Nei M,
  Center for Demographic and Population Genetics,
  University of Texas at Houston, Texas 77025; 01 Jul
  1978; Genetics 89(3):583-590; DOI; PMID; PMC; abstract.
  Received 1 November 1977; revisions requested 13
  February 1978. Systematic biases in sample
  heterozygosity and sample genetic distances are
  evaluated; formulae for unbiased estimates of average
  heterozygosity and genetic distance are developed. The
  number of individuals needed for average heterozygosity
  can be very small if a large number of loci are studied
  and average heterozygosity is low. The number needed
  for genetic distance can also be very small if the
  distance is large and average heterozygosity of the two
  species compared is low. Distinct from filled Nei 1972
  (defines D from gene identity under isolation; this
  paper is the small-sample unbiased estimator). Distinct
  from filled Nei 1973 GST (diversity partition, not
  distance). Distinct from filled Weir and Cockerham 1984
  (moment FST, not Nei D).
One-sentence prediction: Sample heterozygosity and Nei
  distance are downward-biased in small samples; the 1978
  unbiased formulae recover H and D, and few individuals
  suffice when many loci are scored and H is low.
Assumptions: a sexual sample of individuals, not clone
  copies; loci are independent; a cultivar panel is not
  that sample; dual domestication is not one pairwise
  split; chips are not a large number of independent
  electrophoretic loci.
Which fail here: clones fake identity and heterozygosity.
  Dual domestication is two origins, not one D. A nursery
  name-list is not a small sexual sample. Human transport
  mixes the pairwise comparison.
Modern data / statistic: whether wild / cultivar unbiased
  Nei D after clone + IBD filters is a single-split
  clock, versus two domestication centres or clone IBS.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset
  after clone + IBD filters. Use as the unbiased-D
  contrast, not as a published Nei-1978 analysis. Do not
  invent a grape unbiased-distance paper.
What would falsify it: unbiased D is not a single-split
  clock after clone filter (two origins, or clone IBS).
  The 1972 definition remains the distance job. GST
  remains the 1973 job.
What we will not claim: that Nei 1972 is this paper
  (already filled). That Nei 1973 is this paper. That
  Dong 2023 computed unbiased Nei D. That a cultivar
  name is a species in the 1978 pairwise comparison.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
