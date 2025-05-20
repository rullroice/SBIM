# Tunomático – Sistema de Turnos

## Introducción

**Tunomático** es un sistema de gestión de turnos digitales diseñado para optimizar el flujo de atención en instituciones con alto volumen de clientes o pacientes. Permite organizar las colas de espera de forma eficiente, reduciendo los tiempos de espera y mejorando la experiencia de los usuarios al brindarles información clara sobre su posición en la fila y manteniendo un orden de atención justo.

La plataforma ofrece a los usuarios una manera de tomar un ticket virtual y conocer en tiempo real el estado de la fila, al mismo tiempo que el personal puede administrar la atención de manera ordenada y transparente.

El sistema abarca componentes como quioscos digitales o aplicaciones web para la solicitud de turnos, pantallas de visualización que anuncian el número de turno en curso, y un panel de administración para el personal encargado. De esta manera, Tunomático cubre todo el ciclo de atención: desde que el usuario solicita un turno hasta que es atendido.

Además, proporciona herramientas de seguimiento, notificaciones al usuario cuando su turno se aproxima, y generación de reportes, todo ello dentro de una solución integral que busca agilizar la atención al público sin sacrificar la calidad del servicio.

---

## Patrones de Diseño Aplicados

### Patrones Creacionales

- Singleton: Se utilizó el patrón Singleton para gestionar instancias únicas de componentes centrales, como el Administrador de Turnos. Este patrón garantiza que exista una sola instancia encargada de coordinar la asignación y seguimiento de turnos en todo el sistema, evitando inconsistencias y facilitando el acceso global a este recurso compartido.

- Prototype: Se aplicó el patrón Prototype para la clonación de objetos complejos en lugar de crearlos desde cero repetidamente. Se definieron plantillas (prototipos) para configurar servicios de atención estándar, generando nuevas configuraciones copiando y modificando el prototipo inicial.

### Patrones Estructurales

- Adapter (Adaptador): Para integrar Tunomático con dispositivos y servicios externos se implementó el patrón Adapter. Por ejemplo, se adaptó la comunicación con el BotonFisico mediante la clase PuestoAdapter, permitiendo que el sistema se comunique sin cambiar su interfaz central.

- Fachada (Facade): No explícito en el diagrama, pero puede inferirse en la interfaz simplificada de SistemaTurnos, que orquesta operaciones de generación y avance de turno desde un punto cent


---

## Diagramas del Sistema

### 📌 Diagrama de Casos de Uso

Representa los actores (Cliente, Empleado) y casos de uso (tomar turno, avanzar turno, imprimir ticket, etc.)

Patrones implicados:

Este diagrama refleja relaciones <<include>> obligatorias como parte del flujo principal de negocio, que ayudan a modularizar el comportamiento y garantizar reuso.

![Caso de uso](https://github.com/user-attachments/assets/c798f956-26d9-4821-91d9-6c0ed77c30ec)

---

### 📌 Diagrama de Clases

Diseño lógico con clases como Turno, Puesto, SistemaTurnos, patrones Singleton, Prototype, Adapter.

Patrones aplicados visiblemente:

Turno → <<Prototype>>

SistemaTurnos → <<Singleton>>

PuestoAdapter → <<Adapter>>

Interacción de Puesto con SistemaTurnos usando el patrón Observer para notificar cambios.

![Diagrama de Caso de Uso](https://github.com/user-attachments/assets/f496cef0-24b3-4233-8be8-b4aec0c964ab)

---

### 📌 Diagrama de Implementación

Muestra la arquitectura física: servidor, puestos de atención, pantallas, conexiones LAN/video, delegación y comunicación.

Patrones representados en despliegue:

Los .jar independientes en Servidor Central y Puesto de Atención reflejan modularidad basada en los patrones estructurales.

La delegación de Boton → PuestoAdapter → Puesto es aplicación directa de Adapter.

Las conexiones físicas permiten aplicar el principio de separación de responsabilidades entre nodos.

![Implementacion UML](https://github.com/user-attachments/assets/a98539fc-c2dc-4e08-b525-7224dd8e2fbc)

---

## De la Visión Funcional al Diseño Lógico y Físico

Esta es la transición que todo arquitecto debe lograr:

- Desde la **visión funcional**, que describe qué hace el sistema y quién lo usa.
- Pasando al **diseño lógico**, aplicando patrones sobre una estructura robusta.
- Hasta llegar al **diseño físico**, donde los módulos se despliegan en componentes reales.

Esto permite:

- ✅ Diseñar sistemas escalables y mantenibles.
- ✅ Comunicar claramente la arquitectura.
- ✅ Entender cómo los patrones impactan el código y la infraestructura.

---

## Reflexión Final

El modelado y diseño de **Tunomático** demostró que una arquitectura sólida mejora la calidad del software y la experiencia del usuario. Gracias al uso de patrones de diseño, se logró flexibilidad, claridad y modularidad en cada componente.

> “Para que no se pierda el factor humano.”

---

## Créditos

Este proyecto es parte de un ejercicio académico para modelar la arquitectura de un sistema realista utilizando buenas prácticas y patrones de diseño reconocidos.




