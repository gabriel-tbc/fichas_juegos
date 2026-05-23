# fichas_juegos

Contador de fichas para juegos de mesa, pensado para usar en el móvil en horizontal durante la partida.

**Demo:** https://gabriel-tbc.github.io/fichas_juegos/

![preview](https://img.shields.io/badge/web-static-blue) ![license](https://img.shields.io/badge/license-MIT-green)

## Qué es

Una web de una sola página con 5 contadores temáticos — **Dinero**, **Vida**, **Daño**, **Misión**, **Ati** — diseñados con estética de vidriera emplomada. Sirve para llevar la cuenta durante una partida sin papel, sin pantalla complicada y sin que las notificaciones del móvil te desconcentren.

Sin backend, sin base de datos, sin tracking. Todo el estado vive en `localStorage` del navegador, así que tus contadores son privados a tu dispositivo y sobreviven al cerrar el navegador.

## Funcionalidades

- **5 contadores** con icono y color propio (botiquín verde, espadas rojas, pergamino, monedas, símbolo plateado).
- **4 estilos de fondo** (amatista, zafiro, rubí, citrino) que cambian tanto el patrón del fondo como el cristal exterior de cada ficha.
- **Botones `+` / `−`** con clic sintetizado vía Web Audio API — ni un solo archivo de audio descargado.
- **Reiniciar turno** con un solo botón y sonido de barrido.
- **Pantalla completa** desde un botón en la barra superior (en escritorio y Android; en iOS, usa "Añadir a pantalla de inicio" para conseguir el mismo efecto).
- **Estado persistente** entre sesiones.
- **Adaptativo**: 5 fichas en fila en horizontal, 2 columnas en vertical (con tamaños reducidos para que quepa todo).
- **Sin dependencias**: un único archivo `index.html` con HTML, CSS, JS y SVG inline. Solo carga fuentes desde Google Fonts.

## Cómo usar

1. Abre la [demo](https://gabriel-tbc.github.io/fichas_juegos/) en el móvil.
2. Gira el móvil en horizontal para ver las 5 fichas en fila.
3. Pulsa `+` y `−` en cada ficha para subir o bajar el contador.
4. Al acabar tu turno, pulsa el botón redondo de "Reiniciar" arriba a la derecha.
5. Para esconder la barra del navegador y las notificaciones, pulsa el botón de pantalla completa (los cuatro cantos junto a "Reiniciar").

**iOS bonus:** abre la web en Safari → botón Compartir → "Añadir a pantalla de inicio". Cuando la lances desde ese icono, se ejecuta como una app, sin barras del navegador.

## Desarrollo local

No hay build, ni `npm install`, ni nada. Es un único archivo HTML.

```bash
git clone https://github.com/gabriel-tbc/fichas_juegos.git
cd fichas_juegos
# Opción 1: abre index.html directamente con doble clic
# Opción 2: sirve con cualquier servidor estático
python -m http.server
# luego visita http://localhost:8000
```

## Despliegue

Cualquier push a `main` regenera automáticamente el sitio publicado en GitHub Pages en 30-60 segundos.

## Créditos

Diseño original generado con [Claude Design](https://claude.ai/design) e iterado con [Claude Code](https://claude.com/claude-code) para añadir sonidos, modo pantalla completa, ajustes de UX móvil y despliegue automático.

## Licencia

[MIT](LICENSE) — úsalo, forkéalo, modifícalo. Si lo adaptas a otro juego (más contadores, otros colores, otros iconos), pásamelo y le doy un vistazo.
