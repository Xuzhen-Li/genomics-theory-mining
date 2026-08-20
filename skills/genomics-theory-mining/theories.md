# Theory notes (filled)

One theory per job. Original paper first. Assumptions, plant/clonal caveats, one modern falsifier.
Do not treat this file as a literature review. Related skill: `plant-lit-review` is the review workflow; this is the revival test.

Citations below were checked against publisher / PubMed / PMC pages. If a paper is not here, it was dropped or left unverified.

---

## Muller's ratchet

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

---

## Nearly-neutral theory

```
Theory: Nearly-neutral theory
Original paper (year): Ohta T. 1973. Slightly deleterious mutant
  substitutions in evolution. Nature 246:96-98.
  DOI 10.1038/246096a0 PMID 4585855.
  (Ohta 1992 Annu Rev Ecol Syst 23:263-286 is a later synthesis, not
  the source of the theory.)
One-sentence prediction: Mutations with |Nes| near 1 are fixed or lost
  by the joint action of drift and weak selection; substitution is faster
  when Ne is small.
Assumptions: a meaningful Ne; Wright-Fisher-like transmission; fitness
  effects drawn such that a large class is slightly deleterious.
Which fail here: a cultivar collection is not one Ne. Clonal census,
  nursery bottlenecks, and dual domestication (table vs wine) split Ne
  across histories. Somatic mutations are not substitutions in the Ohta
  sense until they are transmitted.
Modern data / statistic: wild vs cultivar nucleotide diversity and
  0-fold / 4-fold (or dN/dS) ratios on a broad Vitis WGS panel.
What would falsify it: load or dN/dS does not rise where Ne is smaller
  (wild vs cultivated; wine vs table) after clones are filtered.
Dataset: Dong Y et al. 2023. Dual domestications and origin of traits
  in grapevine evolution. Science. DOI 10.1126/science.add8655
  PMID 36862793. 3525 cultivated and wild accessions; use as an Ne
  contrast, not as a single population.
What we will not claim: that a 12X chip panel of wine clones estimates Ne.
```

---

## Hitchhiking / sweeps

```
Theory: Genetic hitchhiking
Original paper (year): Maynard Smith J, Haigh J. 1974. The hitch-hiking
  effect of a favourable gene. Genetical Research 23(1):23-35.
  DOI 10.1017/s0016672300014634 PMID 4407212.
One-sentence prediction: A strongly favoured substitution reduces
  heterozygosity at linked sites, more so when recombination is low.
Assumptions: sexual recombination map; the favoured allele spreads in a
  population of unrelated individuals; linked sites start near equilibrium.
Which fail here: clones and first-degree pedigrees produce long IBD
  that looks like a sweep. Cultivar relatedness is not a selective sweep.
Modern data / statistic: haplotype homozygosity or diversity dips around
  domestication loci after clone and kinship filters.
Caution dataset (not a proof of Maynard Smith-Haigh): Dong et al. 2023
  Science (DOI 10.1126/science.add8655). 3525-accession WGS reports
  domestication-trait peaks (berry color, hermaphroditism, muscat,
  palatability). Relatedness among cultivars can fake those peaks.
What would falsify it: a candidate sweep around color / sex / flavor
  disappears once clones and IBD / pedigree are removed, or the dip is
  no deeper than matched unselected regions of equal relatedness.
What we will not claim: that Dong 2023 demonstrated hitchhiking.
```

---

## Hill-Robertson interference

