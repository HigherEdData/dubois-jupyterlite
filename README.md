# JupyterLite deployment for "STEM Data Visualization and Du Boisian Methods"

This repository is version of https://github.com/HigherEdData/Du-Bois-STEM that is designed to running entirely within
the user's web browser with out needing and external server. It is powered by the [JupyterLite](https://jupyterlite.readthedocs.io/) project.

## Technical notes for instructional designers and instructors

There is a GitHub automation included in this repository that build and deploys this repo as a GitHub pages site
at https://highereddata.github.io/dubois-jupyterlite/

When developing this content, be sure to refresh your browser, clear your cache, and use the Help->Clear Browser Data to ensure
you are looking at the most recent version of your content.

If you need to add an additional Python or R library to the software evironment, add the library to the `environment.yml` file.

### `content/` directory

Place any data files, notebooks, or images that you want to make available to learners in the `content/` 
directory of these repo.

This `README.md` file is also automatically copied into the `content` directory when the site is generated.

### Links to specific notebook files

Browsing to https://highereddata.github.io/dubois-jupyterlite/ starts a JupyterLab like interface showing a
file browser and multiple notebook noteboks.

When sharing links to students, providing a direct URL may be preferred. To find this direct link, use this alternative 
URL:

https://highereddata.github.io/dubois-jupyterlite/tree

and then open the notebook you want to share. Copy the URL in the address bar.

Examples:
- https://highereddata.github.io/dubois-jupyterlite/notebooks/?path=notebooks%2Fpython_popmap_dubois-updated.ipynb
- https://highereddata.github.io/dubois-jupyterlite/notebooks/?path=notebooks%2Fpython_time_series_xy_dubois.ipynb

The argument of `?path=` is relative to the `contents/` directory of this repository.

