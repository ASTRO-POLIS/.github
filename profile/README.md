# POLIS — Public Observatory Location and Information Service

## What is POLIS?

POLIS is an open standard for describing astronomical observing facilities on Earth and in space. It was developed out of a need for a common way of obtaining information about observatories, their instruments, capabilities and access arrangements.

Similar in principle to the Domain Name System (DNS), POLIS provides a distributed directory of observing facilities. Information can be maintained by the people who operate these facilities and made available through POLIS Providers to researchers, astronomers, observatory networks and software applications.

One of our aims is to make working across observing facilities easier, starting with knowing what each can offer. Further levels of the standard are designed to support the exchange of operational information and the coordination of observations between sites.

POLIS is intended for all types of observing facilities, including professional and amateur observatories, ground-based and space-based instruments, and mobile or temporary observing installations.

## The three service levels of POLIS

POLIS distinguishes between three levels of services, allowing observatories to participate according to their needs and the extent to which their infrastructure is automated.

| Service level | Description |
|---|---|
| **Level 1 — Static information** | Describes an observing facility, its location, instruments, supported configurations and access arrangements. Information is updated whenever changes are made to the facility. |
| **Level 2 — Dynamic information** | Provides information on changing instrument configurations, known changes in operational status, observing plans and longer-term scheduling and reservations. |
| **Level 3 — Real-time information** | Provides real-time information on observatory and instrument status and is designed to support observation scheduling, communication between observatories and collaborative observations. |

A Level 1 implementation requires no connection to telescope-control software. The information can be maintained manually or through software supporting the POLIS standard. Implementation of the second and third service levels is optional.

These further levels are designed to help coordinate observations across facilities, for example, to observe the same astronomical target simultaneously with different instruments or to maintain continuous monitoring of a target across observatories at different geographical longitudes.

## POLIS Providers

A POLIS Provider makes information about observing facilities available in accordance with the POLIS standard and its query APIs.

The standard distinguishes between four types of providers:

- **Public:** Providers making information about observing facilities available to the wider astronomical community.
- **Private:** Providers supporting the internal infrastructure of individual organisations or serving as local caches.
- **Mirror:** Providers serving as backups to public providers.
- **Experimental:** Providers used to develop and test new functionality and future versions of the standard.

This distributed architecture is intended to avoid a single point of failure. Different providers can offer complete or partial services.

Further information on provider types, requirements and the architecture of POLIS can be found in the [POLIS repository](https://github.com/ASTRO-POLIS/polis).

## POLIS — First light

On 17 September 2026, we presented *POLIS: Public Observatory Location and Information Service – first light* at [Our Unstable Universe](https://www.bao.am/meetings/meetings/BAO80/programme.php), the international symposium marking the 80th anniversary of the Byurakan Astrophysical Observatory of NAS RA in Armenia.

The presentation demonstrated an initial Level 1 implementation using static JSON files to describe Byurakan's observing facilities.

Our work now extends to further observatory descriptions, the development of tools for maintaining and accessing this information, and the further service levels of the POLIS standard.

## Project repositories

### [polis](https://github.com/ASTRO-POLIS/polis)

The main repository of the POLIS project. It contains the documentation of the POLIS standard, its architecture, service levels, provider types, and requirements for data formats and query APIs.

The most current documentation, proposals for new functionality and example files can be found in the [`dev` branch](https://github.com/ASTRO-POLIS/polis/tree/dev).

### [swift-polis](https://github.com/ASTRO-POLIS/swift-polis)

A Swift implementation of the POLIS standard, containing API types and a predefined set of commonly used constants.

Where possible, types follow those defined in [RTML (Remote Telescope Markup Language)](http://www.astro.physik.uni-goettingen.de/~hessman/misc/RTML-3.2b.xsd).

The implementation includes tests for encoding and decoding POLIS data in JSON, with XML support envisaged.

### [polis-providers](https://github.com/ASTRO-POLIS/polis-providers)

The repository dedicated to POLIS Providers.

## How to contribute

The usefulness of POLIS depends to a large extent on the participation of the astronomical community. The people best placed to describe an observatory and keep its information up to date are those who operate it.

We welcome contributions from observatories interested in making information about their facilities available through POLIS, checking and extending the information already collected, or helping us test and further develop the standard.

We are equally interested in hearing from researchers, developers, teachers and amateur astronomers about how they would use POLIS and what information would be useful to them.

For contributions, questions or further input, please contact us at [polis@tuparev.com](mailto:polis@tuparev.com).

## About the project

The idea for POLIS emerged from discussions at the Heterogeneous Telescope Networks (HTN) conferences in Tucson and Göttingen on exchanging information between observatories and negotiating observing time.

Following earlier work on a prototype and subsequent developments within the [SkyObserver](https://www.sky.observer) initiative, ASTRO-POLIS was established as an open-source project in November 2020.

The POLIS project is published under the MIT License.

[POLIS Observer](https://polis.observer/) · [SkyObserver](https://www.sky.observer) · [Tuparev Technologies](https://tuparev.com)
