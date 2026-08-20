---
name: genomics-theory-mining
description: >
  Dig up a classic genomics or population-genetic theory and test it
  against modern data. Use when the user wants old-theory mining,
  forgotten models, Muller ratchet, background selection, Meselson,
  BDM, DDC, Baker, isolation by distance, gene balance, nearly-neutral,
  hitchhiking, Hill-Robertson, Ohno WGD, Kingman coalescent,
  infinite-alleles, molecular clock, McDonald-Kreitman, Tajima D,
  genetic draft, introgression, Haldane, stepping-stone,
  island model, clonal interference, allele surfing, genome shock,
  allopolyploidy, drift-barrier, gBGC, soft sweep, chimera,
  reinforcement, two-fold cost of sex, Haldane cost, inbreeding depression, infinitesimal, genetic assimilation,
  C-value, concerted evolution, birth-and-death, metapopulation,
  breakage-fusion-bridge, fractionation, Ewens, shifting balance, Fisher geometric, mutation-selection balance,
  molecular drive, Holliday conversion, quasispecies, serial founder,
  Lande response, endosymbiosis, Vavilov, Price equation, Hamilton, Nei distance, Weir-Cockerham FST,
  Orr adaptation, Y degeneration, Mayr BSC, HKA, Lewontin-Krakauer, Fay-Wu, Fu-Li, Slatkin gene flow, tension zone,
  Endler clines, Crow load, Haldane cline, Slatkin 1973, Nagylaki, Key tension zone, Barton coupling,
  Kaplan hitchhiking, Braverman SFS, Berg-Coop, Rockman QTN, Rousset IBD, Excoffier AMOVA, Wade-McCauley, Whitlock FST, Slatkin two-locus cline,
  Barton-Bengtsson barrier, Barton hybrid-sink, Kimura 1955 drift, Nei GST, Slatkin 1981, Slatkin-Maruyama, Nei 1978, Kimura K80,
  Tajima-Nei distance, Begun-Aquadro, Ohta 1972, Barton-de Cara, Rieseberg 2003, Nei-Li pi, Tajima 1983, Kimura-Ohta 1969, Charlesworth 1994 BGS, Hudson-Kaplan 1995,
  Nordborg 1996, Wiehe-Stephan, Orr snowball, Turelli-Orr, Coyne-Orr 1989, or a revival paper that
  is not a methods benchmark.
---

# genomics-theory-mining

The paper is the old math plus a new test, not a review with extra adjectives.
Find the original, list the assumptions, then say which modern data can break them.
Filled notes live in `theories.md` (thirty-eight notes: eight first wave, nine second wave, nine third wave, twelve fourth wave). One theory per job.

## When to use

- A user names a "forgotten" or "classic" theory and asks if it still holds.
- A grapevine / clonal / polyploid fact looks like an old model with the wrong organism.
- Someone wants a revival paper, not another tool comparison.

Do not use this for a methods bake-off, a database build, or a literature dump.

## Order

1. **Name the theory in one sentence** (what it predicts, not who is famous).
2. **Read the original paper**, not the 2010s review that cites it. Quote the claim and the year.
3. **Write the assumption list.** Sexual panmixia? Infinite sites? Diploid? Stable Ne? No structure? No clones?
4. **Mark which assumptions fail in the study system** (Vitis: clones, vegetative propagation, high TE, mixed ploidy, capture / aDNA missingness).
5. **Pick the modern test.** One dataset, one statistic, one falsifier. If you cannot name the falsifier, you do not have a paper.
6. **Cite the original math.** Do not rename the theory. Do not invent a "generalized X".

## Worked example 1 (lead): Muller's ratchet in clonal / somatic lineages

```
Theory: Muller's ratchet
Original paper (year): Muller HJ. 1964. The relation of recombination to
  mutational advance. Mutat Res 1:2-9. DOI 10.1016/0027-5107(64)90047-8
  PMID 14195748. (PubMed sometimes prints volume 106; venue is vol. 1.)
Named and simulated: Felsenstein J. 1974. The evolutionary advantage of
  recombination. Genetics 78(2):737-756. DOI 10.1093/genetics/78.2.737
  PMID 4448362 PMC1213231. Finite N is required; infinite populations
  show no ratchet.
One-sentence prediction: Without recombination, the class of genomes
  carrying the fewest deleterious mutations is eventually lost by drift
  and cannot be restored, so load ratchets upward.
Assumptions: finite N; mostly deleterious mutations; no (or rare)
  back-mutation / compensatory recombination; asexual or non-recombining
  transmission of the whole haplotype.
Which fail here: grape cultivars are grafted clonal lineages, not
  panmictic sexuals. Meristems, chimeras, and diplontic selection can
  hide or purge load. Somatic clock != germline clock. Structural
  mutations and TEs are part of the load, not just SNPs.
Modern data / statistic: clone-private coding variants and their
  predicted deleteriousness among vegetatively propagated cultivars.
Lead test bed (not a proof): Vondras AM et al. 2019. The genomic
  diversification of grapevine clones. BMC Genomics 20:972.
  DOI 10.1186/s12864-019-6211-2 PMC6907202. Fifteen Zinfandel clones;
  heterozygous mutations richest in repetitive intergenic / methylated
  cytosine; clones accumulate putatively deleterious exonic variants.
Second test (structural, not SNP-only): Carbonell-Bejerano P et al.
  2017. Catastrophic unbalanced genome rearrangements cause somatic
  loss of berry color in grapevine. Plant Physiol 175:786-801.
  DOI 10.1104/pp.17.00715 PMC5619900. Tempranillo Blanco vs Tinto;
  hemizygous deletion of 313 genes including the color locus;
  chromothripsis-like. A SNP-only ratchet test is incomplete.
Plant asexual comparator: Lovell JT et al. 2017. Mutation accumulation
  in an asexual relative of Arabidopsis. PLoS Genet 13(1):e1006550.
  DOI 10.1371/journal.pgen.1006550. Apomictic Boechera retain more
  mutations at conserved sites than sympatric sexuals.
What would falsify it: clone-private coding mutations are NOT enriched
  for deleterious classes, OR the least-loaded haplotype class is
  continually restored (back-mutation, gene conversion, or diplontic
  replacement). Vondras is a test bed, not a demonstration that the
  ratchet has clicked to extinction.
What we will not claim: that grape clones are doomed; that Pol epsilon
  proofreading defects cause the grape ratchet (see hunch below); that
  a cultivar panel is Ne.
```

**TESTABLE HUNCH, not a result:** if leading-strand DNA polymerase epsilon
proofreading is leaky in shoot meristems, the somatic SNV rate rises and a
ratchet-style load should click faster. No published grape Pol-e x clone
result was verified for this skill. Do not write the hunch as a finding.

Sister clone clocks (lineage, not ratchet proof): Roach MJ et al. 2018.
PLoS Genet 14(11):e1007807 (15 Chardonnay clones; 1620 high-confidence
markers). Carrier G et al. 2012. PLoS ONE 7(3):e32973 (Pinot noir; TE
insertions dominate scored polymorphism). Callipo P et al. 2026. Genome
Biol DOI 10.1186/s13059-026-04184-x (23 Pinot noir clones; SNPs/SVs
depleted from coding sequence; CG/CHG methylation reconstructs clone
trees). Zhou Y et al. 2019. Nat Plants 5:965-979 (SVs accrue as recessive
heterozygotes in clonal lineages).

## Dossier (filled; one modern falsifier each)

