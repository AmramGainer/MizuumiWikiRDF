# MizuumiWikiRDF
A linked data project that Catalogues 50 games featured on the fighting game information site Mizuumi wiki
__Included Files__
* FGCDatasetFINAL.xlsx - a spreadsheet from which this RDF project originates
* Mapping Diagram.png - a representation of how properties of each entry will be organized in RDF format.
* Mizuumi_Dataset.ttl - the RDF export in Pretty Turtle format

## Ontology & Controlled Voabulary
I used schema.org as my primary ontology and its VideoGames type as my controlled vocabulary

## Linking Strategy.
Game Title - Literal. I felt the titles would be very obscure and random, so I figured it would be difficult to find them as URIs in any databases like wikidata. A few games' names came up, but not enough to justify making this a URI in my opinion.
Developer Name - URI. I almost had made this a Literal for the same reason as stated above, but I had some better luck finding creators on wikidata, so I figured it would be ok to make this one a URI. I found at least half on the creators on wikidata and was able to replace the entries without legit URIs with example.com addresses. 

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
  
