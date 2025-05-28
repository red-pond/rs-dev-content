---
title: Program XML
---

### Quick Link:

Validating your `program.xml` file can be done using the following URL:

```
https://raw.githubusercontent.com/Riverscapes/Program/master/Program/XSD/V1/Program.xsd
```

like so:

``` xml
<?xml version="1.0" encoding="utf-8"?>
<Program name="Riverscapes" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:noNamespaceSchemaLocation="https://raw.githubusercontent.com/Riverscapes/Program/master/Program/XSD/V1/Program.xsd">
```

## Background:

We need a way to represent the bucket file structure and hold that structure
programatically so that products can find their homes when they upload and also
so users can find the products they care about.

The following is meant to completely describe the ideas of the following document:
<https://docs.google.com/spreadsheets/d/1PBTDZ_R_fdjydQ8jXVQr1Uf5OCOrzXhkfu9wSvvliIQ/>

So according to this, you would be able to find the output of a fuzzy FHM product like so:
`/ColumbiaRiverBasin/JohnDay/Sites/CBW05583-028079/VISIT_1029/2012/Q_001/Analyses/Fuzzy/Steelhead/Spawner/FHM/outputs/fuzzyHSI.tif`

We do this using some basic building blocks:

* `<Container name="Network"> `: A container is a folder literally called what the name is "Network" in this case
* `<Level name="Watershed"> `: A level will have repeating elements. So instead of "Watershed" you'll have lots
     of folders, each wih the name of the Level (Watershed in this case) in question/
* `<Product>` : Products are the endpoint. If I can find a product then I can download or upload a whole project

```xml
<?xml version="1.0" encoding="utf-8"?>
<Program name="Riverscapes" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:noNamespaceSchemaLocation="Program.xsd">
  <MetaData>
    <Meta name="s3bucket">riverscapesdata</Meta>
  </MetaData>
  <Level name="Region">
    <Level name="Watershed">
        <Container name="Watershed">
          <Product name="GRTS Rollup" id="GRTS" folder="grts"/>
          <Product name="Context Layers" id="context" folder="context_layers"/>
        </Container>
        <Container name="Network">
          <Product name="BRAT Models" id="BRAT" folder="brat"/>
            <Product name="WRAT" id="WRAT" folder="wrat"/>
            <Product name="Matt Imputation Crap" id="MIC" folder="matt_impute"/>
            <Product name="GPP" id="GPP" folder="gpp"/>
            <Product name="Capacity" id="capacity" folder="capacity"/>
            <Product name="River Styles" id="RSTYLES" folder="riverstyles"/>
        </Container>
        <Container name="Sites">
          <Level name="Site">
            <Level name="Visit">
              <Level name="Year">
                <Level name="Flow">
                  <Product name="FHM" id="FHM" folder="FHM"/>
                  <Product name="GUT" id="GUT" folder="GUT"/>
                  <Product name="GCD" id="GCD" folder="GCD"/>
                </Level>
                <Container name="Topography">
                  <Product name="DEM" id="DEM" folder="DEM"/>
                </Container>
              </Level>
            </Level>
          </Level>
        </Container>
    </Level>
  </Level>
</Program>
```
