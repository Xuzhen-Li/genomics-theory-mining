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

---

## Background selection

```
Theory: Background selection
Original paper (year): Charlesworth B, Morgan MT, Charlesworth D. 1993.
  The effect of deleterious mutations on neutral molecular variation.
  Genetics 134(4):1289-1303. DOI 10.1093/genetics/134.4.1289
  PMID 8375663 PMC1205596.
One-sentence prediction: Selection against recurrent deleterious alleles
  reduces linked neutral diversity; the reduction is strongest with
  little or no recombination (and in asexuals or selfers) and is an
  exponential function of the deleterious mutation rate in that segment.
Assumptions: a meaningful recombination map; mutation-selection
  balance at many linked loci; the observed diversity is sexual /
  meiotic, not clone-IBD.
Which fail here: a SNP-chip skeleton is not a recombination map.
  Grafted clones have no meiosis between cuttings. Gene density and
  mutability covary with recombination and can fake a BGS dip.
Modern data / statistic: nucleotide diversity in recombination-rate
  bins on a real Vitis map, after gene-density and mutability control,
  in sexually derived wild or seedling material (not clone-vs-clone).
What would falsify it: diversity is not reduced in low-recombination
  bins after gene-density (and mutability) control.
What we will not claim: that a clone SNP-density track is background
  selection. That is the Hill-Robertson / hitchhiking caution again.
```

Same map requirement as Hill-Robertson. Different job: BGS is the
deleterious-linked null for a diversity dip, not interference among
selected loci.

---

## Meselson effect (allelic divergence in asexuals)

```
Theory: Meselson effect (allelic divergence without sex)
Original paper (year): Mark Welch DB, Meselson M. 2000. Evidence for
  the evolution of bdelloid rotifers without sexual reproduction or
  genetic exchange. Science 288(5469):1211-1215.
  DOI 10.1126/science.288.5469.1211 PMID 10817991.
  This is the molecular TEST of allelic divergence, not a 1960s
  original. Do not cite it as the source of asexuality theory.
One-sentence prediction: After long enough without sex or genetic
  exchange, formerly allelic haplotypes become highly divergent and
  the genome lacks pairs of closely similar sequences.
Assumptions: obligate asexuality for a deep time; no ameiotic
  homogenization; the two copies started as alleles, not ohnologs.
Which fail here: grape cultivars are heterozygous diploids with rare
  sex in the pedigree, not bdelloids. Standing heterozygosity from
  the last outcross is not Meselson divergence. Roach 2018 reports
  ancestral inbreeding in Chardonnay, which cuts the opposite way
  (too little, not too much, haplotype divergence).
Modern data / statistic: haplotype / allelic divergence in old
  vegetatively propagated clones versus sexual wild Vitis, after
  subtracting standing heterozygosity at the last sexual node.
Caution dataset: Roach MJ et al. 2018. PLoS Genet 14(11):e1007807
  (DOI 10.1371/journal.pgen.1007807). 15 Chardonnay clones; ancestral
  inbreeding. Use as a CAUTION, not as a Meselson demonstration.
What would falsify it: haplotype divergence in old clones is not
  higher than in sexual wilds after accounting for standing
  heterozygosity.
What we will not claim: that a grape clone is an ancient asexual;
  that Flot 2013 bdelloid genomics is a Vitis result (dropped).
```

---

## Organelle / plastid Muller ratchet

```
Theory: Muller ratchet in non-recombining organelles
Original paper (year): Muller HJ. 1964. The relation of recombination
  to mutational advance. Mutat Res 1:2-9.
  DOI 10.1016/0027-5107(64)90047-8 PMID 14195748.
  Organelle application (locked): Lynch M. 1996. Mutation accumulation
  in transfer RNAs: molecular evidence for Muller's ratchet in
  mitochondrial genomes. Mol Biol Evol 13(1):209-220.
  DOI 10.1093/oxfordjournals.molbev.a025557 PMID 8583893.
  Lynch 1996 is animal mitochondrial tRNA, not a chloroplast paper
  and not a grape paper.
One-sentence prediction: A non-recombining organelle haplotype cannot
  restore a least-loaded class once it is lost, so mildly deleterious
  substitutions accumulate relative to a recombining nuclear control.
Assumptions: no (or rare) organelle recombination / paternal leakage
  that rebuilds the clean class; a nuclear comparison with a known
  mutation-rate difference; the organelle sample is not one clone.
Which fail here: plastid inheritance in Vitis is typically maternal,
  but biparental leakage and intracellular gene conversion are not
  ruled out by a haplotype label. A cultivar collection is not Ne.
  No grape plastid population-genetic paper was locked for this skill.
Modern data / statistic (dataset type only): complete plastid
  assemblies or haplotype alignments of Vitis, scored for coding
  load or tRNA-stem stability versus nuclear genes after a
  mutation-rate correction.
What would falsify it: plastid coding / tRNA sites are not
  excess-deleterious relative to nuclear genes after mutation-rate
  correction, OR a least-loaded plastid class is continually restored.
What we will not claim: that Lynch 1996 measured grape plastids;
  that a published grape chlorotype paper is a ratchet test (none
  was locked). Do not invent a Vitis plastid popgen citation.
```

---

## Bateson-Dobzhansky-Muller incompatibilities

```
Theory: Bateson-Dobzhansky-Muller hybrid incompatibilities
Original paper (year): Dobzhansky T. 1937. Genetics and the Origin
  of Species. Columbia University Press. Book. Isolating mechanisms
  and hybrid incompatibility as two-locus (or multi-locus) products
  of divergence, not a single substitution that is unfit in the
  ancestor.
  Muller 1942 was not locked on a publisher page and is not cited.
  Bateson 1909 was not locked as the two-locus source and is not cited.
One-sentence prediction: Hybrid inviability or sterility is caused
  by incompatible alleles at two or more loci that never co-occurred
  in either parent lineage.
Assumptions: the parents are diverged populations / species; the
  hybrid phenotype is genetic, not graft incompatibility or virus;
  a single-locus model can be rejected.
Which fail here: a cultivar x cultivar cross is not a species cross.
  Rootstock "failure" can be soil, virus, or graft, not BDM.
  Unreduced gametes and ploidy in Vitis hybrids are not two-locus
  epistasis.
Modern data / statistic (dataset type only): Vitis interspecific
  hybrids (V. vinifera x V. riparia / V. rupestris / V. amurensis)
  or a mapping family from those crosses, scored for inviability /
  sterility QTL. No grape BDM mapping paper was locked.
What would falsify it: hybrid inviability maps to a single locus,
  not two-locus (or multi-locus) BDM.
What we will not claim: that every failed vinifera x American
  rootstock cross is a Dobzhansky incompatibility.
```

---

## DDC / subfunctionalization

```
Theory: Duplication-degeneration-complementation (subfunctionalization)
Original paper (year): Force A, Lynch M, Pickett FB, Amores A,
  Yan YL, Postlethwait J. 1999. Preservation of duplicate genes by
  complementary, degenerative mutations. Genetics 151(4):1531-1545.
  DOI 10.1093/genetics/151.4.1531 PMID 10101175 PMC1460548.
One-sentence prediction: Complementary degenerative mutations
  partition ancestral subfunctions so both duplicates are required;
  preservation need not wait for a new function.
Assumptions: independently mutable subfunctions (often regulatory);
  ohnologs can be told from tandem copies; "partitioned" is scored
  against the ancestral expression / function, not against a
  present-day singleton.
Which fail here: Vitis is palaeo-hexaploid; many "ohnologs" are
  old. Retention by dosage balance (Ohno / Birchler) is a different
  job. Tandem NLR arrays are not DDC.
Modern data / statistic: partitioned expression or function in
  palaeo-hexaploid ohnolog pairs versus randomly retained pairs.
Dataset: Jaillon O et al. 2007. Nature 449:463-467.
  DOI 10.1038/nature06148 PMID 17721507. Three ancestral genomes;
  no recent WGD. Use the ohnolog set. Do not invent a grape
  expression-atlas paper.
What would falsify it: ohnolog pairs do not show partitioned
  expression or function versus randomly retained pairs.
What we will not claim: that every retained grape duplicate is
  DDC (gene-balance is the alternative filled note).
```

---

## Selfish DNA

```
Theory: Selfish DNA
Original papers (year): Doolittle WF, Sapienza C. 1980. Selfish
  genes, the phenotype paradigm and genome evolution. Nature
  284:601-603. DOI 10.1038/284601a0 PMID 6245369.
  Orgel LE, Crick FHC. 1980. Selfish DNA: the ultimate parasite.
  Nature 284:604-607. DOI 10.1038/284604a0 PMID 7366731.
  Same issue; cite both. Neither is a review of the other.
One-sentence prediction: Sequences can spread because they replicate
  inside the genome; no organismal function is required to explain
  their existence.
Assumptions: transposition (or other non-phenotypic survival) is
  demonstrated; "function" is not assumed from presence.
Which fail here: a few TE insertions are domesticated (promoters,
  color sports). Domestication of some copies does not make the
  insertion class adaptive. Scoring only SNPs hides the TE clock.
Modern data / statistic: clone-private TE insertions versus
  adaptive / domesticated annotations in the same cultivar.
Datasets: Carrier et al. 2012 PLoS ONE 7(3):e32973 (147 mobile-
  element insertion events in Pinot noir; TE the largest scored
  class). Vondras et al. 2019 BMC Genomics 20:972 (TE insertions
  among Zinfandel clones).
What would falsify it: TE insertions are systematically
  domesticated or adaptive, not mostly insertion-class load.
What we will not claim: that McClintock 1950 is the selfish-DNA
  paper (different job: mutable alleles). That every berry-color
  sport is a TE (Carbonell-Bejerano 2017 is a rearrangement).
```

---

## Baker's law

```
Theory: Baker's law (self-compatible colonists)
Original paper (year): Baker HG. 1955. Self-compatibility and
  establishment after long-distance dispersal. Evolution
  9(3):347-349. DOI 10.1111/j.1558-5646.1955.tb01544.x
  (also 10.2307/2405656). Pages are sometimes listed 347-348.
One-sentence prediction: After long-distance dispersal, uniparental
  (self-compatible or hermaphrodite) colonists establish more
  readily than self-incompatible or obligately outcrossing ones.
Assumptions: a true colonization step with a mate-finding problem;
  the self-compatible state is derived in the colonists, not
  already fixed in the source.
Which fail here: a nursery or a grafted vineyard is not an oceanic
  island. Humans move both sexes and cuttings. Wild V. sylvestris
  is dioecious; cultivated V. vinifera is mostly hermaphrodite,
  but some wild accessions already carry hermaphrodite haplotypes.
Modern data / statistic: frequency of hermaphrodite sex-locus
  genotypes in wild sylvestris versus cultivars, and whether the
  chromosome-2 sex-determination-region (SDR) sweep survives
  clone and IBD filters.
Dataset: Dong Y et al. 2023. Science. DOI 10.1126/science.add8655
  PMID 36862793. Dual domestications; SDR on chromosome 2;
  hermaphrodite haplotypes (H1, H2 and rarer H types) from
  recombination between male (M) and female (f). Some sylvestris
  accessions in that panel already carry H haplotypes. Use as a
  caution dataset, not a proof of Baker 1955.
What would falsify it: wild sylvestris is already hermaphrodite
  at the same rate as cultivars, OR the sex-locus sweep vanishes
  after IBD / clone filters.
What we will not claim: that VviAGL11 is the sex gene (that name
  is used for seedlessness, not the SDR). That Dong 2023 proved
  Baker's law.
```

---

## Isolation by distance

```
Theory: Isolation by distance
Original paper (year): Wright S. 1943. Isolation by distance.
  Genetics 28(2):114-138. DOI 10.1093/genetics/28.2.114
  PMID 17247074 PMC1209196.
One-sentence prediction: Under limited dispersal, genetic
  similarity declines with geographic distance; the slope is set
  by the neighborhood size.
Assumptions: isolation-by-distance in a continuous or stepping-
  stone sexual population; distance is geographic, not river-km
  or road-km unless you model those as the dispersal kernel;
  samples are not clones or cultivars.
Which fail here: humans and rivers move grapevines. A cultivar
  panel has no geography in the Wright sense. feral vines are
  not wild sylvestris.
Modern data / statistic: isolation-by-distance slope (FST or
  relatedness versus kilometers) in wild V. sylvestris, after
  dropping cultivars, feral escapes, and clones.
Dataset: Dong et al. 2023 Science (DOI 10.1126/science.add8655).
  3525-accession WGS includes wild sylvestris. Use the wild
  subset as a geography test, not the cultivar cloud.
What would falsify it: the isolation-by-distance slope is zero
  after accounting for river and human transport.
What we will not claim: that a wine-region PCA is Wright 1943.
```

---

## Diplontic selection (optional extra)

```
Theory: Diplontic / developmental selection in meristems
Original paper (year): Klekowski EJ. 1988. Mutation, Developmental
  Selection, and Plant Evolution. Columbia University Press.
  DOI 10.7312/klek92068. Book. Cell-lineage competition in
  meristems can purge or fix somatic mutations before they become
  the shoot.
One-sentence prediction: Within a growing plant, cell lineages
  that carry deleterious somatic mutations lose meristem space, so
  the transmitted shoot is cleaner than the raw somatic mutation
  rate.
Assumptions: a structured meristem (layers, initials); a fitness
  effect at the cell or sector level; the mutation is visible to
  that competition (many recessives are not).
Which fail here: grape shoots are chimeric; a sport can be a
  layer-restricted mutant that diplontic selection did not purge.
  Recessive load is invisible in a diploid meristem. Nursery
  selection on cuttings is not Klekowski's cell-lineage filter.
Modern data / statistic: clone-private coding mutations versus
  intergenic / fourfold sites in the same vegetatively propagated
  cultivar (Vondras 2019; Callipo 2026 reports SNPs/SVs depleted
  from coding sequence — a test bed, not a proof).
Companion: Carbonell-Bejerano et al. 2017 (layer-visible
  rearrangement that survived as a color sport).
What would falsify it: clone-private coding mutations are not
  depleted relative to intergenic sites after mutational-
  opportunity correction, OR chimeric load is freely transmitted.
What we will not claim: that coding depletion in Callipo 2026
  proved diplontic selection (constraint and methylation are
  alternatives). That diplontic selection cancels Muller's ratchet
  (it is a caveat in that note, not a replacement).
```

---

## Coalescent (Kingman)

```
Theory: Kingman coalescent
Original paper (year): Kingman JFC. 1982. The coalescent.
  Stochastic Processes and their Applications 13(3):235-248.
  DOI 10.1016/0304-4149(82)90011-4. Continuous-time Markov
  chain on a sample of n members from a large haploid
  population; binary mergers only.
One-sentence prediction: Genealogies of a random sample from
  a large haploid population are binary trees with exponential
  waiting times (the n-coalescent); they are not multiple-merger
  or pedigree stars.
Assumptions: large haploid (or effective-haploid) population;
  a random sample of unrelated individuals; Kingman (binary)
  mergers, not Lambda / multiple-merger coalescents.
Which fail here: Vitis cultivars are grafted clones and close
  pedigrees. A clone panel is not a random sexual sample.
  Identity-by-descent among cuttings produces star-like or
  multiple-merger genealogies that are not Kingman.
Modern data / statistic: inferred tree shape or multiple-merger
  signal in clone and first-degree pedigree samples versus a
  clone-filtered wild sexual sample.
Datasets: Roach et al. 2018 PLoS Genet 14(11):e1007807
  (15 Chardonnay clones; ancestral inbreeding). Vondras et al.
  2019 BMC Genomics 20:972 (15 Zinfandel clones). Dong et al.
  2023 Science (DOI 10.1126/science.add8655) already dropped
  IBS clones before population analyses; that filter is the
  first step, not a Kingman proof.
What would falsify it: clone / pedigree samples still yield
  Kingman (binary, unrelated) genealogies after relatedness
  is scored.
What we will not claim: that every grape tree that is not
  binary disproves Kingman in wild sylvestris. State the
  sample class.
```

---

## Infinite-alleles

```
Theory: Infinite-alleles model
Original paper (year): Kimura M, Crow JF. 1964. The number
  of alleles that can be maintained in a finite population.
  Genetics 49(4):725-738. DOI 10.1093/genetics/49.4.725
  PMID 14156929 PMC1210609.
One-sentence prediction: Each mutation creates a new allele,
  so identity-by-state is identity-by-descent; the effective
  number of alleles is 4Ne u + 1 under neutrality.
Assumptions: an astronomically large allelic state space;
  back-mutation / recurrent mutation negligible; a finite
  sexual population with a meaningful Ne.
Which fail here: SNP chips ascertain a finite, recurrent
  state space (mostly biallelic). Same-site SNPs and TE
  family insertions are recurrent. A cultivar collection
  is not one Ne. Identity-by-state among clones is not
  identity-by-descent in the Kimura-Crow sense.
Modern data / statistic: recurrent same-site or same-element
  events, and IBS versus IBD, on cultivar chips or WGS
  after clone filters.
Datasets: Carrier et al. 2012 PLoS ONE 7(3):e32973 (recurrent
  TE insertions in Pinot noir). Vondras et al. 2019 BMC
  Genomics 20:972 (TE plus methylation-driven transitions
  among Zinfandel clones). Dong et al. 2023 Science (WGS;
  they already used IBS to collapse clone genotypes).
  Do not invent a grape chip-ascertainment paper.
What would falsify it: identity-by-state on Vitis chips
  (or WGS SNPs) behaves as infinite-alleles after clones
  are filtered — recurrent SNPs and ascertainment are
  rare enough not to matter.
What we will not claim: that infinite-alleles is the same
  job as infinite-sites (that note is already filled).
```

---

## Molecular clock

```
Theory: Molecular clock
Original paper (year): Zuckerkandl E, Pauling L. 1962.
  Molecular disease, evolution, and genic heterogeneity.
  In: Kasha M, Pullman B, eds. Horizons in Biochemistry.
  Academic Press, New York / London. Chapter begins p. 189
  (next chapter p. 229 in the 1962 volume table of contents;
  archive scan of the book). Book chapter.
  Expanded statement: Zuckerkandl E, Pauling L. 1965.
  Evolutionary divergence and convergence in proteins.
  In: Bryson V, Vogel HJ, eds. Evolving Genes and Proteins.
  Academic Press. pp. 97-166.
  DOI 10.1016/B978-1-4832-2734-4.50017-6.
  (Zuckerkandl and Pauling 1965 J. Theor. Biol. 8:357-366,
  "Molecules as documents of evolutionary history", is a
  different paper and is not cited as the clock source.)
One-sentence prediction: Sequence difference between
  lineages accumulates roughly linearly with elapsed time
  on a germline / sexual clock, so divergence dates
  molecules.
Assumptions: a roughly constant substitution rate on the
  clock being dated; substitutions, not somatic SNPs;
  the compared lineages share a sexual / meiotic clock.
Which fail here: somatic mutation in grafted clones is
  not the germline clock. Methylation-driven C-to-T in
  repeats inflates the clone clock. A cultivar panel is
  not elapsed speciation time.
Modern data / statistic: somatic SNV / SV rate among
  vegetatively propagated clones versus divergence among
  sexual wild sylvestris on the same site classes.
Datasets: Vondras et al. 2019 BMC Genomics 20:972 and
  Roach et al. 2018 PLoS Genet 14(11):e1007807 (clone
  clocks). Wild contrast: Dong et al. 2023 Science
  (sylvestris subset). Callipo et al. 2026 Genome Biol
  is a sister clone / methylome clock only, not a
  germline-clock proof.
What would falsify it: the somatic clone clock equals
  the germline / sexual clock (Vondras / Roach versus
  wild sylvestris) on matched site classes.
What we will not claim: that a clone tree dated in
  years since planting is Zuckerkandl-Pauling.
```

---

## McDonald-Kreitman

```
Theory: McDonald-Kreitman test
Original paper (year): McDonald JH, Kreitman M. 1991.
  Adaptive protein evolution at the Adh locus in
  Drosophila. Nature 351:652-654.
  DOI 10.1038/351652a0 PMID 1904993.
One-sentence prediction: Under neutrality, the ratio of
  replacement to synonymous differences fixed between
  species equals the ratio of replacement to synonymous
  polymorphisms within species; excess fixed replacements
  reject neutrality (MK alpha).
Assumptions: "fixed differences" are substitutions
  between species or diverged populations; polymorphisms
  are within a sexual population; clones are not a species.
Which fail here: clone-private variants are not
  substitutions. A cultivar panel is not Drosophila
  melanogaster versus simulans. Domestication loci are
  not automatically between-species fixed differences.
Modern data / statistic: MK tables at domestication
  loci after clone and IBD filters, counting only
  variants that are fixed between wild sylvestris and
  cultivated groups (not clone-private SNPs).
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). 3525-accession WGS;
  domestication-trait peaks exist. Do not invent a
  published grape MK paper.
What would falsify it: MK alpha on clone-private
  variants is treated as meaningful (it is not), OR
  after clone / IBD filters, grape MK does not reject
  neutrality at domestication loci.
What we will not claim: that Dong 2023 computed MK
  alpha. That clone-private missense SNPs are
  substitutions.
```

