
<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/emiltj/groundwater_pollution_dk">
    <img src="logo.png" alt="Logo" width="40" height="65">
  </a>

  <h3 align="center">Groundwater pollution and farm use in Denmark</h3>

  <p align="center">
    Spatial analysis exam project 2021
    <br />
    <a href="https://github.com/emiltj/groundwater_pollution_dk"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/emiltj/groundwater_pollution_dk">View Demo</a>
    ·
    <a href="https://github.com/emiltj/groundwater_pollution_dk/issues">Report Bug</a>
    ·
    <a href="https://github.com/emiltj/groundwater_pollution_dk/issues">Request Feature</a>
  </p>
</p>

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#repository-structure">Repository Structure</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

<img src="analysis_example.png" alt="Logo" width="375" height="295">

This project analyzes the relationship between land use and nitrate pollution in the groundwater in Denmark. It investigates the ... bla. bla...

Why this analysis?
* Y
* Y
* Y

Findings of the analysis:
* Y
* Y
* Y

Of course,

### Built With

This project has been built using already existing publically available software and data. 
* [RStudio](https://www.rstudio.com/) - Software used for conducting the analysis
* [GEUS-DATA](https://www.geus.dk/) - Data portal for geological investigations in Denmark/Greenland
* [Danish Agricultural Agency](https://lbst.dk/landbrug/kort-og-markblokke/) - The Danish Agricultural Agency portal, containing geographical information on land use 

<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple example steps.

### Prerequisites

The spatial analysis requires data layers that exceed the maximum filesize on GitHub. To reproduce the analysis the script ```data/data_download.rmd``` has been provided. It will automatically download the files contained within [a Google Drive folder](https://drive.google.com/drive/folders/1ZbnRr2CnVcMm0M2-v3AN7aOMlW5HMXfT?usp=sharing). 

For rerunning the analysis we therefore recommend cloning the repository, as well as using the provided script for downloading the data.
This can be done using the following lines in an unix-based bash:

```bash
git clone https://github.com/emiltj/spatial_exam.git
cd groundwater_pollution_dk/data
bash data_download.sh
```

<!-- REPOSITORY STRUCTURE -->
## Repository structure
This repository has the following directory structure:

| Column | Description|
|--------|:-----------|
```spatial_analysis.md```| Markdown of the spatial analysis
```spatial_analysis.rmd```| Script used for the spatial analysis
```data/``` | Folder which contains the data required for the analysis
```data/data_download.sh``` | Script which downloads the data required for the analysis
```README.md``` | Readme with instructions
```LICENSE``` | [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0) which specifies the permitted usage of the repository


<!-- USAGE EXAMPLES -->
## Usage

For simply examining the analysis and its results, we recommend inspecting the markdown version of the analysis.
* <a href="groundwater_pollution_dk.md">```spatial_analysis.md```</a>

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are greatly appreciated.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Data layers
After running ```data/data_download.sh``` the data layers will have been downloaded to ```data/```

## Contributions

## License
Distributed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0). See ```LICENSE``` for more information.


## Contact

Feel free to write the authors, Emil Jessen or Johan Horsmans for any questions regarding the scripts.
You may do so on Slack ([Emil](https://app.slack.com/client/T01908QBS9X/D01A1LFRDE0), [Johan](google.dk))
