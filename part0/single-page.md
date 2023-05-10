```mermaid
sequenceDiagram
  participant browser
  participant server
    
  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
  activate server
  server->>browser: the html file
  deactivate server
  
  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
  activate server
  server->>browser: the css file
  deactivate server
  
  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
  activate server
  server->>browser: the js file
  deactivate server
  
  note right of browser: javascript fetches json data
  
  broswer->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
  activate server
  server->>browser: the json data
  deactivate server
  
  note right of browser: javascript finishes rendering json data
```