| Theory | Original (verified) | Prediction | Dies in plants / clones | One modern falsifier |
|--------|---------------------|------------|-------------------------|----------------------|
| Muller ratchet | Muller 1964 Mutat Res 1:2-9; Felsenstein 1974 Genetics 78:737-756 | Least-loaded class is lost and not restored | Sexual recombination; somatic != germline | Vondras 2019 clone-private coding load not deleterious-enriched, or least-loaded class restored |
| Nearly-neutral | Ohta 1973 Nature 246:96-98 | Slightly deleterious fix when \|Nes\| < 1; faster in small Ne | A cultivar collection is not one Ne | Dong 2023 3525-accession WGS: load / dN/dS does not scale with wild vs cultivar Ne |
| Hitchhiking | Maynard Smith and Haigh 1974 Genet Res 23:23-35 | Linked diversity collapses around a sweep | Clonal IBD and pedigree fake a sweep | Dong 2023 color / sex / flavor peaks vanish after clone + IBD filters (caution dataset, not a proof) |
| Hill-Robertson | Hill and Robertson 1966 Genet Res 8:269-294 | Linked selected loci interfere; recombination helps | Chip skeleton is not a recombination map | Selection efficacy not weaker in low-recombination bins on a real Vitis map |
| Gene balance / dosage | Ohno 1970 book; Birchler and Veitia 2007 Plant Cell 19:395-402 | Stoichiometric regulators are dosage-sensitive; WGD retains them | Tandem NLRs are not the same dosage as WGD | Jaillon 2007 palaeo-hexaploid ohnologs: TF / signaling genes not preferentially retained vs tandem NLRs |
| Neutral theory (null) | Kimura 1968 Nature 217:624-626 | Most substitutions are drift of neutrals | Treating "neutral" as a conclusion | Clone-private coding SNPs are systematically adaptive, not a drift null |
| Infinite-sites | Kimura 1969 Genetics 61:893-903; Watterson 1975 Theor Popul Biol 7:256-276 | Each mutation hits a new site; theta from S | Recurrent TE and gene conversion | Carrier 2012 / Vondras 2019: recurrent TE or same-site hits make pi != theta_W |
| McClintock TE | McClintock 1950 PNAS 36:344-355 | Mobile loci generate new mutable alleles | Scoring only SNPs | Method-fair genome-wide census: TE insertions negligible vs SNPs (Carrier 2012 scored the opposite in Pinot) |
| Background selection | Charlesworth, Morgan and Charlesworth 1993 Genetics 134:1289-1303 | Linked neutral diversity falls where deleterious mutation is purged | Chip skeleton is not a recombination map | Diversity not reduced in low-recombination bins on a real Vitis map after gene-density control |
| Meselson effect | Mark Welch and Meselson 2000 Science 288:1211-1215 (test, not a 1960s original) | Alleles diverge without sex | Grape clones are heterozygous diploids with rare sex; Roach 2018 inbreeding cuts the other way | Haplotype divergence in old clones is not higher than sexual wilds after standing heterozygosity |
| Organelle ratchet | Muller 1964 applied to organelles; Lynch 1996 Mol Biol Evol 13:209-220 (animal mt tRNA) | Non-recombining plastid / mt load ratchets | No locked grape plastid popgen paper | Plastid assemblies / haplotypes: organelle coding not excess-deleterious vs nuclear after mu correction |
| BDM incompatibilities | Dobzhansky 1937 Genetics and the Origin of Species (book) | Hybrid inviability is two-locus (or more) | Cultivar x cultivar is not a species cross | Hybrid inviability in vinifera x riparia / rupestris / amurensis maps to a single locus |
| DDC / subfunctionalization | Force et al. 1999 Genetics 151:1531-1545 | Ohnologs partition ancestral subfunctions | Retention is not partitioned expression | Jaillon 2007 ohnolog pairs do not show partitioned expression / function vs random retention |
| Selfish DNA | Doolittle and Sapienza 1980 Nature 284:601-603; Orgel and Crick 1980 Nature 284:604-607 | TEs persist by self-replication | Some copies are domesticated | TE insertions systematically adaptive / domesticated, not mostly insertion-class load (Carrier 2012 / Vondras 2019) |
| Baker's law | Baker 1955 Evolution 9:347-349 | Self-compatible colonists establish after long-distance dispersal | A vineyard is not an island; some sylvestris already carry H haplotypes | Wild sylvestris hermaphrodite at the same rate as cultivars, or sex-locus sweep vanishes after IBD filter |
| Isolation by distance | Wright 1943 Genetics 28:114-138 | Similarity declines with geographic distance | Rivers and humans move vines | IBD slope is zero in wild sylvestris after river / human transport |
| Diplontic selection | Klekowski 1988 Mutation, Developmental Selection, and Plant Evolution (book) | Meristem cell-lineage competition purges somatic load | Recessives and chimeras evade the filter | Clone-private coding mutations not depleted vs intergenic after mutational-opportunity correction |
| Coalescent | Kingman 1982 Stoch Proc Appl 13:235-248 | Sample genealogies are binary n-coalescent trees | Clones and pedigrees are not a random haploid sample | Clone / pedigree samples still look Kingman after relatedness is scored |
| Infinite-alleles | Kimura and Crow 1964 Genetics 49:725-738 | Each mutation is a new allele; IBS is IBD | Chips are biallelic and recurrent; clones fake IBS | IBS on Vitis chips / WGS behaves as infinite-alleles after clone filter |
| Molecular clock | Zuckerkandl and Pauling 1962 Horizons ch. p.189; 1965 Evolving Genes and Proteins 97-166 | Divergence accumulates linearly on a germline clock | Somatic clone clock != sexual clock | Clone clock equals wild sylvestris / germline clock on matched sites (Vondras / Roach vs Dong wilds) |
| McDonald-Kreitman | McDonald and Kreitman 1991 Nature 351:652-654 | Dn/Ds equals Pn/Ps under neutrality | Clone-private SNPs are not substitutions | After clone filter, grape MK does not reject neutrality at domestication loci |
| Tajima D | Tajima 1989 Genetics 123:585-595 | pi equals theta_W under neutrality | Cultivar relatedness fakes negative D | Strongly negative D in cultivar panels vanishes after clone + IBD filter |
| Mutation accumulation | Mukai 1964 Genetics 50:1-19; Lovell 2017 plant comparator | Sheltered genomes accumulate deleterious load | Diplontic selection and chimeras are not a Mukai cage | Clone-private load not deleterious-enriched after diplontic / chimera correction |
| Genetic draft | Gillespie 2000 Genetics 155:909-919 | Recurrent sweeps add drift-like noise at linked sites | Chip skeleton is not a map; clone IBD fakes draft | Linked diversity explained by recombination / BGS, not recurrent sweeps |
| Introgression / hybrid swarm | Anderson 1949 Introgressive Hybridization (book) | Backcross tracts are geographically clinal | Cultivar relatedness fakes tracts | Putative tracts vanish after IBD / clone filters or are not clinal (Dong 2023 Syl-W into CG3-CG6 is CAUTION) |
| Haldane's rule | Haldane 1922 J Genet 12:101-109 | The rare / sterile hybrid sex is the heterogametic sex | Grape is not XX/XY; sex is an SDR | Does not map onto Vitis SDR; do not invent a heterogametic sterility test |
| Stepping-stone | Kimura and Weiss 1964 Genetics 49:561-576 | Correlation declines with steps, not Euclidean distance | Cultivar PCA; human / river jumps | Dong 2023 wilds: neighbor-corridor correlation not higher than Euclidean |
| Island model | Wright 1931 Genetics 16:97-159 (1943 named it) | FST = f(Nem); no distance decay | Vineyard is not an island | Dong 2023 wilds: FST not independent of distance |
| Clonal interference | Gerrish and Lenski 1998 Genetica 102:127-144 | Competing asexual beneficials exclude the weaker | Nursery cuttings are not a chemostat | Vondras 2019 / Roach 2018 / Carrier 2012: clone-private sports not mutually exclusive |
| Allele surfing | Edmonds, Lillie and Cavalli-Sforza 2004 PNAS 101:975-979 | Front mutations reach high frequency by founder repeats | Dual domestication; human transport | Dong 2023: edge alleles not in excess of core after clone + IBD filters |
| Genome shock | McClintock 1984 Science 226:792-801 | Unprepared challenge restructures the genome | Constitutive somatic TE clock is not a shock | Carrier 2012 / Vondras 2019: TE / SV not clustered on shock nodes vs per-year clock |
| Allopolyploidy / secondary polyploidy | Stebbins 1947 Adv Genet 1:403-429 | Allo / segmental allo / palaeo-polyploid types leave distinct pairing and retention | Vitis is palaeo-hexaploid, not recent allo | Jaillon 2007: three ancestral genomes, not a recent allo pair; Zhou 2019 SVs change dose without WGD |
| Drift-barrier | Lynch 2011 Genome Biol Evol 3:1107-1118 | Per-site mu falls until antimutators are lost to drift | Cultivar panel is not Ne; somatic != germline mu | Dong 2023: cultivar mu (not load) not higher than wild after clone filter; no locked grape mu paper |
| GC-biased gene conversion | Galtier, Piganeau, Mouchiroud and Duret 2001 Genetics 159:907-911 | GC and W-to-S rise where recombination is high | No meiosis in cuttings; chip is not a map | Dong 2023 on a real Vitis map: GC / W-to-S not higher in high-r bins after CpG control |
| Soft sweep | Hermisson and Pennings 2005 Genetics 169:2335-2352 | Standing / recurrent copies leave multiple haplotypes and a shallow dip | Pedigree IBD fakes a hard sweep | Dong 2023 color / sex / flavor: single star phylogeny kills soft; H1/H2 standing sex haplotypes are the standing-variation test |
| Chimera / tunica-corpus | Satina, Blakeslee and Avery 1940 Am J Bot 27:895-905 | Layered meristem; periclinal chimera is stable and separable | Vitis is L1/L2, not three Datura layers | Franks 2002 Pinot Meunier L1/L2 split; Vondras / Roach / Carrier as genome-wide layer-census companions |
| Reinforcement | Dobzhansky 1940 Am Nat 74:312-321 (paper; 1937 book is BDM) | Premating isolation completes in sympatry where hybrids are unfit | Nursery hybrid is not secondary contact | Premating isolation not stronger in sympatry, or inviability is one-locus (Dong 2023 Syl-W gene flow is CAUTION) |
| Two-fold cost of sex | Maynard Smith 1978 The Evolution of Sex (book) | Asexual females replace sexuals via daughters | Grafted cuttings are not asexual females | Does not map onto grafted clones; do not invent a cost-of-males test |
| Haldane cost of selection | Haldane 1957 J Genet 55:511-524 | Allelic substitution costs ~10-30 generation-equivalents of selective death | Grafted clones are not a substituting sexual population | Does not map onto grafted clones; do not invent a grape cost-of-selection paper |
| Inbreeding depression | Darwin 1876 Cross and Self Fertilisation (book) | Selfed / inbred progeny are less vigorous than crossed progeny | Standing clone heterozygosity is not a self-vs-cross test | Roach 2018 ancestral inbreeding is CAUTION; selfed seedlings not less fit after clone filter |
| Infinitesimal / polygenic | Fisher 1918 Trans R Soc Edinb 52:399-433 (volume imprint 1919) | A metric trait is many Mendelian loci of small effect | Color / sex / flavor are large-effect loci; clones are not a sexual pedigree | Dong 2023 color / sex / flavor peaks are few large-effect loci, not an infinitesimal trait |
| Genetic assimilation | Waddington 1953 Evolution 7:118-126 | An induced phenotype becomes constitutive after selection | Cuttings skip the multi-generation sexual selection | Does not map onto grafted clones; do not invent a grape heat-shock assimilation paper |
| C-value / junk DNA | Ohno 1972 Brookhaven Symp Biol 23:366-370 | Most DNA is failed-duplication debris, not gene number | Scoring only genes hides repeats / TE | Jaillon 2007 genome size explained by gene number, not junk / TE (Carrier 2012 TE class) |
| Concerted evolution | Zimmer et al. 1980 PNAS 77:2158-2162 | Family members are more alike within species than to orthologs | Tandem NLRs are not rDNA; clones fake identity | Tandem copies more like other-Vitis orthologs than paralogs (birth-and-death alternative) |
| Birth-and-death gene family | Nei, Gu and Sitnikova 1997 PNAS 94:7799-7806 | Duplicates persist or die; members need not homogenize | Tandem NLRs are not MHC; palaeo-ohnologs are not tandem | Tandem NLR / disease-gene copies form one homogenized clade, not births plus pseudogenes |
| Metapopulation | Levins 1969 Bull Entomol Soc Am 15:237-240 | Occupancy is a colonization-extinction balance across patches | A vineyard is not a patch; cultivars are not demes | Dong 2023 wild patches: occupancy not a colonization-extinction balance after clone filter |
| Breakage-fusion-bridge | McClintock 1941 Genetics 26:234-282 | Broken ends fuse, bridge, and re-break; rearrangements cycle | SNP-only census hides BFB; distinct from 1950 TE and 1984 shock | Carbonell-Bejerano 2017 rearrangements not BFB-class; clone SVs are SNP-like (Zhou 2019) |
| Fractionation / diploidization | Thomas, Pedersen and Freeling 2006 Genome Res 16:934-946 | After WGD, one homeolog loses genes preferentially; connected genes stay | Vitis is palaeo-hexaploid, not recent tetraploid; SVs change dose without WGD | Jaillon 2007: no biased homeolog loss; TF / signaling not the retained class vs tandem NLRs |
| Ewens sampling formula | Ewens 1972 Theor Popul Biol 3:87-112 | Neutral allele-count configurations follow the sampling formula | Clones fake allele identity; chips are biallelic | Dong 2023 wilds: configuration not Ewens after clone + IBD filters |
| Shifting balance | Wright 1932 Proc 6th Int Congr Genet 1:356-366 | Subdivided races find higher peaks by drift then intergroup export | A vineyard is not a Wright race; cuttings skip the trial | Dong 2023 wild patches: no local nonadaptive peak-shift then export after clone filter |
| Fisher's geometric model | Fisher 1930 Genetical Theory ch. II pp. 38-41 | Large random mutations almost never improve; small ones might | Color / sex / flavor are large-effect; clones are not a walk | Dong 2023 color / sex / flavor peaks are few large-effect loci, not a small-step walk |
| Mutation-selection balance | Haldane 1927 Math Proc Camb Phil Soc 23:838-844 | A deleterious allele sits at a mutation-selection equilibrium | Grafted clones are not a sexual equilibrium; clone-private SNPs are not q | Wild coding load not at mutation-selection equilibrium after clone filter |
| Molecular drive | Dover 1982 Nature 299:111-117 | Genomic turnover cohesively replaces a family in genome and population | Tandem NLRs are not rDNA; clones fake cohesion | Tandem copies not cohesively replacing in the population (Zimmer or birth-and-death instead) |
| Gene conversion | Holliday 1964 Genet Res 5:282-304 | Hybrid-DNA mismatch repair converts one allele to the other | Cuttings skip meiosis; distinct from gBGC | No conversion tracts after clone filter; W-to-S bias is the gBGC job |
| Quasispecies | Eigen 1971 Naturwissenschaften 58:465-523 | A mutant cloud is maintained around a master sequence | RNA virus / prebiotic kinetics, not a grafted clone | Does not map onto grafted clones; do not invent a grape quasispecies paper |
| Serial founder | Ramachandran et al. 2005 PNAS 102:15942-15947 | Heterozygosity falls with distance from a single origin | Dual domestication; human transport | Dong 2023: diversity not a single-origin decline after clone + IBD filters |
| Multivariate response / breeder's equation | Lande 1979 Evolution 33:402-416 | Mean change is G beta (covariance times selection gradient) | Clones are not a sexual pedigree; few large-effect loci | Dong 2023 color / sex / flavor: not a G-matrix response (few large-effect loci) |
| Endosymbiosis / organelle origin | Sagan 1967 J Theor Biol 14:225-274 | Mitochondria and plastids were free-living prokaryotes | Eukaryogenesis is not a grape-clone experiment | Does not map onto grafted clones; do not invent a grape organelle-origin paper |
| Vavilov centers of origin | Vavilov 1932 Proc 6th Int Congr Genet 1:331-342 | Cultivated plants originate in a few geographically small diversity centres | Dual domestication; a vineyard is not a centre | Dong 2023: grape diversity not a single Vavilov-centre decline after clone + IBD filters |
| Price equation | Price 1970 Nature 227:520-521 | Mean change equals covariance of a character with relative fitness (plus transmission) | Cuttings are not a sexual generation; few large-effect loci | Dong 2023 color / sex / flavor: not a Price covariance partition (few large-effect loci) |
| Kin selection / inclusive fitness | Hamilton 1964 J Theor Biol 7:1-16 | Altruism spreads when inclusive fitness rises (relatedness times benefit) | Grafted clones are not social interactors | Does not map onto grafted clones; do not invent a grape kin-selection paper |
| Nei genetic distance | Nei 1972 Am Nat 106:283-292 | Distance from gene identity accumulates with divergence under isolation | Clones fake identity; dual domestication is not one split | Dong 2023 wilds: D not a single-split clock after clone + IBD filters |
| Weir-Cockerham FST | Weir and Cockerham 1984 Evolution 38:1358-1370 | FST is a moment estimator from allele-frequency variance, not Wright's island formula as data | A vineyard is not a deme; clones fake FST | Dong 2023 wilds: WC FST not independent of distance after clone filter (island dies) |
| Orr exponential factors | Orr 1998 Evolution 52:935-949 | Factors fixed on a walk to an optimum are approximately exponential in size | Color / sex / flavor are few large-effect; clones are not a walk | Dong 2023 color / sex / flavor peaks are a few large-effect loci, not an exponential walk |
| Y-chromosome degeneration | Charlesworth 1978 PNAS 75:5618-5622 | A non-recombining Y ratchets load and becomes inert; X dosage rises | Vitis SDR is young, not an XX/XY Y | Dong 2023 chr-2 SDR: little Y-like degeneration / recombination still present after clone filter |
| Biological species concept | Mayr 1942 Systematics and the Origin of Species (book) | Species are interbreeding populations isolated from other such groups | Cultivar x cultivar is not a species test; gene flow is caution | Dong 2023 Syl-W gene flow: sylvestris and vinifera are not isolated biological species |
| HKA test | Hudson, Kreitman and Aguade 1987 Genetics 116:153-159 | High-divergence regions are high-polymorphism regions under neutrality | Clone IBD fakes polymorphism; chips are not loci | After clone + IBD filters, polymorphism does not scale with divergence (MK / Tajima remain other jobs) |
| Lewontin-Krakauer FST outliers | Lewontin and Krakauer 1973 Genetics 74:175-195 | Heterogeneity of F among loci is evidence of selection | Clones fake F; chips are not loci | Dong 2023 wilds: F not heterogeneous among loci after clone + IBD filters |
| Fay-Wu H | Fay and Wu 2000 Genetics 155:1405-1413 | Hitchhiking leaves an excess of derived high-frequency variants | Clone IBD fakes high-frequency derived alleles | Dong 2023 color / sex / flavor: no derived high-frequency excess after clone + IBD filters |
| Fu-Li tests | Fu and Li 1993 Genetics 133:693-709 | External mutations deviate from theta under selection; internal less so | Clone-private SNPs are not external mutations | After clone + IBD filters, external vs internal counts do not reject neutrality (Tajima remains another job) |
| Slatkin private-allele gene flow | Slatkin 1985 Evolution 39:53-65 | Log of private-allele frequency estimates log Nm | Cultivar private alleles are not migrants; clones fake private alleles | Dong 2023 wilds: private-allele Nm not a migration estimate after clone filter |
| Slatkin IBD from pairwise M | Slatkin 1993 Evolution 47:264-279 | Pairwise M = (1/FST-1)/4 declines with distance under restricted dispersal | A vineyard is not a pair of demes; clones fake FST | Dong 2023 wilds: M not a distance function after clone filter (Wright 1943 remains the continuous-space job) |
| Hybrid-zone dynamics | Barton 1979 Heredity 43:341-359 | A tension zone sits where dispersal balances selection against hybrids | Nursery hybrid is not a tension zone | Dong 2023 Syl-W gene flow is CAUTION, not a trapped cline (Anderson / reinforcement remain other jobs) |
| Geographic variation / clines | Endler 1977 Geographic Variation, Speciation and Clines (book) | Steep clines and parapatric split can form despite continuous gene flow | Dual domestication; human transport | Dong 2023: no Endler cline / parapatric split after clone + IBD filters |
| Mutational / genetic load | Crow 1958 Hum Biol 30:1-13 | Standing fitness is lowered by recurrent mutation (and by segregation / incompatibility) | Grafted clones are not a sexual load equilibrium | Wild coding load not a Crow mutational-load partition after clone filter |
| Haldane cline | Haldane 1948 J Genet 48:277-284 | Cline slope at a habitat boundary is a function of selection intensity and migration distance | A vineyard is not a habitat boundary; clones fake allele frequency | Dong 2023: no Haldane equilibrium cline after clone + IBD filters |
| Slatkin cline characteristic length | Slatkin 1973 Genetics 75:733-756 | A population cannot adapt to environmental change shorter than a characteristic length set by gene flow and selection | Human transport is not Slatkin dispersal; clones fake clines | Dong 2023 wilds: no characteristic-length cline after clone filter |
| Nagylaki cline existence | Nagylaki 1975 Genetics 80:595-615 | If migration is too strong (or selection too weak), a cline cannot exist; the population is monomorphic unless overdominant | Dual domestication is not one habitat; nurseries are not migration | Dong 2023: no Nagylaki cline (too much transport, or two origins) after clone filter |
| Key tension zone | Key 1968 Syst Zool 17:14-22 | A tension zone is a narrow secondary-intergradation front that acts as a semipermeable membrane | Nursery hybrid is not a tension zone | Dong 2023 Syl-W gene flow is CAUTION, not a Key membrane (Barton 1979 remains the dynamics job) |
| Barton multilocus clines | Barton 1983 Evolution 37:454-471 | Coupling theta = s/r; when selection exceeds recombination the genome acts as one barrier | A cultivar panel is not a multilocus hybrid zone | Dong 2023: no coupled multilocus barrier after clone + IBD filters |
| Kaplan coalescent hitchhiking | Kaplan, Hudson and Langley 1989 Genetics 123:887-899 | Recurrent hitchhiking in low recombination substantially reduces the number of polymorphic sites | Clone IBD fakes a diversity trough | Dong 2023 color / sex / flavor: no Kaplan reduction after clone + IBD filters |
| Braverman hitchhiking SFS | Braverman et al. 1995 Genetics 140:783-796 | Simple hitchhiking predicts a large negative Tajima D (excess of rare variants) | Clone-private SNPs are not rare variants from a sweep | After clone + IBD filters, candidate loci do not show the simple-hitchhiking SFS (Tajima remains another job) |
| Berg-Coop polygenic adaptation | Berg and Coop 2014 PLoS Genet 10:e1004412 | Adaptation on a polygenic trait is coordinated frequency shifts at many small-effect loci, not a single-locus sweep | Color / sex / flavor are large-effect; clones fake genetic values | Dong 2023 color / sex / flavor peaks are few large-effect loci, not a Berg-Coop coordinated shift |
| Rockman QTN versus polygenes | Rockman 2012 Evolution 66:1-17 | Discoverable large-effect QTNs are unrepresentative; typical evolution is many undetectable small-effect polygenes | Domestication QTNs are not the typical-evolution sample | Dong 2023 color / sex / flavor are large-effect (QTN-class), not Rockman undetectable polygenes |
| Rousset IBD from pairwise FST | Rousset 1997 Genetics 145:1219-1228 | Regression of pairwise FST/(1-FST) on distance (linear habitats) or log distance (2D) estimates density times dispersal second moment | Human transport is not Rousset dispersal; clones fake FST | Dong 2023 wilds: no Rousset density-dispersal slope after clone + IBD filters (Wright 1943 remains continuous IBD; Slatkin 1993 remains pairwise M) |
| Excoffier AMOVA | Excoffier, Smouse and Quattro 1992 Genetics 131:479-491 | Hierarchical molecular variance and phi-statistics from a matrix of haplotype distances; permutation tests significance | Clones fake haplotypes; dual domestication is not one hierarchy | Dong 2023: AMOVA hierarchy is not a biological subdivision after clone + IBD filters (Weir-Cockerham 1984 remains the moment-FST job) |
| Wade-McCauley extinction-recolonization | Wade and McCauley 1988 Evolution 42:995-1005 | Extinction and recolonization increase or decrease differentiation according as K compared with 2Nm; migrant-pool versus propagule-pool colonization | A vineyard is not a deme; nursery planting is not colonization | Dong 2023 wild patches: no Wade-McCauley extinction-recolonization FST after clone filter (Levins 1969 remains occupancy) |
| Whitlock fluctuating FST | Whitlock 1992 Evolution 46:608-615 | Temporal and spatial fluctuations in demography increase FST; spatial variation affects FST more than temporal variation | A cultivar panel is not a fluctuating deme | Dong 2023 wilds: FST not inflated by demographic fluctuation after clone filter (Wade 1988 remains extinction-recolonization) |
| Slatkin two-locus cline | Slatkin 1975 Genetics 81:787-802 | When recombination is of order selection or smaller, linkage shapes two-locus clines and produces substantial LD; linkage can help or hinder tracking the environment | Clone IBD fakes LD; a chip is not the selected map | Dong 2023: no two-locus cline LD after clone + IBD filters (Slatkin 1973 remains characteristic length; Barton 1983 remains many-locus coupling) |
| Barton-Bengtsson gene-flow barrier | Barton and Bengtsson 1986 Heredity 56:357-376 | A genome-wide barrier at linked neutrals requires substantially unfit hybrids and so many selected genes that most markers are closely linked to a selected locus | A nursery hybrid is not that contact | Dong 2023 Syl-W gene flow is CAUTION, not a Barton-Bengtsson genome-wide barrier (Barton 1979 remains dynamics; Barton 1983 remains coupling) |
| Barton hybrid-sink barrier | Barton 1986 Heredity 57:415-426 | Barrier strength combines a physical barrier, a hybrid-sink density reduction, and linkage | Vineyard density is not hybrid unfitness | Dong 2023: no hybrid-sink density barrier after clone filter (1979 remains dynamics; 1983 remains coupling; Barton-Bengtsson 1986 remains the genome-wide selected barrier) |
| Kimura stochastic drift | Kimura 1955 PNAS 41:144-150 | Complete time-dependent diffusion solution for random genetic drift; heterozygosity decays as e^{-t/2N}; the distribution approaches Wright-Fisher steady decay | Clones are not a Wright-Fisher sample; a cultivar panel is not N | Clone / cultivar heterozygosity is not a Kimura-1955 drift trajectory after clone filter (Kimura 1968 remains the substitution-rate null; Kingman 1982 remains the coalescent) |
| Nei GST | Nei 1973 PNAS 70:3321-3323 | GST = DST/HT is the between-group share of total gene diversity | Clones fake identity; dual domestication is not one hierarchy | Dong 2023 wilds: no Nei GST partition after clone + IBD filters (Nei 1972 remains distance; Weir-Cockerham 1984 remains moment FST) |
| Slatkin conditional-frequency gene flow | Slatkin 1981 Genetics 99:323-335 | Allele frequency given occupancy estimates gene flow and is nearly independent of selection and mutation | Clone-private SNPs are not occupancy alleles | Dong 2023 wilds: conditional frequencies not an Nm estimate after clone filter (Slatkin 1985 remains private-allele log Nm) |
| Slatkin-Maruyama drift in a cline | Slatkin and Maruyama 1975 Genetics 81:209-222 | Drift makes a selection-maintained cline less steep than the deterministic prediction | Clones fake cline slope; a vineyard is not a colony | Dong 2023: no drift-flattened cline after clone + IBD filters (Slatkin 1975 two-locus remains LD; Slatkin 1973 remains characteristic length) |
| Nei unbiased distance | Nei 1978 Genetics 89:583-590 | Small-sample heterozygosity and distance are biased; unbiased formulae exist, and few individuals suffice if many loci and H is low | Clones fake identity; a cultivar panel is not a small sexual sample | Dong 2023 wilds: unbiased D not a single-split clock after clone + IBD filters (Nei 1972 remains the distance definition) |
| Kimura two-parameter distance | Kimura 1980 J Mol Evol 16:111-120 | Distance K from transition fraction P and transversion fraction Q; synonymous rate exceeds amino-acid-altering | Clone somatic clock is not T; chips are not sequences | Clone / cultivar K80 distance is not a Kimura-1980 clock after clone filter (Zuckerkandl-Pauling remains the clock job) |
| Tajima-Nei distance | Tajima and Nei 1984 Mol Biol Evol 1:269-285 | Nucleotide distance allows unequal substitution rates among pairs; usable when delta <= 1 | Clone IBS is not a homologous pair; a chip is not a sequence | After clone filter, Tajima-Nei delta is not a substitution clock (Tajima 1989 remains D; Kimura 1980 remains K80) |
| Begun-Aquadro recombination-diversity | Begun and Aquadro 1992 Nature 356:519-520 | Nucleotide diversity rises with recombination; divergence does not, so hitchhiking not mutation-rate variation | Chip is not a map; clone IBD fakes a diversity trough | Dong 2023 on a real Vitis map: diversity not a recombination function after clone + IBD filters (Maynard Smith-Haigh remains hitchhiking; Kaplan 1989 remains coalescent hitchhiking; Charlesworth 1993 remains BGS) |
| Ohta 1972 population-size rate | Ohta 1972 J Mol Evol 1:305-314 | Nearly-neutral substitutions with fluctuating selection fix faster in smaller populations (more uniform environments) | A cultivar panel is not Ne; dual domestication is not one size | Dong 2023: substitution / load rate not higher in the smaller-Ne class after clone filter (Ohta 1973 remains |Nes|<1 slightly deleterious) |
| Barton-de Cara isolation coupling | Barton and de Cara 2009 Evolution 63:1171-1190 | Strong isolation evolves by coupling any incompatibilities (pre- or postzygotic), not only by a universal assortative-mating modifier | Nursery hybrid is not that contact; clones fake associations | Dong 2023 Syl-W gene flow is CAUTION, not a Barton-de Cara coupling (Dobzhansky 1940 remains reinforcement; Barton 1983 remains cline coupling) |
| Rieseberg complementary-gene hybrid speciation | Rieseberg et al. 2003 Science 301:1211-1216 | Complementary gene action in hybrids recreates extreme parental-segment combinations that selection favors; hybridization facilitates ecological divergence | A nursery cross is not a homoploid hybrid species | Dong 2023: no complementary-gene hybrid species after clone filter (Anderson 1949 remains introgression) |
| Nei-Li nucleotide diversity | Nei and Li 1979 PNAS 76:5269-5273 | Polymorphism at the nucleotide level is pi, the average pairwise nucleotide difference per site; net divergence subtracts within-population pi | Clones fake pairwise identity; a chip is not a sequence | Dong 2023 wilds: pi not a Nei-Li nucleotide-diversity estimate after clone + IBD filters (Nei 1972 remains allele-frequency D; Tajima 1989 remains D) |
| Tajima 1983 nucleon genealogy | Tajima 1983 Genetics 105:437-460 | Average pairwise nucleotide differences have large stochastic variance; increasing sample size does not reduce that variance much | Clone / pedigree samples are not nucleons; cultivar relatedness fakes the variance | Dong 2023 wilds: pairwise-difference variance is not the 1983 stochastic variance after clone + IBD filters (Tajima 1989 remains D; Tajima-Nei 1984 remains distance) |
| Kimura-Ohta time to fixation | Kimura and Ohta 1969 Genetics 61:763-771 | A rare neutral mutant takes about 4Ne generations to fixation, excluding the cases of loss | A cultivar panel is not Ne; clone age is not 4Ne generations | Clone / cultivar fixation time is not 4Ne after clone filter (Kimura 1968 remains the substitution-rate null; Kimura 1955 remains the drift diffusion) |
| Charlesworth 1994 BGS on selected variants | Charlesworth 1994 Genet Res 63:213-227 | BGS multiplies Ne by the frequency of mutation-free gametes; slightly deleterious mutations fix faster and advantageous mutations fix slower | Chip is not a map; a cultivar panel is not Ne | Dong 2023 on a real Vitis map: weakly selected substitution rates not a Charlesworth-1994 BGS function after clone filter (Charlesworth 1993 remains neutral-diversity BGS) |
| Hudson-Kaplan BGS with recombination | Hudson and Kaplan 1995 Genetics 141:1605-1617 | Expected nucleotide diversity at a neutral locus has an analytic form when deleterious mutation and recombination both act | Chip is not a map; clone IBD fakes a diversity trough | Dong 2023 on a real Vitis map: diversity not the Hudson-Kaplan BGS function after clone + IBD filters (Charlesworth 1993 remains the BGS lock; Kaplan 1989 remains coalescent hitchhiking) |
| Nordborg-Charlesworth BGS map | Nordborg, Charlesworth and Charlesworth 1996 Genet Res 67:159-174 | BGS reduction of diversity holds for an arbitrary genetic map; weakly selected mutations pattern a chromosome more than strongly selected ones; tips less than the centre | Chip is not a map; a vineyard is not a Drosophila map | Dong 2023 on a real Vitis map: no Nordborg-map BGS patterning after clone + IBD filters (Hudson-Kaplan 1995 remains the recombination formula; Charlesworth 1993 remains the BGS lock) |
| Wiehe-Stephan hitchhiking alpha v | Wiehe and Stephan 1993 Mol Biol Evol 10:842-854 | Steady-state recurrent hitchhiking is characterized by alpha v = 2Ns times the beneficial-mutation frequency; adequate unless recombination is very low | Chip is not a map; clone IBD fakes a trough | Dong 2023 on a real Vitis map: diversity not a Wiehe-Stephan alpha-v hitchhiking function after clone + IBD filters (Maynard Smith-Haigh remains local hitchhiking; Kaplan 1989 remains coalescent hitchhiking; Begun-Aquadro remains the recombination-diversity correlation) |
| Orr snowball incompatibilities | Orr 1995 Genetics 139:1805-1813 | Complementary-gene incompatibilities accumulate faster than linearly with time; the probability of speciation increases at least as the square of time since separation | A nursery cross is not a diverging pair; clones fake complementary genes | Dong 2023: no snowball of complementary-gene incompatibilities after clone filter (Dobzhansky 1937 remains BDM; Orr 1998 remains exponential factors; Rieseberg 2003 remains hybrid speciation) |
| Turelli-Orr dominance Haldane | Turelli and Orr 1995 Genetics 140:389-402 | Hybrid-fitness alleles are partially recessive, so the heterogametic sex suffers more (hemizygous X effects) | Grape is not XX/XY; sex is an SDR | Does not map onto Vitis SDR; do not invent a heterogametic-dominance test (Haldane 1922 remains the rule statement) |
| Coyne-Orr time course of isolation | Coyne and Orr 1989 Evolution 43:362-381 | Mating discrimination and hybrid sterility / inviability increase gradually with time; in sympatry, prezygotic isolation appears well before postzygotic isolation | Nursery hybrid is not a Drosophila pair; grape is not XX/XY | Dong 2023 Syl-W gene flow is CAUTION, not a Coyne-Orr time-course (Dobzhansky 1940 remains reinforcement; Mayr 1942 remains BSC; Haldane 1922 remains the rule) |

