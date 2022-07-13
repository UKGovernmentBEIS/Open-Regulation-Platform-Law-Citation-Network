# UK Law Citation Network

In this repository we look at the creation of the citation network for UK law.

<br>

## Notebooks
Within the notebook directory we have:
* **_citation_scrape_**
* **_citation_network_**



The **_citation_scrape_** notebook looks at acquiring the corpus of law (for the purpose of this repository we only deal
with UKPGA). Then scraping each document for the citations within them. Each citation in a document is then classified.
Finally, the netbook stores each relation, between the scraped document and the documents mentioned through citations
within them, as a network.
<br><br>
The **_citation_network_** notebook looks to visualise the network created in _**citation_scrape**_, it allows for querying the
network for certain relations. It also allows for exploration from "root" document(s) refined through specific citation
relations as well as distance from the "root".
<br>
## Data
Within the data directory we have:
* **_citation_network.csv_**
* **_label_colours.json_**
* **_labels.txt_**
* **_legislation.csv_**

The **_citation_network.csv_** file contains details about the network, each line in the csv states the source document of
a relation, the target document in the relation and the type of relation.

The **_label_colours.json_** file is a simple dictionary, where the key corresponds to a type of relation and the value is
the colour value for the relation. This is used when colouring the network in _**citation_network**_ notebook.

The **_labels.txt_** file contains a list of keywords. Each keyword is an identifier that can be searched in a passage
surrounding a citation in a document to determine the type of relation for the citation.

The **_legislation.csv_** file contains a list of all the legislation used in _**citation_scrape**_. It contains the type of
act, the year and the number of act.
## Requirements
requirements.txt details all used python libraries from across the notebooks

## Credits

This work was conducted as part of a research project with the University of Swansea and is complimentary to the [Open Regulation Platform Alpha project](https://github.com/UKGovernmentBEIS/open-regulation-platform-alpha)
