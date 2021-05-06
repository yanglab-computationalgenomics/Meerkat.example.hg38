# Meerkat.example.hg38

This a toy example to test Meerkat. Meerkat can be downloaded at http://compbio.med.harvard.edu/Meerkat/ or https://github.com/guru-yang/Meerkat. The reads in this example are aligned to hg38. To run this example, modify the path of reference, bwa, samtools, blast, etc and run following:

perl scripts/pre_process.pl -b example.sorted.bam -I /db/hg38/hg38_bwa_idx/hg38.fasta -A /db/hg38/hg38.fasta.fai -W /opt/bwa/ -S /opt/samtools/
perl scripts/meerkat.pl -b example.sorted.bam -F /db/hg38/hg38_fasta/ -W /opt/bwa/ -B /opt/blast/bin/ -S /opt/samtools/
perl scripts/mechanism.pl -b example.sorted.bam -R /db/hg38/rmsk-hg38.txt

The final output example.variants and some of the intermediate files can be found in outputs folder.
