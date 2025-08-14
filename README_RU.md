# 🌙 Shadow Ghost

> Децентрализованный P2P-мессенджер с упором на приватность и анонимность

---

<p align="center">
  <a href="https://www.rust-lang.org/">
    <img src="https://img.shields.io/badge/rust-%23000000.svg?style=for-the-badge&logo=rust&logoColor=white" alt="Rust">
  </a>
  <a href="https://flutter.dev">
    <img src="https://img.shields.io/badge/Flutter-%2302569B.svg?style=for-the-badge&logo=Flutter&logoColor=white" alt="Flutter">
  </a>
</p>
<p align="center">
  <a href="http://creativecommons.org/licenses/by-nc-sa/4.0/">
    <img src="https://img.shields.io/badge/Лицензия-CC%20BY--NC--SA%204.0-lightgrey.svg" alt="CC BY-NC-SA 4.0">
  </a>
</p>

---

##### [**README in English**](README.md)

## 📱 Описание

**Shadow Ghost** — это современный P2P-мессенджер, обеспечивающий полную приватность общения без использования центральных серверов. Все данные передаются напрямую между устройствами с применением сквозного шифрования.

### ✨ Ключевые особенности

- 🔒 **Полная приватность** — без серверов, логов и слежки
- 🌐 **P2P-соединения** — прямое взаимодействие между устройствами
- 💬 **Текстовые сообщения** — быстрый обмен сообщениями
- 📁 **Передача файлов** — безопасный обмен документами
- 🎤 **Голосовые звонки** — зашифрованные аудиозвонки
- 🔐 **Сквозное шифрование** — защита всех данных
- 🚀 **Кроссплатформенность** — Android, Windows, Linux

## 🏗️ Архитектура проекта

```mermaid
graph TB
    classDef flutter fill:#2196F3,stroke:#1976D2,stroke-width:3px,color:#fff
    classDef rust fill:#CE422B,stroke:#8B2500,stroke-width:3px,color:#fff  
    classDef user fill:#4CAF50,stroke:#2E7D32,stroke-width:2px,color:#fff
    classDef network fill:#FF9800,stroke:#F57C00,stroke-width:2px,color:#fff

    subgraph " "
        direction TB
        UI["📱 Пользовательский интерфейс"]:::flutter
        Logic["🧠 Бизнес-логика"]:::flutter
    end
    
    subgraph "  "
        direction LR  
        Protocol["🔗 ShadowProtocol"]:::rust
        P2P["🌐 P2P сеть"]:::network
        Crypto["🔐 Криптография"]:::rust
    end
    
    subgraph "   "
        direction TB
        Peer1["👤 Пользователь 1"]:::user
        Peer2["👤 Пользователь 2"]:::user  
        Peer3["👤 Пользователь N"]:::user
    end
    
    UI -.->|"асинхронные вызовы"| Logic
    Logic ==>|"FFI-мост"| Protocol
    Protocol -.->|"создает"| P2P
    Protocol ==>|"шифрует с помощью"| Crypto
    
    P2P ~~~ Peer1
    P2P -.-> Peer2
    P2P ==> Peer3
    
    Peer1 <-.->|"прямое"| Peer2
    Peer2 <-.->|"mesh-сеть"| Peer3  
    Peer1 -.->|"ретрансляция"| Peer3
```

## 🎯 Поддерживаемые платформы

| Платформа  | Статус      |
| ---------- | ----------- |
| 🤖 Android | 🚧 В планах |
| 🪟 Windows | 🚧 В планах |
| 🐧 Linux   | 🚧 В планах |
| 🍎 iOS     | 🚧 В планах |
| 🍎 macOS   | 🚧 В планах |

---

## 🤝 Вклад в проект

Мы приветствуем любой вклад в разработку проекта!

- 📋 Техническая документация: [**`CONTRIBUTING_RU.md`**](CONTRIBUTING_RU.md)
- 🐛 Сообщить об ошибке: [**Issues**](../../issues)
- 💡 Предложить улучшение: [**Discussions**](../../discussions)

---

## 🔒 Безопасность

Shadow Ghost использует современные криптографические алгоритмы:

- AES-256 для шифрования сообщений
- RSA-4096 для обмена ключами
- SHA-256 для хэширования
- Протокол QUIC для защищенной передачи

---

## 📄 Лицензия

Этот проект распространяется под лицензией [**Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License**](LICENSE).

---

## 🌟 Поддержка проекта

Если вам нравится Shadow Ghost, поставьте ⭐ звезду на репозиторий!

<p align="center">
  <img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&size=20&pause=1000&color=FF2E2E&center=true&vCenter=true&width=800&lines=Made+with+%E2%9D%A4+for+privacy+and+freedom+of+communication.">
</p>
