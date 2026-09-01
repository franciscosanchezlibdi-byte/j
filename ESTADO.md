# ESTADO del proyecto

## Tienda
- Dominio: (pendiente — esperando el enlace del usuario)
- Conexión: pendiente

## Entorno
- Ordenador: remoto (en la nube), Linux
- Node: v22.22.2 ✅
- Shopify CLI: 4.7.0 ✅ (soporta `store auth` / `store execute`)
- Nota importante: al ejecutarse en la nube, el login por navegador de Shopify
  no es viable (la vuelta del navegador apunta al equipo local del usuario).
  Plan adoptado: llave de acceso de app personalizada (`shpat_...`), usada con
  `--password` / `SHOPIFY_CLI_THEME_TOKEN` para el tema y con llamadas directas
  a la Admin API para los datos del producto.

## Fases
- [x] Fase 0 — Entorno preparado
- [ ] Fase 1 — Conexión + sondeo del producto
- [ ] Fase 2 — Proyecto y tema base
- [ ] Fase 3 — Brief / estilo
- [ ] Fase 4 — Secciones personalizadas
- [ ] Fase 5 — Producto y páginas
- [ ] Fase 6 — Publicación

## Producto leído
- (pendiente)

## Decisiones de diseño
- (pendiente)
