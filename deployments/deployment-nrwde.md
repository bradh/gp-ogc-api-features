# Deployments in North-Rhine Westphalia

## 1. Data provider

Datasets from multiple data providers from North-Rhine Westphalia, Germany.

## 2. Thematic scope

The following datasets are available:

* Mining permits (Bergbauberechtigungen), data theme AM
* Fire brigade control centres (Feuerwehrleitstellen), data theme US
* Child care facilities (Kindertageseinrichtungen), data theme US
* Hospitals (Krankenhäuser), data theme US
* Various agricultural datasets relevant in the context of the [Integrated Administration and Control System (IACS)](https://ec.europa.eu/info/food-farming-fisheries/key-policies/common-agricultural-policy/financing-cap/financial-assurance/managing-payments_en), data themes LC/LU
* Low emission zones (Umweltzonen), data theme AM

In addition, extensions to the INSPIRE codelists are published in another API. This currently declares the item type as "features", but it is planned to migrate this in the future to OGC API Records.

## 3. Envisaged use

The APIs are in production since November 2020.

## 4. Requirements classes

From the draft Good Practice:

* Requirements class "INSPIRE-pre-defined-data-set-download-OAPIF"
* Requirements class "INSPIRE-multilinguality"
  * The implementation meets the requirements, but language selection only affects text generated by the API (html and link titles), not text in the data. All text in the data is always in German.
* Requirements class "INSPIRE-OAPIF-GeoJSON"
  * There are some differences to the "INSPIRE UML-to-GeoJSON encoding rule" that we will document.
* Requirements class "INSPIRE-bulk-download"
  * This requirements class is implemented for most APIs, typically linking to a CSV file and/or Shapefile archive.

The current development deployment supports the following OGC API requirements classes:

* OGC API - Features - Part 1: Core 1.0
  * Core (required by INSPIRE)
  * OpenAPI 3.0 (required by INSPIRE)
  * GeoJSON (required by INSPIRE)
  * HTML
* OGC API - Features - Part 2: Coordinate Reference Systems by Reference Release Candidate (in approval vote)
  * Coordinate Reference Systems by Reference
* OGC API - Features - Part 3: Filtering and the Common Query Language (CQL) DRAFT
  * Filter
  * Features Filter
  * Simple CQL
  * CQL Text encoding
  * CQL JSON encoding
* OGC API - Tiles - Part 1: Core DRAFT
  * Tile Set
  * Tile Sets
  * Dataset Tile Sets
  * Geodata Resource Selection
  * Geodata Resource Tile Sets
* OGC API - Tiles - Part 2: Tile Matrix Sets DRAFT
  * Tile Matrix Sets
* OGC API - Styles DRAFT
  * Core
  * HTML
  * Mapbox Styles
  * Queryables
  * Style Info
  * Resources (only, if the style needs symbols)

## 5. Server-side technology

The deployment uses XtraServer Web API from interactive instruments GmbH, which integrates [ldproxy](https://github.com/interactive-instruments/ldproxy). ldproxy is available under the Mozilla Public License 2.0.

## 6. Endpoints and client applications

Landing page of the deployment: https://ogc-api.nrw.de/

APIs:

* Mining permits (Bergbauberechtigungen): https://ogc-api.nrw.de/inspire-am-bergbauberechtigungen/v1
* Fire brigade control centres (Feuerwehrleitstellen): https://ogc-api.nrw.de/inspire-us-feuerwehr/v1
* Child care facilities (Kindertageseinrichtungen): https://ogc-api.nrw.de/inspire-us-kindergarten/v1
* Hospitals (Krankenhäuser): https://ogc-api.nrw.de/inspire-us-krankenhaus/v1
* Agricultural datasets:
  * https://ogc-api.nrw.de/inspire-lc-bena/v1
  * https://ogc-api.nrw.de/inspire-lu-ble/v1
  * https://ogc-api.nrw.de/inspire-lu-blehist/v1
  * https://ogc-api.nrw.de/inspire-lc-ccwas/v1
  * https://ogc-api.nrw.de/inspire-lc-ccwind/v1
  * https://ogc-api.nrw.de/inspire-lc-dgl/v1
  * https://ogc-api.nrw.de/inspire-lc-fb/v1
  * https://ogc-api.nrw.de/inspire-lc-le/v1
  * https://ogc-api.nrw.de/inspire-lc-oevf/v1
  * https://ogc-api.nrw.de/inspire-lc-topup/v1
  * https://ogc-api.nrw.de/inspire-lu-ts/v1
  * https://ogc-api.nrw.de/inspire-lu-tshist/v1
  * https://ogc-api.nrw.de/inspire-lc-udgl/v1
  * https://ogc-api.nrw.de/inspire-lc-umwe/v1
  * https://ogc-api.nrw.de/inspire-lc-zfga/v1
  * https://ogc-api.nrw.de/inspire-lc-zfum/v1
* Low emission zones (Luftreinhalteplan): https://ogc-api.nrw.de/inspire-am-luftreinhaltung/v1
* INSPIRE-Codelist extensions: https://ogc-api.nrw.de/codelist/v1

## 7. Issues

All issues with respect to the requirements in the Good Practice document were resolved as part of the work on the Good Practice specification.

It would be good, if other INSPIRE service types could also be provided using current Web APIs. For example, see the issue on [INSPIRE View Services](https://github.com/INSPIRE-MIF/gp-ogc-api-features/issues/37).
