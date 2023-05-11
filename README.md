# Colocalization analyzer
 Simple data visualization shiny app for colocalization

A Python pipeline was developed to analyze the colocalization of two markers in specific foci when cells are submitted to a putative cancer drug that induces cell death. The foci form prior to the death onset and may serve as a clue into the mechanism of action of that drug. Visualizations in Python are typically done in the Mathplotlib library, with less aesthetic possibilities. This R Shiny  Colocalization analyzer application was developed to give the more customizable and aesthetic output.

The Colocalization analyzer can be run in an Rstudio GUI or off a server with the link provided. The online app is hosted on a virtual Linux server from AWS and can be accessed at the following address:
http://3.75.183.31:3838/data_analyzer/

The application takes a single input (input.csv) file and outputs a single figure (plot.png). It contains:
1. Upload csv data file - Browse button, which can be used to find the location of the file
2. X Axis title and Y Axis title respetively, which are optional and can be left empty, or filled in to give the names of the X and Y axes
3. Input height (px) and Input weight (px) - required fields to set the height and weight of the figure. They become activated initially by pressing the "Update plot" button, then automatically when changed. 
4. Update plot button, which initializes the figure in the Shinyapp and later must be called to update height and width whenever the user changes those parameters
5. Download plot button - in the offline version it can be used to set a download location and save simultaneously, while in the server version it automatically downloads the plot.png file to the default Download folder.

The tpyical use is exemplified in the folowowing way:

1. Initialization - the window will look like this when initialized:
 <br />
<img width="960" alt="initial window" src="https://github.com/neomaster117/Colocalization-analyzer/assets/47111504/e886e002-57d5-464e-8f69-f326b5d50388">
<br />
<br />
<br />
2. File selection:
<br />
<img width="959" alt="file uploaded" src="https://github.com/neomaster117/Colocalization-analyzer/assets/47111504/4c96a549-ee0d-45cf-a267-c9b7812de1cd">
<br />
<br />
<br />
3. Detail update - plot height and width must be supplied as integer (natural) numbers. Titles for the X and Y columns are optional:
<br />
<br />
<br />
<img width="955" alt="all fields filled in" src="https://github.com/neomaster117/Colocalization-analyzer/assets/47111504/80dad226-0a31-4c0a-992d-d82c6785b23e">
<br />
<br />
<br />
4. Generating the plot - pressing the Update plot button generates the figure:
<br />
<br />
<br />
<img width="958" alt="all fields filled and graph generated" src="https://github.com/neomaster117/Colocalization-analyzer/assets/47111504/8ac68469-f8ac-4583-b927-3e3f5004daa2">
<br />
<br />
<br />
The figure itself is visualised bellow the buttons, taking up a large window space, and can be fully visualized by scrolling the window down:
<br />
<br />
<br />
<img width="942" alt="graph generated bellow the buttons" src="https://github.com/neomaster117/Colocalization-analyzer/assets/47111504/2524582f-13de-476c-b491-86f59c08cbf0">
<br />
<br />
<br />
Larger resolutions will not fit well in the GUI but can be also generated as outputs:
<br />
<br />
<br />
<img width="959" alt="all fields filled in for larger image" src="https://github.com/neomaster117/Colocalization-analyzer/assets/47111504/55377414-ff38-4ad3-ae8e-f7a026322964">

<img width="947" alt="larger image in GUI" src="https://github.com/neomaster117/Colocalization-analyzer/assets/47111504/c7c08026-bc9c-432e-ac4d-b1a82a1497ce">
<br />
<br />
<br />

The actual images may look different, because fonts are fixed and the resolution alone can be modified, and the user should customize the figure by also checking the file output itself. Bellow we can see two outputs created with the settings used in the two examples above:

![plot](https://github.com/neomaster117/Colocalization-analyzer/assets/47111504/8e14a48b-89cb-413b-978c-b62c258f7437)
<br />
(the lower, 600x1000 resolutionfile)
<br />
<br />
<br />
![plot larger](https://github.com/neomaster117/Colocalization-analyzer/assets/47111504/1d7625be-5771-4ef6-b475-cfe787b7eb94)
<br />
(the larger, 900x1200 resolution file)






