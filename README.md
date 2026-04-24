# Sistema de Monitoreo y Control para la Optimización de Cultivos de Setas Rosas (Pleurotus djamor)

Este repositorio contiene el desarrollo técnico, firmware y documentación del sistema de monitoreo y control diseñado como proyecto de titulación para la carrera de **Ingeniería en Control y Automatización** de la **ESIME Zacatenco - IPN**.

## Propósito del Proyecto
El objetivo principal de este sistema es automatizar y optimizar las condiciones ambientales dentro de un hábitat controlado para la producción de setas rosas (*Pleurotus djamor*). Mediante la implementación de tecnologías IoT y un enfoque de control modular, el sistema busca reducir la tasa de error humano, maximizar el rendimiento del cultivo y proporcionar una herramienta de análisis de datos para la mejora continua del modelo biológico.

## Variables y Rangos de Operación
Para asegurar el crecimiento óptimo del hongo, el sistema monitorea y regula las siguientes variables críticas:

* **Temperatura:** Mantenida en un rango de **24°C a 28°C**.
* **Humedad Relativa (HR):** Controlada estrictamente entre el **80% y el 90%**.
* **Iluminación:** Ciclos controlados para estimular la fructificación.
* **Ventilación/CO2:** Extracción programada para evitar la acumulación de dióxido de carbono y mantener la oxigenación del sustrato.

## Integración de Tecnologías y Conectividad
El sistema destaca por su capacidad de interconectividad y gestión de datos en tiempo real mediante tres ejes principales:

1.  **Telegram API:** Se utiliza como un canal de mensajería crítica. El sistema envía alertas en tiempo real y reportes de estado directamente al usuario, permitiendo una supervisión remota sin necesidad de estar presente en el sitio de cultivo.
2.  **Remote XY:** Implementado para generar una Interfaz Hombre-Máquina (HMI) móvil. A través de esta aplicación, se pueden visualizar gráficas en tiempo real y forzar el accionamiento de actuadores de forma manual desde un smartphone.
3.  **Google Sheets (Base de Datos Cloud):** Funciona como el núcleo de persistencia de datos. El sistema almacena la información recolectada en una hoja de cálculo con más de **19,000 registros** organizados en **7 columnas** (Timestamp, Temperatura, Humedad, Estado de Actuadores, etc.). Esta infraestructura permitió un flujo de datos constante para el análisis posterior.

## Análisis de Datos y Modelo Matemático
La robustez del control se fundamenta en el análisis de la información almacenada en la nube:
* **Procesamiento:** Los datos recolectados se exportaron a **MATLAB** para su tratamiento estadístico.
* **Optimización:** Se aplicaron métodos de **Mínimos Cuadrados** y **Distancias Ortogonales** para ajustar el modelo matemático del sistema.
* **Resultado:** Esto permitió obtener una respuesta del sistema mucho más precisa, compensando las inercias térmicas y de humedad propias del hábitat de cultivo.

## Características del Sistema
* **Modularidad:** El diseño electrónico y de software es modular, lo que facilita el mantenimiento y la sustitución de sensores o actuadores sin afectar la lógica central.
* **Escalabilidad:** Gracias a la arquitectura basada en microcontroladores con capacidad WiFi y el uso de servicios en la nube, el sistema puede escalarse para controlar múltiples naves de cultivo simultáneamente.
* **Análisis Histórico:** Capacidad de auditoría completa del ciclo de crecimiento gracias al volumen de datos masivo recolectado.

---
**Autores:**
* Jair De Jesus Nava Cisneros
* Oswaldo De Los Santos Hernandez

**Institución:** Instituto Politécnico Nacional - ESIME Zacatenco
