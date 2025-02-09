# What's in the Smart-seq2 Single Sample Pipeline Loom File?

The Loom file is an HDF5 file generated using [Loompy v.3.0.6](http://loompy.org/). It contains global attributes describing the Loom file and workflow that generated it ([Table 1](#table-1-global-attributes)), column attributes detailing metrics for the individual cells ([Table 2](#table-2-column-attributes-cell-metrics)) and row attributes detailing metrics for individual genes ([Table 3](#table-3-row-attributes-gene-metrics)). The main matrix contains the RSEM TPMs and there is an additional layer that contains RSEM expected_counts (the named "estimated_counts").

The tables below document these metrics, list which tools generate them, and define them. This Loom file is the default matrix output of the Smart-seq2 Single Sample pipeline.


## Table 1. Global Attributes

The global attributes in the Loom apply to the whole file, not any specific part. 

| Attribute | Details |
| :-- | :-- |
| pipeline_version | String with the pipeline version |
| LOOM_SPEC_VERSION | String with the loom file spec version |
| CreationDate | Date Loom file was generated |




## Table 2. Column Attributes (Cell Metrics)

| Cell Metrics | Program |Details |
|:---|:---:|:---|
| `CellID` | --- | The unique identifier for each cell; read from the input_id |
| `cell_names` | ---| The unique identifier for each cell; read from the input_id and identical to `CellID` |
| `input_id` | --- | The input_id listed in the pipeline configuration file |
| `input_id_metadata_field` | --- | Optional identifier for the metadata field used for the `input_id` |
| `input_name` | --- | The optional string provided in the pipeline configuration to further identify samples |
| `input_name_metadata_field` | --- | Optional identifier for the metadata field used for the `input_name` |
| `ACCUMULATION_LEVEL` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `ALIGNED_READS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `AT_DROPOUT` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `Aligned 0 time` | [HISAT2](https://ccb.jhu.edu/software/hisat2/manual.shtml) | Number and percent reads aligned 0 times |
| `Aligned 1 time` | [HISAT2](https://ccb.jhu.edu/software/hisat2/manual.shtml) | Number and percent reads aligned 1 time |
| `Aligned >1 times` | [HISAT2](https://ccb.jhu.edu/software/hisat2/manual.shtml) | Number and percent reads aligned more than 1 time |
| `BAD_CYCLES.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `CODING_BASES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `CORRECT_STRAND_READS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `ESTIMATED_LIBRARY_SIZE` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `GC_DROPOUT` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `GC_NC_0_19` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `GC_NC_20_39` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `GC_NC_40_59` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `GC_NC_60_79` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `GC_NC_80_100` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `IGNORED_READS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `INCORRECT_STRAND_READS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `INTERGENIC_BASES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `INTRONIC_BASES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `MEAN_READ_LENGTH.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `MEDIAN_3PRIME_BIAS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `MEDIAN_5PRIME_BIAS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `MEDIAN_5PRIME_TO_3PRIME_BIAS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `MEDIAN_CV_COVERAGE` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `NUM_R1_TRANSCRIPT_STRAND_READS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `NUM_R2_TRANSCRIPT_STRAND_READS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `NUM_UNEXPLAINED_READS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `Overall alignment rate` | [HISAT2](https://ccb.jhu.edu/software/hisat2/manual.shtml) | Overall percent of reads that aligned |
| `PCT_ADAPTER.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PCT_CHIMERAS.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PCT_CODING_BASES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PCT_CORRECT_STRAND_READS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PCT_INTERGENIC_BASES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PCT_INTRONIC_BASES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PCT_MRNA_BASES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PCT_PF_READS.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PCT_PF_READS_ALIGNED.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PCT_PF_READS_IMPROPER_PAIRS.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PCT_R1_TRANSCRIPT_STRAND_READS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PCT_R2_TRANSCRIPT_STRAND_READS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PCT_READS_ALIGNED_IN_PAIRS.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PCT_RIBOSOMAL_BASES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PCT_USABLE_BASES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PCT_UTR_BASES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PERCENT_DUPLICATION` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PF_ALIGNED_BASES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PF_ALIGNED_BASES.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PF_BASES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PF_HQ_ALIGNED_BASES.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PF_HQ_ALIGNED_Q20_BASES.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PF_HQ_ALIGNED_READS.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PF_HQ_ERROR_RATE.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PF_HQ_MEDIAN_MISMATCHES.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PF_INDEL_RATE.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PF_MISMATCH_RATE.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PF_NOISE_READS.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PF_READS.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PF_READS_ALIGNED.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `PF_READS_IMPROPER_PAIRS.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `READS_ALIGNED_IN_PAIRS.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `READS_USED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `READ_PAIRS_EXAMINED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `READ_PAIR_DUPLICATES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `READ_PAIR_OPTICAL_DUPLICATES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `RIBOSOMAL_BASES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `SECONDARY_OR_SUPPLEMENTARY_RDS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `STRAND_BALANCE.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `TOTAL_CLUSTERS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `TOTAL_READS.UNPAIRED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `Total reads` | [HISAT2](https://ccb.jhu.edu/software/hisat2/manual.shtml) | Total number of aligned reads |
| `UNMAPPED_READS` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `UNPAIRED_READS_EXAMINED` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `UNPAIRED_READ_DUPLICATES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `UTR_BASES` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `WINDOW_SIZE` | [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) | See [Picard](https://broadinstitute.github.io/picard/picard-metric-definitions.html) documentation |
| `alignable reads` | [RSEM cnt file](https://github.com/deweylab/RSEM/blob/master/cnt_file_description.txt) | The number of alignable reads |
| `filtered reads` |  [RSEM cnt file](https://github.com/deweylab/RSEM/blob/master/cnt_file_description.txt) | The number of filtered reads due to too many alignments |
| `multiple mapped` |  [RSEM cnt file](https://github.com/deweylab/RSEM/blob/master/cnt_file_description.txt) | The number of reads aligned to multiple genes |
| `strand` |  [RSEM cnt file](https://github.com/deweylab/RSEM/blob/master/cnt_file_description.txt) | The RSEM read_type; describes if data is single- or paired-end |
| `total alignments` |  [RSEM cnt file](https://github.com/deweylab/RSEM/blob/master/cnt_file_description.txt) | The RSEM nHits; the number of total alignments |
| `total reads` |  [RSEM cnt file](https://github.com/deweylab/RSEM/blob/master/cnt_file_description.txt) | The number of total alignable reads |
| `unalignable reads` |  [RSEM cnt file](https://github.com/deweylab/RSEM/blob/master/cnt_file_description.txt) | The number of  reads unalignable |
| `uncertain reads` |  [RSEM cnt file](https://github.com/deweylab/RSEM/blob/master/cnt_file_description.txt) | The number of  reads aligned to multiple locations |
| `unique aligned` |  [RSEM cnt file](https://github.com/deweylab/RSEM/blob/master/cnt_file_description.txt) | The number of reads uniquely alignable to one gene |


## Table 3. Row Attributes (Gene Metrics)

| Gene Metrics                  | Program            |Details                 |
|-------------------------------|--------------------|------------------------|
|`ensembl_ids` | [GENCODE GTF](https://www.gencodegenes.org/) | The gene_id listed in the GENCODE GTF |
|`gene_names` | [GENCODE GTF](https://www.gencodegenes.org/) | The unique gene_name provided in the GENCODE GTF |
| `Gene` | [GENCODE GTF](https://www.gencodegenes.org/) | The unique gene_name provided in the GENCODE GTF; identical to attribute in `gene_names` |
