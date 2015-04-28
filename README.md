This will be our new bcl to fastq pipeline. Features will include:

  * Runs as a background process, rather than a cron job that needs to check if another instance is already running
  * Handles undetermined indices in a more coherent manner
  * Adds quality metrics to the report email
  * Compiles an automated project-report (pdf), to go along with each submission. This uses [ReportLab](https://pypi.python.org/pypi/reportlab).
  * Functions divided into more meaningful subfiles in a module, rather than being scattered across levels of shell scripts
  * Written explicitly for python3, just to future proof things a bit.

To Do
 [ ] - Do we ever have the same sample name split across libraries in the same project/flow cell? The current implementation will overwrite the fastqc results for that. A better option might be to make subdirectories within each FASTQC_projectID directory
 [ ] - Combine flowcells/lanes from submission (with our flowcell focus we still have issues if submissions are spread over many flow cells)
 [ ] - Per-project PDF files
 [ ] - What does DEEP need in addition?
 [ ] - Share stuff to EVA automatically, rather than with `seq_share.sh`
