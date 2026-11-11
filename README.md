# project1-sequence-analysis
This is the code that I have created for my first assessed coding project for the "Introduction to programming for Life Sciences" module, with the intention to find mutations in NGS(next generation sequencing) reads.

To open the file, click on the most recent notebook (as of 10/11/2026 it is the notebook under the notebooks folder ending in (5)). It is important to note that in order to use every function you will have to press "run all" near the top of the UI. This is because some functions utilise other functions that have been defined in previous cells. 

This code, through various functions, should hopefully be able to: 
 - validate_read : check the validity of sequences (a string), outputting any errors that may lead to a sequence becoming invalid to be read against a reference (also a string).
 - find_mutations : compare and show differences (mismatches) in a sequence compared to a reference.
 - analyse_reads : analyse all potential reads (a list of sequences) against a reference, to output a combination of both validate_read and find_mutations.
 - summarise_samples : provide a summary of the output from analyse_reads, as well as information regarding mismatch events, and top three positions with the most mismatches.
 - compare_positions : uses a statistics function and summarise_samples to output sample-level calculations, for example, mismatch percentages, and statistical results generated from a two-sided Welches' t-test, and the associated p-value.
*more information on each specific functions can be found in their respective docstring*

**Code design notes:**
For readability purposes, I have tried my best to make most of the code run with if/elif/else statements. However, I abandoned this philosophy for the get_top_positions function, as it was unnecessarily long, instead opting to use a lambda function instead.
I also used helper functions like get_top_positions when a task is utilised more than once, like in step 4 and 5, which saved a lot of time overall as I didn't have to repeat myself.

Three tests I mainly used were by using empty tests, wrong input tests, and logic tests (for example, confirming that in step 5, difference was the same as treated means - control means).
