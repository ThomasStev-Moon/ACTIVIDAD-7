# ACTIVIDAD 7
# 🐍 Taller: Python, MySQL y Análisis de Datos - Actividad 7

**Autor:** [Thomas Stev Arismendi](https://github.com/ThomasStev-Moon)

Proyecto desarrollado en **Python + Streamlit + MySQL** que recorre:

1. **🟩 Tipos de Datos y Excel** — Investigación sobre los tipos de datos en bases de datos, análisis del impacto de los sistemas informáticos y creación de tablas en Excel.
2. **🐍 Zen de Python + MySQL** — Filosofía del lenguaje, desarrollo en Colab y VS Code, análisis de librerías y una infografía.
3. **🗄️ Diseño de Base de Datos** — Propuesta completa con entidades, atributos, relaciones y análisis de requerimientos funcionales.

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![MySQL](https://img.shields.io/badge/MySQL-8.0-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-1.30%2B-red)
![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-purple)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📋 Tabla de contenido

- [🟩 Punto 1: Tipos de Datos, Excel y Sistemas](#-punto-1-tipos-de-datos-excel-y-sistemas)
- [🐍 Punto 2: Zen de Python y MySQL](#-punto-2-zen-de-python-y-mysql)
- [🗄️ Punto 3: Diseño de BD y Requerimientos](#️-punto-3-diseño-de-bd-y-requerimientos)
- [🛠️ Tecnologías usadas](#️-tecnologías-usadas)
- [📁 Estructura del repositorio](#-estructura-del-repositorio)
- [🚀 Instalación](#-instalación)
- [▶️ Uso](#️-uso)
- [📚 Aprendizajes](#-aprendizajes)
- [👨‍💻 Autor](#️-autor)

---

# 🟩 Punto 1: Tipos de Datos, Excel y Sistemas

## 1. Tipos de datos más comunes en bases de datos

Los tipos de datos le dicen al sistema qué clase de información puede guardar cada columna.

| Tipo | ¿Qué guarda? |
|------|--------------|
| **INT** | Números enteros (sin decimales) |
| **VARCHAR** | Texto de longitud variable |
| **DATE** | Fechas (año-mes-día) |
| **DECIMAL** | Números con decimales exactos |
| **CHAR** | Texto de longitud fija |
| **BOOLEAN** | Verdadero / Falso |
| **FLOAT** | Números con decimales aproximados |
| **TEXT** | Textos largos |

## 2. Ejemplos de cada tipo de dato

**🔹 INT (entero)**
1. **Edad** → 25
2. **Documento de identidad** → 1023456789
3. **Stock** → 150 unidades

**🔹 VARCHAR (texto variable)**
1. **Nombre** → "Ana Gómez"
2. **Correo** → "ana@gmail.com"
3. **Dirección** → "Calle 45 #12-30"

**🔹 DATE (fecha)**
1. **Fecha de nacimiento** → 2000-05-14
2. **Fecha de compra** → 2026-10-02
3. **Fecha de cita médica** → 2026-11-15

**🔹 DECIMAL (decimal exacto)**
1. **Precio** → 19.99
2. **Salario** → 2500.50
3. **Impuesto** → 0.19

**🔹 BOOLEAN**
1. **¿Está activo?** → true
2. **¿Pagó?** → false
3. **¿Es administrador?** → true

## 3. ¿Qué pienso cuando escucho "No hay sistema"?

Pienso en **caos, frustración y pérdida de tiempo**. Cuando no hay sistema informático:

- **No se pueden guardar datos** → información perdida.
- **Se hacen procesos manuales** → más lentos y con errores.
- **No hay control ni seguimiento** → no sabes qué pasó con un pedido, pago o paciente.
- **Se duplican o pierden registros** → inconsistencias.
- **Afecta a las personas** → filas largas, esperas, enojos, decisiones equivocadas.

**En resumen:** sin sistema, todo se vuelve más lento, inseguro y propenso a errores humanos.

## 4. Impacto en banca, salud y comercio

| Sector | Sin sistemas | Ejemplo histórico |
|--------|--------------|-------------------|
| 🏦 **Banca** | No hay registro confiable de saldos, transferencias ni historial | Años 70: los bancos usaban libros contables manuales; un error podía borrar cuentas completas |
| 🏥 **Salud** | Historias clínicas en papel, recetas perdidas, diagnósticos duplicados | Años 50: si se perdía una carpeta, el paciente debía repetir todos los exámenes |
| 🛒 **Comercio** | Inventarios desactualizados, ventas sin registro, pérdidas económicas | Años 60: Sears llevaba inventario en tarjetas perforadas; si fallaban, no sabían qué había en bodega |

## 5. Antes de las computadoras

**Banca antes:**
- Se iba a la sucursal.
- El cajero anotaba en un libro.
- Se sellaba y firmaba.
- Los saldos se actualizaban a mano.
- Transferencias tardaban días.

**Salud antes:**
- Se llenaba una ficha en papel.
- El médico anotaba en la historia clínica física.
- Los exámenes se archivaban en carpetas.
- Si se perdía, todo se repetía.

## 6. Cuadro comparativo: antes vs. ahora

| Proceso | Antes (sin tecnología) | Ahora (con sistemas) |
|---------|------------------------|----------------------|
| Transacción bancaria | Libro manual, sello, firma | App o cajero automático, inmediato |
| Historia clínica | Carpeta física | Base de datos digital |
| Inventario | Tarjetas o cuadernos | Sistema automatizado |
| Búsqueda de datos | Manual, lenta | Consulta instantánea |
| Errores | Frecuentes | Menos, con validaciones |
| Acceso remoto | Imposible | Desde cualquier lugar |

## 7-10. Tablas en Excel

**🚗 Automóvil (auto de tus sueños)**

| Modelo | Marca |
|--------|-------|
| Mustang GT | Ford |
| 911 Carrera | Porsche |
| Model S | Tesla |

**🧑‍⚕️ Paciente**

| Nombre | Edad |
|--------|------|
| Juan Pérez | 20 |
| María López | 22 |
| Carlos Ruiz | 21 |

**🎮 Producto**

| Nombre | Precio |
|--------|--------|
| PlayStation 5 | 499.99 |
| Laptop Gamer | 1200.00 |
| iPhone 16 | 999.99 |

**Cómo hacerlo en Excel:**
1. Abre Excel.
2. Escribe los encabezados en la fila 1.
3. Llena los datos debajo.
4. Selecciona todo y presiona **Ctrl + T** para convertir en tabla.

## 11. Filtrar, ordenar, modificar y eliminar

- **Filtrar y ordenar:** Selecciona la tabla → `Ctrl + T` → clic en la flecha del encabezado → ordenar A-Z o de menor a mayor.
- **Modificar:** clic en una celda y escribe el nuevo valor.
- **Eliminar:** clic derecho sobre la fila → **Eliminar**.

## 12. Excel vs. Base de datos real

| Excel | Base de datos |
|-------|----------------|
| Un archivo por persona | Centralizada y multiusuario |
| Fácil de usar | Requiere conocimientos |
| Se corrompe fácil | Muy segura |
| Sin validaciones fuertes | Reglas y restricciones |
| No maneja millones de filas | Millones de registros sin problema |
| Sin relaciones complejas | Relaciones entre tablas |

👉 **Diferencia clave:** Excel es una **hoja de cálculo**, una base de datos es un **sistema gestor** (MySQL, PostgreSQL, SQL Server).

---

# 🐍 Punto 2: Zen de Python y MySQL

## 2.1 Filosofía de Python

Python tiene un conjunto de **19 aforismos filosóficos** que guían el diseño del lenguaje, conocidos como el **Zen de Python**. Se leen ejecutando `import this` en consola.

| Frase original | En palabras simples |
|----------------|---------------------|
| Beautiful is better than ugly | Escribe código bonito, no desordenado |
| Explicit is better than implicit | Que se entienda qué hace, sin adivinar |
| Simple is better than complex | Lo simple gana |
| Readability counts | Otros (y tú en el futuro) deben entenderlo |
| Errors should never pass silently | No ignores los errores |
| Now is better than never | Mejor hazlo ya |

🌟 **El que más me gustó:** *"Simple is better than complex"* (Lo simple es mejor que lo complejo).

**¿Por qué?** Porque muchas veces uno quiere hacer las cosas rebuscadas, pero al final lo simple funciona mejor, se entiende más rápido y tiene menos errores. Aplica para programar y para la vida.

## 2.2 Desarrollo en Python + MySQL

### En Google Colab

Instalar MySQL, arrancarlo, crear la BD, tabla e insertar datos:

```python
!apt-get update -qq
!apt-get install mysql-server -y -qq
!service mysql start
!pip install mysql-connector-python -q

!mysql -u root -e "ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'colab_pass';"

import mysql.connector

cnx = mysql.connector.connect(
    host="127.0.0.1", user="root", password="colab_pass", charset="utf8mb4"
)
cursor = cnx.cursor(buffered=True)
cursor.execute("CREATE DATABASE IF NOT EXISTS taller_python")
cursor.execute("USE taller_python")
cursor.execute("""
    CREATE TABLE IF NOT EXISTS estudiantes (
        id INT AUTO_INCREMENT PRIMARY KEY,
        nombre VARCHAR(100) NOT NULL,
        edad INT,
        correo VARCHAR(100)
    )
""")

estudiantes = [
    ("Ana Gómez", 20, "ana@email.com"),
    ("Carlos Ruiz", 22, "carlos@email.com"),
    ("María López", 21, "maria@email.com")
]
cursor.executemany(
    "INSERT INTO estudiantes (nombre, edad, correo) VALUES (%s, %s, %s)",
    estudiantes
)
cnx.commit()

cursor.execute("SELECT id, nombre, edad, correo FROM estudiantes")
for fila in cursor:
    print(f"ID: {fila[0]} | Nombre: {fila[1]} | Edad: {fila[2]} | Correo: {fila[3]}")

cursor.close()
cnx.close()
```

**✅ Resultado esperado:**
```
ID: 1 | Nombre: Ana Gómez | Edad: 20 | Correo: ana@email.com
ID: 2 | Nombre: Carlos Ruiz | Edad: 22 | Correo: carlos@email.com
ID: 3 | Nombre: María López | Edad: 21 | Correo: maria@email.com
```

### En Visual Studio Code

MySQL ya está instalado en el PC. Solo se instala la librería:

```bash
pip install mysql-connector-python pandas
```

Y se conecta con `root` + contraseña local. Los datos **quedan guardados permanentemente**.

**Diferencias clave:**

| Aspecto | Colab | VS Code |
|---------|-------|---------|
| ¿Hay que instalar MySQL? | Sí, cada vez | Solo una vez |
| ¿Los datos se guardan? | ❌ Se borran al cerrar | ✅ Permanentes |
| ¿Sirve para producción? | No | Sí |
| ¿Ideal para? | Pruebas rápidas | Proyectos reales |

## 2.3 Librerías: pandas, polars, scipy

| Librería | ¿Qué hace? | ¿Cuándo usarla? |
|----------|-----------|-----------------|
| **pandas** | Maneja tablas (DataFrames), como Excel pero en código | Análisis de datos general |
| **polars** | Igual que pandas, pero **mucho más rápido** | Datos grandes (millones de filas) |
| **scipy** | Cálculos matemáticos y científicos avanzados | Estadística, optimización, física |

**Ejemplo con pandas:**

```python
import pandas as pd
df = pd.DataFrame({"nombre": ["Ana", "Luis"], "edad": [20, 22]})
print(df)
```

**Ejemplo con polars:**

```python
import polars as pl
df2 = pl.DataFrame({"nombre": ["Ana", "Luis"], "edad": [20, 22]})
print(df2)
```

**Ejemplo con scipy:**

```python
from scipy import stats
datos = [1, 2, 3, 4, 5]
print("Media:", stats.tmean(datos))
print("Desviación estándar:", stats.tstd(datos))
```

**Integración MySQL + pandas:**

```python
import pandas as pd
df = pd.read_sql("SELECT * FROM clientes", cnx)
print(df)
```

👉 `pd.read_sql()` combina SQL + pandas → traes los datos y los analizas en una sola línea.

## 2.4 Infografía

📌 **Título:** *"MySQL + Python: La Pareja Perfecta para los Datos"*

**Secciones:**
1. **¿Qué es MySQL?** — Base de datos relacional más usada del mundo.
2. **¿Qué es Python?** — Lenguaje fácil y poderoso.
3. **¿Cómo se conectan?** — `mysql-connector-python` + `pd.read_sql()`.
4. **Aplicaciones reales** — banca, salud, comercio, educación, logística.
5. **Ventajas** — automatización, análisis, reportes, IA.
6. **Alcance** — usado por el 70% de las empresas del mundo.

🖼️ *Ver archivo `punto4_infografia.png`*

---

# 🗄️ Punto 3: Diseño de BD y Requerimientos

## 3.1 Elementos necesarios para conformar una BD

| Elemento | ¿Qué es? | Ejemplo |
|----------|----------|---------|
| **Entidades** | Cosas del mundo real | Cliente, Producto |
| **Atributos** | Características | nombre, precio |
| **Registros** | Cada fila | "Ana / Bogotá" |
| **Columnas** | Cada campo | id, nombre |
| **Tipos de datos** | Qué se guarda | INT, VARCHAR |
| **PK** | Identificador único | id_cliente |
| **FK** | Conecta tablas | pedido → cliente_id |

## 3.2 Propuesta de estructura: Base de datos "tienda_db"

### 🔹 Tabla: clientes

| Columna | Tipo | Restricción |
|---------|------|-------------|
| id | INT | PK, AUTO_INCREMENT |
| nombre | VARCHAR(64) | NOT NULL |
| ciudad | VARCHAR(64) | — |
| correo | VARCHAR(100) | UNIQUE |
| telefono | VARCHAR(20) | — |
| fecha_registro | DATE | DEFAULT hoy |

### 🔹 Tabla: productos

| Columna | Tipo | Restricción |
|---------|------|-------------|
| id | INT | PK, AUTO_INCREMENT |
| nombre | VARCHAR(64) | NOT NULL |
| precio | DECIMAL(10,2) | NOT NULL |
| stock | INT | DEFAULT 0 |
| categoria | VARCHAR(50) | — |
| fecha_ingreso | DATE | — |

### 🔹 Tabla: pedidos

| Columna | Tipo | Restricción |
|---------|------|-------------|
| id | INT | PK, AUTO_INCREMENT |
| cliente_id | INT | FK → clientes(id) |
| producto_id | INT | FK → productos(id) |
| cantidad | INT | DEFAULT 1 |
| fecha | DATE | NOT NULL |
| total | DECIMAL(10,2) | — |
| estado | VARCHAR(20) | DEFAULT 'pendiente' |

### 🔗 Relaciones entre tablas

```
┌─────────────┐         ┌─────────────┐
│  CLIENTES   │         │  PRODUCTOS  │
│─────────────│         │─────────────│
│ id (PK)     │         │ id (PK)     │
│ nombre      │         │ nombre      │
│ ciudad      │         │ precio      │
│ correo      │         │ stock       │
└──────┬──────┘         └──────┬──────┘
       │                       │
       │   ┌──────────────┐    │
       └──▶│   PEDIDOS    │◀───┘
           │──────────────│
           │ id (PK)      │
           │ cliente_id(FK)│
           │ producto_id(FK)│
           │ cantidad     │
           │ fecha        │
           │ total        │
           └──────────────┘
```

## 3.3 Propuesta de desarrollo

1. **Análisis** — Identificar entidades, atributos y reglas de negocio.
2. **Diseño** — Modelo Entidad-Relación, tipos de datos, PKs y FKs.
3. **Implementación en MySQL** — Crear BD con `CREATE TABLE`.
4. **Conexión Python + Streamlit** — Formularios para insertar y consultar.
5. **Pruebas y despliegue** — Validar relaciones y subir a GitHub.

**Script SQL propuesto:**

```sql
CREATE DATABASE tienda_db;
USE tienda_db;

CREATE TABLE clientes (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nombre VARCHAR(64) NOT NULL,
    ciudad VARCHAR(64),
    correo VARCHAR(100) UNIQUE,
    telefono VARCHAR(20),
    fecha_registro DATE
);

CREATE TABLE productos (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nombre VARCHAR(64) NOT NULL,
    precio DECIMAL(10,2) NOT NULL,
    stock INT DEFAULT 0,
    categoria VARCHAR(50),
    fecha_ingreso DATE
);

CREATE TABLE pedidos (
    id INT PRIMARY KEY AUTO_INCREMENT,
    cliente_id INT,
    producto_id INT,
    cantidad INT DEFAULT 1,
    fecha DATE NOT NULL,
    total DECIMAL(10,2),
    estado VARCHAR(20) DEFAULT 'pendiente',
    FOREIGN KEY (cliente_id) REFERENCES clientes(id),
    FOREIGN KEY (producto_id) REFERENCES productos(id)
);
```

## 3.4 Requerimientos funcionales del aplicativo

| Código | Requerimiento | Descripción |
|--------|---------------|-------------|
| **RF01** | Registrar clientes | Crear clientes con nombre, ciudad, correo y teléfono. |
| **RF02** | Listar clientes | Ver todos los clientes en una tabla. |
| **RF03** | Editar clientes | Modificar datos de un cliente existente. |
| **RF04** | Eliminar clientes | Borrar clientes con confirmación. |
| **RF05** | Registrar productos | Agregar productos con nombre, precio, stock y categoría. |
| **RF06** | Listar productos | Ver el inventario completo. |
| **RF07** | Actualizar stock | Ajustar unidades cuando se vende o repone. |
| **RF08** | Registrar pedidos | Crear pedidos asociando un cliente y un producto. |
| **RF09** | Calcular total automático | Multiplicar cantidad × precio. |
| **RF10** | Cambiar estado del pedido | pendiente → enviado → entregado. |
| **RF11** | Consultar pedidos por cliente | Filtrar pedidos de un cliente específico. |
| **RF12** | Reporte de ventas totales | Sumar todo lo vendido por cliente o fecha. |
| **RF13** | Exportar a Excel/CSV | Descargar datos en formato de hoja de cálculo. |
| **RF14** | Buscar productos | Buscar por nombre o categoría. |
| **RF15** | Autenticación básica | Solo usuarios registrados pueden modificar datos. |

**Requerimientos NO funcionales:**

| Código | Requerimiento | Descripción |
|--------|---------------|-------------|
| **RNF01** | Rapidez | Las consultas deben responder en menos de 2 segundos. |
| **RNF02** | Usabilidad | La interfaz debe ser clara e intuitiva. |
| **RNF03** | Seguridad | Las contraseñas deben ir cifradas. |
| **RNF04** | Disponibilidad | Debe funcionar en cualquier navegador. |
| **RNF05** | Escalabilidad | Debe soportar miles de registros sin caerse. |

---

## 🛠️ Tecnologías usadas

- [Python 3.10+](https://www.python.org/)
- [MySQL 8.0](https://www.mysql.com/)
- [Streamlit](https://streamlit.io/)
- [Pandas](https://pandas.pydata.org/)
- [Polars](https://www.pola.rs/)
- [SciPy](https://scipy.org/)
- [Google Colab](https://colab.research.google.com/)
- [Visual Studio Code](https://code.visualstudio.com/)

---

## 📁 Estructura del repositorio

```
ACTIVIDAD-7/
├── README.md
├── requirements.txt
├── punto1_excel_tipos_datos.md
├── punto2_mysql_colab.ipynb
├── punto2_streamlit/
│   ├── app.py
│   ├── db.py
│   └── requirements.txt
├── punto3_diseno_bd.md
├── punto4_infografia.png
└── capturas/
    └── punto2_resultado.png
```

### `requirements.txt`

```txt
streamlit
mysql-connector-python
pandas
polars
scipy
```

---

## 🚀 Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/ThomasStev-Moon/ACTIVIDAD-7.git
cd ACTIVIDAD-7
```

### 2. Crear entorno virtual

**Windows:**

```bash
python -m venv .venv
.venv\Scripts\activate
```

**macOS / Linux:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Instalar dependencias

```bash
pip install -r requirements.txt
```

---

## ▶️ Uso

### 🐍 Notebook de Colab (Punto 2)

Abre `punto2_mysql_colab.ipynb` en Google Colab y ejecuta la celda completa.

### 🖥️ App Streamlit (Punto 2)

```bash
cd punto2_streamlit
python -m streamlit run app.py
```

Abre en `http://localhost:8501`.

### 📊 Script de Excel (Punto 1)

Abre `punto1_excel_tipos_datos.md` para ver el detalle.

---

## 🐛 Problemas conocidos

### `Access denied for user 'root'`

Verifica que la contraseña en `app.py` y `db.py` coincida con la de tu MySQL local.

### `Can't connect to MySQL server`

MySQL no está corriendo. Inícialo desde **Servicios de Windows** (`services.msc`) o con `net start MySQL80`.

### `streamlit: command not found`

Usa `python -m streamlit run app.py` en lugar de `streamlit run app.py`.

---

## 📚 Aprendizajes

- Comprensión de los **tipos de datos** en bases de datos (INT, VARCHAR, DATE, DECIMAL…).
- Análisis del **impacto de los sistemas informáticos** en banca, salud y comercio.
- Creación de **tablas en Excel** con filtros, ordenamiento y modificaciones.
- Comparación entre **Excel y bases de datos reales**.
- Filosofía del **Zen de Python** y su aplicación al escribir código limpio.
- Conexión de **Python con MySQL** tanto en **Google Colab** como en **Visual Studio Code**.
- Uso de **pandas, polars y scipy** para análisis de datos.
- **Diseño de bases de datos** con entidades, atributos, PKs y FKs.
- Análisis de **requerimientos funcionales y no funcionales** de un aplicativo.
- Creación de una **infografía** sobre MySQL + Python y sus aplicaciones.

---

## 👨‍💻 Autor

**Thomas Stev Arismendi**
🔗 [github.com/ThomasStev-Moon](https://github.com/ThomasStev-Moon)

Actividad 7 — Programación de Software SENA

📅 Octubre 2026
📍 Colombia

---

## 📄 Licencia

Este proyecto es de uso educativo. Puedes usarlo, modificarlo y compartirlo libremente.

---

## 🙏 Agradecimientos

- Al instructor por la guía del taller.
- A la comunidad de **Streamlit** por la documentación.
- A **MySQL** y **Python** por ser herramientas accesibles y poderosas.
- A mis compañeros por aportar ideas y datos de prueba.

---

> ⭐ Si te sirvió este proyecto, dale una estrella al repositorio. ¡Gracias!
