# post-review

> Un puntaje y las correcciones exactas antes de publicar.

**Revisión de posts** · Skill para agentes de código de la comunidad [nvvdev](https://github.com/nvv-dev). Funciona en Claude Code como plugin o como skill suelta, y en cualquier agente compatible con el formato abierto [`SKILL.md`](https://agentskills.io).

*English summary at the end.*

## Qué hace

Califica un borrador de post, hilo, carrusel o sección de boletín de 0 a 2 en seis criterios: gancho, una sola idea, prueba, voz, formato de la red y llamado a la acción. Por cada criterio débil cita la parte del borrador y entrega la versión corregida, más tres ganchos alternativos. Pide fuente primaria para noticias y cifras. Nunca publica ni programa nada.

## Objetivo

Que cada post salga con una idea clara, con pruebas y con tu voz, sin depender del gusto del día.

## Cuándo usarla

- Antes de publicar un post o un hilo
- Cuando un borrador "no convence" y no sabes por qué

## Cuándo no

- Copy de páginas: usa landing-copy
- Para que el agente publique: esta skill solo revisa

## Ejemplo

```text
Revisa este borrador para LinkedIn con post-review y dame el puntaje.
```

## Cómo se activa

Esta skill **se activa sola**: Claude Code lee su descripción y la carga cuando la tarea coincide. También puedes pedirla por nombre ("usa la skill post-review") o invocarla con `/post-review:post-review` (plugin) o `/post-review` (copiada a `.claude/skills/`).

## Instalación

### Opción 1: Claude Code, como plugin (recomendada)

Dentro de Claude Code:

```text
/plugin marketplace add nvv-dev/claude-plugins
/plugin install post-review@nvvdev
```

La primera línea agrega el catálogo de nvvdev una sola vez; la segunda instala esta skill. Si prefieres el paquete completo, instala `growth-workflow@nvvdev` en su lugar (incluye esta skill y las demás de [growth-workflow](https://github.com/nvv-dev/growth-workflow)); no instales los dos a la vez.

### Opción 2: Claude Code, copiando la skill

Para un solo proyecto (se comparte con tu equipo por git):

```bash
git clone --depth 1 https://github.com/nvv-dev/post-review.git /tmp/post-review
mkdir -p .claude/skills
cp -R /tmp/post-review/skills/post-review .claude/skills/
```

Para todos tus proyectos, cópiala en `~/.claude/skills/` en lugar de `.claude/skills/`.

### Opción 3: otros agentes

Copia la carpeta `skills/post-review/` en la carpeta de skills de tu agente (cada agente documenta la suya). Con la CLI [skills](https://github.com/vercel-labs/skills) de Vercel Labs:

```bash
DISABLE_TELEMETRY=1 npx skills add nvv-dev/post-review
```

### Verificar

Abre una sesión nueva y pregunta "¿qué skills tienes disponibles?"; `post-review` debe aparecer. Con el plugin, `/plugin` la muestra como instalada.

### Actualizar o desinstalar

- Plugin: `/plugin marketplace update nvvdev` para actualizar; `/plugin uninstall post-review@nvvdev` para quitarla.
- Copia manual: repite la copia para actualizar, o borra la carpeta `.claude/skills/post-review`.

Antes de instalar cualquier skill, incluida esta, conviene leerla: es un solo archivo, [`skills/post-review/SKILL.md`](skills/post-review/SKILL.md). Ver [vetting-external-skills](https://github.com/nvv-dev/vetting-external-skills).

## Contenido

| Ruta | Qué es |
|---|---|
| `skills/post-review/SKILL.md` | La skill: instrucciones en inglés para que los escáneres de seguridad las analicen completas; el agente responde en tu idioma |
| `.claude-plugin/plugin.json` | Manifiesto para instalarla como plugin |
| `.github/workflows/` | Validación de estructura y escaneo con SkillSpector en cada cambio |

## Contribuir

Este repo se **genera** desde [nvv-dev/growth-workflow](https://github.com/nvv-dev/growth-workflow), donde vive la versión canónica. Abre issues y PRs allí. La mejor contribución es un caso real en la sección *Known failures* de la skill, con la regla que lo evita.

## Origen

Escrita desde cero por nvvdev. Inspirada en: [charlie947/social-media-skills](https://github.com/charlie947/social-media-skills) (post-scorer, hook-generator).

## Licencia

MIT.

---

## English

**post-review** — Scores a draft post on hook, single idea, proof, voice, network format and CTA, and returns corrections. Never publishes.

Install in Claude Code with `/plugin marketplace add nvv-dev/claude-plugins` and `/plugin install post-review@nvvdev`, or copy `skills/post-review/` into `.claude/skills/` (project) or `~/.claude/skills/` (personal). Other agents: copy the folder into their skills directory, or run `DISABLE_TELEMETRY=1 npx skills add nvv-dev/post-review`. Loads automatically when the task matches its description. Canonical source: [nvv-dev/growth-workflow](https://github.com/nvv-dev/growth-workflow). License: MIT.
