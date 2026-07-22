# MPGV Monitor Thesis Documentation — Master TODO

> Purpose: master checklist for revising the thesis so it accurately documents the current MPGV Monitor implementation. This file is an audit plan only; completing an item may require a later thesis edit.
>
> Audit baseline (2026-07-22): main document `MPGV Monitor.tex` (article class; numbered sections act as chapters), `references.bib`, `declaration_of_access.tex`, `praufa_copy.tex`, and `Screenshots/`. Current implementation baseline: the `iceland-quake-monitoring-leaflet` repository.
>
> Detected inventory: 10 numbered main-matter sections, 3 appendices, 19 figure environments (21 embedded image files), 12 table environments, 22 unnumbered `verbatim` code/command blocks, and 21 BibTeX entries.

## Overall Progress

- [ ] Thesis fully reviewed
- [ ] Front matter updated
- [ ] All chapters updated
- [ ] All appendices updated
- [ ] Figures updated
- [ ] Tables updated
- [ ] Screenshots updated
- [ ] Architecture updated
- [ ] Algorithms verified
- [ ] UI descriptions updated
- [ ] References checked
- [ ] Bibliography cleaned
- [ ] Final proofreading completed
- [ ] Final PDF reviewed

## Project Structure and Build Baseline

- [ ] Confirm `MPGV Monitor.tex` is the canonical thesis entry point
- [ ] Confirm `declaration_of_access.tex` is a separate deliverable and whether it belongs in the final submission package
- [ ] Confirm `praufa_copy.tex` is template/reference material only and exclude its sample content from thesis auditing
- [ ] Confirm `references.bib` is the only bibliography database used by the main thesis
- [ ] Inventory every file required to build the final PDF
- [ ] Decide whether the monolithic main file should remain monolithic or be split into maintainable chapter files during a later revision
- [ ] Confirm all assets referenced by the main document exist under `Screenshots/`
- [ ] Review unused asset `Screenshots/Installing_Libs.png` and remove it later or document why it is retained
- [ ] Verify filename capitalization and spaces work on the final build platform
- [ ] Record the required LaTeX engine, packages, build command, and build environment
- [ ] Preserve a clean build log as revision evidence

## Front Matter

### Title and submission pages

- [ ] Verify thesis title, author, programme, institution, supervisors, date, and degree wording
- [ ] Verify banner image and University of Iceland branding
- [ ] Verify access/declaration details against current submission requirements
- [ ] Verify page numbering and front-matter ordering

### Abstract

- [x] Read entire abstract
- [x] Align objectives, methods, implementation, and results with the current system
- [x] Mention current MapLibre/deck.gl architecture and Insights capability where academically appropriate
- [x] Remove claims about superseded Leaflet-only or planned functionality
- [x] Verify terminology and word count

### Ágrip

- [x] Read the complete Icelandic summary
- [x] Keep it semantically aligned with the final English abstract
- [x] Verify Icelandic technical terminology and proofreading

### Abbreviations

- [ ] Verify every abbreviation is used and defined at first use
- [ ] Add current implementation abbreviations where needed (API, CSP, CSV, EPOS, GPU, IMO, MPGV, REST, WFS, etc.)
- [ ] Remove obsolete abbreviations
- [ ] Alphabetize and format consistently

### Acknowledgments

- [ ] Verify names, roles, spelling, institutional acknowledgments, and tone

## Chapter Checklist

> Because the document uses `article`, the detected numbered `\section` headings are treated as chapters below.

### Chapter 1 – Introduction

Detected subsections: Context and Motivation; Need for a Modern Monitoring Tool; System Features; Contributions and Future Directions.

- [x] Read entire chapter
- [x] Verify technical accuracy
- [x] Compare with current implementation
- [x] Remove outdated information
- [x] Add missing implementation details
- [x] Improve academic writing
- [x] Check terminology consistency
- [x] Verify equations (if any)
- [ ] Verify citations
- [x] Verify figures (none in Chapter 1)
- [x] Verify tables (none in Chapter 1)
- [x] Verify code listings (none in Chapter 1)
- [x] Verify references to other chapters
- [x] Align research problem, aims, scope, contributions, and thesis outline
- [x] Distinguish implemented contributions from future work
- [ ] Mark chapter complete

### Chapter 2 – Background and Related Work

Detected subsections: Seismotectonic Context of Iceland; Interactive Web Mapping: Frameworks and Tile Architectures; Existing Earthquake Visualization Platforms; Visual Encoding of Seismic Data; Multi-Source Data Integration; Backend Architecture; ShakeMap and Derived Hazard Products; Where Existing Approaches Fall Short; Positioning of MPGV Monitor.

- [ ] Read entire chapter
- [ ] Verify technical accuracy
- [ ] Compare with current implementation
- [ ] Remove outdated information
- [ ] Add missing implementation details
- [ ] Improve academic writing
- [ ] Check terminology consistency
- [ ] Verify equations (if any)
- [ ] Verify citations
- [ ] Verify figures
- [ ] Verify tables
- [ ] Verify code listings
- [ ] Verify references to other chapters
- [ ] Replace Leaflet/React-Leaflet-specific architecture claims with the current MapLibre GL/deck.gl design where applicable
- [ ] Recheck comparisons with IMO, USGS, EMSC, and IRIS against current services
- [ ] Verify literature supports every architectural and visualization claim
- [ ] Verify the novelty/positioning argument remains defensible
- [ ] Mark chapter complete

