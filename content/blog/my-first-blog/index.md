---
title: Investigating Twitter Connections
date: '2024-11-15T12:00:00.00Z'
description: 'Social Network Analysis from a Web Crawler'
---

## How we can use Web Crawling and Social Network Analysis (SNA) to analyze Twitter Connections

In the past, I had been curious as to how people interact with each other and the different forms of connections made between them, especially in online spaces. This came in different forms from platforms like X (formerly Twitter), Instagram, Linkedin, and many more; these platforms share different purposes but ultimately all have the ability to find how people connect to other individuals, whether through followers or another method of detection. This project is centered around that interest, where I use a web crawler to scrape data off of X, and analyze it using SNA. SNA is a method used to examine the relationships between individuals within a network, revealing how they interact and influence each other. On social media platforms like X, SNA can uncover key figures and connections within a community. In this project, I used Elon Musk as the central figure to analyze his network of connections, aiming to understand his reach, influence, and connections within the platform.

![Google inspect element of X site](./web_crawler_image.png)

I used Python for this project, which I will explain in a second, but here are the libraries within which I used also. I will go into further detail throughout this blog on the areas in which they were used.

> BeautifulSoup4: A Python library used to parse HTML and extract data from web pages. It allowed us to extract profile data for each user in the network.

> Selenium: An automation tool that enabled us to navigate the platform dynamically, handling interactions that BeautifulSoup4 alone couldn’t manage (e.g., scrolling to load more connections).

> NetworkX: A Python library used to construct and analyze the network graph, enabling us to calculate centrality metrics and visualize the network structure.

> Matplotlib: A plotting library that helped in creating clear and informative visualizations of the network.

> Plotly: A plotting library as well, providing interactions and a more aesthetic colour schema.

> Sqlalchemy: A lightweight database library handling data collection automation.

## Goals and how they were achieved

### 1. Scrape data from the X web page using a web crawling automated bot

The first step I had to take was to create the automated bot that would be gathering data and storing it in a database for me to use. It was created in Python with the use of multiple libraries alongside it. 

Python was chosen for the project as I had previous experience with using it for data visualizations, and it contains different libraries for machine learning and data visualization that have been highly developed. Additionally, it was picked for its relatively straightforward syntax compared to other languages such as R and its abundance of useful, optimized libraries - even if the language itself isn’t highly performant. 

### Create a visualization of Elon Musk's social network on X using aforementioned data

After data collection, the next step was to construct my social network. This was done using the NetworkX library in python, and using it I was able to transform the raw data which I had into meaningful results which I could interpret. It also was used to create visualizations of the social network, and had features to calculate centrality metrics which can measure the degree of closeness between individuals, which individuals have the most connections, as well as others.

## Step-by-step of the project

The first step to take for the project is to import all the necessary libraries and download the chrome driver. The chrome driver enables automatic web apps to be ran on chrome, which is necessary for our project.

```python
# Path to ChromeDriver
CHROMEDRIVER_PATH = r'path to local chrome driver'
# User credentials
USER_USERNAME = 'name of bot'
USER_PASSWORD = 'password for bot'
USER_EMAIL = 'email for bot'
# Target URL
URL_ID = "scrapingdog"
TARGET_URL = f"https://twitter.com/{URL_ID}"
# Initialize the Chrome WebDriver
driver = webdriver.Chrome(service=Service(CHROMEDRIVER_PATH))
# Open the target URL
driver.get(TARGET_URL)
driver.implicitly_wait(5)
```

- Numquam fugiat quibusdam aut ut
- Soluta necessitatibus deserunt nobis
- Illum esse recusandae facere ipsam

Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde reprehenderit inventore sunt, consequatur omnis tempore ullam natus.

1. Numquam fugiat quibusdam aut ut
2. Soluta necessitatibus deserunt nobis
3. Illum esse recusandae facere ipsam

Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde reprehenderit inventore sunt, consequatur omnis tempore ullam natus, porro odit aut, atque asperiores repudiandae corporis quidem esse eos provident velit perferendis magni fugit eum quisquam eligendi. Atque distinctio iure aliquam veniam inventore, soluta est, cum accusantium possimus illum quasi eveniet sed amet ipsa culpa vel in delectus laboriosam repellendus totam. Facere.

## Suscipit soluta necessitatibus deserunt nobi

Minus rem dicta eos exercitationem illum consequatur consectetur praesentium voluptas. Dolor inventore quasi necessitatibus odio eaque doloribus.



Numquam fugiat quibusdam aut ut, voluptatibus accusamus repellendus quas minus consequuntur possimus!
