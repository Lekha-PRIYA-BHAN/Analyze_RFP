# RFP Analyzer

## Overview

Solutioners are pressed for time and skills when they have to get a sense of what requirements in an RFP (Request for Proposal) can be straightforwardly met from the products, services, and components that are expected to be part of the solution, and what are the gaps requiring special effort. This will help answer the RFPs more accurately besides reducing the time to response.

## Problem Statement

Imagine a solutioner persona, Sanjay, receiving an RFP (Request for Proposal) to be answered within a week's time. The technical areas that will be required to answer this RFP are not easily available and also because an RFP on these topics have come after a long time the solutioner team (including architects) are a bit rusty. As a consequence, to create a solution to meet this RFP within time and create a solution of high quality will become a challenge.

## Solution

RFP Analyzer is an GenAI based tool that can be installed on a solutioner's workstation or laptop and allows the solutioner to run Natural Language (NL) queries based on the RFP to obtain answers whether the potential solution components can actually meet the requirement.

This provides a sense of what can be met straightforwardly from the components including products and services that can be integrated together to form the solution as well as what are gaps and therefore efforts can be put first in these directions to meet the gaps.

## Demonstration

A RFP for a sustainability solution is received (see [here](ESG_RFP.pdf)). The solutioner intends to provide a solution  that is based of off the [Microsoft Cloud for Sustainability](https://learn.microsoft.com/en-us/industry/sustainability/overview). How a solutioner can pick queries being asked in the RFP and use the RFP Analyzer tool to receive answers is demoed below. But before that an architecture of how the RFP Analyzer can be used is provided.

### Architecture of RFP Analyzer

Figure: Architecture for Analyze RFP

![1694198421438](image/README/1694198421438.png)

The documents that describe architecture and usage of a component are ingested into a vector database (provided in RFP Analyzer) using RFP Analyzer. Then RFP Analyzer provides a GUI to query these documents using NL and GenAI. The GenAI tool used is OpenAI public, hence all the documents you ingest into the Vector DB should not be private documents.

### Snapshots Demonstrating Usage

Query 1: Does the system read Arabic data?

The requirement 2.4.1 on page 4 of the provided RFP is used to query the database consisting of documents pertaining to Microsoft Cloud for Sustainability. The query and the response are both shown in the snapshot below.

![1694195921238](image/README/1694195921238.png)

Query 2: What other languages can be supported?

![1694196273983](image/README/1694196273983.png)

Query 3: Need to migrate the current data into the system.

![1694196721731](image/README/1694196721731.png)

![1694196764241](image/README/1694196764241.png)

Query 4: Capability to retain past years’ data (up to 5 years of data).

![1694196907925](image/README/1694196907925.png)

### Quality of Responses

Although only a few queries and their responses are shown above but we ran almost all the queries in the RFP and the responses were of very high quality, providing support to using this tool for RFPs as we have stated above.

## Deployment of RFP Analyzer for Sustainability

Deploy [ingest](https://github.kyndryl.net/Innovation-Council/ingest) and [query](https://github.kyndryl.net/Innovation-Council/query) repositories which are part of the the *Innovation Council* github organization. Once you have installed the tooling then copy the file `chatbot v3.py` in this repository to the repository folder of [query](https://github.kyndryl.net/Innovation-Council/query).

Unzip and then ingest the documents [industry-sustainability.pdf](industry-sustainability.rar) and [industry-well-architected.pdf](industry-well-architected.rar) using the [ingest](https://github.kyndryl.net/Innovation-Council/ingest) tool you have deployed above.

The above tool can be customized for any domain in which the RFP is obtained.
