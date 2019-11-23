# Docker_Shiny_App

Docker app with R Shiny app copied into container 

Referencing docker:container from 

https://github.com/dunhampa/Docker_Shiny

This is the name of image referenced in this docker file. It may need to be rebuilt from the directory from the other reference. It's 'geo-leaflet'

## Build Instructions

```
docker build -t int-app-shiny .
```

and then:

```
docker run -p 3838:3838 -p 8787:8787  -e PASSWORD=test123   -v ~/srv/home/rstudio:/home/rstudio int-app-shiny
```

and then can go to:

```
http://localhost:3838/ohio-county-birth-weights/
```