One hundred twelve filled notes (eight first wave, nine second wave, nine third wave, twelve fourth wave, ten fifth wave, ten sixth wave, nine seventh wave, eight eighth wave, nine ninth wave, eight tenth wave, ten eleventh wave, ten twelfth wave). Long form in `theories.md`. One theory per job.

Kondrashov 1988 (cost of males) is on the door list but was not filled: it does not map onto grafted clones.
Muller 1942 was not locked on a publisher page and is not cited for BDM.
Flor 1971 is a review and was not used as a theory source.
Flor 1955 Phytopathology / Flor 1956 Adv Genet were not opened on a publisher page this wave and are not cited.
Haldane 1922 is filled as "does not map onto Vitis SDR"; grape is not XX/XY.

Reinforcement (Dobzhansky 1940 Am Nat 74:312-321) is filled as a
paper, distinct from the 1937 BDM book. Dong 2023 Syl-W gene flow
is CAUTION, not a reinforcement map.
Two-fold cost of sex (Maynard Smith 1978 book) is filled as "does
not map onto grafted clones"; Kondrashov 1988 is not this paper.
Overdominance / heterozygote advantage is on the door list but was
not filled: term vs theory split (Hull 1946 Agron J vs Dobzhansky
1950 Genetics); standing heterozygosity in clones is not a test of
balancing selection; no locked grape inversion / overdominant QTL
paper.
Red Queen (Van Valen 1973 Evol Theory 1:1-30) is on the door list
but was not filled: the original claim is a constant taxonomic
extinction rate; the host-pathogen reading is later; no grape
pathogen-coevolution paper is locked.
Centromere drive (Henikoff 2001 Science review; Henikoff and Malik
2002 Nature N&V) is on the door list but was not filled: named
papers are a review and a one-page N&V; the claim requires female
meiosis; grafted clones have no meiosis between cuttings; no grape
centromere / CenH3 paper is locked.


