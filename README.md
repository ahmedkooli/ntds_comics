# A Growing Network of Characters In Marvel and DC Universes

# Abstract
Marvel and DC Comics are the two most important comic books publishers in the world. Over the years, each of them told stories of more than 20 000 characters, developing their personalities and making them interact with each others to build two gigantic universes.

The relationships between the characters represent a huge potential for graph visualization:  the characters are nodes, and the links between them show how close they are to each other. Studying these links over time will allow an overall visualization of the evolution of the two separate universes thoughout the years, which will show the emergence of some groups. The study will be made for three different periods of time: \[beginning - 1950], \[beginning - 1990], \[beginning - today] ("beginning" means all the data since Marvel and DC started publishing comic books).

# Dataset
The data for Marvel and DC were taken respectively from the following websites:
- https://marvel.fandom.com/wiki/Marvel_Database
- https://dc.fandom.com/wiki/DC_Comics_Database

In each database, information on characters and on published comics was collected.

For the characters, the gathered attributes were: `Name`, `Current Alias`, `Relatives`, `Affiliation` (team, group or organization the character is affiliated to), `URL` of the webpage (used as a unique ID).

For the comic books, the gathered attributes were: `Publication date`, `Subcomics names` (if a comic book is made of multiple comics)   `Appearing characters` with a URL (to make sure they're in the database). 

The graphs are based on three attributes: the characters that are relatives, the ones that are linked by the same affiliation, and the ones appearing in the same comic book.

# Repository
## Notebooks
All the used notebooks for the data gathering and analysis.
- `parsing_data.ipynb`: scraping of the databases
- `cleaning_data.ipynb`: cleaning the obtained data
- `relatives_analysis.ipynb`: generating the adjacency matrix based on the relatives
- `affiliation_analysis.ipynb`: generating the adjacency matrix based on the affiliations
- `comics_analysis.ipynb`: generating the adjacency matrix based on the comics appearances
- `adjacency_processing.ipynb`: plotting the degree distributions of the adjacency matrices and generating the corresponding CSV files for the graph visualisation (Gephi software)

## Data
Folder containing all the saved data.
- `characters_marvel.txt`: Marvel characters and their attributes
- `comics_marvel.txt`: Marvel comics and their attributes
- `clean_marvel.txt`: Cleaned Marvel dataframe (characters + comics)
- `good_dc.txt`: DC good characters and their attributes
- `bad_dc.txt`: DC bad characters and their attributes
- `characters_dc.txt`: DC characters and their attributes (good + bad)
- `comics_dc.txt`: DC comics and their attributes
- `clean_dc.txt`: cleaned DC dataframe (characters + comics)
- https://drive.google.com/drive/folders/1fZhjABSlYjy7Pkc2HMnRkctInPVhlnGA?usp=sharing: rest of the data that was too large for git
  - `Adjacency matrices`: adjacency matrices, the file names are adj_attribute_date. Attribute: aff means affiliations, relat means relatives, comics means comic books. Date: 50 means until 1950, 90 means until 1990, no date means all the dataset.
  - `CSV`: made from the adjacency matrices to match the Gephi inputs. The name format is the same as the adjacency matrices, replacing adj with edge.

## Report
- `team_28_ntds_2019.pdf`: final report
