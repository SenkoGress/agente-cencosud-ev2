# Sistema de Orquestación y Soporte Corporativo - Cencosud

Este repositorio contiene la implementación de un sistema de orquestación jerárquica diseñado para automatizar y gestionar las consultas de los colaboradores sobre las normativas y reglamentos internos de Cencosud. 

El sistema utiliza una arquitectura basada en agentes de software especializados y procesamiento de lenguaje natural para recuperar información documental y asegurar respuestas precisas y apegadas a la legalidad de la empresa.

## Arquitectura del Sistema

La solución está construida sobre el framework CrewAI, implementando un flujo de tipo `Process.hierarchical` para garantizar la correcta toma de decisiones y delegación de tareas automatizadas.

1. **Gerente de Recursos Humanos (Manager):** Actúa como orquestador del sistema. Recibe la consulta del usuario, evalúa los requerimientos y delega las tareas de búsqueda y redacción a los subprocesos correspondientes. No ejecuta búsquedas en bases de datos por sí mismo.
2. **Analista Senior de Políticas Internas:** Módulo técnico encargado de la recuperación de información. Utiliza herramientas de búsqueda semántica (FAISS) para extraer fragmentos exactos de los reglamentos internos preprocesados.
3. **Especialista en Comunicaciones Internas:** Módulo responsable del formato de salida. Genera respuestas estructuradas, claras y que cumplen con las directrices de comunicación corporativa.

## Requisitos Previos

- Python 3.10 o superior.
- Git.
- Token de acceso (Fine-grained) con permisos de ejecución en repositorios y modelos.

## Instalación y Configuración

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/SenkoGress/agente-cencosud-ev2.git](https://github.com/SenkoGress/agente-cencosud-ev2.git)
   cd agente-cencosud-ev2

   # Asistente de Recursos Humanos Cencosud - Observabilidad y Trazabilidad

# Asistente de Recursos Humanos Cencosud - Observabilidad y Trazabilidad

Este proyecto implementa un agente de IA especializado en consultas internas de RRHH. Incorpora un sistema de observabilidad y trazabilidad que permite monitorear el rendimiento (KPIs), identificar anomalías y asegurar protocolos de ética y privacidad en las respuestas.

## Estructura del Proyecto
- `app.py`: Orquestador principal del agente (CrewAI).
- `dashboard.py`: Dashboard interactivo en Streamlit para visualizar logs y métricas.
- `tools.py`: Herramientas personalizadas para la búsqueda de políticas y evaluación de riesgos.
- `trazabilidad_cencosud.log`: Registro de eventos del sistema.

## Configuración y Ejecución

### Requisitos previos
- Python 3.10 o superior.
- Tener configuradas las llaves de API necesarias.

### Instalación
1. Clonar el repositorio: `git clone https://github.com/SenkoGress/agente-cencosud-ev2.git`
2. Crear un entorno virtual: `python -m venv venv`
3. Activar el entorno:
   - Windows: `venv\Scripts\activate`
   - Linux/Mac: `source venv/bin/activate`
4. Instalar dependencias: `pip install -r requirements.txt`

### Configuración de Credenciales
1. Renombra el archivo `.env.example` a `.env`.
2. Abre el archivo `.env` y completa las credenciales (API Keys, Token de GitHub, etc.).

### Uso del Sistema
- **Ejecutar el Asistente:** `python app.py` (Escribe 'salir' para terminar).
- **Visualizar Dashboard de Observabilidad:** `streamlit run dashboard.py`