### Chapter 3 – Project Overview

Detected subsections: Initial Setup; Data Sources.

- [ ] Read entire chapter
- [ ] Verify technical accuracy
- [ ] Compare with current implementation
- [ ] Remove outdated information
- [ ] Add missing implementation details
- [ ] Improve academic writing
- [ ] Check terminology consistency
- [ ] Verify equations (if any)
- [ ] Verify citations
- [ ] Verify figures
- [ ] Verify tables
- [ ] Verify code listings
- [ ] Verify references to other chapters
- [ ] Clearly label Folium and Vite material as historical where retained
- [ ] Update data-source roles: MPGV archive, IMO Quakes/Skjálftalísa API, EPOS volcano/ShakeMap data, and EGDI/HIKE WFS faults/fissures
- [ ] Verify public catalogue threshold and coverage dates
- [ ] Mark chapter complete

### Chapter 4 – Data Scraping and Merging

Detected subsections: Initial Approach; Previous Approaches (Manual Scraping with Text File Storage; Dynamic Scraping with CSV Storage); Current Approach: Multi-Source Ingestion and Conceptual Merging (Automated Updates with Periodic Jobs; Conceptual Ingestion and Merge Pipeline; Illustrative Ingestion and Merging Workflow; Evolution of the Data Pipeline).

- [ ] Read entire chapter
- [ ] Verify technical accuracy
- [ ] Compare with current implementation
- [ ] Remove outdated information
- [ ] Add missing implementation details
- [ ] Improve academic writing
- [ ] Check terminology consistency
- [ ] Verify equations (if any)
- [ ] Verify citations
- [ ] Verify figures
- [ ] Verify tables
- [ ] Verify code listings
- [ ] Verify references to other chapters
- [ ] Separate historical approaches from the production pipeline
- [ ] Verify scrape cadence, source windows, parsing, validation, storage, error handling, and idempotency
- [ ] Replace “conceptual” descriptions with verified implementation detail where the feature now exists
- [ ] Verify terminology for MPGV-only (`v_only`), matched, and Quakes/Skjálftalísa source records
- [ ] Mark chapter complete

### Chapter 5 – Backend Development

Detected subsections: Core Database Models; Dynamic Data Ingestion; Automated Scheduling; Reconciliation and Merging; ShakeMap Validation Pipeline (Validation Procedure; Audit Mode and Evaluation Results); Flask API Layer; Summary.

- [ ] Read entire chapter
- [ ] Verify technical accuracy
- [ ] Compare with current implementation
- [ ] Remove outdated information
- [ ] Add missing implementation details
- [ ] Improve academic writing
- [ ] Check terminology consistency
- [ ] Verify equations (if any)
- [ ] Verify citations
- [ ] Verify figures
- [ ] Verify tables
- [ ] Verify code listings
- [ ] Verify references to other chapters
- [ ] Verify every SQLAlchemy model and database field against `backend/app.py`
- [ ] Verify scheduler interval, job order, locking, startup behavior, and failure handling
- [ ] Verify reconciliation thresholds and one-to-one conflict resolution against `backend/reconcile.py`
- [ ] Verify ShakeMap lookup, allowlisted hosts, caching, audit workflow, and current evaluation results
- [ ] Document current API routes, query limits, response limits, caching, CORS/CSP, rate limiting, and admin authentication
- [ ] Verify SQLite limitations and deployment implications
- [ ] Mark chapter complete

### Chapter 6 – Frontend Architecture and Implementation

Detected subsections: Migration from Google Maps to Leaflet; User Interface Overview and Interaction Goals; Frontend Codebase Structure; Leaflet Integration and Tile Layer Architecture; Backend Connection; Top-Level Orchestration; Map Rendering and Marker Lifecycle; Basemap Selection; Temporal Filtering; Magnitude Thresholding; Volcano Overlay; Latitude/Longitude Grid Overlay; About Modal; State Interaction Model and Cross-Component Consistency; Rendering Pipeline and Performance Considerations; Comparison with Existing Seismic Web Applications; Summary.

- [ ] Read entire chapter
- [ ] Verify technical accuracy
- [ ] Compare with current implementation
- [ ] Remove outdated information
- [ ] Add missing implementation details
- [ ] Improve academic writing
- [ ] Check terminology consistency
- [ ] Verify equations (if any)
- [ ] Verify citations
- [ ] Verify figures
- [ ] Verify tables
- [ ] Verify code listings
- [ ] Verify references to other chapters
- [ ] Retitle/restructure Leaflet-specific material for the current React + MapLibre GL + deck.gl implementation
- [ ] Document current component and `analysis/` directory structure
- [ ] Verify basemap providers, fallback behavior, attribution, tile licensing, and base path
- [ ] Document fault/fissure WFS loading, onshore filtering, styling, attribution, and caching
- [ ] Document Recent Selections and state preservation between Map and Insights
- [ ] Document heatmap behavior and intentionally unavailable marker selection
- [ ] Document responsive/mobile controls and touch behavior
- [ ] Document the Insights page, filters, summaries, charts, tables, exports, and View on Map flow
- [ ] Mark chapter complete

