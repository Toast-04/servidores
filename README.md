# Aplicaciones web: teoría y tareas

Resúmenes 01 y 02 fusionados como teoría de examen; resúmenes 02 a 06 como tareas realizadas.

[Teoría](#t1)[Tareas realizadas](#tareas)[R3 Navegadores](#r3)[R4 Cliente-servidor](#r4)[R5 Servidores web](#r5)[R6 XAMPP](#r6)

## Parte I. Teoría

### 1. Conceptos básicos

**Situación actual.** El auge del móvil obliga a que las apps web sean *responsive* y compatibles con muchos dispositivos. El patrón **MVC** domina el modelo, el diseño y el control de la página, con **HTML5, CSS3 y JavaScript** como estándar en el cliente. Con la nube, el peso computacional recae en los servidores y se reduce la dependencia del hardware del usuario.

**Qué es una aplicación web.** Software que se ejecuta en el navegador sin instalación, de modo que el rendimiento depende del servidor y no del hardware del cliente. Su éxito se debe a la universalidad del navegador: no hay que compilar para cada dispositivo ni lidiar con las particularidades del cliente.

**Dependencias.** Dependen del navegador y de la conexión a Internet, por eso suelen ser menos potentes que las de escritorio y solo acceden al sistema operativo a través del navegador. Cualquier lenguaje de cliente necesita que el navegador lo interprete; **JavaScript** es el estándar por su compatibilidad universal.

### 2. Ventajas y desventajas

### Ventajas

- Compatible con múltiples dispositivos
- Requiere menos hardware que una app de escritorio
- Sin instalación y mantenimiento fácil
- Compatible con otro software (salvo el navegador)
- Uso sencillo, desde cualquier dispositivo o ubicación
- Datos centralizados

### Desventajas

- Menor potencia en tareas especializadas (vídeo, audio, juegos, imágenes)
- Desaprovechan el hardware y requieren conexión a internet
- Se delega el control de la información si el servidor no es propio
- Mayor riesgo de seguridad

### 3. Evolución de la Web

- **Web 1.0:** páginas estáticas sin interacción; documentos con texto, imágenes e hipervínculos.
- **Web 2.0:** aplicaciones ricas equiparables al escritorio (Google Docs, Office 365), arquitectura **SOA** (hoy microservicios) y web social.
- **Web 3.0:** nace de la competencia entre navegadores, que impulsa el front-end; incorpora la web inteligente (IA, bots, deep learning) y la web semántica con metadatos.

### 4. Visiones de las aplicaciones web

Hay dos vertientes, lado cliente y lado servidor, que añaden elementos al HTML para que se interprete en el navegador.

- **Lado cliente:** HTML, CSS y JS.
- **Lado servidor:** traduce el código (por ejemplo PHP) a lo que el navegador entiende antes de entregarlo, mediante HTTP/HTTPS. Ejemplos: PHP, Ruby, Node.js.

### 5. Arquitectura en tres niveles

**1. Capa de presentación:** HTML, CSS y JS mostrados al usuario en el navegador.

**2. Capa de lógica de negocio:** MVC en el servidor de aplicaciones.

**3. Capa de datos:** bases de datos.

### 6. Tecnologías web

- **Backend:** lenguajes de script de servidor que se incrustan en el HTML y requieren una extensión especial para que el servidor sepa traducirlos (PHP, ASP.NET…).
- **Frameworks MVC:** marco de trabajo para resolver aplicaciones de forma eficiente y segura (Laravel, Angular, Spring…).
- **Móviles:** llevar los servicios de internet al móvil dio lugar a dos tipos de apps: **nativas** (lenguaje del propio dispositivo) y **web apps** (aplicaciones web con interfaz responsive).

## Parte II. Tareas realizadas

| Resumen | Tema | Estado |
| --- | --- | --- |
| 02 | Introducción a las aplicaciones web 2 (recogido en la teoría, apartados 4 a 6) | Realizada |
| 03 | Comparación de capacidades web (navegadores) | Realizada |
| 04 | Modelo cliente-servidor (tres capas) | Realizada |
| 05 | Características de servidores web | Realizada |
| 06 | XAMPP | Realizada |

### Resumen 03. Navegadores

Comparativa de Chrome, Firefox, Safari y Edge. **Conclusión:** cada motor (Blink, Gecko, WebKit) puede interpretar el código de forma distinta, así que conviene probar toda app web en al menos un navegador de cada motor.

|  | Chrome | Firefox | Safari | Edge |
| --- | --- | --- | --- | --- |
| Motor | Blink | Gecko | WebKit | Blink |
| Plataformas | Windows, macOS, Linux, ChromeOS, Android, iOS | Windows, macOS, Linux, Android | macOS, iOS, iPadOS | Windows, macOS, Linux, Android, iOS |
| Sincronización | Cuenta Google | Cuenta Firefox (con containers) | iCloud (con handoff) | Cuenta Microsoft (integración 365) |
| Extensiones | Chrome Web Store, el más amplio | Buen catálogo, Manifest V2 | App Store Web Extensions, limitado | Chrome Web Store + propio |
| Privacidad | Sin protección de seguimiento relevante | Enhanced Tracking Protection, Total Cookie Protection | Intelligent Tracking Prevention | Prevención de seguimiento + cookie protection |
| IA integrada | Gemini | Limitado | Apple Intelligence | Copilot |

**Herramientas de desarrollo.** Acceso con F12 o Ctrl+Shift+I (Safari: Cmd+Opt+I). Todas incluyen inspector DOM/CSS, consola JS, depurador (breakpoints, paso a paso), panel de red, rendimiento, emulación de dispositivos, accesibilidad y automatización.

- **Chrome:** Lighthouse, Memory Inspector, Puppeteer/ChromeDriver, panel de aplicaciones.
- **Firefox:** inspector con box model, animaciones y grid; Shape Editor; Marionette/WebDriver.
- **Safari:** Web Inspector, perfilado de funciones JS y selectores CSS, WebDriver, timelines.
- **Edge:** heredado de Chromium; panel Issues con recomendaciones; Edge WebDriver.

### Resumen 04. Modelo cliente-servidor

La arquitectura de tres capas es una evolución del enfoque cliente-servidor: separa la aplicación en presentación, lógica de negocio y acceso a datos.

- **Presentación:** lo que ve el usuario; muestra información y recoge sus acciones.
- **Lógica de negocio:** reglas y operaciones; recibe las acciones, las procesa y decide las consecuencias.
- **Acceso a datos:** se comunica con la base de datos para hacer consultas.

### Ventajas

- Mayor organización
- Mantenimiento más fácil (capas independientes)
- Mayor escalabilidad
- Mejor seguridad (datos apartados del cliente)
- Reutilización de la lógica
- Trabajo en equipo

### Desventajas

- Mayor complejidad
- Mayor coste inicial
- Más comunicaciones: puede añadir latencia
- Mayor necesidad de planificación

### Resumen 05. Servidores web

|  | Apache | Nginx | Microsoft IIS |
| --- | --- | --- | --- |
| Desarrollador | Apache Software Foundation | NGINX, Inc. | Microsoft |
| Sistemas operativos | Linux, Windows, macOS, Unix | Linux, Windows, Unix | Windows |
| Código abierto | Sí | Sí | No |
| Contenido estático | Sí | Sí, muy eficiente | Sí |
| Ejecutar PHP | PHP-FPM / FastCGI | PHP-FPM / FastCGI | FastCGI |
| Proxy inverso y balanceo | Sí | Sí | Sí |
| Configuración | Flexible y modular | Archivos de configuración | IIS Manager y archivos |
| Uso habitual | Servidores web y apps PHP | Alto tráfico, proxy inverso, estático | Entornos Windows y empresariales |
| Instalar para PHP | Apache + PHP + PHP-FPM/FastCGI | Nginx + PHP + PHP-FPM | IIS + CGI/FastCGI + PHP para Windows |

- **Apache:** destaca por su modularidad y flexibilidad; soporta HTTP/HTTPS, autenticación y proxy inverso. Hay que configurar las peticiones `.php`.
- **Nginx:** arquitectura pensada para aguantar muchas conexiones. No ejecuta PHP directamente, necesita un intérprete; se configura con `fastcgi_pass` (.php a PHP-FPM).
- **IIS:** integrado en Windows Server, orientado a ASP.NET; soporta PHP vía FastCGI mapeando `.php` a `php-cgi.exe`.

### Resumen 06. XAMPP

Paquete de software libre para crear un servidor web local, útil para desarrollar y probar aplicaciones. Incluye Apache, MariaDB, PHP…

- **Siglas:** X (multiplataforma), A (Apache), M (MySQL), P (PHP), p (Perl).
- **Adecuado para desarrollo y aprendizaje:** permite trabajar sin conexión, es cómodo con PHP y bases de datos, sirve para testear antes de lanzar y es sencillo de instalar.
- **Límite:** no es la mejor opción para producción de muchas aplicaciones web.
