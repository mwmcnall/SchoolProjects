# Jupyter Notebook Reveal.js Presentation

Jupyter Notebooks are powerful, fun, sharable versions of Python code and are very well geared towards presentations with their blocks of code and markdown.

This is a **tutorial** on how to create a **reveal.js presentation** that's easily sharable via file-sharing or even just by uploading and linking on GitHub.

Here is a [link to a Final Project of mine](https://nbviewer.jupyter.org/github/mwmcnall/SchoolProjects/blob/master/Data%20Analytics/StackOverflowProject.slides.html#/) I did for a Data Analytics class with a rendered reveal.js presentation as an example.
- Spacebar to go through the presentation
- Up / Down to explore Sub-Slides
- Right / Left to explore Slides
- Escape / Return to explore entire project

## The Basics - Slides in Jupyter Notebook

Step one is outfitting your Notebook with slides. In order to get the ability to turn each Jupyter Notebook block into slides, select:
View -> Cell Toolbar -> Slideshow

![](https://github.com/mwmcnall/SchoolProjects/blob/tuts/Tutorials/Jupyter%20Notebook%20Reveal.js%20presentation/step%201.png)

You'll have the option of choosing these options for any of the blocks

- -: Block will load automatically with the above Slide / Sub-slide
- **Slide**: Presents each block as a new slide. Useful for headers, the start of new sections, can be selected during the presentation with left and right arrow keys
- **Sub-slide**: A continuation of the current slide-chain. Meant more as a continuation of a topic established by a Slide
- **Fragment**: A continuation of the current Slide / Sub-slide. You hit space bar to reveal it during a presentation like you would a powerpoint presentation
- **Skip**: Block does not show up in the presentation
- **Notes**: Block does not show up in the presentation but marked as a note for the presenter

![](https://github.com/mwmcnall/SchoolProjects/blob/tuts/Tutorials/Jupyter%20Notebook%20Reveal.js%20presentation/select%20slide.png)

## Creating the presentation

You'll have to go to the local directory and type out the relevant nbconvert command to convert the Jupyter Notebook into a proper presentation. I use Anaconda Prompt for this.

There are multiple ways to go about this depending on what your needs are

***

If all you want is to see if your presentation is setup the way you want, or you are just sharing it via your current computer, the below command is all you need to convert it into a presentation that will open into your browser

  - **jupyter nbconvert project.ipynb --to slides --post serve**

This does generate an .html file locally but that file is *only* exists as an .html of the .ipynb, not an actual presentation. The **-- post serve** command makes sure the project opens in your browser.

***

If you want a presentation as a **file to share / upload to GitHub and share** than run this line instead

- **jupyter nbconvert project.ipynb --to slides --reveal-prefix "https://cdn.jsdelivr.net/npm/reveal.js@3.6.0 "**

This *will* generate a proper .html file that will render using reveal.js in your browser. This file can be shared immediately, any images in your presentation will also need to be shared and in the same folder to load properly

The url with the --reveal-prefix command *may* not be future-proof, but as of 5/10/2019 it still works correclty

## Sharing via a GitHub link

There are only three steps involved to sharing a Jupyter Notebook presentation via **GitHub**!

- **Step One** - Upload the .html file created with the --reveal-prefix command to your repository
- **Step Two** - Get the url by navigating to the uploaded file via the repository
- **Step Three** - Go to [nbviewer](https://nbviewer.jupyter.org/) and paste in the link to the repository

And there you have it! A link to share your Jupyter Notebook presentation. If you're attempting these steps in succession, you may need to wait for nbviewer to be able to see the project on GitHub.

***

## nbconvert modifiers

There are other commands you can add to the line of code to generate the presentation

- **--SlidesExporter.reveal_scroll=True** : Add a scroll bar to your longer slides. May need to add some extra blank space in the notebook to show everything
- **--SlidesExporter.reveal_transition=none** : If you don't enjoy the transition of the slides and want to flag it off
- **--SlidesExporter.reveal_theme=** : [Here is a link](https://github.com/hakimel/reveal.js/tree/master/css/theme) to the possible base themes, you can also customize your own css file for theming.
- [Even more options](https://nbconvert.readthedocs.io/en/latest/config_options.html)

Thanks for reading! Happy Presentations!

- Wes
