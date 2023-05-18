# Colocalization analyzer
 Simple data visualization shiny app for colocalization


A Python pipeline was developed to analyze the colocalization of two markers in specific foci when cells are submitted to a putative cancer drug that induces cell death. The foci form prior to the death onset and may serve as a clue into the mechanism of action of that drug. Visualizations in Python are typically done in the Mathplotlib library, with less aesthetic possibilities. This R Shiny  Colocalization analyzer application was developed to give the more customizable and aesthetic output.

The Colocalization analyzer can be run in an Rstudio GUI or off a server with the link provided. The online app is hosted on a virtual Linux server from AWS and can be accessed at the following address:
http://3.75.183.31:3838/data_analyzer/

The application takes a single input (input.csv) file and outputs a single figure (plot.png). It contains:
1. Upload csv data file - "Browse" button, which can be used to find the location of the file. For practice, an "input.csv" file is provided in the documentation.
2. "X Axis title" and "Y Axis title" respetively, which are optional and can be left empty, or filled in to give the names of the X and Y axes
3. "Input height (px)" and "Input weight (px)" - required fields to set the height and weight of the figure. They become activated initially by pressing the "Update plot" button, then automatically when changed. 
4. "Update plot" button, which initializes the figure in the Shinyapp and later must be called to update height and width whenever the user changes those parameters. Note: While the GUI image will update automatically whenever new height or width data are inputed, the Update plot button must be pressed before saving for the change to take effect in the output file.
5. "Download plot" button - in the offline version it can be used to set a download location and save simultaneously, while in the server version it automatically downloads the plot.png file to the default Download folder.

The tpyical use is exemplified in the folowowing way:

1. Initialization - the window will look like this when initialized:
 <br />
<img width="960" alt="initial window" src="https://github.com/sorin-tanasa/Colocalization-analyzer/assets/47111504/e9711fd8-0fcb-4bdb-a505-18b45b645dfa">

<br />
<br />
2. File selection:
<br />

<img width="959" alt="file uploaded" src="https://github.com/sorin-tanasa/Colocalization-analyzer/assets/47111504/a786dc77-621b-4ebe-8d7c-4cc2a68afbe8">
<br />
<br />
3. Detail update - plot height and width must be supplied as integer (natural) numbers. Titles for the X and Y columns are optional:
<br />
<br />
<img width="955" alt="all fields filled in" src="https://github.com/sorin-tanasa/Colocalization-analyzer/assets/47111504/c4dd1ead-97b7-46b1-98fe-de08ef4ef949">

<br />
<br />
4. Generating the plot - pressing the Update plot button generates the figure:
<br />
<br />
<img width="944" alt="all fields filled and graph generated" src="https://github.com/sorin-tanasa/Colocalization-analyzer/assets/47111504/0f2bfd87-22dd-43bd-a1d7-11c292967a0c">

<br />
<br />
The figure itself is visualised bellow the buttons, taking up a large window space, and can be fully visualized by scrolling the window down:
<br />
<br />
<img width="960" alt="graph generated bellow the buttons" src="https://github.com/sorin-tanasa/Colocalization-analyzer/assets/47111504/ccfa4bcf-3bb4-4ead-be54-15ba0dfd80bb">

<br />
<br />
Larger resolutions will not fit well in the GUI but can be also generated as outputs:
<br />
<br />
<img width="946" alt="all fields filled in for larger image" src="https://github.com/sorin-tanasa/Colocalization-analyzer/assets/47111504/bfabec4e-051e-4eff-a06e-8e846fb5dcbd">
<img width="945" alt="larger image in GUI" src="https://github.com/sorin-tanasa/Colocalization-analyzer/assets/47111504/d4b1d8cb-0bba-4706-8784-abc728affc24">


<br />
<br />
The actual images may look different, because fonts are fixed and the resolution alone can be modified, and the user should customize the figure by also checking the file output itself. Bellow we can see two outputs created with the settings used in the two examples above:

![plot](https://github.com/sorin-tanasa/Colocalization-analyzer/assets/47111504/a10a153c-de8f-4882-9cec-e6aee069638b)

(the lower, 600x1000 resolution file)

![plot larger](https://github.com/sorin-tanasa/Colocalization-analyzer/assets/47111504/10322735-0461-424d-a847-333d467d7a9b)

(the larger, 900x1200 resolution file)

If the server for some reason doesn't work it may be because of issues at my account at AWS, so feel free to write me at tanasa.sorin@gmail.com for help.






