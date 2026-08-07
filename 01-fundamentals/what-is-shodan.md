# What is Shodan?

## Overview

Shodan is a search engine designed to discover and analyze Internet-connected devices and services.

Unlike traditional search engines such as Google, which primarily index web pages, Shodan collects information from services exposed on the Internet.

This makes Shodan particularly useful for cybersecurity, OSINT, attack surface management, threat intelligence, and security research.

## How Shodan sees the Internet

A useful way to understand Shodan is to think about the relationship between:

```text
Internet
   │
   ├── Devices / Hosts
   │      │
   │      └── Services
   │             │
   │             ├── Port
   │             ├── Protocol
   │             ├── Product
   │             ├── Version
   │             └── Banner
   │
   └── Shodan
          │
          └── Collects publicly observable information



A device can expose multiple services, and each service can provide different information.

For example, a web server may expose information about:

HTTP/HTTPS
Web server software
Software version
HTTP headers
TLS/SSL information
Domain names
Network ownership
Geographic information

The information collected for a service is represented through a banner.

What is a banner?

A banner is metadata obtained from a service running on an Internet-connected device.

A simplified example:

HTTP/1.1 200 OK
Server: nginx/1.1.19
Content-Type: text/html


From this information we may be able to infer:

The service is responding to HTTP.
The web server appears to be nginx.
A software version may be exposed.
Additional metadata may be available depending on the service.

Shodan describes the banner as the fundamental unit of data it collects.

Why is this relevant to cybersecurity?

The information indexed by Shodan can be used to understand Internet exposure.

From a defensive perspective, an organization can use Shodan to ask questions such as:

Which of our assets are visible from the Internet?
Which services are exposed?
Which technologies are being used?
Are software versions being disclosed?
Has an unexpected service become publicly accessible?
How does our external attack surface change over time?

This makes Shodan useful as one source of information for external attack surface analysis.

Shodan vs. Google

The main conceptual difference is:

| Google                               | Shodan                                      |
| ------------------------------------ | ------------------------------------------- |
| Primarily indexes web content        | Indexes Internet-facing services            |
| Focuses on websites and web pages    | Focuses on devices and services             |
| Searches web documents               | Searches service metadata and banners       |
| Useful for web information discovery | Useful for infrastructure exposure analysis |


Shodan itself describes the distinction as Google crawling the World Wide Web while Shodan crawls the Internet.

Security perspective

The existence of a service in Shodan does not automatically mean that the service is vulnerable.

An exposed service can be:

intentional;
properly secured;
protected by authentication;
restricted by network controls;
outdated;
misconfigured;
or potentially vulnerable.

Therefore, Shodan results should be treated as evidence for further analysis, not as an automatic vulnerability finding.

This distinction will be important throughout this laboratory.


Responsible use

This project uses Shodan for educational, defensive, and authorized security research.

The repository will not intentionally publish:

Credentials
API keys
Personal information
Sensitive customer information
Unauthorized access information
Exploit instructions against third-party systems
Sensitive infrastructure details belonging to third parties

Whenever practical exercises involve real Internet infrastructure, results will be limited, anonymized, or replaced with authorized targets.

Key learnings
Shodan is an Internet-connected device and service search engine.
Shodan focuses on services rather than simply web pages.
Banners are a fundamental unit of Shodan data.
A host can expose multiple services.
Exposed information does not automatically mean a vulnerability exists.
Shodan can provide valuable visibility into external attack surface.
Search results must be interpreted in their security context.

References
Shodan Help Center — What is Shodan?
Shodan Help Center — Search Query Fundamentals
