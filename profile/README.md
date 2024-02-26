
![](https://swerik-project.github.io/assets/img/riksdagsbiblioteket4.jpg)

# Swedish Riksdag 1867–2022: An Ecosystem of Linked Open Data (SWERIK)

Research infrastructure project funded by Riksbankens Jubileumsfond



## Overview of the SWERIK Project

The parliament has the power to transform society’s future. Its documents constitute a democratic resource for our present-day that, in turn, can be used by researchers to remodel our understanding of the past. During the last decade, the Swedish parliamentary documents – parliamentary records (which include the Riksdag debates), government bills, private members’ motions, and committee reports – have all been digitized. These four document categories constitute the central part of the Swedish legislation process. Taken together, these documents form a rich source to study political culture and democratic development over long periods. However, the lack of an interconnected metadata structure with linked parliamentary data, including a patchwork of gaps and digitization errors, makes the current state of these compiled digitized documents a primitive research infrastructure. The purpose of SWERIK is to address these limitations by constructing a research corpus with an ecosystem of linked open data of the parliamentary documents from the bicameral and unicameral Riksdag, from 1867 to today.

As a collaborative project between the humanities, statistics, and the Riksdag Library, the infrastructural aim of SWERIK is threefold. (1.) To provide a comprehensive linked open data corpus with annotated metadata that enables scholars to use and analyze parliamentary documents – both qualitatively and foremost quantitatively – in ways that are not possible today. (2.) The annotated SWERIK corpus will serve as the research infrastructure backbone for open user interfaces available for other scholars, nationally and internationally, including being a democratic resource for citizens and journalists to gain knowledge about elected politicians, debates, and democratic decisions. (3.) Connected to the Wikidata project, SWERIK will contribute to the growing open encyclopedia about the Swedish parliamentarians and both make knowledge about the Riksdag available to a wider public and, as a citizen science-oriented project, enable the public to contribute to and improve the work of SWERIK.

The project’s objectives are connected to five work packages. WP1 will focus on marking up parliamentary documents and annotating MPs, speeches, and other textual content in parliamentary records, private members’ motions, government bills, and committee reports. WP2 will build a comprehensive database of all members of parliament (MP) since 1867, including relevant publicly available metadata (e.g. gender, party, constituency, year of birth and death, role in parliament) based on digitized and digitally born sources. WP3 will develop a linked open data infrastructure that ties together identified MPs with their associated parliamentary documents, supported by the database of MP metadata, thus connecting MPs to the debates they took part in, motions they wrote, and committees they were part of et cetera. In WP4, the SWERIK corpus will be aligned with ParlaMint – an international network that provides an open infrastructure standard for annotating and comparing national parliamentary debates. Finally, WP5 will enable the SWERIK corpus to be utilized by different users, for instance by integrating it into the Riksdag web and further developing its user interface based on existing benchmark solutions. Moreover, as a CC BY-license corpus, other scholars can use it and, for example, build their own user interfaces, facilitating a wider use. After the project has ended, the Riksdag Library will be responsible for storing and maintaining the SWERIK corpus.


## Recommendations for working with SWERIK Git repositories

The data organization is currently in progress as we relocate from the [beta Riksdagen Corpus](https://github.com/welfare-state-analytics/riksdagen-corpus) and reorganize some of the data structures to improve usability. 

### API

### Data API

We recomend cloning repositories containing data into the same parent folder, from where workflows can also be built and run.

- riksdagen-records: Riksdagen Records (_Riksdagensprotokoll_)
- riksdagen-records-alto: Riksdagen Records, alto files (output of OCR)
- riksdagen-records-pdf: Riksdagen Records, PDF documents
- riksdagen-motions: Riksdagen Motions (_Motioner_)
- riksdagen-motions-alto: Riksdagen Motions, alto files (output of OCR)
- riksdagen-motions-pdf: Riksdagen Motions, PDF Documents
- riksdagen-politicians: MPs, ministers, and others who address the parliament

For developers who wish do engage with our `src/` directory, this should also be cloned as a sibling of folders beloinging to the data API to ensure interoperability of the different repositories.

### Pyriksdagen

We recommend installing [pyriksdagen](https://github.com/swerik-project/pyriksdagen) via pypi in a virtual environment. Setup and activate your environment, then

	pip install pyriksdagen
	
	
### rcr (Riksdag Corpora R package)

To use the R package [rcr](https://github.com/swerik-project/rcr), run:

	library(remotes)
	remotes::install_github('swerik-project/rcr')
	
then set a local path to the Riksdagen corpora

	set_riksdag_corpora_path("[THE PATH TO THE CORPORA HERE]")