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
<br>
Developer Name - URI. I almost had made this a Literal for the same reason as stated above, but I had some better luck finding creators on wikidata, so I figured it would be ok to make this one a URI. I found at least half on the creators on wikidata and was able to replace the entries without legit URIs with example.com addresses.  There's also the fact that a good fraction of the developers are well known enough and have multiple projects, so it would be good to be able to connect people to the other games they've made.
<br>
Date Published - Literal. (gYear) It's a date, no need to make things more complex than they should be. Just make a note of the year it was made and call it a day
<br>
Platform - URI. Again I was sorta on the fence about whether or not to make this a Literal or URI, but There were two factors that swayed me. 1) It'd be cool to be able to link to a platform's URI and see what other games were released for it, 2) All the game platforms I mention in this dataset have URIs on wikidata, so that made it an easy choice in the end
<br>
website - URI(L?). This one is easy. It's website is already a specific place on the internet, so why not just make it a URI? There is the concern that a game's current website could shut down for any number of reasons without a backup. However this makes the dataset more connective with other places online. 
<br>
Logo - URI. Same thing as above. Same concerns as above, but it's a pretty easy choice if you ask me.

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
  