### Chapter 7 – Final Features

Detected subsections: Final Feature Polishing (Heatmap Gradient and Radius Tuning; Latitude/Longitude Grid Overlay; Marker Rendering Performance; Z-Index Alignment; CSV Export; User Feedback and Interface Adjustments).

- [ ] Read entire chapter
- [ ] Verify technical accuracy
- [ ] Compare with current implementation
- [ ] Remove outdated information
- [ ] Add missing implementation details
- [ ] Improve academic writing
- [ ] Check terminology consistency
- [ ] Verify equations (if any)
- [ ] Verify citations
- [ ] Verify figures
- [ ] Verify tables
- [ ] Verify code listings
- [ ] Verify references to other chapters
- [ ] Reframe “final” features to include all features implemented after the Leaflet-era text
- [ ] Verify current heatmap weights, gradient, radius/intensity, zoom behavior, and density-first rationale
- [ ] Verify marker implementation/performance claims for deck.gl rather than Leaflet canvas markers
- [ ] Verify CSV export scope, limits, columns, metadata, and Insights filtered export
- [ ] Incorporate documented user feedback and identify the evaluation method
- [ ] Mark chapter complete

### Chapter 8 – Deployment, Testing & Debugging

Detected subsections: Backend & Frontend Testing; Early Deployment Testing (Historical) (Setup and Challenges; Lessons Learned); Production Deployment; Model Deployment.

- [ ] Read entire chapter
- [ ] Verify technical accuracy
- [ ] Compare with current implementation
- [ ] Remove outdated information
- [ ] Add missing implementation details
- [ ] Improve academic writing
- [ ] Check terminology consistency
- [ ] Verify equations (if any)
- [ ] Verify citations
- [ ] Verify figures
- [ ] Verify tables
- [ ] Verify code listings
- [ ] Verify references to other chapters
- [ ] Verify current automated test inventory and report reproducible results
- [ ] Verify current Pluto deployment command, port, `/mpgv/` base path, static serving, and health checks
- [ ] Clearly separate historical deployment from current production/deployment state
- [ ] Document environment configuration, scheduler configuration, logging, backups, and recovery
- [ ] Document security hardening and rate-limit deployment requirements
- [ ] Move unimplemented model deployment to Future Development if it remains prospective
- [ ] Add performance/load-testing method and results or explicitly delimit them
- [ ] Mark chapter complete

### Chapter 9 – Future Development

Detected subsections: Accessibility and Inclusive Design; Automated Data Analysis and Visualization; Mobile Application; Prediction Model; Tile Provider Licensing for Production Deployment; Database Migration; Additional Enhancements.

- [ ] Read entire chapter
- [ ] Verify technical accuracy
- [ ] Compare with current implementation
- [ ] Remove outdated information
- [ ] Add missing implementation details
- [ ] Improve academic writing
- [ ] Check terminology consistency
- [ ] Verify equations (if any)
- [ ] Verify citations
- [ ] Verify figures
- [ ] Verify tables
- [ ] Verify code listings
- [ ] Verify references to other chapters
- [ ] Remove/move items already implemented (Insights charts, summary dashboard, responsive/mobile web support, etc.)
- [ ] Distinguish mobile-responsive web support from a native mobile application
- [ ] Reassess accessibility gaps against the current UI and current WCAG guidance
- [ ] Verify licensing work still outstanding for every active/fallback map provider
- [ ] Prioritize future work and identify dependencies, risks, and evaluation criteria
- [ ] Avoid presenting speculative prediction work as an implemented deliverable
- [ ] Mark chapter complete

### Chapter 10 – Conclusion

- [ ] Read entire chapter
- [ ] Verify technical accuracy
- [ ] Compare with current implementation
- [ ] Remove outdated information
- [ ] Add missing implementation details
- [ ] Improve academic writing
- [ ] Check terminology consistency
- [ ] Verify equations (if any)
- [ ] Verify citations
- [ ] Verify figures
- [ ] Verify tables
- [ ] Verify code listings
- [ ] Verify references to other chapters
- [ ] Answer the final research aims/questions explicitly
- [ ] Summarize verified contributions without introducing new claims
- [ ] State limitations and future work consistently with Chapters 8–9
- [ ] Mark chapter complete

## Appendix Checklist

### Appendix A – Installation and Running

Detected subsections: Prerequisites; Clone the Repository; Backend Setup; Frontend Setup; Running Tests; Common Issues.

- [ ] Test every command from a clean supported environment
- [ ] Verify repository URL, branch assumptions, directory names, prerequisites, and version requirements
- [ ] Align local instructions with `run-local.sh`, scheduler defaults, environment variables, and frontend/backend base URLs
- [ ] Verify backend and frontend test commands
- [ ] Document Windows/Linux differences where relevant
- [ ] Remove secrets, private endpoints, and machine-specific values
- [ ] Mark appendix complete

### Appendix B – API Reference

Detected subsection: Example `/earthquakes` Response.

