# CTCF-Motif-Interaction-Directionality
Analysis of directionality bias of CTCF motifs in Hi-C interactions.

Recent work in mammalian genomes has revealed an important function of CTCF binding sites as unidirectional borders to cohesin-mediated loop extrusion. CTCF sites are thought to obstruct the movement of loop-forming cohesin-motors on the DNA in one direction but not the other based on the orientation or strand of the CTCF motif. The primary consequence of this activity is significant looping interactions between convergently oriented CTCF binding sites, visible in Hi-C matrices as enriched points. However, determining the existence of this looping phenomenon in a given genome is challenging as several phenomena can produce punctate enrichments in interaction frequency in Hi-C matrices. Additionally, not all CTCF sites appear to loop, their loops are not always visible due to noise in the Hi-C matrix, and motif-calling to identify CTCF binding sites and their directionality is also not very accurate. These problems are all exacerbated when examining model organisms which tend to have noisier Hi-C data sets, ore fragmented genome assemblies, and potentially divergent CTCF motifs. 

To determine whether CTCF acts as a unidirectional border and forms loops then it is useful to instead query the border activity of CTCF sites rather than attempting to identify the point loops they form. When CTCF acts as a unidirectional border is has a strong orientation bias in its interactions. A CTCF site can have double the Hi-C interactions in its forward orientation over its reverse. So to ascertain CTCF's orientation bias in a given genome we can simply tally the interactions from all identified CTCF motifs in the genome and determine whether there exists an orientation bias in these interactions. With this method even if the genome assembly, Hi-C data, and CTCF identification are all low-quality the meta-analysis of all CTCF sites should provide enough statistical power to detect the orientation bias.

Here we use this method to examine CTCF's orientation bias in humans and in the fruit fly Drosophila melanogaster. The human CTCF it shows strong orientation bias while in Drosophila CTCF does not have oriented interaction biases. This finding is surprising due to despite previous work identifying CTCF as an important architectural protein in the fruit fly genome and the relative conservation of CTCF and its binding motif between flies and humans.

<img src="https://github.com/5centmike/CTCF-Motif-Interaction-Directionality/blob/main/ctcf-human-drosophila.png" width="500">

How CTCF acts as a unidirectional border and what purpose this serves in the architectural regulation of the genome is still poorly understood. We may gain some insight into the function of CTCF looping by determining its evolutationary origins. To this end this pipeline is intende4d to perform this directionality analysis on any assembled genome with Hi-C data. To begin with we attempt to identify CTCF motifs using the FIMO tool from the MEME software suite. We search for the CTCF motif as well as 4 suffled motifs with theame base-composition as the CTCF motif. The examples shown below are from the genome of Strongylocentrotus purpuratus, the purple sea urchin.

<img src="https://github.com/5centmike/CTCF-Motif-Interaction-Directionality/blob/main/StrongylocentrotusCMFA.png" width="500">

Enrichment for the CTCF motif over other motifs with the same base-content in a different order suggests that this motif is conserved and likely still represents the binding site of CTCF in this organism. The randomly shuffled sequences will be used in the directionality analysis as negative controls.

<img src="https://github.com/5centmike/CTCF-Motif-Interaction-Directionality/blob/main/StrongCTCFDistPlot.png" width="400"><img src="https://github.com/5centmike/CTCF-Motif-Interaction-Directionality/blob/main/StrongSH4DistPlot.png" width="400">

<img src="https://github.com/5centmike/CTCF-Motif-Interaction-Directionality/blob/main/StrongCTCFBoxPlot.png" width="400"><img src="https://github.com/5centmike/CTCF-Motif-Interaction-Directionality/blob/main/StrongSH4BoxPlot.png" width="400">
