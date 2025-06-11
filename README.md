# reviewscraper
A simple web scraper tool created to scrape all product reviews off of Amazon India's web pages.

This tool uses urllib.request from the urllib library to download the product page (HTML) using the URL mentioned in url_list_temp.txt file, and uses BeautifulSoup library to navigate through the HTML string, using links included in anchor tags to go to the next page and so on.

The url_list_temp.txt file only contains one URL currently, and that link gives a 404 error. Users are advised to update those links with new ones.

At the time of writing this program, Amazon India did have a server cutoff problem. To tackle this, the program asks (through STDIN) whether you're resuming after a server cutoff. If yes, then it starts scraping from the end of the last completely scraped page.

The HTML architecture of Amazon product pages must have likely changed since the time of writing this program. However, the code can be updated to navigate the new HTML architecture. This can be easily done by inspecting the Amazon pages and finding which anchor tags correspond to the "next page" buttons.