---

## Tajima's D

```
Theory: Tajima's D
Original paper (year): Tajima F. 1989. Statistical
  method for testing the neutral mutation hypothesis
  by DNA polymorphism. Genetics 123(3):585-595.
  DOI 10.1093/genetics/123.3.585 PMID 2513255
  PMC1203831.
One-sentence prediction: Under the neutral mutation
  model, theta from pairwise differences (pi) equals
  theta from segregating sites (theta_W); D measures
  that difference and is near zero at equilibrium.
Assumptions: a random sexual sample; infinite sites;
  no relatedness structure that inflates rare or
  shared haplotypes; the sample is one population.
Which fail here: cultivar panels are clones and
  pedigrees. Relatedness and recent bottlenecks
  produce strongly negative D that looks like a
  sweep. A chip skeleton is not a random sample
  of sites.
Modern data / statistic: genome-wide or
  domestication-locus Tajima's D in cultivar panels
  before versus after clone and IBD / pedigree
  filters, versus wild sylvestris.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). They already
  collapsed IBS clones. Use as a relatedness caution,
  not as a published Tajima result. Do not invent
  a grape Tajima paper.
What would falsify it: strongly negative D in
  cultivar panels vanishes after clone + IBD
  filters (relatedness, not a sweep).
What we will not claim: that negative D in wine
  clones is a selective sweep. That is the
  hitchhiking caution again.
```

---

## Mutation accumulation

```
Theory: Mutation accumulation
Original paper (year): Mukai T. 1964. The genetic
  structure of natural populations of Drosophila
  melanogaster. I. Spontaneous mutation rate of
  polygenes controlling viability. Genetics
  50(1):1-19. DOI 10.1093/genetics/50.1.1
  PMID 14191352 PMC1210633. Chromosomes sheltered
  from selection accumulate viability-reducing
  mutations.
  Plant comparator (not the original): Lovell JT
  et al. 2017. Mutation accumulation in an asexual
  relative of Arabidopsis. PLoS Genet 13(1):e1006550.
  DOI 10.1371/journal.pgen.1006550.
One-sentence prediction: When selection is relaxed,
  mildly deleterious mutations accumulate and mean
  fitness / viability declines; the least-loaded
  class is not restored.
Assumptions: a sheltered chromosome or asexual
  lineage; mutations are mostly deleterious;
  fitness is scored on the sheltered haplotype,
  not on a chimeric shoot.
Which fail here: grape clones are diploid meristems
  with diplontic selection and chimeras. Somatic
  load is not a Mukai second-chromosome cage.
  Nursery selection on cuttings is not relaxed
  in the Mukai sense.
Modern data / statistic: clone-private coding
  load and predicted deleteriousness after
  diplontic / chimera correction, versus
  intergenic / fourfold sites.
Lead test bed (not a proof): Vondras et al. 2019
  BMC Genomics 20:972. Companion structural load:
  Carbonell-Bejerano et al. 2017 Plant Physiol
  175:786-801. Plant asexual comparator: Lovell
  2017 (Boechera).
What would falsify it: clone-private load is not
  enriched for deleterious classes after diplontic
  / chimera correction, OR the least-loaded class
  is continually restored.
What we will not claim: that Vondras proved Mukai
  in grape. That this note replaces Muller's
  ratchet (different job: MA is the experiment;
  the ratchet is the irreversible loss of the
  least-loaded class).
```

---

## Genetic draft

```
Theory: Genetic draft (pseudohitchhiking)
Original paper (year): Gillespie JH. 2000. Genetic
  drift in an infinite population. The
  pseudohitchhiking model. Genetics 155(2):909-919.
  DOI 10.1093/genetics/155.2.909 PMID 10835409
  PMC1461093. Names "genetic draft" for the
  stochastic effects of linked substitutions at
  a closely linked neutral locus.
  (Gillespie 2001 Evolution 55:2161-2169 is a
  later population-size paper, not the naming
  source.)
One-sentence prediction: Recurrent selected
  substitutions induce drift-like stochasticity
  at linked neutral sites even when N is infinite;
  the coalescent has a random number of branches
  at nodes and the frequency spectrum departs
  from the equilibrium neutral model.
Assumptions: recurrent sweeps (not one hitchhiking
  event); a recombination map; the diversity
  pattern is sexual / meiotic, not clone-IBD.
Which fail here: a SNP-chip skeleton is not a
  recombination map. Clone IBD looks like draft.
  Background selection is the deleterious-linked
  null for the same diversity dip (already filled).
  A single domestication sweep is hitchhiking
  (Maynard Smith and Haigh), not draft.
Modern data / statistic: diversity versus
  recombination on a real Vitis map, after gene-
  density control and clone / IBD filters, in
  sexually derived wild or seedling material.
What would falsify it: the linked diversity
  pattern in Vitis is explained by recombination
  / background selection, not by recurrent sweeps
  / draft.
What we will not claim: that a cultivar diversity
  dip is Gillespie draft. That draft replaces
  hitchhiking or BGS (three different jobs).
```

---

## Introgression / hybrid swarm

```
Theory: Introgressive hybridization / hybrid swarm
Original paper (year): Anderson E. 1949.
  Introgressive Hybridization. John Wiley and
  Sons, New York. Book. Pp. ix + 109 (locked from
  the 1950 Nature review of the book). Repeated
  backcrossing moves genes from one species into
  another; hybrid swarms are the visible mix.
One-sentence prediction: After hybridization,
  repeated backcrossing leaves geographically
  clinal tracts of heterospecific ancestry, not
  a one-off F1.
Assumptions: the parents are distinguishable
  populations / species; tracts are ancestry,
  not shared IBD among relatives; geography
  is the test, not a cultivar PCA.
Which fail here: humans move vines. Cultivar
  relatedness and clones fake introgression
  tracts. A nursery hybrid is not a hybrid
  swarm. Feral vines are not wild sylvestris.
Modern data / statistic: putative introgression
  tracts and their geographic cline in wild
  sylvestris or in clone-filtered cultivated
  groups, after IBD / clone filters.
Caution dataset (not a proof of Anderson 1949):
  Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). TreeMix and
  D-statistics report gene flow from Syl-W into
  CG3-CG6 after CG1-related Western Asia
  domesticates entered Europe (~11-18% Syl-W
  in those groups; a further pulse into CG6).
  They already collapsed IBS clones. Relatedness
  among remaining cultivars can still fake
  tracts. Use as CAUTION.
What would falsify it: putative introgression
  tracts vanish after IBD / clone filters, or
  they are not geographically clinal.
What we will not claim: that Dong 2023 proved
  Anderson 1949. That a CG1-to-Syl-W arrow is
  the paper's TreeMix result (the reported
  edges run from Syl-W into cultivated groups).
```

---

## Haldane's rule

```
Theory: Haldane's rule
Original paper (year): Haldane JBS. 1922. Sex
  ratio and unisexual sterility in hybrid animals.
  Journal of Genetics 12(2):101-109.
  DOI 10.1007/BF02983075. IAS Journal of Genetics
  page locked: "When in the F1 offspring of a
  cross between two animal species or races one
  sex is absent, rare, or sterile, that sex is
  always the heterozygous sex."
One-sentence prediction: In animal interspecific
  hybrids, the sex that is absent, rare, or
  sterile is the heterozygous (digametic) sex.
Assumptions: a heterogametic sex (XX/XY or
  ZW/ZZ) whose sex chromosomes are unpaired in
  one sex; the sterility is that sex, not both;
  the cross is an animal hybrid.
Which fail here: this does not map onto Vitis
  SDR. Grape is not XX/XY or ZW in the Haldane
  sense. Sex is a small sex-determination region
  on chromosome 2 (Dong 2023); wild sylvestris
  is dioecious (male M/f, female f/f) and
  cultivated vines are mostly hermaphrodite.
  There is no heterogametic sex whose hybrids
  are the sterile class.
Modern data / statistic: none that tests
  Haldane in grape. Interspecific Vitis hybrid
  sterility, if scored, is not a heterogametic-
  sex contrast.
What would falsify it: not applicable as a
  grape test. The note is filled as "does not
  map onto Vitis SDR" rather than as an
  invented sterility experiment.
What we will not claim: that grape interspecific
  hybrids show Haldane's rule. That the SDR is
  a Y chromosome in the animal sense. That
  VviAGL11 is the sex gene.
```

---

## Stepping-stone model

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

---

## Island model

```
Theory: Island model
Original paper (year): Wright S. 1931. Evolution in Mendelian
  populations. Genetics 16(2):97-159.
  DOI 10.1093/genetics/16.2.97 PMID 17246615 PMC1201091.
  Named: Wright 1943 Genetics 28:114-138 (already filled as IBD)
  writes "we shall refer to it as the island model" and cites
  1931 for the math. Lock 1931 as the source, the same way
  Muller 1964 is the ratchet math and Felsenstein 1974 named it.
  Distinct from filled IBD: island / continent-island has no
  distance. Every deme draws migrants from the same pool.
  FST ~ 1 / (1 + 4Nem). IBD is the distance-dependent
  alternative Wright himself set against this model.
One-sentence prediction: Among equal demes that exchange
  migrants with a common pool (not with neighbors only),
  differentiation is a function of Nem and does not increase
  with geographic distance.
Assumptions: equal demes; a common migrant pool (not neighbor-
  only); no distance dependence of FST; samples are demes,
  not pedigrees or cultivars.
Which fail here: a vineyard is not an island. Nursery stock
  and rivers violate the equal-m pool. Cultivar panels are
  pedigrees, not demes.
Modern data / statistic: FST among wild V. sylvestris patches
  versus geographic distance after river / human transport
  is controlled.
Dataset: Dong et al. 2023 Science (DOI 10.1126/science.add8655).
  Wild sylvestris subset after clone filter.
What would falsify it: FST among wild patches is not
  independent of distance after river / human transport is
  controlled (nonzero IBD slope kills the island null; that
  is Wright's own 1943 contrast).
What we will not claim: that a vineyard block is an island
  deme. That this note replaces Wright 1943 IBD (Wright
  himself set the two models against each other).
```

---

## Clonal interference

```
Theory: Clonal interference
Original paper (year): Gerrish PJ, Lenski RE. 1998. The fate
  of competing beneficial mutations in an asexual population.
  Genetica 102:127-144 (often cited 102/103:127-144; Springer
  landing is vol. 102). DOI 10.1023/A:1017067816551.
  No PMID on the Springer page.
  Not the original: Muller HJ. 1932. Some genetic aspects of
  sex. Am Nat 66:118-138. Precursor for the advantage of
  recombination / ratchet, already dropped as a ratchet
  original. Gerrish and Lenski name "clonal interference"
  and derive the fixation / substitution results.
  Distinct from filled Hill-Robertson: HR is interference
  among linked selected loci with recombination. CI is the
  asexual case: competing beneficials cannot recombine onto
  one haplotype, so the weaker is lost.
One-sentence prediction: In a finite asexual population,
  beneficial mutations that arise on different clones compete;
  the weaker is driven out before fixation, so the substitution
  rate saturates with N and U_b.
Assumptions: finite N; asexual transmission; two (or more)
  competing beneficials on different haplotypes; no
  recombination that joins them.
Which fail here: a grafted cultivar is asexual between
  cuttings, but the "population" is a nursery of cuttings
  from one founder, not an E. coli chemostat. Most scored
  grape sports are single-locus (color, hair) on one clone,
  not two competing beneficials in one finite N.
Modern data / statistic: clone-private putatively beneficial
  (or phenotype-changing) mutations across sister clones;
  test for mutual exclusion of competitor classes.
Datasets: Vondras et al. 2019 BMC Genomics 20:972; Roach
  et al. 2018 PLoS Genet 14(11):e1007807; Carrier et al.
  2012 PLoS ONE 7(3):e32973. Clone panels.
What would falsify it: clone-private putatively beneficial
  (or phenotype-changing) mutations do not show mutual
  exclusion across sister clones (both persist; no lost
  competitor class). A single-sport color loss (not two
  competing sports) is not CI.
What we will not claim: that a color sport is clonal
  interference. That this note replaces Hill-Robertson
  (different job: asexual competing beneficials vs linked
  selected loci with recombination).
```

---

## Allele surfing / range expansion

```
Theory: Allele surfing / range expansion
Original paper (year): Edmonds CA, Lillie AS, Cavalli-Sforza
  LL. 2004. Mutations arising in the wave front of an
  expanding population. Proc Natl Acad Sci USA 101(4):975-979.
  DOI 10.1073/pnas.0308064100 PMID 14732681 PMC327127.
  Named "surfing": Klopfstein S, Currat M, Excoffier L. 2006.
  The fate of mutations surfing on the wave of a range
  expansion. Mol Biol Evol 23(3):482-490.
  DOI 10.1093/molbev/msj057 PMID 16280540. Later name, not
  the source. Lande is not this claim (quantitative genetics
  / founder effect, not wave-front surfing).
One-sentence prediction: A mutation that arises (or is
  sampled) at the front of a range expansion can reach a
  much higher frequency and wider spatial range than the
  same mutation in a stationary population, by repeated
  founder events.
Assumptions: a single expanding front; the mutation is
  sampled at the wave front; geography is the expansion,
  not human transport or dual domestication.
Which fail here: domestication is not a single expanding
  front. Dual domestication (Dong 2023 table vs wine) and
  human transport break the wave. Cultivar relatedness
  fakes a front-to-core cline.
Modern data / statistic: frequency of alleles at a putative
  expansion edge of wild or early-cultivated Vitis versus
  core frequencies, after clone + IBD filters, versus
  matched non-expansion alleles.
Dataset: Dong et al. 2023 Science (DOI 10.1126/science.add8655).
What would falsify it: high-frequency alleles at the
  putative expansion edge of wild or early-cultivated
  Vitis are not in excess of core frequencies after clone
  + IBD filters, or the excess is no larger than matched
  non-expansion alleles (surfing null dies; selection /
  pedigree remains).
What we will not claim: that a cultivar relatedness cline
  is surfing. That Klopfstein 2006 is the source (it named
  the phenomenon).
```

---

## Genome shock

```
Theory: Genome shock
Original paper (year): McClintock B. 1984. The significance
  of responses of the genome to challenge. Science
  226(4676):792-801. DOI 10.1126/science.15739260
  PMID 15739260. Nobel lecture 8 December 1983, Karolinska
  Institutet; the Science paper is the published text. She
  writes "shocks" / "responses of the genome to challenge."
  "Genome shock" is the later name for that claim. Not a
  PNAS paper.
  Distinct from filled McClintock 1950: 1950 is the origin
  and behavior of mutable loci (Ac/Ds). 1984 is the claim
  that unprepared stress restructures the genome (TE
  mobilization, rearrangements) as a response.
One-sentence prediction: A challenge the genome is
  unprepared for (breakage, hybridization, tissue-culture
  shock) mobilizes elements and restructures chromosomes;
  programmed shocks (heat shock, SOS) do not.
Assumptions: an unprepared challenge (not a constitutive
  clock); the response is TE mobilization / rearrangement,
  not a SNP clock; programmed shocks are a different class.
Which fail here: a constitutive somatic TE clock is not a
  shock response. Grafting and nursery propagation are
  chronic, not a single challenge. Scoring only SNPs hides
  the TE / SV class.
Modern data / statistic: clone-private TE insertions and
  SVs clustered on shock-associated nodes (hybridization,
  culture, color-sport events) versus a constitutive
  per-year somatic clock.
Datasets: Carrier et al. 2012 PLoS ONE 7(3):e32973;
  Vondras et al. 2019 BMC Genomics 20:972. SVs: Zhou et al.
  2019 Nat Plants 5:965-979.
What would falsify it: clone-private TE insertions (and
  SVs: Zhou 2019) are not clustered on shock-associated
  nodes versus a constitutive per-year somatic clock. A
  method-fair census that is SNP-dominated would also kill
  the 1984 claim as a grape mechanism (same census as the
  1950 TE note, different job: timing vs presence).
What we will not claim: that McClintock 1950 is the genome-
  shock paper (different job: mutable alleles). That a
  constitutive clone TE clock is a shock response.
```

---

## Allopolyploidy / secondary polyploidy

```
Theory: Allopolyploidy / secondary polyploidy
Original paper (year): Stebbins GL. 1947. Types of
  polyploids: their classification and significance.
  Advances in Genetics 1:403-429.
  DOI 10.1016/S0065-2660(08)60490-3 (also
  10.1016/s0065-2660(08)60490-3). No PMID (book-series
  chapter). ScienceDirect landing 406; title / year /
  venue / pages / DOI locked from citing publisher pages
  and the DOI string itself (same standard as Klekowski
  1988 / Ohno 1970).
  Not used as the source: Stebbins 1940 Am Nat 74:54-66
  DOI 10.1086/280872 (significance of polyploidy; earlier,
  not the auto / allo / segmental classification).
  Stebbins 1950 Variation and Evolution in Plants (book,
  later synthesis).
  Distinct from filled gene balance / Ohno: Ohno 1970 and
  Birchler 2007 are dosage after duplication. Stebbins
  1947 is the classification of polyploid types (auto,
  allo, segmental allo) and the role of secondary /
  palaeo-polyploidy.
One-sentence prediction: Allopolyploids combine
  differentiated genomes; segmental allopolyploids pair
  as if auto at some segments; secondary polyploids
  (palaeo-polyploids) diploidize and hide the event in
  chromosome number.
Assumptions: polyploid type (auto / allo / segmental)
  can be scored from pairing or subgenome differentiation;
  secondary / palaeo-polyploids are distinguished from
  recent allo events; tandem arrays are not homoeologs.
Which fail here: Vitis is palaeo-hexaploid, not a recent
  allopolyploid. Hemizygous SVs in clones change dose
  without a new WGD. Tandem NLR arrays are not homoeologs.
Modern data / statistic: recovery of differentiated
  homoeologous subgenomes versus three palaeo-hexaploid
  ancestral genomes; retention of TF / signaling ohnologs
  versus tandem NLRs.
Dataset: Jaillon O et al. 2007. Nature 449:463-467.
  DOI 10.1038/nature06148 PMID 17721507. Three ancestral
  genomes; no recent WGD. Companion: Zhou et al. 2019
  Nat Plants 5:965-979 (SVs change dose inside a clone
  without WGD).
What would falsify it: the three ancestral genomes are
  not recovered as two (or more) differentiated
  homoeologous subgenomes of a recent allo event, or TF
  / signaling ohnologs are not the retained class versus
  tandem NLRs (gene-balance companion, different job).
  Zhou 2019 SVs change dose inside a clone without WGD.
What we will not claim: that Jaillon 2007 is a recent
  allopolyploid. That this note replaces gene balance /
  Ohno (different job: polyploid type vs dosage after
  duplication). That Stebbins 1940 or 1950 is the source.
```

---

## Drift-barrier hypothesis

```
Theory: Drift-barrier hypothesis
Original paper (year): Lynch M. 2011. The lower bound to
  the evolution of mutation rates. Genome Biol Evol
  3:1107-1118. DOI 10.1093/gbe/evr066 PMID 21821597
  PMC3194889. Original research (theory + comparison to
  published rates). Not a review.
  Not the source: Lynch 2010 Trends Genet 26:345-352 is
  a review (red line). Sung W, Ackerman MS, Miller SF,
  Doak TG, Lynch M. 2012. Drift-barrier hypothesis and
  mutation-rate evolution. PNAS 109(45):18488-18492.
  DOI 10.1073/pnas.1216223109 PMID 23077252 PMC3494944
  is the empirical named-title follow-up; cite as the
  test, not the source.
  Distinct from filled nearly-neutral: Ohta 1973 is
  fixation of slightly deleterious alleles when |Nes| ~ 1.
  Drift-barrier is evolution of the mutation rate itself
  (proofreading / repair) to a floor set by 1/Ne.
One-sentence prediction: Selection pushes the mutation
  rate down until further antimutator advantages fall
  below the power of drift, so per-site mu scales
  negatively with Ne (and with coding target size).
Assumptions: a meaningful Ne; the trait is the mutation
  rate (proofreading / repair), not the load of slightly
  deleterious alleles; mu is germline / sexual, not
  somatic clone mu.
Which fail here: a cultivar collection is not one Ne.
  Somatic clone mu is not the germline / sexual mu the
  theory is about. Dual domestication splits Ne.
Modern data / statistic: per-generation per-site
  mutation rate (not load; load is Ohta) in wild versus
  cultivated lineages after clones are filtered.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild vs cultivar Ne
  contrast after clone filter. No locked grape wild-vs-
  cultivar mu paper; Vondras 2019 / Roach 2018 are
  clone-somatic clocks, usable only as a sister somatic-
  mu dataset, not as the species-level test. Do not
  invent a grape mutation-rate paper.
What would falsify it: per-generation per-site mutation
  rate (not load) is not higher in the smaller-Ne
  cultivated lineages after clones are filtered.
What we will not claim: that Lynch 2010 is the source
  (review). That Vondras / Roach measured species-level
  mu. That load (Ohta) is the drift-barrier test.
```

