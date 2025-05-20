# Tunomático – Sistema de Gestión de Turnos Digitales

## Introducción

**Tunomático** es un sistema de gestión de turnos digitales diseñado para optimizar el flujo de atención en instituciones con alto volumen de clientes o pacientes. Permite organizar las colas de espera de forma eficiente, reduciendo los tiempos de espera y mejorando la experiencia de los usuarios al brindarles información clara sobre su posición en la fila y manteniendo un orden de atención justo.

El sistema cubre todo el ciclo de atención: desde que el usuario solicita un turno hasta que es atendido. Además, proporciona herramientas de seguimiento, notificaciones al usuario y generación de reportes, todo dentro de una solución integral.

---

## Patrones de Diseño Aplicados

### Patrones Creacionales

- **Singleton:** Control de instancia única para `SistemaTurnos`.
- **Prototype:** Clonación de objetos `Turno` para eficiencia y escalabilidad.

### Patrones Estructurales

- **Adapter:** Integración de `BotonFisico` mediante `PuestoAdapter`.
- **Facade:** Interfaz simplificada hacia `SistemaTurnos`.

### Patrones de Comportamiento

- **Observer:** Comunicación reactiva para pantallas y notificaciones.
- **Strategy:** Políticas intercambiables para asignación de turnos.

---

## Diagramas del Sistema

### 📌 Diagrama de Casos de Uso UML

Representa actores y funcionalidades principales del sistema.

![Caso de uso](https://github.com/user-attachments/assets/c798f956-26d9-4821-91d9-6c0ed77c30ec)

---

### 📌 Diagrama de Clases UML

Representación lógica del sistema, incluyendo clases, atributos, métodos y patrones aplicados.

![Diagrama de Caso de Uso](https://github.com/user-attachments/assets/f496cef0-24b3-4233-8be8-b4aec0c964ab)

---

### 📌 Diagrama de Implementación UML

Modelo físico del despliegue de componentes en nodos reales.

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




