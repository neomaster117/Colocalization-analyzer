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
The action of every agent <br />
  into the world <br />
starts <br />
  from their physical selves. <br />
<img width="960" alt="initial window" src="https://github.com/neomaster117/Colocalization-analyzer/assets/47111504/e886e002-57d5-464e-8f69-f326b5d50388">




