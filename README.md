# TiddlyWiki5 for Perchance

**TiddlyWiki5 for Perchance** is a compatibility layer designed to allow users to host TiddlyWiki natively on Perchance. The goal is to integrate features such as AI-powered Language Models (LLM), Image Generation, Gallery View, and Chat into TiddlyWiki5. Additionally, this tool enables users to host semi-private wikis on Perchance without needing to log in to external services.

Due to the use of API keys, when sharing a page, the page is also editable. You only need your API key, username, and wiki name—no need to log in to Perchance.org or any other service.

> **Important:** Since TiddlyWiki uses API keys for authentication, be mindful of privacy and always back up your data regularly. Disabling compatibility layer plugins might cause issues with saving/loading wikis.

---

## How It Works (Theoretical Overview)

The Perchance Compatibility Layer consists of two core components:

1. **The Page Loader (HTML)**: This component loads raw HTML data from the Perchance server storage API and renders it within a fullscreen iframe.
2. **The TiddlyWiki Compatibility Layer**: This is a modified version of the TiddlyWiki external core plugin and required plugins, stored on GitHub. Some plugins are modified to work within Perchance, while others may not be compatible.

Due to the iframe and Perchance environment, some browser storage features may not function properly. As a result, your wiki's footprint is reduced to about **7KB** (compared to the usual 2.3MB/2.6MB size). This smaller file size is especially beneficial if you manage multiple wikis, as it prevents excessive storage usage.

---

## Features

- **LLM Integration**: Chat with an AI, debug TiddlyWiki issues, and generate new tiddlers with the help of the AI.
- **Image Generation**: Generate images directly in TiddlyWiki, with potential to save files as canonical URIs to prevent large wikis.
- **Gallery View**: A gallery view feature for visualizing images and files.
- **Chat View**: An interface for interactive communication with AI.
- **Semi-private Hosting**: Host personal wikis privately on Perchance using API keys for authentication.

---

## Notes

- **Timed Deletion for Files**: If the Perchance file storage API supports timed deletion, files will have a default expiration. This can be disabled in the compatibility layer settings.
- **Data Backup**: Always back up your wiki frequently, as saving directly to the API does not guarantee protection against data loss.

---

## To Do List

- **Rewrite the Saver**:
  - Upload to API
  - Update JS source files:
    ```html
    <script src="https://tiddlywiki-perchance.github.io/TiddlyWiki5-for-Perchance.org/latest/compatabilityplugins.js" onerror="alert('Error: Cannot load core plugins');"></script>
    <script src="https://tiddlywiki-perchance.github.io/TiddlyWiki5-for-Perchance.org/latest/tiddlywikicore.js" onerror="alert('Error: Cannot load tiddlywiki core');"></script>
    ```
- **Implement Image Generation**
- **Implement LLM Access**
- **Create LLM Configurations**
- **Set Up API and Wiki Name Generation**
- **Implement Wiki Deployment with Embedded API Keys/Username/Wiki Name**
- **Optimize Username/Wiki Name Configurations**
- **Implement Gallery View Function**
- **Implement Chat View Function**
- **Version Auto-Update**
- **Version Backporting**: Auto-load the latest kernel by default, with the option to change this in the Perchance settings.

---

## Planned Compatibility Layers

- **Saver/Loader**
- **Image Generation**
- **LLM Read/Write**
- **Chat View**
- **Gallery View**

---

## Potential Future Features

- **URL Sharing for Tiddlers**
- **Community Plugins**
- **Safe Mode Loading**
- **Generated Image Storage via Perchance File Upload**
- **Cookies (Optional)**

---

## Things I’d Love to Add (But Probably Can’t)

- **Dynamic TiddlyWiki Farm**: Porting WebDav Farm into Perchance.
- **Optimized File Storage via File Storage API**
- **Official Compatibility Layer Plugin Database**: Auto-updating and versioning.

---

## Features I Will Not Implement

- **Perchance Syntax Support**
- **Public Hosting of Personal Wikis** on https://perchance.org/tiddlywiki
- **Extensive LLM Chatbot Support**
- **Extensive Flux Image Generation** (e.g., generating multiple images in bulk)
- **Multi-User Editing**: This project is intended for personal use only; multiple users editing the same wiki could cause data conflicts.
- **Full Compatibility for Every TiddlyWiki Plugin/Perchance Plugin**
- **Perchance.org Ad Blocking**

---

## Live Test Page

- **URL:** https://perchance.org/tiddlywiki-test
- **API:** `4xvhPOcChsKj1oG2o9YhVJcYJ2kxKhCS`
- **Username:** `test`
- **Wiki Name:** `test`
- **!Warning! Due to the way Api's work i cant stop bad actors from overwritting the data stored here, proceed with caustion !Warning!
---

## License

This project is open-source. Contributions are welcome! Please see the [LICENSE](LICENSE) file for more details.