```
Theory: Hill-Robertson effect
Original paper (year): Hill WG, Robertson A. 1966. The effect of linkage
  on limits to artificial selection. Genetical Research 8:269-294.
  DOI 10.1017/s0016672300010156.
One-sentence prediction: In finite populations, linked selected loci
  interfere with each other's response to selection; recombination
  reduces that interference.
Assumptions: finite N; two (or more) selected loci; a known recombination
  rate; sexual transmission.
Which fail here: a SNP-chip skeleton is not a recombination map. Clonal
  lineages have no meiotic recombination between cuttings. Interference
  in a grafted clone is not the Hill-Robertson experiment.
Modern data / statistic: efficacy of selection (dN/dS, load, or
  polymorphism) binned by recombination rate on a real Vitis map, in
  sexually derived wild or seedling material (not clone-vs-clone).
What would falsify it: selection efficacy is not weaker in
  low-recombination bins after accounting for gene density and
  mutability.
What we will not claim: that clone SNP density along a chip is
  interference.
```

Felsenstein 1974 (above) already ties this effect to the Fisher-Muller
argument and to the ratchet. Same original math; different job.

---

## Gene balance / dosage (Ohno WGD)

```
Theory: Gene balance / dosage after duplication
Original paper (year): Ohno S. 1970. Evolution by Gene Duplication.
  Springer-Verlag. DOI 10.1007/978-3-642-86659-3.
  Modern statement: Birchler JA, Veitia RA. 2007. The gene balance
  hypothesis: from classical genetics to modern genomics. Plant Cell
  19(2):395-402. DOI 10.1105/tpc.106.049338 PMID 17293565 PMC1867330.
One-sentence prediction: Stoichiometric regulators (transcription
  factors, signaling) are dosage-sensitive; whole-genome duplication
  retains them, while tandem duplicates of the same genes are poorly
  tolerated.
Assumptions: the "dose" is gene copy number in a balanced karyotype;
  aneuploidy != polyploidy; ohnologs can be told from tandem copies.
Which fail here: Vitis is palaeo-hexaploid but not a recent polyploid.
  Hemizygous SVs in clones change dose without WGD. Tandem NLR arrays
  are not the same dosage problem as an ohnolog transcription factor.
Modern data / statistic: retention of TF / signaling ohnologs vs tandem
  NLRs in the grape palaeo-hexaploid gene set.
Dataset: Jaillon O et al. 2007. The grapevine genome sequence suggests
  ancestral hexaploidization in major angiosperm phyla. Nature
  449:463-467. DOI 10.1038/nature06148 PMID 17721507. Three ancestral
  genomes; no recent WGD.
Clone-dose companion: Zhou et al. 2019 Nat Plants 5:965-979
  (DOI 10.1038/s41477-019-0507-8) and Carbonell-Bejerano et al. 2017
  (hemizygous deletion of 313 genes). SVs change dose inside a clone.
What would falsify it: Vitis ohnologs of TF / signaling genes are not
  preferentially retained relative to tandem NLR expansions.
What we will not claim: that every grape gene family expansion is
  dosage balance.
```

---

## Neutral theory (null)

```
Theory: Neutral theory of molecular evolution
Original paper (year): Kimura M. 1968. Evolutionary rate at the
  molecular level. Nature 217:624-626.
  DOI 10.1038/217624a0 PMID 5637732.
One-sentence prediction: Most nucleotide substitutions are the random
  fixation of mutations whose fitness effect is negligible; the
  substitution rate equals the neutral mutation rate.
Assumptions: a large class of truly neutral mutations; substitutions
  counted on an evolutionary (germline / sexual) clock.
Which fail here: "neutral" is the null, not a conclusion. Somatic
  clone SNPs are not substitutions. Methylation-driven C-to-T in
  repeats inflates the apparent clock.
Modern data / statistic: site-frequency or dN/dS of clone-private
  coding SNPs versus intergenic / fourfold sites (Vondras 2019;
  Roach 2018; Callipo 2026).
What would falsify it as a null: clone-private coding SNPs are
  systematically adaptive (not drift / nearly-neutral) after
  mutational-opportunity correction.
What we will not claim: that finding "mostly intergenic SNPs" proves
  Kimura 1968. That is the expected mutational target, not a test.
```

---

## Infinite-sites / Watterson

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

---

## McClintock TE (Vitis extra)

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
