# ⚡ ElectroNexo:  Esquemas Electrónicos

**ElectroNexo** es un motor de ingeniería diseñado para la interpretación, segmentación y estabilización de esquemas
electrónicos complejos. Utiliza una arquitectura de procesamiento de imágenes para transformar esquemas estáticos en
topologías digitales claras y funcionales.

---

## ⚙️ Arquitectura de Procesamiento

El núcleo de la aplicación reside en un **Pipeline de Estabilización**, que procesa la información en capas lógicas para
garantizar la integridad de los datos técnicos y la conectividad galvánica:

### 1\. Segmentación de Capas (Layering)

Para evitar errores de continuidad, el sistema implementa una segregación estricta de elementos:

-   **Identificación de Componentes (Azul/Cian):** Mediante **Clausura Morfológica**, el sistema detecta geometrías base
    y las resalta para facilitar su inspección visual.
-   **Nodos de Conexión (Fucsia/Magenta):** Localización de puntos de unión críticos y terminales.
-   **Conductores (Negro):** Segmentación de trazos eléctricos para análisis de red.

### 2\. Normalización de Terminales (Surgical Clipping)

Técnica diseñada para garantizar la visibilidad de los puntos de anclaje en los terminales del circuito:

1.  **Márgenes de Seguridad:** Genera zonas de despeje alrededor de los nodos para evitar solapamientos visuales.
2.  **Operación de Diferencia Topológica:** Asegura que los conductores no obstruyan la geometría de los pines.
3.  **Resultado:** Los terminales permanecen accesibles para el trazado de redes y la inspección de nodos.

---

## 🧠 Características Principales

-   **Visor WebGL de Alto Rendimiento:** Visualización fluida con sincronización nativa mediante
    ```
    QWebChannel
    ```
    , eliminando retardos en la carga de archivos grandes.
-   **Entorno de Investigación Integrado:** Navegador técnico basado en
    ```
    CustomWebView
    ```
    para la consulta directa de _datasheets_ y documentación PDF sin salir de la interfaz.
-   **Reconocimiento de Geometría:** Algoritmos de visión artificial para la detección de símbolos y etiquetas de texto
    en esquemas complejos.
-   **Gestión de Proyectos por Hash:** Sistema de caché basado en firmas SHA-256 para evitar conflictos de datos entre
    diferentes versiones de un mismo proyecto.

---

## 📥 Descarga e Instalación (v2.1 Estable)

> [!IMPORTANT] >
> [**🚀 Descargar ElectroNexo_Instalador.exe**](https://github.com/Ccom5/Nexo-/releases/download/v2.0.0/ElectroNexo_Instalador.exe)  
> _Versión Estable | 175 MB | Verificado vía SHA-256_

### ⚠️ Aviso sobre la Seguridad de Windows (SmartScreen)

Al ejecutar el instalador por primera vez, es muy probable que Windows muestre una ventana azul con el mensaje
**"Protección de Microsoft Defender"**.

**¿Por qué sucede esto? ** Nexo es un proyecto independiente y gratuito. Para eliminar esta
advertencia, Microsoft requiere el pago de una licencia de desarrollador de alto costo, la cual hemos decidido no
adquirir para mantener el software libre de cargos para el usuario final.

**Pasos para instalar sin problemas:**

1. En la ventana azul de Windows, haz clic en el enlace **"Más información"**
2. Aparecerá un botón nuevo llamado **"Ejecutar de todas formas"**
3. Haz clic en él para iniciar el asistente de instalación

_Este software ha sido analizado y es completamente seguro para su uso._ ElectroNexo se distribuye
como un ejecutable optimizado mediante **Nuitka** para garantizar un despliegue eficiente en sistemas Windows.

### 🏁 Guía Rápida:

1.  **Ejecuta el instalador** en tu estación de trabajo.
2.  **Consulta el [Manual de Configuración Inicial](https://github.com/Ccom5/GF-ElectroNexo/index.html)** para el proceso
    de vinculación de hardware.
3.  **Periodo de Evaluación:** El sistema permite hasta **15 ejecuciones de prueba** con funcionalidad completa antes de
    requerir activación.

---

## ⚖️ Filosofía y Licencia

ElectroNexo sigue la premisa de soberanía de datos y transparencia técnica:

-   **Distribución de Binarios:** Para garantizar la integridad del motor de ingeniería, la distribución se realiza
    mediante binarios compilados.
-   **Activación por Hardware:** La licencia se vincula de forma cifrada al **Machine ID** (UUID de placa base) del
    equipo.
-   **Persistencia de Datos:** Al finalizar el periodo de prueba, se mantienen las funciones esenciales y la integridad
    de los análisis ya realizados.

---

| Módulo               | Tecnología                                          |
| -------------------- | --------------------------------------------------- |
| **Motor Geométrico** | Shapely (Validación de topología anti-degeneración) |
| **Renderizado**      | Three.js (WebGL) con backend Python                 |
| **Seguridad**        | Cifrado AES para persistencia de licencias locales  |
