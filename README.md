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
> **Nota de la Redactora:** Este documento fue creado por María como parte de su portafolio de Technical Writing, aplicando conceptos de comunicación clara sobre estructuras de datos reales.
