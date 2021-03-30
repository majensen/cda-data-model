## Cancer Data Aggregator Data Model


### Cancer Data Aggregator
The Cancer Data Aggregator (CDA) is a query engine to aggregate data across the  [National Cancer Institute's (NCI) Cancer Research Data Commons (CRDC)](https://datascience.cancer.gov/data-commons). CDA will enable cancer researchers to discover, query, retrieve, and aggregate data by developing a single, interoperable, read-only API that can be used to query across disparate data types in CRDC repositories.  

![Figure 1 - Cancer Data Aggregator](https://github.com/CancerDataAggregator/cda-data-model/blob/main/documents/CancerDataAggregator_PMD_0.png)

CDA leverages the work and data model that is concurrently being developed by the [Center for Cancer Data Harmonization (CCDH)](https://datacommons.cancer.gov/center-cancer-data-harmonization).  CCDH will facilitate harmonization across CRDC nodes and data coordination centers by creating a harmonized data model (CRDC-H) and will provide vocabulary services and other tools.

### CDA Data Model
To enable the CDA and the CRDC-H to advance quickly, CDA maintains a data model that meets phased CDA requirements while aligning as closely as possible to released CRDC-H iterations.  

The CCDH data model promises to be a specimen-centric model whereas current CRDC nodes tend to use a case-centric approach.  The diagrams below depicts the shift from the respective GDC and PDC entity models (provided by CCDH - Figure 2) towards a specimen-centric model (Figure 3).

![Figure 2 - GDC and PDC case-centric models ](https://github.com/CancerDataAggregator/cda-data-model/blob/main/documents/GDCPDCModels.png)

As the CCDH model develops, CDA leverages the harmonization work of the CCDH model by extending the model only where necessary to support CDA functionality. For example, adding key search fields that are not yet included in the CCDH model. CDA periodically synchronizes with CCDH to maintain consistency between the  CDA MVP data model and the developing CCDH model.  The CDA MVP data model is expressed as JSON Schema.

![Figure 3 - CCDH specimen-centric model](https://github.com/CancerDataAggregator/cda-data-model/blob/main/documents/CCDH%20Specimen-centric%20Jun2020.png)

In Figure 4, the entities rimmed in blue are not yet part of the CCDH model but are extensions to allow CDA to aggregate and deliver data as the CCDH model evolves. It may be helpful to think about your queries in terms of these entities (e.g. Specimen, Patient, Research Subject, Project, Diagnosis) and their attributes (e.g. derived_from_subject, ethnicity, reference_assembly).

![Figure 4 - CDA Release 1 illustration](https://github.com/CancerDataAggregator/cda-data-model/blob/main/documents/CDA%20MVP%20Release%201.png)

Note that the JSON schema describes the fields for different entities and how the data connect but does not reflect how the data might be stored in a repository.  The repository schema will be optimized based on the performance characteristics of the selected platform.

### CDA API
The Cancer Data Aggregator Application Programming Interface(API) and its design are described in the [CancerDataAggregator/api](https://github.com/CancerDataAggregator/api) github repository.

### Status
Work-in-progress

### Versions
No released versions are available at this time.

### Contact
Please use this repository's Issue Tracker to share comments or concerns related to the data model.

