# Getting started with SISA-KiT

## What is SISA-KiT?
SISA-KiT (Signaling Inspired Synthetically Augmented Kinase Toolkit) is an approach that uses a domain-motif interaction to target a constitutively active tyrosine kinase to a substrate protein of interest to produce recombinant, tyrosine phosphorylated protein. In theory, any enzymatic interaction can replace the tyrosine kinase of interest and any protein target can be used. 

SISA-KiT requires two vectors, engineered to be co-transformed, independently selected, and independently induced in E. coli production systems. In theory, you can move the domain-enzyme fusion and motif-substrate components to any expression system! However, since E. Coli produces a large amount of protein very easily, all our documentation and vectors are currently focused on those systems. 

In the current SISA-KiT, targeting of the kinase to a substrate occurs between an SH3 domain (from ABL) and a polyproline sequence that SH3 domain recognizes. You can change the targeting strength by selecting a different polyproline sequence.

![SISA-KiT two-vector system](Images/vectors_overview_rx.png)

## How do I get started use SISA-KiT for making phosphoproteins?
It's very easy to get started! Our substrate vectors contain common cloning restriction sites and you select your vector(s), clone your substrate, screen for well performing reaction kinases, and optimize for specific product yield (including reaction types).

## What does a reaction look like in SISA-KiT?
We have three types of ways you can produce recombinant, phosphoprotein using SISA-KIT. These are referred to as co-expression, serial induction, and in vitro reactions. Where possible, we recommend using co-expression (simultaneously induce the substrate and kinase) which tends to produce larger yields of both protein and phosphoprotein. If you require phosphorylation occur after protein folding has occurred, you can use serial induction -- produce the subsrate protein first and then turn on the kinase. Finally, if you wish to couple kinases or move outside an E. coli system, you can use an in vitro approach -- make the substrate protein on its own and during the process of purification, resuspend the beads/matrix in kinase-expressing E. coli lysate supplemented in a magnesium- and ATP-rich buffer, then continue washing and elution as usual. 

![SISA-KiT reaction types](Images/reaction_types.png)


## What does the kit contain? 
### Kinases
We have provided 9 kVh-vectors, SH3-fused tyrosine kinases from a wide variety of specifciities that express and perform well in recombinant E. coli systems. All kinases span the catalytic domain only, unless otherwise noted. The kVh system is a highly modified pBAD backbone, retaining L-arabinose based control of kinase induction, but with alternate origins of replication (p15a) and resistance selection (kanamycin), allowing them to be compatible with the substrate vector. These kinases include:
* kVh-ABL
* kVh-EPHB1
* kVh-EPHB2
* kVh-FES
* kVh-FGFR3
* kVh-MERTK
* kVh-EPHA4
* kVh-LYN (contains LYN SH2 domain)
* kVh-SRC (contains SRC SH2 domain)

### Substrate vectors
We have made a variety of substrate vectors that provide the opportunity to use different fusions for the purpose of solubility, detection, purfication, or other purposes. All substrate vectors have induction control under lac-control (lactose/IPTG). We have two main substrate backbones in the toolkit, sVd - a highly modified pGEX (GST removed, and a tyrosine-free yeast sumo domain added for solubility) and a pET vector. All substrates include a C-terminal MYC and 6xHis fusion for detection and purification and at least one version of a targeting sequence. 

#### Polyproline sequences defined
Binding affinity provided based on publication from [Pisabarro et al., JMB 1998](https://pubmed.ncbi.nlm.nih.gov/9698566/)
* no PxxP - there is no targeting sequence
* 3BP1: APTMPPPLPP (34 &mu;M)
* 3BP2: PPAYPPPPVP (5 &mu;M)
* p41:  APSYSPPPPP (1.5 &mu;M)
* p40:  APTYSPPPPP (0.4 &mu;M)
* p40F: APTFSPPPPP (p40 with tyrosine to phenylalanine mutation)
* p40W: APTWSPPPPP (p40 with tyrosine to tryptophan mutation)

#### Substrate vector options
* sVd
* sVd-Avi
* sVd-ALFA
* sVd-mGST
* pET-Halo-GB1
* pET-SUMO-Fh8
* pET-Halo-Fh8
* pET-SUMO-GB1

| Substrate vector | N-terminal fusions | C-terminal fusions | Cleavage sites | 5' restriction sites | 3' restriction sites | Targeting options |
| --- | --- | --- | --- | --- | --- | --- |
| sVd | msmt3-PxxP | MYC, 6xHis | Prescission (after targeting sequence) | BamHI/HindIII | SacII/SalI/XhoI/NotI | No PxxP, 3BP1, 3BP2, p41, p40, p40W |
| sVd-Avi | msmt3-PxxP | AviTag, MYC, 6xHis | Prescission (after targeting sequence) | BamHI | SacII/SalI/XhoI/NotI | p40, p40W |
| sVd-ALFA | ALFA-tag | MYC, 6xHis | TBD | TBD | TBD | p40W |
| sVd-mGST | msmt3-PxxP-Gly linker | GSTm, MYC, 6xHis | TBD | BamHI/AflII | Eco53kI/SacI | p40, p40W |
| pET-Halo-GB1 | HaloTag-PxxP | GB1, MYC, 6xHis | Prescission (after targeting sequence) | EcoRI/BamHI | SacI/SacII/HindIII | p40F |
| pET-SUMO-Fh8 | SUMO-PxxP | Fh8, MYC, 6xHis | Prescission (after targeting sequence) | EcoRI/BamHI | SacI/SacII/HindIII | p40F |
| pET-Halo-Fh8 | HaloTag-PxxP | Fh8, MYC, 6xHis | Prescission (after targeting sequence) | EcoRI/BamHI | SacI/SacII/HindIII | p40F |
| pET-SUMO-GB1 | SUMO-PxxP | GB1, MYC, 6xHis | Prescission (after targeting sequence) | EcoRI/BamHI | SacI/SacII/HindIII | p40F |

#### Tag definitions
For use in SISA-KiT we use tags, fusions, and components that are tyrosine free. We do this by selecting sequences with low to no tyrosines and replace tyrosines with non-phosphorylatable matches to phenylalanines. 

* msmt3 - the yeast sumo domain (smt3) where we have mutated all tyrosines to phenylalanines
* MYC - an epitope for detection (EQKLISEEDL) 
* 6xHis - a repeat of 6 histidines for use in purification using metal affinity chromotography.
* GSTm - the GST tag where all tyrosines are mutated to phenylalanines. This tag is used as an inert fusion to increase size for peptide vectors. GSTm does not work for puriciation. DNA was codon optimized for E. coli expression.
* ALFA-tag - 15 amino acid epitope tag that forms a stable alpha-helix for use in tagging, purification, or detection. The sequence is SRLEEELRRRLTE, DNA was codon optimized for expression in E. coli
* Halo-tag - the 33kDa Halo tag, used for protein labeling. 
* AviTag - for biotinylation, this 15 amino acid sequence (GLNDIFEAQKIEWHE) is selected by BirA ligase for site-specific biotinylation. 
* SUMO - this is the human SUMO2 sequence, where the two tyrosines are mutated to phenylalanines and the codons were optimized for E. coli production.
* Fh8 - for solubility, this sequence is: MPSVQEVEKLLHVLDRNGDGKVSAEELKAFADDSKCPLDSNKIKAFIKEHDKNKDGKLDLKELVSILSS. DNA was codon optimized for E. coli expression.
* GB1 - this 6kDa protein is extremly stable and excellent for increasing yield, all three tyrosines are mutated to phenylalanines. 




