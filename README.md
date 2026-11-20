NutriControl Diario — Registro Nutricional por Fecha (PWA)

NutriControl Diario es una Progressive Web App (PWA) de archivo único (index.html) diseñada para calcular requerimientos calóricos y de macronutrientes, planificar comidas con anticipación o revisar días anteriores mediante un calendario diario, y contrastar en tiempo real cuánto te falta o sobra frente a tu meta nutricional.


Características principales1. Registro diario por fecha y planificación a futuroNavegador de fechas completo: Permite moverte día por día (Anterior / Siguiente), volver a Hoy con un toque o elegir cualquier fecha exacta mediante el selector de calendario (YYYY-MM-DD).


Control pasado y futuro: Puedes revisar lo que comiste hace semanas o planificar tu menú con 10 o más días de anticipación; cada fecha almacena de forma independiente sus comidas y totales.


Copiar menú entre días: Importa las comidas registradas en otra fecha hacia el día activo (sumándolas a lo existente o reemplazando el menú).2. Contraste en tiempo real (Falta vs. Sobra)Barras de progreso dinámicas: Compara automáticamente lo consumido en el día seleccionado frente a tu meta diaria en Calorías (kcal), Proteínas (g), Grasas (g) y Carbohidratos (g).


Indicadores claros: Muestra el porcentaje de avance y señala textualmente cuántos gramos o kilocalorías te faltan para alcanzar el objetivo o cuánto te sobra si lo superaste, además de contabilizar el peso total en gramos de los alimentos del día.3. 
Menú amigable y carga rápida
Organización por tiempos de comida: Desayuno, Almuerzo, Once / Colación y Cena.
Ingreso flexible: Permite registrar cualquier alimento indicando su peso total (g), proteínas (g), grasas (g) y carbohidratos (g). Si dejas las calorías en blanco, se calculan automáticamente con los factores de Atwater ($4\text{ kcal/g}$ proteína, $9\text{ kcal/g}$ grasa, $4\text{ kcal/g}$ carbohidrato).Presets con un clic: Incluye comidas cotidianas frecuentes y un plato completo precalculado de almuerzo ($849\text{ g}$ / $1.854\text{ kcal}$).4. Historial, seguimiento y exportación de datosVista cronológica: Lista todos los días con registros, mostrando fecha legible, etiqueta relativa (Hoy, Ayer, En X días), cumplimiento (En meta, Faltó o Excedido) y promedios del período seleccionado (Todos, Últimos 7 días, Últimos 30 días, Días futuros o Mes actual).Exportación e importación: Descarga todo tu historial en formato CSV (compatible con Excel y Google Sheets) o genera copias de seguridad completas en JSON para restaurarlas en otro dispositivo.5. Calculadora metabólica integrada (Mifflin-St Jeor + g/kg)Calcula tu Tasa Metabólica Basal (TMB) y tu Gasto Energético Total Diario (GETD) según sexo, edad, peso, altura y nivel de actividad física (PAL).Permite ajustar el porcentaje de déficit o superávit y definir proteínas y grasas en gramos por kilogramo de peso corporal ($\text{g/kg}$), asignando la energía restante a los carbohidratos.Estructura del proyectoEl proyecto está construido bajo una arquitectura zero-build contenida en un solo archivo para facilitar su mantenimiento y despliegue:/

├── index.html   # Aplicación completa (HTML5 + Tailwind CSS CDN + Lógica JS + Manifest/SW dinámico)
└── README.md    # Documentación del proyecto y guía de despliegue

Despliegue en GitHub y Vercel
Sube los archivos a GitHub:Crea un repositorio nuevo en GitHub.
Sube index.html y README.md a la rama principal (main).Publica en Vercel:Ingresa a Vercel y selecciona Add New → Project.Importa tu repositorio de GitHub.Mantén la configuración por defecto (Framework Preset: Other, sin comando de build) y haz clic en Deploy.Vercel generará una URL pública con certificado HTTPS (requisito indispensable para habilitar la instalación PWA).Instalación en el celular (PWA)Una vez abierta tu URL de Vercel en el navegador del teléfono:Android (Chrome / Edge / Samsung Internet):Pulsa el botón Instalar app en la barra superior de la aplicación (o abre el menú ⋮ del navegador).Selecciona Instalar aplicación o Agregar a pantalla principal.iPhone / iPad (Safari):Abre el enlace directamente en Safari.Toca el botón Compartir (cuadrado con flecha hacia arriba) y elige Agregar a inicio.Privacidad y almacenamientoTodos tus datos (perfil, metas y registros diarios por fecha) se guardan exclusivamente en el navegador de tu dispositivo mediante localStorage bajo la clave nutricontrol_diario_pwa_v1. No se envían datos personales a servidores externos; utiliza la función Respaldar JSON si deseas transferir tu historial entre dispositivos.