---

## GC-biased gene conversion

```
Theory: GC-biased gene conversion
Original paper (year): Galtier N, Piganeau G, Mouchiroud
  D, Duret L. 2001. GC-content evolution in mammalian
  genomes: the biased gene conversion hypothesis.
  Genetics 159(2):907-911.
  DOI 10.1093/genetics/159.2.907 PMID 11693127
  PMC1461818. Short letter; it is the paper that names
  the hypothesis. Wave 2 dropped gBGC for lack of a
  single original; this is that lock.
  Not the source: Eyre-Walker A. 1993. Recombination and
  mammalian genome evolution. Proc R Soc Lond B
  252:237-243 (precursor: recombination and GC, not the
  named BGC hypothesis). Eyre-Walker 1999 Genetics
  152:675-683 (selection on silent GC). Marais 2003
  Trends Genet 19:330-338 (review).
One-sentence prediction: Meiotic gene conversion is
  biased toward G/C, so GC (and the W-to-S fixation
  rate) rises where recombination is high, mimicking
  directional selection for GC.
Assumptions: meiotic gene conversion; a known
  recombination map; the GC / W-to-S pattern is sexual
  / meiotic, not methylation-driven C-to-T.
Which fail here: gBGC is a meiotic transmission bias.
  Grafted clones have no meiosis between cuttings. A
  chip skeleton is not a recombination map (same map
  requirement as BGS / Hill-Robertson). Vitis GC is
  also driven by methylation-associated C-to-T
  (Vondras 2019).
Modern data / statistic: GC and W-to-S fixation bias
  in recombination-rate bins on a real Vitis map,
  after clone + IBD filters and after gene-density
  and mutability (CpG / methylation) control.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655) as the WGS panel on
  a real Vitis recombination map. Do not invent a
  grape recombination-map paper; the map is a
  requirement, as in the BGS note.
What would falsify it: GC and the W-to-S fixation
  bias are not higher in high-recombination bins once
  gene density and mutability (CpG / methylation)
  are controlled.
What we will not claim: that a chip GC track is gBGC.
  That Eyre-Walker 1993 or Marais 2003 is the named
  source. That clone methylation C-to-T is conversion.
```

---

## Soft sweep

```
Theory: Soft sweep
Original paper (year): Hermisson J, Pennings PS. 2005.
  Soft sweeps: molecular population genetics of
  adaptation from standing genetic variation.
  Genetics 169(4):2335-2352.
  DOI 10.1534/genetics.104.036947 PMID 15716498
  PMC1449620.
  Distinct from filled hitchhiking: Maynard Smith and
  Haigh 1974 is the hard-sweep / new-mutation hitchhike.
  Soft sweep is multiple copies (standing variation or
  recurrent mutation) contributing to the substitution,
  so linked diversity is only partly erased.
One-sentence prediction: Adaptation from standing
  variation (or from recurrent new mutation) produces
  a soft sweep: more than one ancestral haplotype of
  the selected allele survives, and the hitchhiking
  dip is shallower than a hard sweep of equal s.
Assumptions: more than one copy of the selected allele
  (standing or recurrent); a sexual sample; linked
  diversity is not clone-IBD or first-degree pedigree.
Which fail here: cultivar relatedness and first-degree
  pedigrees produce long shared haplotypes that look
  like a hard sweep (Dong 2023 caution, same as
  hitchhiking). Ascertainment of "the" domestication
  allele on a 12X / cultivar panel hides extra
  haplotypes. Clones are not a random sexual sample.
Modern data / statistic: haplotype count and residual
  linked diversity at domestication peaks (color /
  sex / flavor) after clone + IBD filters.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Color / sex / flavor
  peaks. Standing hermaphrodite haplotypes H1/H2
  already in some sylvestris (Dong 2023 SDR) are the
  ascertainment / standing-variation test, not
  VviAGL11.
What would falsify it: if a candidate domestication
  haplotype is a single star phylogeny (hard), the
  soft-sweep claim dies for that locus. If several
  independent haplotypes carry the selected allele
  at residual linked diversity, the hard-sweep
  (Maynard Smith-Haigh) claim dies.
What we will not claim: that Dong 2023 demonstrated
  a soft sweep. That VviAGL11 is the sex-locus test
  (SDR H1/H2 is). That this note replaces hitchhiking
  (hard vs soft are different jobs).
```

---

## Chimera / tunica-corpus meristem layers

```
Theory: Chimera / tunica-corpus meristem layers
Original paper (year): Satina S, Blakeslee AF, Avery
  AG. 1940. Demonstration of the three germ layers
  in the shoot apex of Datura by means of induced
  polyploidy in periclinal chimeras. Am J Bot
  27(10):895-905.
  DOI 10.1002/j.1537-2197.1940.tb13952.x
  JSTOR 2436558. No PMID. Wiley landing Cloudflare-
  blocked; CSHL repository page opened.
  Modern grape lock (allowed by the brief): Franks T,
  Botta R, Thomas MR, Franks J. 2002. Chimerism in
  grapevines: implications for cultivar identity,
  ancestry and genetic improvement. Theor Appl Genet
  104:192-199. DOI 10.1007/s001220100683
  PMID 12582686 (PMID from citing PubMed pages).
  Pinot Meunier: three VVS2 alleles; L1 vs L2 split
  by somatic embryogenesis yield two genotypes /
  phenotypes.
One-sentence prediction: The shoot apex is a layered
  meristem (tunica-corpus). A mutation in one layer
  can stabilize as a periclinal chimera; the layers
  have independent genotypes and can be separated.
Assumptions: a layered meristem whose layers keep
  independent genotypes; a periclinal chimera is
  stable and separable; layer count is scored, not
  assumed from a mixed-leaf SSR.
Which fail here: Datura has three germ layers. Vitis
  SAM is two-layered (L1 / L2). Diplontic selection
  (Klekowski 1988, already filled) can purge a layer.
  Leaf-DNA "triallelic" SSRs are not proof of three
  layers. Recessives in L1 hide from L2 (gametes).
Modern data / statistic: genotypes of layer-split
  regenerants of a chimeric cultivar, and layer-
  restriction of clone-private mutations after a
  method-fair L1 vs L2 census.
Lead test: Franks et al. 2002 Theor Appl Genet
  104:192-199 (Pinot Meunier L1/L2 split). Genome-
  wide companions: Vondras 2019 / Roach 2018 /
  Carrier 2012.
What would falsify it: if layer-split regenerants of
  a chimeric cultivar are genetically identical, or
  if clone-private mutations are not layer-restricted
  after a method-fair L1 vs L2 census, the periclinal-
  chimera claim dies for that cultivar. Do not treat
  a mixed-leaf SSR profile as the theory.
What we will not claim: that Vitis has three Datura
  layers. That a triallelic leaf SSR proves three
  layers. That this note replaces diplontic selection
  (Klekowski is meristem competition; this is layer
  structure).
```

---

## Reinforcement

```
Theory: Reinforcement of reproductive isolation
Original paper (year): Dobzhansky T. 1940. Speciation
  as a stage in evolutionary divergence. The American
  Naturalist 74(753):312-321. DOI 10.1086/280899.
  Isolating mechanisms develop along geographic
  boundaries after adaptive complexes have formed,
  because hybridization is maladaptive.
  (Dobzhansky 1937 book is the BDM source, already
  filled. This 1940 paper is the reinforcement
  argument, not that book. Wave 2 dropped a 1936
  year; the journal page is 1 July 1940, pages
  312-321.)
One-sentence prediction: Where hybrids are unfit,
  selection completes premating isolation in
  sympatry more than in allopatry.
Assumptions: secondary contact with some gene flow;
  hybrids less fit than parentals; the trait under
  test is premating isolation, not a one-locus
  incompatibility.
Which fail here: a nursery hybrid is not secondary
  contact. Cultivar relatedness fakes isolation.
  Humans move both species. BDM (already filled)
  is hybrid inviability genetics, not reinforcement.
Modern data / statistic: premating isolation
  (flowering time, pollen success, mate choice) in
  sympatric versus allopatric vinifera x riparia /
  rupestris / amurensis or sylvestris contacts.
Caution dataset (not a proof of Dobzhansky 1940):
  Dong et al. 2023 Science
  (DOI 10.1126/science.add8655) reports Syl-W gene
  flow into cultivated groups. Gene flow is the
  opposite of completed reinforcement; use as
  CAUTION, not as a reinforcement map. Do not invent
  a grape hybrid / prezygotic-isolation paper.
What would falsify it: premating isolation is not
  stronger in sympatry than in allopatry, OR hybrid
  inviability maps to a single locus with no
  premating increment.
What we will not claim: that Dong 2023 proved
  reinforcement. That this note replaces BDM
  (Dobzhansky 1937 book). That a grape
  powdery-mildew NLR paper exists here.
```

---

## Two-fold cost of sex

```
Theory: Two-fold cost of sex (cost of males)
Original paper (year): Maynard Smith J. 1978. The
  Evolution of Sex. Cambridge University Press.
  242 pp. ISBN 052121887X. Book. Sexual females
  invest about half their offspring in sons; an
  asexual female that makes only daughters doubles
  in frequency when rare if all else is equal.
  (Kondrashov 1988 is a different, already-dropped
  cost-of-males / deterministic-mutation paper.
  Do not substitute it here.)
One-sentence prediction: An asexual mutant that
  produces only daughters replaces a dioecious
  sexual population in a few tens of generations
  unless a short-term benefit of sex counters the
  two-fold cost.
Assumptions: separate sexes and an equal sex
  ratio; the asexual is a female that skips sons;
  all-else-equal fecundity and survival; the
  comparison is sexual versus asexual reproduction,
  not cutting versus seed.
Which fail here: this does not map onto grafted
  clones. A grafted vine is a cutting of an
  existing genotype, not an asexual female
  replacing sexuals via daughters. Cultivated
  grape is mostly hermaphrodite, not dioecious
  with a cost of sons. Nursery propagation is not
  Maynard Smith's experiment.
Modern data / statistic: none that tests the
  two-fold cost in grape. Clone versus seedling
  yield is not a cost-of-males contrast.
What would falsify it: not applicable as a grape
  test. The note is filled as "does not map onto
  grafted clones" rather than as an invented
  asexual-female invasion.
What we will not claim: that grape clones
  demonstrate the two-fold cost. That Kondrashov
  1988 is this paper. That hermaphroditism is a
  test of the cost of males (that is Baker, already
  filled).
```

---

## Haldane cost of selection (mutation load / cost of substitution)

```
Theory: Haldane cost of selection (cost of substitution)
Original paper (year): Haldane JBS. 1957. The cost of natural
  selection. Journal of Genetics 55:511-524.
  DOI 10.1007/BF02984069. IAS Journal of Genetics page locked:
  https://www.ias.ac.in/article/fulltext/jgen/055/03/0511-0524
  Summary: unless selection is very intense, the number of deaths
  needed to substitute one gene for another is independent of the
  intensity of selection and is often about 30 times the number of
  organisms in a generation.
  Distinct from filled Haldane 1922 (heterogametic hybrid sterility).
  Distinct from dropped Kondrashov 1988 and filled Maynard Smith
  1978 (costs of sex / males).
One-sentence prediction: Substituting one allele for another by
  selection requires a large number of selective deaths (or lost
  fertility), so many loci cannot be substituted at once.
Assumptions: a sexual (or equivalent) population substituting
  alleles; generations of parents and offspring; the cost is
  counted over the substitution, not over a cutting.
Which fail here: this does not map onto grafted clones. A cultivar
  panel is not a substituting sexual population. Cuttings skip
  the substitution. Nursery selection on sports is not Haldane
  cost. Dual domestication is human choice, not horotelic
  substitution at thousands of loci.
Modern data / statistic: none that tests Haldane 1957 in grape.
  Wild-to-cultivar substitutions on Dong-class WGS, if scored,
  are not the cost experiment.
What would falsify it: not applicable as a grape test. The note
  is filled as "does not map onto grafted clones" rather than as
  an invented cost-of-selection experiment.
What we will not claim: that Dong 2023 measured Haldane cost.
  That this note replaces Haldane 1922 (different job). That a
  grape mutation-load paper is locked (none was).
```

---

## Inbreeding depression

```
Theory: Inbreeding depression
Original paper (year): Darwin CR. 1876. The effects of cross
  and self fertilisation in the vegetable kingdom. London: John
  Murray. Book. viii + 482 pp. (Freeman F1249; darwin-online
  bibliographic record locked). Crossed progeny exceeded selfed
  progeny in height and fertility in the tabulated genera.
  Charlesworth and Charlesworth reviews are not the source.
One-sentence prediction: Offspring of self-fertilisation (or
  close inbreeding) are less vigorous or less fertile than
  offspring of a cross, when both are grown in the same garden.
Assumptions: a self-versus-cross contrast in sexual plants;
  fitness is scored on progeny, not on a chimeric shoot;
  standing heterozygosity in a clone is not the experiment.
Which fail here: grafted cultivars are not a self-vs-cross
  trial. Standing heterozygosity in clones is not inbreeding
  depression (that is why overdominance was not filled). Roach
  2018 ancestral inbreeding in Chardonnay is a pedigree fact,
  not a Darwin garden test. Nursery cuttings skip meiosis.
Modern data / statistic: fitness or vigor of selfed versus
  outcrossed seedlings after clone / IBD filters, not clone-
  private heterozygosity.
Caution dataset: Roach et al. 2018 PLoS Genet 14(11):e1007807
  (DOI 10.1371/journal.pgen.1007807). Ancestral inbreeding in
  Chardonnay. Use as CAUTION, not as a depression proof. Do
  not invent a grape selfing-depression paper.
What would falsify it: selfed / inbred seedlings are not less
  fit than outcrossed seedlings after clone / IBD filters, OR
  clone heterozygosity is treated as the Darwin test (it is
  not).
What we will not claim: that Roach 2018 measured inbreeding
  depression. That standing clone heterozygosity is overdominance
  (that door item stays dropped).
```

---

## Infinitesimal / polygenic

```
Theory: Infinitesimal / polygenic inheritance
Original paper (year): Fisher RA. 1918. The correlation
  between relatives on the supposition of Mendelian
  inheritance. Transactions of the Royal Society of Edinburgh
  52:399-433. DOI 10.1017/S0080456800012163. Paper read 1918;
  volume imprint on the Cambridge Core landing is 1919
  (Earth and Environmental Science Transactions of The Royal
  Society of Edinburgh 52(2):399-433). Lock the venue as the
  1918 Transactions paper. Names variance and partitions it
  among Mendelian causes.
  Distinct from Fisher 1930 book (geometric model; book locked,
  geometric page not locked this wave and not filled).
One-sentence prediction: A continuously varying trait is the
  sum of many Mendelian loci of small effect plus environment;
  relatives correlate in proportion to shared Mendelian variance.
Assumptions: many loci, each small; a sexual pedigree; the
  trait is not one or a few large-effect substitutions;
  clones and first-degree cuttings are not the relatives.
Which fail here: berry color, hermaphroditism, and muscat /
  flavor in grape are large-effect domestication loci (Dong
  2023). A cultivar panel is not a Fisher pedigree. Clone IBD
  fakes a polygenic correlation.
Modern data / statistic: number and effect-size of loci for
  a domestication trait after clone + IBD filters, versus an
  infinitesimal (many small) expectation.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Color / sex / flavor peaks.
  Use as the large-effect contrast, not as a published
  infinitesimal test. Do not invent a grape GCTA paper.
What would falsify it: a candidate domestication trait is
  explained by one or a few large-effect loci (infinitesimal
  dies for that trait). If many small loci remain after clone
  + IBD filters, the single-gene claim dies.
What we will not claim: that Dong 2023 estimated SNP
  heritability. That this note is Fisher's 1930 geometric
  model (not filled). That VviAGL11 is the sex-locus test
  (SDR H1/H2 is).
```

---

## Genetic assimilation

```
Theory: Genetic assimilation
Original paper (year): Waddington CH. 1953. Genetic
  assimilation of an acquired character. Evolution 7(2):118-126
  (June 1953). JSTOR 2405747. JSTOR scan opened (author,
  title, volume, issue, pages, year). Crossveinless, first a
  heat-shock phenocopy, appeared without the shock after
  selection. Waddington 1942 Nature 150:563 is the canalisation
  note, not this experiment. Waddington 1952 Nature 169:278
  is the preliminary account, not the full paper.
One-sentence prediction: Selection on an environmentally
  induced phenotype canalises development so the phenotype
  appears in the ancestral environment without the inducing
  shock.
Assumptions: many sexual generations of selection on the
  induced phenotype; the trait starts as a phenocopy; the
  later constitutive state is genetic, not a lingering shock.
Which fail here: this does not map onto grafted clones.
  Cuttings skip the multi-generation sexual selection
  Waddington used. A nursery sport is not a phenocopy that
  was assimilated. Plastic berry / leaf traits without a
  selection experiment are not assimilation.
Modern data / statistic: none that tests Waddington 1953
  in grape. A heat / drought phenocopy that becomes
  constitutive after seedling selection would be the
  dataset type; no such grape paper is locked.
What would falsify it: not applicable as a grape clone
  test. The note is filled as "does not map onto grafted
  clones" rather than as an invented assimilation trial.
What we will not claim: that a clone sport is genetic
  assimilation. That Waddington 1942 is this paper. That
  a grape heat-shock paper exists here.
```

---

## C-value / junk DNA

```
Theory: C-value / junk DNA
Original paper (year): Ohno S. 1972. So much "junk" DNA
  in our genome. Brookhaven Symposia in Biology 23:366-370.
  PMID 5065367. EuropePMC and PubMed esummary locked.
  No article DOI on those pages. Distinct from filled
  selfish DNA (Doolittle and Sapienza 1980; Orgel and Crick
  1980): 1972 is failed-duplication debris and the C-value
  paradox; 1980 is persistence by self-replication.
  Distinct from filled Ohno 1970 gene-duplication book.
One-sentence prediction: Genome size (C-value) is not
  gene number; most DNA is non-coding debris from failed
  duplications.
Assumptions: gene number can be told from total DNA;
  "junk" is not assumed to be functional from presence;
  TEs may contribute debris but are not required for the
  1972 claim.
Which fail here: scoring only genes on a 12X panel hides
  the repeat / TE fraction. Palaeo-hexaploidy (Jaillon
  2007) adds ohnologs without explaining all DNA. Clone
  hemizygous SVs change dose without changing C-value.
Modern data / statistic: grape genome size versus
  annotated gene number, and the TE / repeat fraction,
  versus a gene-number explanation of C-value.
Datasets: Jaillon et al. 2007 Nature 449:463-467
  (DOI 10.1038/nature06148). Carrier et al. 2012 PLoS ONE
  7(3):e32973 (TE insertions the largest scored class in
  Pinot noir). Vondras 2019 (TE plus repeat SNPs).
What would falsify it: Vitis genome size is explained by
  gene number, not by junk / repeat / TE DNA.
What we will not claim: that Ohno 1972 is the selfish-DNA
  paper (different job). That every TE insertion is junk
  (some copies are domesticated; that is the 1980 falsifier).
  That Jaillon 2007 measured C-value across Vitis.
```

---

## Concerted evolution

