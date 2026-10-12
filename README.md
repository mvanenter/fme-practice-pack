## Download the practice pack

Download the datasets and supporting files for the FME practice exercises.

[**Download the FME Practice Pack (ZIP)**](./files.zip)

# FME practice pack: five spatial data cleaning scenarios

A set of hands-on practice exercises for anyone learning FME (Feature Manipulation Engine) who has finished a beginner course and wants to try real workflows. Each scenario has messy data with deliberately planted errors, a set of requirements, and an answer key so you can check your results against known answers instead of guessing.

Created by Melanie van Enter, with the help of AI (Claude by Anthropic), as personalised training material while learning FME.

## About the data

All of the data is synthetic. It was generated for practice, it is set around Christchurch, New Zealand, and none of it comes from a real organisation or person. It is safe to share and use.

## The five scenarios

| # | Scenario | Level | What you practise |
| --- | --- | --- | --- |
| 1 | Road safety analysis | Beginner | Duplicates, date and time parsing, text cleaning, lookups, swapped coordinates, rejects, summary reports |
| 2 | Water infrastructure asset audit | Beginner to intermediate | Joins, ID normalisation, validation, orphan records, reprojection, pipe lengths |
| 3 | Rainfall and river monitoring | Intermediate | Placeholder values, duplicate readings, daily aggregation, statistics, spatial join to catchments |
| 4 | Property and zoning integration | Intermediate | Duplicate parcels, centroid overlay, status rules, exception reporting |
| 5 | Electricity network migration | Intermediate to advanced | Merging two systems, ID formats, CRS problems, unit conversion, multi-format output |

## What is in each folder

- `REQUIREMENTS.md` explains the story, the input files and exactly what to produce.
- `data/` holds the files to load into FME (CSV and GeoJSON).
- `answer_key/` holds the expected counts, summary tables and row-level expected outputs.

## How to use it

1. Start with scenario 1 and work upwards. Each one is harder than the last.
2. Read `REQUIREMENTS.md` and look at the data. Before fixing anything, list the problems you can find.
3. Build your workspace. Aim for one clean chain of transformers, and keep the rejects (bad rows) in their own output so you can count them.
4. Do not open `answer_key/` until you have finished your own attempt.
5. Compare your results with the answer key: first the headline counts in `ANSWER_KEY.md`, then join your output to the expected CSV on the ID column to find any rows that differ.

## Things to know

- Coordinates are NZTM (EPSG:2193) unless a file says otherwise. The GeoJSON files are WGS84 (EPSG:4326), so reprojection is part of the practice.
- Numeric tolerances (lengths, areas, coordinates) are stated in each answer key.
- The answer keys were calculated with a separate reference solution, not in FME. If your result differs, check the wording of the rules first, and then tell me if you think the answer key is wrong.
- You need FME Form (a trial licence is fine). A GIS such as QGIS or ArcGIS Pro helps for checking the spatial outputs.

## Feedback

If you try it, I would love to hear how it went and which scenarios were most useful. Message me on LinkedIn.

Free to use for learning. If you share it, please credit the source.