- [ ] Inventory all current public, maintenance, export, health, Insights, volcano, reconciliation, and ShakeMap endpoints
- [ ] Verify methods, paths, parameters, response schemas, status codes, authentication, and rate limits
- [ ] Verify the `/earthquakes` example against a current real response schema
- [ ] Document API limits and error responses, including HTTP 400/401/403/405/429/5xx as applicable
- [ ] Distinguish public GET routes from authenticated maintenance POST routes
- [ ] Mark appendix complete

### Appendix C – Database Schema

Detected model tables: Earthquake; EarthquakeSRaw; EarthquakeMerged; Volcano; ShakeMapLink.

- [ ] Verify all five documented tables against current SQLAlchemy/SQLite schema
- [ ] Verify names, types, nullability, keys, indexes, unique constraints, and relationships
- [ ] Explain source-of-truth and provenance semantics for raw and merged earthquake rows
- [ ] Verify volcano refresh/replacement safety behavior
- [ ] Verify ShakeMap cache/audit fields
- [ ] Add captions and labels to all five currently uncaptioned schema tables
- [ ] Mark appendix complete

## Figures

> Numbering below follows source order. Final numbers must be confirmed from a clean LaTeX build. A figure can contain more than one image. Apply every checkbox to each figure.

### Figure 1 – Early Folium prototype (`Screenshots/Folium_Map_version.png`, source line 507)

- [ ] Screenshot still matches the historical version being described
- [ ] Caption accurate
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Add a stable `\label` if the figure is retained

### Figure 2 – Vite development server (`Screenshots/Vite_terminal.png`, line 522)

- [ ] Screenshot still matches the current or explicitly historical setup
- [ ] Caption accurate
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Add a stable `\label` if retained

### Figure 3 – IMO/MPGV source website (`Screenshots/hraun_vedur.png`, line 534)

- [ ] Screenshot still matches the source website or is dated as historical
- [ ] Caption accurate
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Add a stable `\label` if retained

### Figure 4 – MPGV year/month/tabular source examples (`Year.png`, `Month.png`, `Data.png`, line 542)

- [ ] All three screenshots still match the sources or are dated as historical
- [ ] Composite layout, cropping, and sizing are consistent
- [ ] Caption accurate and MPGV capitalization corrected
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Add a stable `\label` if retained

### Figure 5 – Skjálftalísa API documentation (`Screenshots/S_Api.png`, line 561)

- [ ] Screenshot still matches current API documentation
- [ ] Caption accurate
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Add a stable `\label` if retained

### Figure 6 – Skjálftalísa event JSON (`Screenshots/Quake_event.png`, line 569)

- [ ] Screenshot still matches the current response schema
- [ ] Sensitive/irrelevant content is excluded
- [ ] Caption accurate
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Add a stable `\label` if retained

### Figure 7 – Initial raw MPGV data (`Screenshots/Raw_Data.png`, line 601)

- [ ] Screenshot accurately represents the stated October 2023 historical dataset
- [ ] Caption accurate
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Add a stable `\label` if retained

### Figure 8 – CSV-based scraping flowchart (`Screenshots/CSV-based solution.png`, `fig:csv-flowchart`, line 656)

- [ ] Diagram matches the historical approach
- [ ] Caption accurate
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Source/editable diagram retained if available

### Figure 9 – Multi-source data pipeline (`Screenshots/Data_pipeline.png`, `fig:data-pipeline`, line 711)

- [ ] Diagram matches current ingestion and reconciliation pipeline
- [ ] Caption accurate
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Update source names, tables, cadence, and branch logic

### Figure 10 – Full system architecture (`Screenshots/MPGV_sys_arc.png`, `fig:system-architecture`, line 738)

- [ ] Diagram matches current frontend, backend, database, APIs, external services, security, and deployment
- [ ] Caption accurate
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Replace Leaflet-era elements with MapLibre/deck.gl and Insights architecture

### Figure 11 – APScheduler workflow (`Screenshots/APScheduler_working.png`, line 913)

- [ ] Diagram matches current job sequence and three-minute cadence
- [ ] Caption accurately distinguishes scheduled jobs from on-demand ShakeMap work
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Add a stable `\label` if retained

### Figure 12 – Reconciliation workflow (`Screenshots/Reconciliation workflow.png`, `fig:reconcile-workflow`, line 940)

- [ ] Diagram matches current thresholds and one-to-one candidate allocation
- [ ] Caption accurate
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Include competing-MPGV-row behavior and `v_only` fallback

### Figure 13 – ShakeMap validation workflow (`Screenshots/ShakeMap validation workflow.png`, line 1009)

- [ ] Diagram matches current on-demand lookup, validation, URL allowlisting, and cache/audit behavior
- [ ] Caption accurate
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Add a stable `\label` if retained

### Figure 14 – Main web application (`Screenshots/Webapp_front.png`, line 1136)

- [ ] Replace with the latest MapLibre/deck.gl UI
- [ ] Show current controls/layers without obscuring key content
- [ ] Caption no longer describes the frontend as Leaflet-based
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Add a stable `\label`

### Figure 15 – Frontend mapping integration (`Screenshots/Frontend integration.png`, line 1194)

- [ ] Replace Leaflet architecture with current MapLibre/deck.gl integration and raster fallback
- [ ] Caption accurate
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Add a stable `\label`

### Figure 16 – Frontend data flow (`Screenshots/Frontend data flow.png`, line 1227)

