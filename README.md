
<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/emiltj/groundwater_pollution_dk">
    <img src="README_images/logo.png" alt="Logo" width="40" height="65">
  </a>

  <h3 align="center">Groundwater pollution and farm use in Denmark</h3>

  <p align="center">
    Spatial analysis exam project 2021
    <br />
    <a href="https://github.com/emiltj/groundwater_pollution_dk/report.pdf"><strong>Read the report»</strong></a>
    <br />
    <a href="https://github.com/emiltj/groundwater_pollution_dk/blob/master/groundwater_pollution_dk.md">View markdown</a>
    ·
    <a href="https://github.com/emiltj/groundwater_pollution_dk/issues">Report bug</a>
    ·
    <a href="https://github.com/emiltj/groundwater_pollution_dk/issues">Request feature</a>
  </p>
</p>


<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About the project</a>
    </li>
    <li>
      <a href="#getting-started">Getting started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
      </ul>
    </li>
    <li><a href="#repository-structure">Repository structure</a></li>
    <li><a href="#data">Data</a></li>
    <li><a href="#usage">Usage</a></li>
        <ul>
          <li><a href="#running-the-script">Running the script</a></li>
        </ul>
        <ul>
          <li><a href="#inspecting-the-script">Inspecting the script</a></li>
        </ul>      
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>


<!-- ABOUT THE PROJECT -->
## About the project

<p align="center"><img src="groundwater_pollution_dk_files/figure-gfm/unnamed-chunk-34-1.png" alt="Logo" width="504" height="360"></p>
<p align="center"><em>Example visualization from the project, showing nitrate measurement placements and kriged nitrate concentrations in the groundwater </em>
</p>

