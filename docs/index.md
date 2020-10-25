# General info for using ABCD data

!!! Notice
	Only users registered with a named application can use this data.
	Check with Dr Heather Whalley if you have any question.
	Watch this video to know more about [data protection](https://www.gotostage.com/channel/138fa524383b4041afc49f8694688dc3/recording/77a3a9ede95846568e2bc56596c97292/watch).


- [ABCD protocol papers](https://www.sciencedirect.com/journal/developmental-cognitive-neuroscience/vol/32/suppl/C)
- [Data dictionary for release 2.0.1](https://nda.nih.gov/data_dictionary.html?source=ABCD%2BRelease%2B2.0&submission=ALL)
- [A summary of ABCD study](https://nda.nih.gov/abcd)

*****

# Data location

* Eddie: /exports/igmm/eddie/GenScotDepression/data/abcd/release2.0.1
* Eddie datastore: /exports/igmm/datastore/GenScotDepression/data/abcd/release2.0.1
* CMVM datastore: 

*****

# Data download

## Data

- Go to: https://nda.nih.gov/abcd
- Login with NDA credentials and go to 'my dashboard'
- Click username at the topright of the page to go to your profile
- Go to 'Data packages' and select the packages to download (add to 'My Data Packages' using tab 'Actions')
- Click 'Download Manager' 
- Run the downloaded 'Download Manager'
- Login with NDA credentials
- Download data
!!! Note 
	It takes a while before the added packages appears in your account. Large data may take up to around 30 mins
	Including bulk data may take up a very large space

The latest curated data packages downloaded are: ABCDstudyNDA

!!! Download files
	In subfolder 'i.files_from_web'


## Supporting documentations
[Summary of the latested release](https://nda.nih.gov/study.html?id=634)
Check the hyperlinks 'DEAP-NDA variables mapping' and 'Release Notes' for more information about the current dataset.

!!! Downloaded documentations
	In subfolder 'ii.docs'


*****

# Segment data by category

[Functions need](https://github.com/xshen796/ABCD_UoEPsych/tree/main/Util/organise_dat)

- Summary
  - process_files.R is the default R script for all main steps
  - baseline.R and baseline_imputation.R are functions for baseline measures
  - Other files are used by process_files.R

- Files essential for process_files.R (all need manual check for each data release)
  - Instruments.ABCD_summary_web_dictionary.csv: This file should be created manually. Copy contents from [URL] (https://nda.nih.gov/data_dictionary.html?source=ABCD%2BRelease%2B2.0&submission=ALL)
  - ls.category: a list of object names and categories, a master list of all object names that ABCD ever released
  - ls.category.PreiousVersionOnly: like ls.category, but contains the objects only release in a previous version
  - ls.category.CurrentVersion: like ls.category, but contains objects released in the lasted version
  - ls.faultyobjects: sometimes ABCD have objects that need to be removed (e.g. some imaging files from release 2.0, fixed in release 2.0.1)

