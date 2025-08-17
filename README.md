# Frax

**Frax** is a dynamic server communication system for Roblox.  
It allows you to **send and receive structured objects** across servers using Roblox’s [`MessageService`](https://create.roblox.com/docs/reference/engine/classes/MessageService).  

Instead of just passing raw strings, Frax serializes objects so your servers can talk in a richer and more flexible way ✨  

---

## ✨ Features
- 🔗 **Dynamic Channels** – Create and manage communication channels on the fly.  
- 📡 **Cross-Server Object Messaging** – Pass tables and structured data, not just strings.  
- ⚡ **Adaptive System** – Automatically adjusts to your server’s needs.  
- 🛠️ **Simple API** – Clean, developer-friendly interface.  

---

## 📦 Installation
Clone the repo or drop the ModuleScript into your project:

```sh
git clone https://github.com/yourusername/frax.git
````

---

## 🚀 Usage

Here’s a simple example of **sending objects** with Frax:

```lua
local Frax = require(path.to.frax)

-- Subscribe to a channel
Frax:Subscribe("PlayerData", function(data)
	print("Got player data:", data.UserId, data.Level)
end)

-- Publish an object (table)
Frax:Publish("PlayerData", {
	UserId = 123456,
	Level = 42,
	Inventory = { "Sword", "Shield" }
})
```

---

## 📖 API Reference

### `Frax:Subscribe(channelName: string, callback: function)`

Subscribe to a channel. The callback receives full object data (tables, strings, numbers, etc).

### `Frax:Publish(channelName: string, message: any)`

Publish an object to a channel. Other servers subscribed will receive the full object.

### `Frax:Unsubscribe(channelName: string)`

Unsubscribes the current server from a channel.

---

## 🤝 Contributing

Frax is currently moving to Rojo, so this repository will be more than a DynamicRequire.index! (Be patient, I have many projects...)
When that's complete, contributions are welcome! Please open issues or submit PRs to help improve Frax.

---