```
Theory: Concerted evolution
Original paper (year): Zimmer EA, Martin SL, Beverley SM,
  Kan YW, Wilson AC. 1980. Rapid duplication and loss of
  genes coding for the alpha chains of hemoglobin. Proc
  Natl Acad Sci USA 77(4):2158-2162.
  DOI 10.1073/pnas.77.4.2158 PMID 6929543 PMC348671.
  PMC page locked. The abstract says the alpha polypeptides
  within each species have been evolving in concert.
  Dover 1982 molecular drive is later and is not used.
  Not a review.
One-sentence prediction: Members of a repeated family stay
  more similar within a species than to orthologs in other
  species, by ongoing duplication, loss, or intergenic
  exchange.
Assumptions: a true repeated family (not palaeo-ohnologs
  of a hexaploid); identity is not clone IBD; the comparison
  is within-species paralogs versus between-species
  orthologs.
Which fail here: tandem NLR arrays are not rRNA or globin.
  Palaeo-hexaploid ohnologs (Jaillon 2007) are a different
  job (DDC / gene balance / fractionation). Clone IBD fakes
  family identity. Birth-and-death is the alternative
  (next note).
Modern data / statistic: within-species identity of tandem
  copies (rDNA or tandem NLR / disease genes) versus
  identity to orthologs in other Vitis, after clone filter.
Datasets: Jaillon et al. 2007 Nature 449:463-467 (genome
  and ohnolog set; do not invent a grape rDNA paper).
  Zhou et al. 2019 Nat Plants 5:965-979 (SVs; tandem
  change without homogenization).
What would falsify it: tandem copies are more like
  orthologs in other Vitis than like paralogs in the same
  genome (birth-and-death pattern), OR identity is only
  clone IBD.
What we will not claim: that Nei 1997 is this paper
  (opposite job). That every NLR array is concerted. That
  a grape rDNA homogenization paper is locked.
```

---

## Birth-and-death gene family

```
Theory: Birth-and-death evolution of gene families
Original paper (year): Nei M, Gu X, Sitnikova T. 1997.
  Evolution by the birth-and-death process in multigene
  families of the vertebrate immune system. Proc Natl Acad
  Sci USA 94(15):7799-7806.
  DOI 10.1073/pnas.94.15.7799 PMID 9223266 PMC33709.
  PMC page locked. New genes arise by duplication; some
  persist, others become pseudogenes or are deleted;
  members need not be closer within species than between
  species. The paper says the model was formally presented
  by Nei and Hughes 1992 (workshop chapter; not opened).
  Nei and Rooney 2005 Annu Rev Genet is a review (red line).
  Distinct from filled concerted evolution (Zimmer 1980).
One-sentence prediction: A family expands and contracts by
  duplication and loss; some copies persist, others die;
  within-species copies need not be homogenized.
Assumptions: a multi-copy family with a phylogeny that can
  reject homogenization; tandem arrays can be told from
  ohnologs; pseudogenes are scored, not assumed absent.
Which fail here: grape tandem NLRs are not MHC. Palaeo-
  hexaploid ohnologs are DDC / gene-balance / fractionation
  jobs, not birth-and-death of a tandem family. Clone SVs
  change copy number without a family phylogeny.
Modern data / statistic: phylogeny of a tandem Vitis
  family (NLR or other disease-related) with pseudogenes,
  testing within-species homogenization versus births and
  deaths.
Datasets: Jaillon et al. 2007 Nature 449:463-467 (ohnolog
  versus tandem contrast). Zhou et al. 2019 Nat Plants
  5:965-979 (SV copy-number change). Do not invent a grape
  NLR phylogeny paper.
What would falsify it: tandem copies form one homogenized
  within-species clade with no births, deaths, or
  pseudogenes (concerted pattern).
What we will not claim: that Nei and Rooney 2005 is the
  source (review). That every grape family expansion is
  birth-and-death. That this note replaces DDC or gene
  balance.
```

---

## Metapopulation

```
Theory: Metapopulation (population of populations)
Original paper (year): Levins R. 1969. Some demographic
  and genetic consequences of environmental heterogeneity
  for biological control. Bulletin of the Entomological
  Society of America 15(3):237-240.
  DOI 10.1093/besa/15.3.237. DOI / OpenAIRE listings
  locked (author, year, venue, volume, pages). Occupancy
  of patches is a colonization-extinction balance.
  Distinct from filled Wright 1931 island model (no
  distance; common migrant pool) and Kimura and Weiss
  1964 stepping-stone (neighbor steps, not extinction).
  Distinct from filled Wright 1943 IBD (continuous
  distance).
One-sentence prediction: A set of discrete habitat
  patches persists as a population of populations when
  colonization exceeds local extinction; occupancy is
  not one panmictic Ne.
Assumptions: discrete patches that can go extinct and
  be recolonized; samples are patches, not clones or
  cultivars; a vineyard block is not a Levins patch.
Which fail here: a vineyard is not a patch. Humans and
  nurseries recolonize without extinction. Cultivar
  panels are pedigrees. Wild sylvestris along rivers
  may be patches; feral escapes are not.
Modern data / statistic: patch occupancy and turnover
  (presence / absence, or recolonization after local
  loss) among wild V. sylvestris patches after clone /
  pedigree filters.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris
  subset. Use as geography / occupancy, not as a
  published metapopulation analysis. Do not invent a
  grape patch-turnover paper.
What would falsify it: wild patches do not show a
  colonization-extinction occupancy balance after
  clone filter (stable occupancy, or one panmictic
  cloud). A nonzero IBD slope is the Wright 1943
  job, not this one.
What we will not claim: that a vineyard block is a
  Levins patch. That this note replaces island,
  stepping-stone, or IBD (four different spatial
  jobs).
```

---

## Breakage-fusion-bridge

```
Theory: Breakage-fusion-bridge cycle
Original paper (year): McClintock B. 1941. The
  stability of broken ends of chromosomes in Zea
  mays. Genetics 26(2):234-282.
  DOI 10.1093/genetics/26.2.234 PMID 17247004
  PMC1209127. PMC page locked. Broken ends remain
  unstable in some tissues and produce further
  rearrangement.
  Distinct from filled McClintock 1950 (mutable
  loci / Ac-Ds) and filled McClintock 1984 (genome
  shock). Not a TE paper.
One-sentence prediction: A broken chromosome end
  fuses, forms a bridge at anaphase, and breaks
  again, cycling rearrangements and losses until
  the end heals.
Assumptions: a broken end (not a TE insertion and
  not a constitutive SNP clock); the cycle is
  scored as rearrangements, not as SNPs; healing
  can stop the cycle.
Which fail here: scoring only SNPs hides BFB.
  A hemizygous deletion can be one break without
  a cycle. Chromothripsis-like events are a
  related class, not automatically BFB. Distinct
  from diplontic selection and chimera notes.
Modern data / statistic: clone-private
  rearrangements with inverted duplications,
  bridges, or oscillating copy number versus a
  single-break or chromothripsis-like class.
Lead test bed (not a proof): Carbonell-Bejerano
  et al. 2017 Plant Physiol 175:786-801
  (DOI 10.1104/pp.17.00715). Tempranillo Blanco;
  hemizygous deletion of 313 genes; chromothripsis-
  like. Companion SVs: Zhou et al. 2019 Nat Plants
  5:965-979. Clone SNP/SV clocks: Vondras 2019 /
  Carrier 2012.
What would falsify it: clone-private
  rearrangements are not BFB-class (no fusion-
  bridge cycle; single-break or chromothripsis-
  like only), OR a method-fair census is SNP-
  dominated with negligible rearrangements.
What we will not claim: that Carbonell-Bejerano
  2017 proved BFB (they report a catastrophic
  unbalanced rearrangement). That McClintock
  1950 or 1984 is this paper. That every color
  sport is a bridge cycle.
```

---

## Fractionation / diploidization after WGD

```
Theory: Fractionation / diploidization after WGD
Original paper (year): Thomas BC, Pedersen B,
  Freeling M. 2006. Following tetraploidy in an
  Arabidopsis ancestor, genes were removed
  preferentially from one homeolog leaving
  clusters enriched in dose-sensitive genes.
  Genome Research 16(7):934-946.
  DOI 10.1101/gr.4708406 PMID 16760422
  PMC1484460. Publisher abstract and PMC page
  locked. One homeolog was preferentially
  (about 1.6x) targeted for fractionation;
  retained islands are connected / dose-sensitive
  genes. Freeling and Thomas 2006 Genome Res
  16:805-814 is a companion perspective, not
  this data paper. Freeling 2009 Annu Rev Plant
  Biol is a review (red line).
  Distinct from filled Ohno / Birchler gene
  balance (dosage after duplication), filled
  Stebbins 1947 (polyploid type), and filled
  DDC / Force 1999 (subfunction partition).
One-sentence prediction: After whole-genome
  duplication, most pairs reduce to one gene by
  loss from one homeolog; loss is biased, and
  dose-sensitive (connected) genes are retained
  as pairs.
Assumptions: homeologs of a WGD can be aligned;
  tandem arrays are condensed, not counted as
  ohnologs; Vitis palaeo-hexaploidy is old, not
  a recent tetraploid.
Which fail here: Vitis is palaeo-hexaploid, not
  a recent Arabidopsis-style tetraploid (Jaillon
  2007: three ancestral genomes; no recent WGD).
  Hemizygous SVs in clones change dose without
  WGD (Zhou 2019; Carbonell-Bejerano 2017).
  Tandem NLRs are not homeologs.
Modern data / statistic: biased gene loss from
  one of the three palaeo-hexaploid ancestral
  genomes, and retention of TF / signaling
  ohnologs versus tandem NLRs.
Dataset: Jaillon et al. 2007 Nature 449:463-467
  (DOI 10.1038/nature06148). Three ancestral
  genomes; no recent WGD. Companion: Zhou et al.
  2019 Nat Plants 5:965-979 (SVs change dose
  without WGD).
What would falsify it: the three ancestral
  genomes do not show biased homeolog loss, OR
  TF / signaling ohnologs are not the retained
  class versus tandem NLRs (gene-balance
  companion, different job). Zhou 2019 SVs
  change dose inside a clone without WGD.
What we will not claim: that Jaillon 2007 is a
  recent tetraploid. That this note replaces
  gene balance, Stebbins polyploid type, or DDC.
  That Freeling 2009 is the source (review).
```

---

---

## Ewens sampling formula

```
Theory: Ewens sampling formula
Original paper (year): Ewens WJ. 1972. The sampling theory of
  selectively neutral alleles. Theoretical Population Biology
  3(1):87-112. DOI 10.1016/0040-5809(72)90035-4 PMID 4667078.
  EuropePMC HTML landing opened (author, title, year, venue,
  volume, issue, pages, DOI, PMID). ScienceDirect HTML timed
  out this wave; lock from the EuropePMC page. The paper
  begins a sampling theory of a sample of genes from a
  selectively neutral locus, including a test that the
  alleles are indeed selectively neutral. Karlin and McGregor
  1972 Theor Popul Biol 3:113-116 is the same-issue addendum
  (PMID 4667073), not the source.
  Distinct from filled Kimura and Crow 1964 infinite-alleles
  (each mutation is a new allele; IBS is IBD). 1972 is the
  sampling distribution of allele-count configurations under
  that model.
  Distinct from filled Kingman 1982 coalescent.
One-sentence prediction: Under selective neutrality and
  infinite-alleles mutation, the configuration of allele
  counts in a sample follows Ewens's sampling formula; the
  number of types is a sufficient statistic for theta.
Assumptions: a random sample of genes from one locus;
  selective neutrality; infinite-alleles mutation; samples
  are not clones or first-degree cuttings; chips are not
  forced-biallelic.
Which fail here: a cultivar panel is not a random haploid
  sample. Clone IBD fakes allele identity. SNP chips are
  biallelic. Pedigree repeats are not new alleles.
Modern data / statistic: allele-count configuration (or
  haplotype-count configuration) in wild V. sylvestris
  after clone + IBD filters, versus the Ewens null.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset.
  Use as a configuration test after clone + IBD filters,
  not as a published Ewens analysis. Do not invent a grape
  Ewens-sampling paper.
What would falsify it: the configuration is not Ewens after
  clone + IBD filters, OR clone IBS is treated as the allele
  sample (it is not).
What we will not claim: that Kimura and Crow 1964 is this
  paper (different job). That Dong 2023 fitted Ewens's
  formula. That a cultivar PCA is a neutral sample.
```

---

## Shifting balance

```
Theory: Shifting balance
Original paper (year): Wright S. 1932. The roles of mutation,
  inbreeding, crossbreeding and selection in evolution.
  Proceedings of the Sixth International Congress of Genetics
  (Ithaca, New York, 1932) 1:356-366. ESP facsimile PDF
  opened (http://www.esp.org/books/6th-congress/facsimile/contents/6th-cong-p356-wright.pdf);
  ESP TOC HTML opened (chapter page 356, S. Wright). Running
  headers: "PROCEEDINGS OF THE SIXTH" / "INTERNATIONAL
  CONGRESS OF GENETICS". Author line: Sewall Wright,
  University of Chicago. Figure 2 (p. 358) is the adaptive
  surface with peaks and "valleys". Figure 4F / text p. 363:
  a large species subdivided into many small local races,
  each breeding largely within itself but occasionally
  crossbreeding; one race under a higher peak expands and
  by crossbreeding pulls the whole species toward the new
  position; subdivision is "the most effective mechanism
  for trial and error in the field of gene combinations."
  Distinct from filled Wright 1931 Genetics 16:97-159
  (island-model math) and filled Wright 1943 IBD
  (continuous distance). 1931 is cited in the 1932
  literature list. The 1932 congress paper is the named
  shifting-balance original (peak-shift via subdivided
  trial-and-error), not the 1931 island formula.
One-sentence prediction: A species subdivided into small
  local races can shift from a lower adaptive peak to a
  higher one by local nonadaptive wandering, then export
  of the successful combination by intergroup selection
  and crossbreeding.
Assumptions: many small, partially isolated sexual races;
  an adaptive surface with more than one peak; samples are
  races, not clones or cultivars; a vineyard block is not
  a Wright race.
Which fail here: grafted cultivars are not local races.
  Cuttings skip the inbreeding / crossbreeding trial.
  Dual domestication is human choice, not intergroup
  export of a peak. Wild sylvestris patches may be races;
  feral escapes and nursery clones are not.
Modern data / statistic: local nonadaptive differentiation
  among wild patches, then export of a higher-fitness
  combination, after clone / pedigree filters.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset.
  Use as geography / patch structure, not as a published
  shifting-balance analysis. Do not invent a grape
  peak-shift paper.
What would falsify it: wild patches do not show local
  nonadaptive peak-shift followed by intergroup export
  after clone filter (one panmictic cloud, or a Wright
  1943 IBD slope with no peak-shift). A vineyard PCA is
  not the test.
What we will not claim: that Wright 1931 is this paper
  (island math, already filled). That a wine-region PCA
  is a shifting-balance landscape. That this note
  replaces island, stepping-stone, IBD, or metapopulation
  (four different spatial jobs).
```

---

## Fisher's geometric model

```
Theory: Fisher's geometric model of adaptation
Original paper (year): Fisher RA. 1930. The Genetical
  Theory of Natural Selection. Oxford: Clarendon Press.
  Chapter II ("The Fundamental Theorem of Natural
  Selection"), running headers pages 38-41 of the 1930
  edition. Archive.org scan / djvu text opened
  (identifier geneticaltheoryo00fishuoft; title page
  "OXFORD AT THE CLARENDON PRESS 1930"). Geometric
  claim locked on those pages, not only in the TOC:
  a point A and an optimum O; superior adaptations lie
  in a sphere through A centred at O; a displacement of
  length r improves only if it falls inside the sphere;
  as r tends to 0 the chance of improvement tends to
  one-half; if r is as great as the diameter there is
  no chance of improvement; in many dimensions the
  chance of improvement falls rapidly while r is still
  small compared with d; Fig. 3 plots probability of
  improvement versus r sqrt(n)/d when n is large; the
  microscope-adjustment analogy is on pp. 40-41.
  Distinct from filled Fisher 1918 infinitesimal /
  polygenic (many small Mendelian loci for a metric
  trait). 1930 geometric is random mutations in an
  n-dimensional phenotype space. Wave 5 had dropped
  this item because the geometric page was not locked;
  it is filled now.
One-sentence prediction: A large random mutation almost
  never improves a well-adapted phenotype; only changes
  small compared with a standard magnitude d/sqrt(n)
  have an appreciable chance of improvement.
Assumptions: an n-dimensional phenotype with an optimum;
  mutations are undirected displacements; the organism
  is already somewhat adapted; a walk is sexual
  generations, not cuttings.
Which fail here: berry color, hermaphroditism, and
  muscat / flavor in grape are large-effect
  domestication substitutions (Dong 2023), not a
  small-step geometric walk. A cultivar panel is not
  Fisher's n-space. Clone sports are not random
  mutations in phenotypic n-space.
Modern data / statistic: effect-size of domestication
  substitutions after clone + IBD filters, versus a
  small-step (large-n) geometric expectation.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Color / sex / flavor
  peaks. Use as the large-effect contrast, not as a
  published geometric-model test. Do not invent a grape
  FGM paper.
What would falsify it: a candidate domestication trait
  is explained by one or a few large-effect loci
  (small-step geometric dies for that trait). If only
  tiny-effect mutations remain after clone + IBD
  filters, the large-effect claim dies.
What we will not claim: that this note is Fisher 1918
  (already filled). That Dong 2023 estimated n or
  d/sqrt(n). That a nursery sport is a geometric
  displacement.
```

---

## Mutation-selection balance

```
Theory: Mutation-selection balance
Original paper (year): Haldane JBS. 1927. A mathematical
  theory of natural and artificial selection, Part V:
  Selection and mutation. Mathematical Proceedings of
  the Cambridge Philosophical Society 23(7):838-844
  (July 1927). DOI 10.1017/S0305004100015644.
  Cambridge Core HTML landing opened (author, title,
  volume, issue, pages, year, DOI). New factors arise
  by mutation; the paper treats initial survival of a
  mutant and then the course when the factor is no
  longer at risk of chance extinction. Distinct from
  filled Haldane 1922 (heterogametic hybrid sterility)
  and filled Haldane 1957 (cost of substitution).
  Distinct from filled Mukai 1964 mutation accumulation
  (a cage experiment, not the equilibrium). Crow load
  papers were not used as the source.
One-sentence prediction: A deleterious allele is held
  in the population at an equilibrium set by mutation
  input and selection against it, not by a substituting
  sweep and not by a mutation-accumulation cage.
Assumptions: a sexual population at equilibrium;
  mutation and selection both act each generation;
  clone-private SNPs are not the equilibrium frequency;
  a cutting is not a generation of selection.
Which fail here: grafted clones are not a sexual
  mutation-selection equilibrium. Clone-private coding
  variants are a somatic clock (Vondras / Roach /
  Carrier), not q = mu/s. Nursery selection on sports
  is not Haldane 1927. Dual domestication is human
  choice, not equilibrium load.
Modern data / statistic: frequency of deleterious
  coding alleles in wild sylvestris after clone /
  IBD filters, versus a mutation-selection equilibrium.
  Clone-private load is the Mukai / ratchet job, not
  this one.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild subset for
  equilibrium load. Clone clocks remain Vondras 2019 /
  Roach 2018 / Carrier 2012 (different job). Do not
  invent a grape mutation-load equilibrium paper.
What would falsify it: wild coding load is not at a
  mutation-selection equilibrium after clone filter,
  OR clone-private SNPs are treated as the 1927
  equilibrium (they are not).
What we will not claim: that this note is Haldane 1957
  cost (already filled; does not map). That Mukai 1964
  is this paper. That Vondras 2019 measured q = mu/s.
```

---

## Molecular drive

```
Theory: Molecular drive
Original paper (year): Dover G. 1982. Molecular drive:
  a cohesive mode of species evolution. Nature
  299(5879):111-117 (9 September 1982).
  DOI 10.1038/299111a0 PMID 7110332.
  Nature HTML landing and EuropePMC HTML opened
  (author, title, year, venue, volume, issue, pages,
  DOI, PMID, abstract). Fixation of mutations in a
  family of genes or noncoding sequences may proceed
  by molecular turnover (random or directional) rather
  than by selection or drift; the concerted pattern of
  fixation can establish novelty and species
  discontinuities. Distinct from filled Zimmer et al.
  1980 concerted evolution (within-species paralogs
  more alike than orthologs). 1980 is the pattern;
  1982 is the population-genetic process that can
  drive that pattern through a genome and a
  population. Distinct from filled Nei, Gu and
  Sitnikova 1997 birth-and-death (copies need not
  homogenize). Distinct from filled selfish DNA 1980.
  Wave 5 red line forbade citing Dover 1982 as the
  concerted original; this note fills drive as a
  different job.
One-sentence prediction: Turnover (unequal exchange,
  conversion, transposition) cohesively replaces a
  variant through a repeated family and through the
  population, without requiring selection or drift
  at that locus.
Assumptions: a true repeated family (not palaeo-
  ohnologs); cohesion is not clone IBD; the comparison
  is population-level replacement, not only within-
  genome identity.
Which fail here: tandem NLR arrays are not rRNA.
  Palaeo-hexaploid ohnologs (Jaillon 2007) are DDC /
  gene-balance / fractionation jobs. Clone IBD fakes
  family identity. Birth-and-death is the alternative
  if copies do not homogenize.
Modern data / statistic: within-species identity of
  tandem copies plus population-level replacement of
  one family variant, after clone filter, versus
  orthologs in other Vitis.
Datasets: Jaillon et al. 2007 Nature 449:463-467
  (genome and ohnolog set; do not invent a grape rDNA
  drive paper). Zhou et al. 2019 Nat Plants 5:965-979
  (SVs; tandem change without cohesive replacement).
What would falsify it: tandem copies are not
  cohesively replacing in the population (Zimmer-only
  within-genome identity without population drive, or
  a birth-and-death phylogeny with pseudogenes), OR
  identity is only clone IBD.
What we will not claim: that Zimmer 1980 is this paper
  (pattern, already filled). That Nei 1997 is this
  paper (opposite job). That every NLR array is drive.
```

