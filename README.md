**FastQ Processor**

This project implements a FASTQ file processor in Python without using external bioinformatics libraries (e.g., Biopython). The script performs basic read preprocessing and quality analysis.

**Feature**

1)Load FASTQ files manually

2)Sliding window quality trimming (trim low-quality regions based on Phred scores)

3)Length filtering (remove reads shorter than a specified minimum)

4)GC-content calculation

5)Average Phred quality calculation at specific positions

6)Output filtered reads to a new FASTQ file


**Functions Overview**

1) *load_fastq*	- Loads FASTQ file into a list of (header, sequence, quality) tuples
   
2) *phred_score* -	Converts ASCII quality character to Phred+33 score

3) *sliding_window_trim* -	Performs sliding window trimming of reads based on quality

4) *length_filter* - Filters reads shorter than a specified length

6) *gc_content* -	Calculates GC content (%) of a read

7) *average_phred_at_pos* -	Computes average Phred score at a given 1-based position

8) *process_fastq* - Main function: trims, filters, computes statistics, writes output


**Testing**

download data - https://ctlab.itmo.ru/~aivanov/ct_algo_2026/reads.fastq

```python fastq_processor.py```
