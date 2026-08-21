# HKA test

```
Theory: HKA test (polymorphism-divergence scaling)
Original paper (year): Hudson RR, Kreitman M, Aguade M.
  1987. A test of neutral molecular evolution based on
  nucleotide data. Genetics 116(1):153-159 (1 May 1987).
  DOI 10.1093/genetics/116.1.153 PMID 3110004 PMC1203113.
  EuropePMC HTML opened (Hudson RR, Kreitman M, Aguade M;
  01 May 1987; Genetics 116(1):153-159; DOI; PMID; PMC;
  abstract). Neutral theory predicts that regions evolving
  at high rates in interspecific comparisons also show high
  polymorphism within species. A conservative test of that
  prediction from at least two regions compared between
  species plus intraspecific polymorphism in the same
  regions; rejected for Adh and 5' flanking sequence in
  D. melanogaster / D. sechellia in a direction consistent
  with balanced polymorphism in the coding region.
  Distinct from filled Kimura 1968 (the neutral null).
  Distinct from filled McDonald and Kreitman 1991 (Dn/Ds
  versus Pn/Ps in a coding alignment). Distinct from
  filled Tajima 1989 (pi versus theta_W in one sample).
  Hudson 1990 Oxford Surveys in Evolutionary Biology
  7:1-44 (coalescent survey) was not opened and is not
  the source. Hudson 2002 Bioinformatics 18:337-338 (ms
  sampler) is a method; not a named theory; not used.
One-sentence prediction: Under neutrality, polymorphism
  and divergence co-vary across loci; a locus with extra
  polymorphism (or extra divergence) relative to another
  rejects the constant-rate neutral model.
Assumptions: comparable loci that are not clones or
  first-degree cuttings; polymorphism is not clone-private
  SNPs; divergence is not a cultivar split; chips are not
  forced-biallelic loci; a real recombination map is not
  required for the two-region test but clone IBD still
  fakes polymorphism.
Which fail here: a cultivar panel is not two species plus
  a random sample. Clone IBD fakes polymorphism. Pedigree
  repeats are not new mutations. Dual domestication is
  human choice, not a species split. SNP chips are
  biallelic.
Modern data / statistic: polymorphism versus divergence
  across loci on Dong-class WGS after clone + IBD filters,
  versus the HKA null. MK and Tajima remain other jobs.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild versus cultivar /
  other Vitis as the divergence contrast after clone + IBD
  filters. Use as an HKA-style test, not as a published
  grape HKA paper. Do not invent a grape HKA paper.
What would falsify it: polymorphism does not scale with
  divergence after clone + IBD filters, OR clone-private
  SNPs are treated as the polymorphism sample (they are
  not). Coding MK is the 1991 job; one-sample Tajima D
  is the 1989 job.
What we will not claim: that McDonald and Kreitman 1991
  is this paper (already filled). That Tajima 1989 is this
  paper. That Hudson 1990 or Hudson 2002 is the source.
  That Dong 2023 ran HKA.
```

---

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
