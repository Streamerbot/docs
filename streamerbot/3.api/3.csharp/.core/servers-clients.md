---
title: Servers & Clients
description: C# methods for Streamer.bot servers and clients
---

## Websocket Server

### `WebsocketBroadcastString`
Send a custom event over the Streamer.bot WebSocket server
:csharp-method{name=WebsocketBroadcastString}

### `WebsocketBroadcastJson`
Send a custom JSON event over the Streamer.bot WebSocket server
:csharp-method{name=WebsocketBroadcastJson}

## Websocket Clients
```csharp
void WebsocketConnect(int connection = 0);
void WebsocketDisconnect(int connection = 0);
```

```csharp
bool WebsocketIsConnected(int connection = 0);
```

```csharp
void WebsocketSend(string data, int connection = 0);
void WebsocketSend(byte[] data, int connection = 0);
```

## Custom Websocket Servers
```csharp
void WebsocketCustomServerStart(int connection = 0);
void WebsocketCustomServerStop(int connection = 0);
```

```csharp
bool WebsocketCustomServerIsListening(int connection = 0);
```

```csharp
void WebsocketCustomServerCloseAllSessions(int connection = 0);
void WebsocketCustomServerCloseSession(string sessionId, int connection = 0);
void WebsocketCustomServerBroadcast(string data, string sessionId, int connection = 0);
```

```csharp
int WebsocketCustomServerGetConnectionByName(string name);
```

## UDP Broadcast
```csharp
int BroadcastUdp(int port, object data);
```