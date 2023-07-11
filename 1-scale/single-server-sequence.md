```mermaid

sequenceDiagram
    participant User 
    participant DNS
    participant Web Server
    
    User -->> DNS: api.mysite.com
    DNS ->> User: 15.124.123.53
    User -->> Web Server: 15.124.123.53
    Web Server ->> User: 15.124.123.53
    
    
```