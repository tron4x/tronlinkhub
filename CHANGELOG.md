# Changelog

Alle bemerkenswerten Änderungen an diesem Projekt werden in dieser Datei dokumentiert.

Das Format basiert auf [Keep a Changelog](https://keepachangelog.com/de/1.0.0/),
und dieses Projekt folgt der [Semantischen Versionierung](https://semver.org/lang/de/).

---

## [3.2.2]

### Geändert
- **NPM Packages aktualisiert**: Alle Abhängigkeiten auf die neuesten stabilen Versionen aktualisiert
- Rancher Kubernetes: Neue RKE2 Cluster hinzugefügt
- ArgoCD: Neue RKE2 Cluster hinzugefügt

## [3.1.4] - 2026-01-16

### Geändert
- **NPM Packages aktualisiert**: Alle Abhängigkeiten auf die neuesten stabilen Versionen aktualisiert
  - Next.js 16.1.2
  - React 19.2.3
  - Framer Motion 12.26.2
  - Lucide React 0.562.0
  - Tailwind CSS 3.4.19
  - TypeScript 5.3.3

### Sicherheit
- Sicherheitsupdates durch aktualisierte Abhängigkeiten

### Behoben
- **Docker Build**: Node.js Version im Dockerfile von 18 auf 20 aktualisiert (Next.js 16 benötigt Node.js >=20.9.0)

---

## [3.1.2] - 2025-10-27

### Hinzugefügt
- **TEST-INTE Subcluster Support**: Erweiterte Unterstützung für TEST-INTE Subcluster
- **Subviews für TEST-INTE**: Neue Unteransichten für folgende Services:
  - ArgoCD
  - Kyverno
  - Kasten

### Geändert
- Verbesserte Multi-Cluster-Verwaltung für TEST-INTE Umgebung

---

## [3.1.1] - 2025-09-24 bis 2025-09-30

### Hinzugefügt
- **Portworx Integration**: Vollständiges Portworx Storage Platform Modal
  - Multi-Cluster Management Tools
  - Interaktive Hilfe-Dokumentation
  - Lizenz-Management mit Ablaufwarnungen und farbcodierten Alerts
  - Copy-to-Clipboard für bashrc Konfigurationen

- **Neue Bash-Funktionen**:
  - `mc` / `multicluster` - kubectl Befehle über mehrere Cluster ausführen
  - `mc_px` - pxctl Befehle auf allen Portworx-Clustern ausführen
  - `mc_pxlicense` - Alle Lizenzen mit farbcodiertem Status prüfen (expired, critical, warning)
  - `mc_pxlicense_expiring` - Nur problematische Lizenzen anzeigen (anpassbarer Schwellenwert)
  - `pxadmin` - Schnelles Admin-Kontext-Setup
  - Multiple `px*` Aliase für häufige Operationen (Status, Volumes, Alerts, Nodes, etc.)

- **Dokumentation**:
  - Ausklappbare Hilfe-Sektionen mit detaillierten Funktionsbeschreibungen
  - Umgebungsspezifische Portworx-Cluster-Links
  - BitBucket Dokumentations-Integration

### Geändert
- **Nginx Konfiguration**: Optimierte Nginx-Einstellungen für bessere Performance
- **UI/UX Verbesserungen**:
  - Smooth Animations mit Framer Motion
  - Purple/Indigo Gradient Theme für Portworx Modal
  - Responsive Design für alle Bildschirmgrößen

---

## [3.1.0] - 2025-09-24

### Hinzugefügt
- **12 Vollständig integrierte Service-Modals**:
  - Rancher Kubernetes (Grün)
  - ArgoCD (Orange)
  - Kasten (Indigo)
  - Kyverno (Lila)
  - Grafana (Orange)
  - JFrog Artifactory (Smaragd)
  - NeuVector (Rose)
  - Jenkins (Blau)
  - Splunk (Dunkel-Lila)
  - Sealed Secrets (Schiefer)
  - Cluster Viewer (Schiefer)
  - Portworx (Blau)

- **Professionelles Animations-System**:
  - Floating Icons mit 4s Loop
  - Gestaffelte Animationen für Listen und Grids
  - Spring Physics für natürliche Bewegungen
  - Hardware-beschleunigte 60fps Animationen

- **Moderne Tech-Stack Migration**:
  - Next.js 16 App Router
  - React 19 mit Server Components
  - TypeScript mit Strict Mode
  - Tailwind CSS 3.4
  - Framer Motion 12

### Geändert
- Komplette Neugestaltung der LinkHub
- Dunkles Theme als Standard
- Service-spezifische Farbthemen für jeden Modal

---

## [3.0.0] - 2025-09-01

### Hinzugefügt
- **Initiales Release** der TRON LinkHub
- Next.js Projekt-Setup
- Grundlegende Komponenten-Struktur
- Docker-Deployment-Konfiguration
- Nginx als Reverse Proxy

### Architektur
```
src/
├── app/                    # Next.js App Router
├── components/             # React Komponenten
│   ├── Hero.tsx           # Haupt-Landing-Komponente
│   ├── *Modal.tsx         # Service Modals
│   ├── animations/        # Animation Komponenten
│   └── icons/             # Service Icons
├── lib/                   # Utility Funktionen
└── styles/                # Globale Styles
```

---

## Versionsübersicht

| Version | Datum | Highlights |
|---------|-------|------------|
| 3.1.4 | 2026-01-16 | NPM Packages Update |
| 3.1.2 | 2025-10-27 | TEST-INTE Subcluster Support |
| 3.1.1 | 2025-09-30 | Portworx Integration, Bash-Tools |
| 3.1.0 | 2025-09-24 | 12 Service Modals, Animation System |
| 3.0.0 | 2025-09-01 | Initiales Release |

---

## Docker Images

| Version | Image Tag | Registry |
|---------|-----------|----------|
| 3.1.4 | `landi:v3.1.4` | tron-linkhub-docker.registry.tron.dev |
| 3.1.2 | `landi:v3.1.2` | tron-linkhub-docker.registry.tron.dev |
| 3.1.1 | `landi:v3.1.1` | tron-linkhub-docker.registry.tron.dev |

---

## Mitwirkende

- **Entwickler**: Konstantinos Poulios
- **Team**: TRON LinkHub Team

---

**Entwickelt mit ❤️ für die TRON LinkHub**
