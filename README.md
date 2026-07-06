# HoneyComb-Client-IOS
# 🍯 HoneyComb Client

> **If the system has a limit, bypass it.**

HoneyComb Client is a heavily tweaked, high-performance Minecraft: Java Edition client designed specifically to push the boundaries of iOS and iPadOS hardware. Standing on the solid foundation of Zenith Launcher and Amethyst, this project is rebuilt from the ground up to eliminate performance bottlenecks, bypass strict sandbox limits, and deliver a seamless, crash-free mobile gaming experience.

<p align="center">
  <img src="https://img.shields.io/badge/Development%20build-passing-brightgreen?logo=github" alt="Build Status" />
  <img src="https://img.shields.io/badge/Platform-iOS%2015%2B-555555?logo=apple&logoColor=white" alt="Platform" />
  <img src="https://img.shields.io/badge/Language-Objective--C%20%2F%20Swift-orange" alt="Language" />
  <img src="https://img.shields.io/badge/License-Zenith%20Launcher-purple" alt="License" />
  <img src="https://img.shields.io/badge/Built%20by-glunguz%20%26%20Glungug-red" alt="Built by" />
</p>

---

## ⚡ Overview

While iOS users are traditionally left out of the launcher loop, HoneyComb Client steps in to bridge the gap. Remixed by **glunguz** and **Glungug**, it provides a highly optimized gateway to run Java Edition natively on your mobile device, featuring custom layout mechanics, advanced memory allocation fixes, and clean visual overhauls.

---

## 🧐 Why HoneyComb Client?

Let's be entirely real: if you want to run custom Minecraft launchers, we’d still recommend using an Android device. Android is way more exploitable, completely open, and infinitely easier to configure. 

Right now, Apple users are stuck with an incredibly small selection of mobile launchers because, sadly, almost nobody is willing to spend the time building them for iOS. Poor iOS users are left in the dark. As it stands, the entire ecosystem relies on just three pillars: **Amethyst**, **PojavLauncher**, and **Zenith Launcher**. 

We got tired of watching from the sidelines. HoneyComb Client is our answer to the locked-down iOS sandbox. If Apple builds a wall, we poke a hole in it.

---

## 🚀 Key Features

* **Lag-Reduction Architecture** – Fine-tuned environment profiles engineered to maximize frame rates and prevent memory allocation crashes (actively fighting the `getmoreram` limit).
* **HoneyComb Lobby Menu** – A completely transformed, sweet single-player and multiplayer layout that completely replaces the stock title screen with a custom theme.
* **Full Version Coverage** – Zero restrictions on game versions. Seamlessly boot anything from legacy alpha environments up to modern snapshots, with ongoing integration for Java 25.
* **Error-Free Offline Play** – Patched authentication systems that clean up local account generation bugs alongside standard Microsoft login support.
* **Streamlined JIT Launching** – Built to work hand-in-hand with TrollStore and jailbroken environments, replacing standard system alerts with a fast, custom launch override.
* **Mod Framework Compatibility** – Drop-in optimization engines supporting Fabric, Forge, Sodium, and custom rendering tweaks natively out of the box.
* **Adaptive Control Sets** – Fully modifiable virtual touch layouts, alongside native mapping for physical controllers, Bluetooth mice, and keyboards.

---

## 🧠 Technical Breakdown: Killing the Lag

To make HoneyComb Client truly lag-free on an iOS device, we can't just rely on standard game settings. Mobile hardware handles Java bytecode completely differently than a PC. Here is how we are squeezing out every drop of performance:

### 🔋 Memory Over-Allocation Prevention
iOS uses a strict process called **Jetsam** to instantly kill any app that uses more RAM than Apple thinks it should. HoneyComb Client alters how the internal JVM arguments are passed on startup, using aggressive garbage collection flags (`-XX:+UseG1GC` and `-XX:MaxGCPauseMillis=20`) to clean up dead memory blocks before iOS can panic and crash the launcher.

