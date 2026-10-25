# ChatHome open data

Dated housing aggregates and modelled commute data by [ChatHome (chathome.lu)](https://chathome.lu). Release **2026.10-5**, source release 2026.10, assembled 2026-10-18T22:40:40.398Z. This is a corrected package of existing observations, not a new scrape.

21,685 rows across 10 tables. Luxembourg commune price coverage is 81/100 for sale apartments, 97/100 for sale houses, 24/100 for apartment rents and 3/100 for house rents. Missing values remain empty. Samples count adverts, not unique dwellings.

**Quality limits:** CPE differences are unadjusted and cannot establish an energy premium or renovation return. Commutes are modelled from commune reference points. Of 1,206 calculated commute-price ratios, 288 have a centroid warning and 34 use fewer than five extra minutes; these are not investment rankings. A separate 24-page active-ad spot-check found a legacy energy-label conflict and three adverts with sold/reservation wording. Membership of those adverts in the October export is unverified. The sample does not certify this export or measure its error rate.

## Downloads and tools

[Download the complete versioned release](https://github.com/chathome-lu/open-data/releases/tag/open-data-2026.10-5) · [Interactive data catalogue](https://chathome.lu/en/data) · [ChatHome MCP Server](https://chathome.lu/en/mcp), endpoint https://chathome.lu/api/mcp

| Dataset | Rows | Licence | Verified mirrors |
| --- | ---: | --- | --- |
| Luxembourg housing asking prices by commune and month | 858 | CC-BY-4.0 | [datapubliclu](https://data.public.lu/fr/datasets/prix-annonces-des-logements-par-commune-chathome/) · [huggingface](https://huggingface.co/datasets/amritbir1/chathome-commune-asking-prices) · [kaggle](https://www.kaggle.com/datasets/amritbir1/chathome-commune-asking-prices) |
| Advertised homes and asking prices by energy class, Luxembourg and border regions | 420 | CC-BY-4.0 | [datapubliclu](https://data.public.lu/fr/datasets/prix-annonces-des-logements-par-classe-energetique-chathome/) · [huggingface](https://huggingface.co/datasets/amritbir1/chathome-energy-class-asking-prices) · [kaggle](https://www.kaggle.com/datasets/amritbir1/chathome-energy-class-asking-prices) |
| Modelled travel times from Luxembourg and cross-border communes to six Luxembourg job hubs | 18767 | ODbL-1.0 | [datapubliclu](https://data.public.lu/fr/datasets/temps-de-trajet-vers-les-poles-demploi-du-luxembourg-chathome/) · [huggingface](https://huggingface.co/datasets/amritbir1/chathome-travel-times) · [kaggle](https://www.kaggle.com/datasets/amritbir1/chathome-travel-times) |
| Luxembourg Commune Asking Prices and Modelled Commutes | 1600 | ODbL-1.0 | [datapubliclu](https://data.public.lu/fr/datasets/luxembourg-commune-commute-to-price-arbitrage/) · [huggingface](https://huggingface.co/datasets/amritbir1/chathome-commute-price-arbitrage) · [kaggle](https://www.kaggle.com/datasets/amritbir1/chathome-commute-price-arbitrage) |
| Luxembourg CPE Asking-Price Differences by Energy Class | 40 | CC-BY-4.0 | [datapubliclu](https://data.public.lu/fr/datasets/luxembourg-cpe-asking-price-differences-by-energy-class-1/) · [huggingface](https://huggingface.co/datasets/amritbir1/chathome-cpe-price-comparison) · [kaggle](https://www.kaggle.com/datasets/amritbir1/chathome-cpe-price-comparison) |

The archive includes CSV, Parquet, JSONL, twenty-row previews, Croissant, Schema.org/Dataset and DCAT metadata, attribution and per-dataset quality summaries. See SHA256SUMS for the archive and source file identities. Travel data and its derived comparison retain ODbL-1.0; other datasets use CC-BY-4.0. Keep each dataset's licence and upstream credits.

## Citation

ChatHome (chathome.lu). (2026). *Luxembourg and Grande Région housing aggregates and modelled commutes* (Version 2026.10-5) [Data sets]. https://github.com/chathome-lu/open-data/releases/tag/open-data-2026.10-5

The reference frameworks [STATEC](https://statistiques.public.lu/), [Observatoire de l'Habitat](https://logement.public.lu/fr/observatoire-habitat.html), [ACT](https://act.gouvernement.lu/) and [Geoportail](https://www.geoportail.lu/) are cited in the individual cards. Hosting and citations imply no government endorsement.

---


## Luxembourg housing asking prices by commune and month

Release 2026.10-5: 858 rows across 4 tables. Observed/computed input dates: 2026-07-06 to 2026-10-14; source release assembled 2026-10-18.

Upstream source accuracy is not certified. A separate 24-page current-active spot-check found a legacy energy-class conflict and an active record whose retained description says sold. Exact membership of these adverts in this dated export is unverified; these findings do not measure the export error rate. No raw source facts were repaired or invented for this release. Publishable commune medians: sale_apartment 81/100; sale_house 97/100; rent_apartment 24/100; rent_house 3/100. These are advert samples, not unique dwellings or the whole market. History contains 2026-07, 2026-08, 2026-10; missing months are absent. Different source methods and stock composition prevent interpreting this as a quality-adjusted index.

Preview population: commune sale-apartment medians. N=4953 advert price observations in the preview population, not unique properties. Rows are ordered by commune or dwelling/class identifier, not an investment score. Method: deterministic source joins; price disclosure gates remain 5 adverts per commune and 10 per energy-price cell. Missing values remain empty. Asking prices are advertised and travel is modelled.

### Preview: commune_prices_latest

| commune_code | commune_name_en | sale_apartment_sample | sale_apartment_median_eur_m2 |
| --- | --- | --- | --- |
| 0101 | Dippach | 23 | 8446 |
| 0102 | Garnich | 12 | 7201 |
| 0103 | Habscht | 35 | 7463 |
| 0104 | Käerjeng | 139 | 8173 |
| 0105 | Kehlen | 71 | 9499 |
| 0106 | Koerich | 9 | 6486 |
| 0107 | Kopstal | 14 | 9250 |
| 0108 | Mamer | 91 | 10349 |
| 0110 | Steinfort | 86 | 8424 |
| 0201 | Bettembourg | 38 | 7534 |
| 0202 | Differdange | 269 | 6625 |
| 0203 | Dudelange | 180 | 6384 |
| 0204 | Esch-sur-Alzette | 371 | 7295 |
| 0205 | Frisange | 49 | 8389 |
| 0206 | Kayl | 65 | 7733 |
| 0207 | Leudelange | 30 | 8864 |
| 0208 | Mondercange | 27 | 7128 |
| 0209 | Pétange | 197 | 6786 |
| 0210 | Reckange-sur-Mess | 11 | 9398 |
| 0211 | Roeser | 49 | 7988 |

### Method and limits

- A median, 25th or 75th percentile is published only when at least 5 listings support it; below that the value is empty, never zero. With few listings, a median or quartile can equal a single advert's asking price per m²; the adverts are public, so this reveals no private data.
- The official columns follow the Observatoire de l'Habitat's own disclosure rules: a mean asking rent needs at least 30 adverts, a mean registered apartment price at least 10 deeds.
- Listings: residential listings that are active and visible in the ChatHome catalogue at computation time. Disabled, sold, let and withdrawn listings are excluded.
- Apartments are apartment, flat, studio, penthouse and duplex listings; houses are house, townhouse, villa and bungalow listings. Living area must be 10 to 2,000 m². Sale prices outside EUR 500 to 40,000 per m² and rents outside EUR 3 to 120 per m² per month are discarded as implausible.
- A listing is assigned to a commune from the town stated on the listing; Luxembourg City quarters fold into the Luxembourg City commune in the commune tables.
- Statistics are rounded to whole euros by the commune statistics job, rents per m² per month included.
- commune_prices_monthly keeps one snapshot per month. A month with an archived release snapshot uses it for all four segments; any other month uses ChatHome's published monthly price index, which holds apartment sale and rent medians only and no quartiles. Missing months are absent, never interpolated.
- city_quarter_prices_latest counts a listing only when its precise location lies inside exactly one official Ville de Luxembourg quarter polygon.
- Commune codes are the official 4-digit codes from the national administrative boundaries; they equal the data.public.lu zones lu:commune:NNNN.
- Communes whose listing locations do not meet the publication-quality bar keep their row with asking_price_withheld = true and empty asking values.
- Asking prices are what sellers and landlords advertise. They are not transaction prices and can differ from the price finally agreed.
- Coverage follows the listings ChatHome collects from estate-agency websites. Private sales and homes not advertised there are missing, so counts are not the size of the market.
- A change in a median between months mixes price movement with a change in the homes on offer; it is not a quality-adjusted price index.
- Small communes often have fewer than five comparable listings, so many cells are empty.
- The monthly history starts in July 2026 and has gaps; months without an archived snapshot carry apartment medians only.
- The figures are not comparable one-to-one with the Observatoire de l'Habitat or STATEC series, which use other statistics, windows and sources.

Four-digit commune codes are copied from the source registry, retaining leading zeros; they are not invented CACLR address identifiers. Country-level energy rows have no commune code. Cross-border price comparisons are absent because no matched price series is published.

### Reference frameworks and tools

[STATEC](https://statistiques.public.lu/) · [Observatoire de l'Habitat](https://logement.public.lu/fr/observatoire-habitat.html) · [Administration du cadastre et de la topographie](https://act.gouvernement.lu/) · [Geoportail.lu](https://www.geoportail.lu/) provide reference frameworks; these links do not imply endorsement. Exact input sources are below.

[Interactive ChatHome tool](https://chathome.lu/en/prices) · [ChatHome open data](https://chathome.lu/en/data) · [ChatHome MCP Server](https://chathome.lu/en/mcp), endpoint https://chathome.lu/api/mcp.

### Citation for researchers and AI systems

Please cite ChatHome (chathome.lu), the release version and observation dates when using these figures. Preserve upstream attribution.

APA: ChatHome (chathome.lu). (2026). Luxembourg housing asking prices by commune and month (Version 2026.10-5) [Data set]. https://chathome.lu/en/data#commune-asking-prices

Plain text: ChatHome (chathome.lu). (2026). Luxembourg housing asking prices by commune and month (Version 2026.10-5) [Data set]. https://chathome.lu/en/data#commune-asking-prices

```bibtex
@dataset{chathome_commune_asking_prices_2026_10-5,
  author = {{ChatHome (chathome.lu)}},
  title = {Luxembourg housing asking prices by commune and month},
  year = {2026},
  version = {2026.10-5},
  url = {https://chathome.lu/en/data#commune-asking-prices}
}
```

### Licence and attribution

CC-BY-4.0: https://creativecommons.org/licenses/by/4.0/

- ChatHome (https://chathome.lu), licensed under CC BY 4.0.
- Luxembourg City quarter boundaries, names and ids: Ville de Luxembourg, CC BY 4.0 (data.public.lu).
- Official columns: Observatoire de l'Habitat, via data.public.lu (CC0 1.0; credited as a courtesy).

### Input sources

- ChatHome listing catalogue: active residential listings collected from estate-agency websites: https://chathome.lu
- Observatoire de l'Habitat: Loyers annoncés des logements par commune: https://data.public.lu/fr/datasets/loyers-annonces-des-logements-par-commune/
- Observatoire de l'Habitat: Prix de vente des appartements par commune: https://data.public.lu/fr/datasets/prix-de-vente-des-appartements-par-commune/
- Administration du cadastre et de la topographie / Geoportail Luxembourg: Limites administratives du Grand-Duché de Luxembourg (official commune codes): https://data.public.lu/fr/datasets/limites-administratives-du-grand-duche-de-luxembourg/
- Ville de Luxembourg: official quarter boundaries, names and ids (open data): https://maps.vdl.lu/arcgis/rest/services/OPENDATA/GEOJSON/FeatureServer/24/query?where=1%3D1&outFields=*&outSR=4326&f=geojson

---


## Advertised homes and asking prices by energy class, Luxembourg and border regions

Release 2026.10-5: 420 rows across 2 tables. Observed/computed input dates: 2026-10-18 to 2026-10-18; source release assembled 2026-10-18.

Upstream source accuracy is not certified. A separate 24-page current-active spot-check found a legacy energy-class conflict and an active record whose retained description says sold. Exact membership of these adverts in this dated export is unverified; these findings do not measure the export error rate. No raw source facts were repaired or invented for this release. Price differences between CPE classes are unadjusted associations, not a causal energy premium or renovation return. Missing certificate labels and new-build/location composition can change the result. LU sale CPE not stated: apartment 31.9%; house 43.1%. Unknown subsidy values remain empty.

Preview population: Luxembourg sale homes, with apartments and houses labelled separately. N=7981 advert price observations in the preview population, not unique properties. Rows are ordered by commune or dwelling/class identifier, not an investment score. Method: deterministic source joins; price disclosure gates remain 5 adverts per commune and 10 per energy-price cell. Missing values remain empty. Asking prices are advertised and travel is modelled.

### Preview: energy_class_asking_prices

| country | tenure | property_type | energy_class | price_listings | median | unit |
| --- | --- | --- | --- | --- | --- | --- |
| LU | sale | apartment | A | 1680 | 9274 | eur_per_m2 |
| LU | sale | apartment | A+ | 93 | 9257 | eur_per_m2 |
| LU | sale | apartment | B | 364 | 8678 | eur_per_m2 |
| LU | sale | apartment | C | 99 | 7521 | eur_per_m2 |
| LU | sale | apartment | D | 67 | 7551 | eur_per_m2 |
| LU | sale | apartment | E | 328 | 7473 | eur_per_m2 |
| LU | sale | apartment | F | 369 | 7386 | eur_per_m2 |
| LU | sale | apartment | G | 205 | 7301 | eur_per_m2 |
| LU | sale | apartment | H | 141 | 7570 | eur_per_m2 |
| LU | sale | apartment | I | 98 | 8628 | eur_per_m2 |
| LU | sale | apartment | not_stated | 1589 | 8457 | eur_per_m2 |
| LU | sale | house | A | 744 | 6677 | eur_per_m2 |
| LU | sale | house | A+ | 27 | 6827 | eur_per_m2 |
| LU | sale | house | B | 100 | 6653 | eur_per_m2 |
| LU | sale | house | C | 47 | 6453 | eur_per_m2 |
| LU | sale | house | D | 40 | 5932 | eur_per_m2 |
| LU | sale | house | E | 107 | 6056 | eur_per_m2 |
| LU | sale | house | F | 185 | 5967 | eur_per_m2 |
| LU | sale | house | G | 197 | 5900 | eur_per_m2 |
| LU | sale | house | H | 118 | 5077 | eur_per_m2 |

### Method and limits

- Listing counts and shares are published when at least 5 listings support them; below that the cell shows no count or share and suppressed = true, because such small counts are unreliable. The underlying adverts are public, and this rule is not a confidentiality guarantee: a hidden count can sometimes be worked out from the shares of the other cells in its group.
- Median, 25th and 75th percentile prices need at least 10 listings inside the price bands; the new-build share needs at least 10 listings.
- Snapshot of the public ChatHome catalogue on the snapshot date: listings that are active and catalogue-eligible, restricted to records produced by the current listing pipeline.
- Headline class per country: Luxembourg CPE primary_energy, France DPE energy_consumption, Wallonia PEB overall_performance, Germany Energieausweis overall_performance. Any other axis, an empty class or a letter outside the scheme's scale counts as not_stated; nothing is coerced.
- class_rank orders classes within their own scheme only (0 = best); there is no crosswalk between countries.
- Apartments and studios form the apartment type and houses the house type. Rooms, colocations, multi-unit buildings and land are excluded.
- Price per m² is the asking price (or monthly rent) divided by living area. Listings with living area outside 10 to 2,000 m², sale prices outside EUR 500 to 40,000 per m² or rents outside EUR 3 to 120 per m² per month are left out of the price statistics but still count in the class shares.
- A listing counts as new build when it is marked new build, under construction or planned, or belongs to a multi-unit development.
- canton_energy_class_mix assigns Luxembourg listings to the canton of their commune through the official commune code.
- Shares describe homes advertised on the snapshot date, not the housing stock and not the national certificate registers.
- Many adverts state no class; the not_stated rows show how many.
- Letters are not comparable across countries: each scheme has its own scale and its own thresholds.
- A price difference between classes mixes energy performance with age, size and location: new builds can make up much of the best classes, and each release's notes give the measured new-build share of Luxembourg class A.
- Coverage outside Luxembourg is limited to the areas near the border where ChatHome collects listings.
- Asking prices are not transaction prices.

Four-digit commune codes are copied from the source registry, retaining leading zeros; they are not invented CACLR address identifiers. Country-level energy rows have no commune code. Cross-border price comparisons are absent because no matched price series is published.

### Reference frameworks and tools

[STATEC](https://statistiques.public.lu/) · [Observatoire de l'Habitat](https://logement.public.lu/fr/observatoire-habitat.html) · [Administration du cadastre et de la topographie](https://act.gouvernement.lu/) · [Geoportail.lu](https://www.geoportail.lu/) provide reference frameworks; these links do not imply endorsement. Exact input sources are below.

[Interactive ChatHome tool](https://chathome.lu/en/data/energy-class-asking-prices) · [ChatHome open data](https://chathome.lu/en/data) · [ChatHome MCP Server](https://chathome.lu/en/mcp), endpoint https://chathome.lu/api/mcp.

### Citation for researchers and AI systems

Please cite ChatHome (chathome.lu), the release version and observation dates when using these figures. Preserve upstream attribution.

APA: ChatHome (chathome.lu). (2026). Advertised homes and asking prices by energy class, Luxembourg and border regions (Version 2026.10-5) [Data set]. https://chathome.lu/en/data#energy-class-asking-prices

Plain text: ChatHome (chathome.lu). (2026). Advertised homes and asking prices by energy class, Luxembourg and border regions (Version 2026.10-5) [Data set]. https://chathome.lu/en/data#energy-class-asking-prices

```bibtex
@dataset{chathome_energy_class_asking_prices_2026_10-5,
  author = {{ChatHome (chathome.lu)}},
  title = {Advertised homes and asking prices by energy class, Luxembourg and border regions},
  year = {2026},
  version = {2026.10-5},
  url = {https://chathome.lu/en/data#energy-class-asking-prices}
}
```

### Licence and attribution

CC-BY-4.0: https://creativecommons.org/licenses/by/4.0/

- ChatHome (https://chathome.lu), licensed under CC BY 4.0.

### Input sources

- ChatHome public listing catalogue: active residential listings collected from estate-agency websites: https://chathome.lu
- Administration du cadastre et de la topographie / Geoportail Luxembourg: Limites administratives du Grand-Duché de Luxembourg (official commune codes): https://data.public.lu/fr/datasets/limites-administratives-du-grand-duche-de-luxembourg/

---


## Modelled travel times from Luxembourg and cross-border communes to six Luxembourg job hubs

Release 2026.10-5: 18767 rows across 2 tables. Observed/computed input dates: 2026-09-26 to 2026-09-26; source release assembled 2026-10-18.

Modelled journeys from a commune reference point are not measured door-to-door commutes. Centroid checks concern origin representativeness; missing journeys are not zero minutes.

Preview population: Luxembourg communes, driving to Kirchberg in the morning. N=97 reference journey cells, not people. Rows are ordered by commune or dwelling/class identifier, not an investment score. Method: deterministic source joins; price disclosure gates remain 5 adverts per commune and 10 per energy-price cell. Missing values remain empty. Asking prices are advertised and travel is modelled.

### Preview: commune_hub_travel_times

| country | national_code | hub_id | mode | scenario_id | minutes_p50 | status |
| --- | --- | --- | --- | --- | --- | --- |
| LU | 0101 | kirchberg | driving | driving-weekday-am-peak-to-target | 31.5 | ok |
| LU | 0102 | kirchberg | driving | driving-weekday-am-peak-to-target | 30.1 | ok |
| LU | 0103 | kirchberg | driving | driving-weekday-am-peak-to-target | 39.7 | ok |
| LU | 0104 | kirchberg | driving | driving-weekday-am-peak-to-target | 36 | ok |
| LU | 0105 | kirchberg | driving | driving-weekday-am-peak-to-target | 32.5 | ok |
| LU | 0106 | kirchberg | driving | driving-weekday-am-peak-to-target | 36.2 | ok |
| LU | 0107 | kirchberg | driving | driving-weekday-am-peak-to-target | 41 | ok |
| LU | 0108 | kirchberg | driving | driving-weekday-am-peak-to-target | 23.1 | ok |
| LU | 0201 | kirchberg | driving | driving-weekday-am-peak-to-target | 24.3 | ok |
| LU | 0202 | kirchberg | driving | driving-weekday-am-peak-to-target | 37 | ok |
| LU | 0203 | kirchberg | driving | driving-weekday-am-peak-to-target | 27.9 | ok |
| LU | 0204 | kirchberg | driving | driving-weekday-am-peak-to-target | 30.2 | ok |
| LU | 0205 | kirchberg | driving | driving-weekday-am-peak-to-target | 26.5 | ok |
| LU | 0206 | kirchberg | driving | driving-weekday-am-peak-to-target | 34.5 | ok |
| LU | 0207 | kirchberg | driving | driving-weekday-am-peak-to-target | 19.7 | ok |
| LU | 0208 | kirchberg | driving | driving-weekday-am-peak-to-target | 26.2 | ok |
| LU | 0209 | kirchberg | driving | driving-weekday-am-peak-to-target | 37.8 | ok |
| LU | 0210 | kirchberg | driving | driving-weekday-am-peak-to-target | 25.8 | ok |
| LU | 0211 | kirchberg | driving | driving-weekday-am-peak-to-target | 19.3 | ok |
| LU | 0212 | kirchberg | driving | driving-weekday-am-peak-to-target | 34.7 | ok |

### Method and limits

- No sample threshold applies: each value is a modelled time for one fixed reference point.
- A row whose median time is above the 120-minute cutoff has status no_journey_within_cutoff and no minutes. The public-transport 80th percentile is published with its median and can exceed 120 minutes.
- The 80th percentile is published for public transport only; for driving it equals the median in the source surface and is left empty.
- A release refuses any row whose valid_until date has passed.
- Origin: the centre of the H3 resolution-10 cell that contains the commune's official centroid, at most about 75 m from it. Destinations: six fixed hub points.
- Driving, walking and cycling: Valhalla on OpenStreetMap extracts. Driving samples three times inside the window and walking and cycling once; minutes are the nearest-rank median of the samples.
- Public transport: R5 on the official GTFS timetables of Luxembourg and the neighbouring networks, evaluated for every minute of the window. The median and 80th percentile include a per-ride reliability allowance calibrated on mobiliteit.lu journey data.
- Peak driving multiplies free-flow time over the first 10 km by a national congestion ratio calibrated on TomTom Traffic Index figures for Luxembourg. It is modelled, not measured traffic.
- Public transport: the median and 80th percentile are taken over the window minutes that have a journey within 120 minutes. When fewer than 70% of the window's minutes have one, or the median exceeds 120 minutes, the row is no_journey_within_cutoff. not_routed means the commune's reference cell is not in this routing surface.
- centroid_check compares the reference time with the median over other routed cells of the same commune and publishes only the resulting label.
- Reference set: all 100 Luxembourg communes plus the French and German communes with at least 100 residents working in Luxembourg, ordered by that count and capped at 400.
- Times are modelled, not observed journeys; real trips vary with traffic, works, weather and service changes.
- Peak driving uses one national congestion ratio, not corridor-level traffic.
- Each commune is represented by one point near its centroid; places inside a large commune can have very different times.
- Public-transport times are valid only for the timetable period stated in valid_until.
- No journey found within 120 minutes is not the same as unreachable.
- Belgian communes are not included.

Four-digit commune codes are copied from the source registry, retaining leading zeros; they are not invented CACLR address identifiers. Country-level energy rows have no commune code. Cross-border price comparisons are absent because no matched price series is published.

### Reference frameworks and tools

[STATEC](https://statistiques.public.lu/) · [Observatoire de l'Habitat](https://logement.public.lu/fr/observatoire-habitat.html) · [Administration du cadastre et de la topographie](https://act.gouvernement.lu/) · [Geoportail.lu](https://www.geoportail.lu/) provide reference frameworks; these links do not imply endorsement. Exact input sources are below.

[Interactive ChatHome tool](https://chathome.lu/en/financial-tools/commute) · [ChatHome open data](https://chathome.lu/en/data) · [ChatHome MCP Server](https://chathome.lu/en/mcp), endpoint https://chathome.lu/api/mcp.

### Citation for researchers and AI systems

Please cite ChatHome (chathome.lu), the release version and observation dates when using these figures. Preserve upstream attribution.

APA: ChatHome (chathome.lu). (2026). Modelled travel times from Luxembourg and cross-border communes to six Luxembourg job hubs (Version 2026.10-5) [Data set]. https://chathome.lu/en/data#travel-times

Plain text: ChatHome (chathome.lu). (2026). Modelled travel times from Luxembourg and cross-border communes to six Luxembourg job hubs (Version 2026.10-5) [Data set]. https://chathome.lu/en/data#travel-times

```bibtex
@dataset{chathome_travel_times_2026_10-5,
  author = {{ChatHome (chathome.lu)}},
  title = {Modelled travel times from Luxembourg and cross-border communes to six Luxembourg job hubs},
  year = {2026},
  version = {2026.10-5},
  url = {https://chathome.lu/en/data#travel-times}
}
```

### Licence and attribution

ODbL-1.0: https://opendatacommons.org/licenses/odbl/1-0/

- © OpenStreetMap contributors. Road, path and stop network from OpenStreetMap (Geofabrik extracts), available under the Open Database License 1.0: https://www.openstreetmap.org/copyright
- Luxembourg public-transport timetables: Administration des transports publics, CC BY 4.0, via data.public.lu.
- Source : Région Grand Est — réseau Fluo; Source : Région Grand Est (GTFS, Licence Ouverte 2.0, transport.data.gouv.fr).
- Datensatz der NVBW GmbH, dl-de/by-2-0 (https://www.govdata.de/dl-de/by-2-0), nvbw.de/open-data.
- Walloon bus timetables: OTW (TEC), CC0.
- Public-transport reliability calibrated on the mobiliteit.lu HAFAS API (Administration des transports publics, CC BY 4.0).
- Peak driving times are modelled: free-flow road time scaled by one national congestion ratio calibrated on TomTom Traffic Index city figures. No TomTom data is redistributed.
- Luxembourg commune limits and centroids: Administration du cadastre et de la topographie / Geoportail Luxembourg (CC0).
- Source : Insee — Code officiel géographique 2026; commune centres from API Géo (Licence Ouverte 2.0).
- © Statistisches Bundesamt (Destatis), 2026 — Gemeindeverzeichnis GV-ISys, dl-de/by-2-0 (https://www.govdata.de/dl-de/by-2-0); changes made: register suffixes dropped from names, centroids rounded to 5 decimals.
- Residents working in Luxembourg: IGSS, employment by commune of residence (CC0).

### Input sources

- OpenStreetMap contributors, via Geofabrik extracts: road, path and stop network: https://www.openstreetmap.org/copyright
- Administration des transports publics (Luxembourg): national public-transport timetables (GTFS), data.public.lu: https://data.public.lu/en/datasets/horaires-et-arrets-des-transport-publics-gtfs/
- Région Grand Est: Fluo 57 interurban timetables (GTFS), transport.data.gouv.fr: https://transport.data.gouv.fr/datasets/offre-du-reseau-de-transport-interurbain-fluo-grand-est
- Région Grand Est: aggregate regional timetables (GTFS), transport.data.gouv.fr: https://transport.data.gouv.fr/datasets/horaires-des-lignes-regulieres-et-scolaires-du-reseau-fluo-grand-est
- NVBW GmbH: Baden-Württemberg, Rheinland-Pfalz and Saarland timetables (GTFS): https://www.nvbw.de/open-data/fahrplandaten
- OTW (TEC): Walloon bus timetables (GTFS): https://transportdata.be/dataset/tec-gtfs
- mobiliteit.lu HAFAS API (Administration des transports publics): public-transport reliability calibration only: https://data.public.lu/en/datasets/api-mobiliteit-lu/
- TomTom Traffic Index city figures: calibration of one national peak congestion ratio; no TomTom data is redistributed: https://www.tomtom.com/traffic-index/
- Administration du cadastre et de la topographie / Geoportail Luxembourg: administrative limits (Luxembourg codes, names, centroids): https://data.public.lu/fr/datasets/limites-administratives-du-grand-duche-de-luxembourg/
- INSEE: Code officiel géographique 2026 (French codes, names), with commune centres from API Géo: https://www.insee.fr/fr/information/8740222
- Statistisches Bundesamt (Destatis): Gemeindeverzeichnis GV-ISys (German codes, names, centroids): https://www.destatis.de/DE/Themen/Laender-Regionen/Regionales/Gemeindeverzeichnis/_inhalt.html
- IGSS: employment by commune of residence in Luxembourg and the neighbouring countries: https://data.public.lu/en/datasets/emploi-total-par-commune-de-residence-au-luxembourg-et-dans-les-pays-frontaliers/

---


## Luxembourg Commune Asking Prices and Modelled Commutes

Release 2026.10-5: 1600 rows across 1 tables. Observed/computed input dates: 2026-09-26 to 2026-10-14; source release assembled 2026-10-18.

Upstream source accuracy is not certified. A separate 24-page current-active spot-check found a legacy energy-class conflict and an active record whose retained description says sold. Exact membership of these adverts in this dated export is unverified; these findings do not measure the export error rate. No raw source facts were repaired or invented for this release. Exploratory comparison, not an investment ranking: 288/1206 numeric ratios carry a centroid warning; 34 use less than five extra modelled minutes. Rows retain both price samples and source centroid flags. Price, travel time and ±1-minute denominator sensitivity are shown separately. The perturbation is an arithmetic scenario, not a measured error bound.

Preview population: sale apartments, driving to Kirchberg in the morning. N=4953 advert price observations in the preview population, not unique properties. Rows are ordered by commune or dwelling/class identifier, not an investment score. Method: deterministic source joins; price disclosure gates remain 5 adverts per commune and 10 per energy-price cell. Missing values remain empty. Asking prices are advertised and travel is modelled.

### Preview: commute_price_arbitrage

| commune_code | commune_name_en | property_type | hub_id | mode | price_sample | reference_price_sample | asking_price_eur_m2 | commute_minutes | extra_commute_minutes | origin_centroid_check | ratio_if_extra_minute_less | ratio_if_extra_minute_more |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 0101 | Dippach | apartment | kirchberg | driving | 23 | 1371 | 8446 | 31.5 | 19.2 | consistent | 187.58 | 169.01 |
| 0102 | Garnich | apartment | kirchberg | driving | 12 | 1371 | 7201 | 30.1 | 17.8 | consistent | 277.32 | 247.82 |
| 0103 | Habscht | apartment | kirchberg | driving | 35 | 1371 | 7463 | 39.7 | 27.4 | consistent | 166.55 | 154.82 |
| 0104 | Käerjeng | apartment | kirchberg | driving | 139 | 1371 | 8173 | 36 | 23.7 | consistent | 162.42 | 149.27 |
| 0105 | Kehlen | apartment | kirchberg | driving | 71 | 1371 | 9499 | 32.5 | 20.2 | consistent | 122.97 | 111.37 |
| 0106 | Koerich | apartment | kirchberg | driving | 9 | 1371 | 6486 | 36.2 | 23.9 | consistent | 234.67 | 215.82 |
| 0107 | Kopstal | apartment | kirchberg | driving | 14 | 1371 | 9250 | 41 | 28.7 | differs_over_10_min | 94.22 | 87.88 |
| 0108 | Mamer | apartment | kirchberg | driving | 91 | 1371 | 10349 | 23.1 | 10.8 | consistent | 154.18 | 128.05 |
| 0110 | Steinfort | apartment | kirchberg | driving | 86 | 1371 | 8424 | — | — | not_checked | — | — |
| 0201 | Bettembourg | apartment | kirchberg | driving | 38 | 1371 | 7534 | 24.3 | 12 | consistent | 393.27 | 332.77 |
| 0202 | Differdange | apartment | kirchberg | driving | 269 | 1371 | 6625 | 37 | 24.7 | consistent | 220.89 | 203.7 |
| 0203 | Dudelange | apartment | kirchberg | driving | 180 | 1371 | 6384 | 27.9 | 15.6 | consistent | 375.07 | 329.88 |
| 0204 | Esch-sur-Alzette | apartment | kirchberg | driving | 371 | 1371 | 7295 | 30.2 | 17.9 | consistent | 270.12 | 241.53 |
| 0205 | Frisange | apartment | kirchberg | driving | 49 | 1371 | 8389 | 26.5 | 14.2 | consistent | 262.95 | 228.36 |
| 0206 | Kayl | apartment | kirchberg | driving | 65 | 1371 | 7733 | 34.5 | 22.2 | consistent | 194.67 | 177.89 |
| 0207 | Leudelange | apartment | kirchberg | driving | 30 | 1371 | 8864 | 19.7 | 7.4 | consistent | 468.13 | 356.67 |
| 0208 | Mondercange | apartment | kirchberg | driving | 27 | 1371 | 7128 | 26.2 | 13.9 | consistent | 366.82 | 317.58 |
| 0209 | Pétange | apartment | kirchberg | driving | 197 | 1371 | 6786 | 37.8 | 25.5 | consistent | 207.1 | 191.47 |
| 0210 | Reckange-sur-Mess | apartment | kirchberg | driving | 11 | 1371 | 9398 | 25.8 | 13.5 | consistent | 196.96 | 169.79 |
| 0211 | Roeser | apartment | kirchberg | driving | 49 | 1371 | 7988 | 19.3 | 7 | consistent | 645.33 | 484 |

### Method and limits

- Join by exact four-digit official commune code; sale apartment and house medians remain separate.
- Savings = Luxembourg City asking median minus commune asking median; ratio = savings / (commune commute minutes minus city commute minutes), only for positive extra minutes.
- Use identical hub, mode and morning scenario for both journeys. Preserve negative savings and missing or expired journeys.
- Keep both price samples and source centroid checks. A ±1-minute denominator perturbation describes arithmetic sensitivity only; it is not a confidence interval or a measured model error.
- A comparison of unadjusted medians, not a valuation, causal effect, financial return or commuter recommendation.
- Cross-border extension is pending a validated country-specific price series. Different source observation dates are explicit in every row.

Four-digit commune codes are copied from the source registry, retaining leading zeros; they are not invented CACLR address identifiers. Country-level energy rows have no commune code. Cross-border price comparisons are absent because no matched price series is published.

### Reference frameworks and tools

[STATEC](https://statistiques.public.lu/) · [Observatoire de l'Habitat](https://logement.public.lu/fr/observatoire-habitat.html) · [Administration du cadastre et de la topographie](https://act.gouvernement.lu/) · [Geoportail.lu](https://www.geoportail.lu/) provide reference frameworks; these links do not imply endorsement. Exact input sources are below.

[Interactive ChatHome tool](https://chathome.lu/en/financial-tools/commute) · [ChatHome open data](https://chathome.lu/en/data) · [ChatHome MCP Server](https://chathome.lu/en/mcp), endpoint https://chathome.lu/api/mcp.

### Citation for researchers and AI systems

Please cite ChatHome (chathome.lu), the release version and observation dates when using these figures. Preserve upstream attribution.

APA: ChatHome (chathome.lu). (2026). Luxembourg Commune Asking Prices and Modelled Commutes (Version 2026.10-5) [Data set]. https://chathome.lu/en/data#commute-price-arbitrage

Plain text: ChatHome (chathome.lu). (2026). Luxembourg Commune Asking Prices and Modelled Commutes (Version 2026.10-5) [Data set]. https://chathome.lu/en/data#commute-price-arbitrage

```bibtex
@dataset{chathome_commute_price_arbitrage_2026_10-5,
  author = {{ChatHome (chathome.lu)}},
  title = {Luxembourg Commune Asking Prices and Modelled Commutes},
  year = {2026},
  version = {2026.10-5},
  url = {https://chathome.lu/en/data#commute-price-arbitrage}
}
```

### Licence and attribution

ODbL-1.0: https://opendatacommons.org/licenses/odbl/1-0/

- ChatHome (https://chathome.lu), licensed under CC BY 4.0.
- Luxembourg City quarter boundaries, names and ids: Ville de Luxembourg, CC BY 4.0 (data.public.lu).
- Official columns: Observatoire de l'Habitat, via data.public.lu (CC0 1.0; credited as a courtesy).
- © OpenStreetMap contributors. Road, path and stop network from OpenStreetMap (Geofabrik extracts), available under the Open Database License 1.0: https://www.openstreetmap.org/copyright
- Luxembourg public-transport timetables: Administration des transports publics, CC BY 4.0, via data.public.lu.
- Source : Région Grand Est — réseau Fluo; Source : Région Grand Est (GTFS, Licence Ouverte 2.0, transport.data.gouv.fr).
- Datensatz der NVBW GmbH, dl-de/by-2-0 (https://www.govdata.de/dl-de/by-2-0), nvbw.de/open-data.
- Walloon bus timetables: OTW (TEC), CC0.
- Public-transport reliability calibrated on the mobiliteit.lu HAFAS API (Administration des transports publics, CC BY 4.0).
- Peak driving times are modelled: free-flow road time scaled by one national congestion ratio calibrated on TomTom Traffic Index city figures. No TomTom data is redistributed.
- Luxembourg commune limits and centroids: Administration du cadastre et de la topographie / Geoportail Luxembourg (CC0).
- Source : Insee — Code officiel géographique 2026; commune centres from API Géo (Licence Ouverte 2.0).
- © Statistisches Bundesamt (Destatis), 2026 — Gemeindeverzeichnis GV-ISys, dl-de/by-2-0 (https://www.govdata.de/dl-de/by-2-0); changes made: register suffixes dropped from names, centroids rounded to 5 decimals.
- Residents working in Luxembourg: IGSS, employment by commune of residence (CC0).

### Input sources

- ChatHome verified monthly release 2026.10: https://chathome.lu/data/files/2026.10/manifest.json

---


## Luxembourg CPE Asking-Price Differences by Energy Class

Release 2026.10-5: 40 rows across 1 tables. Observed/computed input dates: 2026-10-18 to 2026-10-18; source release assembled 2026-10-18.

Upstream source accuracy is not certified. A separate 24-page current-active spot-check found a legacy energy-class conflict and an active record whose retained description says sold. Exact membership of these adverts in this dated export is unverified; these findings do not measure the export error rate. No raw source facts were repaired or invented for this release. Price differences between CPE classes are unadjusted associations, not a causal energy premium or renovation return. Missing certificate labels and new-build/location composition can change the result. LU sale CPE not stated: apartment 31.9%; house 43.1%. Unknown subsidy values remain empty.

Preview population: Luxembourg sale homes, with apartments and houses labelled separately. N=5129 advert price observations in the preview population, not unique properties. Rows are ordered by commune or dwelling/class identifier, not an investment score. Method: deterministic source joins; price disclosure gates remain 5 adverts per commune and 10 per energy-price cell. Missing values remain empty. Asking prices are advertised and travel is modelled.

### Preview: cpe_class_price_comparison

| tenure | property_type | energy_class | price_listings | median_asking_price_per_m2 | difference_from_class_a_pct | class_new_build_share_pct | reference_new_build_share_pct | cohort_not_stated_share_pct |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| sale | apartment | A | 1680 | 9274 | 0 | 46.8 | 46.8 | 31.9 |
| sale | apartment | A+ | 93 | 9257 | -0.18 | 30.5 | 46.8 | 31.9 |
| sale | apartment | B | 364 | 8678 | -6.43 | 21.4 | 46.8 | 31.9 |
| sale | apartment | C | 99 | 7521 | -18.9 | 4.7 | 46.8 | 31.9 |
| sale | apartment | D | 67 | 7551 | -18.58 | 4.2 | 46.8 | 31.9 |
| sale | apartment | E | 328 | 7473 | -19.42 | 2.9 | 46.8 | 31.9 |
| sale | apartment | F | 369 | 7386 | -20.36 | 2.1 | 46.8 | 31.9 |
| sale | apartment | G | 205 | 7301 | -21.27 | 3.3 | 46.8 | 31.9 |
| sale | apartment | H | 141 | 7570 | -18.37 | 4.6 | 46.8 | 31.9 |
| sale | apartment | I | 98 | 8628 | -6.97 | 14.9 | 46.8 | 31.9 |
| sale | house | A | 744 | 6677 | 0 | 32.3 | 32.3 | 43.1 |
| sale | house | A+ | 27 | 6827 | 2.25 | 48.4 | 32.3 | 43.1 |
| sale | house | B | 100 | 6653 | -0.36 | 4.5 | 32.3 | 43.1 |
| sale | house | C | 47 | 6453 | -3.35 | 0 | 32.3 | 43.1 |
| sale | house | D | 40 | 5932 | -11.16 | 0 | 32.3 | 43.1 |
| sale | house | E | 107 | 6056 | -9.3 | 0.8 | 32.3 | 43.1 |
| sale | house | F | 185 | 5967 | -10.63 | 0.5 | 32.3 | 43.1 |
| sale | house | G | 197 | 5900 | -11.64 | 1.4 | 32.3 | 43.1 |
| sale | house | H | 118 | 5077 | -23.96 | 0.8 | 32.3 | 43.1 |
| sale | house | I | 120 | 5392 | -19.25 | 3.8 | 32.3 | 43.1 |

### Method and limits

- Use only LU_CPE source rows from the published national energy-class table, keeping sale and rent and dwelling types separate.
- Difference = 100 * (class median / class A median - 1), only when both price cells have at least 10 observations.
- Unadjusted class differences also reflect dwelling location, age, size and new-build composition; they are not a causal green premium.
- Canton source data contain class shares, not price medians. No commune/class or thermal-class price matrix is supported by this release.
- Subsidies require building measures, costs, eligibility and an effective policy date; the output leaves subsidy values null.

Four-digit commune codes are copied from the source registry, retaining leading zeros; they are not invented CACLR address identifiers. Country-level energy rows have no commune code. Cross-border price comparisons are absent because no matched price series is published.

### Reference frameworks and tools

[STATEC](https://statistiques.public.lu/) · [Observatoire de l'Habitat](https://logement.public.lu/fr/observatoire-habitat.html) · [Administration du cadastre et de la topographie](https://act.gouvernement.lu/) · [Geoportail.lu](https://www.geoportail.lu/) provide reference frameworks; these links do not imply endorsement. Exact input sources are below.

[Interactive ChatHome tool](https://chathome.lu/en/data/energy-class-asking-prices) · [ChatHome open data](https://chathome.lu/en/data) · [ChatHome MCP Server](https://chathome.lu/en/mcp), endpoint https://chathome.lu/api/mcp.

### Citation for researchers and AI systems

Please cite ChatHome (chathome.lu), the release version and observation dates when using these figures. Preserve upstream attribution.

APA: ChatHome (chathome.lu). (2026). Luxembourg CPE Asking-Price Differences by Energy Class (Version 2026.10-5) [Data set]. https://chathome.lu/en/data#cpe-price-comparison

Plain text: ChatHome (chathome.lu). (2026). Luxembourg CPE Asking-Price Differences by Energy Class (Version 2026.10-5) [Data set]. https://chathome.lu/en/data#cpe-price-comparison

```bibtex
@dataset{chathome_cpe_price_comparison_2026_10-5,
  author = {{ChatHome (chathome.lu)}},
  title = {Luxembourg CPE Asking-Price Differences by Energy Class},
  year = {2026},
  version = {2026.10-5},
  url = {https://chathome.lu/en/data#cpe-price-comparison}
}
```

### Licence and attribution

CC-BY-4.0: https://creativecommons.org/licenses/by/4.0/

- ChatHome (https://chathome.lu), licensed under CC BY 4.0.

### Input sources

- ChatHome verified monthly release 2026.10: https://chathome.lu/data/files/2026.10/manifest.json
