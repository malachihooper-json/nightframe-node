# Mesh Networking

Plug-and-play P2P mesh network library for distributed computation.

## Quick Start

```bash
dotnet build
```

```csharp
using MeshNetworking;

var node = new NetworkCore(nodeId: "node-1");
await node.StartAsync();
await node.JoinMeshAsync("mesh-network");
node.OnMessageReceived += (sender, msg) => { /* handle */ };
await node.BroadcastAsync(new Message { Type = "work", Payload = data });
```

## Components

| File | Purpose |
|------|---------|
| NetworkCore.cs | Core mesh logic with connection management |
| NeuralNetworkMesh.cs | Distributed neural inference |
| NodeRegistry.cs | Node discovery and health tracking |
| NodePersistence.cs | State persistence and recovery |
| NodeReplicationManager.cs | State replication and consistency |
| TravelingNode.cs | Mobile node capabilities |
| GossipProtocol.cs | Epidemic-style message propagation |
| CollectiveCapabilities.cs | Shared capability discovery |
| NetworkAssessment.cs | Network health assessment |
| NetworkTroubleshooter.cs | Automatic troubleshooting |

## Features

- Automatic peer discovery on local network
- Gossip protocol for state synchronization
- Node health monitoring and failure detection
- Persistent node identity across restarts

## Requirements

- .NET 8.0+
- Network access for peer discovery
