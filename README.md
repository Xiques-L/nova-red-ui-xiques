```text
╔══════════════════════════════════════════════════════════╗
║        █▄▄▄ █ █ ▄▀▄ ▄▀▄   █▀▄▄▀█ ██ █ █▀▄             ║
║        █▄▄  █▄█ ▀▄▀ ▀▄▀   █ ▀▀ █ █▄█ █ █▀              ║
║                                                          ║
║    █▀▄▀█ █▀▀█ █▀▀  █ █   █▀▀ █▀▀█ █▀▀  █▀▀█            ║
║    █ ▀ █ █▄▄█ ▀▀█  █▄█   █   █▄▄█ ▀▀█  █▄▄█            ║
║    ▀   ▀ ▀  ▀ ▀▀▀  ▄▀▄   ▀▀▀ ▀  ▀ ▀▀▀  ▀  ▀            ║
╚══════════════════════════════════════════════════════════╝
```

# Nova Red UI

> **Tema ámbar sobre negro para Cyberpunk RED Core (Foundry VTT).**  
> Glass interface, layout vertical, estética terminal Nova Red.

---

## Instalación

Agrega este manifiesto en Foundry VTT:

```
https://github.com/DKSEN404/nova-red-ui/releases/latest/download/module.json
```

**Módulo:** `Sistema → Módulos → Instalar módulo → Pegar URL del manifiesto`

---

## Características

- **Glass Interface** — Ventanas, sidebar y paneles con transparencia y blur(4px)
- **Layout Vertical** — Hojas de personaje y mook con navegación por pestañas laterales
- **Override completo** — Variables CSS `--cpr-*` sobrescritas — funciona sin modificar el sistema
- **Templates propios** — 7 templates Handlebars que reemplazan los del sistema vía `registerPartial`
- **100% CSS/JS** — Sin imágenes externas, sin dependencias adicionales
- **Compatible** — Foundry VTT v12, Cyberpunk RED Core v0.92.4+

---

## Preview

| Componente | Efecto |
|-----------|--------|
| Ventanas de actor (personaje y mook) | Layout vertical + glass |
| Hojas de item, diálogos, journal | Transparencia + blur |
| Sidebar, paneles internos, chat | Fondo semitransparente |
| Inputs, botones, selects | Fondo sólido (usabilidad) |

---

## Changelog

### v1.0.3 — Glass Effect en Layout Vertical *(2026-05-28)*
- Efecto glass/transparencia completo en layout vertical de personaje y mook
- Cobertura total: `.character-vertical`, `.mook-sheet-vertical`, `.sheet-vertical`, `.profile-header`, `.stats-bar`, `.mook-header`, `.navtabs-side`, tab-content, skills, combat, equipment, notes
- `backdrop-filter: blur(4px)` en contenedores principales del layout vertical
- Variables `--nv-glass-*` aplicadas a todos los paneles internos del layout vertical
- Inputs, selects y botones mantienen fondo sólido para usabilidad

### v1.0.2 — Vertical Layout y Theme Override *(2026-05-28)*
- Nuevo layout vertical para hojas de personaje (`.character-vertical`) y mook (`.mook-sheet-vertical`)
- 7 templates propios del módulo para independencia del sistema:
  - `cpr-character-sheet.hbs`, `cpr-mook-sheet.hbs`
  - `character/cpr-sheet-header.hbs`, `cpr-profile-tab.hbs`, `cpr-rolefight-tab.hbs`
  - `mook/cpr-mook-tab1.hbs`, `cpr-mook-tab2.hbs`
- Override completo de variables CSS `--cpr-*` para tema ámbar/negro sin modificar el sistema
- Patrón de cuadrícula cyberpunk en fondo (`html[data-cpr-theme="default"]`)
- Registro de partials vía `Handlebars.registerPartial` para instalaciones limpias
- Monkey-patch de sheet templates para usar las plantillas del módulo
- Compatibilidad 100% con Foundry VTT v12 sin dependencias externas

### v1.0.1 — Glass Interface *(2026-05-28)*
- Efecto glass/transparencia con `backdrop-filter: blur(4px)` en todas las ventanas del sistema
- Sidebar, ventanas de actor, hojas de item, diálogos, journal, notificaciones, chat tooltips
- 4 variables CSS personalizables: `--nv-glass-{deep,dark,mid,light}`
- Elementos interactivos (inputs, botones, selects) mantienen fondo sólido para usabilidad
- Código limpio: solo CSS, sin JS adicional, sin imágenes

---

## Créditos

| Recurso | Fuente |
|---------|--------|
| Módulo original | **scifi-ui** por iotech |
| Tab Icons | Rexard 7000 Icons Bundle (licenciado) |
| Tablas | Font Awesome vía Wikimedia Commons (CC BY) |
| Chat bubble | Adaptado de CoreUI Icons (CC BY) |
| Sidebar frame | Original por iotech |
| Flechas izq/der | Hexagonal Icon (CC BY SA) |
| Botones | imacat — Public Domain (OpenGameArt) |
| Denim075 | Atropos (FoundryVTT) |

## Licencia

Este trabajo (excepto gráficos) está bajo **CC BY 4.0**.  
https://creativecommons.org/licenses/by/4.0/
