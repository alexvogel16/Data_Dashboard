			     ____________________________________
			     | 					 |
                             | 	Author: Alexander Michael Vogel  |
			     |	Contact: alexvogelmhs@gmail.com  |
			     |	Organization: NYC DOHMH OSH      |
			     |	Supervisors: Dr. Cheryl Lawrence |
			     |		   : Dr. Andres Jimenez  |
			     |	Published: May 27, 2021          |
			     |___________________________________|

-------------------------NYC DOHMH Office of School Health Data Dashboard------------------------- 

SOFTWARE
	1. Data Analysis: RStudio Version 1.4.1106
		a. Additional Data Management: Microsoft Excel for Microsoft 365 MSO (16.0.13929.20360) 64-bit 
		b. YRBS Data Management: SAS Proprietary Software 9.4 (TS1M6)
	2. Data Visualization: Tableau Desktop (Professional Edition) Version 2020.3.9 (20203.21.0509.1143) 64-bit
		a. See included Tableau Packaged Workbook: "datadashboardvis.twb"

OUTPUT
	1. Master Spreadsheet: "dashboarddata2021.csv"
	2. Data Visualization (Built Environment) supplement: "schdat.csv"

DATA SOURCES
		a. See links for associated codebooks and internal data sources
		b. Details regarding coding are found within:
			i.  "dashboarddata.html" (HTML file, best viewed in Google Chrome)
			ii. "dashboarddata.Rmd" (R Markdown file, best viewed in RStudio)
	1. Crosswalks: https://www1.nyc.gov/site/planning/data-maps/nyc-population/geographic-reference.page 
		a. ZIP Code
		b. Borough Code
		c. ZCTA Code
		d. Borough Name
		e. PUMA Code
		f. NTA Code
		g. NTA Name
		h. UHF Name
	2. School District Crosswalk: https://github.com/vr00n/NYC-LocalGeo-CrossWalk
	3. Demographics (US Census data joined with NYC GIS data): https://github.com/mfherman/nycgeo
			i. "The spatial files contained in the nycgeo package are available on websites such as the New York City Department of City Planning’s Bytes of the Big Apple and the U.S. Census Bureau TIGER/Line® Shapefiles, but this package aims to make accessing the spatial data more convenient. Instead of downloading and converting shapefiles each time you need them, nycgeo provides the files in a consistent format (sf) with added metadata that enable joins with non-spatial data."
		a. White Percent
		b. Black Percent
		c. Hispanic Percent
		d. Asian Percent
		e. Bachelor's Degree or Above Percent
		f. Poverty Percent

	4. Health and Environment: see "nycdatasources.csv" or http://a816-dohbesp.nyc.gov/IndicatorPublic/BuildATable.aspx 
		a. Blood Lead Level Elevated in Children Under 6 years Percent: https://a816-hrt.nyc.gov/DataCatalog/Pages/DataView.cshtml?id=928fe7e8-1d4d-4ad6-b336-2b9704f2466b 
			i. "Number of children under 6 years of age tested with blood lead levels (BLL) 5 mcg/dL or greater; divided by the total number of children under 6 years of age who were tested; expressed as cases per 1;000 tested. While children can receive more than one test during the calendar year; for this measure children are only counted once per year using the highest confirmed blood lead level during the calendar year. If the child does not have a confirmed test in a given year; the child’s blood lead level is based on the highest capillary or unknown test type."
		b. Asthma ED Visits in Children Age 0-4 (Annual Average Rate per 10000 Resident 0-4-year-olds): https://a816-hrt.nyc.gov/DataCatalog/Pages/DataView.cshtml?id=cdce56d2-b59f-44a1-a65f-c99d6fde372d 
			i. "Average annual number of asthma-related emergency department (ED) visits among NYC resident children aged 5 to 17 years; divided by the population of children 5 to 17 years old; using NYC DOHMH intercensal estimates; expressed as cases per 10;000 residents"
		c. Asthma ED Visits in Children Age 5-17 (Annual Average Rate per 10000 Resident 5-17-year-olds): https://a816-hrt.nyc.gov/DataCatalog/Pages/DataView.cshtml?id=cdce56d2-b59f-44a1-a65f-c99d6fde372d 
			i. "Average annual number of asthma-related emergency department (ED) visits among NYC resident children aged 5 to 17 years; divided by the population of children 5 to 17 years old; using NYC DOHMH intercensal estimates; expressed as cases per 10;000 residents"
		d. Incarceration Percent: https://www.health.ny.gov/statistics/sparcs/access/ 
			i. "Crude rate of of incarcerated adults in NYC Department of Correction facilities per 1;000 population ages 18 and older"
		e. High School Graduation Percent: American Community Survey
			i. "Estimated number of people 25 years and over who have completed High School (Includes Equivalency); divided by the total number of people 25 years and over; expressed as percent"
		f. Limited English Percent: American Community Survey
			i. "Estimated number of people who do not speak English at home and are not English Proficient divided by the total population; expressed as percent"
		g. Rent-Burdened Households Percent: American Community Survey
			i. "Estimated number of renter households whose gross rent (rent plus electricity and heating fuel costs) equals at least 30 percent of their income divided by the total number of households; expressed as percent"
		h. Unemployment Percent: American Community Survey
			i. "Estimated number of people in the civilian labor force (16 years and older) who are unemployed divided by the total civilian labor force; expressed as percent"
		i. Court-Ordered Eviction Percent: American Community Survey
			i. "Rate of executed evictions ordered by the New York City Housing Court; including those pending and scheduled as of December 31; per 10;000 housing units"
	5. Access
		a. Number of Mental Health Facilities in ZIP Code: https://www1.nyc.gov/site/planning/data-maps/open-data/dwn-selfac.page 
			i. Number of mental health facilities summed by zip code
		b. Number of Parks in ZIP Code: https://data.cityofnewyork.us/api/views/ghu2-eden/rows.csv?accessType%3DDOWNLOAD&sa=D&source=editors&ust=1617036530589000&usg=AFQjCNG2TyjP1v9A3pIBAUxrqOzjghVJAg 
			i. Number of parks summed by zip code
	6. Behavior (Youth Risk Behavioral Survey, 2019 National Dataset): https://www.cdc.gov/HEALTHYYOUTH/DATA/YRBS/DATA.HTM 
			iv. Downloaded in SAS format, formatted in SAS, exported as .csv, filtered by location and survey year in Excel, saved as .csv
		a. Obesity Percent
		b. Overweight Percent
		c. Did Not Go to School Because of Safety Concerns Percent
		d. Physical Fight at School Percent
		e. Bullied at School Percent
		f. Physically Active One Hour Five Days a Week Percent
		g. Sleeps Eight or More Hours Percent
		h. Bisexual Percent
		i. Gay or Lesbian Percent
		j. Heterosexual Percent
		k. Unsure of Sexuality Percent
		l. Transgender Percent
		m. Unsure if Transgender Percent
		n. Not Transgender Percent
		o. Doesn't Know What Transgender Means Percent

