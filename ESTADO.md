# ESTADO del proyecto

## Tienda
- Dominio: vzwpha-ut.myshopify.com
- Conexión: pendiente (esperando llave de acceso `shpat_...`)

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
- [x] Fase 2 — Proyecto y tema base (Dawn 16.0.0 descargado)
- [ ] Fase 3 — Brief / estilo
- [ ] Fase 4 — Secciones personalizadas
- [ ] Fase 5 — Producto y páginas
- [ ] Fase 6 — Publicación

## Producto leído
- (pendiente)

## Decisiones de diseño
- (pendiente)
