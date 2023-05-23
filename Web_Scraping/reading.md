# Web Scraping 

## What are the key differences between scraping static and dynamic websites?

- Static websites: Static websites are built with HTML and CSS, where the content remains the same until it is manually updated. Scraping static websites involves fetching the HTML source code of a webpage and extracting the desired information directly from the HTML structure.

- Dynamic websites use client-side scripting languages like JavaScript to generate content on the fly. The content may change dynamically based on user interactions or data from external sources. Scraping dynamic websites requires executing JavaScript code to load and interact with the page before extracting the desired data.



## Explain at least three techniques or best practices that can be employed to avoid getting blocked while scraping websites.

- Respect website's terms of service: Check if the website has any terms of service or scraping policies
- Use scraping frameworks or libraries like BeautifulSoup
- delays between requests to mimic human browsing behavior. Randomize the delays and add variations in the request timing to avoid patterns that might trigger anti-scraping measures.


## What is Playwright, and how does it assist in web scraping tasks? Provide an example of a use case where Playwright would be particularly beneficial.

Playwright is an open-source library for automating browsers, developed by Microsoft. It provides a high-level API to control browsers, allowing developers to interact with web pages, fill forms, click buttons, and perform other actions. Playwright supports multiple browser engines (Chromium, WebKit, and Firefox) and offers powerful features for web scraping tasks.

Use case: Playwright is particularly beneficial when scraping websites that heavily rely on JavaScript to render content. For example, if you need to scrape a website that loads data dynamically using AJAX calls or performs complex client-side rendering, Playwright can execute the JavaScript code and retrieve the fully rendered content, making it easier to extract the desired data.

## Describe the purpose of using Xpath in web scraping, and provide an example of an Xpath expression to select a specific HTML element from a webpage.

Xpath (XML Path Language) is a query language used to navigate and select elements from XML or HTML documents. In web scraping

lxml is an example of libraries to work wit html file 


## Things I want to know more about

so the question is ? 

why i need to extract information from the html page ,what's the type of information sould be extracted , where will be used and whay ? 


look at this code 
```
from bs4 import BeautifulSoup

with open('./home.html', 'r') as html_file :

    content = html_file.read()
    # print(content)

    soup= BeautifulSoup(content, 'lxml')
    # print(soup.prettify())

    tag=soup.find('h5')  # find h5 tag first one
    tags= soup.find_all('h5') # find all h5 tags
    # print(tag) 

    for tag in tags:
        print(tag.text) 

    cards=soup.find_all('div', class_='cards') # add _ to class world becouse it's reversed to python

    for card in cards:
        name=card.h5.text
        price=card.a.text.split()[-1]

        print(f'{card} cost {price}')
```

all off these information is meanles for me until now 

tosee full code 
[link](https://github.com/AbdelrahmanElatrash/web_socet)