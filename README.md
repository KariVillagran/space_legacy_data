# Proyecto de Datos Legacy de la Agencia Espacial Universal (AEU)

Este proyecto proporciona los datos necesarios para un desafío de migración y modernización de procesos batch, enfocado en la transformación de sistemas legacy de la Agencia Espacial Universal (AEU). Los datos están organizados en archivos CSV que representan distintos informes y operaciones del sistema legacy actual.

## Estructura del Proyecto

El proyecto contiene la siguiente estructura de directorios y archivos.

### Archivos CSV

Los archivos en el directorio `data/` representan los distintos tipos de datos legacy que se utilizarán en los procesos batch:

1. **`colisiones_meteoritos_diarios.csv`**: 
   - Contiene información diaria sobre trayectorias de meteoritos y posibles colisiones. Los errores simulados incluyen coordenadas fuera de rango, fechas mal formateadas y niveles de riesgo no especificados.

2. **`distancias_estelares_mensuales.csv`**: 
   - Proporciona registros mensuales de distancias entre planetas o cuerpos celestes. Incluye problemas como distancias negativas, errores tipográficos en nombres de planetas y formatos de fecha inconsistentes.

3. **`combustible_estelar_anual.csv`**: 
   - Incluye el historial anual de consumo de combustible de las naves espaciales, con posibles errores como datos faltantes, valores negativos y fechas mal formateadas.

## Problemas Simulados en los Datos

Los datos han sido diseñados con algunos problemas típicos para simular un entorno legacy:
- **Valores negativos o cero**: Anomalías en los datos, como velocidades negativas o consumos de combustible no realistas, que requieren validación y manejo adecuado.
- **Formatos de fecha inconsistentes**: Algunas fechas están en un formato incorrecto (`yyyy/MM/dd` en lugar de `yyyy-MM-dd`), lo que podría causar problemas durante el procesamiento.
- **Campos faltantes o nulos**: Algunos registros tienen valores importantes, como coordenadas o distancias, vacíos.
- **Registros duplicados**: Múltiples filas con los mismos datos para simular inconsistencias comunes en sistemas antiguos.
- **Errores tipográficos y valores fuera de rango**: Por ejemplo, nombres de planetas mal escritos o distancias estelares que no son razonables.

Estos problemas deberán ser gestionados mediante políticas de reintento y omisión en Spring Batch para garantizar la integridad y calidad de los datos procesados.

**¡Buena suerte con el desafío!**
