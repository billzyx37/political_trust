# Codebook

## Unit of Observation
### year × congressional district

---

## Identifiers

### `year`
- **Type:** integer
- **Description:** Election year
- **Range:** 1956–2024

### `state_code`
- **Type:** string (2)
- **Description:** USPS state abbreviation (e.g. VA, CA)

### `district_code`
- **Type:** string (2)
- **Description:** Congressional district number
- **Notes:** `00` indicates at-large district and `98` indicates DC

### `state_district_code`
- **Type:** string (4)
- **Description:** State FIPS + congressional district number

---

## Trust Variables
### Source: ANES 
### Year range: 1956-2024
### Original Geographic Level: Congressional District

### `trust_gov_right`
- **Type:** float
- **Description:** To what extent does respondent trusts the federal government to do the right thing
- **Range:** 1-5
- **Note:** Range was 1-4 before 2024; all standardized based on 2024 scale

### `gov_for_all`
- **Type:** float
- **Description:** If the respondent trusts the federal government to serve for the good of all
- **Range:** 1-2

### `gov_waste`
- **Type:** float
- **Description:** How much the respondent thinks the government waste tax money
- **Range:** 1-3

### `crooked_officials`
- **Type:** float
- **Description:** How many officials are crooked in the respondent's opinion
- **Range:** 1-5

### `trust_gov_index`
- **Type:** float
- **Description:** Index constructed based on trust variables above
- **Range:** 0-100

### Notes
- For all trust variables, higher value implies more trust
- Z-score and dummy terms are constructed based on all trust variables, labeled as `_z` and `_d`
- Variables have various availability across time

---

## Election Outcomes
### Source: MIT Election Lab
### Year range: 1976-2022 (house); 2000-2024 (presidential)
### Original Geographic Level: Congressional District (house); County (presidential)

### `party`
- **Type:** string
- **Description:** Winning party

### `total_votes`
- **Type:** float
- **Description:** Total number of votes

### `vote_share`
- **Type:** float
- **Description:** Vote share toward the winning party

### `dem_share`
- **Type:** float
- **Description:** Vote share toward the democeratic party

### `dem_win_margin`
- **Type:** float
- **Description:** Democratic vote margin relative to 50% (=`dem_share_h - 0.5`)

### Notes
- House and presidential election has the same sets of variables, each labled as `_h` and `_p`
- Original data of presidential election is in county level
- Only the two major parties are included

---

## County Business Pattern (CBP)
### Source: Census Bureau
### Year range: 1986-2023
### Original Geographic Level: County

### `sector`
- **Type:** string
- **Description:** Sector of the establishment

### `emp`
- **Type:** integer
- **Description:** Total number of employment of the sector

### `est`
- **Type:** integer
- **Description:** Total number of establishments of the sector

### `qp1`
- **Type:** float
- **Description:** Total first quarter payroll (in $1,000)

### `ap`
- **Type:** float
- **Description:** Total annual payroll (in $1,000)

### Notes
- Sector aggregated from industries

---

## NHGIS Population Variables
### Source: NHGIS/American Community Survey (ACS)
### Year range: 1970-2023
### Original Geographic Level: County

### `total_pop`
- **Type:** float
- **Description:** total population

### `urban_pop`
- **Type:** float
- **Description:** population living in urban area

### `rural_pop`
- **Type:** float
- **Description:** population living in rural area

### `male_pop`
- **Type:** float
- **Description:** male population

### `female_pop`
- **Type:** float
- **Description:** female population

### `median_age`
- **Type:** float
- **Description:** median age

### `white_pop`
- **Type:** float
- **Description:** white population

### `black_pop`
- **Type:** float
- **Description:** black population

### `indig_pop`
- **Type:** float
- **Description:** american indian and alaska native population

### `asian_pop`
- **Type:** float
- **Description:** asian population

### `two_race_pop`
- **Type:** float
- **Description:** population identifying as two races

### `hispanic_pop`
- **Type:** float
- **Description:** hispanic and latino population

### `family_pop`
- **Type:** float
- **Description:** population in family households

### `non_family_pop`
- **Type:** float
- **Description:** population in non-family households

### `total_households`
- **Type:** float
- **Description:** total number of households

### `total_families`
- **Type:** float
- **Description:** total number of families

### `native_pop`
- **Type:** float
- **Description:** native-born population

### `foreign_pop`
- **Type:** float
- **Description:** foreign-born population

### `no_hs_pop`
- **Type:** float
- **Description:** 25 years and older population with less than 9 years of education

### `hs_college_pop`
- **Type:** float
- **Description:** 25 years and older population with 9 years to less-than-bachelor's education

### `college_grad_pop`
- **Type:** float
- **Description:** population with a bachelor's degree or higher

### `labor_force_pop`
- **Type:** float
- **Description:** population in the labor force

### `armed_force_pop`
- **Type:** float
- **Description:** population in the armed forces

### `civ_pop`
- **Type:** float
- **Description:** civilian population

### `out_labor_force_pop`
- **Type:** float
- **Description:** population not in the labor force


### Notes
- Five year rolling average and decennial data
- Moving towards 1-year data
- Once mapped to district level, calculate relative information (e.g. male percentage)
- Socio-economic data available but not included: employed population, unemployed population, travel time to work, per capita income, and population in poverty


