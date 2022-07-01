# UK Law Citation Network

In this repository we look at the creation of the citation network for UK law.
<br>
## Notebooks
Within the notebook directory we have:
* citation_scrape
* citation_network

The **citation_scrape** notebook looks at acquiring the corpus of law (for the purpose of this repository we only deal 
with UKPGA). Then scraping each document for the citations within them. Each citation in a document is then classified. 
Finally, the netbook stores each relation, between the scraped document and the documents mentioned through citations
within them, as a network.
<br><br>
The **citation_network** notebook looks to visualise the network created in _citation_scrape_, it allows for querying the
network for certain relations. It also allows for exploration from "root" document(s) refined through specific citation 
relations as well as distance from the "root".
<br>
## Data
Within the data directory we have:
* citation_network.csv
* label_colours.json
* labels.txt
* legislation.csv

The **citation_network.csv** file contains details about the network, each line in the csv states the source document of
a relation, the target document in the relation and the type of relation.

The **label_colours.json** file is a simple dictionary, where the key corresponds to a type of relation and the value is
the colour value for the relation. This is used when colouring the network in _citation_network_ notebook.

The **labels.txt** file contains a list of keywords. Each keyword is an identifier that can be searched in a passage 
surrounding a citation in a document to determine the type of relation for the citation.

The **legislation.csv** file contains a list of all the legislation used in _citation_scrape_. It contains the type of 
act, the year and the number of act.