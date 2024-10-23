```mermaid
sequenceDiagram
    participant Browser
    participant Server

    Browser -->> Server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    activate Server
    Server -->> Browser: HTML code (minimal)
    deactivate Server

    Browser -->> Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate Server
    Server -->> Browser: the CSS file
    deactivate Server

    Browser -->> Server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    activate Server
    Server -->> Browser: the JavaScript file
    deactivate Server

    Browser -->> Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate Server
    Server -->> Browser: JSON data with notes
    deactivate Server

    Note over Browser: The SPA dynamically updates the view without full page reload
