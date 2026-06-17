<div align="center">
  <img src="banner.svg" alt="xClans Banner" width="100%">

  <h1>xClans</h1>
  <p>The Ultimate High-Performance, Fully Customizable Clan System for Modern Minecraft Networks</p>

  <img src="https://img.shields.io/badge/Platform-Spigot%20%7C%20Paper-2077B4?style=for-the-badge&logo=minecraft" alt="Platform">
  <img src="https://img.shields.io/badge/Java-17%20%2B-ED8B00?style=for-the-badge&logo=openjdk" alt="Java Version">
  <img src="https://img.shields.io/badge/Version-1.0.0--RELEASE-007ACC?style=for-the-badge" alt="Version">
  <img src="https://img.shields.io/badge/Optimization-Ultra%20%7C%20Async-4CAF50?style=for-the-badge" alt="Optimization">
</div>

---

## 📌 Overview

**xClans** is a premium, enterprise-grade clan management solution engineered specifically for high-population Paper/Spigot networks and competitive OPS modes. Designed from the ground up for absolute optimization, xClans offloads intensive data operations and chat rendering onto asynchronous threads, ensuring absolute flawless server performance (20.0 TPS) even during peak gameplay.

Unlike traditional legacy clan plugins, **xClans features a 100% dynamic string engine supporting custom legacy colors (`&`) and precise HEX gradients (`&#HEX`) natively**, giving your VIP players ultimate creative freedom without risking configuration corruption.

---

## ⚡ Key Features

* **Dynamic Custom Rank System (`/c rank`):** Leaders can assign fully colorized, bespoke text-based ranks (e.g., `&#1488CC&lO&#1A73C6&lw&#205DBF&ln&#2548B9&le&#2B32B2&lr`) that render exclusively inside the internal clan chat.
* **Asynchronous Color Parsing Engine:** Custom legacy and `&#RRGGBB` hex strings are efficiently stripped down for length validation checks and accurately compiled for native display.
* **Total Chat Isolation Architecture:** Seamless integration with standard networks. Global chat displays pure clan names while dynamically preserving third-party tags (e.g., **LuckPerms Group Prefixes via Vault**), whereas internal chat (`/cc`) handles specialized rank structures.
* **Strict Owner/Leader Safeguards:** High-risk economic and tactical parameters like inventory serialization (`/c kitcreate`) and base management (`/c createhome`) are restricted strictly to the absolute clan owner.
* **Mathematical Leaderboard System (`/c top`):** A robust dynamic sorting engine that processes and displays TOP 10 statistics with zero-leak KDR formatting fixed to exactly 2 decimal places.

---

## 🛠️ Configuration (`config.yml`)

The plugin features a 100% editable metadata structural model. Zero hardcoded placeholders. Zero forced emojis. Pure clean typography.

```yaml
# xClans Core System Configuration
messages:
  no-clan: "&cError: You must be in a clan to use this command."
  no-permission: "&cError: Only the ultimate Clan Leader can use this command."
  clan-exists: "&cError: A clan with this name already exists."
  invalid-syntax: "&cError: Invalid Usage!"
  home-teleporting: "&aTeleporting to clan home in 3 seconds... Do not move."
  home-cancelled: "&cTeleportation cancelled because you moved or took damage."
  kit-claimed: "&aSuccess: You have claimed your clan kit."
  kit-created: "&aSuccess: Clan kit has been successfully updated from your inventory."
  home-created: "&aSuccess: Clan home location has been updated."

chat-formats:
  # Seamless integration with Vault / LuckPerms prefixes
  global-chat: "{LUCKPERMS_PREFIX} {CLAN_TAG} &f{PLAYER_NAME}&8: &7{MESSAGE}"
  tab-list: "{CLAN_TAG} &f{PLAYER_NAME}"
  clan-chat: "&b[CLAN CHAT] {RANK_PREFIX} &f{PLAYER_NAME}&8: &b{MESSAGE}"

ranks:
  default-member: "&7[Member]"
