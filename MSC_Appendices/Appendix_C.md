### Appendix C

Trimmomatic script used to trim sequences

>java -jar /usr/local/bin/Trimmomatic-0.36/trimmomatic-0.36jar PE -threads20 -phred33 BRLCL-3730-09-44-01_S9_L001_R1_001.fastq.gz BRLCL-3730-09-44-01_S9_L001_R2_001.fastq.gz
output18_fwdpaired.fq.gz output18_fwdunpaired.fq.gz
output18_revpaired.fq.gz output18_revunpaired.fq.gz
Trimmomatic-0.35/adapters/TruSeq3-PE.fa:2:30:10 LEADING:5 TRAILING:5 SLIDING WINDOW:4:20 MINLEN;20

BreSEQ script used to align reads to PAO1-Otago
>breseq -r ILPAO_for_breseq.gff3 output18_fwdpaired.fq.gz output18_revpaired.fq.gz -j 100 -o Documents/output18
