
sequenceDiagram
    participant browser;
    participant server;


    browser->server: POST https://studies.cs.helsinki.fi/exampleapp/new_note;
    activate server;
    server-->browser: GET notes HTML File;
    deactivate server;
    browser-->server: GET https://studies.cs.helsinki.fi/exampleapp/main.css;
    activate server
    server-->browser: The main.css File with the styles;
    deactivate server;
    browser-->server: GET https://studies.cs.helsinki.fi/exampleapp/main.js;
    activate server
    server-->browser: The main.js File with the rendering functions;
    deactivate server
    browser-->server: GET https://studies.cs.helsinki.fi/exampleapp/data.json;
    activate server
    server-->browser: The data.json file with the current notes including the new note sent;
    deactivate server
