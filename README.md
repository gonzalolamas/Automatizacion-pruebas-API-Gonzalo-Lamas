# Automatizacion-pruebas-API-Gonzalo-Lamas

Este proyecto contiene un conjunto de pruebas automatizadas para validar endpoints de una API REST (GET, POST y DELETE).  
Las pruebas están desarrolladas en **Python** utilizando **Pytest** y generan reportes HTML para facilitar el análisis de los resultados.

---

## 📌 Propósito del proyecto

El objetivo de este proyecto es:

- Validar el funcionamiento de endpoints REST mediante pruebas automatizadas.
- Verificar estructura, tipos de datos y códigos de respuesta.
- Practicar técnicas de automatización de pruebas API.
- Generar reportes claros y reutilizables para evaluar los resultados de las pruebas.

---

## ⚙️ Tecnologías utilizadas

- **Python**
- **Pytest**
- **Requests** (para realizar llamadas HTTP)
- **pytest-html** (para generar reportes en formato HTML)

---

## 📁 Estructura del proyecto

```
📦 mi-proyecto-api
├── tests/
│ ├── test_get_posts.py
│ ├── test_create_post.py
│ ├── test_delete_post.py
│ └── init.py
├── utils/
│ └── helpers.py # Funciones auxiliares (si aplica)
├── requirements.txt
└── README.md
```
---

## ▶️ ¿Cómo ejecutar las pruebas?

- Ejecutar todas las pruebas:

pytest -s


- Ejecutar un archivo específico:

pytest tests/test_get_posts.py -s


- Generar reporte HTML:

pytest --html=report.html --self-contained-html

## 📊 ¿Cómo interpretar los reportes generados?

- Se genera un archivo:

report.html

- Este reporte incluye:

✔️ Pruebas pasadas

❌ Pruebas fallidas

🔍 Detalle de errores

📌 Logs y prints (si los habilitaste con -s)

Solo debes abrir el archivo en tu navegador:

./report.html

🧪 Endpoints probados (ejemplos)
✔️ GET /posts

- Validación de código de estado 200

- Validación de estructura JSON

- Validación de tipos de datos

✔️ POST /posts

- Envío de payload válido

- Validación de código de estado 201

- Validación de respuesta y campos devueltos

✔️ DELETE /posts/{id}

- Eliminación de un recurso

- Validación de status code esperado (200 / 204)