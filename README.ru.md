# Репозиторий приложений Kortex (Kortex App Hub Catalog) 🏪
### Официальный каталог программного обеспечения и манифестов для KortexOS

[![Версия каталога](https://img.shields.io/badge/каталог-v1.0.0-00f0ff.svg?style=for-the-badge)](apps.json)
[![Лицензия](https://img.shields.io/badge/лицензия-MIT-00ff41.svg?style=for-the-badge)](LICENSE)
[![Совместимость](https://img.shields.io/badge/KortexOS-v1.0.0%2B-ff003c.svg?style=for-the-badge)](https://github.com/ArtiomITPROGRAMING/KortexOS)

[ 🇬🇧 Read in English ](README.md) | [ 🇷🇺 Читать на русском ](README.ru.md) | [ 🌌 Основной репозиторий KortexOS ](https://github.com/ArtiomITPROGRAMING/KortexOS)

Добро пожаловать в официальный **Каталог приложений KortexOS**! Этот репозиторий выступает открытым децентрализованным облачным бэкендом для встроенного магазина **Kortex App Hub (`kortex-store`)**.

Каждая программа, добавленная сюда, автоматически становится доступной пользователям KortexOS по всему миру без необходимости обновлять образ системы.

---

## 🚀 Как это работает?

1. **Синхронизация с облаком**:
   Когда пользователь открывает Магазин Приложений в KortexOS (`kortex-store` или клавиша `Super + P`), клиент автоматически загружает свежий каталог:
   ```
   https://raw.githubusercontent.com/ArtiomITPROGRAMING/kortex-apps/main/apps.json
   ```
2. **Оффлайн-режим (Кэш)**:
   Если интернет отключен, система берет локальную резервную копию `/usr/share/kortex/apps.json`.
3. **Установка в 1 клик**:
   Пользователь выбирает приложение и нажимает `[ УСТАНОВИТЬ ]`. Поддерживаются:
   - **`native`**: Официальные пакеты Arch Linux (`pacman`).
   - **`flatpak`**: Изолированные пакеты из Flathub.
   - **`bundle`**: Автономные скрипты и AppImage.

---

## 🤝 Как добавить свое приложение в каталог?

Мы рады вкладу любого разработчика! Добавить свою программу очень просто:

### Шаг 1: Сделайте Fork репозитория
Нажмите кнопку **Fork** на странице `https://github.com/ArtiomITPROGRAMING/kortex-apps` и склонируйте свою копию.

### Шаг 2: Добавьте описание в `apps.json`
Откройте файл [`apps.json`](apps.json) и добавьте ваш блок в массив `"apps"`:

```json
{
  "id": "my-awesome-app",
  "name": "Название Программы",
  "category": "Development & IDE",
  "description": "Краткое и понятное описание функций приложения.",
  "version": "1.0.0",
  "icon": "🚀",
  "type": "native",
  "package": "my-awesome-app",
  "install_cmd": "sudo pacman -S --noconfirm my-awesome-app",
  "launch_cmd": "my-awesome-app",
  "homepage": "https://example.com",
  "size": "25 MB"
}
```

### Доступные категории:
- `Audio & Music` — Аудио, музыка и синтезаторы
- `Browsers & Web` — Браузеры и интернет
- `Development & IDE` — Среды разработки, компиляторы и редакторы
- `Communication` — Мессенджеры и связь
- `Media & Graphics` — Графика, видео и 3D
- `Gaming & Emulation` — Игры и эмуляторы
- `Cybersecurity & Net` — Утилиты анализа сети и безопасности
- `System Utilities` — Системные инструменты и мониторы

### Шаг 3: Отправьте Pull Request
Создайте Pull Request в ветку `main`. После проверки и объединения ваша программа мгновенно появится в магазине у всех пользователей KortexOS!

---

## 📄 Лицензия
Этот каталог и манифесты распространяются под свободной лицензией [MIT License](LICENSE).