---

## Gene conversion

```
Theory: Gene conversion (hybrid DNA / mismatch repair)
Original paper (year): Holliday R. 1964. A mechanism
  for gene conversion in fungi. Genetical Research
  5(2):282-304 (July 1964).
  DOI 10.1017/S0016672300001233.
  Cambridge Core HTML landing opened (author Robin
  Holliday, title, volume, issue, pages, year, DOI).
  Homologous strands anneal; if the hybrid spans a
  heterozygous site, mismatch repair converts one
  allele to the other without requiring a replication
  copy-choice. Distinct from filled Galtier,
  Piganeau, Mouchiroud and Duret 2001 gBGC (GC-biased
  conversion as a force on GC content and W-to-S).
  1964 is the conversion mechanism; 2001 is the
  GC-biased population consequence. Distinct from
  filled Dover 1982 (drive as a family-level process)
  and filled Zimmer 1980 (concerted pattern).
  Whitehouse 1963 Nature 199:1034-1040 is a related
  crossing-over scheme, not this paper.
One-sentence prediction: A heteroduplex spanning a
  heterozygous site is repaired to one parental
  sequence, converting one allele to the other, often
  with recombination of flanking markers.
Assumptions: meiosis (or a mitotic analogue) with
  hybrid DNA; conversion is scored as tracts, not as
  a GC or W-to-S map; cuttings skip meiosis.
Which fail here: grafted cuttings have no meiosis
  between years. A chip skeleton is not a conversion
  map (same map rule as BGS / HR / gBGC). Clone IBD
  fakes identity. gBGC is a different job (bias, not
  the mechanism).
Modern data / statistic: conversion tracts (not just
  W-to-S) after clone filter, versus a gBGC GC /
  W-to-S map on a real Vitis recombination map.
Datasets: Zhou et al. 2019 Nat Plants 5:965-979 (SVs;
  do not invent a grape conversion-tract paper).
  Dong et al. 2023 Science (DOI 10.1126/science.add8655)
  only as a panel that still needs a real map. Do not
  invent a grape recombination-map paper.
What would falsify it: no conversion tracts after
  clone filter, OR a W-to-S / GC pattern is treated
  as this paper (that is Galtier 2001 gBGC).
What we will not claim: that Galtier 2001 is this
  paper (already filled as gBGC). That every
  homogenized tandem array is Holliday conversion.
  That a grape gene-conversion paper is locked.
```

---

## Quasispecies

```
Theory: Quasispecies (molecular mutant cloud)
Original paper (year): Eigen M. 1971. Selforganization
  of matter and the evolution of biological
  macromolecules. Naturwissenschaften 58:465-523
  (October 1971). DOI 10.1007/BF00623322.
  Springer HTML landing opened (author Manfred Eigen,
  title, year, venue, volume, pages, DOI). Kinetics of
  replication, mutation, and selection in molecular
  populations. Eigen and Schuster 1977 / 1979
  hypercycle papers name later developments; they are
  not used as the source (same Muller-1964 /
  Felsenstein-1974 split: 1971 is the math).
One-sentence prediction: At a high enough mutation
  rate, a replicating population is a cloud of mutants
  around a master sequence, not a single wild-type
  genotype.
Assumptions: a molecular replicator (RNA virus /
  prebiotic polymer) with mutation rate high enough
  to populate a cloud; a grafted cultivar is not that
  replicator; clone-private SNPs are not a quasispecies
  distribution.
Which fail here: this does not map onto grafted clones.
  A cultivar panel is not an RNA mutant cloud.
  Meristem mosaics and periclinal chimeras are layer
  structure (Satina / Franks), not Eigen kinetics.
  Somatic clocks (Vondras / Roach / Carrier) are not
  a master-sequence distribution.
Modern data / statistic: none that tests Eigen 1971
  in grape. Do not invent a grape quasispecies paper.
What would falsify it: not applicable as a grape
  clone test. The note is filled as "does not map
  onto grafted clones" rather than as an invented
  RNA-cloud experiment.
What we will not claim: that Vondras 2019 measured a
  quasispecies. That a chimera is a mutant cloud.
  That Eigen and Schuster 1977 is the source.
```

---

## Serial founder

```
Theory: Serial founder effect
Original paper (year): Ramachandran S, Deshpande O,
  Roseman CC, Rosenberg NA, Feldman MW, Cavalli-Sforza
  LL. 2005. Support from the relationship of genetic
  and geographic distance in human populations for a
  serial founder effect originating in Africa. Proc
  Natl Acad Sci USA 102(44):15942-15947.
  DOI 10.1073/pnas.0507611102 PMID 16243969
  PMC1276087. EuropePMC HTML landing opened (authors,
  title, year, venue, volume, issue, pages, DOI,
  PMID, PMC, abstract). Heterozygosity is best
  explained by expansion from one origin via successive
  founder events; an equilibrium isolation-by-distance
  reading of FST versus distance is not required.
  Distinct from filled Wright 1943 IBD (equilibrium
  isolation by distance). Distinct from filled Edmonds,
  Lillie and Cavalli-Sforza 2004 allele surfing (front
  mutations reach high frequency). Distinct from
  filled Levins 1969 metapopulation (occupancy /
  extinction). Isolation-by-colonization is not filled
  as a second named original; this is the one lock.
One-sentence prediction: Heterozygosity declines with
  geographic distance from a single origin because
  each colonization is a founder subsample of the last.
Assumptions: one origin and a chain of founders;
  samples are colonizing demes, not clones or
  cultivars; dual domestication is not one origin.
Which fail here: Dong 2023 dual domestication is two
  origins, not one African-style serial founder.
  Humans and nurseries move vines farther than one
  step. A cultivar PCA is not a founder chain. Allele
  surfing is a different job (front mutations, already
  filled).
Modern data / statistic: heterozygosity versus
  distance from a candidate origin among wild
  V. sylvestris after clone + IBD filters, versus a
  single-origin serial-founder decline.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Dual-domestication
  geography; wild sylvestris after clone + IBD
  filters. Use as the two-origin contrast, not as a
  published serial-founder analysis. Do not invent a
  grape out-of-one-refuge paper.
What would falsify it: diversity does not decline
  from one origin after clone + IBD filters (two
  domestication centres, or an equilibrium IBD slope
  with no founder chain). Surfing of front mutations
  is the Edmonds 2004 job, not this one.
What we will not claim: that Dong 2023 fitted a
  serial-founder model. That this note replaces IBD,
  stepping-stone, island, surfing, or metapopulation.
  That a wine-region PCA is a founder chain.
```

---

## Multivariate response / breeder's equation

```
Theory: Multivariate selection response / breeder's
  equation
Original paper (year): Lande R. 1979. Quantitative
  genetic analysis of multivariate evolution, applied
  to brain:body size allometry. Evolution
  33(1Part2):402-416 (1 March 1979).
  DOI 10.1111/j.1558-5646.1979.tb04694.x
  PMID 28568194. EuropePMC HTML landing opened
  (author Russell Lande, title, year, venue, volume,
  issue, pages, DOI, PMID). The mean multivariate
  response is the genetic covariance matrix times the
  selection gradient (G beta; equivalently G P^{-1} s).
  Lush 1937 Animal Breeding Plans is the univariate
  R = h^2 S original and was not opened; lock 1979 as
  the named multivariate paper. Lande 1976 Evolution
  30:314-334 (phenotypic evolution with drift) was
  not used as the source. Distinct from filled Fisher
  1918 infinitesimal (univariate metric trait as many
  small Mendelian loci). Distinct from filled Fisher
  1930 geometric (random mutations in n-space).
One-sentence prediction: The change in the mean
  phenotype equals the genetic covariance matrix
  times the selection gradient; correlated traits
  cannot be selected independently of G.
Assumptions: additive genetic covariances estimated
  from a sexual pedigree; many small-effect loci;
  clones and first-degree cuttings are not the
  relatives; a few large-effect substitutions are not
  a G-matrix response.
Which fail here: berry color, hermaphroditism, and
  muscat / flavor are few large-effect loci (Dong
  2023), not a G-matrix walk. A cultivar panel is not
  a Lande pedigree. Clone IBD fakes a genetic
  covariance.
Modern data / statistic: whether a domestication
  trait's response is G beta after clone + IBD
  filters, versus one or a few large-effect loci.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Color / sex / flavor
  peaks. Use as the large-effect contrast, not as a
  published G-matrix estimate. Do not invent a grape
  GCTA / G-matrix paper.
What would falsify it: a candidate domestication
  trait is explained by one or a few large-effect
  loci (G-matrix / infinitesimal dies for that
  trait). If many small loci remain after clone +
  IBD filters, the single-gene claim dies.
What we will not claim: that Lush 1937 is this paper
  (univariate; not opened). That this note is Fisher
  1918 or Fisher 1930 geometric (different jobs).
  That Dong 2023 estimated G.
```

---

## Endosymbiosis / organelle origin

```
Theory: Endosymbiosis / organelle origin
Original paper (year): Sagan L. 1967. On the origin
  of mitosing cells. Journal of Theoretical Biology
  14(3):225-274 (March 1967; EuropePMC HTML prints
  14(3):255-274; ScienceDirect listing is Volume 14
  Issue 3 pp. 225-274 plus IN plates). Lock the venue
  as the 1967 J Theor Biol paper.
  DOI 10.1016/0022-5193(67)90079-3 PMID 11541392.
  EuropePMC HTML landing opened (author Sagan L,
  title, year, venue, DOI, PMID, abstract). By
  hypothesis, mitochondria, photosynthetic plastids,
  and (9+2) basal bodies were once free-living
  prokaryotic cells. The author later published as
  Lynn Margulis; the 1967 byline is Sagan. Distinct
  from filled Lynch 1996 organelle ratchet (load in
  non-recombining animal mt tRNA, not origin).
  Distinct from filled selfish DNA 1980. Endosymbiotic
  gene transfer is not filled: Timmis, Ayliffe, Huang
  and Martin 2004 Nat Rev Genet is a review (red
  line); a Martin original was not opened this wave.
One-sentence prediction: Mitochondria and plastids
  originated as free-living prokaryotes that became
  organelles, not as autogenous partitions of a
  eukaryotic nucleus.
Assumptions: eukaryogenesis is a historical cell-
  biology claim; a grape cultivar panel is not that
  experiment; organelle mutation accumulation is a
  different job (Lynch 1996 / Muller applied to
  organelles).
Which fail here: this does not map onto grafted
  clones. Jaillon 2007 sequenced a land-plant genome
  that has mitochondria and plastids; that is a
  phylogenetic fact, not a test of 1967
  eukaryogenesis. Clone-private organelle SNPs would
  be the organelle-ratchet job, not this one.
Modern data / statistic: none that tests Sagan 1967
  in grape. Do not invent a grape organelle-origin
  or EGT paper.
What would falsify it: not applicable as a grape
  clone test. The note is filled as "does not map
  onto grafted clones" rather than as an invented
  eukaryogenesis experiment.
What we will not claim: that Jaillon 2007 tested
  endosymbiosis. That Lynch 1996 is this paper
  (organelle ratchet, already filled). That Timmis
  2004 is the source (review). That a grape EGT
  paper is locked.
```

---

---

## Vavilov centers of origin

```
Theory: Vavilov centers of origin (geographical origin of
  cultivated plants)
Original paper (year): Vavilov NI. 1932. The process of
  evolution in cultivated plants. Proceedings of the Sixth
  International Congress of Genetics (Ithaca, New York, 1932)
  1:331-342. ESP facsimile PDF opened
  (http://www.esp.org/books/6th-congress/facsimile/contents/6th-cong-p331-vavilov.pdf);
  ESP TOC HTML opened (chapter page 331, N. I. Vavilov).
  Running headers: "INTERNATIONAL CONGRESS OF GENETICS" /
  "PROCEEDINGS OF THE SIXTH". Author line: N. I. Vavilov,
  Institute of Plant Industry, Leningrad. Title on the
  facsimile is "IN cultivated plants" (ESP TOC said "ON").
  Pages 334-335 lock seven principal world centres of origin
  of cultivated plants (Southwestern Asia / Transcaucasia;
  India; Eastern China; Abyssinia; Mediterranean; Southern
  Mexico and Central America; Peru and Bolivia). Earlier
  Berlin congress had five; this paper updates to seven.
  "The geographical principle in evolution" is the named
  heading (p. 333). Distinct from filled Ramachandran et al.
  2005 serial founder (heterozygosity declining from one
  origin). Distinct from filled Dong-class dual
  domestication as a grape fact; 1932 is the crop-centre
  original. Homologous series is named here (p. 336) as
  Vavilov 1922 J Genet; that 1922 paper was not opened and
  is not this source. Hammer 1984 domestication syndrome
  was not used.
One-sentence prediction: The greatest varietal diversity of
  a cultivated plant, and the keys to its origin, sit in a
  few geographically small primary centres (mountains and
  foothills), not uniformly across the crop's present range.
Assumptions: centres are regions of origin of sexual crop
  species; samples are landraces and wild relatives, not
  clones or nursery cultivars; a vineyard block is not a
  Vavilov centre; dual domestication is not one centre.
Which fail here: grafted cultivars are not landraces.
  Humans and nurseries move vines farther than a foothill
  centre. Dong 2023 dual domestication is two grape origins,
  not the seven-crop map. Feral escapes and clone IBD fake
  a diversity centre.
Modern data / statistic: geographic concentration of wild
  and landrace diversity after clone + IBD filters, versus
  a single (or seven-crop) centre-of-origin decline.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Dual-domestication
  geography; wild sylvestris after clone + IBD filters.
  Use as the two-origin contrast, not as a published
  Vavilov-centre analysis. Do not invent a grape centres-
  of-origin paper.
What would falsify it: grape diversity does not sit in one
  geographically small primary centre after clone + IBD
  filters (two domestication centres, or an equilibrium
  IBD slope with no centre). A wine-region PCA is not the
  test.
What we will not claim: that Dong 2023 fitted Vavilov's
  seven centres. That this note is serial founder
  (Ramachandran 2005, already filled). That Vavilov 1922
  homologous series is this paper. That Hammer 1984 is
  the source.
```

---

## Price equation

```
Theory: Price equation (selection as covariance)
Original paper (year): Price GR. 1970. Selection and
  covariance. Nature 227:520-521 (1 August 1970).
  DOI 10.1038/227520a0 PMID 5428476.
  Nature HTML landing opened (George R. Price, Galton
  Laboratory, University College; title; 227:520-521;
  01 August 1970; DOI; received 12 November 1969).
  EuropePMC HTML opened (Price GR, 01 Aug 1970, Nature
  227(5257):520-521, DOI, PMID). Preliminary communication
  applying a mathematical treatment of selection in general
  to genetical selection. Price 1972 Ann Hum Genet
  35:485-490 (extension of covariance selection mathematics)
  and Price 1972 Ann Hum Genet 36:129-140 (Fisher's
  fundamental theorem) were not used as the source; 1970
  is the named original (same Muller-1964 / Felsenstein-1974
  split). Distinct from filled Lande 1979 multivariate
  G beta (response is covariance times a selection
  gradient in a sexual pedigree). Distinct from filled
  Fisher 1918 infinitesimal and Fisher 1930 geometric.
One-sentence prediction: The change in the mean of a
  character equals its covariance with relative fitness
  (plus a transmission term); selection is that covariance,
  not a named force at one locus.
Assumptions: a well-defined parental and offspring
  generation; fitness and the character are scored on the
  same individuals; clones and cuttings are not that
  generation; a few large-effect substitutions are not a
  covariance partition across many characters.
Which fail here: grafted cuttings skip the sexual
  generation. Berry color, hermaphroditism, and muscat /
  flavor are few large-effect loci (Dong 2023), not a
  Price partition. Clone IBD fakes a parent-offspring
  covariance. Nursery choice of sports is not 1970
  selection.
Modern data / statistic: whether domestication-trait
  change is a fitness-covariance partition after clone +
  IBD filters, versus one or a few large-effect loci.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Color / sex / flavor
  peaks. Use as the large-effect contrast, not as a
  published Price-equation estimate. Do not invent a grape
  Price-equation paper.
What would falsify it: a candidate domestication trait is
  explained by one or a few large-effect loci (the
  covariance partition dies for that trait). If only a
  G-matrix / infinitesimal response remains after clone +
  IBD filters, the single-gene claim dies (that is Lande
  1979 / Fisher 1918, already filled).
What we will not claim: that Price 1972 is this paper.
  That Lande 1979 is this paper (already filled). That
  Dong 2023 estimated a Price covariance. That a nursery
  sport is a 1970 generation.
```

---

## Kin selection / inclusive fitness

```
Theory: Kin selection / inclusive fitness
Original paper (year): Hamilton WD. 1964. The genetical
  evolution of social behaviour. I. Journal of Theoretical
  Biology 7(1):1-16 (July 1964).
  DOI 10.1016/0022-5193(64)90038-4 PMID 5875341.
  EuropePMC HTML opened (Hamilton WD, 01 Jul 1964, J Theor
  Biol 7(1):1-16, DOI, PMID). Part I PDF opened (J. Theoret.
  Biol. (1964) 7, 1-16; received 13 May 1963, revised
  24 February 1964; Galton Laboratory, University College,
  London). A genetical model for interactions between
  relatives; Wright's coefficient of relationship measures
  replica genes; the quantity that incorporates the
  maximizing property of Darwinian fitness is named
  "inclusive fitness"; species following the model evolve
  behaviour that appears to maximize inclusive fitness,
  implying limited restraint on selfish competition and
  limited self-sacrifice. Hamilton 1964 part II (J Theor
  Biol 7:17-52; DOI 10.1016/0022-5193(64)90039-6 PMID
  5875340) is the biological sequel, not used as the
  source (same Muller-1964 / Felsenstein-1974 split).
One-sentence prediction: A social behaviour that lowers
  the actor's direct fitness can still spread if it raises
  inclusive fitness, i.e. if benefits to relatives weighted
  by relatedness outweigh the cost.
Assumptions: social interactions among sexual relatives;
  relatedness is IBD, not clone IBS; a grafted cultivar is
  not a social group; cuttings skip the generation in which
  altruism is scored.
Which fail here: this does not map onto grafted clones.
  A vineyard is not a sibship. Clone IBD is not Hamilton
  relatedness. Meristem layers and chimeras (Satina /
  Franks) are not social interactors. Somatic clocks
  (Vondras / Roach / Carrier) are not inclusive-fitness
  accounting.
Modern data / statistic: none that tests Hamilton 1964
  in grape. Do not invent a grape kin-selection or
  altruism paper.
What would falsify it: not applicable as a grape clone
  test. The note is filled as "does not map onto grafted
  clones" rather than as an invented social-insect
  experiment.
What we will not claim: that Hamilton 1964 part II is the
  source. That a chimera is kin selection. That Trivers
  1974 is this paper (not filled; not a genomics job).
  That Dong 2023 measured inclusive fitness.
```

---

## Nei genetic distance