## Plant / Vitis checks

- Filter clones before any "population" statistic that assumes unrelated sexuals.
- Do not treat a cultivar panel as Ne.
- Somatic mutation and germline mutation are different clocks. Say which one you measured.
- Plastid / TE / graph coordinates are not interchangeable with a 12X SNP panel.
- aDNA samples project onto a modern panel; they do not redefine the theory.
- A real recombination map is required for background selection and Hill-Robertson. A chip skeleton is not that map.
- Standing heterozygosity and ancestral inbreeding (Roach 2018) are not the Meselson effect.
- Wild sylvestris geography is the isolation-by-distance test; a cultivar PCA is not.
- Hermaphroditism is the Baker test (Dong 2023 SDR on chromosome 2), not VviAGL11.
- Diplontic selection in meristems is a caveat on the ratchet, not a replacement theory.
- Kingman coalescent assumes a random sample from a large haploid population. Clones and pedigrees are not that sample.
- Clone-private SNPs are not McDonald-Kreitman substitutions.
- Strongly negative Tajima's D in a cultivar panel is relatedness until clones and IBD are removed.
- The somatic clone clock is not the Zuckerkandl-Pauling germline clock.
- Genetic draft is recurrent linked substitutions, not one hitchhiking event and not background selection.
- Haldane's rule does not map onto the Vitis sex-determination region.

- Stepping-stone is neighbor-only steps; a cultivar PCA is not a lattice.
- The island model has no distance; a nonzero IBD slope in wild sylvestris kills it.
- Clonal interference needs two competing beneficials in one finite N; a single sport is not CI.
- Allele surfing needs a single expanding front; dual domestication and human transport break it.
- Genome shock is an unprepared challenge, not a constitutive somatic TE clock.
- Vitis is palaeo-hexaploid, not a recent allopolyploid; SVs change dose without WGD.
- Drift-barrier is evolution of mu, not Ohta load; no locked grape wild-vs-cultivar mu paper.
- gBGC is meiotic; a chip skeleton is not a recombination map (same map rule as BGS / HR).
- Soft sweep is multiple surviving haplotypes; pedigree IBD fakes a hard sweep.
- Vitis SAM is L1/L2, not three Datura layers; Franks 2002 Pinot Meunier is the grape test.
- Reinforcement is premating isolation after secondary contact, not BDM inviability and not Dong 2023 gene flow.
- The two-fold cost of sex does not map onto grafted clones. Hermaphroditism is the Baker test, not a cost of males.

- Haldane 1957 cost does not map onto grafted clones as a substituting sexual population.
- Darwin 1876 is a self-versus-cross progeny test; standing clone heterozygosity is not that test.
- Fisher 1918 infinitesimal dies where Dong 2023 color / sex / flavor are few large-effect loci.
- Waddington 1953 assimilation needs many sexual generations; cuttings skip them.
- Ohno 1972 junk DNA is C-value versus gene number, not selfish-DNA persistence (1980).
- Zimmer 1980 concerted evolution is within-species homogenization; Nei 1997 is the opposite job.
- Levins 1969 is patch occupancy; a vineyard is not a patch (island / stepping-stone / IBD remain separate).
- McClintock 1941 BFB is broken-end cycling, not 1950 TE and not 1984 shock.
- Thomas, Pedersen and Freeling 2006 fractionation is biased homeolog loss after WGD, not Ohno dosage and not Stebbins polyploid type.

- Ewens 1972 is the sampling configuration under infinite-alleles; Kimura and Crow 1964 is the allele model (already filled). Clone IBS is not the sample.
- Wright 1932 shifting balance is peak-shift by subdivided trial-and-error; Wright 1931 island and Wright 1943 IBD remain separate jobs. A vineyard is not a Wright race.
- Fisher 1930 geometric is random mutations in n-space (pages 38-41); Fisher 1918 infinitesimal is already filled.
- Haldane 1927 mutation-selection balance is equilibrium load; Haldane 1957 cost and Mukai 1964 MA are different jobs. Clone-private SNPs are not q = mu/s.
- Dover 1982 molecular drive is cohesive replacement through genome and population; Zimmer 1980 concerted is the within-species pattern (already filled).
- Holliday 1964 gene conversion is hybrid-DNA mismatch repair; Galtier 2001 gBGC is the GC-biased population force (already filled). Cuttings skip meiosis.
- Eigen 1971 quasispecies does not map onto grafted clones. A chimera is not a mutant cloud.
- Ramachandran 2005 serial founder is heterozygosity declining from one origin; dual domestication, IBD, and allele surfing are different jobs.
- Lande 1979 is G beta; Dong 2023 color / sex / flavor are few large-effect loci, not a G-matrix response. Not Fisher 1918 and not Fisher 1930 geometric.
- Sagan 1967 organelle origin does not map onto grafted clones. Lynch 1996 remains the organelle-ratchet note. Timmis 2004 is a review.

- Vavilov 1932 is seven geographically small crop centres (ESP facsimile pp. 331-342). Homologous series is named there as Vavilov 1922 J Genet; that paper was not opened. Dual domestication is not one centre. Serial founder remains Ramachandran 2005.
- Price 1970 is selection as covariance; Lande 1979 remains G beta. Cuttings are not a generation. Dong 2023 color / sex / flavor are few large-effect loci.
- Hamilton 1964 inclusive fitness does not map onto grafted clones. A chimera is not kin selection. Trivers 1974 was not filled.
- Nei 1972 is between-population distance from gene identity; Wright 1931 island, Wright 1943 IBD, and Nei 1997 birth-and-death remain other jobs. Clone IBS is not identity.
- Weir and Cockerham 1984 is the FST estimator; Wright 1931 remains the island parameter. A vineyard is not a deme.
- Orr 1998 is the exponential distribution of factors fixed on a walk; Fisher 1930 geometric is the chance a random mutation improves (already filled). Orr 2005 is a review.
- Charlesworth 1978 is Y degeneration by ratchet plus dosage compensation. Haldane 1922 remains does-not-map for heterogametic sterility. Charlesworth 1991 Science is a review. Dong 2023 chr-2 SDR is the young-SDR contrast.
- Mayr 1942 is the biological species book; Dobzhansky 1937 remains BDM and 1940 remains reinforcement. Founder effect (often 1954) was not opened.
- HKA 1987 is polymorphism-divergence scaling; MK 1991 and Tajima 1989 remain other jobs. Hudson 1990 survey and Hudson 2002 ms were not used as sources.

- Lewontin-Krakauer 1973 is F heterogeneity among loci as a selection test. Wright 1931 remains island math; Wright 1943 remains IBD; Weir-Cockerham 1984 remains the estimator. Beaumont and Nichols 1996 was not used.
- Fay-Wu 2000 H is derived high-frequency excess. Maynard Smith and Haigh 1974 remains diversity collapse; Tajima 1989 remains pi versus theta_W; HKA 1987 remains polymorphism-divergence scaling.
- Fu-Li 1993 is external versus internal mutations. Tajima 1989 remains the other one-sample job. Clone-private SNPs are not external mutations.
- Slatkin 1985 is private-allele Nm. Slatkin 1987 Science is a review. Wright 1931 remains the island parameter.
- Slatkin 1993 is pairwise M versus distance. Wright 1943 remains the continuous-space original. Serial founder remains Ramachandran 2005.
- Barton 1979 is tension-zone dynamics. Barton and Hewitt 1985 is a review. Anderson 1949 remains introgression; Dobzhansky 1940 remains reinforcement; Mayr 1942 remains BSC.
- Endler 1977 is clines / parapatric differentiation despite gene flow (book). Not Wright 1943 and not Barton 1979.
- Crow 1958 is the mutational / segregation / incompatibility load partition. Haldane 1957 remains does-not-map (substitution cost). Haldane 1927 remains equilibrium q. Muller 1964 remains the ratchet. Muller 1950 body was not opened.

- Haldane 1948 is the selection-migration slope of an equilibrium cline at a habitat boundary. Endler 1977 remains the parapatric-despite-gene-flow book. Barton 1979 remains tension-zone dynamics. Wright 1943 remains continuous IBD. Fisher 1937 was not opened.
- Slatkin 1973 is characteristic length: populations cannot track environmental grain shorter than that scale. Distinct from Slatkin 1985 private alleles and Slatkin 1993 pairwise M.
- Nagylaki 1975 is the existence threshold: too much migration erases the cline (monomorphism unless overdominance). Distinct from Haldane 1948 slope-given-a-cline.
- Key 1968 names the tension zone as a semipermeable secondary-intergradation membrane. Barton 1979 remains the dynamics original. Barton and Hewitt 1985 remains a review.
- Barton 1983 is multilocus coupling (theta = s/r) and a genome-wide barrier. Distinct from 1979 single-locus / hybrid-zone dynamics.
- Kaplan, Hudson and Langley 1989 is coalescent hitchhiking reducing the number of polymorphic sites in low recombination. Maynard Smith and Haigh 1974 remains deterministic collapse. Charlesworth 1993 remains BGS. Fay-Wu 2000 remains derived high-frequency H. Stephan 1992 was not opened.
- Braverman et al. 1995 is the hitchhiking SFS: simple hitchhiking predicts large negative Tajima D. Tajima 1989 remains the statistic. Kaplan 1989 remains the site-count job. Clone-private SNPs are not rare sweep variants.
- Berg and Coop 2014 is polygenic adaptation as coordinated frequency shifts. Pritchard, Pickrell and Coop 2010 is a review. Hermisson 2005 remains the soft-sweep original. Fisher 1918 remains infinitesimal inheritance.
- Rockman 2012 is the claim that mapped large-effect QTNs mislead about typical evolution. Distinct from Fisher 1918. Boyle 2017 omnigenic was a review.

