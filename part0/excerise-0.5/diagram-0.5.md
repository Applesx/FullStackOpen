graph TD
    A[User accesses URL: https://studies.cs.helsinki.fi/exampleapp/spa] --> B[Browser makes HTTP GET request to the server]
    B --> C[Server responds with HTML, CSS, and JS files]
    C --> D[Browser loads the page and initializes the JS application]
    D --> E[JS makes an API request to fetch notes ]
    E --> F[Server responds with JSON data containing notes]
    F --> G[JS dynamically updates the DOM to display the notes]
