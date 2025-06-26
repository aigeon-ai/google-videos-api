```markdown
# Aigeon AI Google Videos API

Aigeon AI Google Videos API is a Python-based server application designed to facilitate video searches using the Google Videos API. This application leverages the SerpAPI to provide structured video search results, including video titles, links, thumbnails, and durations. The server is built on the FastMCP framework, ensuring efficient and scalable handling of search requests.

## Features Overview

- **Google Videos Search**: Perform video searches using Google's video search engine with support for advanced query syntax.
- **Location-Based Searches**: Customize search results based on geographical location.
- **Language and Domain Customization**: Specify language and Google domain preferences for tailored search results.
- **Advanced Search Parameters**: Utilize advanced search filters such as date and duration.
- **Safe Search Filtering**: Control the inclusion of adult content in search results.
- **Pagination and Result Limiting**: Manage the number of results and pagination for efficient data handling.
- **Device Type Specification**: Simulate searches from different device types like desktop, tablet, or mobile.
- **Cache Control**: Enable or disable caching for search results.
- **Asynchronous Search Mode**: Option to perform searches asynchronously for enhanced performance.

## Main Features and Functionality

The core functionality of the Aigeon AI Google Videos API is encapsulated in the `search_videos` function. This function is exposed as a tool through the FastMCP server, allowing clients to perform video searches with a wide array of customizable parameters. The function constructs a request payload based on user inputs and sends it to the SerpAPI endpoint to retrieve search results.

### Key Functionalities:

- **Search Query**: Accepts a search query string that supports advanced Google search syntax.
- **Location and Language**: Allows specifying a location and language for localized search results.
- **Advanced Filters**: Supports additional filters such as safe search, language restriction, and search result filtering.
- **Pagination**: Provides options for result pagination and limiting the number of returned results.
- **Device Emulation**: Simulates searches from different device types to mimic various user environments.
- **Cache Management**: Offers control over caching behavior to ensure fresh results when needed.
- **Asynchronous Execution**: Supports asynchronous search execution for improved performance in certain scenarios.

## API Endpoints or Main Functions Description

### `search_videos`

This is the primary function of the application, designed to interact with the Google Videos API via SerpAPI. It accepts several parameters to customize the search:

- **q**: The search query string, supporting advanced syntax like `inurl:`, `site:`, `intitle:`, etc.
- **location**: Geographical location for the search, specified at a city level (e.g., 'Austin, TX').
- **uule**: Google encoded location, mutually exclusive with `location`.
- **google_domain**: The Google domain to use, defaulting to 'google.com'.
- **gl**: Country code for the search (e.g., 'us' for the United States).
- **hl**: Language code for the search (e.g., 'en' for English).
- **lr**: Restricts search to specific languages (e.g., 'lang_fr|lang_de').
- **tbs**: Advanced search parameters for filtering by date, duration, etc.
- **safe**: Safe search filter, either 'active' or 'off'.
- **nfpr**: Excludes spelling correction results (1 for yes, 0 for no).
- **filter**: Enables or disables result filtering (1 for enabled, 0 for disabled).
- **start**: Pagination offset (e.g., 0 for the first page, 10 for the second page).
- **num**: Number of results to return, ranging from 10 to 100.
- **device**: Device type for the search ('desktop', 'tablet', or 'mobile').
- **no_cache**: Disables caching if set to `True`.
- **async_mode**: Enables asynchronous result fetching if set to `True`.

The function returns structured JSON data containing video search results, which include video titles, links, thumbnails, and durations.

---

This README provides a comprehensive overview of the Aigeon AI Google Videos API, detailing its features, functionalities, and the main search function. The application is designed to be flexible and efficient, catering to various search needs through customizable parameters.
```