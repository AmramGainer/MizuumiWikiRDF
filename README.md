# MizuumiWikiRDF
A linked data project that Catalogues 50 games featured on the fighting game information site Mizuumi wiki
__Included Files__
* FGCDatasetFINAL.xlsx - a spreadsheet from which this RDF project originates
* Mapping Diagram.png - a representation of how properties of each entry will be organized in RDF format.
* Mizuumi_Dataset.ttl - the RDF export in Pretty Turtle format

## Example RDF
### Game: Hinokakera Chaotic Eclipse
#### Human Readable format
author is Reddish Region

date Published is 2010

game platform is PC

image is located at "https://mizuumi.wiki/images/1/1d/Hikake_Logo.png"

English name is Hinokakera Chaotic Eclipse 

url is https://mizuumi.wiki/w/Hinokakera_Chaotic_Eclipse


#### Turtle Format
  rdf:type              schema:videoGame;
  
  schema:author         :Reddish Region;
  
  schema:datePublished  "2010"^^xsd:gYear;
  
  schema:gamePlatform   wd:Q16338;
  
  schema:image          "https://mizuumi.wiki/images/1/1d/Hikake_Logo.png";
  
  schema:name           "Hinokakera Chaotic Eclipse"@en;
  
  schema:url            "https://mizuumi.wiki/w/Hinokakera_Chaotic_Eclipse" .
  
