
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

* Techincal Governance
* Installation
* Bulk transfer
* Publish
* Search
* Download
* User interaction

we can break these down further, identify the output (*Vision*), decide on the *Features*
for each *Sprint* and generate task lists (*Backlog*) for each *Sprint* which, when
accumulated, will produce the *Vision* for the *Epic*.

## E1 - Technical Governance

### *Vision*

Determine mandatory principles for working.

### *Tasks*
- **T1.1** Write or adapt the LICENSE that all software will be developed under
- **T1.2** Setup, adapt or collate the software repositories
- **T1.3** Write the versioning, tagging and release specification that all software will be committed and released under
- **T1.4** Assign repository managers and write specifications for code-review and acceptance

### *Acceptance criteria*

## E2 - Installation

### *Vision*
The latest version of the software can be easily installed by any ESGF partner.

### *Tasks*

- **T2.1** Update support for podman version of the installation.
  - GFDL have reported that the podman installation works, but there are some issues around container networks and file permissions still to resolve. We'll also need to merge their changes into the main repo.
- **T2.2** Add Rocky 9 as the base for the next version of the images.
  - Will require us to resolve the issue in the gitlab.com pipeline caused by a communication failure with the Rocky RPM server.
- **T2.3** Resolve issues with the CMCC stats service:
  - Debugging CEDA's communication problems with the stats server.
  - Solving the problem where a failure to communicate with the stats server causes the file-server containers to crash.
- **T2.4** Add S3 file system support.
  - This has been done for Kubernetes but needs to be added for the Ansible version of the installation.
  - We will also want to add better support for including a certificate in the file-server container for verifying the S3 connection.

### *Acceptance criteria*

## E3 - Bulk transfer

### *Vision*
Data can be transferred between ESGF nodes with excellent performance.

### *Tasks*
- **T3.1** Install Globus at all European nodes.

### *Acceptance criteria*

## E4 - Publish

### *Vision*
Data can be ingested into ESGF and made available for search.

### *Tasks*

- **T4.1** Test current pipeline is compatible with expected CMIP7 data
- **T4.2** Test and develop PID and DOI assignment
- **T4.3** ES-DOC scanning and ingest
- **T4.4** Errata service for updated data
- **T4.5** Revoke data at a single site and over all sites
- **T4.6** Publish a new version at a single site and over all sites
- **T4.7** Adapt publishing pipeline to produce STAC catalogue records
  - **T4.7.1** ES-DOC ingest
  - **T4.7.2** Update data
  - **T4.7.3** Revoke data
  - **T4.7.4** Publish new version

## E5 - Search
 
### *Vision* 
A user can search the ESGF catalogue and get the correct result in a timely manner.

### *Tasks*

- **T5.1** Write an example of searching with `pystac-client` in a notebook.  Search a wide space in the catalogue.
- **T5.2** Demonstrate searching with MetaGrid.  Show that results for CMIP6 match the current implementation.
- **T5.3** Compatability with legacy search (*this is something we might not want to do*)
  - **T5.3.1** Write an example of searching with `esgf-client`
  - **T5.3.2** Demonstrate searching in CoG
- **T5.4** Demonstrate consistency of search between STAC implementation and Globus implementation.

### *Acceptance criteria*

## E6 - Download

### *Vision*
A user can download the data they searched for, in a timely manner.

### *Tasks*

- **T6.1**

### *Acceptance criteria*

## E7 - User interaction

### *Vision*
A user can interact with the data they searched for, to transform it into new data.

### *Tasks*

- **T7.1** User can find the data on JASMIN
- **T7.2** User can analyse the data in a Jupyter Notebook on JASMIN
- **T7.3** User can analyse the data on an interactive analysis node on JASMIN
- **T7.4** User can analyse the data on batch compute (LOTUS) on JASMIN

### *Acceptance criteria*
