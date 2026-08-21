# Muller's ratchet

```
Theory: Muller's ratchet
Original paper (year): Muller HJ. 1964. The relation of recombination to
  mutational advance. Mutation Research 1:2-9.
  DOI 10.1016/0027-5107(64)90047-8 PMID 14195748.
Named / simulated: Felsenstein J. 1974. The evolutionary advantage of
  recombination. Genetics 78(2):737-756.
  DOI 10.1093/genetics/78.2.737 PMID 4448362 PMC1213231.
One-sentence prediction: In a finite population without recombination, the
  class of genomes with the fewest deleterious mutations is eventually lost
  by drift and cannot be rebuilt, so mutational load ratchets upward.
Assumptions: finite N; mutations mostly deleterious; back-mutation rare;
  no sex / no recombination that restores the least-loaded haplotype.
Which fail here: Vitis cultivars are vegetatively propagated clones (grafted
  meristems), not asexual animals in the Muller sense. Chimeras and diplontic
  selection can hide or purge load. Somatic clock != meiotic clock. Load is
  SNP + SV + TE, not SNPs alone.
Modern data / statistic: clone-private coding variants and predicted
  deleteriousness among vegetatively propagated cultivars.
Lead test bed (not a proof): Vondras AM et al. 2019. The genomic
  diversification of grapevine clones. BMC Genomics 20:972.
  DOI 10.1186/s12864-019-6211-2 PMC6907202. Fifteen Zinfandel clones;
  heterozygous mutations richest in repetitive intergenic / methylated
  cytosine; clones accumulate putatively deleterious exonic variants.
Second test (structural): Carbonell-Bejerano P et al. 2017. Catastrophic
  unbalanced genome rearrangements cause somatic loss of berry color in
  grapevine. Plant Physiol 175:786-801. DOI 10.1104/pp.17.00715
  PMC5619900. Tempranillo Blanco vs Tinto; hemizygous deletion of 313
  genes including the color locus; chromothripsis-like. SNP-only tests
  miss this class of load.
Plant asexual comparator: Lovell JT, Williamson RJ, Wright SI, McKay JK,
  Sharbel TF. 2017. Mutation accumulation in an asexual relative of
  Arabidopsis. PLoS Genet 13(1):e1006550.
  DOI 10.1371/journal.pgen.1006550. Apomictic Boechera accumulate more
  mutations at conserved sites than sympatric sexuals.
What would falsify it: clone-private coding mutations are not enriched for
  deleterious classes, OR the least-loaded haplotype class is continually
  restored (back-mutation, gene conversion, meristem replacement).
What we will not claim: that grape clones are doomed; that Vondras proved
  the ratchet; that Pol epsilon proofreading defects cause a grape ratchet.
```

TESTABLE HUNCH, not a result: leaky Pol epsilon proofreading in meristems
would raise the somatic SNV rate and should speed a ratchet-style click.
No verified grape Pol-e x clone paper was found. Do not publish the hunch
as a finding.

Sister clocks (lineage reconstruction, not ratchet proof):
- Roach MJ et al. 2018. Population sequencing reveals clonal diversity and
  ancestral inbreeding in the grapevine cultivar Chardonnay. PLoS Genet
  14(11):e1007807. DOI 10.1371/journal.pgen.1007807. 15 clones; 1620 markers.
- Carrier G et al. 2012. Transposable elements are a major cause of somatic
  polymorphism in Vitis vinifera L. PLoS ONE 7(3):e32973.
  DOI 10.1371/journal.pone.0032973.
- Callipo P, Robinson H, Schmidt M, Voss-Fels KP. 2026. A dual
  genome-methylome map of clonal evolution in grapevine. Genome Biology.
  DOI 10.1186/s13059-026-04184-x. 23 Pinot noir clones; SNPs/SVs depleted
  from coding sequence; CG/CHG methylation reconstructs clone trees.
- Zhou Y, Minio A, Massonnet M, Solares E, Lv Y, Beridze T, Cantu D,
  Gaut BS. 2019. The population genetics of structural variants in
  grapevine domestication. Nat Plants 5:965-979.
  DOI 10.1038/s41477-019-0507-8. SVs accrue as recessive heterozygotes
  in clonal lineages.

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification
