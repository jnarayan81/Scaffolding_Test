# Scaffolding_Test
Scaffolding test data ! Generate simulated hifi reads using BBmap tool

```

# make 30x haploid coverage for PacBio reads for Hifi reads
# error rate from 1 - 0.1 % minimum 9000bp midlength 10000bp max 12000bp
/genetics/elbers/bbmap-38.86/randomreads.sh build=1 \
ow=t seed=1 \
ref=ref.fasta \
illuminanames=t addslash=t \
pacbio=t pbmin=0.001 pbmax=0.01 \
coverage=15 paired=f \
gaussianlength=t \
minlength=9000 midlength=10000 maxlength=12000 \
out=hifi.fastq.gz > random_reads_pacbio_hifi.log 2>&1

```
Log file of bbmap/randomreads

```
java -ea -Xmx126922m -cp /home/urbe/Tools/MyTools/Jod/testData/bbmap/current/ align2.RandomReads3 build=1 build=1 ow=t seed=1 ref=ref.fa illuminaname
io=t pbmin=0.001 pbmax=0.01 coverage=15 paired=f gaussianlength=t minlength=9000 midlength=10000 maxlength=12000 out=hifi.fastq.gz
Executing align2.RandomReads3 [build=1, build=1, ow=t, seed=1, ref=ref.fa, illuminanames=t, addslash=t, pacbio=t, pbmin=0.001, pbmax=0.01, coverage=1
anlength=t, minlength=9000, midlength=10000, maxlength=12000, out=hifi.fastq.gz]

Writing reference.
Executing dna.FastaToChromArrays2 [ref.fa, 1, writeinthread=false, genscaffoldinfo=true, retain, waitforwriting=false, gz=true, maxlen=536670912, wri
caf=1, midpad=500, nodisk=false]

Set genScaffoldInfo=true
Writing chunk 1
Waiting for writing to finish.
Finished.
snpRate=0.0, max=0, unique=true
insRate=0.0, max=0, len=(0-0)
delRate=0.0, max=0, len=(0-0)
subRate=0.0, max=0, len=(0-0)
nRate  =0.0, max=0, len=(0-0)
genome=1
PERFECT_READ_RATIO=0.0
ADD_ERRORS_FROM_QUALITY=false
REPLACE_NOREF=false
paired=false
read length=9000-12000
reads=142
Wrote hifi.fastq.gz
Time:   1.472 seconds.
```
