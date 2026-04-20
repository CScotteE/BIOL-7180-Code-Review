# BIOL-7180-Code-Review
## Paper Summary


## Major comments
### Jupyter Notebook
My first major comment here is going to address the general accessibility of the tool in regards to the provided jupyter notebook. This jupyter notebook was included within the GitHub repository in order to make the code and tool more user friendly for those unfamiliar with Python. Utilizing this notebook within the Jupyter environment walks you through the scripts functions with easily interpretable, well-defined (in the READ.me) prompts. These prompts are really helpful as they allow you to easily provide the accompanied python codes with the necessary documentation required to develop and test your HCR probes. While, in theory and somewhat in practice, this noteboook helps to make the code more accessible, I think learning how to use a Jupyter notebook in itself can be a bit cumbersome. This could be because of my lack of familiarity with Jupyter lab in general, but in trying to set this up myself, I had to do some researching beyond the Jupyter help documentation that was provided within the GitHub. 

### Dependency Error
Beyond this, one major flaw I noticed in running the script was no actual information about the dependencies that are required to run the script. This led to the following error:

```python3
ModuleNotFoundError: No module named 'Bio'  
```

Information regarding the dependencies would have been useful to have on the main READ.me page to avoid this obstacle. With this, in trying to remedy the error, I found that the following command:

```python3
    from Bio.Blast.Applications import NcbiblastnCommandline as bn
```

is no longer compatible with the latest biopython version and I needed to install biopython v1.79 into my own conda environment in order to properly use the tool. 

Upon fixing this, I also ran into trouble with the pandas version I was using. The ability to `.append` was removed from all pandas versions >2.0. With this, I had to downgrade my padas version to pandas 1.5 in order to accomodate. 

biopython v1.79
Numpy v1.23
Pandas v1.5

Providing a conda environment with the necessary versions would have been a MUCH better method.

After doing some digging within the appropriate New_TO_PYTHON_JUPYTER.md file, however, there is helpful information on how to generate a conda environment with the required dependencies using the GUI-assisted Anaconda Navigator.  This ultimately made install the necessary dependencies for running the code much easier. 

### READ.me
READ.me was incredibly helpful in understanding the input parameters required to run. Definitions of all 

### Reproducibility


### Overall effectiveness

## Minor Comments
1. NEW_TO_PYTHON_JUPYTER.md links to the wrong file.
   - Seems to link to a previously developed repository... Similar information is contained within the .md, but clicking the link moves you to a completely different repository that contains different .py scripts. This could lead to some major confusion for those unfamiliar with github navigation or python.

2.


How easy was it for you to obtain, install, and run the code?  Not the easiest. Address in Jupyter portion
If you ran into road blocks, what were they, and what could the authors do differently to make their code easier to use?
Do the authors provide good documentation, both inside and outside (e.g., README files) of their code?
Do the authors provide information about how to reproduce the results in their paper?
Do the authors provide or specify a way to create a computational environment with all the requirements in place for their code to work? YES AND NO. 
Do the authors provide examples/tutorials for how to use their software? NO.
Is the code modular. I.e., is it broken up into into functions and/or class methods? Long sections of code is often a sign of poor coding practices.
-----------------------------------------------------------------------------------------------------------

### Paper Link
"Segment number threshold determines juvenile onset of germline cluster expansion in Platynereis dumerilii."\
_Kuehn et. al., 2021_

Link: https://pmc.ncbi.nlm.nih.gov/articles/PMC9114164/

### Associated GitHub repository
"insitu_probe_generator"\
_Ozpolat lab_

Link: https://github.com/rwnull/insitu_probe_generator/blob/v.0.3.2/README.md

### Rationale
I have to develop HCR probes soon and this would be really useful if it's reproducible. 
