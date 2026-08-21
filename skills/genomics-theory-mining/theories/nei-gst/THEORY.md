# Nei GST

```
Theory: Nei GST (gene-diversity partition)
Original paper (year): Nei M. 1973. Analysis of gene diversity
  in subdivided populations. Proc Natl Acad Sci USA
  70(12):3321-3323 (December 1973; communicated 6 August 1973).
  DOI 10.1073/pnas.70.12.3321 PMID 4519626 PMCID PMC427228.
  EuropePMC HTML opened (https://europepmc.org/article/MED/4519626):
  Nei M; 01 Dec 1973; PNAS 70(12):3321-3323; DOI; PMID; PMC;
  abstract. Gene diversity (heterozygosity) of a subdivided
  population partitions into within- and between-subpopulation
  components; absolute and relative measures of gene
  differentiation among subpopulations are proposed; applicable
  without regard to allele number, mutation / selection /
  migration mix, or reproductive method. Seed-lock PDF
  (https://europepmc.org/articles/PMC427228?pdf=render):
  Center for Demographic and Population Genetics, University of
  Texas at Houston; communicated by Sewall Wright, 6 August
  1973. Gene diversity H (probability two random genes differ)
  of a subdivided population partitions as HT = HS + DST.
  GST = DST/HT is the relative coefficient of gene
  differentiation (equivalent to a weighted-average FST with
  two alleles; works with any number of alleles, any mating
  system, and any mix of mutation, selection, and migration).
  Dm = s DST/(s-1) is the absolute between-subpopulation
  diversity excluding self-comparisons; RST = Dm/HS. The
  partition extends to further hierarchy (HT = HC + DCS +
  DST). Distinct from filled Nei 1972 (genetic distance D from
  gene identity under isolation; not the GST partition).
  Distinct from filled Weir and Cockerham 1984 (moment FST
  estimator). Distinct from filled Wright 1931 (island formula)
  and filled Wright 1943 (continuous IBD). Distinct from filled
  Excoffier, Smouse and Quattro 1992 (AMOVA / phi from
  haplotype distances). Wright 1951 / 1965 F-statistics still
  have no claim text; not the source.
One-sentence prediction: Differentiation is the between-group
  share of total gene diversity (GST = DST/HT), not a
  distance and not Wright's island FST as data.
Assumptions: subpopulations are sexual demes, not clones or
  cultivars; gene identity is not clone IBS; a vineyard is
  not a subpopulation; dual domestication is not one
  hierarchy; chips are not forced-biallelic loci.
Which fail here: clones fake gene identity. A nursery block
  is not a Nei subpopulation. Dual domestication is two
  origins. Human transport mixes patches. SNP chips are
  biallelic.
Modern data / statistic: whether wild-patch GST is a Nei
  HT = HS + DST partition after clone + IBD filters, versus
  clone IBS or two domestication centres.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset after
  clone + IBD filters. Use as the GST contrast, not as a
  published Nei-1973 analysis. Do not invent a grape GST
  paper.
What would falsify it: wild-patch diversity is not a Nei
  GST partition after clone filter (clone IBS, or two
  origins). Distance under isolation remains the Nei 1972
  job; moment FST remains Weir-Cockerham 1984; island FST
  remains Wright 1931; AMOVA remains Excoffier 1992.
What we will not claim: that Nei 1972 is this paper (already
  filled). That Weir and Cockerham 1984 is this paper. That
  Wright 1951 / 1965 is the source. That Dong 2023 computed
  GST. That a cultivar name is a subpopulation.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
