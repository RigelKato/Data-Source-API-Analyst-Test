# Data-Source-API-Analyst-Test

## Objetivo
Este repositorio contiene la práctica para la vacante de Data Source API Analyst, enfocada en la extracción de datos usando la API de GitHub.

## Estructura del repositorio

- **README.md**: Documentación general y resumen del proyecto.
- **Content/**: Documentos y código relacionado con la autenticación, endpoints, manejo de errores, paginación, y guías de solución de problemas.
- **Postman_Collection/**: Colección Postman o notebooks para probar los endpoints de la API.

## Paso 1: Investigación de la API de GitHub

### Endpoints principales:
- Búsqueda de repositorios públicos (`search/repositories`)
- Listado de commits (`repos/{owner}/{repo}/commits`)
- Contenidos de repositorios (`repos/{owner}/{repo}/contents/{path}`)

### Aspectos importantes:
- Paginación para manejar múltiples resultados.
- Manejo de límites de tasa (rate limits).
- Autenticación mediante tokens personales.

## Paso 2: Configuración del repositorio

- Crear repositorio público en GitHub con el nombre `Data-Source-API-Analyst-Test`.
- Subir la estructura y archivos iniciales.

## Paso 3: Uso de Postman o Google Colab para extracción

- Implementar las pruebas de extracción de datos en Postman o en un notebook de Colab.
- Incluir manejo de errores y paginación.

## Paso 4: Guía de solución de problemas

- Documentar errores comunes (401, límites de tasa, variables de entorno).

## Paso 5: Resultados

- Exportar colección Postman o notebook y subirlos al repositorio.

---

*Este repositorio es una base para completar la práctica de Data Source API Analyst.*

### Reflexión Final:
Esta tarea fue una valiosa experiencia de aprendizaje. Antes de empezar, no tenía experiencia con API, repositorios de GitHub ni Google Colab. A lo largo del proyecto, investigué la API de GitHub, gestioné la autenticación y aprendí a gestionar la paginación y los límites de velocidad con Python. A pesar de la confusión inicial, completé con éxito todos los pasos y ahora me siento más seguro trabajando con extracción de datos y flujos de trabajo basados en API. Este ejercicio me proporcionó conocimientos prácticos y reforzó mis habilidades de resolución de problemas y resiliencia.
