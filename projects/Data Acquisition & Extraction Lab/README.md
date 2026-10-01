# Digital Forensics Investigation

## Overview

In this Forensic Computing lab, I used FTK Imager and Autopsy on Windows to practice data acquisition and investigate a supplied `SuspectData.dd` disk image. I performed keyword searches, tagged files and images, extracted data, and generated an Autopsy report. Screenshots document the acquisition and reporting stages.

## Tools and Topics

- **FTK Imager:** Forensic data acquisition.
- **Autopsy:** Case creation, disk image analysis, and report generation.
- **Evidence review:** Keyword searches, file and image tagging, and data extraction.

## Workflow

1. **Practiced disk acquisition in FTK Imager.** Selected `PHYSICALDRIVE1` as the source and started creating a “Suspect USB Image” on the destination drive. The screenshot captures imaging in progress and the output image segments.
2. **Created an Autopsy case.** Set up case `001-SuspectUSB-JN`, case number `001`, with my name as examiner.
3. **Added the supplied evidence image.** Loaded `SuspectData.dd` as the case’s data source and used the `America/New_York` time zone.
4. **Searched and reviewed the evidence.** Performed keyword searches, inspected files and images, and extracted data from the supplied image.
5. **Tagged relevant items.** Tagged files and images to organize the items selected for reporting.
6. **Generated an HTML report.** Exported an Autopsy forensic report and captured its case summary, evidence source, and navigation sections.

## Results

The report screenshot shows **one data source, four keyword hits, one tagged file, and one tagged image** in Autopsy 4.23.1. The materials document the acquisition and reporting stages; the complete exported HTML report is not included.

## Materials

- [Data acquisition screenshot](./Lab1%201st%20Screenshot.png)
- [Autopsy report screenshot](./Lab1%20Autopsy%20report.png)
- [Provided disk image](./SuspectData.dd)