- Rousset 1997 is pairwise FST/(1-FST) versus distance or log distance as an estimator of density times dispersal second moment. Wright 1943 remains continuous IBD. Slatkin 1993 remains pairwise M. Weir-Cockerham 1984 remains the moment estimator.
- Excoffier, Smouse and Quattro 1992 is AMOVA: haplotype-distance hierarchical variance and phi-statistics with permutation tests. Distinct from Weir-Cockerham 1984 moment FST and Nei 1972 distance. Dual domestication is not one nested hierarchy. Clones fake haplotypes.
- Wade and McCauley 1988 is extinction and recolonization: migrant pool versus propagule pool; differentiation depends on K versus 2Nm, not primarily on the extinction rate. Levins 1969 remains occupancy. Pannell and Charlesworth 2000 is a review.
- Whitlock 1992 is fluctuating demography inflating FST; spatial variation greater than temporal. Distinct from Wade 1988 colonization models. A cultivar panel is not a fluctuating deme.
- Slatkin 1975 two-locus is linkage and LD in a cline when r is of order s. Distinct from Slatkin 1973 characteristic length and Barton 1983 many-locus coupling. Sex locus is Dong 2023 chromosome-2 SDR, never VviAGL11.
- Barton and Bengtsson 1986 is the genome-wide barrier at linked neutrals: hybrids must be substantially unfit and selected loci numerous. Distinct from Barton 1979 dynamics and Barton 1983 coupling. Hewitt 1988 TREE is a review.
- Barton 1986 hybrid-sink paper combines physical barrier, hybrid-sink density, and linkage. Distinct from Barton-Bengtsson 1986. Vineyard density is not hybrid unfitness.
- Kimura 1955 is the complete time-dependent diffusion solution for panmictic random drift; H decays as e^{-t/2N}. Distinct from Kimura 1968, Kimura-Weiss 1964, Kimura-Crow 1964, Kimura 1969, Kingman 1982. Clone age is not Wright-Fisher t.

- Nei 1973 is GST = DST/HT, the between-group share of total gene diversity. Nei 1972 remains genetic distance. Weir-Cockerham 1984 remains the moment estimator. Excoffier 1992 remains AMOVA. Wright 1951 still has no claim text.
- Slatkin 1981 is conditional average frequency given occupancy as a gene-flow estimate nearly independent of selection and mutation. Slatkin 1985 remains private-allele log Nm. Slatkin 1993 remains pairwise M.
- Slatkin and Maruyama 1975 is drift flattening a selection-maintained cline. Distinct from Slatkin 1975 two-locus LD and Slatkin 1973 characteristic length. Sex locus is Dong 2023 chromosome-2 SDR, never VviAGL11.
- Nei 1978 is the small-sample unbiased estimator of heterozygosity and D. Distinct from Nei 1972 (definition) and Nei 1973 (GST).
- Kimura 1980 is K80 / K2P distance from transition fraction P and transversion fraction Q. Distinct from Kimura 1968, Kimura 1955, Kimura 1969, and Zuckerkandl-Pauling. Clone age is not T. Jukes and Cantor 1969 was not opened.
- Tajima and Nei 1984 is unequal-rate nucleotide distance delta (usable when delta <= 1). Distinct from Tajima 1989 D and from Kimura 1980 K80.
- Begun and Aquadro 1992 is the genome-wide recombination-diversity correlation with no matching divergence correlation. Distinct from Maynard Smith and Haigh 1974, Kaplan 1989, and Charlesworth 1993 BGS. A chip is not a map.
- Ohta 1972 is nearly-neutral substitutions with fluctuating selection fixing faster in smaller, more uniform populations. Distinct from Ohta 1973 |Nes|<1. Ohta 1992 remains a review. A cultivar panel is not Ne.
- Barton and de Cara 2009 is coupling of any incompatibilities as a route to strong isolation, distinct from Dobzhansky 1940 reinforcement and Barton 1983 cline coupling. Barton 2000 is a review.
- Rieseberg et al. 2003 is complementary-gene recreation of extreme parental-segment combinations in a hybrid species. Distinct from Anderson 1949 introgression. Rieseberg 1997 Annu Rev is a review. A nursery cross is not a homoploid hybrid species.

- Nei and Li 1979 is nucleotide diversity pi, the mean pairwise nucleotide difference per site, with net divergence subtracting within-population pi. Nei 1972 remains allele-frequency D. Nei 1973 remains GST. Nei 1978 remains unbiased H/D. Tajima 1989 remains D. A chip is not a sequence. Clone IBS is not pi.
- Tajima 1983 is the nucleon-genealogy theory that pairwise-difference estimates have large stochastic variance that extra samples do not shrink. Distinct from Tajima 1989 D and Tajima-Nei 1984 distance. A cultivar panel is not a nucleon sample. Tajima 1993 was not opened.
- Kimura and Ohta 1969 is the 4Ne-generation mean time to fixation of a rare neutral, excluding loss. Distinct from Kimura 1968, Kimura 1955, and Ohta 1972 / 1973. A cultivar panel is not Ne. Clone age is not 4Ne. Kimura and Ohta 1971 Nature had no claim text.
- Charlesworth 1994 is BGS on weakly selected linked variants: Ne multiplied by the frequency of mutation-free gametes; slightly deleterious fix faster; advantageous fix slower. Charlesworth 1993 remains neutral-diversity BGS. A chip is not a map.
- Hudson and Kaplan 1995 is the analytic BGS expression for nucleotide diversity when deleterious mutation and recombination both act. Distinct from Charlesworth 1993 and from Kaplan 1989 hitchhiking. A chip is not a map.
- Nordborg, Charlesworth and Charlesworth 1996 is BGS on an arbitrary map: weakly selected mutations pattern a chromosome more; tips less than the centre. Distinct from 1993 / 1994 / 1995. A chip is not a map.
- Wiehe and Stephan 1993 is steady-state recurrent hitchhiking characterized by alpha v = 2Ns times beneficial-mutation frequency. Distinct from Maynard Smith and Haigh 1974, Kaplan 1989, and Begun-Aquadro 1992. Stephan 1992 remains unopened. A chip is not a map.
- Orr 1995 is the snowball: complementary-gene incompatibilities accumulate faster than linearly; P(speciation) increases at least as t squared. Distinct from Dobzhansky 1937 BDM, Orr 1998 exponential, and Rieseberg 2003 hybrid speciation. A nursery cross is not a snowball test.
- Turelli and Orr 1995 is the dominance theory of Haldane's rule (partially recessive hybrid-fitness alleles; hemizygous X). Distinct from Haldane 1922. Does not map onto Vitis SDR. Sex locus is Dong 2023 chromosome-2 SDR, never VviAGL11.
- Coyne and Orr 1989 is the comparative time course: isolation increases with time; prezygotic isolation appears first in sympatry. Distinct from Dobzhansky 1940 reinforcement and Mayr 1942 BSC. Coyne and Orr 1997 is a revisit. Syl-W gene flow is CAUTION.

## Sources to open first (fetched)

- Muller 1964: https://doi.org/10.1016/0027-5107(64)90047-8
- Felsenstein 1974: https://doi.org/10.1093/genetics/78.2.737 (PMC1213231)
- Ohta 1973: https://doi.org/10.1038/246096a0
- Maynard Smith and Haigh 1974: https://doi.org/10.1017/s0016672300014634 (PMID 4407212)
- Hill and Robertson 1966: https://doi.org/10.1017/s0016672300010156
- Kimura 1968: https://doi.org/10.1038/217624a0
- Kimura 1969: https://doi.org/10.1093/genetics/61.4.893
- Watterson 1975: https://doi.org/10.1016/0040-5809(75)90020-9
- McClintock 1950: https://doi.org/10.1073/pnas.36.6.344
- Birchler and Veitia 2007: https://doi.org/10.1105/tpc.106.049338 (PMC1867330)
- Vondras 2019: https://doi.org/10.1186/s12864-019-6211-2 (PMC6907202)
- Carbonell-Bejerano 2017: https://doi.org/10.1104/pp.17.00715 (PMC5619900)
- Roach 2018: https://doi.org/10.1371/journal.pgen.1007807
- Carrier 2012: https://doi.org/10.1371/journal.pone.0032973
- Dong 2023: https://doi.org/10.1126/science.add8655 (PMID 36862793)
- Zhou 2019: https://doi.org/10.1038/s41477-019-0507-8
- Jaillon 2007: https://doi.org/10.1038/nature06148
- Lovell 2017: https://doi.org/10.1371/journal.pgen.1006550
- Charlesworth, Morgan and Charlesworth 1993: https://doi.org/10.1093/genetics/134.4.1289 (PMID 8375663 PMC1205596)
- Mark Welch and Meselson 2000: https://doi.org/10.1126/science.288.5469.1211 (PMID 10817991)
- Lynch 1996: https://doi.org/10.1093/oxfordjournals.molbev.a025557 (PMID 8583893)
- Force et al. 1999: https://doi.org/10.1093/genetics/151.4.1531 (PMID 10101175 PMC1460548)
- Doolittle and Sapienza 1980: https://doi.org/10.1038/284601a0 (PMID 6245369)
- Orgel and Crick 1980: https://doi.org/10.1038/284604a0 (PMID 7366731)
- Baker 1955: https://doi.org/10.1111/j.1558-5646.1955.tb01544.x (also 10.2307/2405656)
- Wright 1943: https://doi.org/10.1093/genetics/28.2.114 (PMID 17247074 PMC1209196)
- Klekowski 1988 book: https://doi.org/10.7312/klek92068
- Kingman 1982: https://doi.org/10.1016/0304-4149(82)90011-4
- Kimura and Crow 1964: https://doi.org/10.1093/genetics/49.4.725 (PMID 14156929 PMC1210609)
- Zuckerkandl and Pauling 1965 chapter: https://doi.org/10.1016/B978-1-4832-2734-4.50017-6
- McDonald and Kreitman 1991: https://doi.org/10.1038/351652a0 (PMID 1904993)
- Tajima 1989: https://doi.org/10.1093/genetics/123.3.585 (PMID 2513255 PMC1203831)
- Mukai 1964: https://doi.org/10.1093/genetics/50.1.1 (PMID 14191352 PMC1210633)
- Gillespie 2000: https://doi.org/10.1093/genetics/155.2.909 (PMID 10835409 PMC1461093)
- Haldane 1922: https://doi.org/10.1007/BF02983075 (IAS: https://www.ias.ac.in/article/fulltext/jgen/012/02/0101-0109)

- Kimura and Weiss 1964: https://doi.org/10.1093/genetics/49.4.561
- Wright 1931: https://doi.org/10.1093/genetics/16.2.97
- Gerrish and Lenski 1998: https://doi.org/10.1023/A:1017067816551
- Edmonds et al. 2004: https://doi.org/10.1073/pnas.0308064100
- Klopfstein et al. 2006 (name only): https://doi.org/10.1093/molbev/msj057
- McClintock 1984: https://doi.org/10.1126/science.15739260
- Stebbins 1947: https://doi.org/10.1016/S0065-2660(08)60490-3
- Lynch 2011: https://doi.org/10.1093/gbe/evr066
- Sung et al. 2012 (test, not source): https://doi.org/10.1073/pnas.1216223109
- Galtier et al. 2001: https://doi.org/10.1093/genetics/159.2.907
- Hermisson and Pennings 2005: https://doi.org/10.1534/genetics.104.036947
- Satina, Blakeslee and Avery 1940: https://doi.org/10.1002/j.1537-2197.1940.tb13952.x
- Franks et al. 2002: https://doi.org/10.1007/s001220100683
- Dobzhansky 1940: https://doi.org/10.1086/280899
- Maynard Smith 1978 book: ISBN 052121887X (Cambridge University Press)

- Haldane 1957: https://doi.org/10.1007/BF02984069 (IAS: https://www.ias.ac.in/article/fulltext/jgen/055/03/0511-0524)
- Darwin 1876 book: https://darwin-online.org.uk/content/record?itemID=F1249
- Fisher 1918: https://doi.org/10.1017/S0080456800012163
- Waddington 1953: JSTOR 2405747 (Evolution 7:118-126)
- Ohno 1972: PMID 5065367 (EuropePMC MED 5065367)
- Zimmer et al. 1980: https://doi.org/10.1073/pnas.77.4.2158 (PMC348671)
- Nei, Gu and Sitnikova 1997: https://doi.org/10.1073/pnas.94.15.7799 (PMC33709)
- Levins 1969: https://doi.org/10.1093/besa/15.3.237
- McClintock 1941: https://doi.org/10.1093/genetics/26.2.234 (PMC1209127)
- Thomas, Pedersen and Freeling 2006: https://doi.org/10.1101/gr.4708406 (PMC1484460)

- Ewens 1972: https://doi.org/10.1016/0040-5809(72)90035-4 (EuropePMC MED 4667078)
- Wright 1932: http://www.esp.org/books/6th-congress/facsimile/contents/6th-cong-p356-wright.pdf (TOC: http://www.esp.org/books/6th-congress/facsimile/index.html)
- Fisher 1930 book, geometric pages 38-41: https://archive.org/details/geneticaltheoryo00fishuoft
- Haldane 1927: https://doi.org/10.1017/S0305004100015644
- Dover 1982: https://doi.org/10.1038/299111a0 (EuropePMC MED 7110332)
- Holliday 1964: https://doi.org/10.1017/S0016672300001233
- Eigen 1971: https://doi.org/10.1007/BF00623322
- Ramachandran et al. 2005: https://doi.org/10.1073/pnas.0507611102 (PMC1276087; EuropePMC MED 16243969)
- Lande 1979: https://doi.org/10.1111/j.1558-5646.1979.tb04694.x (EuropePMC MED 28568194)
- Sagan 1967: https://doi.org/10.1016/0022-5193(67)90079-3 (EuropePMC MED 11541392)

- Vavilov 1932: http://www.esp.org/books/6th-congress/facsimile/contents/6th-cong-p331-vavilov.pdf (TOC: http://www.esp.org/books/6th-congress/facsimile/index.html)
- Price 1970: https://doi.org/10.1038/227520a0 (EuropePMC MED 5428476)
- Hamilton 1964: https://doi.org/10.1016/0022-5193(64)90038-4 (EuropePMC MED 5875341)
- Nei 1972: https://doi.org/10.1086/282771 (Crossref work JSON; CiNii crid 1364233269783061504)
- Weir and Cockerham 1984: https://doi.org/10.1111/j.1558-5646.1984.tb05657.x (EuropePMC MED 28563791)
- Orr 1998: https://doi.org/10.1111/j.1558-5646.1998.tb01823.x (EuropePMC MED 28565213)
- Charlesworth 1978: https://doi.org/10.1073/pnas.75.11.5618 (PMC393018; EuropePMC MED 281711)
- Mayr 1942 book: https://books.google.com/books/about/Systematics_and_the_Origin_of_Species_fr.html?id=XxMgAQAAMAAJ
- Hudson, Kreitman and Aguade 1987: https://doi.org/10.1093/genetics/116.1.153 (PMC1203113; EuropePMC MED 3110004)

