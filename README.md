# water-permit-webscraping
Webscrape IGAM water permit data

This study presents an automated web scraping methodology to systematically retrieve water permit data from the environmental licensing system of Minas Gerais, Brazil. Utilizing Python, the script initiates a sequence starting from a predefined permit ID (87) and iteratively requests data up to a specified final ID (last_id). For each permit ID, the script constructs a URL to access the corresponding permit details, performs an HTTP GET request using the requests library, and verifies the response status to ensure successful retrieval.

The HTML content of each page is parsed using the BeautifulSoup library, allowing for the extraction of various data components. General information is extracted from specific HTML tags and structured into a DataFrame with pandas. Additionally, the script identifies and processes tables containing flow-related data, converting text to numeric values where applicable and integrating this information into the main DataFrame. Coordinates data are similarly extracted and merged.

Moreover, the methodology includes the extraction of water use purposes from designated tables, appending these details to the consolidated DataFrame. Each entry is also annotated with its source URL for reference. The cumulative result is a comprehensive DataFrame (df_outorga_decisao) that aggregates all relevant water permit data, facilitating subsequent analysis and research.

This approach demonstrates a robust framework for the automated acquisition of environmental data, leveraging libraries such as requests, BeautifulSoup, pandas, geopandas, and re. It emphasizes its applicability in environmental monitoring, regulatory compliance, and resource management studies, offering a compelling blend of geospatial and data science techniques.
