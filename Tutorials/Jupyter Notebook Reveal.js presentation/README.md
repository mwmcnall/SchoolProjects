# Jupyter Notebook Reveal.js Presentation

Jupyter Notebooks are powerful, fun, sharable versions of Python code and are very well geared towards presentations with their blocks of code and markdown.

This is a **tutorial** on how to create a **reveal.js presentation** that's easily sharable via file-sharing or even just by uploading and linking on GitHub.

## The Basics - Slides in Jupyter Notebook

Step one is outfitting your Notebook with slides. In order to get the ability to turn each Jupyter Notebook block into slides, select:
View -> Cell Toolbar -> Slideshow

Step one image

You'll have the option of choosing these options for any of the blocks

- -: Block will load automatically with the above Slide / Sub-slide
- **Slide**: Presents each block as a new slide. Useful for headers, the start of new sections, can be selected during the presentation with left and right arrow keys
- **Sub-slide**: A continuation of the current slide-chain. Meant more as a continuation of a topic established by a Slide
- **Fragment**: A continuation of the current Slide / Sub-slide. You hit space bar to reveal it during a presentation like you would a powerpoint presentation
- **Skip**: Block does not show up in the presentation
- **Notes**: Block does not show up in the presentation but marked as a note for the presenter

Select Slide image

## Creating the presentation

You'll have to go to the local directory and type out the relevant nbconvert command to convert the Jupyter Notebook into a proper presentation.

There are multiple ways to go about this depending on what your needs are

- Testing / Local presentation
  - If all you want is to see if your presentation is setup the way you want, or you are just sharing it via your current computer, the below command is all you need to convert it into a presentation that will open into your browser
  - **jupyter nbconvert project.ipynb --to slides --post serve**
  - This does generate an .html file locally but that file is *only* exists as an .html of the .ipynb, not an actual presentation
- Presentation to share / upload
  - **jupyter nbconvert project.ipynb --to slides --reveal-prefix "https://cdn.jsdelivr.net/npm/reveal.js@3.6.0 "**
  - Generates an .html file that will properly render as a reveal.js presentation, which *can* be shared
  - The reveal-prefix command *may* not be future proof, but it was correct as of 5/10/2019


## Project modifiers

