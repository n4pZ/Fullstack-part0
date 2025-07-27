# Fullstack-part0

## Exercise 0.4
```mermaid
sequenceDiagram
    Client->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note with user input
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate Server
    Server-->>Client: html html file
    deactivate Server
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate Server
    Server-->>Client: css file
    deactivate Server
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    activate Server
    Server-->>Client: js file
    deactivate Server
    Note right of Client: The js file creates a list and adds the userinput
    Client->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate Server
    Server-->>Client: [{ "content": "HTML is easy", "date": "2023-1-1" }, ... ]
    deactivate Server
    Note right of Client: the browser executes the callback function and renders the notes to the list
```

## Exercise 0.5
```mermaid
sequenceDiagram
    client->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    server-->>client: HTML document
    deactivate server

    client->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>client: the css file
    deactivate server

    client->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    activate server
    server-->>client: the JavaScript file
    deactivate server

    Note right of client: The client starts executing the JavaScript code that fetches the JSON from the server

    client->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>client: [{ "content": "HTML is easy", "date": "2023-1-1" }, ... ]
    deactivate server

    Note right of client: The client executes the callback function that renders the notes
```

## Exercise 0.6
```mermaid
sequenceDiagram
    client->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    server-->>client: response in json format that note was created
```
