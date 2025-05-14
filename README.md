# Subnet CDN Node

**Subnet CDN Node** is a decentralized content delivery node built on top of the Subnet overlay network. It enables fast and secure distribution of static content (images, videos, files, etc.) by routing user requests to the nearest available provider node. Designed for high-performance and fault-tolerant web3 infrastructure, it integrates seamlessly with container runtimes and decentralized storage backends.

---

## Overview

Traditional CDNs rely on centralized data centers. Subnet CDN Node replaces this model with a peer-to-peer network of nodes that cache and serve content locally, reducing latency and improving resilience.

This node can be embedded in decentralized apps (DApps), blockchain-based marketplaces, or any system needing reliable content delivery without relying on centralized providers.

---

## Features

* **Low-Latency Delivery**: Serve files from the closest node using the Subnet overlay network.
* **Decentralized Architecture**: Peer-to-peer data propagation using `libp2p`.
* **Content Storage**: Store and retrieve content locally or via IPFS.
* **Access Control**: Integrated with Subnet Node's firewall and security layers.
* **Dynamic Discovery**: Automatically connects to other CDN nodes in the network.
* **Container-Friendly**: Easily deployable using Docker or Containerd.

---

## Technology Stack

* Golang — core implementation
* libp2p — P2P overlay network
* Containerd / Docker — runtime container management
* IPFS (optional) — decentralized file storage backend
* Subnet Node Infrastructure — for networking and access control

---

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-org/subnet-cdn-node.git
cd subnet-cdn-node
```

### 2. Configuration

Create a `.env` file or update environment variables:

```env
NODE_ID=node-abc123
STORAGE_PATH=/data/cdn
PORT=8080
USE_IPFS=true
IPFS_API=http://127.0.0.1:5001
```

### 3. Run with Docker Compose

```bash
docker-compose up -d
```

Or run directly with Go:

```bash
go run main.go
```

---

## API Endpoints

| Method | Endpoint         | Description                     |
| ------ | ---------------- | ------------------------------- |
| GET    | `/health`        | Check node status               |
| GET    | `/content/{cid}` | Retrieve content by CID or hash |
| POST   | `/upload`        | Upload and store new content    |

---

## Use Cases

* Serve decentralized frontend assets and media
* Distribute large AI models across nodes
* Caching layer for DApps and Web3 storage
* Regional CDN edge nodes for latency optimization

---

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

---

## Contributing

We welcome contributions! Please open issues or pull requests to help improve the project.

---

## Contact

For support or business inquiries, reach out to: **[team@yourproject.org](mailto:team@yourproject.org)**
