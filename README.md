# Data and Code
Shortcuts will be availalbe here to all available datasets and computer code.

## Data
These datasets are open access and available to the public. They contain no personally identifying information. All datasets are either used with permission or only contain public data. Attributions to orignal source material are provided.

1. [Corpus of FDA-approved controlled substance US drug labels](https://github.com/opioiddatalab/ExcipientHarm/blob/master/inactive%20ingredients/DrugLabelCorpus.md)<br>
Published: October 3, 2019 by Nabarun Dasgupta<br>
Observations: 2,177<br>
Format: ZIP archive of .txt files <br>
Size: 50 MB<br>
Origin: United States Food and Drug Administration via NIH National Library of Medicine DailyMed API service
License: Creative Commons Sharealike 4.0 International<br>

2. [Inactive Ingredients in Controlled Substances](https://github.com/opioiddatalab/ExcipientHarm/blob/master/inactive%20ingredients/allcsingredientswide.xls)<br>
Published: November 14, 2019 by Nabarun Dasgupta<br>
Observations: 18,876<br>
Format: .xls<br>
Size: 8.8 MB<br>
Origin: United States Food and Drug Administration via NIH National Library of Medicine DailyMed API service<br>
License: Creative Commons Sharealike 4.0 International<br>
[Codebook available here](https://github.com/opioiddatalab/ExcipientHarm/blob/master/inactive%20ingredients/inactive%20ingredients%20codebook.pdf)


## Code
Each set of code listed below is provided for public use, with the author's consent. Each code set contains a license that details sharing and reuse permissions. Code is written in SAS, Python, Stata, and/or R. 

1. [PubMed Search Volume Query](https://github.com/opioiddatalab/DataCode/blob/master/code/PubMedVolume.md)<br>
Python 3.7, November 2019, MIT License<br>
By Nabarun Dasgupta<br>
This straightforward code will let you take a list of potential search terms and return the number of search term results from PubMed. It was create to identify noisy and irrelevant terms when building a search strategy for a systematic review.

1. [Distinguishing Brand Versus Generic Controlled Substances](https://github.com/opioiddatalab/ExcipientHarm/blob/ecf050dbc548d6dd81b02727ed7c24d257e724de/Data%20cleaning%20brand%20names.do)<br>
Stata MP 16, October 2019, MIT License<br>
By Nabarun Dasgupta<br>
This code differentiates brand names from generic names of controlled substances. Useful for cleaning data from prescription monitoring program (PMP or PDMP), insurance claims, electronic health records, etc.

1. [Data Cleaning for Historical Dix Asylum Intake Ledger](https://github.com/opioiddatalab/DixLedger/blob/master/Dix%20Hospital%20Ledger%20-%20data%20cleaning.ipynb)<br>
Stata MP 16 in iPython notebook, November 13, 2019, MIT License<br>
By Nabarun Dasgupta<br>
This code will process, format, and create variables from the Dix Asylum (Raleigh, NC, USA) Intake Ledger, covering years 1856 to 1919. 