- [ ] Diagram includes current Map and Insights flows, `/insights/limits`, navigation handoff, and relevant caching
- [ ] Caption accurate
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Add a stable `\label`

### Figure 17 – Event information panel (`Screenshots/info_window.png`, line 1277)

- [ ] Replace with latest earthquake card and current map UI if outdated
- [ ] Verify ShakeMap action, fields, volcano card behavior, grid, and overlays
- [ ] Caption accurate
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Add a stable `\label`

### Figure 18 – Early Pluto deployment (`Screenshots/Deployment_Testing.png`, line 1542)

- [ ] Retain only if it provides useful historical evidence
- [ ] Caption clearly identifies historical status
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Add a stable `\label` if retained

### Figure 19 – Pluto deployment terminal (`Screenshots/deployed_pluto.png`, line 1570)

- [ ] Screenshot matches current deployment procedure or is dated as historical
- [ ] Verify command, port, base path, and service process shown
- [ ] Caption accurate
- [ ] Figure number correct
- [ ] Referenced correctly in text
- [ ] Image resolution acceptable
- [ ] Add a stable `\label` if retained

### Non-float image asset

- [ ] Verify title-page `Screenshots/banner.png` quality, crop, licensing, and continued use (source line 93)

## Tables

> Numbering follows source order and must be confirmed from a clean build.

### Table 1 – Dataset coverage summary (`tab:data-coverage`, line 862)

- [ ] Values still correct
- [ ] Caption updated
- [ ] Numbering correct
- [ ] Mentioned in text
- [ ] Record dataset snapshot date and reproducible query

### Table 2 – ShakeMap audit summary (`tab:shakemap-audit`, line 1033)

- [ ] Values still correct
- [ ] Caption updated and fits on one coherent source block
- [ ] Numbering correct
- [ ] Mentioned in text
- [ ] Rerun audit and record configuration/date/sample size

### Table 3 – Basemap/tile providers (`tab:tile-providers`, line 1176)

- [ ] Values still correct for Map, Satellite, Terrain, Heatmap, and fallback sources
- [ ] Caption updated
- [ ] Numbering correct
- [ ] Mentioned in text
- [ ] Verify attribution and licences

### Table 4 – Frontend performance optimizations (`tab:frontend-perf`, line 1374)

- [ ] Values still correct for MapLibre/deck.gl implementation
- [ ] Caption updated
- [ ] Numbering correct
- [ ] Mentioned in text
- [ ] Support quantitative claims with measurements

### Table 5 – Seismic web application comparison (`tab:seismic_comparison`, line 1411)

- [ ] Values still correct
- [ ] Caption updated
- [ ] Numbering correct
- [ ] Mentioned in text
- [ ] Date the comparison and cite each external product claim

### Table 6 – Heatmap radii (`tab:heatmap-radii`, line 1455)

- [ ] Values still correct for current MapLibre heatmap expressions
- [ ] Caption updated
- [ ] Numbering correct
- [ ] Mentioned in text
- [ ] Verify intensity and weight settings are documented alongside radius

### Table 7 – API endpoints (`tab:api-endpoints`, line 1750)

- [ ] Values still correct
- [ ] Caption updated
- [ ] Numbering correct
- [ ] Mentioned in text
- [ ] Add current methods, authentication, limits, and Insights/security endpoints

### Table 8 – Earthquake schema (line 1798; currently no caption/label)

- [ ] Values still correct
- [ ] Add/update caption
- [ ] Add label and verify numbering
- [ ] Mentioned in text

### Table 9 – EarthquakeSRaw schema (line 1817; currently no caption/label)

- [ ] Values still correct
- [ ] Add/update caption
- [ ] Add label and verify numbering
- [ ] Mentioned in text

### Table 10 – EarthquakeMerged schema (line 1837; currently no caption/label)

- [ ] Values still correct
- [ ] Add/update caption
- [ ] Add label and verify numbering
- [ ] Mentioned in text

### Table 11 – Volcano schema (line 1862; currently no caption/label)

- [ ] Values still correct
- [ ] Add/update caption
- [ ] Add label and verify numbering
- [ ] Mentioned in text

### Table 12 – ShakeMapLink schema (line 1883; currently no caption/label)

- [ ] Values still correct
- [ ] Add/update caption
- [ ] Add label and verify numbering
- [ ] Mentioned in text

## Code Listings and Command Blocks

> The thesis currently has no `lstlisting`, `minted`, or numbered listing floats. The following 22 blocks use uncaptioned/unlabelled `verbatim`. For each, decide whether to convert it to a formal listing, a concise pseudocode/algorithm, a terminal block, or remove it.

Apply to every block:

- [ ] Matches current implementation
- [ ] Still necessary
- [ ] Syntax highlighting/language identification correct
- [ ] Caption added or updated if treated as a listing
- [ ] Label and in-text reference added if treated as a numbered listing
- [ ] Long lines wrap without overflow
- [ ] Excerpt is minimal and academically explained

Detected blocks:

