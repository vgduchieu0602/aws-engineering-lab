# Lesson 01 — Server, Client & Data Center

## Core concepts
- Client: a program or device requesting a service.
- Server: a program or system providing services; a role rather than a physical form factor.
- Physical server: hardware providing CPU, RAM, persistent storage and networking.
- Data center: a physical facility housing computing, storage and networking equipment, supported by power, cooling, physical security and monitoring.

## Client–server model
```mermaid
flowchart LR
    C[Client] -->|Request| S[Server]
    S -->|Response| C
```

## Resource management
| Resource | Purpose |
|---|---|
| CPU | Execute instructions |
| RAM | Working memory |
| SSD/HDD | Persistent storage |
| Network interface | Network communication |
| OS | Manage hardware and processes |

## Engineering principles
- Capacity is not availability.
- Redundancy reduces dependency on individual components.
- A single point of failure can interrupt the entire service.
- High CPU utilization is a signal to investigate, not automatic justification for scaling.
- Troubleshooting: observe, identify, investigate, optimize, measure.
- Backup supports recovery; it does not by itself ensure availability.

## Practical lab (local, no AWS charges)
1. Run `node -e "require('node:http').createServer((req,res)=>res.end('OK')).listen(3000,'127.0.0.1')"`.
2. In another terminal run `curl.exe http://127.0.0.1:3000` (Windows) or `curl http://127.0.0.1:3000` (Linux/macOS).
3. Verify the response is `OK`.
4. Stop the server with Ctrl+C and repeat the request. Observe the connection failure.
5. Record the commands and actual results in `labs/01-local-server.md`.

## Acceptance criteria
- Explain the client and server roles.
- Distinguish physical server from data center.
- Explain why a single server does not guarantee availability.
- Demonstrate successful and failed local requests.
