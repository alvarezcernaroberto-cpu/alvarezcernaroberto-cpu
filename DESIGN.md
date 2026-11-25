# gamer-dev — Sistema de diseño

Referencia visual: foto de Roberto de pie frente a una esfera gigante de neón verde, con control en mano, audífonos al cuello, pared de ladrillo oscuro de fondo y el sello `gamer-dev` con el ícono de GitHub en la esquina inferior derecha.

El diseño no copia la foto: toma su atmósfera — oscuro, ladrillo, un solo punto de luz verde — y la convierte en reglas.

## 1. Paleta

| Uso | Color | Hex | Notas |
| --- | --- | --- | --- |
| Fondo principal | Negro GitHub | `#0D1117` | Fondo del README y de las tarjetas de stats |
| Fondo secundario | Gris azulado oscuro | `#111827` | Tablas alternas, bloques secundarios |
| Fondo terciario | Verde-negro | `#141A17` | Solo para separar una sección, nunca como bloque grande |
| Acento principal | Verde Xbox | `#107C10` | Badges clave, enlaces activos, sello |
| Acento vivo | Verde neón | `#22C55E` | Títulos de stats, iconos, barras de progreso |
| Acento de detalle | Verde eléctrico | `#39FF14` | Solo en detalles: un borde, un punto, un glow. Nunca en texto corrido ni en fondos |
| Texto principal | Gris claro | `#E6EDF3` | Texto sobre fondo oscuro |
| Texto secundario | Gris medio | `#8B949E` | Subtítulos, notas, metadatos |
| Borde | Gris oscuro | `#30363D` | Bordes de tablas, tarjetas y separadores |
| Ladrillo / neutro | Gris ladrillo | `#3A3F44` | Solo en gráficos, nunca como fondo de texto |

**Regla de saturación:** el verde neón nunca cubre más del ~10% visible de la pantalla. Si una sección se ve verde, sobra verde.

### Modo claro de GitHub

El README usa los mismos colores. En modo claro, GitHub pone fondo blanco, pero:

- Las badges `flat-square` y las tarjetas de stats con `bg_color=0D1117` se mantienen oscuras a propósito: son islas oscuras, no texto verde sobre blanco.
- No se usa texto verde claro (`#22C55E` / `#39FF14`) en texto corrido: en fondo blanco pierde contraste.
- Los enlaces heredan el azul de GitHub en modo claro; en modo oscuro, el verde solo aparece en badges y títulos de stats.

## 2. Tipografía y jerarquía

- **Fuente:** la de GitHub por defecto (system UI). No se fuerza otra fuente en Markdown: mantiene legibilidad en móvil y escritorio.
- **H1:** solo `gamer-dev`, una vez, centrado, bajo el banner.
- **H2:** secciones principales (`Sobre mí`, `Stack`, `Proyectos destacados`, `Contacto`). Sin emojis en los títulos.
- **H3:** subsecciones dentro de un proyecto.
- **Texto:** frases cortas, una idea por párrafo. Sin clichés (“apasionado por la tecnología”, “el código es mi vida”).
- **Tablas:** una sola estructura en todo el repo: encabezado en negrita, primera columna en negrita, sin colores dentro de las celdas.

## 3. Banner y foto

- **Banner:** `assets/banner.svg` (1600 × 500, vectorial y ligero). Ladrillo oscuro + esfera neón a la derecha, sin persona ni texto dentro de la imagen. El texto va en Markdown, debajo, para que sea legible y se pueda editar. La versión fotorrealista `assets/banner.webp` queda como alternativa local: si la prefieres, súbela por la web de GitHub y cambia la primera imagen del README a `assets/banner.webp`.
- **Foto personal:** `assets/hero.jpg` — **no incluida en este paquete**. Súbela tú:
  1. Recorta en vertical, con la esfera y el ladrillo visibles detrás.
  2. Exporta en JPG, máx. 1200 px de ancho, < 500 KB (TinyPNG / Squoosh).
  3. Guarda como `assets/hero.jpg` y descomenta el bloque `FOTO PERSONAL` en `README.md`.
- **Avatar:** usa la misma foto recortada en cuadrado para el avatar de GitHub. Coherencia > variedad.
- **Bordes:** en GitHub no se puede forzar `border-radius` fiable en Markdown. La limpieza se logra con: una sola imagen a ancho completo, centrada, sin marcos dobles ni sombras pegadas en la imagen.

## 4. Badges

- Estilo único: `style=flat-square`.
- Orden fijo: lenguaje principal → framework → datos → ecosistema Microsoft → GitHub.
- Colores de marca reales para Python / PostgreSQL, y `#107C10` solo para Power Platform y el sello gamer-dev.
- No más de 5 badges en la cabecera. El resto va en la tabla de Stack.

## 5. Stats

Servicio `github-readme-stats`, con tema oscuro fijo para que no rompa en modo claro:

```
bg_color=0D1117
title_color=22C55E
icon_color=22C55E
text_color=E6EDF3
border_color=30363D
```

Si el servicio falla, el README sigue completo: las stats son un extra, no la presentación.

## 6. Sello gamer-dev

`assets/gamer-dev-badge.svg` — rectángulo oscuro `#111827`, borde `#107C10`, texto `gamer-dev` en blanco y un punto neón `#39FF14`. Se usa solo al pie del README y como identificador en `projects/`. No se pone en cada sección.

## 7. Qué no hacer

- No usar el nombre interno del sistema de la planta en público.
- No publicar código, credenciales, respaldos ni configuraciones internas de la empresa.
- No añadir más de un banner por página.
- No mezclar estilos de badges (`flat`, `for-the-badge`, `plastic`) en el mismo repo.
- No poner la foto original sin comprimir: GitHub la muestra lenta y pesa en cada clon.
