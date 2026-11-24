# Aula AI — primera entrega

Aplicación web progresiva en español para organizar tareas de estudio.

## Incluido
- Interfaz responsive para PC y móvil.
- Registro e inicio de sesión por correo/contraseña con Supabase Auth.
- Crear y consultar actividades privadas en `public.study_tasks`.
- Historial de las 50 actividades recientes.
- Manifiesto, icono y service worker para PWA.

## Pendiente
- Proveedor Google OAuth (requiere configuración de credenciales).
- Respuestas de IA (requiere función backend y clave privada).
- Adjuntos y análisis de PDF, imágenes y audio.
- Pruebas integrales y publicación.

## Publicación
Subir todos los archivos de esta carpeta a la raíz del repositorio `jsantacruzu-ui/aula-ai` y conectar el repositorio a Cloudflare Pages. No requiere build: comando de compilación vacío; directorio de salida `/`.

La URL y publishable key de Supabase están en `app.js`. La publishable key es apta para cliente público; nunca introducir aquí `service_role` ni claves secretas.

En Supabase, habilitar Email en Authentication > Providers y configurar las URLs permitidas. La tabla `study_tasks` debe mantener RLS y políticas por propietario (`auth.uid() = user_id`).

## Privacidad
No subir información confidencial o sensible. El navegador usa solo la publishable key. Las contraseñas las gestiona Supabase Auth.
Actualización de configuración de despliegue Aula AI - 24/11/2026
