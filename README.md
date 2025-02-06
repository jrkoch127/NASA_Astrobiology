# NASA Astrobiology

This repository contains files associated with the SciX/NASA Astrobiology curation project. Use the python-based jupyter notebook (NASA_Astrobiology.ipynb) to run the scripts that support bibcode matching, updating the [NASA Astrobiology Library](https://scixplorer.org/public-libraries/UTViEyO9T7izQP7i_r6yqA), or batch curating records in SciX/ADS Tagged Format.

Requirements:
- [Python3](https://www.python.org/downloads/)
- [Jupyter Notebook](https://jupyter.org/)
- Python libraries: [pandas](https://pandas.pydata.org/docs/getting_started/install.html), re, json, requests, [pyingest](https://github.com/adsabs/adsabs-pyingest/tree/master).serializers.classic, and datetime
- An ADS/SciX API token: When logged into your ADS/SciX account, go to your [user settings](https://scixplorer.org/user/settings/token) to get an API token, and insert it in the Jupyter Notebook
- A local folder where these files can be stored on your computer (your copy of the notebook, the excel spreadsheet as your input file, and any resulting output files).

The Jupyter Notebook has three sections that can be run independently for the relevant task, using data in the associated excel spreadsheet (NASA_Astrobiology.xlsx) as input.

As monthly digests are shared, one can manually add DOIs, and other metadata, as new rows in the spreadsheet. Then we can follow the subsequent steps:

+ **Bibcode Matching**: Use this cell section to look for existing records in our databases on rows/records where a bibcode is not yet identified. When a match occurs, a 'bibcode' will return as a result. From there we can copy & paste the bibcode into the spreadsheet to identify the record.
+ **Updating the Scix/ADS Library**: Use this cell section to populate/update the Library. Any new bibcodes listed in the column will automatically get sent to the Library.
+ **Data Curation**: Use this cell to programmatically generate a ".tag" file of new items needed to be indexed in the SciX/ADS databases. This will consist of the respective metadata taken from the spreadsheet for rows/records that do not have a bibcode identified (a null/empty 'bibcode' cell). Email the file to Jenny Koch (SciX/ADS Librarian) at jennifer.koch@cfa.harvard.edu for subsequent ingest processing. Alternatively, manually submit individual records to the [online feedback form](https://scixplorer.org/feedback/missingrecord?from=%2F), which will notify the curation team of the new record in need of indexing.

Please email any questions to Jenny Koch (SciX/ADS Librarian) at jennifer.koch@cfa.harvard.edu. 
 