- [ ] CSV scraper `scrape_all_to_csv()` (line 629)
- [ ] `Earthquake` model (line 753)
- [ ] `EarthquakeSRaw` model (line 765)
- [ ] `EarthquakeMerged` model (line 778)
- [ ] `Volcano` model (line 797)
- [ ] `ShakeMapLink` model (line 811)
- [ ] APScheduler configuration (line 887)
- [ ] Reconciliation loop beginning `for v in v_rows` (line 951)
- [ ] ShakeMap validator command (line 1019)
- [ ] Flask `/earthquakes` route (line 1073)
- [ ] Frontend `fetchEarthquakeData()` API helper (line 1214)
- [ ] Timeline/magnitude marker colour selection (line 1312)
- [ ] Historical Gunicorn deployment command (line 1535)
- [ ] Repository clone command (line 1674)
- [ ] Backend directory/virtual-environment setup (line 1684)
- [ ] Backend dependency installation (line 1692)
- [ ] Backend development-server command (line 1697)
- [ ] Frontend directory/dependency setup (line 1708)
- [ ] Frontend development-server command (line 1714)
- [ ] Backend test command (line 1724)
- [ ] Frontend test command (line 1730)
- [ ] Example `/earthquakes` JSON response (line 1776)

## Architecture Review

- [ ] Produce one authoritative current system-context diagram
- [ ] Produce one deployment diagram and distinguish it from logical architecture
- [ ] Frontend architecture: React, Vite, MapLibre GL, deck.gl, Recharts, routing/navigation, state, components, and responsive behavior
- [ ] Backend architecture: Flask application, SQLAlchemy models, ingestion modules, validation, caching, and static frontend serving
- [ ] Database: SQLite schema, ownership, constraints, provenance, concurrency, migration, backup, and recovery
- [ ] Data flow: source acquisition → validation → raw storage → reconciliation → merged catalogue → APIs → Map/Insights
- [ ] External APIs: MPGV archive, IMO Quakes/Skjálftalísa, EPOS volcano/ShakeMap, EGDI/HIKE WFS, and map tile providers
- [ ] Public/internal API surface: methods, schemas, errors, authentication, limits, and base paths
- [ ] Scheduler: cadence, job order, locking, failure isolation, configuration, and lifecycle
- [ ] Reconciliation pipeline: thresholds, Haversine distance, candidate ranking, one-to-one matching, statuses, and repeatability
- [ ] ShakeMap pipeline: eligibility, lookup, thresholds, best-match selection, URL validation, audit cache, and UI flow
- [ ] Volcano refresh pipeline and safe replacement behavior
- [ ] Fault/fissure overlay fetch, filtering, styling, attribution, and in-memory caching
- [ ] Deployment architecture: Pluto hosting, Gunicorn/process model, reverse proxy/base URL, static assets, health check, HTTPS, logging, and scheduler ownership
- [ ] Security section: CSP/security headers, CORS policy, admin token, allowed ShakeMap hosts, request/row/date limits, rate limiting, secrets, and production settings
- [ ] Technologies used: remove superseded stack items and verify versions/roles from manifests and requirements
- [ ] Identify single points of failure, third-party dependencies, and graceful fallbacks
- [ ] Ensure diagrams, prose, tables, API appendix, and database appendix agree

## Algorithms and Quantitative Claims

- [ ] Verify Haversine formula, units, implementation, and tests
- [ ] Verify reconciliation maximum time difference (current documented value: 2 seconds)
- [ ] Verify reconciliation maximum distance (current documented value: 10 km)
- [ ] Verify reconciliation maximum magnitude difference (current documented value: 3.0)
- [ ] Verify strict/inclusive comparison operators for every threshold
- [ ] Verify unique-match and competing-candidate tie-breaking behavior
- [ ] Verify each Quakes API event can be consumed at most once
- [ ] Verify which source supplies location, depth, time, and magnitude for matched rows
- [ ] Verify public magnitude threshold (currently documented as M ≥ 3.0)
- [ ] Verify scheduler cadence (currently documented as every 3 minutes)
- [ ] Verify heatmap magnitude-band weights (currently documented as 0.20/0.30/0.45)
- [ ] Verify heatmap radius/intensity expressions across zoom levels
- [ ] Verify timeline and magnitude colour mappings and perceptual rationale
- [ ] Verify Insights bins, grouping, depth-quality policy, overflow handling, sorting, pagination, and statistics
- [ ] Reproduce all dataset counts, percentages, timing results, and audit metrics from recorded commands/data snapshots
- [ ] Add assumptions, boundary cases, complexity, and limitations for each important algorithm

## MPGV Monitor Feature Coverage

### Map and navigation

- [ ] Interactive MapLibre map with deck.gl earthquake markers
- [ ] Map, Satellite, Terrain, and Heatmap modes
- [ ] OpenFreeMap vector default and CARTO raster fallback when WebGL is unavailable
- [ ] Active-basemap and overlay attribution
- [ ] Default Iceland view/reset action
- [ ] Timeline colour mode
- [ ] Magnitude colour mode
- [ ] Magnitude filtering with current default minimum
- [ ] Time-window filtering
- [ ] Earthquake information card
- [ ] Eligible-event ShakeMap lookup
- [ ] Recent Selections (latest ten unique selections)
- [ ] Recent Selections hidden/closed in Heatmap mode
- [ ] State preservation when navigating between Map and Insights

### Layers and overlays

