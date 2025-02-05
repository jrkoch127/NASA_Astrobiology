# NASA Astrobiology

This repository contains files associated with the SciX/NASA Astrobiology curation project. Use the python-based jupyter notebook (NASA_Astrobiology.ipynb) to run the scripts that support bibcode matching, updating the [NASA Astrobiology Library](https://scixplorer.org/public-libraries/UTViEyO9T7izQP7i_r6yqA), or batch curating records in SciX/ADS Tagged Format.

Requirements:
- [Python3](https://www.python.org/downloads/)
- [Jupyter Notebook](https://jupyter.org/)
- Python libraries: [pandas](https://pandas.pydata.org/docs/getting_started/install.html), re, json, requests, [pyingest](https://github.com/adsabs/adsabs-pyingest/tree/master).serializers.classic, and datetime
- An ADS/SciX API token: When logged into your ADS/SciX account, go to your [user settings](https://scixplorer.org/user/settings/token) to get an API token, and insert it in the Jupyter Notebook
- A local folder where these files can be stored on your computer (your copy of the notebook, the excel spreadsheet as your input file, and any resulting output files).

The Jupyter Notebook has three sections that can be run independently for the relevant task, based on the data in the associated excel spreadsheet (NASA_Astrobiology.xlsx).

As monthly digests are shared, one can manually add DOIs, and other metadata, as new rows in the spreadsheet. Then we can follow the subsequent steps:

+ **Bibcode Matching**: Use this cell section to find existing records in our databases. When a match occurs, a 'bibcode' will return as a result. From there we can insert the bibcode into the spreadsheet to identify the record.
+ **Updating the Scix/ADS Library**: Use this cell section to update the Library. Any new bibcodes will automatically get send to the Library.
+ **Data Curation**: Use this cell to automatically generate a ".tag" file. This will consist of the respective metadata taken from the spreadsheet for rows that do not have a bibcode. Email the file to Jenny Koch (SciX/ADS Librarian) at jennifer.koch@cfa.harvard.edu for subsequent ingest processing. Alternatively, manually submit records to the [online feedback form](https://scixplorer.org/feedback/missingrecord?from=%2F).

Please email any questions to Jenny Koch (SciX/ADS Librarian) at jennifer.koch@cfa.harvard.edu. 
 

