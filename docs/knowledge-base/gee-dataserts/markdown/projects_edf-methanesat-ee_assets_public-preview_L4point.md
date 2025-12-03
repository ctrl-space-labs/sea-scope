



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MethaneSAT L4 Point Sources Public Preview V1\.0\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================================









info


 This dataset is part of a Publisher Catalog, and not managed by Google Earth Engine.
 
 Contact [EDF\-MethaneSAT](https://www.methanesat.org/contact)
 
 for bugs or [view more datasets](https://developers.google.com/earth-engine/datasets/publisher/edf-methanesat-ee)
 from the Environmental Defense Fund \- MethaneSAT Catalog. [Learn more about Publisher datasets](/earth-engine/datasets/publisher).
 






Catalog Owner
Environmental Defense Fund \- MethaneSAT
Dataset Availability
2024\-06\-14T00:00:00Z–2025\-01\-17T00:00:00Z
Dataset Provider


[Environmental Defense Fund \- MethaneSAT](https://methanesat.org)


Contact
[EDF\-MethaneSAT](https://www.methanesat.org/contact)

Earth Engine Snippet


`ee.FeatureCollection("projects/edf-methanesat-ee/assets/public-preview/L4point")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/edf-methanesat-ee/projects_edf-methanesat-ee_assets_public-preview_L4point)





Tags


[atmosphere](/earth-engine/datasets/tags/atmosphere)
[climate](/earth-engine/datasets/tags/climate)
[edf](/earth-engine/datasets/tags/edf)
[edf\-methanesat\-ee](/earth-engine/datasets/tags/edf-methanesat-ee)
[emissions](/earth-engine/datasets/tags/emissions)
[ghg](/earth-engine/datasets/tags/ghg)
[methane](/earth-engine/datasets/tags/methane)
[methanesat](/earth-engine/datasets/tags/methanesat)
[publisher\-dataset](/earth-engine/datasets/tags/publisher-dataset)
[table](/earth-engine/datasets/tags/table)








#### Description



This early "Public Preview" dataset provides high precision data for methane emissions from
discrete point sources. These methane emission fluxes were produced using a point source
detection and emissions quantification framework specialized to exploit the high spatial
resolution, wide spatial coverage, and high precision of MethaneSAT data (methodology is
described in [Chulakdabba et al. (2023\)](https://doi.org/10.5194/amt-16-5771-2023).)
The point source quantification framework was extensively tested in blind controlled\-release
experiments as detailed in
[Chulakdabba et al. (2023\)](https://doi.org/10.5194/amt-16-5771-2023) and
[Abbadi et al. (2024\)](https://doi.org/10.1021/acs.est.4c02439). 


Total emissions for a scene–from both dispersed area and point source emissions–may be
obtained by summing the area emissions and point source emissions for a given collection ID
(see L4 Area Sources Public Preview).


Not all data products (L3 concentration, L4 area and L4 points) are available for all
collection IDs. Contact the data provider for more information about the project at this link:
<https://www.methanesat.org/contact/>.




---


7/2/2025 Important Update: 


As you may be aware, we recently lost contact with the satellite. After exploring all possible  

recovery options, we have now confirmed that it is no longer functioning, due to an
undetermined problem with the outer platform carrying our methane detector. While there is no
question this is a setback, we are undeterred in our efforts to drive down methane pollution.
Please see our official statement here:
[MethaneSAT Loses Contact with Satellite \| MethaneSAT](https://www.methanesat.org/project-updates/methanesat-loses-contact-satellite).


What this means for the Public Preview data: The existing datasets will remain accessible on
Google platforms and on our web portal for the foreseeable future. Additionally, over the next
few months, we will release substantial new data collected by MethaneSAT prior to the loss of
contact. This will include hundreds of scenes (of targets that are roughly 200kmx200km). We
hope this will be useful for you. Should there be any changes to data availability, we will
notify you well in advance.


Looking ahead: While we don’t have all the answers yet, we plan to leverage our advanced Data
Processing Platform (DPP) to quantify other streams of satellite and/or aerial data. We will
also take the necessary time to evaluate the best next step in our efforts to enable methane
reductions. To stay up to date with further updates, feel free to sign up for our
[newsletter](https://mailchi.mp/methanesat/methanesat-newsletter-sign-up).
For additional information about the MethaneAIR instrument, instrument
calibration and emission detections, please refer to recent publications by
[Loughner et al. (2021\)](https://doi.org/10.1175/JAMC-D-20-0158.1),
[Staebell et al. (2021\)](https://doi.org/10.5194/amt-14-3737-2021),
[Conway et al. (2023\)](https://doi.org/10.5194/amt-2023-111),
[Chulakadabba et al. (2023\)](https://doi.org/10.5194/egusphere-2023-822),
[Abbadi et al. (2023\)](https://doi.org/10.31223/X51D4C),
[Omara et al. (2023\)](https://doi.org/10.5194/essd-15-3761-2023),
and [Miller et al. (2023\)](https://doi.org/10.5194/egusphere-2023-1962).


Contact the data provider for more information about the project at this
link: <https://www.methanesat.org/contact/>





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| collection\_id | STRING | Satellite observation identifier. |
| date | STRING | Data collection date format STRING (ISO 8601\). |
| flux | INT | Methane flux quantification. Note: this may be null in the case that we're confident in the presence and location of the point but not its flux value. |
| flux\_sd | INT | Standard deviation of methane flux quantification, in kg/h. Note: this may be null in the case that we're confident in the presence and location of the point but not its flux value. |
| processing\_id | STRING | (internal) Processing run identifier that represents the calculations that led to the features. It is not an attribute describing the flight, but the processing pipeline. |
| plume\_id | STRING | Plume id (unique across satellite observations). |
| plume\_id\_in\_scene | INT | Plume id (unique per satellite observation). |
| region | STRING | Region of scene. |
| target\_id | INT | Satellite Target ID. |




### Terms of Use


**Terms of Use**


Use of this data is subject to [MethaneSAT's Content License Terms of Use](https://www.methanesat.org/sites/default/files/2025-02/MethaneSAT%20-%20Content%20License%20Terms%20of%20Use%20%28Revised%202-12-2025%29%5B25%5D.pdf).


YOUR LICENSE TO ACCESS THE DATA


* We hereby grant you a limited, nonexclusive, nonassignable, nontransferable, revocable license to use, reproduce, publish, make derivative works, display and perform publicly any Data first made available through the Platform pursuant to the terms set forth herein, subject to your agreement to, compliance with and satisfaction of these Terms of Use (the “License”)
* You agree to and acknowledge the following restrictions relating to the License:


	+ (1\) To access the Data, you must complete this [Request Form](https://docs.google.com/forms/d/e/1FAIpQLSdzJDwpTs99tMT5bGk0gep10_UEHi64kGtJWat1FrP8ZjwQcA/viewform), which will ask for your contact information, intended use cases, target customers, and other details that will assist MethaneSAT’s understanding of how the Data is being used by you, and, upon submission of such form, MethaneSAT may (in its sole discretion) grant you access to the Data;
	+ (2\) With respect to certain aspects of the Data as described herein, you may use methane concentrations, in parts per billion or any other unit of concentration (“Level 3 Data” or “L3 Data”) and methane emission fluxes, in kilograms per hour (“Level 4 Data” or “L4 Data”) for:
	
	
		- (i) internal business evaluation and testing,
		- (ii) commercial applications, such as developing and selling derivative products and services that incorporate or are informed by the L3 Data or L4 Data,
		- (iii) distribution of the Data made available herein to wholly controlled affiliates of which you will be responsible and liable on their behalf for adherence to these Terms of Use, or
		- (iv) methane mitigation activities, including both commercial and non\-commercial initiatives;
	+ (3\) You are strictly prohibited from using L3 Data to calculate or derive L4 Data or any similar outputs, except and exclusively for internal use purposes and not to distribute to any third party;
	+ (4\) You may not distribute, publish, sublicense, sell, or otherwise provide L3 Data or L4 Data in its raw form to any third parties, provided, however, that you may develop, commercialize, and sell derivative products and services based on your review of the L3 Data and L4 Data, provided, further (and for the avoidance of doubt), that the underlying L3 Data and L4 Data (in its raw form) shall not be shared nor made directly accessible to end users/third parties; and
	+ (5\) That you are not permitted to distribute the Data on any other platform that would make the Data available to third parties, other than to you and your wholly controlled affiliates.
* As a condition of accessing the Data, you further agree and acknowledge that:


	+ (1\) MethaneSAT seeks information about how the Data will be used and, as such, you shall use best efforts, upon request by MethaneSAT, that you will
	
	
		- (i) provide feedback on the quality of the Data and any proposed improvements thereto, and
		- (ii) share anonymized insights on target customers and market applications;
	+ (2\) MethaneSAT may use aggregated or anonymized insights to refine its Data offerings.


ATTRIBUTION


If you share or use the Data in any manner with any third parties, you must:


* Explicitly state to these third parties that they are agreeing to be bound by the Terms of Use;
* Display a citation that states: “Data from MethaneSAT” and “Download the most current dataset at Google Earth Engine and/or Google Cloud”; and
* Explicitly state to these third parties that, if such third party creates a further project containing the Data, any such users of that project must also agree to be bound by these Terms of Use.




### Citations



Citations:
* Chulakadabba, A., Sargent, M., Lauvaux, T., Benmergui, J. S., Franklin, J.
E., Chan Miller, C., Wilzewski, J. S., Roche, S., Conway, E., Souri, A. H.,
Sun, K., Luo, B., Hawthrone, J., Samra, J., Daube, B. C., Liu, X., Chance,
K., Li, Y., Gautam, R., Omara, M., Rutherford, J. S., Sherwin, E. D.,
Brandt, A., and Wofsy, S. C. 2023\. Methane point source quantification using
MethaneAIR: a new airborne imaging spectrometer, Atmos. Meas. Tech., 16,
5771\-5785\.
[doi:10\.5194/amt\-16\-5771\-2023](https://doi.org/10.5194/amt-16-5771-2023),





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Request access to this data by filling out the form at: https://forms.gle/jqw4Mvr63dsV1fUF8
vardataset=ee.FeatureCollection("projects/edf-methanesat-ee/assets/public-preview/L4point");

// Add a `style` property with `pointSize` dependent on flux value.
varminSize=25;
dataset=dataset.map(function(feature){
varflux=ee.Number(feature.get('flux'));
varsize=ee.Algorithms.If(flux,flux.divide(150).min(minSize),minSize);
returnfeature.set('style',{pointSize:size,color:'red'});
});
vardatasetVis=dataset.style({styleProperty:'style'});

Map.setCenter(-43.03,37.48,3);
Map.addLayer(datasetVis,null,'Methane point sources flux in kg/h');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/edf-methanesat-ee/projects_edf-methanesat-ee_assets_public-preview_L4point)
### Visualize as a FeatureView



 A `FeatureView` is a view\-only, accelerated representation of a
 `FeatureCollection`. For more details, visit the
 [`FeatureView` documentation.](/earth-engine/guides/featureview_overview) 



**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Request access to this data by filling out the form at: https://forms.gle/jqw4Mvr63dsV1fUF8
varfvLayer=ui.Map.FeatureViewLayer('FeatureViews/projects_edf-methanesat-ee_assets_public-preview_L4point_FeatureView');

varvisParams={
color:'red',
fillColor:'red',
opacity:1,
pointSize:5
};

fvLayer.setVisParams(visParams);
fvLayer.setName('Feature view of methane point sources flux in kg/h');

Map.setCenter(-43.03,37.48,3);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/edf-methanesat-ee/projects_edf-methanesat-ee_assets_public-preview_L4point_FeatureView)


[MethaneSAT L4 Point Sources Public Preview V1\.0\.0](/earth-engine/datasets/catalog/projects_edf-methanesat-ee_assets_public-preview_L4point)

This early "Public Preview" dataset provides high precision data for methane emissions from discrete point sources. These methane emission fluxes were produced using a point source detection and emissions quantification framework specialized to exploit the high spatial resolution, wide spatial coverage, and high precision of MethaneSAT data (methodology is described …

 projects/edf\-methanesat\-ee/assets/public\-preview/L4point,
 atmosphere,climate,edf,edf\-methanesat\-ee,emissions,ghg,methane,methanesat,publisher\-dataset,table

2024\-06\-14T00:00:00Z/2025\-01\-17T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