- [ ] Density-first MapLibre heatmap and hidden individual markers
- [ ] EPOS volcano layer and right-side volcano list/card
- [ ] EGDI/HIKE fault and fissure layer
- [ ] Solid-fault/dotted-fissure legend and onshore filtering
- [ ] Latitude/longitude grid with Iceland-focused spacing
- [ ] Overlay loading, errors, refresh, and caching behavior

### Insights page

- [ ] Dedicated responsive Insights route (`/mpgv/analysis` in deployment)
- [ ] Catalogue-bound date filter
- [ ] Minimum/maximum magnitude filters
- [ ] Minimum/maximum depth filters
- [ ] Reference-only versus explicitly included unverified depth policy
- [ ] Data-category filter
- [ ] Day/week/month/year grouping
- [ ] Dynamic `/insights/limits` requests and validation/clamping
- [ ] Summary cards
- [ ] Magnitude distribution chart
- [ ] Depth distribution chart
- [ ] Magnitude-versus-depth chart
- [ ] Average magnitude over time chart
- [ ] Data category over time chart
- [ ] Desktop hover tooltips and mobile touch tracking
- [ ] Time-chart brushes and visible-range labels
- [ ] Recent and strongest tables with sorting/pagination
- [ ] View on Map handoff
- [ ] Filtered CSV export
- [ ] Print-ready/browser PDF output
- [ ] Reference/unverified depth labelling in charts, tooltips, tables, and exports

### Application quality and operations

- [ ] About page/modal content
- [ ] Responsive desktop layout
- [ ] Mobile layout and touch interactions
- [ ] Accessibility status and limitations
- [ ] Multi-source ingestion and reconciliation
- [ ] Volcano metadata refresh
- [ ] Scheduler and manual maintenance routes
- [ ] API response caching and query/row/date limits
- [ ] Rate limiting and HTTP 429 behavior
- [ ] Production admin-token protection
- [ ] Health endpoint and deployment observability
- [ ] Automated backend and frontend tests

## Screenshots

> Included raster screenshots are listed individually even where several belong to one figure. Architecture/workflow images should be maintained as diagrams, not refreshed as UI screenshots.

Apply to every UI, website, API, data, and terminal screenshot:

- [ ] Replace with latest version if outdated, or label/date it as historical
- [ ] Crop consistently
- [ ] High resolution
- [ ] Matches current UI/source/schema/command
- [ ] Caption updated
- [ ] No private information, tokens, local usernames, or irrelevant browser/terminal chrome

Screenshot inventory used by the thesis:

- [ ] `Folium_Map_version.png` — historical Folium UI
- [ ] `Vite_terminal.png` — Vite terminal
- [ ] `hraun_vedur.png` — IMO/MPGV website
- [ ] `Year.png` — MPGV year source
- [ ] `Month.png` — MPGV month source
- [ ] `Data.png` — MPGV tabular data
- [ ] `S_Api.png` — Skjálftalísa API documentation
- [ ] `Quake_event.png` — API event response
- [ ] `Raw_Data.png` — historical raw data
- [ ] `APScheduler_working.png` — scheduler workflow (treat as diagram)
- [ ] `Webapp_front.png` — current main map UI
- [ ] `info_window.png` — current information card/UI
- [ ] `Deployment_Testing.png` — historical deployment response
- [ ] `deployed_pluto.png` — deployment terminal
- [ ] `CSV-based solution.png` — historical flowchart (treat as diagram)
- [ ] `Data_pipeline.png` — current data pipeline diagram
- [ ] `MPGV_sys_arc.png` — current system architecture diagram
- [ ] `Reconciliation workflow.png` — reconciliation diagram
- [ ] `ShakeMap validation workflow.png` — ShakeMap diagram
- [ ] `Frontend integration.png` — frontend architecture diagram
- [ ] `Frontend data flow.png` — frontend data-flow diagram

Missing current-UI screenshots to consider adding later:

- [ ] Insights desktop overview
- [ ] Insights mobile/responsive layout
- [ ] Each active basemap and Heatmap mode where visual comparison is useful
- [ ] Fault/fissure overlay and legend
- [ ] Volcano panel/card
- [ ] Recent Selections
- [ ] Filtered charts/tables and View on Map flow

## References, Cross-References, and Bibliography

### Citations and references

- [ ] Every citation resolves correctly
- [ ] Every figure/table/listing/appendix reference resolves correctly
- [ ] No broken or undefined references
- [ ] No duplicate labels
- [ ] Every numbered figure and table is mentioned in text
- [ ] Replace fragile hard-coded section/figure/table numbers with labels and references
- [ ] Verify citations are placed at the claim they support
- [ ] Add citations for technology behavior, external service capabilities, standards, algorithms, and comparative claims
- [ ] Prefer primary/official sources for APIs, libraries, standards, and product behavior
- [ ] Verify every URL and access date

### Bibliography audit (`references.bib`, 21 detected entries)

- [ ] `imo_quakes_48h`
- [ ] `earthquakes_is`
- [ ] `usgs_latest_map`
- [ ] `emsc_home`
- [ ] `emsc_map`
- [ ] `iris_ieb_app`
- [ ] `iris_ieb_help`
- [ ] `Netek2020`
- [ ] `MelgarejoHernandez2026`
- [ ] `Crameri2020`
- [ ] `Strollo2021`
- [ ] `ShakeMapManual`
- [ ] `Mazzei2022`
- [ ] `Netek2023`
- [ ] `WCAG21`
- [ ] `WAI_ARIA`
- [ ] `Brewer2003ColorBrewer`
- [ ] `GutenbergRichter1944`
- [ ] `Ester1996DBSCAN`
- [ ] `DeVries2018LSTM`
- [ ] `OSM_TileUsage`

