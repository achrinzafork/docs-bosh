# Docker

The `docker` cpi can be used with Docker.

## Concepts

The following table maps BOSH concepts to their respective IaaS concept.

| BOSH              | Docker                                                                                    |
|-------------------|-------------------------------------------------------------------------------------------|
| Availability Zone | Ignored.                                                                                  |
| Virtual Machine   | Container                                                                                 |
| Network Subnet    | [Bridge network](https://docs.docker.com/engine/network/drivers/bridge/)                  |
| Virtual IP        | [Static External IP](https://cloud.google.com/compute/docs/ip-addresses/#reservedaddress) |
| Persistent Disk   |                                                                                           |
| Disk Snapshot     | Not implemented.                                                                          |
| Stemcell          | OCI-commpliant images                                                                     |
| Agent Settings    |                                                                                           |

## Feature Support

The following sections describe some specific BOSH features supported by the
CPI.

### Network

The CPI does not support multiple NICs being attached to a VM.

| Network Type | Support       |
|--------------|---------------|
| Manual       | Supported     |
| Dynamic      | Supported     |
| VIP          | Not Supported |

### Miscellaneous

| Feature                           | Support       |
|-----------------------------------|---------------|
| Multi-CPI                         | Not Supported |
| Native Disk Resize                | Not Supported |
| Native Disk Update                | Not Supported |
| Generic VM Resource Configuration | Not Supported |
