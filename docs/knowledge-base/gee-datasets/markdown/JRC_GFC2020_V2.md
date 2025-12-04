



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

EC JRC global map of forest cover 2020, V2


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================================








Dataset Availability
2020\-12\-31T00:00:00Z–2020\-12\-31T00:00:01Z
Dataset Provider


[Joint Research Centre, European Commission](https://forest-observatory.ec.europa.eu/forest/)



Earth Engine Snippet


`ee.ImageCollection("JRC/GFC2020/V2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GFC2020_V2)





Cadence
1 Year
Tags


[eudr](/earth-engine/datasets/tags/eudr)
[forest](/earth-engine/datasets/tags/forest)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[jrc](/earth-engine/datasets/tags/jrc)








#### Description



The global map of forest cover provides a spatially explicit representation
of forest presence and absence for the year 2020 at 10m spatial resolution.


The year 2020 corresponds to the cut\-off date of the Regulation from the
European Union "on the making available on the Union market and the export
from the Union of certain commodities and products associated with
deforestation and forest degradation" (EUDR, Regulation (EU) 2023/1115\).
In the context of the EUDR, the global forest cover map can be used as a
non\-mandatory, non\-exclusive and not legally binding source of information.
Further information about the map and its use can be found on the [EU
Observatory on Deforestation and Forest Degradation](https://forest-observatory.ec.europa.eu/forest/) (EUFO) and namely in
the section on Frequently Asked Questions.


Forest means land spanning more than 0\.5 hectares with trees higher than
5 meters and a canopy cover of more than 10%, or trees able to reach those
thresholds in situ, excluding land that is predominantly under agricultural
or urban land use. Agricultural use means the use of land for the purpose of
agriculture, including for agricultural plantations (i.e. tree stands in
agricultural production systems such as fruit tree plantations, oil palm
plantations, olive orchards and agroforestry systems) and set\- aside
agricultural areas, and for rearing livestock. All plantations of relevant
commodities other than wood, that is cattle, cocoa, coffee, oil palm,
rubber, soya are excluded from the forest definition.


The global map of forest cover was created by combining existing global
spatial layers (wall\-to\-wall or global in their scope), e.g. on land cover,
land use, and tree height. The map aims to represent the state of forest
cover by 31 December 2020\. The global land cover from the ESA World Cover
project serves as one baseline layer to define the extent of tree cover for
year 2020 at 10 m spatial resolution. In 2024, the global map of forest
cover 2020 was improved by integrating user feedback, and new or revised
spatial data layers.


It now better captures temporally unstocked forests, low\-density
tropical forests, and secondary tropical forests that have regrown for at
least five years. Additionally, the exclusion criteria have been enhanced
to more effectively exclude trees in urban areas, mining sites, wetlands,
areas with shifting cultivation, and tree plantations. This is achieved by
utilizing multiple global maps of canopy height, crop area, and specific
crop commodity maps to more accurately distinguish forests from trees
under agricultural use.


For direct access and metadata, please consult the JRC
data catalogue ([JRC 2024](https://data.jrc.ec.europa.eu/dataset/e554d6fb-6340-45d5-9309-332337e5bc26)). A technical report ([Bourgoin et al 2025](https://op.europa.eu/en/publication-detail/-/publication/e2c286ac-14e9-11f0-b1a3-01aa75ed71a1/language-en))
describes the mapping approach for the second version. The accuracy
assessment of the Global Forest Cover map is described in a
[separate report](https://op.europa.eu/en/publication-detail/-/publication/e86f56dd-15b5-11f0-b1a3-01aa75ed71a1/language-en).


The global map of forest cover may be revised if
new information, additional large\-scale data layers, or revised global
spatial data layers will be made available for year 2020\.


For a list of known issues please refer to [this website](https://forobs.jrc.ec.europa.eu/GFC).





### Bands



**Pixel Size**
  
10 meters



**Bands**




| Name | Description |
| --- | --- |
| `Map` | Global forest cover 2020 |


**Map Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#4d9221 | Forest |




### Terms of Use


**Terms of Use**


The data may be used by anyone, anywhere, anytime without permission,
license or royalty payment. Attribution using the recommended citation
is requested.




### Citations



Citations:
* Bourgoin, Clement; Verhegghen, Astrid; Degreve, Lucas; Ameztoy, Iban;
Carboni, Silvia; Colditz, Rene; Achard, Frederic (2024\): Global map of
forest cover 2020 \- version 2\. European Commission, Joint Research
Centre (JRC) \[Dataset]
PID: [http://data.europa.eu/89h/e554d6fb\-6340\-45d5\-9309\-332337e5bc26](http://data.europa.eu/89h/e554d6fb-6340-45d5-9309-332337e5bc26)
* Bourgoin, C., Verhegghen, A., Carboni, S., Degreve, L., Ameztoy Aramendi, I., Ceccherini, G., Colditz, R. and Achard, F., Global Forest Maps for the Year 2020 to Support the EU Regulation on Deforestation\-free Supply Chains, Publications Office of the European Union, Luxembourg, 2025, [https://data.europa.eu/doi/10\.2760/1975879](https://data.europa.eu/doi/10.2760/1975879), JRC141702\.
* Colditz, R., Verhegghen, A., Carboni, S., Bourgoin, C., Duerauer, M., Mansuy, N., De Marzo, T., Beuchle, R., Janouskova, K., Armada Bras, T., Desclée, B., Orlowski, K., Mutendeudzi, M., Ameztoy Aramendi, I., Fritz, S., Lesiv, M., Oom, D., Carreiras, J., San\-Miguel, J., Herold, M., Berger, K., Nepomshina, O., Gond, V., Defourny, P., Lamarche, C., Bos, A., Collet, T., Delhez, B., Mollicone, D., Bastin, J.\-F., De Haulleville, T., Brink, A., Lupi, A., Tsendbazar, N.E., Stehman, S.V. and Achard, F., Accuracy Assessment of the Global Forest Cover Map for the Year 2020: Assessment Pro\-tocol and Analysis, Publications Office of the European Union, Luxembourg, 2025, [https://data.europa.eu/doi/10\.2760/7632707](https://data.europa.eu/doi/10.2760/7632707), JRC141231\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varimage2020=ee.ImageCollection('JRC/GFC2020/V2').mosaic();

varvisualization={
bands:['Map'],
palette:['4D9221']};

Map.setCenter(0.0,0.0,2);

Map.addLayer(image2020,visualization,'EC JRC Global forest cover 2020 – V2');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GFC2020_V2)


[EC JRC global map of forest cover 2020, V2](/earth-engine/datasets/catalog/JRC_GFC2020_V2)

The global map of forest cover provides a spatially explicit representation of forest presence and absence for the year 2020 at 10m spatial resolution. The year 2020 corresponds to the cut\-off date of the Regulation from the European Union "on the making available on the Union market and the export …

 JRC/GFC2020/V2,
 eudr,forest,forest\-biomass,jrc

2020\-12\-31T00:00:00Z/2020\-12\-31T00:00:01Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








