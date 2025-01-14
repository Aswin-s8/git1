```mermaid
sequenceDiagram
    participant U as User
    participant B as Browser
    participant P as Page
    participant S as Server

    U->>B: Navigates to https://studies.cs.helsinki.fi/exampleapp/spa
    B->>S: Sends request for the SPA page
    S->>B: Responds with the SPA page
    B->>P: Renders the SPA page
    P->>S: Sends request for notes data (AJAX or Fetch)
    S->>P: Responds with notes data
    P->>U: Displays notes on the page