- Lewontin and Krakauer 1973: https://doi.org/10.1093/genetics/74.1.175 (PMC1212935; EuropePMC MED 4711903)
- Fay and Wu 2000: https://doi.org/10.1093/genetics/155.3.1405 (PMC1461156; EuropePMC MED 10880498)
- Fu and Li 1993: https://doi.org/10.1093/genetics/133.3.693 (PMC1205353; EuropePMC MED 8454210)
- Slatkin 1985: https://doi.org/10.1111/j.1558-5646.1985.tb04079.x (EuropePMC MED 28563643)
- Slatkin 1993: https://doi.org/10.1111/j.1558-5646.1993.tb01215.x (EuropePMC MED 28568097)
- Barton 1979: https://doi.org/10.1038/hdy.1979.87 (Nature / Heredity HTML)
- Endler 1977 book: https://press.princeton.edu/books/paperback/9780691081922/geographic-variation-speciation-and-clines
- Crow 1958: EuropePMC REST EXT_ID 13513111; reprint PDF https://freethoughtblogs.com/pharyngula/files/2015/01/crow_selectioninman.pdf (1958 imprint on the reprint)

- Haldane 1948: https://doi.org/10.1007/BF02986626 (EuropePMC MED 18905075; IAS https://www.ias.ac.in/article/fulltext/jgen/048/03/0277-0284)
- Slatkin 1973: https://doi.org/10.1093/genetics/75.4.733 (PMC1213045; EuropePMC MED 4778791)
- Nagylaki 1975: https://doi.org/10.1093/genetics/80.3.595 (PMC1213362; EuropePMC MED 1232026)
- Key 1968: https://doi.org/10.1093/sysbio/17.1.14 (Oxford Academic HTML)
- Barton 1983: https://doi.org/10.1111/j.1558-5646.1983.tb05563.x (EuropePMC MED 28563316; ISTA https://research-explorer.ista.ac.at/record/3668)
- Kaplan, Hudson and Langley 1989: https://doi.org/10.1093/genetics/123.4.887 (PMC1203897; EuropePMC MED 2612899)
- Braverman et al. 1995: https://doi.org/10.1093/genetics/140.2.783 (PMC1206652; EuropePMC MED 7498754)
- Berg and Coop 2014: https://doi.org/10.1371/journal.pgen.1004412 (PMC4125079; EuropePMC MED 25102153; PLoS HTML)
- Rockman 2012: https://doi.org/10.1111/j.1558-5646.2011.01486.x (PMC3386609; EuropePMC MED 22220860)

- Rousset 1997: https://doi.org/10.1093/genetics/145.4.1219 (PMC1207888; EuropePMC MED 9093870)
- Excoffier, Smouse and Quattro 1992: https://doi.org/10.1093/genetics/131.2.479 (PMC1205020; EuropePMC MED 1644282)
- Wade and McCauley 1988: https://doi.org/10.1111/j.1558-5646.1988.tb02518.x (EuropePMC MED 28581169)
- Whitlock 1992: https://doi.org/10.1111/j.1558-5646.1992.tb02069.x (EuropePMC MED 28568658)
- Slatkin 1975 two-locus: https://doi.org/10.1093/genetics/81.4.787 (PMC1213435; EuropePMC MED 1213276)
- Barton and Bengtsson 1986: https://doi.org/10.1038/hdy.1986.135 (EuropePMC MED 3804765; Nature PDF https://www.nature.com/articles/hdy1986135.pdf)
- Barton 1986 hybrid-sink: https://doi.org/10.1038/hdy.1986.142 (EuropePMC MED 3804768; Nature PDF https://www.nature.com/articles/hdy1986142.pdf)
- Kimura 1955: https://doi.org/10.1073/pnas.41.3.144 (PMC528040; EuropePMC MED 16589632; PDF https://europepmc.org/articles/PMC528040?pdf=render)

- Nei 1973: https://doi.org/10.1073/pnas.70.12.3321 (PMC427228; EuropePMC MED 4519626)
- Slatkin 1981: https://doi.org/10.1093/genetics/99.2.323 (PMC1214504; EuropePMC MED 17249120)
- Slatkin and Maruyama 1975: https://doi.org/10.1093/genetics/81.1.209 (PMC1213384; EuropePMC MED 1205126)
- Nei 1978: https://doi.org/10.1093/genetics/89.3.583 (PMC1213855; EuropePMC MED 17248844)
- Kimura 1980: https://doi.org/10.1007/bf01731581 (EuropePMC MED 7463489)
- Tajima and Nei 1984: https://doi.org/10.1093/oxfordjournals.molbev.a040317 (EuropePMC MED 6599968)
- Begun and Aquadro 1992: https://doi.org/10.1038/356519a0 (EuropePMC MED 1560824)
- Ohta 1972: https://doi.org/10.1007/BF01653959 (Springer HTML; EuropePMC MED 4681232 bibliographic)
- Barton and de Cara 2009: https://doi.org/10.1111/j.1558-5646.2009.00622.x (EuropePMC MED 19154394)
- Rieseberg et al. 2003: https://doi.org/10.1126/science.1086949 (EuropePMC MED 12907807)

- Nei and Li 1979: https://doi.org/10.1073/pnas.76.10.5269 (PMC413122; EuropePMC MED 291943)
- Tajima 1983: https://doi.org/10.1093/genetics/105.2.437 (PMC1202167; EuropePMC MED 6628982)
- Kimura and Ohta 1969: https://doi.org/10.1093/genetics/61.3.763 (PMC1212239; EuropePMC MED 17248440)
- Charlesworth 1994: https://doi.org/10.1017/s0016672300032365 (EuropePMC MED 8082838)
- Hudson and Kaplan 1995: https://doi.org/10.1093/genetics/141.4.1605 (PMC1206891; EuropePMC MED 8601498)
- Nordborg, Charlesworth and Charlesworth 1996: https://doi.org/10.1017/s0016672300033619 (EuropePMC MED 8801188)
- Wiehe and Stephan 1993: https://doi.org/10.1093/oxfordjournals.molbev.a040046 (EuropePMC MED 8355603)
- Orr 1995: https://doi.org/10.1093/genetics/139.4.1805 (PMC1206504; EuropePMC MED 7789779)
- Turelli and Orr 1995: https://doi.org/10.1093/genetics/140.1.389 (PMC1206564; EuropePMC MED 7635302)
- Coyne and Orr 1989: https://doi.org/10.1111/j.1558-5646.1989.tb04233.x (EuropePMC MED 28568554)

## Red lines

- Do not cite a review as the source of the theory.
- Do not apply a sexual-diploid model to clones and call it a test.
- Do not invent citations, years, or the original equation.
- Do not turn this into a 50-theory catalog. One theory per job.
- No unpublished genotypes or private site coordinates in the public note.
- Label Pol-e x ratchet as a TESTABLE HUNCH, never as a grape result.
- Do not cite Mark Welch and Meselson 2000 as a 1960s original.
- Do not invent a grape plastid popgen paper or a grape BDM map.
- Do not write VviAGL11 as the sex gene (Dong 2023 SDR is chromosome 2).
- Do not treat clone-private SNPs as McDonald-Kreitman substitutions.
- Do not write a clone tree in years-since-planting as the molecular clock.
- Do not invent a heterogametic sterility pattern for Vitis. Haldane does not map onto the SDR.
- Do not cite Flor 1971. Flor 1955 / 1956 originals were not locked this wave.
- Do not invent a grape powdery-mildew NLR paper.

- Do not cite Lynch 2010 Trends Genet as the drift-barrier source (review).
- Do not invent a grape mutation-rate paper or a grape recombination-map paper.
- Do not write VviAGL11 as the soft-sweep sex-locus test (SDR H1/H2 is).
- Do not treat a mixed-leaf SSR profile as tunica-corpus proof.
- Do not fill overdominance, Red Queen, or centromere drive.
- Do not invent a grape hybrid / prezygotic-isolation paper for reinforcement.
- Do not invent a cost-of-males test in grafted clones. Two-fold cost does not map.
- Do not cite McClintock 1984 as the 1950 TE note (different job).
- Do not cite Stebbins 1940 or 1950 as the 1947 polyploid-type source.

- Do not cite Wang and Bradburd 2014 as an IBE original (review).
- Do not fill adaptive introgression as distinct from Anderson 1949.
- Do not cite Nei and Rooney 2005 or Freeling 2009 as theory sources (reviews).
- Do not cite Dover 1982 as the concerted-evolution original (Zimmer 1980 is).
- Do not cite McClintock 1941 as the 1950 TE note or the 1984 shock note.
- Do not invent a grape cost-of-selection, assimilation, rDNA, NLR-phylogeny, or patch-turnover paper.
- Do not treat standing clone heterozygosity as Darwin 1876 inbreeding depression.
- Do not write Fisher 1918 as the 1930 geometric model.

Heterosis / hybrid vigor is on the candidate list but was not filled: no single named original distinct from filled Darwin 1876 inbreeding depression and the already-dropped overdominance split (Hull 1946 vs Dobzhansky 1950); Shull 1908 / 1914 pages were not opened; standing clone heterozygosity is not hybrid vigor.
Endosymbiotic gene transfer is on the candidate list but was not filled as a separate note: Timmis, Ayliffe, Huang and Martin 2004 Nat Rev Genet is a review; a Martin original was not opened; Sagan 1967 is organelle origin, not gene transfer.
Isolation by colonization is on the candidate list but was not filled as a second named original: Ramachandran et al. 2005 is the one serial-founder lock.
Soft vs hard selection (Wallace 1968 chapter / Wallace 1975 Evolution 29:465-473 / Christiansen 1975 Am Nat 109:11-16) is on the candidate list but was not filled: Wallace 1975 Evolution HTML was Cloudflare / timeout; Christiansen 1975 Am Nat HTML was not opened; the 1968 Lewontin-volume chapter was not opened.
Outcrossing depression / Bateson is on the candidate list but was not filled: Bateson 1909 was already dropped for the two-locus incompatibility claim; no distinct outbreeding-depression original was opened.
Phylogeography Avise is on the candidate list but was not filled: Avise et al. 1987 Annu Rev Ecol Syst is a review.
Vavilov centers / domestication syndrome is on the candidate list but was not filled: ESP TOC lists N. I. Vavilov 1932 "The Process of Evolution on Cultivated Plants" at p. 331; that PDF was not opened; Hammer 1984 was not used.

- Do not cite Dover 1982 as the concerted-evolution original (Zimmer 1980 is). This note is drive, a different job.
- Do not cite Timmis et al. 2004 or Nei and Rooney 2005 or Freeling 2009 as theory sources (reviews).
- Do not cite Eigen and Schuster 1977 as the quasispecies source (1971 is).
- Do not cite Lush 1937 as opened (it was not); Lande 1979 is the locked multivariate paper.
- Do not write Fisher 1930 geometric as Fisher 1918 infinitesimal.
- Do not write Wright 1932 as Wright 1931 island or Wright 1943 IBD.
- Do not write Holliday 1964 as Galtier 2001 gBGC.
- Do not write Sagan 1967 as Lynch 1996 organelle ratchet, or as EGT.
- Do not invent a grape Ewens, peak-shift, FGM, mutation-load-equilibrium, rDNA-drive, conversion-tract, quasispecies, serial-founder, G-matrix, or organelle-origin paper.
- Do not fill heterosis, EGT, isolation-by-colonization as a second original, soft vs hard selection, outcrossing depression, Avise phylogeography, or Vavilov / domestication syndrome this wave.

Heterosis / hybrid vigor is on the candidate list but was not filled: no single named original distinct from filled Darwin 1876 and dropped overdominance (Hull 1946 vs Dobzhansky 1950); Shull 1908 / 1914 pages were not opened; standing clone heterozygosity is not hybrid vigor.
Soft vs hard selection (Wallace 1968 chapter / Wallace 1975 Evolution 29:465-473 DOI 10.1111/j.1558-5646.1975.tb00836.x PMID 28563194 / Christiansen 1975 Am Nat 109:11-16 DOI 10.1086/282970) is on the candidate list but was not filled: Wallace 1975 EuropePMC HTML opened for author+year+venue this wave but carried no abstract or claim text; the 1968 Lewontin-volume chapter was not opened; Christiansen 1975 Chicago HTML was Cloudflare. Do not fill without quoting the hard/soft claim from an opened page.
Phylogeography Avise is on the candidate list but was not filled: Avise et al. 1987 Annu Rev Ecol Syst is a review.
Trivers 1974 parent-offspring conflict is on the candidate list but was not filled: not a genomics job for this skill.
Pritchard JK, Stephens M, Donnelly P. 2000. Inference of population structure using multilocus genotype data. Genetics 155(2):945-959. DOI 10.1093/genetics/155.2.945 PMID 10835412 PMC1461096. EuropePMC HTML opened (abstract names a model-based clustering method and software). DROP: method, not a named theory; this skill is not a methods bake-off.
Li and Durbin 2011 PSMC is on the candidate list but was not filled: too new, and a method, not a named original theory.
Lewontin 1974 The Genetic Basis of Evolutionary Change (Columbia) is on the candidate list but was not filled: book pages were not opened; the paradox-of-variation job would overlap filled Kimura 1968 / Lewontin-Hubby territory without a locked 1966 page.
Kimura 1983 The Neutral Theory of Molecular Evolution (book) was skipped: Kimura 1968 is already filled.
Crow and Kimura 1970 An Introduction to Population Genetics Theory was skipped: intro book, not a named original.
Gillespie 1991 The Causes of Molecular Evolution was skipped: Gillespie 2000 draft is already filled.
Charlesworth 1994 evolution of sex chromosomes was skipped: no 1994 paper of that title was found; 1991 Science 251:1030-1033 is a review. 1978 PNAS is the filled original.
Hudson 1990 Oxford Surveys coalescent chapter was skipped: survey; not opened. Hudson 2002 Bioinformatics ms was skipped: software method.
Mayr founder effect as a second named original was skipped: 1942 is the BSC lock; the founder-principle paper (often 1954) was not opened. Serial founder remains Ramachandran 2005.

