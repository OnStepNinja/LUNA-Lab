# LUNA-Lab
Electronics/Maker Bridge



**MCP Server + Lua Scripting Engine on ESP32**

> Let Claude AI control your telescope, camera, and entire observatory — in plain language.

![Version](https://img.shields.io/badge/version-v5.9.3-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Platform](https://img.shields.io/badge/platform-ESP32-orange)

---

## LUNA Docs (NotebookLM)

📚 LUNA Docs — Start here for setup guides, technical references, and FAQ.
Ask questions directly inside NotebookLM and get answers from the official documentation.
👉 https://notebooklm.google.com/notebook/f2ce997f-18c2-44c4-8738-973b204c190c

💬 AiBridgeMCP Community — Join our Facebook group to ask questions, share your results, and connect with other users. The developer is also a member. Everyone is welcome.
👉 https://www.facebook.com/groups/1230935959149731

---

## What is LUNA?

LUNA is a firmware for ESP32 that turns it into an **MCP (Model Context Protocol) server with a built-in Lua scripting engine**.

Connect LUNA to your telescope or observatory equipment, then control everything through Claude AI — in plain language.

```
You ──→ Claude AI ──→ LUNA (ESP32) ──→ Telescope / Serial Device
              "Go to M42"    serial command    🔭 slews

You ──→ Claude AI ──→ LUNA (ESP32) ──→ NINA (PC) ──→ Camera / Focuser / Guider
         "Image M42 tonight"   HTTP API       🌟 full automation
```

LUNA runs **Lua scripts autonomously** on the ESP32. Claude writes the scripts, deploys them, and monitors results — all through the MCP protocol.

![Hardware_Pinout_RS232C_Wiring_Guide](assets/Hardware_Pinout_RS232C_Wiring_Guide2.png)

![LUNA Observatory System v5.9.6](assets/LUNA%20Observatory%20System%20v5.9.6.png)

---


📚 **[LUNA Docs on NotebookLM](https://notebooklm.google.com/notebook/f2ce997f-18c2-44c4-8738-973b204c190c)** — Ask questions about LUNA directly.

---

## License

The LUNA firmware binary is distributed under the [MIT License](LICENSE).
Source code is proprietary and not published.

Copyright © 2026 Nishioka Sadahiko

---

### Third-Party Licenses

LUNA incorporates **Lua 5.1**, distributed under the MIT License:

> Copyright © 1994–2012 Lua.org, PUC-Rio.
> Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions: The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software. THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.

See also: https://www.lua.org/license.html

---

## Author

**Nishioka Sadahiko**
GitHub: [@OnStepNinja](https://github.com/OnStepNinja)
