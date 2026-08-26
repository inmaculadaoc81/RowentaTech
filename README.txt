RowentaTech ONE PAGE

Dominio: https://repararrobotaspirador.com.es/
Teléfono caja: +34 910 05 47 06
Teléfono botones: +34 914 46 85 03

DIAGNÓSTICO:
20 € + IVA.
No indicar diagnóstico gratuito en esta web.

Variables SMTP compartidas en Vercel:
SMTP_HOST=cp7124.webempresa.eu
SMTP_PORT=465
SMTP_SECURE=true
SMTP_USER=soporte@kelatos.com
SMTP_PASS=[configurada solo en Vercel]
CONTACT_EMAIL=soporte@kelatos.com

El correo no aparece visible en la web, solo en backend.

Google Analytics:
No se proporcionó código para esta web; no se ha añadido ninguno.

REVISIÓN (fixes aplicados):
- Menú móvil: el botón .menu-btn existía visualmente pero no tenía
  ninguna acción asociada (sin onclick) ni existía el desplegable
  #mobileMenu, así que no hacía nada al pulsarlo. Añadido el desplegable
  y su lógica de apertura/cierre.
- Banner de cookies: añadido (Aceptar / Rechazar / Política de
  privacidad → https://kelatos.com/privacy-policy/), con la corrección
  de base ya aplicada (el botón sí desaparece al pulsar cualquiera de
  las tres acciones o la X) y diseño móvil apilado a ancho completo.
- Datos schema.org: no existían. Añadido LocalBusiness con la dirección,
  el teléfono de los botones y los enlaces de Maps/YouTube.
- Añadida sección de contenido SEO propio (#guia), enlazada en el menú
  de escritorio y en el móvil.
- Añadidas etiquetas og:*/robots, que faltaban.

REDIRECCIÓN DE URLS ANTIGUAS:
Este sitio era antes multipágina (tenía /servicios/... y /modelos/...,
eliminados en commits anteriores al pasar a one-page). Añadido
middleware.mjs: cualquier URL que no sea "/" redirige (301) a la home,
para que enlaces antiguos indexados en Google no den 404. Se ha añadido
la dependencia "@vercel/functions" en package.json, necesaria para el
middleware.
