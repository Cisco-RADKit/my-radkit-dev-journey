<p align="center">
  <img src="./images/my_radkit_dev_journey___.gif" alt="Cisco RADKit" style="width:400" /></br>
</p>

# 🚀 My RADKit Dev Journey

Welcome to the RADKit developer journey! This repository collects practical examples, patterns, and notes built up while learning and working with the RADKit platform.

RADKit exposes three distinct APIs, each targeting a different persona and use case. Depending on what you are trying to accomplish, you will want to explore one or more of the collections below.

---

## 🧭 Which collection is right for you?

| Persona | Goal | Collection |
|---|---|---|
| 🤖 **Network Automation Developer** | Write scripts or applications that run commands, collect data, or interact with devices through RADKit | [Client API Examples](#client-api-examples) |
| 🛠️ **Platform / IT Administrator** | Programmatically provision users, devices, labels, roles, and admins on a RADKit service | [Control API Examples](#control-api-examples) |

---

## 🐍 Client API Examples
Covers the `radkit_client` Python SDK: the primary library used to connect to RADKit and interact with managed devices.

| Code notebook | What it covers |
|---|---|
| 🔗 [**How to authenticate**](./Client%20API%20examples/01-authentication-connection.ipynb) | Authenticating and establishing a connection: SSO login, certificate login, access token login, direct service connections, and HTTP proxy configuration |
| 🔗 [**How to connect to my RADKit service**](./Client%20API%20examples/02-connect-to-my-service.ipynb) | Connecting and plugging into your RADKit service |
| 🔗 [**How to structure and manage scripts**](./Client%20API%20examples/03-structure-manage-scripts.ipynb) | Managing the `Client` lifecycle in scripts, Jupyter Notebooks, and FastAPI apps |
| 🔗 [**How to execute commands on devices**](./Client%20API%20examples/04-execute-commands-on-devices.ipynb) | Inspecting inventory, filtering target devices, running commands on single or multiple devices, and handling execution results and partial failures |
| 🔗 [**How to parse command outputs with Genie**](./Client%20API%20examples/05-parse-outputs-with-genie.ipynb) | Parsing outputs with Genie parsers |
| 🔗 [**How to transfer files**](./Client%20API%20examples/06-file-transfer.ipynb/) | Transferring files to and from devices using SCP/SFTP |
| 🔗 [**How to use SNMP and NETCONF**](./Client%20API%20examples/07-snmp-and-netconf.ipynb) | Performing SNMP walk and get operations, and executing NETCONF/YANG calls against devices |

---

## ⚙️ Control API Examples
Covers the `ControlAPI`: the administrative plane for managing the RADKit service itself: users, devices, labels, roles, and admins.

| Code notebook | What it covers |
|---|---|
| 🔗 [**How to manage users**](./Control%20API%20examples/01-manage-users.ipynb) | Creating, listing, fetching, updating and deleting remote users |
| 🔗 [**How to manage devices**](./Control%20API%20examples/02-manage-devices.ipynb) | Same, but for your devices |
| 🔗 [**How to manage labels**](./Control%20API%20examples/03-manage-labels.ipynb) | Managing your labels for remote users and devices when RBAC is enabled in your service |
| 🔗 [**How to manage admins**](./Control%20API%20examples/04-manage-admins.ipynb) | Listing, creating, and deleting admin accounts on the service |
| 🔗 [**How to manage roles**](./Control%20API%20examples/05-manage-roles.ipynb) | Managing your roles for admin users |

---