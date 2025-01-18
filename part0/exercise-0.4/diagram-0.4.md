sequenceDiagram
    participant Browser
    participant Server

    Browser->>Browser: User enters text into the text field
    Browser->>Browser: User clicks the "Save" button
    Browser->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate Server
    Server-->>Browser: Response with confirmation (success or failure)
    deactivate Server

    Note right of Browser: The browser updates the UI to display the new note
    Browser->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate Server
    Server-->>Browser: Returns the updated list of notes (including the new one)
    deactivate Server
    Browser->>Browser: The browser renders the updated list of notes