### 🎮 Pre-Loaded Optimization Stack
Out of the box, HoneyComb Client initializes rendering hooks designed to pair perfectly with modern rendering mods. By rewriting internal pathing, we ensure that optimization engines like **Sodium**, **Lithium**, and **VulkanMod** can communicate directly with the iOS Metal graphics API without translation stutters.

---

## 🎨 Customization & The HoneyComb Look

We believe launchers shouldn't just run well—they should look exceptional. HoneyComb Client drops the generic grid interfaces for an aesthetic, streamlined setup:

* **The HoneyComb UI:** Custom asset sheets replacing basic buttons with smooth, rounded corners and dark amber themes.
* **Responsive Layouts:** Virtual joystick and button mappings that automatically scale based on whether you are playing on a compact iPhone screen or a wide iPad Pro.
* **Built-in Resource Management:** A dedicated directory file structure allowing you to drop custom control JSON profiles directly into the app using mobile file managers.

---

## 🛠️ Planned Roadmap & Current Exploits

We are systematically tearing through the source code to fix the most annoying mobile bugs. Here is what we are tracking:

- [ ] **The `getmoreram` Jetsam Fix:** Testing custom extended memory allocation entitlements to trick iOS into giving the launcher more RAM before triggering a crash loop.
- [ ] **Java 25 Implementation:** Compiling and paths-testing mobile OpenJDK 25 runtime binaries directly inside the app bundle.
- [ ] **Local Account Patching:** Stripping out format-exception errors so local/offline profiles log in instantaneously without verifying network handshakes.
- [ ] **The "Launch Anyway" Override:** Swapping out the intrusive standard JIT warnings for a clean, non-recommended bypass popup that doesn't halt execution.

---

## 📱 Mobile-First Workflow (How We Build PC-Free)

This entire repository is managed and developed using mobile-first tools. You do not need a MacBook or a desktop setup to fork, edit, or remix this client. Our environment stack consists of:

1. **Working Copy** – A powerful iOS Git client used to manage clones, branches, and pushing commits straight back to this repository.
2. **Koder / Textastic** – Code editors used on-device to tweak structural JSON files, edit property lists (`Info.plist`), and rewrite configuration scripts.
3. **GitHub Actions** – Our cloud compiler. Every single time a code adjustment is pushed, GitHub's automated macOS runners execute the heavy build scripts and output a clean, ready-to-sideload `.ipa` file.

---

## 📲 Suggested On-Device Installation

Because HoneyComb Client requires Just-In-Time (JIT) compilation to execute Java bytecode smoothly without severe lag, we highly recommend installing the compiled `.ipa` through:
1. **TrollStore** (For permanent signing and instant root-level JIT access)
2. **Jailbroken Environments** (Dopamine / Palera1n utilizing automated JIT tools)
3. **Sideloading Automations** (SideStore / LiveContainer setups with active JIT configurations)

---

## ❔ FAQ & Sandbox Survival Matrix

| Problem | Root Cause | HoneyComb Client Solution |
| :--- | :--- | :--- |
| **App instantly closes on startup** | Missing JIT (Just-In-Time) compilation. | Run via TrollStore or enable JIT manually through SideStore/AltStore before booting. |
| **`getmoreram` Error / Game freezes** | iOS Jetsam limits killed the memory allocation. | Keep the RAM slider inside launcher settings locked between 1.2GB - 1.5GB. Our internal garbage collection tweaks will handle the rest. |
| **Local profile won't load worlds** | Broken UUID format checks in standard offline scripts. | Fixed natively in HoneyComb Client's offline authentication patch. |

---

## 📢 STEP IN EVERYONE
HoneyComb Client is a community-driven remix born out of pure frustration with ecosystem constraints. If you are tired of iOS app limits and zero launcher support, grab the code and help us break things. 

Eternal respect and huge credits go to the **Amethyst** team and **TheNullAstris** for their incredible work on **Zenith Launcher**, which served as the structural core for this project.
