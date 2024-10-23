```mermaid
sequenceDiagram
    participant Browser
    participant Server


    Browser -->>Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate Server
    Server -->>Browser: HTML code
    deactivate Server

    Browser -->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate Server
    Server -->> Browser: the CSS file
    deactivate Server

    Browser -->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    activate Server
    Server -->> Browser: the JavaScript file
    deactivate Server

    Browser -->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate Server
    Server -->> Browser: [ { "content": "hj hh bhjbhy","date": "2024-10-21T11:00:26.412Z" },...]
    deactivate Server

