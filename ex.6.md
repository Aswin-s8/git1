```mermaid
sequenceDiagram
    participant U as User
    participant B as Browser
    participant P as Page
    participant S as Server

    U->>P: Enters text into the note input field
    U->>P: Clicks "Save" button
    P->>S: Sends new note data to the server (via AJAX or Fetch)
    S->>P: Saves the note and responds with a confirmation
    P->>U: Displays confirmation (e.g., "Note saved successfully")
    P->>S: Request for updated notes list
    S->>P: Responds with updated notes data
    P->>U: Displays updated notes list
    U->>B: Pushes answers to GitHub
    B->>S: Sends commit request to GitHub
    S->>B: Confirms successful commit
    U->>B: Marks exercises as done in the submission system
    B->>S: Sends request to mark as done
    S->>B: Confirms exercises marked as done
