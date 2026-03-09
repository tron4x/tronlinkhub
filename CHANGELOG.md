# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [Unreleased]

### Added
- **Website Favicon Component**: Introduced a reusable `WebsiteFavicon` component for URL-based favicon rendering.
  - Supports multi-source favicon resolution
  - Includes robust fallback handling

### Changed
- **Link/Sub-Link Icon Defaults**: Updated icon behavior for links and sub-links.
  - Default behavior is now **favicon-first**
  - If favicon is missing/invalid/unavailable, it automatically falls back to the **inherited tile icon**
- **Per-Link Icon Modes**: Added explicit icon mode options for links and sub-links:
  - `Inherit`, `Favicon`, `Emoji`, `Text`, `Image URL`

### Improved
- **Sub-Link Icon UX in Editor**: Simplified and clarified sub-link icon settings in the tile editor.
  - Clearer mode selection labels
  - Better inline guidance for inheritance/default behavior
  - More intuitive icon input placeholders based on selected icon type

### Documentation
- **README Updated (English)**:
  - Documented hostname-based favicon lookup
  - Documented default favicon-first behavior with inherited fallback
  - Documented link/sub-link icon override modes
  - Added beta availability note: favicon-related link/sub-link icon features are currently only available in `ghcr.io/tron4x/tronlinkhub-beta`
    - https://github.com/tron4x/tronlinkhub/pkgs/container/tronlinkhub-beta

## [4.1.3] - 2026-03-08

### Changed
- **Header Links Updated**: Modernization of default header links
  - Replaced Reddit with GitLab
  - Replaced YouTube with Slack
  - Added new icons: `gitlab.svg`, `slack.svg`

### Improved
- **Extended Icon Support**: 
  - Slack icon integrated in Header, HeaderLinksModal and useHeaderLinks
  - GitLab icon fully implemented
  - All icon handlers updated for seamless integration

### Fixed
- **Memory Leak Prevention**: Fixed potential memory leaks in custom hooks
  - `useHeaderLinks.ts`: Replaced global `serverSaveTimeout` with `useRef` for proper cleanup
  - `useContactInfo.ts`: Replaced global `serverSaveTimeout` with `useRef` for proper cleanup
  - `useSiteTitle.ts`: Replaced global `serverSaveTimeout` with `useRef` for proper cleanup
  - Added proper cleanup functions in `useEffect` to clear timeouts on unmount
  - Ensures no orphaned setTimeout callbacks persist after component unmount
- **Helm Chart Secret**: Fixed "secret not found" error in Kubernetes deployment
  - `helm/linkhub v1.3.3`: Secret is now created with default password even when `editModePassword` is empty
  - Uses default password "changeme" if not specified in values.yaml
  - Prevents pod startup failures due to missing secret reference

---

## Version Overview

| Version | Date | Highlights |
|---------|------|------------|
| 4.1.3 | 2026-03-08 | Header Links Update (GitLab, Slack), Memory Leak Fixes |
| 3.2.2 | - | NPM Packages Update, RKE2 Clusters |

---

## Contributors

- **Developer**: tron4x
- **Team**: TRON LinkHub Team

---

**Developed with ❤️ for TRON LinkHub**
