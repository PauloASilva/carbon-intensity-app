[![update data](https://github.com/KKulma/carbon-intensity-app/actions/workflows/schedule.yml/badge.svg)](https://github.com/KKulma/carbon-intensity-app/actions/workflows/schedule.yml)        [![deploy](https://github.com/KKulma/carbon-intensity-app/actions/workflows/deploy.yml/badge.svg)](https://github.com/KKulma/carbon-intensity-app/actions/workflows/deploy.yml)

# How much electricity in UK comes from low-carbon sources?

Our electricity is not made equal and can be associated with higher or lower carbon intensity. How much of UK's electricity is produced using low-carbon sources? Has this proportion decreased or increased over time? [This Shiny app](https://kasiakulma.shinyapps.io/carbon-intensity-app/) will help answer these questions.

The web app and the underlying data pipeline was built using open source tools. Web app's front-end was built using Shiny, electricity composition was extracted from National Grid's [Carbon Intensity API](https://carbonintensity.org.uk/) using [{intensegRid}](https://kkulma.github.io/intensegRid/articles/intro-to-carbon-intensity.html) package. Data and deployment pipelines were developed using GitHub Actions: `schedule.yml` pulls the carbon intensity data from the API, saves it in `data/daily_ci.rds` file daily and pushes the changes to the repo; `deploy.yml` deploys the changes to the [shinyapps.io server](https://kasiakulma.shinyapps.io/carbon-intensity-app/) on push. 



 
