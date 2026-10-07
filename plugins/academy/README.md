# academy

Conecta Claude Code a Academy (`https://academy.mariogarridotorres.com/mcp`) con una sola
skill:

- `skills/academy/`: antes de nada, pedirle la guía a Academy (`academy_guide`) y seguirla;
  nada está guardado en Academy hasta que la herramienta que lo escribe responde ok.
- `hooks/`: al empezar cada sesión, el texto de `session-context.md` (que la persona es
  alumna de Academy y que lo de su curso se guarda en Academy, nunca en la memoria de
  Claude). `hooks.json` solo hace `cat` de `session-start.json`, que se genera desde ese
  texto en el repositorio de Academy.

Las guías las sirve Academy a quien ha entrado con su correo; no están en este plugin.

Instalación y actualización: el `README.md` de la raíz.
