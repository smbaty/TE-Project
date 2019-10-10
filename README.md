# TE-Project
Updated TE Project involving Baeolophus bicolor and Dryobates pubescens.



The preliminary steps includes renaming the original fastq files for both species to have numbered names. The paired R1 and R2 files have the same beginning number; 1_R1, 1_R2, 2_R1, 2_R2 and so on.



Directories includes tools used in order and what scripts were used.
1. rCorrector (read error-correcting)
2. Unique python script (used to remove pairs where one end is unfixable)
3. Trimgalore (trimming low quality bases)
4. HISAT (alignment) (aligned to indexes for Parus major and Picoides pubescens)
5. samtools was used to sort sam files by read name to prepare for HTSeq.
6. HTSeq used to built count tables. Following options were used:
      a. TEs in introns or not (two different gtf files)
      b. Union vs intersection-strict options (default vs --mode intersection-strict)
      c. Nonunique all vs nonunique none options (default vs --nonunique all)
