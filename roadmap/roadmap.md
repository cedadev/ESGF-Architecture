
# ESGF Roadmap
**Neil Massey and Philip Kershaw**

**06/02/2024**

## Introduction

We (CEDA) would like to approach the development and roll out of ESGF 2.0 for CMIP7 in
an Agile way.  This will consist of:

* Epics
* Sprints
* A focus on minimal viable products
* A component working at the end of a sprint
* Feature lock offs
* etc.

We are inspired by the data challenges, but want to reformulate them into Agile 
methodology and only concentrate on what is relevant in 2024.  A translation between
data challenges and Agile terms:

* Data challenge == *Epic*
* Outcome of the data challenge == *Vision*
* Task == *Sprint*
* Steps in each task == *Features*, which 

The development will be *Feature led*, and lead to a *minimal viable product*.  For each
*Epic* we need to ask "what is the minimum we have to achieve to realise the *Vision* for
this *Epic*?".

We have identified different areas that we believe are important to deliver ESGF, and 
could be the target for each *Epic*.

* Governance
* Installation
* Bulk transfer
* Publish
* Search
* Download
* User interaction

we can break these down further, identify the output (*Vision*), decide on the *Features*
for each *Sprint* and generate task lists (*Backlog*) for each *Sprint* which, when
accumulated, will produce the *Vision* for the *Epic*.

## E1 - Governance

### *Vision*
Determine mandatory principles for working.

### *Tasks*


## E2 - Installation

### *Vision*
The latest version of the software can be easily installed by any ESGF partner.

## E3 - Bulk transfer

### *Vision*
Data can be transferred between ESGF nodes with excellent performance.

### *Tasks*

 - Tier-1 sites deploy GCSv5 endpoints
 - Identify test set of CMIP data
 - Transfer test benchmarking

## E4 - Publish

### *Vision*
Data can be ingested into ESGF and made available for search.

### *Tasks*

 - `esg-publisher` needs test suite
 - Push records to Globus Search
 - Push records to Elastic Search
 - Implement workflows
 - Add QC checks to workflows
 - Open question for ElasticSearch ingest:  how is access control implemented?

## E5 - Search
 
### *Vision* 
A user can search the ESGF catalogue and get the correct result in a timely manner.

## E6 - Download

### *Vision*
A user can download the data they searched for, in a timely manner.

### *Tasks*

 - Upgrade wget API to support Globus Search backend
 - Upgrade wget API to support Elasic Search backend (or STAC) ?
 - Enhance `esgpull` to support Globus Transfer
 - integrate `esgpull` with Metagrid
 - Retire wget?

## E7 - User interaction

### *Vision*
A user can interact with the data they searched for, to transform it into new data.
