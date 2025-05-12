# NTUAFlix

NTUAFlix is a web-based movie discovery and metadata platform. The system enables users to search and explore movie information via a responsive web interface or through a RESTful API. Core functionalities include full-text movie search by title or cast, genre-based top-10 listings, and detailed metadata views for both movies and contributors. The backend is implemented in Python using Flask, with data persistence handled via a MySQL relational database. The front-end is served through Flask as well, supporting interaction through dynamically generated HTML pages. A command-line interface (CLI) written in Python is provided for programmatic interaction with the REST API.

## Installation

1. Clone the repository:
    
    ```bash
    git clone https://github.com/dimitraseferiadi/softeng
    cd softeng
    
    ```
    
2. Set up the backend and database:
    
    ```bash
    python setup.py
    
    ```
    
3. Run the front-end server:
    
    ```bash
    cd front-end
    python server.py
    
    ```
    

The application will be available at [http://127.0.0.1:5000](http://127.0.0.1:5000/).

## CLI Access

A command-line interface is provided via `se2305.py`. For global use on Windows, create a `.bat` file:

```
@echo off
python C:\temp\cli-client\se2305.py %*

```

Place it in `C:/Windows/System32` and run commands like:

```bash
se2305 movies --title "Interstellar" --format json

```

## API Functionality

The REST API supports:

- `/top10?genre=action` – Get top 10 movies by genre
- `/search?title=matrix` – Search by movie title
- `/search?person=nolan` – Search by contributor name
- `/movie/<id>` – Get full details of a movie
- `/person/<id>` – Get full details of a contributor

## Documentation
For complete technical specs and diagrams, refer to the included [SRS document](https://github.com/dimitraseferiadi/SoftEng11/blob/main/documentation/SRS_team5.pdf).
