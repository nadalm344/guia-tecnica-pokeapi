# guia-tecnica-pokeapi
Ejercicio de documentación técnica: Auditoría de seguridad y usabilidad para integración de APIs
# 📕 Guía de Referencia: API de Pokémon (PokeAPI)

## 📋 Introducción
Esta guía explica cómo interpretar los datos técnicos que devuelve la **PokeAPI** (JavaScript Object Notation), una de las fuentes de datos más utilizadas para aprender a conectar aplicaciones. 

Como redactora técnica, mi objetivo en este documento es traducir el formato **JSON** a una explicación funcional para el equipo de desarrollo y producto.

---

## 🔍 Ejemplo de Consulta (Endpoint)
Para obtener los datos de un Pokémon, la dirección que se utiliza es:
`https://pokeapi.co/api/v2/pokemon/pikachu`

---

## 📊 Interpretación de los Datos (JSON a lenguaje claro)

Cuando realizamos la consulta anterior, la API nos devuelve un bloque de datos. A continuación, se explican los campos más importantes para el negocio:

| Campo Técnico | Tipo de dato | Descripción para el Usuario | Ejemplo |
| :--- | :--- | :--- | :--- |
| `name` | Texto | El nombre oficial del Pokémon en la base de datos. | `"pikachu"` |
| `base_experience` | Número | Puntos de experiencia que otorga al ser derrotado. Útil para balancear niveles de juego. | `112` |
| `height` | Número | La altura del Pokémon expresada en decímetros. | `4` (equivale a 0.4m) |
| `abilities` | Lista (Array) | Conjunto de habilidades especiales que el personaje puede usar en combate. | `static`, `lightning-rod` |

---

## 🛠️ Cómo leer un error común
Si el usuario busca un Pokémon que no existe (ejemplo: `pikachu-azul`), la API devolverá un **Error 404 (Not Found)**.

* **Significado:** El servidor funciona bien, pero el recurso solicitado no está en nuestra base de datos.
* **Acción sugerida:** Verificar que el nombre esté escrito en minúsculas y sin espacios.
---
# Auditoría de Documentación y Usabilidad de API 🚀

Este proyecto presenta una auditoría técnica realizada a una guía de integración, aplicando principios de **Comunicación para el Desarrollo** y visión estratégica de **Negocios**.

## 📑 Hallazgos Críticos Identificados

### 1. Vulnerabilidad de Seguridad (Password en URL)
- **Error:** La guía sugería enviar la contraseña directamente en los parámetros de la URL.
- **Riesgo:** Las URLs quedan almacenadas en el historial del navegador y registros del servidor, exponiendo credenciales.
- **Solución:** Implementar el envío de credenciales a través del encabezado de autorización (Authorization Header) o en el cuerpo de una petición POST.

### 2. Ambigüedad en Lógica Financiera (Manejo de Decimales)
- **Error:** Confusión en la instrucción para el campo de moneda/monto.
- **Riesgo:** Si el sistema espera centavos (integers) y el usuario envía decimales, se producen errores de cobro o pérdidas económicas.
- **Solución:** Clarificar que los montos deben enviarse en la unidad mínima de la moneda (ej. centavos) y proporcionar ejemplos claros (e.g., $10.00 = 1000).

### 3. Cumplimiento Legal y Económico (Compliance)
- **Error:** Referencia a políticas económicas genéricas o de otros países.
- **Riesgo:** Incumplimiento de regulaciones locales (como normativas bancarias o de protección de datos).
- **Solución:** Ajustar la documentación para reflejar los marcos legales vigentes del territorio de operación, asegurando la transparencia para el cliente final.

---
**Auditoría realizada por:** [María Nadal]  
*Technical Writer con enfoque en Negocios y Comunicación Estratégica.*

---
> **Nota de la Redactora:** Este documento fue creado por María como parte de su portafolio de Technical Writing, aplicando conceptos de comunicación clara sobre estructuras de datos reales.
