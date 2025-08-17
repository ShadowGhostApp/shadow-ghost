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
flowchart TD
    Start([📱 Пользователь открывает ShadowGhost])
    
    IP[☁️ Узнать мой публичный IP<br/>через STUN сервер]
    
    Join[🚀 Войти в P2P сеть<br/>через Bootstrap узел]
    
    Find[🔍 Найти адрес друга<br/>в базе сети]
    
    Connect{🎯 Попробовать прямое соединение}
    
    Direct[✅ Прямой P2P чат<br/>Быстро и приватно]
    
    Relay[🔄 Через сервер-посредник<br/>Всё равно работает!]
    
    Chat([💬 Зашифрованная переписка])
    
    Start --> IP
    IP --> Join
    Join --> Find
    Find --> Connect
    Connect -->|Успех| Direct
    Connect -->|Заблокировано| Relay
    Direct --> Chat
    Relay --> Chat
    
    classDef process fill:#4CAF50,stroke:#2E7D32,color:#fff
    classDef decision fill:#FF9800,stroke:#F57C00,color:#fff
    classDef result fill:#2196F3,stroke:#1565C0,color:#fff
    
    class Start,IP,Join,Find,Chat process
    class Connect decision
    class Direct,Relay result
```

## 🎯 Поддерживаемые платформы

| Платформа  | Статус      |
| ---------- | ----------- |
| 🤖 Android | 🚧 В планах |
| 🪟 Windows | 🚧 В планах |
| 🐧 Linux   | 🚧 В планах |

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
