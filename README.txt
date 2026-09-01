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
G-EQGDTB55ZG

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

REVISIÓN ADICIONAL (checklist unificado de la familia, a petición del cliente):
- BUG REAL — schema.org usaba el teléfono compartido de los botones
  (+34914468503) en vez del propio de la caja de información
  (+34 910 05 47 06), regla estándar de la familia desde hace tiempo
  (mismo tipo de bug encontrado antes en TechMac/ToshibaWEB2).
  Corregido.
- BUG REAL — el H1 era una pregunta ("¿Tu Rowenta no funciona?...",
  22 palabras), incumpliendo la regla de la familia (nunca pregunta,
  máximo 10 palabras). Reescrito: "Tu Rowenta no aspira o no carga.
  Aquí lo revisamos." (10 palabras, afirmativo).
- BUG REAL — el formulario no tenía ninguna casilla de consentimiento
  de política de privacidad. Añadida, con enlace a
  https://kelatos.com/privacy-policy/ en azul y subrayado.
- Añadida franja de aviso de servicio técnico independiente debajo
  del menú (no existía).
- Añadido "Sábados, domingos y días festivos estamos cerrados" debajo
  del horario.
- Botón "Atención Telefónica..." sin icono, a diferencia del de
  WhatsApp. Añadido.
- Texto decorativo del hero ya se ocultaba en móvil; el de la
  sección de datos ("NO HAGAS PRUEBAS AL AZAR") es una etiqueta
  legible de 20px, no una marca de agua gigante, así que no aplica el
  problema de corte visto en otros repos.
- Formulario verificado: fetch a /api/contacto coincide con
  api/contacto.js; conexión correcta.

REVISIÓN ADICIONAL (checklist unificado de la familia, a petición del cliente — repo 15/48):
- BUG REAL — enlace de Cal.com desactualizado. Actualizado a
  https://cal.com/kelatos/30min?embed=true&theme=light&attendeePhoneNumber=%2B34&overlayCalendar=true.
- Verificado: el correo soporte@kelatos.com no aparece visible.
- BUG REAL — el mensaje prellenado de WhatsApp decía "¡Hola Kelatos!".
  Corregido a "¡Hola RowentaTech!".
- BUG REAL — el menú móvil (#mobileMenu, estilo atributo hidden) no
  tenía ningún listener que lo cerrara al pulsar un enlace. Añadido el
  script estándar de la familia.
- Verificado: sin iconos ni imágenes con proporciones fijas
  incorrectas.
- BUG REAL — el H1 en móvil estaba en 40px. Corregido a 48px.
- BUG REAL — botones del hero (.cta) con border-radius de 15px y sin
  estado hover. Aumentado a border-radius:999px; añadido
  filter:brightness(.88) en whatsapp/pickup (colores sólidos) y
  relleno sólido con var(--blue) + texto blanco en el botón de
  teléfono (estilo contorno) al pasar el ratón.
- Verificado: este repo no usa el patrón de franja de insignias bajo
  el H1 (familia Dyson); no aplica la reubicación.
