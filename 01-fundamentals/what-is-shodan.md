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