- Do not cite Vavilov 1922 as this paper (homologous series; named in the 1932 facsimile but not opened).
- Do not cite Hammer 1984 as the centres source.
- Do not cite Price 1972 as the Price-equation source (1970 is).
- Do not cite Hamilton 1964 part II as the source (part I is the math).
- Do not cite Orr 2005 Nat Rev Genet as the adaptation source (review; 1998 is).
- Do not cite Charlesworth 1991 Science as the Y-degeneration source (review). Do not invent a 1994 Charlesworth sex-chromosome original.
- Do not write Mayr 1942 as Dobzhansky 1937 BDM or as Ramachandran 2005 serial founder. Do not write it as Mayr 1954 founder (not opened).
- Do not cite Hudson 1990 or Hudson 2002 as the HKA source.
- Do not cite Pritchard 2000 as a theory original (clustering method).
- Do not write Nei 1972 as Nei 1997 birth-and-death, or as Wright 1931 / Weir-Cockerham 1984.
- Do not write Weir-Cockerham 1984 as Wright 1931 island math.
- Do not write Orr 1998 as Fisher 1930 geometric or Fisher 1918 infinitesimal.
- Do not invent a grape Vavilov-centre, Price-equation, kin-selection, Nei-distance, FST-estimator, adaptive-walk, Y-degeneration, biological-species, or HKA paper.

Heterosis / hybrid vigor is on the candidate list but was not filled: no single named original distinct from filled Darwin 1876 and dropped overdominance (Hull 1946 vs Dobzhansky 1950); Shull 1908 Journal of Heredity os-4:296-301 DOI 10.1093/jhered/os-4.1.296 bibliographic lock only (Oxford 406 / timeout; Zenodo / CSHL PDF not opened); 1914 coinage first printed later (often 1922 / Shull 1948 Genetics 33:439-446 clarification). Standing clone heterozygosity is not hybrid vigor.
Soft vs hard selection (Wallace B. 1975. Evolution 29(3):465-473. DOI 10.1111/j.1558-5646.1975.tb00836.x PMID 28563194 / Christiansen FB. 1975. Am Nat 109:11-16. DOI 10.1086/282970 / Wallace 1968 Lewontin-volume chapter) is on the candidate list but was not filled: Wallace 1975 EuropePMC HTML opened this wave (author, Department of Genetics, Development, and Physiology, Cornell; 01 Sep 1975; Evolution 29(3):465-473; DOI; PMID) but carried no abstract or claim text; Christiansen 1975 Crossref JSON opened (Freddy Bugge Christiansen; The American Naturalist 109(965):11-16; 1975-01; DOI) with no abstract; 1968 chapter not opened. Do not fill without quoting the hard/soft claim from an opened page.
Mayr founder effect / genetic revolution (Mayr E. 1954. Change of genetic environment and evolution. Pp. 157-180 in Huxley J, Hardy AC, Ford EB, eds. Evolution as a Process. Allen and Unwin, London) is on the candidate list but was not filled: Ridley classic-texts HTML opened (title, 1954, Huxley/Hardy/Ford, pp. 157-180) but the chapter PDF timed out; 1942 remains the BSC lock. Serial founder remains Ramachandran 2005.
Charlesworth 1991 Science 251:1030-1033 was skipped: tagged review; 1978 PNAS is the filled Y-degeneration original.
Slatkin M. 1987. Gene flow and the geographic structure of natural populations. Science 236(4803):787-792. DOI 10.1126/science.3576198 PMID 3576198. EuropePMC HTML opened (abstract is a review of direct and indirect gene-flow methods). DROP: review; 1985 is the lock.
Wright S. 1951. The genetical structure of populations. Ann Eugen 15(4):323-354 (Wiley / Crossref also print January 1949, vol. 15 issue 1, same pages). DOI 10.1111/j.1469-1809.1949.tb02451.x PMID 24540312. EuropePMC HTML opened (author, 01 Mar 1951, 15(4):323-354, DOI, PMID) but no abstract or claim text. Wiley Cloudflare. DROP without a quoted FIS/FIT/FST claim. Wright 1965 Evolution 19:395-420 DOI 10.1111/j.1558-5646.1965.tb01731.x likewise not opened for claim text. 1931 remains island math; 1943 remains IBD; 1984 remains the estimator.
Beaumont MA, Nichols RA. 1996. Evaluating loci for use in the genetic analysis of population structure. Proc R Soc Lond B 263:1619-1626. DROP: method, not a named theory; Lewontin-Krakauer 1973 is the lock.
Hudson 1990 Oxford Surveys in Evolutionary Biology 7:1-44 was skipped: survey chapter; not a named original. Hudson 2002 ms remains a software method.
Muller HJ. 1950. Our load of mutations. Am J Hum Genet 2(2):111-176. PMID 14771033 PMCID PMC1716299. PMC / EuropePMC HTML opened (title, June 1950, 2(2):111-176, PMID, PMC) but no abstract or body. DROP as source; Crow 1958 is the lock. Morton, Crow and Muller 1956 PNAS 42:855-863 DOI 10.1073/pnas.42.11.855 PMID 16589958 PMC528351 opened as bibliographic only; not used as the source.
Stebbins 1950 Variation and Evolution in Plants was skipped: 1947 Adv Genet is already filled as allopolyploidy.
Grant V. 1981. Plant Speciation. 2nd ed. Columbia University Press. Not opened; later synthesis. Not filled.
Rieseberg hybrid speciation was not filled: Rieseberg 1997 Annu Rev Ecol Syst is a review; no named original locked. Abbott hybrid-speciation reviews were skipped.
Barton and Hewitt 1985 Analysis of hybrid zones. Annu Rev Ecol Syst 16:113-148 is a review. 1979 is the lock.

- Do not cite Slatkin 1987 Science as the gene-flow source (review; 1985 is).
- Do not cite Slatkin 1981 as the private-allele source (qualitative precursor).
- Do not cite Barton and Hewitt 1985 Annu Rev as the hybrid-zone source (review; 1979 is).
- Do not cite Beaumont and Nichols 1996 as the FST-outlier source (method; 1973 is).
- Do not cite Fu 1997 as the Fay-Wu or Fu-Li source.
- Do not cite Muller 1950 as the genetic-load source (landing only; no body). Do not cite Morton, Crow and Muller 1956 as this paper.
- Do not write Crow 1958 as Haldane 1957 cost or Haldane 1927 equilibrium q or Muller 1964 ratchet.
- Do not write Slatkin 1993 as Wright 1943 IBD, or as Slatkin 1985 private alleles.
- Do not write Endler 1977 as Wright 1943 or as Barton 1979.
- Do not write Fay-Wu 2000 as Maynard Smith and Haigh 1974 or as Tajima 1989.
- Do not write Fu-Li 1993 as Tajima 1989.
- Do not write Lewontin-Krakauer 1973 as Wright 1931 / 1943 or as Weir-Cockerham 1984.
- Do not invent a grape FST-outlier, Fay-Wu, Fu-Li, private-allele, pairwise-M, hybrid-zone, cline, or genetic-load paper.

Wright S. 1951. The genetical structure of populations. Ann Eugen 15(4):323-354 (also printed 1949). DOI 10.1111/j.1469-1809.1949.tb02451.x PMID 24540312. Wright 1965 Evolution 19:395-420 DOI 10.1111/j.1558-5646.1965.tb01731.x. Still no claim text. DROP. 1931 remains island math; 1943 remains IBD; 1984 remains the estimator.
Slatkin M. 1987. Gene flow and the geographic structure of natural populations. Science 236(4803):787-792. DOI 10.1126/science.3576198 PMID 3576198. Review. DROP. 1985 is the lock.
Mayr E. 1954. Change of genetic environment and evolution. Pp. 157-180 in Huxley J, Hardy AC, Ford EB, eds. Evolution as a Process. Allen and Unwin, London. Chapter PDF still not opened. 1942 remains the BSC lock. Serial founder remains Ramachandran 2005.
Muller HJ. 1950. Our load of mutations. Am J Hum Genet 2(2):111-176. PMID 14771033 PMC1716299. Body still not opened. Crow 1958 remains the load lock.
Barton NH, Hewitt GM. 1985. Analysis of hybrid zones. Annu Rev Ecol Syst 16:113-148. Review. 1979 and 1983 are the locks.
Fisher RA. 1937. The wave of advance of advantageous genes. Ann Eugen 7(4):355-369. DOI 10.1111/j.1469-1809.1937.tb02153.x. Wiley HTML opened as a historical-archive disclaimer only (no scientific abstract). Adelaide digital-library PDF 404. DROP without a quoted wave-of-advance claim from an opened page.
Kolmogorov AN, Petrovsky IG, Piscounov NS. 1937. KPP travelling-wave equation. Russian original not opened. DROP.
Stephan W, Wiehe THE, Lenz MW. 1992. The effect of strongly selected substitutions on neutral polymorphism: analytical results based on diffusion theory. Theor Popul Biol 41(2):237-254. DOI 10.1016/0040-5809(92)90045-U. ScienceDirect HTML timed out; no EuropePMC / PMID page opened this wave. DROP. Kaplan 1989 is the coalescent-hitchhiking lock.
Nielsen R. 2005. Molecular signatures of natural selection. Annu Rev Genet 39:197-218. Methods / review. Skip.
Voight BF, Kudaravalli S, Wen X, Pritchard JK. 2006. A map of recent positive selection in the human genome. PLoS Biol 4(3):e72. iHS method. Skip.
Sabeti PC et al. 2002. Detecting recent positive selection in the human genome from haplotype structure. Nature 419:832-837. EHH method. Skip.
Pritchard JK, Pickrell JK, Coop G. 2010. The genetics of human adaptation: hard sweeps, soft sweeps, and polygenic adaptation. Curr Biol 20(4):R208-R215. DOI 10.1016/j.cub.2009.11.055 PMID 20178769 PMC2994553. Tagged review on publisher / PMC pages. DROP. Hermisson 2005 remains the soft-sweep lock; Berg and Coop 2014 is the polygenic lock.
Coop G et al. 2009. The role of geography in human adaptation. Not opened as a named original this wave. Not filled.
Boyle EA, Li YI, Pritchard JK. 2017. An expanded view of complex traits: from polygenic to omnigenic. Cell 169(7):1177-1186. DOI 10.1016/j.cell.2017.05.038 PMID 28622505 PMC5536862. EuropePMC HTML opened and tagged Review. DROP.
Mackay TFC. 2001. Quantitative trait loci in Drosophila. Nat Rev Genet 2(1):11-20. DOI 10.1038/35047544 PMID 11253063. Review. DROP.
Falconer DS. Introduction to Quantitative Genetics (book). No specific chapter opened this wave. Not filled. Fisher 1918 remains the infinitesimal lock; Lande 1979 remains the multivariate-response lock.
Heterosis / hybrid vigor remains unfilled: Shull 1908 / 1914 pages still not opened; Darwin 1876 already filled; standing clone heterozygosity is not hybrid vigor.

- Do not cite Fisher 1937 as the cline source (wave-of-advance claim text not opened).
- Do not cite Kolmogorov / KPP 1937 as the source (not opened).
- Do not cite Stephan, Wiehe and Lenz 1992 as the hitchhiking source (page not opened).
- Do not cite Pritchard, Pickrell and Coop 2010 Curr Biol as the polygenic-adaptation source (review; 2014 is).
- Do not cite Boyle, Li and Pritchard 2017 as the omnigenic / polygenic source (tagged review).
- Do not cite Barton and Hewitt 1985 Annu Rev as the tension-zone or multilocus-cline source (review; 1968 / 1979 / 1983 are).
- Do not write Key 1968 as Barton 1979 dynamics, or Barton 1983 as Barton 1979.
- Do not write Haldane 1948 as Endler 1977 or as Wright 1943 IBD.
- Do not write Slatkin 1973 as Slatkin 1985 private alleles or as Slatkin 1993 pairwise M.
- Do not write Nagylaki 1975 as Haldane 1948 slope.
- Do not write Kaplan 1989 as Maynard Smith and Haigh 1974 or as Charlesworth 1993 BGS or as Fay-Wu 2000.
- Do not write Braverman 1995 as Tajima 1989 or as Kaplan 1989.
- Do not write Berg-Coop 2014 as Hermisson 2005 or as Fisher 1918.
- Do not write Rockman 2012 as Fisher 1918.
- Do not invent a grape cline, tension-zone, hitchhiking-SFS, polygenic-adaptation, or QTN-catalog paper.

