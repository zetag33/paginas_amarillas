# paginas_amarillas
Scraping of Paginas_Amarillas. A spanish website that contains the data of businesses in the country that advertise themselves in the page.

This code handles url crawling, firstly, in order to have all the urls needed to be scrapped. After that it does a connection to each one of those urls and scraps the content I need, that includes:
  - Name of the business
  - Sector of the business
  - Address
  - Postal Code
  - Phone
  - Web
  - Technology of the web(from the web I check how it was built)
  - Description
  - Province
  - City

It uses Selenium in order to deal with javascript, there is a lot of logic associated with how that specific website is structured, but the essence of the code may be appliable to any page that has a geographic structure and has also a catalog structure.
So we scrap each url, we check if there is a next button that redirects to page 2 of the initial url, if it doesnt then gets to the next url to be scrapped, else it continue to scrap in the catalog of the same initial page until there are no more pages.
In a nutshell, we are scrapping all urls and all the child urls associated with those, until there are no more.

I use multiprocessing in order to be able to do the process faster, in my case I use 10 CPU's and the process took like 2 hours and 30 minutes.

The project scrapped approximately 11.000 urls and I was able to scrap data from 65k businesses.

