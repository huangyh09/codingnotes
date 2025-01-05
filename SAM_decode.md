# Notes for processing SAM file

## Useful references
Major keys: FLAG and CIGAR

* https://samtools.github.io/hts-specs/SAMv1.pdf
* https://broadinstitute.github.io/picard/explain-flags.html
* https://pysam.readthedocs.io/en/latest/api.html#pysam.AlignedSegment

## PySam
TODO:

* confirm if `is_read1`, `is_read2` are decoded from FLAG in the way listed in picard above.

## STAR

* keep unsorted bam will retain the paired reads in order and unmapped reads.
