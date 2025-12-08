# README

## General information

1.  Title of Dataset:

    Clinical surveillance of suspected and confirmed cholera cases in Uvira, Democratic Republic of the Congo (2017–2021)

2.  Author Information

**Author A**

-   First name: Karin\
-   Surname: Gallandat\
-   ORCID iD: <https://orcid.org/0000-0001-6412-1483>\
-   Email: [karin.gallandat\@lshtm.ac.uk](mailto:karin.gallandat@lshtm.ac.uk){.email}

**Author B**

-   First name: Amy\
-   Surname: Macdougall\
-   ORCID iD: Not available\
-   Email: Not available (see corresponding author above)

**Author C**

-   First name: Aurélie\
-   Surname: Jeandron\
-   ORCID iD: Not available\
-   Email: Not available (see corresponding author above)

3.  Date of data collection (single date, range, approximate date):

    January 2017 – December 2021

4.  Geographic location of data collection:

    Uvira, South Kivu Province, Democratic Republic of the Congo

5.  Information about funding sources that supported the collection of the data

    Data collection and trial implementation were funded by the French Agency for Development (AFD, ref. EVA/364-2015) and the Veolia Foundation (VF, ref. 13/14 HD 1123). Construction works on the water supply infrastructure were funded by AFD, the Veolia Foundation, the European Union, and Oxfam GB.

------------------------------------------------------------------------

## Sharing / access information

1.  Licenses/restrictions placed on the data This dataset and the associated publication are made available under the Creative Commons Attribution 4.0 International license (CC BY 4.0), which permits unrestricted use, distribution, and reproduction in any medium, provided the original author and source are credited.

2.  Links to publications that cite or use the data:

    -   Gallandat K, Macdougall A, Jeandron A, et al. Improved water supply infrastructure to reduce acute diarrhoeal diseases and cholera in Uvira, Democratic Republic of the Congo: Results and lessons learned from a pragmatic trial. *PLOS Neglected Tropical Diseases*. 2024;18(7):e0012265. <https://doi.org/10.1371/journal.pntd.0012265>

3.  Links to other publicly accessible locations of the data:

    -   Open Science Framework (OSF) project: <https://osf.io/hbyze/?view_only=82b2b9986ed14389963ce8b45555e14c>

4.  Links/relationships to ancillary data sets:

    The OSF project also hosts related datasets and code, including water service monitoring data, water service quality indices, and R scripts used in the main analyses of Gallandat et al. (2024).

5.  Was data derived from another source?

    Yes. Clinical surveillance data were derived from routine patient registers at the cholera treatment centre (CTC) and cholera treatment unit (CTU) in Uvira, and from laboratory records of rapid diagnostic tests (RDTs). Cluster-level information and population estimates were derived from official local population records and spatial allocation procedures described in the trial publications.

------------------------------------------------------------------------

## Methodological information

1.  Description of methods used for collection/generation of data:

    The dataset contains individual-level clinical records for patients admitted with acute watery diarrhoea to the main cholera treatment facilities in Uvira (CTC and CTU). For each admission, demographic information (age, sex, residence), dates of admission and outcome, and basic clinical information were recorded in routine registers. From April 2016, rectal swabs were systematically collected from eligible consenting patients for laboratory enrichment and cholera confirmation using rapid diagnostic tests (Crystal VC O1/O139). Line-list data were then cleaned, anonymised, and linked to spatial clusters defined for the pragmatic trial evaluating water supply infrastructure improvements.

2.  Methods for processing the data:

    Within this project, the original Excel file (`Dataset_2017-2021_OSF.xlsx`, sheet 2) was imported into R and processed to obtain an analysis-ready dataset. Variable names were standardised to syntactically valid forms, and variable types were harmonised (e.g. patient identifier stored as character, admission date converted to a Date object, age stored as numeric, sex and cholera treatment centre as categorical factors, and temporal variables such as month and year stored as integers). The RDT confirmation variable (`confirmed`) was recoded from the original character values (“TRUE”, “FALSE”, and missing) into a binary indicator, where 1 denotes a positive RDT result, 0 denotes a negative RDT result, and NA indicates that the patient was not tested. The treatment outcome variable (`outcome`) was converted to a categorical factor with predefined levels corresponding to discharge status, treatment refusal, transfer, and death. Records with missing cluster, year, or admission date were removed, reducing the dataset from 4,559 to 4,556 observations and yielding a consistent analysis-ready dataset which is saved as `clinical_surveillance_2017_2021_processed.csv` in the `data/processed` directory.

3.  Instrument- or software-specific information needed to interpret the data:

    -   Clinical confirmation of cholera was based on APW-enriched rectal swabs tested with Crystal VC O1/O139 rapid diagnostic tests, as described in Gallandat et al. (2024).\
    -   [**Data processing and analysis for this project were performed using R within RStudio, using the packages `readxl`, `tidyverse` packages.....**]{.underline}

4.  Standards and calibration information, if appropriate:

    Rapid diagnostic test performance (sensitivity and specificity) and laboratory procedures follow those reported in the main trial paper and referenced laboratory validation studies; no additional calibration was undertaken within this project.

5.  Environmental/experimental conditions:

    Data were collected in a cholera-endemic urban setting in Uvira, South Kivu, Democratic Republic of the Congo, during a period of substantial water supply infrastructure improvements, intermittent conflict, and population displacement. The trial coincided with events affecting the water system, including major flooding in April 2020 and progressive expansion and rehabilitation of the piped water network, as described in Gallandat et al. (2024).

6.  Describe any quality-assurance procedures performed on the data:

    In the original study, clinical surveillance data were cleaned, anonymised, and cross-checked by the research team in collaboration with local health authorities, with additional linkage to spatial clusters and population estimates as described in the published protocol and main analysis. In this project, further quality-assurance steps included verification of variable types, inspection of distributions and missingness patterns, explicit recoding of RDT confirmation and outcome variables, and removal of records missing key identifiers (cluster, year, or admission date) prior to analysis.

7.  People involved with sample collection, processing, analysis and/or submission:

    Clinical data collection and rectal swab sampling were carried out by staff at the Uvira cholera treatment centre and cholera treatment unit in collaboration with provincial health authorities. Data curation, linkage to clusters, and preparation of the anonymised research dataset were led by the study team of Gallandat et al. (2024), including co-authors responsible for data curation and investigation (e.g. Jaime Mufitini Saidi and Baron Bashige Rumedeka), under the supervision of the principal investigators and co-authors based at the London School of Hygiene and Tropical Medicine and partner institutions.
