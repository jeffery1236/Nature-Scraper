<!-- PROJECT SHIELDS -->
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
<!-- [![MIT License][license-shield]] -->
<!-- [![LinkedIn][linkedin-shield]][linkedin-url] -->

# Nature Scraper
A Toolkit for scraping articles from Nature.com
<br />
<a href="https://github.com/jeffery1236/NatureScraper/issues">Report Bug</a>
·
<a href="https://github.com/jeffery1236/NatureScraper/issues">Request Feature</a>

<!-- ABOUT THE PROJECT -->
## About The Project
This is a simple scraper built with BeautifulSoup and pdfkit.</br>

It allows the user to search for article with the *related search term* within a *date range*. The scraper then extracts content sentences and/or *save the article as a pdf*.


## Installation

1. Clone the repo
   ```sh
   git clone https://github.com/jeffery1236/Nature-Scraper.git
   ```
2. Install Python dependencies (>= Python 3.6)
    ```sh
    pip install -r requirements.txt
    ```
3. Install additional dependencies for saving article as pdf </br>
    Debian/Ubuntu:
    ```sh
    apt-get install wkhtmltopdf
    ```
    Windows:
    ```sh
    choco install wkhtmltopdf
    ```
    MacOS:
    ```sh
    brew install Caskroom/cask/wkhtmltopdf
    ```



<!-- USAGE EXAMPLES -->
## Usage

Example:

```python
from NatureScraper import Scraper

scraper = Scraper()
articles = scraper.extract_nature_articles('2020-02-07', '2020-02-12', 'coronavirus', save_pdf=True, pdf_dir='./saved_articles')

# articles is a list of dictionaries with the following fields
# {
#     'Title': str,
#     'Author': List[str],
#     'Published Date': str,
#     'Url': str,
#     'Summary': str,
#     'Content': List[str] # list of text paragraphs within each p-tag on the website
# }
```



<!-- CONTRIBUTING -->
## Contributing

Additonal features or bug fixes are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<!-- LICENSE -->
<!-- ## License

Distributed under the MIT License. See `LICENSE` for more information. -->

<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [BeautifulSoup](https://pypi.org/project/beautifulsoup4/)
* [Pdfkit](https://pdfkit.org/)



[forks-shield]: https://img.shields.io/github/forks/jeffery1236/NatureScraper
[forks-url]: https://github.com/jeffery1236/NatureScraper/network/members
[stars-shield]: https://img.shields.io/github/stars/jeffery1236/NatureScraper
[stars-url]: https://github.com/jeffery1236/NatureScraper/stargazers
[issues-shield]: https://img.shields.io/github/issues/jeffery1236/NatureScraper
[issues-url]: https://github.com/jeffery1236/NatureScraper/issues
<!-- [license-shield]: https://img.shields.io/github/license/jeffery1236/NatureScraper -->
<!-- [license-url]: https://github.com/jeffery1236/NatureScraper/blob/master/LICENSE.txt -->
