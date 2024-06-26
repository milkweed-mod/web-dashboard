<h1 align="center">

MilkweedMod

</h1>

<h2 align="center">

**Identifying Priority Survey Sites for Early-Season Milkweed Conservation**

</h2>

<h2 align="center">

<img src = "https://github.com/MEDS-SBBG-milkweed/.github/assets/98177666/b98e752a-194c-4e54-8623-15ef18f8409b" alt="MilkweedMod capstone group hexsticker. Dark green background with a white outline of California, filled in with illustrated milkweed plants and an orange monarch butterfly accompanying the text Milkweed Mod" width="300">

<h2 align="center">

**Milkweed Site Finder Dashboard**

</h2>

## Table of Contents

[Project Description](##project-description)

[Data](#data)

[Usage](#usage)

[Repository Structure](#repository-structure)

[Disclaimer](#disclaimer)

[Authors](#authors)

[Client](#client)

## Project Description
The milkweed-site-finder repository contains all of the R code in order to build the Rshiny interactive web dashboard to facilitate field survey planning for the Santa Barbara Botanic Garden staff for identifying high priority survey locations for early-season milkweed in the Los Padres National Forest (LPNF). For additional information regarding the Milkweed Site Finder Dashboard please visit the [Bren project page and technical documentation](https://bren.ucsb.edu/projects/identifying-priority-survey-sites-early-season-milkweed-conservation). for this project.
 
## Data
All data products hosted in this dashboard can be found in the [milkweed-mod](https://github.com/milkweed-mod/milkweed-mod) repository within the [MEDS-SBBG-milkweed](https://github.com/MEDS-SBBG-milkweed) GitHub organization. 

## Usage

### Home

The **Home** page of the RShiny dashboard contains background information about the project and links to where additional information about the code can be found. The homepage also contains a disclaimer as provided by the Forest Service regarding data collection.

</h2>

<img src="https://github.com/MEDS-SBBG-milkweed/milkweed-site-finder/blob/main/figs/home.png" alt="Home Page of Milkweed Site Finder Dashboard">

### Milkweed Locations

The **Milkweed Locations** page of the RShiny dashboard contains information regarding the Santa Barbara Botanic Garden’s first year of field surveys. This information is displayed in a map in which a user can select the species or combinations  of early-season milkweed species they would like to see. This map indicates the general location a data point was collected at.

</h2>

<img src="https://github.com/MEDS-SBBG-milkweed/milkweed-site-finder/blob/main/figs/milkweed_locations.png" alt="Milkweed Locations Tab of Milkweed Site Finder Dashboard">

### Milkweed Habitat Suitability

The **Milkweed Habitat Suitability** page of the RShiny dashboard contains information and the general approach used to create habitat suitability models for each of the four early-season milkweed species. These habitat suitability models are displayed as a heatmap in a grid pattern on this page to allow for visual comparison. Additionally, there is a map of maximum habitat suitability for all four species which represents the overall likelihood of finding any of the early-season milkweed across the LPNF.

</h2>

<img src="https://github.com/MEDS-SBBG-milkweed/milkweed-site-finder/blob/main/figs/habitat_suitability_models.png" alt="Milkweed Habitat Suitability Tab of Milkweed Site Finder Dashboard">

### Survey Site Accessibility

The **Survey Site Accessibility** page of the RShiny dashboard contains information and the general approach used to create a survey site accessibility index for the LPNF. The survey site accessibility index is displayed using two maps. The map on the left side of the dashboard page allows a user to select the layer of the site accessibility index they would like to examine. The map on the right side of the dashboard page shows the total site accessibility index for the LPNF.

</h2>

<img src="https://github.com/MEDS-SBBG-milkweed/milkweed-site-finder/blob/main/figs/survey_site_accessibility.png" alt="Survey Site Accessibility Tab of Milkweed Site Finder Dashboard">

### High-Priority Survey Sites

The **High-Priority Survey Sites** page of the RShiny dashboard contains information and the general approach used to the create the survey site priority score for each species of early-season milkweed. The user is able to select which species they would like to visualize the survey site priority score across the LPNF for. Additionally, there is a data table at the bottom of the page which has a row for each raster cell of the LPNF that contains information about the Latitude, Longitude, Priority scores for each species, Site Accessibility Index score, as well as whether or not that location has been visited by the SBBG team. This datatable is able to be downloaded as a csv, or an excel file. 

</h2>

<img src="https://github.com/MEDS-SBBG-milkweed/milkweed-site-finder/blob/main/figs/high_priority.png" alt="High-Priority Survey Site Tab of Milkweed Site Finder Dashboard">

### Data

The **Data** page of the RShiny dashboard contains a general description, citation, and licensing information for the data used to create this project. 

</h2>

<img src="https://github.com/MEDS-SBBG-milkweed/milkweed-site-finder/blob/main/figs/data.png" alt="Data Tab of Milkweed Site Finder Dashboard">


## Repository Structure
```
├── .gitignore 
├── figs                      # folder containing figures used in README.md
│   ├── data.png
│   ├── habitat_suitability_models.png
│   ├── high_priority.png
│   ├── home.png
│   ├── milkweed_locations.png
│   ├── MilkweedMod.jpeg
│   └── survey_site_accessibility.png
├── global.R
├── LICENSE
├── milkweed-site-finder.Rproj
├── R
│   └── addLegend_decreasing.R        # function to create legend in leaflet
├── README.md
├── rsconnect                         # folder for app deployment
│   └── shinyapps.io
│       └── mwidas                    # this will change to username of account
│           └── milkweed-site-finder.dcf
├── server.R
├── session_info.txt      # session_info and operating system information
├── text    # folder containing all markdown files used and where text is stored
│   ├── authors.md
│   ├── background_context.md
│   ├── background_info.md
│   ├── disclaimer.md
│   ├── habitat_suitability_all.md
│   ├── high_priority_table.md
│   ├── overview_data.md
│   ├── overview_habitat_suitability.md
│   ├── overview_milkweed_locations.md
│   ├── overview_site_accessibility.md
│   ├── overview_site_finder.md
├── ui.R
└── www                                 # graphics folder
    ├── fonts
    │   ├── 5cfb33b712cbdaf9310b.woff2
    │   ├── ab9aea6faeaea5115410.woff2
    │   ├── bace964bccc02d90d74e.woff2
    │   ├── da1fdeda6d5756ee6227.ttf
    │   ├── ebec98131cf900cb698e.woff2
    │   └── edfac2e6370304cd74ae.woff2
    ├── monarch_milkweed.jpeg
    ├── sass-style.css
    ├── sass-style.scss                # sass file for styling 
    └── SBBG_logo.png
```

## Disclaimer

**Plant and seed collection on Forest Service land is not permissible without a plant collection permit from the Los Padres National Forest.**

This project was completed as a part of the [Master of Environmental Data Science](https://bren.ucsb.edu/masters-programs/master-environmental-data-science) program at the Bren School of Environmental Science & Management at the University of California, Santa Barbara. 

## Authors
 Amanda Herbst { [GitHub](https://github.com/amandaherbst) | [Website](amandaherbst.github.io) | [LinkedIn](https://www.linkedin.com/in/amanda-herbst/) }

 Anna Ramji { [GitHub](https://github.com/annaramji) | [Website](https://annaramji.github.io/) | [LinkedIn](https://www.linkedin.com/in/annaramji/) }

 Melissa Widas { [GitHub](https://github.com/mwidas) | [Website](https://mwidas.github.io/) | [LinkedIn](https://www.linkedin.com/in/mwidas/) }

 Sam Muir { [GitHub](https://github.com/shmuir) | [Website](https://shmuir.github.io/) | [LinkedIn](https://www.linkedin.com/in/shmuir/) }

## Client
Dr. Sarah Cusser, Terrestrial Invertebrate Conservation Ecologist

Santa Barbara Botanic Garden <br>
1212 Mission Canyon Rd. <br>
Santa Barbara, CA 93105


