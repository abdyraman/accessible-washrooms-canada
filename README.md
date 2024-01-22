# acceessible-washrooms-canada
This Python script is using the Geoapify API to obtain information about accessible washrooms in different cities and then converting the obtained data into a pandas DataFrame.


1. **Importing Dependencies:**
   - The script imports necessary libraries, including `requests` for making HTTP requests, `json` for handling JSON data, and `pandas` for data manipulation.
   - It also imports an API key (`geoapify_key`) from a configuration file (`config.py`).

2. **Setting Parameters:**
   - Parameters like language (`lang`) and result limit (`limit`) are defined.

3. **Defining City Codes:**
   - Geoapify place codes for different cities are stored in the `city_name` list.

4. **Initializing Empty Lists:**
   - Lists are created to store information about districts, addresses, postcodes, latitudes, longitudes, names, and cities.

5. **Looping Through Cities:**
   - A loop iterates through each city code in `city_name`.
   - For each city, it constructs a Geoapify API URL, sends a request, and retrieves information about accessible washrooms.
   - Relevant details (district, address, postcode, latitude, longitude, name, city) for each washroom are extracted and appended to the corresponding lists.

6. **Creating a DataFrame:**
   - The retrieved information is organized into a dictionary (`washrooms`).
   - A pandas DataFrame (`washrooms_df`) is created from this dictionary.

7. **Saving to CSV:**
   - The DataFrame is saved to a CSV file named "accessible_washrooms_datasets_canada.csv".
   - The `index=False` parameter ensures that the DataFrame's index is not included in the CSV file.

In summary, the script fetches data about accessible washrooms for different cities using the Geoapify API, processes the data, and stores it in a pandas DataFrame. The DataFrame is then saved to a CSV file for further analysis or use.