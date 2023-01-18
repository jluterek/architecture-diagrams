# HTML Rendering Approaches

## Static Rendering

 ```mermaid
sequenceDiagram
    participant Client
    participant Server
    participant Build
    Build->>+Build: Render HTML
    Build->>+Server: Transfer HTML Files
    Client->>+Server: Request URL
    Server-->>-Client: Serve HTML
    Client->>+Client: Display HTML
```


## Server-Side Rendering

 ```mermaid
sequenceDiagram
    participant Client
    participant Server
    Client->>+Server: Request URL
    Server->>Server: Render HTML
    Server-->>-Client: Serve HTML
    Client->>+Client: Display HTML
```


## Client-Side Rendering

 ```mermaid
sequenceDiagram
    participant Client
    participant Server
    Client->>+Server: Request URL
    Server-->>-Client: Serve Application
    Client->>Client: Parse Application
    Client->>+Server: Request JavaScript
    Server-->>-Client: Serve JavaScript
    Client->>Client: Execute JavaScript
    Client->>+Server: Request JSON
    Server-->>-Client: Serve JSON
    Client->>+Client: Render HTML
    Client->>+Client: Display HTML
```