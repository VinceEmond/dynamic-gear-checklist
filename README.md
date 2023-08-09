# Dynamic Gear Checklist

### Summary

An app designed to streamline the process of creating a dynamic checklist required for the daily truck load-out of equipment for a Window/Gutter/Power washing business. The business owner wanted to be able to embed this checklist into his Google Site therefor the app was written in a single file using HTML, Javascript, CSS.

### Features

- Merges items from multiple selected "job types" into one main master list without duplicates
- If a peice of equipment is required by more than one of the selected jobs and each one holds a different level of importance (Required/Sometimes/Rarely), the app only lists the one with the highest tier of importance.
- Reset button to reset the app

### Screenshots

<p align="middle" float="left">
  <img align="top" src="https://github.com/VinceEmond/dynamic-gear-checklist/blob/main/public/Shine-99-Gear-Checklist.png?raw=true" width="40%" />
  <img src="https://github.com/VinceEmond/dynamic-gear-checklist/raw/main/public/Shine-99-Gear-Checklist-2.png" width="40%" />
</p>

### App Logic

- Gather which job type has been checkmarked

  - For each checkmarked job --> Pull list of all equipment

    - For each "Required" gear item
      - If the gear doesn't already exist in Master Required list, add to Master Required list
    - For each "Sometimes" gear item
      - If the gear doesn't already exist in the Master Required OR Master Sometimes list, add to Master Sometimes list
    - For each "Rarely" gear item
      - If the gear doesn't already exist in the Master Required OR Master sometimes list or Master Rarely list, add to Rarely list

  - For Each list item in the Master Required list

    - Generate list dom element and Append to List

  - For Each list item in the Master Sometimes list

    - Generate list dom element and Append to List

  - For Each list item in the Rarely Sometimes list
    - Generate list dom element and Append to List
