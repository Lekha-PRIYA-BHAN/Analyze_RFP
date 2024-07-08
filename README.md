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

![image](https://github.com/Lekha-PRIYA-BHAN/Analyze_RFP/assets/167432155/a1e12229-f787-4b14-a306-65518801f162)


The documents that describe architecture and usage of a component are ingested into a vector database (provided in RFP Analyzer) using RFP Analyzer. Then RFP Analyzer provides a GUI to query these documents using NL and GenAI. The GenAI tool used is OpenAI public, hence all the documents you ingest into the Vector DB should not be private documents.

### Snapshots Demonstrating Usage

Query 1: Does the system read Arabic data?

The requirement 2.4.1 on page 4 of the provided RFP is used to query the database consisting of documents pertaining to Microsoft Cloud for Sustainability. The query and the response are both shown in the snapshot below.

![image](https://github.com/Lekha-PRIYA-BHAN/Analyze_RFP/assets/167432155/47dcfddc-c892-4a7b-ae30-2738573f9941)


Query 2: What other languages can be supported?

![image](https://github.com/Lekha-PRIYA-BHAN/Analyze_RFP/assets/167432155/a6e665c9-6def-45fa-b71d-ce3ce57c54e5)


Query 3: Need to migrate the current data into the system.



![image](https://github.com/Lekha-PRIYA-BHAN/Analyze_RFP/assets/167432155/e4a76ed9-6a3a-4c97-8150-fad3537a783b)


Query 4: Capability to retain past years’ data (up to 5 years of data).

![image](https://github.com/Lekha-PRIYA-BHAN/Analyze_RFP/assets/167432155/495be2a1-6560-4293-8813-2b7055ba90e8)


### Quality of Responses

Although only a few queries and their responses are shown above but we ran almost all the queries in the RFP and the responses were of very high quality, providing support to using this tool for RFPs as we have stated above.

