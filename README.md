# 🧠 Polygon Miden Node Setup Guide (Beginner-Friendly)

> A straightforward, step-by-step guide to run the **Polygon Miden Node** on a VPS (Linux Ubuntu).  
> Designed for beginners with minimal technical knowledge — just follow along!

---

## ✅ Requirements

| Item              | Description                                                         |
|-------------------|---------------------------------------------------------------------|
| VPS               | Minimum: 4 vCPU, 16GB RAM, 100+ GB SSD (Ubuntu 20.04 or 22.04)      |
| SSH Client        | For accessing your VPS (PuTTY for Windows, Terminal for Mac/Linux)  |
| Rust              | Version 1.82 or higher                                               |

---

## 🖥 Recommended VPS Providers

| Provider   | Recommended Plan         | Link                        |
|------------|--------------------------|-----------------------------|
| Contabo    | VPS S (16 GB RAM)        | https://contabo.com         |
| Hetzner    | CPX21 or higher          | https://hetzner.com         |
| Vultr      | High Performance Plan    | https://www.vultr.com       |

---

## 🔐 Step 1: Connect to Your VPS

### 🪟 Windows Users
1. Download & install **[PuTTY](https://www.putty.org/)**.
2. Enter your VPS IP in "Host Name".
3. Login with:
   - Username: `root`
   - Password: (Paste by right-clicking)

### 🍎 Mac/Linux Users
Open your Terminal and connect:
```bash
ssh root@YOUR_VPS_IP
```
> Replace `YOUR_VPS_IP` with the IP address provided by your VPS provider.

---

## ⚙️ Step 2: Install Rust

Ensure you have Rust installed (version 1.82 or higher):

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

After installation, restart your shell or run:

```bash
source $HOME/.cargo/env
```

Verify Rust installation:

```bash
rustc --version
```

---

## 📦 Step 3: Install Miden Client

Install the Miden client with the concurrent feature:

```bash
cargo install miden-cli --features concurrent
```

This will install the `miden` binary at `~/.cargo/bin/miden`.

---

## 🛠 Step 4: Initialize Miden Client

Initialize the Miden client configuration:

```bash
miden init
```

This will create a `miden-client.toml` file in your current directory.

---

## 🚀 Step 5: Run the Miden Client

Start the Miden client:

```bash
miden
```

The client will connect to the local Miden node and start processing.

---

## 🧪 Step 6: Verify Node Is Running

Check if the Miden client is running properly by observing the logs:

```bash
miden
```

If everything is set up correctly, you should see logs indicating that the client is connected and operating.

---

## 🛑 Bonus Commands

To stop the Miden client, simply press `Ctrl + C` in the terminal where it's running.

To update the Miden client to the latest version:

```bash
cargo install miden-cli --features concurrent --force
```

---

## 🔗 Useful Links

- 🔧 [Miden Node GitHub Repository](https://github.com/0xPolygonMiden/miden-node)
- 📖 [Miden Documentation](https://0xpolygonmiden.github.io/miden-docs/)
- 💬 [Polygon Discord](https://discord.gg/polygon)

---

## 🙋 Need Help?

If you’re stuck, ask for help in the [Polygon Discord](https://discord.gg/polygon).

---

## 📢 Disclaimer

> This guide is for educational purposes only. Guide By Zeeshan Khan (ZK)