For every entry above:

- [ ] Entry is cited or deliberately retained
- [ ] Citation key is clear and consistent
- [ ] Authors/editors, title, year, venue/publisher, volume/issue/pages, DOI/URL, and access date are complete where applicable
- [ ] Capitalization and Icelandic/diacritic characters render correctly
- [ ] Entry type and field formatting are correct

Bibliography completion:

- [ ] No duplicate references
- [ ] All URLs still valid
- [ ] Bibliography style consistent and institutionally acceptable
- [ ] Unused bibliography entries removed
- [ ] Missing current stack/API/security/accessibility sources added
- [ ] Bibliography ordering and final rendered entries reviewed

## Terminology and Consistency

- [ ] Use one canonical product name: “MPGV Monitor”
- [ ] Standardize MPGV capitalization (avoid “Mpgv”)
- [ ] Standardize “Skjálftalísa”, “IMO Quakes API”, and source-role terminology
- [ ] Clearly distinguish MPGV archive data, Quakes/Skjálftalísa data, EPOS data, and merged data
- [ ] Clearly distinguish Leaflet-era historical implementation from current MapLibre/deck.gl implementation
- [ ] Standardize frontend/backend, client-side/server-side, dataset/catalogue, basemap/base map, and ShakeMap spelling
- [ ] Define `v_only`, matched, reference depth, and unverified depth consistently
- [ ] Use consistent British or American English according to programme requirements
- [ ] Use consistent capitalization in headings, captions, and table cells
- [ ] Use consistent units, symbols, magnitude notation, date/time format, and decimal precision

## LaTeX Quality

- [ ] No compilation errors
- [ ] No compilation warnings requiring action
- [ ] No overfull or underfull boxes requiring action
- [ ] No undefined references
- [ ] No undefined citations
- [ ] No duplicate labels
- [ ] All floats placed acceptably
- [ ] All figures have captions and labels
- [ ] All tables have captions and labels
- [ ] Formal listings/algorithms have captions and labels
- [ ] Consistent formatting
- [ ] Consistent spacing
- [ ] Consistent capitalization
- [ ] Consistent heading hierarchy (including the unnumbered “Migration from Google Maps to Leaflet” subsubsection directly under Chapter 6)
- [ ] Consistent front-matter and appendix numbering
- [ ] URLs and code wrap without exceeding margins
- [ ] Special characters and Icelandic diacritics render correctly
- [ ] Images are not distorted by forced width/height combinations
- [ ] PDF metadata, bookmarks, hyperlinks, and accessibility tags reviewed
- [ ] Table of contents depth and entries correct
- [ ] List of figures generated and correct
- [ ] List of tables generated and correct
- [ ] List of listings generated if formal listings are adopted

## Final Submission Checklist

- [ ] Entire thesis read from start to finish
- [ ] All checklist items resolved or explicitly deferred with rationale
- [ ] All screenshots verified
- [ ] All figures referenced
- [ ] All tables referenced
- [ ] All listings/algorithms referenced
- [ ] Grammar review completed
- [ ] Spell check completed
- [ ] Technical terminology consistent
- [ ] Claims traceable to implementation, results, or citations
- [ ] Historical and current implementation descriptions clearly separated
- [ ] Reproducibility information complete
- [ ] PDF generated successfully from a clean checkout/submission package
- [ ] Table of contents correct
- [ ] List of figures correct
- [ ] List of tables correct
- [ ] Bibliography and hyperlinks manually spot-checked in the PDF
- [ ] Page numbering, margins, fonts, cover, declarations, and appendices meet University of Iceland requirements
- [ ] Final PDF reviewed on screen at multiple zoom levels
- [ ] Final PDF printed or print-previewed for layout issues
- [ ] Source archive contains every required `.tex`, `.bib`, image, and build file and no secrets/generated clutter
- [ ] Ready for supervisor review
- [ ] Supervisor feedback incorporated and rechecked
- [ ] Ready for final submission

## Revision Log

Use this table to keep the checklist maintainable as implementation and thesis revisions continue.

| Date | Area reviewed | Implementation commit/version | Thesis change summary | Reviewer | Remaining follow-up |
|---|---|---|---|---|---|
| 2026-07-22 | Initial structural inventory and checklist creation | Record before thesis revision begins | No thesis content changed | — | Complete all items above |
| 2026-07-22 | Chapter 1 -- Introduction | Current local implementation reviewed on 2026-07-22 | Rewrote Chapter 1 for the MapLibre/deck.gl and Insights implementation; corrected data thresholds and distinguished historical frontend stages | Codex | Add an authoritative geological citation, then complete the citation and chapter checks |
| 2026-07-22 | Abstract and Ágrip | Current local implementation reviewed on 2026-07-22 | Rewrote both summaries to align the research problem, reconciliation method, final architecture, implemented features, contribution, and limitations | Codex | Native Icelandic proofreading is still recommended before submission |
