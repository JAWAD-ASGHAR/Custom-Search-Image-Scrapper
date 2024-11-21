
# Google Custom Search Image Scraper

This project is a simple Node.js script designed to fetch image URLs for a list of products using the Google Custom Search API. It reads product data from a JSON file, queries the API to find an image for each product, and then saves the updated product data with image URLs to a new JSON file.

---

## Features
- Reads product data from a local JSON file.
- Uses the Google Custom Search API to fetch image URLs.
- Handles API responses and errors gracefully.
- Outputs updated product data to a new JSON file.

---

## Prerequisites
- Node.js installed on your machine.
- A Google Cloud Project with the Custom Search API enabled.
- API Key and Search Engine ID (CX) configured in your environment variables.

---

## Installation
1. Clone the repository
   ```bash
   git clone https://github.com/JAWAD-ASGHAR/Custom-Search-Image-Scrapper
   cd Custom-Search-Image-Scrapper
   ```

2. Install dependencies:
   ```bash
   npm install axios
   ```

3. Set up environment variables:
   Create a `.env` file in the project root and add:
   ```env
   GOOGLE_CUSTOM_SEARCH_API_KEY=your_api_key
   GOOGLE_CUSTOM_SEARCH_CX=your_search_engine_id
   ```

---

## Usage
1. Place your product data in a file named `products.json` inside a `Data` directory. The file should look like this:
   ```json
   [
     { "name": "Product 1", "price": 100 },
     { "name": "Product 2", "price": 200 }
   ]
   ```

2. Run the script:
   ```bash
   node script.js
   ```

3. Check the output file:
   The updated product data with image URLs will be saved as `products_with_images.json` in the `Data` directory.

---

## Example Output
Input (`products.json`):
```json
[
  { "name": "Laptop", "price": 1200 },
  { "name": "Smartphone", "price": 800 }
]
```

Output (`products_with_images.json`):
```json
[
  { "name": "Laptop", "price": 1200, "imageUrl": "https://example.com/laptop.jpg" },
  { "name": "Smartphone", "price": 800, "imageUrl": "https://example.com/smartphone.jpg" }
]
```

---

## Notes
- Ensure you have sufficient quota for the Google Custom Search API.
- API key and CX must remain confidential to avoid misuse.

---

## License
This project is licensed under the MIT License. Feel free to use and modify it as needed.
