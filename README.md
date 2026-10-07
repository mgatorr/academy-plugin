# Academy para Claude Code

El plugin de [Academy](https://academy.mariogarridotorres.com), la plataforma de cursos de
Mario Garrido Torres. Con un solo comando, tu Claude Code queda conectado a tu cuaderno de
Academy y sabe que, antes de nada, tiene que pedirle a Academy su guía: cómo se trabaja en
el curso se lo explica Academy, solo a quien ha entrado con su correo.

Solo sirve si estás dado de alta en Academy: entras con tu correo y un código, como en la
web.

## Instalarlo

En la terminal:

```sh
claude plugin marketplace add mgatorr/academy-plugin && claude plugin install academy@academy
```

Después abre `claude`, escribe `/mcp`, elige **plugin:academy:academy** → **Authenticate** y
entra con tu correo y el código.

Para trabajar: «¿qué me toca en Academy?», o los comandos del curso (`/` y escribe
`academy`).

## Tenerlo al día

```sh
claude plugin update academy@academy
```

O, una vez: `/plugin` → **Marketplaces** → academy → **Enable auto-update**.

## Qué trae

- La conexión con Academy (el servidor MCP `https://academy.mariogarridotorres.com/mcp`).
- Una skill, `academy`, que le dice a Claude que pida la guía a Academy (`academy_guide`) y
  que nada está guardado hasta que Academy responde ok.
- Un aviso al empezar cada sesión de Claude Code (un hook `SessionStart`): unas líneas que
  le dicen a Claude que eres alumno de Academy y que lo que pidas apuntar o recordar de tu
  curso va a Academy, nunca a su memoria. Son las de `plugins/academy/hooks/session-context.md`;
  el hook solo las imprime, no ejecuta nada más ni usa la red.

Lo demás vive en Academy, detrás de tu sesión: las guías y, para los cursos de fotografía,
`lr-check`, que se descarga desde tu cuaderno.

Este repositorio es una copia publicada desde el de Academy: los cambios se hacen allí.