Fisher RA. 1937. The wave of advance of advantageous genes. Ann Eugen 7(4):355-369. DOI 10.1111/j.1469-1809.1937.tb02153.x. Wiley HTML still a historical-archive disclaimer (no scientific abstract). Adelaide digital-library item page bibliographic (Fisher; 1937; Annals of Eugenics 7:355-369); PDF 404. DROP without a quoted wave-of-advance claim from an opened page.
Kolmogorov AN, Petrovsky IG, Piscounov NS. 1937. KPP travelling-wave equation. Russian original not opened. DROP.
Stephan W, Wiehe THE, Lenz MW. 1992. The effect of strongly selected substitutions on neutral polymorphism: analytical results based on diffusion theory. Theor Popul Biol 41(2):237-254. DOI 10.1016/0040-5809(92)90045-U. ScienceDirect HTML 403 / timeout; Semantic Scholar no abstract; no EuropePMC abstract page. DROP. Kaplan 1989 remains the coalescent-hitchhiking lock.
Barton NH. 2000. Not opened as a named original this wave. 1986 papers are the locks.
Slatkin M, Maruyama T. 1975. Genetic drift in a cline. Genetics 81(1):209-222. Not opened as the lock; 1975 two-locus paper is the lock.
Malecot G. 1948. Les mathematiques de l'heredite. Masson. English 1969 Freeman translation (Yermanos). Book; no lockable claim page opened. Wright 1943 remains IBD. DROP.
Hewitt GM. 1988. Hybrid zones-natural laboratories for evolutionary studies. Trends Ecol Evol 3(7):158-167. DOI 10.1016/0169-5347(88)90033-X PMID 21227192. Review. Skip. 1968 / 1979 / 1983 / 1986 are the locks.
Haldane JBS. 1932. The Causes of Evolution. Longmans / Princeton reprints. Book; no specific chapter opened this wave. Not filled.
Pannell JR, Charlesworth B. 2000. Effects of metapopulation processes on measures of genetic diversity. Philos Trans R Soc Lond B. Review. Skip. Wade 1988 is the extinction-recolonization lock.
Harrison RG. 1993. Hybrid zones and the evolutionary process (book / review). Skip unless a lockable original paper; none opened.
Wright S. 1951 / 1965 F-statistics. Still no claim text. 1931 remains island math; 1943 remains IBD; 1984 remains the estimator.

- Do not cite Fisher 1937 as the wave-of-advance source (claim text still not opened).
- Do not cite Kolmogorov / KPP 1937 as the source (not opened).
- Do not cite Stephan, Wiehe and Lenz 1992 as the hitchhiking source (page not opened; Kaplan 1989 is the lock).
- Do not cite Hewitt 1988 TREE as the hybrid-zone source (review).
- Do not cite Pannell and Charlesworth 2000 as the extinction-recolonization source (review; Wade 1988 is).
- Do not cite Harrison 1993 as a hybrid-zone original (review).
- Do not cite Malecot 1948 / 1969 as the IBD source (book not opened; Wright 1943 remains).
- Do not cite Haldane 1932 The Causes of Evolution as a filled original (chapter not opened).
- Do not write Rousset 1997 as Wright 1943 or as Slatkin 1993.
- Do not write Excoffier 1992 as Weir-Cockerham 1984.
- Do not write Wade 1988 as Levins 1969 occupancy, or Whitlock 1992 as Wade 1988.
- Do not write Slatkin 1975 two-locus as Slatkin 1973 characteristic length or as Barton 1983 coupling.
- Do not write Barton-Bengtsson 1986 as Barton 1979 or as Barton 1983, or Barton 1986 hybrid-sink as Barton-Bengtsson 1986.
- Do not write Kimura 1955 as Kimura 1968 or as Kingman 1982 or as Kimura-Weiss 1964.
- Do not write VviAGL11 as the sex locus (Dong 2023 chromosome-2 SDR).
- Do not invent a grape IBD, AMOVA, metapopulation-FST, two-locus-cline, hybrid-barrier, or drift-trajectory paper.

Fisher RA. 1937. The wave of advance of advantageous genes. Ann Eugen 7(4):355-369. DOI 10.1111/j.1469-1809.1937.tb02153.x. Wiley HTML still a historical-archive disclaimer (no scientific abstract). DROP without a quoted wave-of-advance claim from an opened page.
Kolmogorov AN, Petrovsky IG, Piscounov NS. 1937. KPP travelling-wave equation. Russian original not opened. DROP.
Stephan W, Wiehe THE, Lenz MW. 1992. The effect of strongly selected substitutions on neutral polymorphism: analytical results based on diffusion theory. Theor Popul Biol 41(2):237-254. DOI 10.1016/0040-5809(92)90045-U. ScienceDirect HTML Cloudflare-blocked this wave; no EuropePMC abstract page opened. DROP. Kaplan 1989 remains the coalescent-hitchhiking lock.
Barton NH. 2000. Genetic hitchhiking. Philos Trans R Soc Lond B 355:1553-1562. DOI 10.1098/rstb.2000.0716 PMID 11127900. Tagged Review. DROP. Maynard Smith and Haigh 1974 remains the hitchhiking lock.
Jukes TH, Cantor CR. 1969. Evolution of protein molecules. In Munro HN (ed.) Mammalian Protein Metabolism vol. III, pp. 21-132. Academic Press. Book chapter; no lockable claim page opened. Kimura 1980 is the nucleotide-distance lock. DROP.
Wright S. 1951 / 1949. The genetical structure of populations. Ann Eugen 15:323-354. DOI 10.1111/j.1469-1809.1949.tb02451.x PMID 24540312. Wiley HTML still a historical-archive disclaimer; no scientific claim text. 1931 remains island math; 1943 remains IBD; 1984 remains the estimator. DROP.
Sabeti PC et al. 2002. Detecting recent positive selection in the human genome from haplotype structure. Nature 419:832-837. DOI 10.1038/nature01140 PMID 12397357. Method (EHH / long-range haplotype scan). Skip. Maynard Smith and Haigh 1974 remains hitchhiking.
Andolfatto P. 2005. Adaptive evolution of non-coding DNA in Drosophila. Nature 437:1149-1152. DOI 10.1038/nature04107. Nature HTML opened (author, 2005, Nature 437:1149-1152, DOI, abstract: MK extension to non-coding DNA). DROP as a named theory: empirical result using filled MK 1991, not a new original. MK remains the lock.
Rieseberg LH. 1997. Hybrid origins of plant species. Annu Rev Ecol Syst 28:359-389. Review. Skip. 2003 is the lock.
Malecot G. 1948 / 1969 isolation. Book; no lockable claim page. Wright 1943 remains IBD.

- Do not cite Fisher 1937 as the wave-of-advance source (claim text still not opened).
- Do not cite Kolmogorov / KPP 1937 as the source (not opened).
- Do not cite Stephan, Wiehe and Lenz 1992 as the hitchhiking source (page not opened; Kaplan 1989 is the lock).
- Do not cite Barton 2000 as a hitchhiking original (review; Maynard Smith and Haigh 1974 is the lock).
- Do not cite Jukes and Cantor 1969 as the nucleotide-distance source (book chapter not opened; Kimura 1980 is the lock).
- Do not cite Wright 1951 / 1965 as the F-statistics source (no claim text; 1931 / 1943 / 1984 remain).
- Do not cite Sabeti 2002 as a named theory (method; skip).
- Do not cite Andolfatto 2005 as a named theory original (empirical MK extension; MK 1991 remains).
- Do not cite Rieseberg 1997 Annu Rev as the hybrid-speciation source (review; 2003 is the lock).
- Do not write Nei 1973 GST as Nei 1972 distance or as Weir-Cockerham 1984.
- Do not write Slatkin 1981 as Slatkin 1985 private alleles or as Slatkin 1993 pairwise M.
- Do not write Slatkin and Maruyama 1975 as Slatkin 1975 two-locus or as Slatkin 1973 characteristic length.
- Do not write Nei 1978 as Nei 1972.
- Do not write Kimura 1980 as Kimura 1968 or as Zuckerkandl-Pauling.
- Do not write Tajima and Nei 1984 as Tajima 1989 D or as Kimura 1980.
- Do not write Begun and Aquadro 1992 as Maynard Smith and Haigh 1974 or as Charlesworth 1993 BGS.
- Do not write Ohta 1972 as Ohta 1973.
- Do not write Barton and de Cara 2009 as Dobzhansky 1940 or as Barton 1983.
- Do not write Rieseberg 2003 as Anderson 1949.
- Do not write VviAGL11 as the sex locus (Dong 2023 chromosome-2 SDR).
- Do not invent a grape GST, conditional-frequency, drift-cline, unbiased-distance, K80, Tajima-Nei-distance, recombination-diversity, nearly-neutral-precursor, isolation-coupling, or hybrid-speciation paper.

Jukes TH, Cantor CR. 1969. Evolution of protein molecules. In Munro HN (ed.) Mammalian Protein Metabolism vol. III, pp. 21-132. Academic Press. Book chapter; no lockable claim page opened. Kimura 1980 remains the nucleotide-distance lock. DROP.
Kimura M, Ohta T. 1971. Protein polymorphism as a phase of molecular evolution. Nature 229(5285):467-469. DOI 10.1038/229467a0 PMID 4925204. EuropePMC HTML opened this wave; no abstract / no claim text. DROP.
Tajima F. 1993. Measurement of DNA polymorphism. Book chapter / later methods paper; no lockable claim page opened this wave. Tajima 1983 is the lock. DROP.
Fay JC, Wyckoff GJ, Wu CI. 2001. Positive and negative selection on the human genome. Genetics 158(3):1227-1234. DOI 10.1093/genetics/158.3.1227 PMID 11454770. Search listing opened; empirical MK extension to genomic data, not a named theory original. MK 1991 remains. DROP.
Fay JC, Wyckoff GJ, Wu CI. 2002. Testing the neutral theory of molecular evolution with genomic data from Drosophila. Nature 415(6875):1024-1026. DOI 10.1038/4151024a PMID 11875569. Search listing opened; empirical MK extension. MK 1991 remains. DROP.
Stephan W, Wiehe THE, Lenz MW. 1992. The effect of strongly selected substitutions on neutral polymorphism: analytical results based on diffusion theory. Theor Popul Biol 41(2):237-254. DOI 10.1016/0040-5809(92)90045-U. Still no lockable abstract page this wave. DROP. Kaplan 1989 remains the coalescent-hitchhiking lock; Wiehe and Stephan 1993 is the lock for alpha v.
Gillespie JH. 1991. The Causes of Molecular Evolution. Oxford University Press. Book. Skip.
Gillespie JH. 1994. Substitution processes in molecular evolution. III. Deleterious alleles. Genetics 138(3):943-952. DOI 10.1093/genetics/138.3.943 PMID 7851786. Paper exists (house-of-cards / deleterious substitutions); not draft-adjacent. Gillespie 2000 remains the draft lock. DROP this wave.
Orr HA. 2005. Dobzhansky-Muller / speciation review or later paper. Not opened. 1995 is the snowball lock. DROP.
Coyne JA, Orr HA. 1997. Patterns of speciation in Drosophila revisited. Evolution 51:295-303. Revisit. 1989 is the lock. DROP.
Grant V. 1981. Plant Speciation. Book. Skip.
Arnold ML. 1997 / 2006. Hybridization books. Skip.
Mallet J. 2007. Hybrid speciation. Nature 446:279-283. Review dump. Skip. Rieseberg 2003 remains the complementary-gene hybrid-speciation lock.
Abbott R et al. 2013. Hybridization and speciation. J Evol Biol. Review. Skip.
Soltis DE / Soltis PS. 2009 / 2015 polyploidy papers. Not opened as a distinct original this wave. Stebbins 1947 and Thomas-Freeling 2006 remain. DROP.
Comai L. 2005. The advantages and disadvantages of being polyploid. Nat Rev Genet 6(11):836-846. DOI 10.1038/nrg1711 PMID 16304599. Tagged Review. DROP.
Otto SP, Whitton J. 2000. Polyploid incidence and evolution. Annu Rev Genet. Review. Skip.
Wright S. 1938. Size of population and breeding structure in relation to evolution. Science 87:430-431. Short letter; no lockable claim page opened. Wright 1931 remains island / Ne math. DROP.
Crow JF, Kimura M. 1970. An Introduction to Population Genetics Theory. Book. Skip.

- Do not cite Jukes and Cantor 1969 as the nucleotide-distance source (book chapter not opened; Kimura 1980 remains).
- Do not cite Kimura and Ohta 1971 Nature as the polymorphism-phase source (no claim text).
- Do not cite Tajima 1993 as the nucleon-genealogy source (not opened; 1983 is the lock).
- Do not cite Fay, Wyckoff and Wu 2001 / 2002 as a named theory (empirical MK; MK 1991 remains).
- Do not cite Stephan, Wiehe and Lenz 1992 as the hitchhiking source (page not opened; Kaplan 1989 remains).
- Do not cite Gillespie 1991 / 1994 as the draft source (book / house-of-cards; Gillespie 2000 remains).
- Do not cite Orr 2005 as the snowball source (not opened; 1995 is the lock).
- Do not cite Coyne and Orr 1997 as the time-course source (revisit; 1989 is the lock).
- Do not cite Grant 1981, Arnold 1997 / 2006, Mallet 2007, Abbott 2013, Comai 2005, Otto and Whitton 2000, or Crow and Kimura 1970 as theory originals (book or review).
- Do not cite Wright 1938 as the effective-size source (letter; no claim text; Wright 1931 remains).
- Do not write Nei and Li 1979 as Nei 1972 / 1973 / 1978 or as Tajima 1989.
- Do not write Tajima 1983 as Tajima 1989 D or as Tajima-Nei 1984.
- Do not write Kimura and Ohta 1969 as Kimura 1968 or as Ohta 1972 / 1973.
- Do not write Charlesworth 1994 as Charlesworth 1993.
- Do not write Hudson and Kaplan 1995 as Charlesworth 1993 or as Kaplan 1989 hitchhiking.
- Do not write Nordborg 1996 as Charlesworth 1993 or as Hudson-Kaplan 1995.
- Do not write Wiehe and Stephan 1993 as Maynard Smith and Haigh 1974 or as Begun-Aquadro 1992.
- Do not write Orr 1995 as Dobzhansky 1937 or as Orr 1998 or as Rieseberg 2003.
- Do not write Turelli and Orr 1995 as Haldane 1922.
- Do not write Coyne and Orr 1989 as Dobzhansky 1940 or as Mayr 1942.
- Do not write VviAGL11 as the sex locus (Dong 2023 chromosome-2 SDR).
- Do not invent a grape nucleotide-diversity, nucleon-genealogy, 4Ne, BGS-on-selected, BGS-with-recombination, BGS-map, alpha-v hitchhiking, snowball-incompatibility, Haldane-dominance, or isolation-time-course paper.

Related: `plant-lit-review`, `vitis-popgen`, `grapevine-adna`, `vitis-pangenome`.
