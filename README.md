# BIOL-7180-Code-Review
## Paper Summary


## Major comments
### Jupyter Notebook
My first major comment here is going to address the general accessibility of the tool in regards to the provided jupyter notebook. This jupyter notebook was included within the GitHub repository in order to make the code and tool more user friendly for those unfamiliar with Python. Utilizing this notebook within the Jupyter environment walks you through the scripts functions with easily interpretable, well-defined (in the READ.me) prompts. These prompts are really helpful as they allow you to easily provide the accompanied python codes with the necessary documentation required to develop and test your HCR probes. While, in theory and somewhat in practice, this noteboook helps to make the code more accessible, I think learning how to use a Jupyter notebook in itself can be a bit cumbersome. This could be because of my lack of familiarity with Jupyter lab in general, but in trying to set this up myself, I had to do some researching beyond the Jupyter help documentation that was provided within the GitHub. To make this more user-friendly, perhaps consider generating a python code with functions that could be utilized right in the terminal. This way would allow you to provide specific code that should be run while still allow for input from the user directly in the terminal. 

### Dependency Error
To start this comment off, I do want to recognize that the information in the appropriate NEW_TO_PYTHON_JUPYTER.md file (see comment below) for setting up an environment is very helpful. Providing links to Anaconda and it's GUI systems allows even beginners to install the general dependencies required for this package without much coding knowledge required. 

However, one major flaw I noticed in running the script was a lack of actual information about the dependency versions that are required to run the script. This led to quite a large number of dependency errors showing up as I tried to run the code and a fair bit of troubleshooting to figure out what combination of package versions I needed. At first, it wasn't clear that Biopython was required (see minor comment #3 below) and so I got a number of errors denoting that BioPython was missing. After installing Biopython and running the script again, I noticed an error regarding the latest Biopython version I downloaded and the functions being used in the script. With this I had to go back and install biopython v1.79. After remedying this situation, I found incompatibilities with both the latest numpy package and, subsequently, the latest pandas package. This required me to go around and search for which version are compatible with the functions required, but also which versions are compatible with each other. The correct combination ended up being Biopython v1.79, Numpy v1.23, and Pandas v1.5. To avoid these issues from popping up, perhaps consider generating a simple YAML file that people could use to generate a conda environment with the proper versions you used to run your package. I'm personally not familiary with the Anaconda GUI Navigator, but does this system allow you to choose the versions you want? This may be another reason to consider generating a YAML file. 

### READ.me and withn code documentation
Overall, I thought the READ.me was incredibly helpful in understanding the input parameters required to develop these probes. Full explanations of each parameter along with the output descriptions of each unique input were provided. In addition, this section provides links to outside sources to better understand some of the nuances behind HCR probe development. While the information provided is very helpful, I did find navigating through the READ.me to bit a bit cumbersome and generally disorganized. It comes across as one giant block of code and doesn't utilze any markdown formatting that would help make the file a bit more readable. 

In terms of within-code documentation, I do want to mention the lack of notation in the code itself. While I recognize that the Jupyter notebook is supposed to run the code "under the hood", it is still important to make sure your code is notated properly to provide better reproducibility and confidence. A lack of notation in the code ultimately requires blind-faith in someone who isn't fluent in the python langauge. I think proper notation throughout the code could help guide someone through the 

### Reproducibility
In terms of reproducibility, it would be great if you could provide a sample sequence, sample .fasta, and expected output results. While I want to recognize a decent description of the outputs in the READ.me, it would be nice to ensure that the code is running properly and that there are no hiccups after cloning the repository. By using the same data used to develop probes for the publication, any new users can ensure the code is working correctly. In the same vein (though somewhat less code related), including the method/considerations you used to develop the probes in the associated publication could help serve as a guide for someone who is just beginning to develop probes. For some of the optional features, I know there are genreally standards to follow (<5 AT repeats, etc.), so providing a tutorial and addressing these would made this repository and package incredibly accessible. 

### Overall effectiveness


## Minor Comments
1. NEW_TO_PYTHON_JUPYTER.md links to the wrong file.
   - Seems to link to a previously developed repository... Similar information is contained within the .md, but clicking the link moves you to a completely different repository that contains different .py scripts. This could lead to some major confusion for those unfamiliar with github navigation or python.

2. Saving the output as a .csv may be useful, rather than relying on copy/paste.
   - While I recognize IDT requires an .xlsx file, converting a .csv to an .xlsx file might be a bit less convoluted than copying and pasting. A simple conversion like this could also prevent any errors from occuring during the copy and paste process.
  
3. Information on dependencies hidden in the "NEW_TO_PYTHON_JUPYTER.md" file.
   - Moving this to the general READ.me file where all of the other basic information is would be beneficial. I personally wasn't very new so I didn't think to look here for general information about dependencies.
  
4. 






Is the code modular. I.e., is it broken up into into functions and/or class methods? Long sections of code is often a sign of poor coding practices.
    Modular to an extent, but havily driven by input. ONly two real function were designed 
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
