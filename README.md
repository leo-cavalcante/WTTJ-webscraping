<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>

# Web Scraping "Welcome to the Jungle" website by Leo
**Leonardo Cavalcante Araújo**

*Data Analytics Full-Time FEB2021, Paris & February 22nd 2021*

## Content
- [Project Description](#project-description)
- [Objective](#objective)
- [Workflow](#workflow)
- [Organization](#organization)
- [Links](#links)

<img src="https://cdn.welcometothejungle.co/wttj-front/production/assets/images/social/logo_v2.png?v=478410c0b052c7b9fa53dc2b4206d041" alt="Welcome to the Jungle Logo" width="500" style="text-align:center"/>

## Project Description
Amidst the difficult context to find job during Covid-19 pandemic and because of all of the frustration that Job Search can provide, I decided to use a Data-Driven approach to help me structure my Job Search Strategy.

Therefore, I decided to scrap my preferred Job Search Website : ["Welcome to the Jungle"](https://www.welcometothejungle.com/en/jobs?query=data%20analyst&page=1&aroundQuery=Paris%2C%20France&refinementList%5Boffice.district%5D%5B0%5D=Paris&refinementList%5Boffice.state%5D%5B0%5D=Ile-de-France&refinementList%5Boffice.country_code%5D%5B0%5D=FR) (WTTJ).

The data scraped would be stored in 2 different databases:
1. **Jobs**: one line per job position open and all the details related to it.
2. **Companies**: one line per company offering a position in Data, with all the relevant details from this company page in the WTTJ website.

## Objective
Obtain exploitable data that could be used for analysis to help me guide in my Job search, by prioritizing the job references that corresponds the most to me and that provides me the most chance of succeeding.

## Workflow
First, it was necessary to get Jobs data and clean it from the Jobs Search:
1. Web scraping ["Welcome to the Jungle - Data Analyst Jobs "](https://www.welcometothejungle.com/en/jobs?query=data%20analyst&page=1&aroundQuery=Paris%2C%20France&refinementList%5Boffice.district%5D%5B0%5D=Paris&refinementList%5Boffice.state%5D%5B0%5D=Ile-de-France&refinementList%5Boffice.country_code%5D%5B0%5D=FR) and storing it to *Jobs* dataframe. 
2. Cleaning the Jobs dataframe.
3. Export the Jobs table to SQL.
4. Save data in a Pickle to avoid scraping everytime the session in Jupyter Notebook is restarted.

Secondly, it was necessary to get Companies data and clean it for *every company* in the previous scraping:
1. Web scraping the Jobs dataframe looping through each value of "https:/welcometothejungle.com/en/companies/" + Jobs\["organization_slug]. Then storing all data collected in the *Companies* datafram. 
2. Cleaning the Companies dataframe.
3. Export the Companies data to SQL.
4. Save data in a Pickle to avoid scraping everytime the session in Jupyter Notebook is restarted.

Third, it was necessary to formalize everything in functions so things could run smoothly by calling less than 10 functions.

Lastly, it was time to analyze the results using Python, Pandas and data vizualization tools.

## Organization
- Repository "https://github.com/leo-cavalcante/data-ft-par-labs/blob/main/Projects/Week-3/" : you may find my 2 main Python codes stored as a Jupyter Notebook format, also the pickles stored for each database and the Jobs.csv.

*PS.: individual project.*

## Links
Here you may find the relevant links for my repository, my main code  and presentation slides.

[Jobs_and_Companies_vFinal](https://github.com/leo-cavalcante/data-ft-par-labs/blob/main/Projects/Week-3/Jobs_and_Companies_vFinal.ipynb)  
[Another_way_of_scraping_Companies](https://github.com/leo-cavalcante/data-ft-par-labs/blob/main/Projects/Week-3/Another_way_of_scraping_Companies.ipynb)  
[GitHub Repository](https://github.com/leo-cavalcante/data-ft-par-labs/tree/main/Projects/Week-3)  
[Final Presentation - Google Slides](https://docs.google.com/presentation/d/1H91rL3dhN7dNDxZEJCj6XTysaTC8qrk_XPpgmEk8PXw/edit?usp=sharing)