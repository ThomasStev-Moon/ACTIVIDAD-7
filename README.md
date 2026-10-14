# ACTIVIDAD 7 
# 🐍 Taller: Python, MySQL y Análisis de Datos - Actividad 

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
