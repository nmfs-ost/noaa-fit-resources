---
title: "Share Web Applications with RStudio"
excerpt: "RStudio Products"
date: 2021-07-01
toc: true
categories:
  - onboarding
tags:
  - resources
  - R
  - RStudio
---

Shiny server, shinyapps.io, and RStudio Connect are all ways to share web applications and interactive documents. Once you’ve written a [Shiny application](https://shiny.rstudio.com/articles/basics.html), you can either [share your app to run locally](https://shiny.rstudio.com/articles/basics.html) or make it available to anyone who has a web browser. To make it available via web browser, you can either host the application on your own server or on an RStudio server virtually. Below is a brief overview of the available RStudio products and how they differ. For a more comprehensive comparison see the [comparison on the RStudio website](https://www.rstudio.com/products/shiny/shiny-server/), [‘Deploying Shiny Apps to the Web,’](https://shiny.rstudio.com/articles/deployment-web.html) and [‘Hosting and Deployment.’](https://shiny.rstudio.com/deploy/)

More information about Shiny for RStudio, including video and written tutorials, [here](https://shiny.rstudio.com/tutorial/).

## RStudio Products

### [Shiny server](https://www.rstudio.com/products/shiny/shiny-server/)

An open source, back end program that builds a web server designed to host Siny applications. On Shiny Server you can host your apps in a controlled environment, like inside your organization, so your Shiny app (and whatever data it needs) will never leave your control. You can also use Shiny Server to make your apps available across the Internet when you choose. Shiny Server will host each app at its own web address and automatically start the app when a user visits the address. When the user leaves, Shiny Server will automatically stop the app. More information about Shiny Server features [here](https://shiny.rstudio.com/articles/shiny-server.html).

### [Shinyapps.io](https://www.shinyapps.io/)

Another way to share Shiny apps and interactive documents if you prefer to have RStudio host the Shiny applications. You don’t need to own a server, or know how to configure a firewall to deploy and manage applications in the cloud, and you can easily deploy to the web at the push of a button (or one line of R code). No hardware, installation, or annual purchase contract required. When using shinyapps.io, your code and data must be copied to RStudio servers since it is hosted by RStudio. More information about using shinyapps.io [here](https://docs.rstudio.com/shinyapps.io/index.html).

### [RStudio Connect](https://www.rstudio.com/products/connect/)

RStudio’s publishing platform. You can share Shiny applications, R Markdown reports, dashboards, plots, APIs, and more. Use push-button publishing from the RStudio IDE, scheduled execution of reports, and flexible security policies. More information about RStudio Connect [here](https://www.rstudio.com/products/connect/?_ga=2.81644759.1748737478.1624996316-492922235.1612387008). Also see the [RStudio Connect Demo](https://noaa-fisheries-integrated-toolbox.github.io/resources/onboarding/rstudio-connect/) for NOAA Fisheries to learn how RStudio Connect can be used by NOAA scientists. 