```
Theory: Nei genetic distance
Original paper (year): Nei M. 1972. Genetic distance
  between populations. The American Naturalist
  106(949):283-292 (May 1972).
  DOI 10.1086/282771.
  Crossref work JSON opened (Masatoshi Nei; title; The
  American Naturalist; volume 106; issue 949; pages
  283-292; published-print 1972-05; DOI 10.1086/282771;
  publisher University of Chicago Press). CiNii HTML
  opened (same author, title, journal, 106(949):283-292,
  1972-05, DOI). Semantic Scholar API opened (M. Nei;
  American Naturalist; 1972; DOI). Chicago journal HTML
  was Cloudflare this wave; no PMID on EuropePMC REST.
  Lock author+year+venue from Crossref + CiNii. Title is
  the named distance; the paper formulates a genetic
  distance from the identity of genes between populations.
  Distinct from filled Wright 1931 island (FST as a
  function of Nem) and filled Wright 1943 IBD (similarity
  declining with continuous distance). Distinct from
  filled Weir and Cockerham 1984 (this wave; the FST
  estimator). Distinct from filled Nei, Gu and Sitnikova
  1997 birth-and-death (a gene-family process, not a
  between-population distance).
One-sentence prediction: Genetic distance from gene
  identity between populations accumulates with time under
  sexual isolation (and with geography in some migration
  models); clones and forced-biallelic chips are not that
  identity.
Assumptions: allele frequencies from random samples of
  populations, not clones or first-degree cuttings; identity
  is not clone IBS; dual domestication is not one split;
  a cultivar PCA is not a Nei tree.
Which fail here: a cultivar panel is not two random
  populations. Clone IBD fakes gene identity. SNP chips
  are biallelic. Dong 2023 dual domestication is two
  origins, not one clock-linear split. Humans and nurseries
  move vines farther than isolation.
Modern data / statistic: Nei D (or a sequence analogue)
  among wild V. sylvestris patches after clone + IBD
  filters, versus a single-split clock or a dual-
  domestication two-cluster pattern.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset
  after clone + IBD filters. Use as geography / split
  structure, not as a published Nei-distance analysis.
  Do not invent a grape genetic-distance paper.
What would falsify it: D among wild patches is not a
  single-split accumulation after clone + IBD filters
  (two domestication centres, or an IBD slope with no
  split). Clone IBS treated as gene identity is not the
  test.
What we will not claim: that Nei 1997 is this paper
  (already filled as birth-and-death). That Wright 1931
  or 1943 is this paper. That Dong 2023 reported Nei D.
  That a wine-region PCA is a genetic-distance tree.
```

---

## Weir-Cockerham FST

```
Theory: Weir-Cockerham FST estimator
Original paper (year): Weir BS, Cockerham CC. 1984.
  Estimating F-statistics for the analysis of population
  structure. Evolution 38(6):1358-1370 (1 November 1984).
  DOI 10.1111/j.1558-5646.1984.tb05657.x PMID 28563791.
  EuropePMC HTML opened (Weir BS, Cockerham CC;
  Department of Statistics, North Carolina State
  University; 01 Nov 1984; Evolution 38(6):1358-1370;
  DOI; PMID). Wiley / OUP HTML not used (prior-wave
  Cloudflare pattern). Wright 1951 / 1965 named FST,
  FIT, and FIS; 1931 already filled as the island-model
  math. 1984 is the moment estimator from allele-frequency
  variance that accounts for sample size, number of
  populations, and multiple alleles (Cockerham 1969 / 1973
  parameters extended). Distinct from filled Wright 1931
  island (the parameter FST = f(Nem), no distance decay).
  Distinct from filled Wright 1943 IBD and Kimura and
  Weiss 1964 stepping-stone. Distinct from filled Nei 1972
  genetic distance (this wave; a between-population
  identity distance, not an FST estimator).
One-sentence prediction: Population structure is summarized
  by moment estimates of FST / FIT / FIS from allele-
  frequency variance; finite samples and unequal deme
  sizes are part of the estimator, not nuisances to ignore.
Assumptions: samples are demes, not clones or cultivars;
  a vineyard block is not a deme; clone IBS is not
  coancestry; the island formula is not plugged in as the
  data function.
Which fail here: grafted cultivars are not demes. Clone
  IBD fakes FST. A wine-region PCA is not a Weir-Cockerham
  analysis. Dual domestication and human transport violate
  the island reading already filled as Wright 1931.
Modern data / statistic: Weir-Cockerham FST among wild
  V. sylvestris patches after clone + IBD filters, versus
  distance (island: no decay; IBD / stepping-stone: decay).
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset
  after clone + IBD filters. Use as structure, not as a
  published WC-FST analysis. Do not invent a grape FST
  paper.
What would falsify it: WC FST among wild patches is not
  independent of distance after clone filter (the island
  reading dies; that is the Wright 1931 job already
  filled). Treating clone IBS as FST is not the test.
What we will not claim: that Wright 1931 is this paper
  (island math, already filled). That Nei 1972 is this
  paper. That Dong 2023 reported Weir-Cockerham FST.
  That a cultivar PCA is an FST table.
```

---

## Orr exponential factors

```
Theory: Orr exponential distribution of adaptive factors
Original paper (year): Orr HA. 1998. The population
  genetics of adaptation: the distribution of factors
  fixed during adaptive evolution. Evolution 52(4):935-949
  (1 August 1998).
  DOI 10.1111/j.1558-5646.1998.tb01823.x PMID 28565213.
  EuropePMC HTML opened (Orr HA, Department of Biology,
  University of Rochester; 01 Aug 1998; Evolution
  52(4):935-949; DOI; PMID; abstract). Using Fisher's
  geometric model, the size distribution of factors fixed
  on a stepwise walk to a phenotypic optimum is
  approximately exponential; the result is insensitive to
  the fitness function and to the input distribution of
  mutational effects. Distinct from filled Fisher 1930
  geometric (chance a random mutation of size r improves;
  Clarendon pages 38-41). 1930 is the geometry of one
  mutation; 1998 is the distribution of factors that
  actually fix on the walk. Distinct from filled Fisher
  1918 infinitesimal (many small Mendelian loci for a
  metric trait) and filled Lande 1979 G beta. Distinct
  from filled Hermisson and Pennings 2005 soft sweep
  (standing / recurrent copies, not the size distribution
  of substitutions). Orr 2005 Nat Rev Genet is a review
  (red line); not used as the source.
One-sentence prediction: Factors fixed during adaptation
  toward a fixed optimum are approximately exponential in
  phenotypic effect: most are small, a few are large, and
  the largest is larger than a one-step Fisher reading.
Assumptions: a walk of sexual substitutions toward an
  optimum; mutations are drawn, then filtered by fixation;
  clones are not a walk; a few domestication loci of very
  large effect are not an exponential series.
Which fail here: berry color, hermaphroditism, and muscat /
  flavor in grape are few large-effect domestication
  substitutions (Dong 2023), not an exponential walk of
  many factors. A cultivar panel is not Orr's walk.
  Clone sports are not substitutions. Cuttings skip the
  stepwise generations.
Modern data / statistic: effect-size distribution of
  domestication substitutions after clone + IBD filters,
  versus an exponential series of fixed factors.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Color / sex / flavor
  peaks. Use as the large-effect contrast, not as a
  published Orr-walk fit. Do not invent a grape adaptive-
  walk paper.
What would falsify it: a candidate domestication trait is
  explained by one or a few large-effect loci (the
  exponential walk dies for that trait). If many small
  fixed factors remain after clone + IBD filters, the
  single-gene claim dies (Fisher 1918 / Lande 1979 jobs).
What we will not claim: that this note is Fisher 1930
  geometric (already filled). That Orr 2005 is the source
  (review). That Dong 2023 fitted an exponential series.
  That a nursery sport is a fixed factor.
```

---

## Y-chromosome degeneration

```
Theory: Y-chromosome degeneration (ratchet on a
  non-recombining sex chromosome)
Original paper (year): Charlesworth B. 1978. Model for
  evolution of Y chromosomes and dosage compensation.
  Proc Natl Acad Sci USA 75(11):5618-5622 (1 November
  1978). DOI 10.1073/pnas.75.11.5618 PMID 281711
  PMC393018. EuropePMC HTML opened (Charlesworth B;
  01 Nov 1978; PNAS 75(11):5618-5622; DOI; PMID; PMC;
  abstract). An alternative to the classical inverted-Y
  model: Muller's ratchet in the absence of crossing-over
  raises the number of mutant loci on an average Y
  (individual deleterious alleles stay rare); selection
  then increases X activity in the heterogametic sex at
  the expense of the Y, yielding an inert Y and dosage
  compensation. Distinct from filled Muller 1964 (whole-
  genome ratchet) and filled Haldane 1922 (heterogametic
  hybrid sterility; does not map onto Vitis SDR). Distinct
  from filled Baker 1955 (self-compatible colonists; Dong
  2023 sex haplotypes are that test). Charlesworth 1991
  Science 251:1030-1033 (PMID 1998119) is tagged Review on
  EuropePMC; red line; not the source. No 1994
  Charlesworth paper titled "The evolution of sex
  chromosomes" was found; do not invent one.
One-sentence prediction: A non-recombining Y accumulates
  deleterious load by ratchet and becomes genetically
  inert, while the X evolves dosage compensation.
Assumptions: a pair of sex chromosomes with suppressed
  recombination; finite N; the SDR is old enough for
  degeneration; grape is not assumed to be XX/XY; a young
  plant SDR may still recombine.
Which fail here: Vitis sex is a chromosome-2 SDR, not a
  degenerated animal Y (Haldane 1922 already filled as
  does-not-map for heterogametic sterility). Dong 2023
  hermaphrodite haplotypes H1/H2 from M x f recombination
  imply recombination is not fully suppressed. Grafted
  clones skip meiosis between cuttings. Cuttings are not
  a Y-ratchet generation.
Modern data / statistic: gene loss / load / recombination
  suppression on the Dong 2023 chromosome-2 SDR after
  clone filter, versus a degenerated inert Y plus dosage
  compensation.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Chromosome-2 SDR; H1/H2
  hermaphrodite haplotypes. Use as the young-SDR contrast,
  not as a published Y-degeneration analysis. Do not
  invent a grape Y-chromosome paper.
What would falsify it: the Vitis SDR shows little Y-like
  degeneration and recombination still present after clone
  filter (H1/H2 from M x f). Treating Haldane's rule as
  this paper is not the test (already filled as does-not-
  map). Whole-genome clone load is the Muller 1964 job.
What we will not claim: that Charlesworth 1991 is the
  source (review). That a 1994 sex-chromosome paper is
  locked. That Haldane 1922 is this paper. That Dong 2023
  tested Y degeneration. That Baker 1955 is this paper.
```

---

## Biological species concept

```
Theory: Biological species concept
Original paper (year): Mayr E. 1942. Systematics and the
  Origin of Species from the Viewpoint of a Zoologist.
  New York: Columbia University Press. Columbia biological
  series no. 13. 334 pages.
  Google Books bibliographic page opened
  (https://books.google.com/books/about/Systematics_and_the_Origin_of_Species_fr.html?id=XxMgAQAAMAAJ):
  Ernst Mayr; Columbia University Press, 1942; 334 pages;
  Columbia biological series no. 13; general editor L. C.
  Dunn. Same book standard as filled Maynard Smith 1978 /
  Anderson 1949 / Klekowski 1988. Archive.org scan HTML
  timed out this wave (identifier
  systematicsorigi0000mayr_p0y7 is a reprint listing);
  definition page not locked in a 1942 page image. Lock
  1942 as the named biological-species book. Founder
  effect / founder principle is not this lock (often Mayr
  1954; that paper was not opened). Distinct from filled
  Dobzhansky 1937 BDM book (two-locus hybrid
  incompatibility as a mechanism) and filled Dobzhansky
  1940 reinforcement (premating isolation in sympatry).
  Distinct from filled Ramachandran et al. 2005 serial
  founder (heterozygosity from one origin).
One-sentence prediction: Species are groups of
  interbreeding natural populations that are reproductively
  isolated from other such groups; rank below that
  (subspecies, cultivars) is not a species split.
Assumptions: sexual populations that can be tested for
  interbreeding and isolation; a cultivar x cultivar cross
  is not a species test; gene flow is caution, not a
  species name; clones are not populations.
Which fail here: V. vinifera ssp. sylvestris and ssp.
  vinifera interbreed; treating them as two biological
  species is a rank error. Dong 2023 Syl-W gene flow into
  cultivar groups is CAUTION that isolation is incomplete.
  Nursery hybrids are not secondary contact (reinforcement
  job already filled). A vineyard is not a Mayr population.
Modern data / statistic: whether wild sylvestris and
  cultivated vinifera remain reproductively isolated after
  clone + IBD filters, versus gene flow / a single
  biological species with dual domestication.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Dual domestication; Syl-W
  gene flow into CG3-CG6 is CAUTION, not a BSC
  demonstration. Do not invent a grape biological-species
  paper.
What would falsify it: sylvestris and vinifera are not
  isolated (gene flow after clone + IBD filters; they are
  one biological species with subspecies rank). Hybrid
  inviability mapping to a single locus is the BDM job
  (already filled), not this definition.
What we will not claim: that Dobzhansky 1937 is this paper
  (BDM mechanism, already filled). That Mayr 1954 founder
  is this paper (not opened). That Dong 2023 applied the
  biological species concept. That a cultivar name is a
  species.
```

---

## HKA test

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

---

## Lewontin-Krakauer FST outliers

```
Theory: Lewontin-Krakauer test (F heterogeneity among loci)
Original paper (year): Lewontin RC, Krakauer J. 1973. Distribution
  of gene frequency as a test of the theory of the selective
  neutrality of polymorphisms. Genetics 74(1):175-195 (1 May 1973).
  DOI 10.1093/genetics/74.1.175 PMID 4711903 PMCID PMC1212935.
  EuropePMC HTML opened (Lewontin RC, Krakauer J; 01 May 1973;
  Genetics 74(1):175-195; DOI; PMID; PMC; abstract). PMC HTML
  opened (Department of Theoretical Biology / Department of
  Biology, University of Chicago; received 14 February 1972;
  revision requested 16 January 1973). Breeding structure should
  affect all loci the same way; significant heterogeneity among
  loci in apparent inbreeding coefficients
  F = s(p)^2 / p(1-p) is evidence for selection. Human polymorphic
  genes showed highly significant heterogeneity in F worldwide;
  temporal variation in Dacus oleae did not. Distinct from filled
  Wright 1931 island (FST as a function of Nem, no locus test).
  Distinct from filled Wright 1943 IBD and filled Weir and
  Cockerham 1984 (the moment estimator, not a heterogeneity
  test). Distinct from filled Kimura 1968 (the neutral null).
  Beaumont and Nichols 1996 is a later method; not used.
One-sentence prediction: Loci that share a breeding structure
  share F; a locus whose F is an outlier relative to the others
  is a candidate for selection.
Assumptions: samples are demes, not clones or cultivars; F is
  not clone IBS; chips are not forced-biallelic loci; dual
  domestication is not one breeding structure; a vineyard is
  not a deme.
Which fail here: grafted cultivars are not demes. Clone IBD
  fakes F. SNP chips are biallelic. Dual domestication and
  human transport violate a single shared breeding structure.
  A wine-region PCA is not a Lewontin-Krakauer table.
Modern data / statistic: heterogeneity of locus F (or FST)
  among wild V. sylvestris patches after clone + IBD filters,
  versus a single shared breeding-structure null.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset after
  clone + IBD filters. Use as structure, not as a published
  Lewontin-Krakauer analysis. Do not invent a grape FST-outlier
  paper.
What would falsify it: F among wild-patch loci is not
  heterogeneous after clone + IBD filters (the selection
  reading dies). Treating clone IBS as F is not the test.
  Island / IBD / WC-estimator jobs remain other notes.
What we will not claim: that Wright 1931 or 1943 is this
  paper. That Weir-Cockerham 1984 is this paper. That
  Beaumont and Nichols 1996 is the source. That Dong 2023
  ran a Lewontin-Krakauer test. That a cultivar PCA is an
  F-outlier table.
```

---

## Fay-Wu H

```
Theory: Fay-Wu H (derived high-frequency hitchhiking)
Original paper (year): Fay JC, Wu CI. 2000. Hitchhiking under
  positive Darwinian selection. Genetics 155(3):1405-1413
  (1 July 2000). DOI 10.1093/genetics/155.3.1405 PMID 10880498
  PMCID PMC1461156. EuropePMC HTML opened (Fay JC, Committee
  on Genetics, University of Chicago; Wu CI; 01 Jul 2000;
  Genetics 155(3):1405-1413; DOI; PMID; PMC; abstract). PMC
  HTML opened (same authors, venue, abstract). If recombination
  is present but rare, linked variation hitchhikes to low or
  high frequency; an excess of derived variants at high
  frequency is a unique hitchhiking pattern (derived =
  nonancestral state from an outgroup). Statistic H measures
  excess of high compared with intermediate frequency variants.
  Distinct from filled Maynard Smith and Haigh 1974 (linked
  diversity collapses around a sweep; no derived-frequency
  statistic). Distinct from filled Tajima 1989 (pi versus
  theta_W in one sample; no outgroup). Distinct from filled
  HKA 1987 (polymorphism-divergence scaling) and filled
  McDonald and Kreitman 1991 (Dn/Ds versus Pn/Ps). Fu 1997
  Genetics 147:915-925 is a later neutrality battery; not
  used as the source.
One-sentence prediction: A recent hitchhiking event leaves
  an excess of derived high-frequency variants at linked
  sites (negative H); neutrality and BGS do not produce that
  excess.
Assumptions: a random sample of sequences plus an outgroup;
  derived state is not clone IBS; polymorphism is not
  clone-private SNPs; a cultivar panel is not that sample;
  chips are not forced-biallelic loci.
Which fail here: a cultivar panel is not a random sample.
  Clone IBD fakes high-frequency derived alleles. Pedigree
  repeats are not new mutations. Dual domestication is human
  choice, not a sweep generation. SNP chips are biallelic.
Modern data / statistic: Fay-Wu H at candidate domestication
  loci on Dong-class WGS after clone + IBD filters, versus
  the high-frequency-derived null. Tajima and HKA remain
  other jobs.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Color / sex / flavor peaks.
  Use as the hitchhiking contrast, not as a published Fay-Wu
  analysis. Do not invent a grape Fay-Wu paper.
What would falsify it: no excess of derived high-frequency
  variants after clone + IBD filters (H does not reject).
  Treating clone IBS as derived high frequency is not the
  test. Diversity collapse without an outgroup is the 1974
  hitchhiking job; one-sample Tajima D is the 1989 job.
What we will not claim: that Maynard Smith and Haigh 1974
  is this paper (already filled). That Tajima 1989 or HKA
  1987 is this paper. That Fu 1997 is the source. That
  Dong 2023 computed H. That a nursery sport is a hitchhiking
  haplotype.
```

---

## Fu-Li tests

```
Theory: Fu-Li tests (external versus internal mutations)
Original paper (year): Fu YX, Li WH. 1993. Statistical tests
  of neutrality of mutations. Genetics 133(3):693-709
  (1 March 1993). DOI 10.1093/genetics/133.3.693 PMID 8454210
  PMCID PMC1205353. EuropePMC HTML opened (Fu YX, Center for
  Demographic and Population Genetics, University of Texas,
  Houston; Li WH; 01 Mar 1993; Genetics 133(3):693-709; DOI;
  PMID; PMC; abstract). Mutations in a sample genealogy are
  external (on external branches) or internal (on internal
  branches). Under neutrality the expected number of external
  mutations equals theta = 4 Ne mu, independent of sample
  size; external counts deviate under selection while internal
  counts are less affected. Several tests of the all-mutations-
  neutral hypothesis follow from those properties and from
  two common theta estimates. Distinct from filled Tajima 1989
  (pi versus theta_W; no external/internal split). Distinct
  from filled Watterson 1975 (S as a theta estimator) and
  filled Kimura 1969 infinite-sites. Distinct from filled
  HKA 1987 and filled Fay and Wu 2000 H (this wave; derived
  high-frequency excess, not external-branch counts).
One-sentence prediction: Selection (or a non-neutral
  demography that mimics it) shows up first as a deviation
  of external mutations from theta; internal mutations stay
  closer to the neutral expectation.
Assumptions: a random sample of DNA sequences from one
  population; the genealogy is Kingman-like, not a clone
  pedigree; external mutations are not clone-private SNPs;
  chips are not forced-biallelic loci.
Which fail here: a cultivar panel is not a random sample.
  Clone IBD fakes external mutations. Cuttings skip the
  sexual genealogy. Dual domestication is not one population.
  SNP chips are biallelic.
Modern data / statistic: Fu-Li D / F (or an external-versus-
  internal analogue) on Dong-class WGS after clone + IBD
  filters, versus the neutral theta expectation. Tajima and
  Fay-Wu remain other jobs.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild versus cultivar /
  other Vitis after clone + IBD filters. Use as a Fu-Li-
  style test, not as a published grape Fu-Li paper. Do not
  invent a grape Fu-Li paper.
What would falsify it: external versus internal counts do
  not reject neutrality after clone + IBD filters, OR
  clone-private SNPs are treated as external mutations
  (they are not). One-sample Tajima D is the 1989 job;
  derived high-frequency excess is the Fay-Wu job.
What we will not claim: that Tajima 1989 is this paper
  (already filled). That Fay and Wu 2000 is this paper.
  That Watterson 1975 is this paper. That Dong 2023 ran
  Fu-Li tests. That a chimera layer is an external branch.
```

