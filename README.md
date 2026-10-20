<div align="center">

<img src="docs/assets/other/logo.png" alt="VKBOTS" height="72">

# VKBOTS Wiki

**Developer documentation for VK BOTS, the VKH6 humanoid robot, joint actuators, and ROS 2 control systems.**

[Online Documentation](https://library.vkbots.com) · [3D Robot Viewer](https://library.vkbots.com/viewer/) · [Official Website](https://vkbots.com)

</div>

---

## Overview

The **VKBOTS Wiki** is a documentation platform built with **MkDocs Material** covering technical specifications, operation instructions, control software, actuator interfaces, and motion frameworks for VK BOTS robotics platforms:

- **VKH6 Humanoid Robot**: 31-DoF full-body specifications, unboxing, operation, safety guidelines, and whole-body control.
- **Developer Guide**: System network setup, CAN bus configuration, arm inverse kinematics, dexterous hands, teleoperation, sonic control, SLAM navigation, and manipulation.
- **Actuators**: CAN & CANFD register protocols, MIT mode polling/reply, and motor series (VKBOTS5014-19, VKBOTS5018-19, VKBOTS7010-19, VKBOTS8515-19) along with electric grippers.
- **Software**: VKBOTS Control App, BLE provisioning, HMAC authentication, and VKBOTS Tool diagnostics.
- **Reinforcement Learning**: Mod API 4.0 architecture, state machine transitions, sim-to-real transfer, and Isaac Gym / MuJoCo policy deployment.

---

## Local Development & Preview

Run the wiki locally with MkDocs Material:

```bash
# 1. Create and activate a Python virtual environment
python3 -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# 2. Install dependencies
pip install -r requirements.txt

# 3. Start local preview server
mkdocs serve
```

Open your browser to `http://127.0.0.1:8000` to preview the live documentation with hot-reloading.

---

## Project Structure

```
vkbots-wiki/
├── mkdocs.yml                 # MkDocs configuration (theme, navigation, plugins)
├── requirements.txt           # Python dependencies
├── overrides/                 # Custom layout overrides & branding
│   ├── main.html              # SEO metadata & titles
│   └── partials/
│       ├── header.html        # Custom header with VK BOTS links
│       └── copyright.html     # Clean copyright footer
├── hooks/
│   └── redirect_empty_sections.py  # Hook for section redirect routing
├── docs/
│   ├── .nav.yml               # Global navigation configuration
│   ├── vkh6/                  # VKH6 robot specs, quick start, safety & developer guide
│   ├── actuators/             # Planetary joint actuators, CAN protocols & grippers
│   ├── software/              # Control App, backend APIs & diagnostic tools
│   ├── rl/                    # Reinforcement learning framework & Mod API
│   ├── remapping/             # Joint & sensor remapping guides
│   ├── others/                # Appendices and supplementary references
│   ├── assets/                # Static images, diagrams, drawings & logos
│   └── stylesheets/           # Custom CSS styling tokens
└── .github/workflows/
    └── deploy.yml             # GitHub Actions automated Pages build & deploy
```

---

## Deployment to GitHub Pages

Documentation is automatically built and deployed via GitHub Actions whenever changes are pushed to `main`:

1. Push your changes to the `main` branch.
2. In your repository on GitHub, go to **Settings** → **Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.
4. GitHub Actions will build and deploy the documentation site automatically.

---

<div align="center"><sub>Copyright © 2026 VKBOTS · <a href="https://vkbots.com">vkbots.com</a></sub></div>
