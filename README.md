# DeRace Data
## Overview
This is data I pulled from DeRace. It's all publicly available anyway. I used Selenium and Scrapy but I don't feel like releasing the spider, so that's the only hint you're getting. Anyways, all files with the `.jl` extension are JSON Lines files. Every line is a complete JSON tree and represents one entry. Should be pretty easy to process. Unless otherwise stated, each file was scraped on the date indicated by its folder.
## Types of Entries
For now there's only one type of entry.
### races.jl
This was pulled straight from www.derace.com/races/results. Each entry represents one race and has the following fields:
  - race_id
  - entry_requirement
  - prize_pool
  - hippodrome
  - length
  - start_time
  - podium_prizes
    - 1st
    - 2nd
    - 3rd
  - fastest_time
  - results (array of dicts, one for each place)
    - place
    - horse_name
    - horse_id
    - time
