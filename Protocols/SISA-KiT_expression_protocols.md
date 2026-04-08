# Overview
This document covers the logistics of producing phosphoprotein using the synthetic toolkit. This assumes you have selected your substrate backbone and you have a selected kinase. See other areas for setting up to find these approaches.  

There are three main ways to use the SISA-KiT for producing phosphoproteins in recombinant E. Coli systems. These are referred to as:
1. Co-Expression (you co-induce kinase and substrate at the same time)
2. Serial Induction (you first produce substrate, allowing it to create enough folded protein, then come in with a second induction of kinase)
3. In Vitro Reactions (during the process of purification of the substrate, you incubate protein beads with kinase-containing lysate, using an in vitro approach).

## Tips and Tricks
Co-expression has almost always been shown to be superior for phosphoprotein yield and is especially useful for multisite phosphorylation. However, in those cases where phosphorylation of a folded protein might result in misfolding and increased protein insolubility, then serial induction can help overcome that. Finally, in vitro reactions are very low efficiency (compared to co- and serial-induction), but the toolkit is still significantly cheaper and easier than requiring a recombinant kinase. In this case, we are able to induce kinase in a single E. Coli (typically a 10Beta background), lyse it in a magnesium- and ATP-rich buffer and then incubate the lysate with substrate-bound beads (no kinase purification is required). Following incubation, washes and elution continue for the substrate. 

# Co-expression
Follow the base innoculation protocol and at induction time, add both IPTG and L-arabinose. Typically we use 0.5mM IPTG and 0.5% L-arabinose. Induction times are best for 4 hours at 37C or overnight at 18C. 

# Serial Induction
Follow the base innoculation protocol. Add IPTG and induce overnight at 18C, the next morning move the culture to 37C and add L-arabinose for 4 hours. 

# In vitro kinase Reactions
Follow the process
