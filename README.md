# Port_Cautivo_UVM
# Sistema Web de Portal Cautivo para Acceso a Red Universitaria 🌐
### Universidad del Valle de México (UVM) — Campus Villahermosa 
**Materia:** Modelos y métodos para el desarrollo de software  
**Docente:** Manuel Antonio García Herrera  
**Fecha de Entrega (Sprint 1):** 18 de mayo de 2026  

---

## 👥 Equipo Integrador (Integrantes y Matrículas) 
* **David Alexandes Méndez León** — `620241280` 
* **Carlos Leonardo Mata Silva** — `620257664` 
* **José Raúl Zuñiga Montejo** — `620245089` 
* **Anahí Falcón Hernández** — `620244067` 
* **Luis Gonzalo Guzman Sánchez** — `620178462` 

---

## 📝 Descripción del Proyecto
Este repositorio aloja el desarrollo de la **Semana 1** del **Sistema Web de Portal Cautivo**. Es una solución tecnológica diseñada para optimizar la experiencia de conectividad de la comunidad estudiantil dentro del campus. 

El flujo de trabajo técnico, el control de versiones, el histórico de cambios y la integración colaborativa de los cinco integrantes están gestionados al 100% mediante **Git y GitHub**.

### ❗ Planteamiento del Problema
La red inalámbrica institucional **"UVM_estudiantes"** presenta intermitencias y dificultades de acceso para laptops y teléfonos inteligentes. El origen técnico del problema radica en el protocolo de autenticación avanzado **IEEE 802.1X**, el cual exige configuraciones manuales de certificados específicos y suplicantes que no todos los dispositivos de los alumnos manejan de forma nativa. Esto genera:
* Procesos de conexión complejos y pérdida de tiempo académico.
* Una experiencia de usuario (UX) deficiente.
* Una brecha latente de acceso digital interno.

### ✔️ Solución Propuesta
Se desarrolló un **Portal Cautivo (Captive Portal)** basado exclusivamente en el *Frontend* con tecnologías web nativas (HTML5, CSS3 y JavaScript). El sistema intercepta las peticiones HTTP del navegador del cliente no autenticado y las enruta automáticamente hacia nuestro formulario centralizado. 

> **Nota de Simulación Académica:** Para efectos del alcance de este proyecto integrador y con el fin de maximizar el rendimiento y la velocidad de carga en entornos de baja señal, la autenticación y la persistencia de sesión se ejecutan mediante lógica de simulación en el lado del cliente a través de *Cookies* de estado, prescindiendo de bases de datos pesadas en esta fase inicial.

---

## 🎯 Alcance del Sistema (Historias de Usuario - Sprint 1) 

### Funcionalidades Implementadas (Qué SÍ hace):
* **Redirección Automática (Historia 2):** El sistema intercepta la navegación simulada del cliente y lo redirige forzosamente a la vista de login sin configuraciones manuales.
* **Formulario de Autenticación (Historia 3):** Interfaz para la captura de matrícula y contraseña bajo reglas de validación predefinidas.
* **Mensajes de Error Dinámicos (Historia 4):** Manipulación del DOM para alertar visualmente al usuario si los datos ingresados no coinciden con los del entorno simulado.
* **Página de Bienvenida (Historia 5):** Interfaz limpia que confirma visualmente el éxito de la conexión a la red universitaria.
* **Soporte de Diseño Responsivo (Historia 6):** Maquetación adaptativa fluida diseñada específicamente para las pantallas de teléfonos celulares y tabletas.

### Exclusiones del Proyecto (Qué NO hace):
* No interactúa con la infraestructura física de red ni altera el ancho de banda del campus.
* No almacena información en bases de datos relacionales ni sistemas escolares reales.

---

## 🛠️ Stack Tecnológico de la Semana 1
* **Estructura y Semántica:** HTML5 (Texto plano ejecutable nativamente).
* **Estilos e Identidad Visual:** CSS3 (Implementación de Flexbox y Media Queries con la paleta institucional UVM).
* **Motor de Lógica y Estado:** JavaScript Vanilla (Control de eventos y simulación de persistencia de sesión por Cookies).
* **Herramienta Eje de Desarrollo:** Git (DVCS) y GitHub (Servidor remoto para el gobierno del código fuente).

---

## 📂 Arquitectura de Directorios del Repositorio
La estructura del proyecto se organizó de manera agnóstica para optimizar la colaboración y evitar la sobrecarga (*overhead*) de frameworks de compilación pesados:

```text
portal-cautivo-uvm/
├── .gitignore              # Archivos excluidos del versionado (configuraciones de IDEs)
├── README.md               # Documentación técnica e institucional del proyecto 
├── index.html              # Capa de interceptación y ruteo inicial (Historia 2) 
├── login.html              # Vista de autenticación y captura de credenciales (Historia 3) 
├── error.html              # Renderizado dinámico de fallas de validación (Historia 4) 
├── bienvenida.html         # Landing page de confirmación de acceso exitoso (Historia 5) 
├── css/
│   └── estilos.css         # Hojas de estilo responsivas optimizadas para móviles (Historia 6) 
└── js/
    └── autenticacion.js    # Script de lógica simulada de credenciales y manejo de cookies
