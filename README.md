# Nova Red UI
Tema ámbar sobre negro para Cyberpunk RED Core con estética terminal Nova Red.

Basado en el módulo original **scifi-ui** creado por **iotech** para Foundry VTT.


Credits/License
This entire work (except graphics) is CC BY 4.0
https://creativecommons.org/licenses/by/4.0/

Tab Icons

Scenes		Rexard 7000 Icons Bundle (licensed)

Items		Rexard 7000 Icons Bundle (licensed)

Journals		Rexard 7000 Icons Bundle (licensed)

Tables		CC BY Font Awesome via Wikimedia Commons https://commons.wikimedia.org/wiki/File:Font_Awesome_5_solid_dice.svg

Music		Rexard 7000 Icons Bundle (licensed)

Compendiums		Rexard 7000 Icons Bundle (licensed)

Combat		Rexard 7000 Icons Bundle (licensed)

Actors		Rexard 7000 Icons Bundle (licensed)

Settings		Rexard 7000 Icons Bundle (licensed)

Chat bubble		CC BY Adapted from https://commons.wikimedia.org/wiki/File:Chat-bubble_(CoreUI_Icons_v1.0.0).svg


Other images

Sibebar frame		Original by iotech

Left arrow		CC BY SA https://commons.wikimedia.org/wiki/File:Left_arrow_Hexagonal_Icon.svg

Right arrow		CC BY SA https://commons.wikimedia.org/wiki/File:Right_arrow_Hexagonal_Icon.svg

Buttons		by imacat Public Domain https://opengameart.org/content/buttons-sci-fi

Denim075    by Atropos (FoundryVTT)

## Changelog

### v1.0.2 — Vertical Layout y Theme Override (2026-05-28)
- Nuevo layout vertical para hojas de personaje (`.character-vertical`) y mook (`.mook-sheet-vertical`)
- 7 templates propios del módulo para independencia del sistema:
  - `cpr-character-sheet.hbs`, `cpr-mook-sheet.hbs`
  - `character/cpr-sheet-header.hbs`, `cpr-profile-tab.hbs`, `cpr-rolefight-tab.hbs`
  - `mook/cpr-mook-tab1.hbs`, `cpr-mook-tab2.hbs`
- Override completo de variables CSS `--cpr-*` para tema ámbar/negro sin modificar el sistema
- Patrón de cuadrícula cyberpunk en fondo (`html[data-cpr-theme="default"]`)
- Registro de partials vía Handlebars.registerPartial para que funcione en instalaciones limpias
- Monkey-patch de sheet templates para usar las plantillas del módulo
- Compatibilidad 100% con Foundry VTT v12 sin dependencias externas

### v1.0.1 — Glass Interface (2026-05-28)
- Efecto glass/transparencia con `backdrop-filter: blur(4px)` en todas las ventanas del sistema
- Sidebar, ventanas de actor, hojas de item, diálogos, journal, notificaciones, chat tooltips
- 4 variables CSS personalizables: `--nv-glass-{deep,dark,mid,light}`
- Elementos interactivos (inputs, botones, selects) mantienen fondo sólido para usabilidad
- Compatibilidad 100% con Foundry VTT v12
- Código limpio: solo CSS, sin JS adicional, sin imágenes
