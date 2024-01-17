sequenceDiagram
    participant browser
    participant server

    browser-->server: GET https://studies.cs.helsinki.fi/exampleapp/spa;
    activate server
    server-->browser: HTML File with the page details
    deactivate server
    browser-->server: GET https://studies.cs.helsinki.fi/exampleapp/main.css;
    activate server
    server-->browser: The css file with the classes style
    deactivate server
    browser-->server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    activate server
    server-->browser: The spa.js file containing all the SPA logic
    deactivate server
    browser-->server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->browser: The data.json file containing current notes
    deactivate server