### Same Origin Policy restrictions
When loading data (such as with a command like `pd.read_csv(url)` you may encounter an error involving the
the acronym CORS (Cross-Origin Resource Sharing). This is security feature of modern web-browsers.  

One solution to this issue is to ensure any files (e.g. `.csv` or `.png` files) that you need to reference in these notebooks
are also included in the this repository. Then instead of using a URL, you can reference the relative path.

If the notebooks are in the directory `contents/notebooks/`, then the relative path to various files could be

Examples:
- `../data/data.csv`
- `../readings-images/original-plate-02.jpg`
- `../data/us_state_2020/us_state_2020_reduced.shp`

Another solution is use URLs that have CORS configured to accept request from all origins (e.g. https://raw.githubusercontent.com)

Reference: https://github.com/jupyterlite/jupyterlite/issues/729

### JupyterLite vs JupyterLab

JupyterLite attempts most of the functionality of JupyterLab instance
that normally would require a server but running only in the local web browser. 

While many libraries and modules have been successfully made to run with JupyterLite, there are some functionality which
not (yet) work fully with JupyterLite. The Python and R libraries used in these Du Bois notebooks work as intended but
there may be compatability issues if additional libraries are needed. The JupyterLite ecosystem is under active development.

# STEM Data Visualization and Du Boisian Methods

<div>
<img src="https://github.com/carpentries-incubator/R-Data-Viz-with-Du-Bois/blob/main/episodes/files/du-bois-title.png?raw=true"
width="400" />
</div>

This repository publishes data and Jupyter Notebooks for the **STEM Data Visualization 
and Du Boisian Methods** learning modules. The lessons (we use the terms module 
and lesson interchangeably) are designed for learning how 
to create scientific data visualizations in in multiple programming languages.
The modules use examples from charts created by Black social scientist W.E.B. 
Du Bois and a diverse team of collaborators for the 1900 Paris World Expo.

## Why learn STEM data visualization with Du Bois?

The Du Bois team's visualizations were state of the art in 1900, using most of
the major chart types still employed across the sciences and engineering today.
The Du Bois charts provided some of the first widely accessible scientific 
analyses to refute false, biologically based theories of racial inequality. For
their innovative analyses, beauty, and historical importance, the original 
hand drawn charts are preserved in the U.S. Library of Congress.

## Module Organization

The modules are published in separate "lesson language" websites for your programming language of
choice. The websites were produced using the **Data Carpentries** workbench for
open source Github lesson sites. You can navigate to our lesson sites here:
* [STEM Data Visualization and Du Boisian Methods with R](https://carpentries-incubator.github.io/R-Data-Viz-with-Du-Bois/)
* STEM Data Visualization and Du Boisian Methods with Python
* STEM Data Visualization and Du Boisian Methods with Stata
* STEM Data Visualization and Du Boisian Methods with Pen and Paper

Each lesson language site is divided into separate **episodes**. Learners and instructors
can select the the episodes that best suite their prior programming experience and
learning objectives. All but the final episodes are designed for learners with little
re no programming experience.

The first episode of every lesson site starts with the social and scientific context
in which Du Bois created the visualizations. The lesson then introduces
key chart types for different kinds of data and visualization best practices. 
Multiple episodes are then offered for using the lesson's language (R, Python, Stata) 
for recreating or adapting selected Du Bois charts with modern data and STEM field related
data. Chart recreation eplisodes include Du Bois bar graphs and statistical maps.

The lesson sites are designed so that instructors can teach the modules
from the site. Learners can also use the sites to learn their content independently
and asynchronously. For instructors, we find that the sites are pedagogically
most effective when used as lecture notes and learning activity instructions. We do not
recommend lecturing with a screen share of the lesson site or projection of the lesson site.
This combination of text, activity prompts, and verbal narration tends to exceed effective
cognitive loads for learners.

Where appropriate, we instead provide images (like charts, diagrams, and photographs)
that can be opened from the lesson site in separate browser tab for display. We also
provide links to google slide files with all images for each episode. You can copy
edit the google slide files suit your particular teaching practices.

## Learning Objectives

Episode specific learning objectives and questions are noted at the beginning of each
episode. Overall learning objectives for entire modules are:
* Understand the social and scientific context of visualizations as a process of
scientific discovery (observation, hypothesis formation, data collection, analysis).
* Practice creative and visual thinking as valuable methods for scientific
discovery and communication.
* Comprehend major chart types (pie bar, bar chart, line chart, statistical map)
and their suitability for different levels of measurement and multivariate
relationships.
* Apply visualization best including accessible design and data story telling.
* Create and modify a Du Bois chart using R to experience the value of coding
to reproduce and adapt data visualizations in STEM.

## Coding Interactives

Our coding interactives with Jupyter Notebooks   can be accessed from the Du Bois
Cloud using any web browser with no installation required.Links to the associated
coding interactives are provided on each lesson site.  But you can also navigate 
directly to them here:
* [Literacy Bar Graph with R Notebook](http://dubois.2i2c.cloud/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2FHigherEdData%2FDu-Bois-STEM&urlpath=tree%2FDu-Bois-STEM%2Fr_literacy_dubois.ipynb&branch=main)
  * [Video Tutorial](https://drive.google.com/file/d/1ld6zO3PAOv-2vvkHhK5Guq9O3TT4GnHN/view?usp=sharing)
  * [Static version]()
* [Literacy to Biodiversity with R Notebook](https://dubois.2i2c.cloud/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2FHigherEdData%2FDu-Bois-STEM&urlpath=tree%2FDu-Bois-STEM%2Fr_literacy_biodiversity_dubois.ipynb&branch=main)
  * [Video Tutorial](https://drive.google.com/file/d/13gA01M3Vw0Y5udUOFjUnx8GI2ZDCXArh/view?usp=drive_web)
  * [Static version]()
* [Literacy Bar Graph with Python Notebook](http://dubois.2i2c.cloud/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2FHigherEdData%2FDu-Bois-STEM&urlpath=tree%2FDu-Bois-STEM%2Fpython_literacy_dubois.ipynb&branch=main)
  * [Static version]()
* [Black Population Map Python Notebook](http://dubois.2i2c.cloud/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2FHigherEdData%2FDu-Bois-STEM&urlpath=tree%2FDu-Bois-STEM%2Fnotebooks%2Fpython_popmap_dubois.ipynb&branch=main)
  * [Static version]()


## Our Team

The **STEM Data Visualization and Du Boisian Methods** learning modules were created by
a collaboration between STEM researchers and instructors at **University of California 
Merced**, **Princeton**, and **Fisk University** where Du Bois earned his first 
undergraduate degree. Development and testing of the modules is funded by the 
**National Science Foundation**.
