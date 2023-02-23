---
tag:General
---

# 1. Record architecture decisions

Date: 2023-02-16

## Status

Accepted

## Context

There is a desire to document decisions made during the construction of the new Ensembl product which is broken up into multiple repositories within [Ensembl Github organisation](https://github.com/Ensembl). The documentation process needs to be light to ensure a low cost of ownership, to this end it was previously decided to use ADRs. These ADRs live in a few places and suffered from doubt on what a good ADR looks like. Although it is recommended that ADRs live as close to the code as possible this recommendation does not cater for projects that are split across multiple repositories. This led to gaps in ADRs where decisions occurred upstream of repository specific ADRs.

## Decision

It has been decided that **all ADRs for the Ensembl project will live in a central repository**. This ADR has the date of when the this decision was made, the following ADRs will have older dates as it is important to preserve when the decisions where made.

## Consequences

- Good - A single place to find decisions 
- Good - A chance to clean up existing ADRs
- Bad - Existing ADRs need to be migrated to this repo
