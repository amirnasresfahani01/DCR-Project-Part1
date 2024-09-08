HTML File Parser and Database Search Tool

Overview

This project is a Python tool to:

Parse HTML files and extract their text content.
Store the content in a MySQL database.
Allow users to search the database for files by their name or content.

Requirements
Python 3.6 or higher
MySQL Server
Python packages: mysql-connector-python, lxml, rich
Installation
Install Python Packages
pip install mysql-connector-python lxml rich

create a table named wiki

CREATE TABLE wiki (
    id INT AUTO_INCREMENT PRIMARY KEY,
    filename VARCHAR(255),
    file_size BIGINT,
    full_path TEXT,
    last_modified DATETIME,
    content LONGTEXT
);

Update Database Configuration Update the database connection details in the script if needed:

connection = mysql.connector.connect(
    host="127.0.0.1",
    user="root",
    password="my password",
    database=""
)

Usage

Insert Data into Database

To parse HTML files from a directory and insert them into the database:

directory_path = r'D:\DCRB with index'
parse_and_insert_data(directory_path)

Run the Search Tool
Start the search tool by running the script:

python.py

Search Interface
Enter a search term to find files by their name or content.
Type exit to quit the tool.

Functions

parse_html_file(file_path): Extracts text from an HTML file.
create_indexes(connection): Creates indexes in the database for faster search.
parse_directory(directory_path, connection): Parses HTML files in a directory and inserts them into the database.
parse_and_insert_data(directory_path): Combines parsing and insertion process.
search_files_in_database(search_query, connection): Searches the database for files matching the search query.
display_search_results(search_query, filename_results, content_results): Shows search results in a table.
highlight_search_query(text, query): Highlights search terms in the text.

Contact

For any questions or issues, contact [amir.nasresfahani01@universitadipavia.it]. or you cna ask me on my linkedin : www.linkedin.com/in/amir-nasr-esfahani-584b90142
