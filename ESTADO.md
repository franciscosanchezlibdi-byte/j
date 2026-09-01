# ESTADO — Tienda Shopify

## Tienda
- Dominio: vzwpha-ut.myshopify.com
- Panel: https://admin.shopify.com/store/vzwpha-ut

## Dónde está el trabajo
- Carpeta del proyecto: /home/user/j (este repositorio)
- Rama: claude/new-session-oitifu
- Tema base: Dawn 16.0.0 (oficial de Shopify), ya descargado

## Fases
- [x] Fase 0 — Entorno: Node 22 y el programa de Shopify (CLI 4.7.0) instalados
- [ ] Fase 1 — Conexión + lectura del producto  ⛔ BLOQUEADA
- [x] Fase 2 — Proyecto y tema base (Dawn 16.0.0)
- [ ] Fase 3 — Estilo de la tienda
- [ ] Fase 4 — Secciones personalizadas
- [ ] Fase 5 — Página de producto y páginas legales
- [ ] Fase 6 — Publicación

## ⛔ Bloqueo actual (lo primero que hay que resolver)
El entorno en la nube donde se ejecuta esta sesión tiene el acceso a Shopify
denegado por política de red. Comprobado:

    vzwpha-ut.myshopify.com  -> conexión rechazada (HTTP 000)
    admin.shopify.com        -> conexión rechazada (HTTP 000)
    shopify.dev              -> conexión rechazada (HTTP 000)
    github.com               -> OK

No es un problema de credenciales: la conexión se corta antes de enviarlas.

### Solución
En claude.ai/code, editar el entorno de la nube y poner el acceso de red en
"Personalizado" (Custom) con estos dominios permitidos, marcando también la
casilla de incluir la lista por defecto:

    *.shopify.com
    *.myshopify.com
    shopify.dev

El cambio solo afecta a sesiones NUEVAS: hay que abrir una sesión nueva después.

### Sobre las credenciales
- El código que se probó empieza por `atkn_` (token de automatización de apps).
  Para la Admin API hace falta el token de app personalizada, que empieza por
  `shpat_` (Credenciales de API -> Revelar el token una vez).
- Ese token debe guardarse en `clave-tienda.txt` (está en .gitignore, nunca se
  sube al repositorio).
- Con la red desbloqueada, el login normal por navegador tampoco funcionará
  (el entorno no tiene navegador), así que el token `shpat_` sigue siendo
  necesario. Se usa con:
    - Admin API:  cabecera `X-Shopify-Access-Token`
    - Subir tema: `shopify theme push --store ... --password <token>`

## Decisiones de diseño
- Aún ninguna: no se ha podido leer el producto de la tienda.
