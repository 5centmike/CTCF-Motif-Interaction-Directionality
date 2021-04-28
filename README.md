# CTCF-Motif-Interaction-Directionality
Analysis of directionality bias of CTCF motifs in Hi-C interactions.

Recent work in mammalian genomes has revealed an important function of CTCF binding sites as unidirectional borders to cohesin-mediated loop extrusion. CTCF sites are thought to obstruct the movement of loop-forming cohesin-motors on the DNA in one direction but not the other based on the orientation or strand of the CTCF motif. The primary consequence of this activity is significant looping interactions between convergently oriented CTCF binding sites, visible in Hi-C matrices as enriched points. However, determining the existence of this looping phenomenon in a given genome is challenging as several phenomena can produce punctate enrichments in interaction frequency in Hi-C matrices. Additionally, not all CTCF sites appear to loop, their loops are not always visible due to noise in the Hi-C matrix, and motif-calling to identify CTCF binding sites and their directionality is also not very accurate. These problems are all exacerbated when examining model organisms which tend to have noisier Hi-C data sets, ore fragmented genome assemblies, and potentially divergent CTCF motifs. To determine whether CTCF acts as a unidirectional border and forms loops then it is useful to instead query the border activity of CTCF sites rather than attempting to identify the point loops they form. When CTCF acts as a unidirectional border is has a strong orientation bias in its interactions. A CTCF site can have double the Hi-C interactions in its forward orientation over its reverse.




<img src="https://github.com/5centmike/CTCF-Motif-Interaction-Directionality/blob/main/ctcf-human-drosophila.png" width="500">

<img src="https://github.com/5centmike/CTCF-Motif-Interaction-Directionality/blob/main/StrongylocentrotusCMFA.png" width="500">

Enrichment for the CTCF motif over other motifs with the same base-content in a different order suggests that this motif is conserved and likely still represents the binding site of CTCF in this organism. The randomly shuffled sequences will be used in subsequent analyses as negative controls.


<img src="https://github.com/5centmike/CTCF-Motif-Interaction-Directionality/blob/main/StrongCTCFDistPlot.png" width="400"><img src="https://github.com/5centmike/CTCF-Motif-Interaction-Directionality/blob/main/StrongSH4DistPlot.png" width="400">

<img src="https://github.com/5centmike/CTCF-Motif-Interaction-Directionality/blob/main/StrongCTCFBoxPlot.png" width="400"><img src="https://github.com/5centmike/CTCF-Motif-Interaction-Directionality/blob/main/StrongSH4BoxPlot.png" width="400">
