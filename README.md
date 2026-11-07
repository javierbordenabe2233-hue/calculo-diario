# Cálculo diario · Paso San Sebastián

App web para completar la **Planilla de cálculos de entrada y salida** a partir de fotos de las pantallas del S.I.Ca.M. (Administración de tránsitos).

## Uso
1. **Fotos**: subí las capturas de Compañías y Vehículos (Entrada y Salida) y de caminantes. La app las lee y completa los datos.
2. **Carga de datos**: revisá y corregí. TRIP por micro = 2 por defecto, editable.
   - *Números para Gendarmería*: vehículos y pasajeros.
   - *Para planilla diaria*: ingresos/egresos.
3. **Lista estadística**: copiá la columna de 29 filas y pegala en el Excel.
4. **Ajustes**: tasas editables ($1.000 camión chileno, $6.000 micro chileno) y clave de API de Anthropic para leer fotos.

Todo es un solo archivo (`index.html`), sin servidor. Los datos y la clave quedan sólo en el navegador.

## Reglas de cálculo
- Pasajeros = total de personas − tripulantes
- Tripulantes = personas en camiones + TRIP de los micros
- Pasajeros micros = suma PAX − suma TRIP
