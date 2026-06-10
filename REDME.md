## nexuse-haproxy

This setup uses **HAProxy** to route traffic to three separate **Nexus Repository Manager** instances based on the type of repository:

- Maven artifacts → Nexus 1
- NuGet packages → Nexus 2
- Other repositories → Nexus 3

HAProxy acts as a single entry point and distributes traffic to the appropriate backend service based on the exposed frontend ports.

---

## Components

### Nexus Repositories

| Service | Purpose | Port |
|--------|--------|------|
| Nexus1 | Maven repositories | 8081 |
| Nexus2 | NuGet repositories | 8082 |
| Nexus3 | Other formats      | 8083 |

### HAProxy

- Acts as reverse proxy
- Routes traffic based on frontend port
- Provides unified access layer

---
