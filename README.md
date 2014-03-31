#Supplemental files for Rogers _et al._ Landscape of standing variation for tandem duplications in *Drosophila yakuba* and *Drosophila simulans*.

Strain names and numbers are found in FlyLines.txt
CY=Cameroon D.yakuba
NY= Nairobi D.yakuba

MD=Madagascar D.simulans
NS=Nairobi D.simulans

Chromosome names and numbers are found in 
DsimChromNames.txt
DyakChromNames.txt

Genes captured by duplications are found in
DupGenes.dsim.txt
DupGenes.dyak.txt

Bed Format files compatible with UCSC browser are found in 
DsimTandemDups.bed                                                                         
DyakTandemDups.bed 
Format:
chrom start stop identifier freqency

##CNV calls
Raw data calls prior to all filtering (including ancestral duplications, reference duplications, and divergent reads spanning more than 25kb) are in
RawCallsByLineSim/\*.div.cov3.mm2.rearr
RawCallsByLineYak/\*.div.cov3.mm2.rearr

The format of these files is 10 columns:
<ol>
<li>id = Event identification number (arb. integer)</li>
<li>chrom1 = Chromosome number in reference where the first read cluster is</li>
<li>coverage = Number of read pairs supporting the event</li>
<li>strand1 = Strand of first read cluster.  0 = plus, 1 = minus</li>
<li>start1 = Start position of first read cluster.</li>
<li>stop1 = Stop position of second read cluster.</li>
<li>chrom2 = Chromosome number in reference where the second read cluster is</li>
<li>start2 = Start position of second read cluster.</li>  
<li>stop2 = Stop position of second read cluster.</li> 
<li>reads = Pipe-separated (the pipe is the | character) list of the read pairs supporting the event.  Format is readPairName;start,stop,strand,start,stop,strand, where the last two values are for the two reads in the pair.</li>
</ol>

##Transposable element (TE) calls

The TE calls are in the TEcalls directories.  The file formats are based on the line number used in the paper.  Thus, there are 20 files per species.  The format is the following:

<ol>
<li>Chromsosome</li>
<li>Insert site position 1</li>
<li>Insert site position 2</li>
<li>Annotation information</li>
<li>shared or novel>

The second and third column represent the range of possible insert site postions.  These positions are zero-offset (e.g., position 1 on each chromosome is 0). Column 4 is a crude attempt at annotating what the TE is.  (Note that the annotation scheme differs from Cridand et al. doi: 10.1093/molbev/mst129.  Further, our purpose in the paper was to define presence/absence and thus we ingore the annotation information for our own analyses.  The issue of accurate TE annotation of the reference genomes needs to be addressed in the future in order to improve the annotation of TE presence/absence polymorphism.)

The final column simply records whether or not the TE is found in the relevant reference genome sequence or not.