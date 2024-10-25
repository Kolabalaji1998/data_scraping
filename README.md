# World Bank Data Scraper & FastAPI Service

This project demonstrates how to scrape country-specific data from the World Bank’s website and serve it through a FastAPI-based REST API. The code, written in a Jupyter notebook, combines web scraping with API development, allowing easy access to global economic and social data.

## Project Structure
```bash
scraping_data/
├── scraping_worldbank_fastapi.ipynb    # Jupyter notebook with scraping and API setup
└── README.md                           # Project documentation
```
## Features
Data Extraction: Uses Selenium and BeautifulSoup to scrape World Bank data.
API Service: FastAPI is used to create a REST API that serves the data.
Data Storage: Scraped data is stored in CSV format using Pandas.

## Getting Started
### Prerequisites
- Python 3.7+
- Jupyter Notebook
- ChromeDriver (for Selenium)
### Installation
1. Clone this repository:

```bash
git clone https://github.com/Kolabalaji1998/scraping_data.git
cd scraping_worldbank_fastapi
```
### Install dependencies:

```bash
pip install -r requirements.txt
Ensure ChromeDriver is installed and accessible.
```
### Usage
#### Run the Jupyter Notebook:

- Open `scraping_worldbank_fastapi.ipynb` in Jupyter Notebook.
- Run each cell sequentially to scrape the World Bank data and set up the API server.
#### Start FastAPI Server:

- After scraping, follow the instructions in the notebook to run the FastAPI server using:
```bash
uvicorn main:app --reload
```
The API will be available at http://127.0.0.1:8000.

### API Endpoints

|Method	|       Endpoint              |	Description                                 |
|-------|-----------------------------|---------------------------------------------|
|GET	| /countries/{country_code}   |	Retrieves data for a specific country.      |
|GET	| /indicators/{indicator_code}|	Retrieves data based on specific indicators.|

Example: Access `http://127.0.0.1:8000/countries/USA` to get data for the USA.
