![ga4gh logo](http://genomicsandhealth.org/files/logo_ga.png)

Schemas for the Workflow Execution API
======================================

This is used by the Data Working Group - Containers and Workflows Task Team

![](http://online.swagger.io/validator/?url=https://raw.githubusercontent.com/ga4gh/tool-registry-schemas/develop/src/main/resources/swagger/ga4gh-tool-discovery.yaml)

The [Global Alliance for Genomics and Health](http://genomicsandhealth.org/) is an international
coalition, formed to enable the sharing of genomic and clinical data.

The [Data Working Group](http://ga4gh.org/#/) concentrates on data representation, storage,
and analysis, including working with platform development partners and
industry leaders to develop standards that will facilitate
interoperability.

Containers and Workflows Task Team
----------------------------------

The Containers & Workflows working group is an informal, multi-vendor working group born out of the BOSC 2014 codefest, consisting of various organizations and individuals that have an interest in portability of data analysis workflows. Our goal is to create specifications that enable data scientists to describe analysis tools and workflows that are powerful, easy to use, portable, and support reproducibility for a variety of problem areas including data-intensive science like bioinformatics, physics, and astronomy; and business analytics such as log analysis, data mining, and ETL.

What is this?
------------

Currently, this is the home of the Workflow Execution API proposal. The Workflow Execution API is a minimal common API describing how a user can submit workflow requests to workflow execution systems in a standardized ways.
Workflow execution engines (SevenBridges, FireCloud, etc) can support this API so users can make workflow requests
programmatically, adding the ability to scale up.  In addition, these workflow services could have (and probably do have)
UIs that would (possibly) use this API under the hood to facilitate workflow execution requests.

Having this standard API supported by multiple execution engines will give people options of processing
the same workflow (CWL or WDL) across different workflow execution platforms running across various clouds/environments.
As an example use case, I can find a workflow in CWL on [Dockstore.org](http://dockstore.org), use Dockstore to
generate a JSON parameterization file, and submit this to SevenBridges/FireCloud/Consonance or some other GA4GH-compliant
workflow execution service.  NOTE: I'm making the leap of faith here that SevenBridges/FireCloud and/or other
systems support this API, this example is not an endorsement or commitment to support the API by these
providers, just an example of how that would work if they did.

Key features of the current API proposal:

* ability to request a workflow run using CWL or WDL (and maybe future formats)
* ability to parameterize that workflow using a JSON schema that's simple and used in common between CWL and WDL
* ability to get information about running workflows, status, errors, output file locations etc

Outstanding questions:

* JSON parameterization format, see work by Peter, is that checked in?
* standardizing terms, job, workflow, steps, tools, etc

How to view
------------

See the swagger editor to view our [schema in progress](http://editor.swagger.io/#/?import=https://raw.githubusercontent.com/ga4gh/workflow-execution-schemas/develop/src/main/resources/swagger/ga4gh-tool-discovery.yaml).

If the current schema fails to validate, visit [debugging](http://online.swagger.io/validator/debug?url=https://raw.githubusercontent.com/ga4gh/workflow-execution-schemas/develop/src/main/resources/swagger/ga4gh-tool-discovery.yaml)



How to contribute changes
-------------------------

Take cues for now from the [ga4gh/schemas](https://github.com/ga4gh/schemas/blob/master/CONTRIBUTING.rst) document.

License
-------

See the [LICENSE]

  []: http://genomicsandhealth.org/files/logo_ga.png
  [Global Alliance for Genomics and Health]: http://genomicsandhealth.org/
  [INSTALL.md]: INSTALL.md
  [CONTRIBUTING.md]: CONTRIBUTING.md
  [LICENSE]: LICENSE
  [Google Forum]: https://groups.google.com/forum/#!forum/ga4gh-dwg-containers-workflows
