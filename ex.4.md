```mermaid
sequenceDiagram
    participant U as User
    participant P as Page
    participant S as Server

    U->>P: Enters text into the text field
    U->>P: Clicks "Save" button
    P->>S: Sends new note data to the server
    S->>P: Saves the note and responds with confirmation
    P->>U: Displays confirmation (e.g., "Note saved successfully")