---

## Slatkin private-allele gene flow

```
Theory: Slatkin private-allele estimator of gene flow
Original paper (year): Slatkin M. 1985. Rare alleles as
  indicators of gene flow. Evolution 39(1):53-65
  (1 January 1985). DOI 10.1111/j.1558-5646.1985.tb04079.x
  PMID 28563643. EuropePMC HTML opened (Slatkin M,
  Department of Zoology, NJ-15, University of Washington,
  Seattle; 01 Jan 1985; Evolution 39(1):53-65; DOI; PMID;
  abstract). Log of the average number of migrants exchanged
  between local populations, Nm, is approximately linearly
  related to the log of the average frequency of private
  alleles, p(1); the relation is relatively insensitive to
  other parameters except Nm and the number of individuals
  sampled. Applied to 16 species, estimated Nm ranged from
  much greater than 1 to less than 0.1, confirming the
  qualitative analysis of Slatkin 1981. Distinct from filled
  Wright 1931 island (FST = f(Nem) as the parameter, not a
  private-allele estimator). Distinct from filled Wright
  1943 IBD and filled Kimura and Weiss 1964 stepping-stone.
  Distinct from filled Weir and Cockerham 1984 (moment FST).
  Slatkin 1987 Science 236:787-792 (PMID 3576198) is a
  review of direct and indirect gene-flow methods; red line;
  not the source. Slatkin 1981 is the qualitative precursor,
  not used as the source (same Muller-1964 / Felsenstein-1974
  split).
One-sentence prediction: The rarer the private alleles in
  a set of local samples, the larger Nm; private alleles
  that are common imply little gene flow.
Assumptions: samples are local sexual populations, not
  clones or cultivars; a private allele is not a clone-
  private SNP or a nursery sport; sample size is scored
  (the paper's correction); a vineyard block is not a
  local population.
Which fail here: grafted cultivars are not demes. Clone
  IBD fakes private alleles. Humans and nurseries move
  vines farther than local migration. Dual domestication
  is not one subdivided species with a single Nm.
Modern data / statistic: private-allele frequency among
  wild V. sylvestris patches after clone + IBD filters,
  converted to Nm, versus an island / IBD / stepping-stone
  reading.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset
  after clone + IBD filters. Use as structure, not as a
  published private-allele analysis. Do not invent a grape
  gene-flow paper.
What would falsify it: private-allele Nm among wild patches
  is not a migration estimate after clone filter (clone-
  private SNPs treated as private alleles are not the test).
  FST independent of distance is the Wright 1931 job;
  continuous IBD slope is the Wright 1943 job.
What we will not claim: that Slatkin 1987 is the source
  (review). That Slatkin 1981 is this paper. That Wright
  1931 or Weir-Cockerham 1984 is this paper. That Dong
  2023 estimated Nm from private alleles. That a cultivar
  private SNP is a migrant.
```

---

## Slatkin IBD from pairwise M

```
Theory: Slatkin isolation by distance from pairwise M
Original paper (year): Slatkin M. 1993. Isolation by
  distance in equilibrium and non-equilibrium populations.
  Evolution 47(1):264-279 (1 February 1993).
  DOI 10.1111/j.1558-5646.1993.tb01215.x PMID 28568097.
  EuropePMC HTML opened (Slatkin M, Department of
  Integrative Biology, University of California, Berkeley;
  01 Feb 1993; Evolution 47(1):264-279; DOI; PMID;
  abstract). For allele-frequency data a useful pairwise
  gene-flow measure is M = (1/FST - 1)/4, the estimated
  island-model Nm at equilibrium; for sequences, replace
  FST by NST. Analytic theory gives a simple relationship
  between M and geographic distance in both equilibrium and
  non-equilibrium populations, approximately independent of
  mutation rate when that rate is small. Simulations show
  IBD can be detected with reasonable samples and that some
  non-equilibrium patterns can be distinguished. Applied to
  gull and pocket-gopher allozymes. Distinct from filled
  Wright 1943 IBD (continuous isolation by distance as the
  process; no pairwise-M diagnostic). 1993 is the FST-based
  estimator of that pattern, the same split as filled Weir-
  Cockerham 1984 versus filled Wright 1931 island math.
  Distinct from filled Kimura and Weiss 1964 stepping-stone
  and from filled Slatkin 1985 private alleles (this wave;
  a different gene-flow estimator). Distinct from filled
  serial founder (Ramachandran et al. 2005).
One-sentence prediction: Pairwise M declines with geographic
  distance under restricted dispersal, in both equilibrium
  and some non-equilibrium histories; a flat M-distance
  plot is not that pattern.
Assumptions: pairs are demes, not clones or cultivars; FST
  is not clone IBS; a vineyard is not a pair of demes;
  dual domestication is not one expanding range; mutation
  is small relative to migration.
Which fail here: grafted cultivars are not demes. Clone
  IBD fakes FST and therefore M. Humans and rivers move
  vines farther than restricted dispersal. Dual
  domestication is two origins, not one IBD surface.
Modern data / statistic: pairwise M among wild
  V. sylvestris patches after clone + IBD filters, versus
  geographic distance (IBD: decline; island: flat).
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset
  after clone + IBD filters. Use as geography, not as a
  published Slatkin-M analysis. Do not invent a grape
  isolation-by-distance estimator paper.
What would falsify it: M among wild patches is not a
  function of distance after clone filter (the restricted-
  dispersal reading dies). Treating clone IBS as FST is
  not the test. Wright 1943 remains the continuous-space
  original; this note is the pairwise-M diagnostic.
What we will not claim: that Wright 1943 is this paper
  (already filled). That Slatkin 1985 is this paper.
  That Ramachandran 2005 is this paper. That Dong 2023
  reported pairwise M. That a wine-region PCA is an
  M-distance plot.
```

---

## Hybrid-zone dynamics

```
Theory: Hybrid-zone dynamics (tension zone)
Original paper (year): Barton NH. 1979. The dynamics of
  hybrid zones. Heredity 43(3):341-359 (1 December 1979).
  DOI 10.1038/hdy.1979.87. Nature / Heredity HTML opened
  (N. H. Barton, School of Biological Sciences, University
  of East Anglia, Norwich NR4 7TJ; received 14 March 1979;
  issue date 01 December 1979; DOI; summary). Hybrid zones
  maintained by a balance between dispersal and selection
  against hybrids: a single-locus zone can move in response
  to a selective imbalance between homozygotes and to
  variation in density or dispersal; it can be trapped by
  natural barriers, so an allele selected against when rare
  cannot advance even if advantageous when common. The
  continuous model approximates a stepping-stone cline that
  contains several demes. Sampling drift is negligible
  unless the zone includes few organisms and few loci;
  barriers still trap zones, so they remain roughly where
  they first formed. Distinct from filled Anderson 1949
  introgression / hybrid swarm (backcross tracts are
  geographically clinal). Distinct from filled Dobzhansky
  1940 reinforcement (premating isolation completes in
  sympatry). Distinct from filled Mayr 1942 BSC.
  Barton and Hewitt 1985 Annu Rev Ecol Syst 16:113-148 is
  a review; red line; not the source. Barton and Hewitt
  1980 chapter (in press in the 1979 reference list) is
  later; not used.
One-sentence prediction: A tension zone sits where
  dispersal into the zone is balanced by selection against
  hybrids; it can shift with density or selection but is
  trapped by barriers and is not a nursery cross.
Assumptions: two sexual populations meet along a front;
  hybrids are unfit relative to parentals; a cultivar x
  cultivar cross is not a tension zone; gene flow without
  a cline is not this model; clones are not hybridizing
  demes.
Which fail here: nursery hybrids are not secondary contact.
  Dong 2023 Syl-W gene flow into CG3-CG6 is CAUTION that
  isolation is incomplete, not a mapped tension zone.
  Treating sylvestris and vinifera as two biological
  species is the Mayr 1942 job. A vineyard is not a Barton
  front.
Modern data / statistic: whether a wild-cultivar contact
  is a trapped cline (dispersal versus hybrid unfitness)
  after clone + IBD filters, versus diffuse gene flow /
  a single biological species.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Syl-W gene flow into
  CG3-CG6 is CAUTION, not a Barton-zone demonstration.
  Do not invent a grape hybrid-zone paper.
What would falsify it: contact is not a trapped cline
  (gene flow after clone + IBD filters with no hybrid-
  unfitness barrier). Single-locus hybrid inviability is
  the BDM job (already filled). Premating isolation in
  sympatry is the reinforcement job (already filled).
What we will not claim: that Barton and Hewitt 1985 is
  the source (review). That Anderson 1949 is this paper.
  That Dobzhansky 1940 is this paper. That Dong 2023
  mapped a tension zone. That a nursery hybrid is a
  hybrid zone.
```

---

## Geographic variation / clines

```
Theory: Geographic variation / clines (parapatric
  differentiation despite gene flow)
Original paper (year): Endler JA. 1977. Geographic
  Variation, Speciation, and Clines. Princeton: Princeton
  University Press. Monographs in Population Biology 10.
  262 pages. ISBN 9780691081922.
  Princeton University Press HTML opened
  (https://press.princeton.edu/books/paperback/9780691081922/geographic-variation-speciation-and-clines):
  John A. Endler; published 21 September 1977; copyright
  1978; 262 pages; ISBN 9780691081922; Monographs in
  Population Biology. Same book standard as filled Mayr
  1942 / Maynard Smith 1978 / Anderson 1949 / Klekowski
  1988. Publisher blurb on that live page: earlier writers
  thought intense geographic differentiation and speciation
  required complete isolation; Endler shows geographic
  differentiation and speciation may develop in spite of
  continuous gene flow (steep clines; parapatric
  speciation; hybrid zones; sexual isolation). Distinct
  from filled Wright 1943 IBD (similarity declines with
  continuous distance; not a speciation-despite-gene-flow
  claim). Distinct from filled Barton 1979 (this wave;
  tension-zone dynamics, not the cline / parapatric book).
  Distinct from filled Mayr 1942 BSC and filled
  Ramachandran et al. 2005 serial founder.
One-sentence prediction: Steep clines, and a parapatric
  split, can form along an environmental gradient even
  when gene flow is continuous; complete isolation is not
  required.
Assumptions: sexual populations arranged in space, not
  clones or cultivars; a vineyard is not a cline; dual
  domestication is not one gradient; human transport is
  not Endler gene flow.
Which fail here: humans and nurseries move vines farther
  than a continuous cline. Dong 2023 dual domestication
  is two origins, not one parapatric split. Syl-W gene
  flow is CAUTION that isolation is incomplete, not an
  Endler cline. A wine-region PCA is not a cline.
Modern data / statistic: whether wild sylvestris /
  cultivar geography is a steep environmental cline
  after clone + IBD filters, versus two domestication
  centres or an equilibrium IBD slope with no split.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Dual-domestication
  geography; Syl-W gene flow. Use as the two-origin /
  gene-flow contrast, not as a published Endler-cline
  analysis. Do not invent a grape cline paper.
What would falsify it: grape geography is not a steep
  cline or parapatric split after clone + IBD filters
  (two domestication centres, or an IBD slope with no
  environmental step). Wright 1943 remains the continuous
  IBD original; Barton 1979 remains the tension-zone
  original.
What we will not claim: that Wright 1943 is this paper
  (already filled). That Barton 1979 is this paper.
  That Mayr 1942 is this paper. That Dong 2023 fitted
  an Endler cline. That a cultivar name is a subspecies
  on a cline.
```

---

## Mutational / genetic load

```
Theory: Mutational / genetic load (Crow partition)
Original paper (year): Crow JF. 1958. Some possibilities
  for measuring selection intensities in man. Human
  Biology 30(1):1-13 (February 1958). PMID 13513111.
  EuropePMC REST JSON opened (CROW JF; Hum Biol 30(1):1-13;
  1958 Feb; PMID 13513111; Journal Article). 1989 Wayne
  State reprint PDF opened
  (https://freethoughtblogs.com/pharyngula/files/2015/01/crow_selectioninman.pdf):
  Human Biology, February 1958, Vol. 30, No. 1, pp. 1-13;
  reprinted Human Biology 61(5/6):763-775 (1989); James F.
  Crow, University of Wisconsin. Genetic load is the
  proportion by which population fitness is decreased
  relative to an optimum genotype. Three components:
  mutational load (fitness lowered by recurrent harmful
  mutants; at equilibrium Lm equals the mutation rate,
  following Haldane 1937); segregation load (inferior
  homozygotes from an unfixable superior heterozygote);
  incompatibility load (parent-offspring serological
  mismatch). Mutation load is sensitive to inbreeding;
  segregation load is not. Distinct from filled Haldane
  1957 cost of selection (generation-equivalents of
  selective death per substitution; does-not-map).
  Distinct from filled Haldane 1927 mutation-selection
  balance (the equilibrium frequency q, not the load
  partition). Distinct from filled Muller 1964 ratchet
  (least-loaded class lost without recombination).
  Muller 1950 Am J Hum Genet 2:111-176 (Our load of
  mutations; PMID 14771033 PMC1716299) was opened as a
  landing only (no abstract or body); not the source.
  Morton, Crow and Muller 1956 PNAS 42:855-863 is the
  consanguinity application named in 1958; no abstract
  opened; not used as the source (same Muller-1964 /
  Felsenstein-1974 split).
One-sentence prediction: Standing mean fitness is lower
  than the optimum by a mutational load of order equal
  to the mutation rate, plus a segregation load if
  heterozygotes are unfixable; inbreeding inflates the
  mutational component.
Assumptions: a sexual population at mutation-selection
  (or segregation) equilibrium; fitness is scored on
  that generation; grafted clones are not that
  equilibrium; clone-private SNPs are not q; a vineyard
  is not a Crow population.
Which fail here: grafted cuttings skip the sexual
  generation in which load is paid. Clone-private SNPs
  are not the mutational-load sample. Standing clone
  heterozygosity is not a segregation load. Roach 2018
  ancestral inbreeding is CAUTION for the inbreeding
  contrast (already used on Darwin 1876), not a Crow
  load estimate. Haldane 1957 remains does-not-map.
Modern data / statistic: whether wild coding load after
  clone + IBD filters is a Crow mutational-load
  partition (order of the mutation rate; inflated by
  inbreeding), versus ratchet accumulation or a few
  large-effect domestication loci.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset
  after clone + IBD filters. Use as a load contrast,
  not as a published Crow-load analysis. Do not invent
  a grape genetic-load paper. Roach 2018 ancestral
  inbreeding is CAUTION only.
What would falsify it: wild coding load is not a
  mutational-load partition after clone filter (not
  order of mu; not inflated by inbreeding). Treating
  clone-private SNPs as q is not the test. Equilibrium
  frequency of a deleterious allele is the Haldane 1927
  job; substitution cost is the 1957 job; whole-genome
  clone load is the Muller 1964 job.
What we will not claim: that Muller 1950 is the source
  (landing only; no body). That Morton, Crow and Muller
  1956 is this paper. That Haldane 1957 or 1927 is this
  paper. That Dong 2023 estimated a Crow load. That a
  nursery sport is a segregation-load heterozygote.
```

---

---

## Haldane cline

```
Theory: Haldane cline (selection-migration slope at a boundary)
Original paper (year): Haldane JBS. 1948. The theory of a cline.
  Journal of Genetics 48(3):277-284 (January 1948).
  DOI 10.1007/BF02986626 PMID 18905075.
  IAS HTML opened
  (https://www.ias.ac.in/article/fulltext/jgen/048/03/0277-0284):
  J. B. S. Haldane, F.R.S.; Journal of Genetics 48 number 3;
  January 1948; summary. EuropePMC HTML opened (HALDANE JB;
  01 Jan 1948; Journal of Genetics 48(3):277-284; DOI; PMID; no
  abstract there). Where one phenotype is favoured in one area
  and another phenotype in a neighbouring area, the character
  shows a cline near the boundary. On stated assumptions the
  relation between selection intensity, mean distance migrated
  per generation, and the slope of the cline can be calculated.
  Applied to Peromyscus polionotus; intensities of about 0.1
  percent. Distinct from filled Endler 1977 (book: parapatric
  split despite gene flow; not the 1948 slope formula). Distinct
  from filled Barton 1979 (tension-zone dynamics, hybrid
  unfitness). Distinct from filled Wright 1943 IBD (similarity
  declines with distance; no selection-migration cline). Fisher
  1937 wave of advance was not opened for claim text; not the
  source.
One-sentence prediction: At a sharp habitat boundary, cline
  slope is set by selection versus migration distance; a steep
  cline implies stronger selection or less dispersal.
Assumptions: a sexual population at equilibrium across a
  linear habitat; migration is random, not nursery transport;
  a vineyard is not the boundary; clones are not demes; dual
  domestication is not one step-environment.
Which fail here: humans and nurseries move vines farther
  than Haldane migration. Dong 2023 dual domestication is two
  origins, not one habitat step. Syl-W gene flow is CAUTION
  that isolation is incomplete, not a fitted 1948 cline. A
  wine-region PCA is not a Haldane transect.
Modern data / statistic: whether wild-cultivar or wild-patch
  allele-frequency geography is a Haldane equilibrium cline
  (slope versus selection / migration) after clone + IBD
  filters, versus two domestication centres or an IBD slope
  with no environmental step.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Dual-domestication geography;
  Syl-W gene flow. Use as the two-origin / gene-flow contrast,
  not as a published Haldane-cline analysis. Do not invent a
  grape cline paper.
What would falsify it: grape geography is not a Haldane
  selection-migration cline after clone + IBD filters (two
  origins, or an IBD slope with no habitat step). Endler 1977
  remains the parapatric-despite-gene-flow book; Barton 1979
  remains the tension-zone original; Wright 1943 remains
  continuous IBD.
What we will not claim: that Endler 1977 is this paper
  (already filled). That Barton 1979 is this paper. That
  Fisher 1937 is the source (claim text not opened). That
  Dong 2023 fitted a Haldane cline. That a cultivar name is
  a habitat-boundary phenotype.
```

---

## Slatkin cline characteristic length

```
Theory: Slatkin cline (characteristic length of gene flow
  versus selection)
Original paper (year): Slatkin M. 1973. Gene flow and
  selection in a cline. Genetics 75(4):733-756
  (1 December 1973). DOI 10.1093/genetics/75.4.733
  PMID 4778791 PMCID PMC1213045. EuropePMC HTML opened
  (Slatkin M; 01 Dec 1973; Genetics 75(4):733-756; DOI;
  PMID; PMC; abstract). A continuously distributed infinite
  population with spatially varying selection: step change,
  environmental pocket, periodic environment, and a
  geographic barrier. (1) There is a characteristic length
  scale of gene-frequency variation; the population cannot
  respond to environmental change over a shorter distance.
  The result does not depend on the pattern of selection or
  the exact dispersal function. (2) Heterozygote unfitness
  steepens the cline. (3) A barrier shifts frequencies
  drastically only when almost all would-be migrants are
  stopped. Distinct from filled Haldane 1948 (this wave; the
  slope formula at a step, not the characteristic-length
  scale). Distinct from filled Endler 1977 and filled Barton
  1979. Distinct from filled Slatkin 1985 private alleles
  and filled Slatkin 1993 pairwise M.
One-sentence prediction: Local adaptation fails when the
  environmental grain is shorter than the characteristic
  length set by gene flow and selection; only coarser
  gradients can hold a cline.
Assumptions: a continuous sexual habitat, not clones or
  cultivars; dispersal is the paper's kernel, not human
  transport; a vineyard is not an environmental pocket;
  dual domestication is not one infinite population.
Which fail here: humans and rivers move vines farther than
  the characteristic length. Clone IBD fakes a cline. Dual
  domestication is two origins. A nursery block is not a
  Slatkin pocket.
Modern data / statistic: whether wild-patch allele
  frequencies track environmental change at a scale longer
  than Slatkin's characteristic length after clone + IBD
  filters, versus being swamped or two-centred.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset
  after clone + IBD filters. Use as geography, not as a
  published characteristic-length analysis. Do not invent
  a grape cline paper.
What would falsify it: wild-patch frequencies do not show
  a characteristic-length cline after clone filter (swamped
  by transport, or two domestication centres). Treating
  clone IBS as a cline is not the test. Haldane 1948 remains
  the slope-at-a-boundary original.
What we will not claim: that Haldane 1948 is this paper.
  That Slatkin 1985 or 1993 is this paper. That Endler 1977
  is this paper. That Dong 2023 estimated a characteristic
  length. That a wine region is an environmental pocket.
```

---

## Nagylaki cline existence

