Roadmap de Desarrollo: Padel Pro Manager (Propuesta)
Este documento describe el plan de desarrollo por fases para la aplicación web de gestión de profesores de pádel y tenis. El objetivo es lanzar un Producto Mínimo Viable (MVP) enfocado y luego escalar la funcionalidad de manera iterativa.
🎯 Perfil de Usuario (User Persona)
Nombre: Profesor Independiente (Ej: "Profe Carlos").
Necesidad Principal: Organizar su agenda de clases, que es variable y caótica.
Dolor (Problema): Pierde la cuenta de quién le pagó, cuánto gastó en arriendos y no sabe cuál es su ganancia real a fin de mes.
Objetivo con la App: Tener claridad total sobre su agenda y su rentabilidad mensual en un solo lugar.
🚀 Fase 1: El MVP (Producto Mínimo Viable)
Objetivo: Lanzar la versión funcional más simple que resuelva los problemas centrales: Agenda, Cobros y Ganancias.
1. Módulo de Autenticación y Configuración Inicial
[ ] Login/Registro: Que el profesor pueda crear una cuenta (Email/Contraseña).
[ ] Configuración del Profesor:
[ ] Poder definir sus "Tipos de Clase" (Individual 60m, Dupla 60m, etc.) con sus precios base.
[ ] Poder crear sus "Clubes" (solo nombre y dirección, ej: "Club Padel Norte").
2. Módulo de Alumnos (CRM Básico)
[ ] Crear/Editar Alumno: Una lista simple de alumnos.
[ ] Ficha de Alumno: Guardar (Nombre, Teléfono, Email). Los campos adicionales (RUT, notas) se dejan para Fase 2.
3. Módulo de Agenda (El Corazón de la App)
[ ] Vista de Calendario: Un calendario visual (día, semana, mes).
[ ] Crear Evento/Clase: Al hacer clic en el calendario, debe poder:
[ ] Seleccionar el "Tipo de Clase" (carga el precio automático).
[ ] Seleccionar el/los "Alumno(s)" de su lista.
[ ] Seleccionar el "Club" donde será la clase.
[ ] Añadir una nota simple (ej: "Cancha 3").
[ ] Definir fecha y hora.
[ ] Editar/Cancelar Clase: Poder modificar o eliminar una clase agendada.
4. Módulo de Finanzas (Registro Manual)
[ ] Estado de Pago de la Clase: En el detalle de la clase (en el calendario), debe haber un botón/switch para marcarla como "Pagada" o "Pendiente".
[ ] Registro de Costos: Una sección simple para añadir costos variables:
[ ] Concepto (ej: "Arriendo Cancha 2", "Tarro de Pelotas").
[ ] Monto (CLP).
[ ] Fecha.
[ ] Dashboard Básico: Una sola pantalla con 3 métricas clave (para el mes actual):
[ ] Total Ingresos (Suma de clases "Pagadas").
[ ] Total Costos (Suma de costos registrados).
[ ] Ganancia Neta (Ingresos - Costos).
📈 Fase 2: Potenciando la Gestión y el Seguimiento
Objetivo: Mejorar la relación con el alumno y automatizar tareas repetitivas.
1. Módulo de Alumnos (CRM Avanzado)
[ ] Ficha de Alumno Completa: Añadir campos:
[ ] "Posición en pista", "Nivel", "Notas de Progreso".
[ ] Historial del Alumno: Una vista que muestre:
[ ] Todas las clases tomadas (con acceso a las notas de esa clase).
[ ] Historial de pagos y deudas.
[ ] Notas por Clase: Poder añadir notas específicas a esa clase (ej: "Mejorar volea de revés") que se guarden en el historial del alumno.
2. Módulo de Clases Recurrentes y Packs
[ ] Clases Recurrentes: Al crear una clase, poder marcarla para que se repita (ej: "Cada martes a las 10:00").
[ ] Gestión de Packs:
[ ] Poder "vender" un pack (ej: "Pack 8 clases") a un alumno, registrando el pago total.
[ ] Al agendar una clase, poder marcarla como "Usar clase del pack".
[ ] En la ficha del alumno, ver "Le quedan 3 de 8 clases".
3. Módulo de Notificaciones (Integración)
[ ] Recordatorios: Enviar un recordatorio (vía Google Calendar o WhatsApp) al alumno 12-24h antes de la clase. Esto requiere una integración externa.
📊 Fase 3: Inteligencia de Negocio y Escalabilidad
Objetivo: Dar al profesor herramientas de análisis para tomar mejores decisiones.
1. Dashboard Avanzado y Reportes
[ ] Gráficos Financieros:
[ ] Evolución de Ganancia Neta (últimos 6 meses).
[ ] Gráfico de Torta: "Costos por Club" (para ver dónde arrienda más).
[ ] Gráfico de Torta: "Ingresos por Tipo de Clase".
[ ] Metas: Poder definir una "Meta de Ganancia Mensual" y ver el progreso en el dashboard.
[ ] Reportes de Alumnos:
[ ] Ranking: "Top 5 Alumnos por N° de Clases".
[ ] Ranking: "Top 5 Alumnos por Ingresos".
[ ] Exportar a Excel: Poder descargar reportes de ingresos/costos.
2. Gestión Multi-Profesor (SaaS)
[ ] Roles y Permisos: Preparar la app para que una "Academia" pueda registrarse y añadir a sus profesores, cada uno con su propia agenda y finanzas (pero bajo una misma cuenta de pago).
💡 Sugerencias Técnicas (Stack Inicial)
Para una App Web moderna, rápida de desarrollar y escalar:
Frontend (Lo que ve el usuario): React (con Vite). Es el estándar de la industria.
Backend (Lógica y Base de Datos): Firebase.
Firestore (Base de Datos): Ideal para guardar alumnos, clases y costos.
Authentication: Soluciona el Login de forma segura.
Hosting: Publica la App Web fácilmente.
Componentes de UI: Shadcn/UI o Material-UI (MUI) para tener componentes listos (calendarios, botones, modales) y acelerar el desarrollo.
