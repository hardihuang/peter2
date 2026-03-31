# Peter's Code Repository

This repository contains code created by Friday (AI Assistant) for Peter.

## Structure

```
.
├── games/          # Game projects
│   └── pixel-smash-bros.html    # 2D PVP fighting game
├── web-tools/      # Web-based tools and utilities
└── docs/           # Documentation and notes
```

## Projects

### Pixel Smash Bros
A 2D pixel art PVP fighting game similar to Super Smash Bros.
- Features: 2-player local multiplayer, sound effects, health bars, 3 maps
- Controls: WASD/Arrows for movement, F/G and K/L for attack/jump
- Open `games/pixel-smash-bros.html` in a browser to play

---

## Backup System

### Friday Backups
Automatic backups of Friday's data are created every 2 weeks.

**Location:** `friday-backups/`

**Structure:**
```
friday-backups/
├── 2026-03-31/          # Backup from March 31, 2026
│   ├── extensions/      # OpenClaw extensions
│   ├── identity/        # Device identity
│   ├── logs/            # System logs
│   ├── media/           # Media files
│   ├── memory/          # Memory files
│   └── ...              # Other config files
└── 2026-04-14/          # Next backup (only 2 kept)
```

**Retention:** Only the 2 most recent backups are kept. Older backups are automatically deleted when a new one is created.

**Schedule:** Every 14 days at midnight (00:00)

**Manual Backup:** Run `./scripts/backup-friday.sh` from the repo root

---

*Managed by Friday* 🤖

### Friday Intro Page
An interactive terminal-style intro page for Friday AI Assistant.
- Features: Typewriter animation, interactive Q&A, terminal aesthetic
- Open `web-pages/intro/index.html` in a browser to view
