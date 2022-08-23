# Data Dispatches

[Data Dispatches](https://jhu-data-services.github.io/data-dispatches/)

## Installation

This blog is built in [Quarto](https://quarto.org/). Quarto is a
language-agnostic scientific and technical publishing system built on
Pandoc.

To install `Quarto`, visit [Quarto Get
Started](https://quarto.org/docs/get-started/) and select the Quarto
command line interface (CLI) approrpiate to your operating system.

Ensure that you have the appropriate languages installed for the
documents you would like to render. For example, if you are rendering
both `*.Rmd` and `*.ipynb` files, make sure you have `R` and `Python`
installed.

## Usage

Begin by cloning the Data Dispatches repository to a directory of your preference:

`git clone git@github.com:jhu-data-services/data-dispatches.git`

To compile the project:

`cd data-dispatches`

`quarto render`

The rendered website will be added to `/docs`. 

## Configuration

Configuration of the Data Dispatches website is accomplished by setting parameters within the `_quarto.yml` project file.

To understand the structure of the `_quarto.yml` details are provided for each of the `_quarto.yml` sections.

### Project

``` yaml
project:
  type: website
  output-dir: docs
```

### Website

``` yaml
website:
  title: "Data Dispatches - JHU Data Services"
  reader-mode: false
  page-navigation: true
  search:
    location: sidebar
```

#### Navbar

``` yaml
  navbar: 
    logo: logos/data-dispatches-white.png
    background: primary
    right: 
    - icon: github
      href: https://github.com/jhu-data-services
    - icon: globe 
      href: https://dataservices.library.jhu.edu/
    - text: "Help"
      menu:
        - text: "Report an Issue"
          icon: "bug"
          href: "https://github.com/jhu-data-services/data-dispatches/issues"
        - text: "Get Help"
          icon: "chat-right-text"
          href: "https://v2.libanswers.com/chati.php?hash=8b19eda5bc7bc7b80e623cad56abdd12"
```

#### Sidebar

``` yaml
  sidebar: 
    - id: dispatches
      title: "Data Tutorials"
      style: "floating"
      search: true
      collapse-level: 2
      contents:
        - index.qmd
        - section: "Data Visualization"
          contents:
            - dispatches/data-visualization/custom-ggplot2-theme.qmd
```

##### Page Footer

``` yaml
  page-footer: 
    background: primary
    left: "Copyright 2022, JHU Data Services." 
    right: "This site was built with [Quarto](https://quarto.org/)."
```

#### Format

``` yaml
format:
  html:
    theme: litera 
    css: styles.css
    toc: true
```

#### Editor

``` yaml
editor: visual
```

## Contributing

Submit a pull-request to add new content to the Data Dispatches site.
