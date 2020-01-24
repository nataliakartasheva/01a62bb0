# 01a62bb0

<h1 align="center">Milan pollution Shiny App </h1>
<p> The aim of this project is to analysise the datas from the website of the Comune di Milano. In particular, the study is focused on the different pollutants detected during the years from ARPA's stations. 
<br>
<h2> Installation</h2>

```R
# first install the R package "devtools" (.... OTHERS TO BE SPECIFIED) if not installed
devtools::install_github('unimi-dse/01a62bb0')
```

<br>
<h2> Usage</h2>
<p> Load the package. </p>

```R
require(milanpollution)
```

<p> There are two main functions of the package that are <code> pollution()</code> and <code> installpack()</code>. </p>
  
 <h3> Functions </h3>
 <code> installpack()</code>
 <p>This function will install the needed packages to run the application. <bold> It is suggested </bold> to run this function before the <italic> pollution() </italic> function. </p>

<br>
 <code> pollution()</code>
 <br>
 <code> shiny::runApp("milanpollution") </code>
  <p> This function loads the Shiny  application. </p>
  
  <br>
 
 <h2> Technologies </h2>
 
- shiny App for the User Interface with other library of data visualization.
- CKAN Data Application programming interface(API) to import datas directly from the openData Milano webasite.
- R language

<br>
 <h2> Description of the application </h2>
<p> When runned the pollution() function in the console, the application will run. It takes a bit to load the data from the OpenData Comune di Milano website since the app is using CKAN API. In particular, it checks the years 2017, 2018 and 2019 datasets. Also, to optimise the loading, the scraping function after getting the informations, the dataset is saved in the application memory. In this way, is not necessary to download the data each time we select the dataset of interest and the performance are better.</p>

<h3> Main page: Pollution </h3>

<p> In the main page are presented two plots: the time series of the datas and the related forecast. 
 
 ![Alt Text](https://raw.githubusercontent.com/unimi-dse/01a62bb0/master/img/mainpage.JPG)

  <li> The first plot represents the time series of the data deteceted by every station day by day. It is possible to check the Checkbox to enable the visualization of the linear regression line. </li>
  
 ![Alt Text](https://raw.githubusercontent.com/unimi-dse/01a62bb0/master/img/mainpage2.JPG)


  <li> The second plot represents the forecast of the time series. It is possible to set a different lag for the forecast using the slidebar. </li>
  <p> Then is possible to select the year of the dataset in interest using a selector </p>
</p>

<h3> Second page: Stations </h3>

![Alt Text](https://raw.githubusercontent.com/unimi-dse/01a62bb0/master/img/secondpage.JPG)

<p> In this page is possible to see the barplot representing the detected data from each station in the selected year. </p>

<h3> Third page: About </h3>
<p> This section describes the aim of the project. </p>