**See [here](https://github.com/emiltj/groundwater_pollution_dk/blob/main/spatial_analytics_exam_2021.pdf) for the written report. The written report contains the motivation as well as an in-depth introduction to the topic, specifics to running the analysis, results and finally also a discussion of the project.**

The quality of Denmark’s groundwater supplies is under threat due to the use of nitrate in agriculture. The popular public opinion is that conventional agricultural farming contributes more to this negative development compared to organic agriculture. We wish to assess the scientific validity of this belief. Using kriging, linear modeling and coefficient t-tests, we carry out a spatial analysis comparing nitrate concentration levels in Denmark for conventional- and organic agricultural farming. Here, we find significantly higher nitrate concentrations for organic fields, with organic- and conventional fields having mean nitrate concentrations of 24.51 mg/L and 23.48 mg/L, respectively. Followingly, we discuss potential confounding factors in our analysis and their impact on our results. Furthermore, follow-up questions and prospects for relevant future research are discussed.

<!-- GETTING STARTED -->
## Getting started

To get a local copy up and running follow these simple example steps.

### Prerequisites

The spatial analysis requires data layers that exceed the maximum filesize on GitHub. To reproduce the analysis the script ```data/data_download.sh``` has been provided. It will automatically download the files contained within [a Google Drive folder](https://drive.google.com/drive/folders/1ZbnRr2CnVcMm0M2-v3AN7aOMlW5HMXfT?usp=sharing). 

For rerunning the analysis we therefore recommend cloning the repository, as well as using the provided script for downloading the data.
This can be done using the following lines in an unix-based bash:

```bash
git clone https://github.com/emiltj/spatial_exam.git
cd groundwater_pollution_dk
bash data_download.sh
```

<!-- REPOSITORY STRUCTURE -->
## Repository structure
This repository has the following structure:

| File | Description|
|--------|:-----------|
```groundwater_pollution_dk.md```| Markdown of the spatial analysis
```groundwater_pollution_dk.rmd```| Script used for the spatial analysis
```data/data_download.sh``` | Script which downloads the data required for the analysis
```data/nitrat.csv```| Groundwater samples containing information on nitrate and geographical coordinates of samples in the period 1900-2021.
```data/denmark_administrative_outline_boundary.*```| Shapefiles containing a map of Denmark.
```data/Markblok.*```| Shapefiles containing polygons of fields in Denmark in the period 1990-2021.
```data/Oekologiske_arealer.*```| Shapefiles containing polygons of organic field in 2018-2021
```README_images/*.png```| Images used for the README
```README.md``` | Readme with instructions
```LICENSE``` | [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0) which specifies the permitted usage of the repository

<!-- USAGE EXAMPLES -->
## Data

The data used in the analysis is all publicly available and has been acquired through the online portals of the respective ministries and software companies that are in possession of the data.
Note that the portals’ links and data availability may be deprecated in the future. However, in such instances access to the data can still nonetheless still be achieved through our script ```data_download.sh```. The four datasets that were used in our analysis are:

1. Point data with samples of nitrate levels in Denmark. This dataset contains 14,350 measurements of nitrate concentrations at different geographic locations in Denmark from 1900 to March 2021. The dataset was provided by courtesy of De Nationale Geologiske Undersøgelser for Danmark og Grønland (GEUS). The included variables used in our analysis are: coordinates, measurement date, nitrate concentration and measurement depth. The data was retrieved from their [webpage](https://data.geus.dk/geusmap/ows/help/?mapname=nitrat_2mg_and_above_aggr&epsg=25832).
2. A shapefile containing polygons of all current agricultural fields in Denmark as of April 2021.  This dataset is provided by the Ministry of Food, Agriculture and Fisheries of Denmark (Danish Agricultural Agency). The dataset was retrieved from the following [webpage](https://kortdata.fvm.dk/download/).
3. Shapefiles containing polygons of all organic agricultural fields in Denmark, registered each year between the period of 2012 to 2020. This dataset is provided by the Danish Agricultural Agency. The dataset was supposed to be publicly available through the Danish Agricultural Agency’s website, but since this was not the case, we were sent the following [link](https://filkassen.statens-it.dk/userportal/#/shared/public/0Kr0R6Oq9A3CqvRM/%C3%98kologiske%20arealer) to the dataset in a mail correspondence with the agency.
4. A shapefile containing a polygon in the shape of Denmark, courtesy of the software company IGIS MAP. The shapefile was retrieved from the their [webpage](https://www.igismap.com/).


<!-- USAGE EXAMPLES -->
## Usage

### Running the script

After cloning the repository and downloading the required data, open up the <a href="groundwater_pollution_dk.md">```groundwater_pollution_dk.rmd```</a> R markdown in Rstudio (see written report for version specifics). Running the code, top-down should result in a direct access to the analysis the lays the foundation for our project report.

### Inspecting the script

As an alternative to rerunning our script, you may merely want to inspect the code and the output.
For simply examining the analysis and its results, we recommend inspecting the markdown version of the analysis <a href="groundwater_pollution_dk.md">```groundwater_pollution_dk.md```</a>.

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are greatly appreciated.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b analysis/extended_analysis`)
3. Commit your Changes (`git commit -m 'Add some extended_analysis'`)
4. Push to the Branch (`git push origin analysis/extended_analysis`)
5. Open a Pull Request

<!-- LICENSE -->
## License
Distributed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0). See ```LICENSE``` for more information.

<!-- CONTACT -->
## Contact

Feel free to write the authors, Emil Jessen or Johan Horsmans for any questions regarding the scripts.
You may do so on Slack ([Emil](https://app.slack.com/client/T01908QBS9X/D01A1LFRDE0), [Johan](https://app.slack.com/client/T01908QBS9X/D01BDPKT3BL))

<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [RStudio](https://www.rstudio.com/) - Software used for conducting the analysis
* [GEUS-DATA](https://www.geus.dk/) - Data portal for geological investigations in Denmark/Greenland
* [Danish Agricultural Agency](https://lbst.dk/landbrug/kort-og-markblokke/) - The Danish Agricultural Agency portal, containing geographical information on land use 
* [README template](https://github.com/othneildrew/Best-README-Template) - README template by othneildrew
* [Rstudio](https://www.rstudio.com/) - Software used for conducting the analysis
* [Overleaf](https://www.overleaf.com/) - Software used to format and write the report
