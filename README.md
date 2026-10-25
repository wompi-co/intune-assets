---
title: "intune-assets"
generated_by: archai-docgen
generated_at: "2026-06-30T18:07:22.474Z"
repo_type: "Library"
primary_language: "XML"
---

<div style="margin-bottom:15px">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://cdn.wompi.com/brand_wompi/logos/logo-secondary.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://cdn.wompi.com/brand_wompi/logos/logo-primary.svg">
  <img alt="Wompi Logo" src="https://cdn.wompi.com/brand_wompi/logos/logo-primary.svg" width="150">
</picture>
</div>

# intune-assets

## Description

The `intune-assets` repository is an asset storage and distribution repository for Microsoft Intune device management deployments at Wompi. It contains binary deployment packages, configuration files, and corporate branding resources that IT administrators upload to the Microsoft Intune console for deployment to managed macOS and Windows devices across the organization.

This repository provides centralized version control and storage for endpoint security software deployments (Palo Alto Networks Cortex XDR with configuration) and corporate device wallpapers themed "Aprendemos Continuamente." IT teams use these assets to standardize security posture and branding across enrolled devices through Intune's cloud-based endpoint management service.

## Installation

This repository is not an npm package and cannot be installed via a package manager. To use these assets:

```bash
git clone <repository-url>
cd intune-assets
```

Assets are accessed directly from the repository filesystem and uploaded manually to the Microsoft Intune admin portal for deployment to managed devices.

## Quick Start

IT administrators deploy assets through the Microsoft Intune console. For example, to deploy Cortex XDR:

```bash
. Clone the repository
git clone <repository-url>

# 2. Navigate to the security app directory
cd intune-assets/App-Intune

# 3. Upload CortexXDR.pkg and Config.xml to Intune console
#    via Apps > macOS > Line-of-business app

# 4. Assign deployment policy to target device groups
```

For wallpaper deployment, upload image files from the `Wallpaper/` directory via Device Configuration profiles in the Intune portal.

## API Reference

This repository does not export code functions or classes. It contains the following deployable assets:

| Asset Path | Type | Purpose |
|------------|------|---------|
| `App-Intune/CortexXDR.pkg` | Binary package | Palo Alto Networks Cortex XDR endpoint security installer for macOS |
| `App-Intune/Config.xml` | XML configuration | Cortex XDR deployment configuration (distribution ID: ff2f989534e14aaa80a579b675065820, endpoint tags: WOMPI) |
| `Wallpaper/fondoMacAprendemosContinuamente.jpeg` | Image asset | Corporate wallpaper for macOS devices |
| `Wallpaper/fondoWindowsAprendemosContinuamente.jpeg` | Image asset | Corporate wallpaper for Windows devices |
| `Wallpaper/locked_screen.png` | Image asset | Lock screen wallpaper |

**Config.xml Parameters:**
- `distribution_id`: ff2f989534e14aaa80a579b675065820
- `cloud_elb_address`: https://distributions.traps.paloaltonetworks.com
- `endpoint_tags`: WOMPI
- `proxy_list`: Empty

## Compatibility

| Requirement | Supported Versions |
|-------------|-------------------|
| Microsoft Intune | Required infrastructure for deployment |
| CortexXDR.pkg target | macOS devices |
| Wallpaper assets | macOS and Windows endpoints |
| Admin access | Microsoft Intune administrator permissions required |

## License

No license file found in this repository. Internal Wompi asset repository — not for external distribution.