```
Theory: Nagylaki conditions for the existence of clines
Original paper (year): Nagylaki T. 1975. Conditions for
  the existence of clines. Genetics 80(3):595-615
  (1 July 1975). DOI 10.1093/genetics/80.3.595
  PMID 1232026 PMCID PMC1213362. EuropePMC HTML opened
  (Nagylaki T; 01 Jul 1975; Genetics 80(3):595-615; DOI;
  PMID; PMC; abstract). PMC HTML opened (Department of
  Medical Genetics and Mathematics Research Center,
  University of Wisconsin, Madison; received 16 October
  1974; same abstract). A diffusion equation for gene
  frequency in a continuous monoecious habitat reduces to
  the Fisher-Haldane cline model under isotropic
  homogeneous migration, uniform density, and local
  Hardy-Weinberg. If at least one allele is favoured only
  in a finite region, and migration is too strong or
  selection too weak, a cline cannot exist at all; unless
  there is overdominance the population must be
  monomorphic. A barely existing cline can still show large
  gene-frequency variation. Distinct from filled Haldane
  1948 (this wave; slope given that a cline exists).
  Distinct from filled Slatkin 1973 (this wave;
  characteristic length, not the existence threshold).
  Distinct from filled Endler 1977.
One-sentence prediction: Too much gene flow relative to
  selection erases a cline entirely (monomorphism), rather
  than merely flattening it, unless heterozygotes are
  overdominant.
Assumptions: one diallelic locus; no mutation or drift in
  the model; migration independent of genotype; samples are
  demes, not clones; dual domestication is not one habitat;
  a vineyard is not an environmental pocket.
Which fail here: human transport is stronger than the
  paper's migration. Dual domestication is two origins, not
  one pocket. Clone IBD fakes polymorphism. Overdominance
  was not locked as a grape original (already dropped).
Modern data / statistic: whether a wild environmental
  pocket holds a Nagylaki cline after clone + IBD filters,
  versus monomorphism / two domestication centres.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset
  after clone + IBD filters. Use as the existence contrast,
  not as a published Nagylaki analysis. Do not invent a
  grape cline paper.
What would falsify it: no cline exists after clone filter
  because migration / transport is too strong (the
  monomorphic reading), or because there are two origins
  rather than one pocket. Slope-given-a-cline is the
  Haldane 1948 job; characteristic length is the Slatkin
  1973 job.
What we will not claim: that Haldane 1948 is this paper.
  That Slatkin 1973 is this paper. That Dong 2023 tested
  Nagylaki existence. That a cultivar is an environmental
  pocket.
```

---

## Key tension zone

```
Theory: Key tension zone (secondary intergradation as a
  semipermeable membrane)
Original paper (year): Key KHL. 1968. The concept of
  stasipatric speciation. Systematic Zoology 17(1):14-22
  (1 March 1968; now hosted as Systematic Biology).
  DOI 10.1093/sysbio/17.1.14.
  Oxford Academic HTML opened
  (https://academic.oup.com/sysbio/article/17/1/14/1622370):
  K. H. L. Key, Division of Entomology, CSIRO, Canberra;
  1968/03/01; Systematic Biology / Zoology 17(1):14-22;
  DOI; abstract beginning: difficulties in stasipatric
  speciation; allopatric and parapatric components; races
  of morabine grasshoppers meet along very narrow zones of
  secondary intergradation, or "tension zones"; these act
  like semipermeable membranes, allowing free passage to
  some genetic modifications but holding back others. The
  tension zone moves as a front toward the less adapted
  form. Distinct from filled Barton 1979 (dynamics:
  dispersal versus selection against hybrids; 1968 names
  the zone). Distinct from filled Anderson 1949
  introgression and filled Dobzhansky 1940 reinforcement.
  Barton and Hewitt 1985 Annu Rev is a review; not the
  source.
One-sentence prediction: Secondary contact sits in a
  narrow tension zone that behaves as a semipermeable
  membrane: some alleles cross, others are held, and the
  front can move.
Assumptions: two sexual races meet after expansion from
  isolation; a cultivar x cultivar cross is not that
  contact; gene flow without a narrow front is not a
  tension zone; clones are not hybridizing demes.
Which fail here: nursery hybrids are not secondary
  contact. Dong 2023 Syl-W gene flow into CG3-CG6 is
  CAUTION that isolation is incomplete, not a mapped Key
  membrane. Treating sylvestris and vinifera as two
  biological species is the Mayr 1942 job. A vineyard is
  not a tension zone.
Modern data / statistic: whether wild-cultivar contact is
  a narrow semipermeable front after clone + IBD filters,
  versus diffuse gene flow / a single biological species.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Syl-W gene flow into
  CG3-CG6 is CAUTION, not a Key-zone demonstration. Do
  not invent a grape tension-zone paper.
What would falsify it: contact is not a narrow
  semipermeable front (gene flow after clone + IBD filters
  with no held-back class of alleles). Barton 1979 remains
  the dynamics original; Anderson 1949 remains
  introgression; Dobzhansky 1940 remains reinforcement.
What we will not claim: that Barton 1979 is this paper
  (already filled). That Barton and Hewitt 1985 is the
  source (review). That Dong 2023 mapped a tension zone.
  That a nursery hybrid is a tension zone.
```

---

## Barton multilocus clines

```
Theory: Barton multilocus clines (coupling coefficient)
Original paper (year): Barton NH. 1983. Multilocus clines.
  Evolution 37(3):454-471 (1 May 1983).
  DOI 10.1111/j.1558-5646.1983.tb05563.x PMID 28563316.
  EuropePMC HTML opened (Barton NH, Department of
  Genetics, University of Cambridge, Downing St.,
  Cambridge CB2 3EH; 01 May 1983; Evolution 37(3):454-471;
  DOI; PMID; no abstract there). ISTA research-explorer
  HTML opened (https://research-explorer.ista.ac.at/record/3668):
  Barton NH 1983; Evolution 37(3):454-471; DOI 10.2307/2408260;
  abstract. When two populations that differ at many loci
  meet, introgression depends on selection per locus s,
  recombination r, and the number of loci n. Behaviour
  scales with theta = s/r and with n. When selection is
  stronger than recombination (theta > 1), effective
  selection on each locus is comparable to total selection
  over the genome (s* ~ n s). When theta < 1, effective
  selection is weaker but still stronger than single-locus
  s. Even with weak selection, multilocus clines have a
  sharp central step flanked by independent tails; the
  barrier to gene flow is strongest when selection is
  spread over many loci. Distinct from filled Barton 1979
  (single-locus / hybrid-zone dynamics; this paper is
  multilocus coupling). Distinct from filled Key 1968
  (this wave; names the tension zone). Distinct from
  filled Haldane 1948 / Slatkin 1973 / Nagylaki 1975
  (single-locus clines). Barton and Hewitt 1985 remains
  a review.
One-sentence prediction: If many selected loci are
  coupled (theta = s/r large), the hybrid zone acts as
  one genome-wide barrier with a sharp central step; if
  recombination wins, loci introgress independently.
Assumptions: two sexual populations differ at many loci;
  a cultivar panel is not that meeting; clone IBD is not
  coupling LD; chips are not the selected map; dual
  domestication is not one hybrid zone.
Which fail here: nursery crosses are not secondary
  contact. Clone IBD fakes LD among loci. Dong 2023
  color / sex / flavor are few large-effect loci, not a
  many-locus barrier. Syl-W gene flow is CAUTION, not a
  Barton-1983 coupling estimate.
Modern data / statistic: whether wild-cultivar contact
  shows coupled multilocus clines (sharp central step;
  theta large) after clone + IBD filters, versus
  independent introgression of a few loci.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Syl-W gene flow;
  color / sex / flavor peaks. Use as the coupling
  contrast, not as a published multilocus-cline
  analysis. Do not invent a grape hybrid-zone paper.
What would falsify it: contact is not a coupled
  multilocus barrier after clone filter (few independent
  loci, or diffuse gene flow). Single-locus tension-zone
  dynamics remain the 1979 job. Haldane / Slatkin /
  Nagylaki remain single-locus cline jobs.
What we will not claim: that Barton 1979 is this paper
  (already filled). That Barton and Hewitt 1985 is the
  source. That Key 1968 is this paper. That Dong 2023
  estimated theta. That a SNP chip is a selected map.
```

---

## Kaplan coalescent hitchhiking

```
Theory: Kaplan-Hudson-Langley coalescent hitchhiking
Original paper (year): Kaplan NL, Hudson RR, Langley CH.
  1989. The "hitchhiking effect" revisited. Genetics
  123(4):887-899 (1 December 1989).
  DOI 10.1093/genetics/123.4.887 PMID 2612899
  PMCID PMC1203897. EuropePMC HTML opened (Kaplan NL,
  Statistics and Biomathematics Branch, National Institute
  of Environmental Health Sciences, Research Triangle Park,
  North Carolina 27709; Hudson RR; Langley CH; 01 Dec 1989;
  Genetics 123(4):887-899; DOI; PMID; PMC; abstract). Using
  the coalescent for a neutral sample linked to a selected
  substitution, a stochastic finite-population model gives
  the steady-state effect of hitchhiking on the number of
  selectively neutral polymorphic sites. In regions of low
  crossing over, strongly selected substitutions in the
  history of the sample can substantially reduce the number
  of polymorphic sites relative to a neutral model.
  Distinct from filled Maynard Smith and Haigh 1974
  (deterministic diversity collapse; no coalescent).
  Distinct from filled Charlesworth, Morgan and Charlesworth
  1993 BGS (deleterious mutations, not advantageous
  substitutions). Distinct from filled Fay and Wu 2000 H
  (derived high-frequency excess). Distinct from filled
  Gillespie 2000 draft. Stephan, Wiehe and Lenz 1992 was
  not opened for claim text; not the source.
One-sentence prediction: Recurrent hitchhiking in low
  recombination reduces the number of polymorphic sites
  in a sample below the neutral coalescent expectation.
Assumptions: a random sample of sequences from one
  population; the genealogy is not a clone pedigree;
  polymorphism is not clone-private SNPs; a cultivar
  panel is not that sample; chips are not forced-
  biallelic loci.
Which fail here: a cultivar panel is not a random sample.
  Clone IBD fakes a diversity trough. Pedigree repeats
  are not new mutations. Dual domestication is human
  choice, not a sweep generation. SNP chips are biallelic.
Modern data / statistic: number of segregating sites (or
  pi) at candidate domestication loci versus recombination
  on Dong-class WGS after clone + IBD filters, against the
  Kaplan low-recombination reduction. Fay-Wu and Tajima
  remain other jobs.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Color / sex / flavor
  peaks. Use as the hitchhiking contrast, not as a
  published Kaplan analysis. Do not invent a grape
  coalescent-hitchhiking paper.
What would falsify it: no reduction of polymorphic sites
  in low recombination after clone + IBD filters. Treating
  clone IBS as a trough is not the test. Deterministic
  diversity collapse is the 1974 hitchhiking job; BGS is
  the 1993 job; derived high-frequency excess is the
  Fay-Wu job.
What we will not claim: that Maynard Smith and Haigh 1974
  is this paper (already filled). That Charlesworth 1993
  BGS is this paper. That Fay and Wu 2000 is this paper.
  That Stephan 1992 is the source (not opened). That Dong
  2023 fitted a Kaplan coalescent.
```

---

## Braverman hitchhiking SFS

```
Theory: Braverman hitchhiking site-frequency spectrum
Original paper (year): Braverman JM, Hudson RR, Kaplan NL,
  Langley CH, Stephan W. 1995. The hitchhiking effect on
  the site frequency spectrum of DNA polymorphisms.
  Genetics 140(2):783-796 (1 June 1995).
  DOI 10.1093/genetics/140.2.783 PMID 7498754
  PMCID PMC1206652. EuropePMC HTML opened (Braverman JM,
  Center for Population Biology, University of California,
  Davis; Hudson RR; Kaplan NL; Langley CH; Stephan W;
  01 Jun 1995; Genetics 140(2):783-796; DOI; PMID; PMC;
  abstract). Simple hitchhiking (directional selection on
  rare advantageous mutants sweeping linked neutrals)
  predicts a skew toward rare variants. Coalescent
  simulations of recurrent hitchhiking show (1) expected
  Tajima D is large and negative, (2) Tajima's test has
  reasonable power for realistic parameters, and (3) some
  Drosophila datasets with reduced diversity but no SFS
  skew are very unlikely under simple hitchhiking; that
  model is then not a sufficient explanation. Distinct
  from filled Tajima 1989 (the D statistic as a neutrality
  test; this paper is the hitchhiking prediction for D).
  Distinct from filled Kaplan, Hudson and Langley 1989
  (this wave; reduction in the number of sites, not the
  SFS / D prediction). Distinct from filled Fay and Wu
  2000 H (derived high-frequency excess). Distinct from
  filled Maynard Smith and Haigh 1974.
One-sentence prediction: Simple recurrent hitchhiking
  leaves a large negative Tajima D (excess of rare
  variants) at linked sites; reduced diversity without
  that skew is not simple hitchhiking.
Assumptions: a random sample of sequences; rare variants
  are not clone-private SNPs; a cultivar panel is not
  that sample; chips are not forced-biallelic loci;
  demography is not a confounder that mimics D.
Which fail here: a cultivar panel is not a random sample.
  Clone IBD and clone-private SNPs fake rare variants.
  Dual domestication is not one equilibrium population.
  SNP chips are biallelic.
Modern data / statistic: Tajima D (and the SFS) at
  candidate domestication loci on Dong-class WGS after
  clone + IBD filters, versus the large-negative-D
  hitchhiking prediction. Kaplan site-count and Fay-Wu H
  remain other jobs.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Color / sex / flavor
  peaks. Use as the SFS contrast, not as a published
  Braverman analysis. Do not invent a grape hitchhiking-SFS
  paper.
What would falsify it: candidate loci do not show large
  negative D after clone + IBD filters (simple hitchhiking
  dies; BGS or demography remain other readings). Treating
  clone-private SNPs as rare sweep variants is not the
  test. One-sample Tajima as a generic test is the 1989
  job; site-count reduction is the Kaplan job.
What we will not claim: that Tajima 1989 is this paper
  (already filled). That Kaplan 1989 is this paper. That
  Fay and Wu 2000 is this paper. That Dong 2023 computed
  a Braverman SFS. That a nursery sport is a rare variant
  from a sweep.
```

---

## Berg-Coop polygenic adaptation

```
Theory: Berg-Coop polygenic adaptation (coordinated
  allele-frequency shifts)
Original paper (year): Berg JJ, Coop G. 2014. A population
  genetic signal of polygenic adaptation. PLoS Genetics
  10(8):e1004412 (7 August 2014).
  DOI 10.1371/journal.pgen.1004412 PMID 25102153
  PMCID PMC4125079. PLoS HTML opened
  (https://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1004412):
  Berg JJ, Coop G; published 7 August 2014; received
  3 August 2013; accepted 17 April 2014; PLoS Genet
  10(8):e1004412; DOI; abstract and author summary.
  EuropePMC HTML opened (Berg JJ, UC Davis Population
  Biology / Center for Population Biology / Evolution and
  Ecology; Coop G, same; 07 Aug 2014; PMID; PMC; same
  abstract). Adaptation on a polygenic phenotype may occur
  via subtle allele-frequency shifts at many loci, too
  diffuse for single-locus sweep scans. GWAS effect sizes
  give mean additive genetic values as weighted sums of
  allele frequencies; tests look for environmental
  correlation of those values and for overdispersion
  relative to a drift-and-relatedness null, i.e. positive
  covariance among like-effect alleles. Distinct from
  filled Hermisson and Pennings 2005 soft sweep (standing
  variant at one locus). Distinct from filled Maynard
  Smith and Haigh 1974 hard hitchhiking. Distinct from
  filled Fisher 1918 infinitesimal (the trait model, not
  the population-genetic signal). Pritchard, Pickrell and
  Coop 2010 Curr Biol 20:R208-R215 is a review; red line;
  not the source.
One-sentence prediction: Local adaptation of a polygenic
  trait shows up as coordinated frequency shifts of many
  small-effect alleles in the same direction, not as a
  single-locus sweep.
Assumptions: GWAS loci are causal-enough tags, not clone
  IBS; genetic values are not cultivar means; a vineyard
  is not a Berg-Coop population; color / sex / flavor are
  not assumed to be highly polygenic; chips are not the
  whole architecture.
Which fail here: Dong 2023 color / sex / flavor peaks are
  few large-effect loci, not a polygenic coordinated
  shift. Clone IBD fakes genetic values. Dual
  domestication is human choice, not many-population
  local adaptation of one trait. A wine-region mean is
  not a genetic value.
Modern data / statistic: whether domestication traits
  show Berg-Coop overdispersion / environmental
  correlation of genetic values after clone + IBD
  filters, versus a few large-effect QTNs or a hard /
  soft sweep at one locus.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Color / sex / flavor
  peaks as the large-effect contrast. Use as a polygenic
  versus oligogenic test, not as a published grape
  polygenic-adaptation paper. Do not invent a grape GWAS
  local-adaptation paper.
What would falsify it: trait differentiation is not a
  coordinated many-locus shift after clone filter (few
  large-effect peaks, or a single-locus sweep). Soft
  sweep remains the Hermisson 2005 job; infinitesimal
  inheritance remains the Fisher 1918 job; hitchhiking
  diversity collapse remains 1974.
What we will not claim: that Pritchard, Pickrell and
  Coop 2010 is the source (review). That Hermisson 2005
  is this paper. That Fisher 1918 is this paper. That
  Dong 2023 ran a Berg-Coop test. That a cultivar mean
  is a genetic value.
```

---

## Rockman QTN versus polygenes

```
Theory: Rockman QTN program versus undetectable polygenes
Original paper (year): Rockman MV. 2012. The QTN program
  and the alleles that matter for evolution: all that's
  gold does not glitter. Evolution 66(1):1-17
  (print 2012; EuropePMC date 6 November 2011).
  DOI 10.1111/j.1558-5646.2011.01486.x PMID 22220860
  PMCID PMC3386609. EuropePMC HTML opened (Rockman MV,
  Department of Biology and Center for Genomics and
  Systems Biology, New York University, 12 Waverly Place,
  New York, NY 10003; Evolution 66(1):1-17; DOI; PMID;
  PMC; abstract). Large-effect quantitative trait
  nucleotides accessible to experimentalists may be
  unrepresentative of the alleles that matter. Neither
  theory nor data justify treating discoverable
  large-effect alleles as the primary molecular substrate
  of evolution; evolution often acts via large numbers of
  small-effect polygenes, individually undetectable, and
  those variants differ in kind at the molecular level
  from large-effect QTNs. Distinct from filled Fisher 1918
  infinitesimal (the additive many-locus model; 2012 is
  the argument that mapped QTNs mislead). Distinct from
  filled Fisher 1930 geometric (large mutations almost
  never help). Distinct from filled Orr 1998 exponential
  factors. Distinct from filled Berg and Coop 2014 (this
  wave; the population-genetic signal of polygenic
  adaptation). Boyle, Li and Pritchard 2017 omnigenic was
  tagged Review; not used.
One-sentence prediction: The large-effect QTNs one can
  map are not a random sample of the alleles that matter;
  typical evolution is many undetectable small-effect
  polygenes.
Assumptions: the mapped QTN set is being read as the
  architecture of evolution, not as a few domestication
  exceptions; clones are not a sexual mapping population;
  color / sex / flavor may be exactly the unrepresentative
  large-effect class the paper warns about.
Which fail here: Dong 2023 color / sex / flavor are few
  large-effect domestication QTNs (the glittering class).
  That is a legitimate QTN finding and a caution against
  reading those loci as typical wild evolution. Grafted
  clones are not a QTN mapping pedigree. Standing clone
  heterozygosity is not polygenic standing variation.
Modern data / statistic: whether wild trait architecture
  after clone + IBD filters is Rockman undetectable
  polygenes, versus a few large-effect domestication QTNs
  (Dong color / sex / flavor) or a Berg-Coop coordinated
  shift.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Color / sex / flavor
  peaks as the large-effect QTN contrast. Use as the
  architecture caution, not as a published grape QTN
  paper. Do not invent a grape QTN-catalog paper.
What would falsify it: wild architecture is not
  undetectable polygenes after clone filter (few
  large-effect QTNs explain the traits). Infinitesimal
  math remains the Fisher 1918 job; polygenic adaptation
  as a frequency-shift test remains the Berg-Coop job.
What we will not claim: that Fisher 1918 is this paper
  (already filled). That Berg and Coop 2014 is this paper.
  That Boyle 2017 is the source (review). That Dong 2023
  mapped a representative QTN catalog. That a nursery
  sport is a typical evolutionary allele.
```

---
