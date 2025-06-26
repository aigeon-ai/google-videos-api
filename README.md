```markdown
# Aigeon AI Google Videos API

## Project Description

The Aigeon AI Google Videos API is a server application designed to interact with the Google Videos search engine through the SerpAPI. This application provides a robust interface for querying video search results with various customizable parameters, delivering structured data that includes video titles, links, thumbnails, and durations.

## Features Overview

- **Customizable Search Queries**: Supports advanced search syntax and various parameters to refine video search results.
- **Geolocation Support**: Allows searches to be tailored to specific geographic locations.
- **Language and Domain Customization**: Provides options to specify language and Google domain for search results.
- **Safe Search and Filtering**: Includes options for safe search filtering and result filtering.
- **Pagination and Result Control**: Offers control over the number of results and pagination.
- **Device Type Specification**: Allows specifying the device type for search results.
- **Cache Management**: Options to enable or disable caching of results.
- **Asynchronous Search**: Supports asynchronous search operations.

## Main Features and Functionality

The Aigeon AI Google Videos API is built using the FastMCP server framework, leveraging the SerpAPI to perform video searches on Google. The application is designed to be flexible and efficient, allowing users to tailor their search queries with a wide range of parameters:

- **Search Customization**: Users can input search queries with advanced syntax such as `inurl:`, `site:`, `intitle:`, etc., to refine their search results.
- **Location and Language Options**: The application supports specifying a location (city-level precision) and language settings to customize search results based on geographical and linguistic preferences.
- **Search Filters**: Users can apply filters for safe search, language restrictions, and advanced search parameters like date or duration filters.
- **Result Management**: The application provides options to control the number of results returned, pagination, and whether to exclude spelling correction results.
- **Device and Cache Control**: Users can specify the device type (desktop, tablet, mobile) and manage caching preferences to optimize search performance.
- **Asynchronous Mode**: For advanced users, the application supports asynchronous search operations, which can be useful for large-scale or delayed result retrieval.

## Main Functions Description

### `search_videos`

This is the core function of the application, responsible for performing video searches using the Google Videos API via SerpAPI. It accepts a variety of parameters to customize the search:

- **`q`**: The search query string, supporting advanced syntax for refined searches.
- **`location`**: Specifies the geographic location for the search, enhancing relevance based on user location.
- **`uule`**: An encoded geographic location, mutually exclusive with `location`.
- **`google_domain`**: The Google domain to use for the search, defaulting to `google.com`.
- **`gl`**: Country code for the search, defaulting to `us`.
- **`hl`**: Language code for the search, defaulting to `en`.
- **`lr`**: Language restriction for the search results.
- **`tbs`**: Advanced search parameters for filtering by date or duration.
- **`safe`**: Safe search filter, with options for active or off.
- **`nfpr`**: Option to exclude spelling correction results.
- **`filter`**: Result filtering toggle.
- **`start`**: Pagination offset for results.
- **`num`**: Number of results to return, ranging from 10 to 100.
- **`device`**: Device type for the search, defaulting to `desktop`.
- **`no_cache`**: Toggle for disabling cache.
- **`async_mode`**: Toggle for asynchronous result retrieval.

The function constructs a request payload with the provided parameters, sends a request to the SerpAPI, and returns the structured JSON response containing video search results.

---

This README provides a comprehensive overview of the Aigeon AI Google Videos API, detailing its capabilities and the flexibility it offers for video search operations. The application is designed to be a powerful tool for developers and users seeking to harness the power of Google's video search capabilities in a customizable and efficient manner.
```