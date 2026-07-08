# 💩 CacaMap

El mapa social de tus cagadas: regístrate, marca tus territorios en un mapa
interactivo y compite con tus amigos por el trono.

Vibecodeada en un prompt. Un único fichero (`index.html`), sin build, sin
dependencias que instalar y sin servidor.

## Cómo usarla

**Opción 1 — abrir directamente**: descarga `index.html` y ábrelo en el
navegador. Ya está.

**Opción 2 — GitHub Pages (recomendada para compartir con amigos)**: en este
repo, ve a *Settings → Pages*, en "Source" elige la rama `main` y carpeta
`/ (root)`, y guarda. En un minuto la app quedará publicada en
`https://malbisudlf.github.io/CacaMa-/` y cualquiera con el enlace podrá
usarla desde el móvil.

## Qué incluye

- **Registro e inicio de sesión** por usuario (contraseña con hash SHA-256 +
  sal en `localStorage`; varios usuarios pueden compartir navegador).
- **Mapa interactivo** (Leaflet + teselas oscuras de CARTO): clic en cualquier
  punto para registrar una cagada con lugar, fecha, calidad (1–5 💩) y nota.
  Botón de geolocalización para centrarte donde estés.
- **Comparación entre amigos sin servidor**: exporta tu *caca-código* (JSON en
  base64), mándaselo a un amigo por donde quieras; al importarlo, sus cagadas
  aparecen en tu mapa con su propio color.
- **Ranking de tronos** con medallas, estadísticas personales (total, mes en
  curso, calidad media) e historial con borrado.

## Limitaciones asumidas

- Los datos viven en el `localStorage` de cada navegador: no hay backend ni
  sincronización automática — la comparación entre amigos va por intercambio
  de códigos. La "autenticación" es local y no protege nada frente a alguien
  con acceso al dispositivo: es una app de risas, no de banca.
- Leaflet y las teselas del mapa se cargan por CDN: hace falta conexión.
