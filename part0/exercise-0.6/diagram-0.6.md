sequenceDiagram
    participant Browser as Browser
    participant Server as Server

    Browser->>Server: Sends request to create new note (POST /notes)
    Server->>Server: Process and save note data
    Server-->>Browser: Sends confirmation response
    Browser-->>Browser: Updates UI with new note
