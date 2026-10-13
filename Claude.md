# CLAUDE.md — Conocimiento-BESS-BYD

## Propósito
Repo de texto con la documentación pública de BYD Battery-Box
(fichas técnicas, manuales, certificados) convertida a markdown.
Es la fuente de verdad para el Project "Conocimiento BESS".

## Estructura (nombres exactos y estables)
/productos/<familia>/<tipo>_<modelo>.md   (ej. /productos/HVS/ficha_HVS.md)
/manifiesto.md                            (índice maestro, un solo archivo activo)
/historial/YYYYMMDD_manifiesto.md         (copias fechadas)

## Reglas
- Solo texto (.md) en el repo. Los PDF originales NO se commitean
  (van en /_descargas/, que está en .gitignore).
- Un archivo activo por documento, sin fecha en el nombre.
- Si cambia una versión, edita el archivo oficial directo y deja la
  versión anterior en /historial/.
- Cada .md empieza con un encabezado: producto, tipo de documento,
  versión/fecha del PDF, URL de origen, hash SHA-256 del PDF.
- Tablas de specs: conservarlas como tablas markdown. Si una tabla no
  se convierte limpia, marcarla con "⚠ REVISAR TABLA" en vez de
  reconstruirla de memoria. Nunca completar ni aproximar cifras.
- Diff-first: ningún cambio al archivo oficial sin mostrar qué cambia
  y por qué. Nunca mergear tu propio PR.
- Renombrar, eliminar, fusionar o reordenar: señalizar en el PR para
  revisión humana, no decidir solo.
