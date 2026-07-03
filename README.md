# LUNA Lab Edition

### AI-Native Firmware for ESP32 & ESP32-S3

**You don't write code. You have a conversation — and your hardware does the rest.**

![Platform](https://img.shields.io/badge/platform-ESP32%20%7C%20ESP32--S3-orange)
![Protocol](https://img.shields.io/badge/protocol-MCP-blueviolet)
![License](https://img.shields.io/badge/license-MIT-green)
![Distribution](https://img.shields.io/badge/distribution-binary%20releases-lightgrey)

---

## This is not another IoT framework.

For seventy years, "programming a microcontroller" has meant the same ritual: install a toolchain, learn a language, write code by hand, compile it, flash it, watch it fail, read a cryptic error, fix it, flash it again.

LUNA Lab Edition throws that ritual away.

You describe what you want, in plain language, to an AI. The AI writes the code, runs it **live** on your ESP32, reads back what actually happened, fixes what's wrong, and keeps going — until it works. No IDE. No compiler on your side. No debugging alone at 2am.

**This is AI-Native Firmware: hardware built to be programmed by an AI, not a human.**

---

## The old way vs. the LUNA Lab way

| | Traditional embedded dev | LUNA Lab Edition |
|---|---|---|
| Skill required | Learn C/C++, toolchains, wiring quirks | Describe what you want, in your own words |
| Iteration loop | Write → compile → flash → observe → repeat (minutes) | Describe → AI writes, runs, and self-corrects (seconds) |
| Debugging | You read the stack trace | The AI reads the result and fixes itself |
| Tooling | Arduino IDE / PlatformIO required every time | One-time flash, then just talk |
| Who can do it | People who already know how to code | Literally anyone |

---

## How it works

1. **Flash it once.** LUNA Lab Edition firmware turns your ESP32 into an MCP (Model Context Protocol) server with a built-in Lua scripting engine.
2. **Connect your AI.** Point Claude Desktop, Claude Code, or any MCP-compatible AI client at the device.
3. **Say what you want.** "Turn on the LED when the button is pressed." "Log the temperature every 10 seconds and post it over WiFi." "Blink SOS in Morse code."
4. **Watch it happen.** The AI writes a Lua script, runs it on the device instantly, checks the result, fixes bugs automatically, and — if you want — saves it to auto-run on every boot.

No recompiling your firmware. No re-flashing. Your logic lives as a script the AI can rewrite in real time, for as long as you keep talking to it.

---

## See it in action

```
You:    Turn on GPIO2 for 3 seconds whenever the button on GPIO4 is pressed.

Claude: [writes a Lua script, runs it on the device, checks the log]
        Done — I tested it by simulating a press and confirmed the LED
        stayed on for exactly 3.0s. Saved as "button_led.lua" and set
        to run on every boot.

You:    Actually make it flash 3 times instead of staying on.

Claude: [rewrites the script, re-runs it, verifies the timing]
        Updated and verified — 3 flashes, 200ms each. Want me to add
        a WiFi notification too?
```

No code was shown. None was needed. That's the point.

---

## Why this changes everything

- **Zero barrier to entry** — a complete beginner can build working hardware behavior in their first minute
- **Self-testing, self-fixing loop** — the AI doesn't just write code, it runs it, reads the outcome, and corrects itself, autonomously
- **One firmware, infinite programs** — your logic runs as Lua scripts pushed live over the network; the compiled firmware never needs to change
- **Protocol, not a platform lock-in** — built on MCP (Model Context Protocol), an open standard. Works with Claude today, and with any future MCP-compatible AI
- **Full hardware access** — GPIO, ADC, DAC, PWM, WiFi, BLE, UART, HTTP, TCP/UDP, and a filesystem, all exposed as tools an AI can call directly

---

## Who is this for?

**Everyone who has ever had an idea for a gadget and no idea how to code it.**

- Makers and hobbyists who want to build faster than they can learn C++
- Complete beginners — students, kids, artists — for whom "programming" was the wall between an idea and a working prototype
- Educators who want to teach *concepts* (sensors, logic, automation) without getting stuck on syntax
- Artists and installation builders who think in behavior, not code
- Professional engineers who want to prototype in seconds instead of a full build cycle
- Anyone, anywhere, in any field, who has a physical idea and wants an AI to build it with them

If you can describe it, LUNA Lab Edition can build it.

---

## Meet the family

| Model | Chip | Highlights |
|---|---|---|
| **Lab32** | ESP32 | The essentials: GPIO / ADC / DAC / WiFi / UART / Lua — the standard starting point |
| **LabS3** | ESP32-S3 | Full-featured: adds BLE5, extended advertising, USB HID, and more |
| **LabNode** | ESP32-S3 | A lightweight BLE-only companion node for multi-device setups (MicroPython edition planned) |

All three speak the same MCP protocol and the same Lua scripting model — pick the chip that fits your project, not a different way of working.

---

## Get started

LUNA Lab Edition firmware is distributed as **ready-to-flash binaries** — no build toolchain required.

1. Download the latest release for your board (Lab32 / LabS3 / LabNode) from the [Releases](../../releases) page
2. Flash it with your preferred tool (e.g. `esptool`)
3. Connect to the device's WiFi access point and complete first-time setup
4. Add the device to your MCP client (Claude Desktop / Claude Code) using its address
5. Start talking to your hardware

Full setup guides are included with each release.

---

## Philosophy: AI-Native Firmware

LUNA Lab Edition isn't a library, a framework, or a set of code examples. It's a different answer to the question "how does a human make a microcontroller do something?"

The old answer was: *learn to speak its language.*
The new answer is: *let an AI speak it for you, and just tell it what you want.*

We think this is the direction all embedded development is headed — and we want every maker, student, and dreamer on the planet to have it today, not in ten years.

---

## Relationship to LUNA Observatory

LUNA Lab Edition is a sibling project to **LUNA Observatory**, our telescope-control edition for astronomy. Lab Edition contains **no astronomy-specific code** — it's a clean, general-purpose platform for electronics and IoT projects of any kind. If you're looking to control a telescope mount, see the LUNA Observatory edition instead.

---

## License

Firmware binaries are free to use and redistribute. Source code is not publicly distributed. See [LICENSE](LICENSE) for full terms.

"LUNA" and "LUNA Lab Edition" are trademarks of Nishioka Sadahiko.

## Acknowledgments

LUNA Lab Edition is built on the shoulders of great open-source work, including the [Lua](https://www.lua.org/) scripting language (Copyright © Lua.org, PUC-Rio, MIT License) and other open-source libraries. See [LICENSE](LICENSE) for full third-party notices.

## Author

**Nishioka Sadahiko**
GitHub: [@OnStepNinja](https://github.com/OnStepNinja)

---

**LUNA Lab Edition — talk to your hardware.**
