<p align="center">
  <img src="./images/my_radkit_dev_journey.png" style="width: 200px;" alt="Cisco RADKit" /></br>
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
| 🔗 **Integration / Backend Developer** | Authenticate machine-to-machine, generate tokens/OTPs, and call RADKit HTTP endpoints directly | [Access API Examples](#access-api-examples) |

---

## 🐍 Client API Examples
Covers the `radkit_client` Python SDK: the primary library used to connect to RADKit and interact with managed devices.

| Code notebook | What it covers |
|---|---|
| 🔗 [**How to authenticate**](./Client%20API%20examples/01-authentication-connection.ipynb) | The different ways to authenticate and establish a connection: SSO login, certificate login, access token login, direct service connections, and HTTP proxy configuration |
| 🔗 [**How to connect to my RADKit service**](./Client%20API%20examples/02-connect-to-my-service.ipynb) | How to plugin into your RADKit service |
| 🔗 [**How to structure and manage scripts**](./Client%20API%20examples/03-structure-manage-scripts.ipynb) | How to correctly manage the `Client` lifecycle in scripts, Jupyter Notebooks, and FastAPI apps |
| 🔗 [**How to execute commands on devices**](./Client%20API%20examples/04-execute-commands-on-devices.ipynb) | Inspect inventory, filter target devices, run commands on single or multiple devices, and handle execution results and partial failures. |
| 🔗 [**How to parse command outputs with Genie**](./Client%20API%20examples/05-parse-outputs-with-genie.ipynb) | Parsing outputs with Genie parsers |
| 🔗 [**How to transfer files**](./Client%20API%20examples/06-file-transfer.ipynb/) | Transferring files to and from devices using SCP/SFTP |
| 🔗 [**How to use SNMP and NETCONF**](./Client%20API%20examples/07-snmp-and-netconf.ipynb) | Performing SNMP walk and get operations, and executing NETCONF/YANG calls against devices |

---

## ⚙️ Control API Examples
Covers the `ControlAPI`: the administrative plane for managing the RADKit service itself: users, devices, labels, roles, and admins.

| Code notebook | What it covers |
|---|---|
| 🔗 [**How to manage users**](./Control%20API%20examples/01-manage-users.ipynb) | Creating, listing, fetching, and deleting remote users |
| 🔗 [**How to manage devices**](./Control%20API%20examples/02-manage-devices.ipynb) | Creating, listing, updating, and deleting devices; importing from CSV and JSON; using `DeviceType` enums instead of raw strings |
| 🔗 [**How to manage labels**](Control%20API%20examples/) | Creating and deleting labels; assigning labels to devices and users for RBAC scoping |
| 🔗 [**How to manage admins**](Control%20API%20examples/) | Listing, creating, and deleting admin accounts on the service |
| 🔗 [**How to manage roles**](Control%20API%20examples/) | Listing, creating, and assigning custom roles; deleting roles |
| 🔗 [**How to check on your service**](Control%20API%20examples/) | Checking your service status and other settings |

---

## 🔐 Access API Examples

Covers the RADKit HTTP REST API — used for machine-to-machine authentication, token lifecycle management, OTP generation, and direct HTTP integration.

| Code snippet | What it covers |
|---|---|
| 🔗 [**How to handle errors and follow API conventions**](Access%20API%20examples/) | Handling HTTP 4xx/5xx responses, correct use of `Authorization: Bearer` and `Content-Type: application/json` headers, and base URL configuration |
| 🔗 [**How to authenticate and manage tokens**](Access%20API%20examples/) | OAuth 2.0 client credentials grant, generating client credentials and API tokens via the SDK, calling `/oauth2/token` and `/auth/token` endpoints, token revocation, OpenID configuration discovery, and secure credential handling |
| 🔗 [**How to check service status**](Access%20API%20examples/) | Querying `GET /public/admin/service/status/:service_id` to check whether a service is active and online |
| 🔗 [**How to generate OTPs**](Access%20API%20examples/) | Generating one-time passwords for service enrollment via `POST /public/otp/certificate`, handling OTP errors, and using the OTP inside the enrollment flow |
| 🔗 [**How to automate multi-tenant access**](Access%20API%20examples/) | Using email alias syntax (`user+tag@cisco.com`) to create per-customer identities, generating scoped API tokens with `endpoint_id`, and building auditable multi-tenant access patterns |
