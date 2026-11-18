# prueba-deploy

Repositorio plantilla (Template repository) para las apps de la caja de apps publicadas en GitHub Pages.

## Al crear un repo nuevo con "Use this template"

1. **Settings → Pages:** Source = **Deploy from a branch → main → / (root)**.
2. Poner la app en `index.html`, con `<meta name="app-version" content="v0.0.1">` en el `<head>` (o el número con que deba arrancar).
3. Hacer el primer push con `[patch]`, `[minor]` o `[major]` en el mensaje: la primera Release toma el número escrito en el HTML.

El commit inicial que crea GitHub ("Initial commit") **no** genera Release, porque no lleva tipo.

## Versiones

Flujos copiados de `luchorcompartidos/home` → `plantilla/` (ver `ESTANDAR-VERSIONES.md`):

- `release.yml`: en cada push a main crea tag y Release según `[major]`, `[minor]` o `[patch]` en el mensaje del commit. Sin etiqueta (o con `[skip release]`) publica igual, pero no crea Release.
- `reemplazar-version.yml`: se lanza a mano desde Actions para rehacer o crear una versión puntual.
