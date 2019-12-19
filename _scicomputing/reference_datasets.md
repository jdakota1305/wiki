---
title: Reference Data Sets
primary_reviewers: vortexing, fizwit
---

There are a variety of tool and genome oriented reference datasets available in shared locations at the Fred Hutch.  To orient you to some basic sources of shared reference data sets there are some available on our filesystem (Local) and some available in cloud-based locations (Cloud).  

For these data locations organization is critical to make it easier for people to find what they need.  However for both Local and Cloud based reference data, users are likely to use hard coded paths to these inputs in their processes.  Thus, we do require users to be a little flexible in filtering through these resources manually a bit to find what you need as the resources evolve.  If a new location makes more sense for a data set we have to balance all the code that will be broken if we just move it.  To that same end, however, keep in mind that these locations should not be interpreted as immutable and thus may require adjustments in the future should filesystem or cloud based storage organization need to be changed. Consider writing your code in such a way that these datasets could be easily updated in an environment variable or workflow input file.   

## Local Reference Data



## Cloud Reference Data

### AWS S3
Currently there is a bucket containing a variety of reference datasets that are commonly used by multiple tools or multiple users in an S3 bucket called: `fh-ctr-public-reference-data`.  If you would like to see more data be available here, you can post in our [Slack Question and Answer channel](https://fhbig.slack.com/archives/CD3HGJHJT) to ask if others would also like to have that dataset or if someone already does.  Then you (or whoever has the dataset already downloaded) can file a ticket to `scicomp` and request that it be moved into this public S3 bucket (include a path to the dataset in the filesystem or a public data source location in your ticket).

#### S3 Bucket Organization
Currently the bucket is generally organized by:
- genome_data - all data that is specific to certain genomes and organized by species and version, ideally with source and date obtained clearly stated.
- reagent_specific_data - all data that is linked to an analysis due to the particular reagents used such as hybrid capture bed files.
- tool_specific_data - all data that is specifically required by a tool itself like custom indexes or the like that are generally generated once per genome or build and used repeatedly.
- wiki_example_data - contains example data for Wiki-related examples
- workflow_testing_data - contains example data for Nextflow or Cromwell based workflows shared between users at the Fred Hutch
