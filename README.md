# data-incident-copilot
POC de Prompt Engineering para análisis y comunicación de incidentes de calidad de datos.
 POC implementa un copiloto para el análisis de incidentes de calidad de datos. El notebook consume un dataset CSV desde GitHub, selecciona un incidente y construye dos alternativas de instrucciones para un modelo de IA: un prompt básico y un prompt optimizado.

El prompt optimizado incorpora técnicas de Fast Prompting, como definición de rol, contexto delimitado en JSON, reglas para evitar afirmaciones no verificadas, ejemplo few-shot, solicitudes de SQL exclusivamente de validación y una salida JSON estructurada.

La conexión con la API se configuró mediante Colab Secrets, evitando exponer la clave en el repositorio. Durante las pruebas, la API respondió con el error 429 insufficient_quota debido a la falta de créditos; por ello se aplicó manejo controlado del error y no se ejecutaron reintentos automáticos.

Aunque no se obtuvieron respuestas generadas por falta de saldo en la API, la comparación metodológica muestra que el prompt optimizado ofrece mayor consistencia, seguridad, trazabilidad y potencial de automatización que el prompt básico.
