
# Конспект по Expo

> **Expo** - это фреймворк React Native, который облегчает разработку приложений для Android и iOS. 

---

## Create a project (Создание проекта)

### Системные требования 

Node.js (LTS).
поддерживаются macOS, Windows (Powershell и WSL 2) и Linux.

### Создание проекта

Для создания нового проекта искользуется команда: npx create-expo-app@latest

Вместо стандартного проекта можно начать с одного из примеров Expo. Это небольшие приложения, каждое из которых демонстрирует определённую функцию или интеграцию, такие как Expo Router, Expo Widgets или экран камеры.

Чтобы просмотреть полный список и выбрать интерактивно, запустите с помощью create-expo-app--example Опция и Нет имени:
npx create-expo-app@latest --example

Чтобы создать известный пример напрямую, передайте его имя:
npx create-expo-app@latest --example with-widgets

### Настройте агента ИИ

Новый проект включает AGENTS.md с контекстом проекта для ИИ-агентов. При установке Claude Code также включает .claude/settings.json для включения плагина Expo. Claude Code и Codex имеют официальный плагин для Expo. Используя одну команду, вы можете установить Expo Skills и зарегистрировать сервер Expo Model Context Protocol (MCP):
claude plugin install expo@claude-plugins-official

Затем пройдите внутрь сессии Claude Code и войдите в свой аккаунт Expo./mcp

---
