# ACTIVIDAD 7 

> **"Sin importar qué carrera o especialidad estudies, terminarás enviando correos electrónicos y usando Excel."**

Repositorio con el desarrollo completo del taller: tipos de datos, Excel, Zen de Python, MySQL, análisis de datos y diseño de bases de datos.

---

## 📚 Tabla de contenidos

- [PUNTO 1: Tipos de Datos, Excel y Sistemas](#-punto-1-tipos-de-datos-excel-y-sistemas)
- [PUNTO 2: El Zen de Python y MySQL](#-punto-2-el-zen-de-python-y-mysql)
- [PUNTO 3: Diseño de BD y Requerimientos](#️-punto-3-diseño-de-bd-y-requerimientos)
- [Tecnologías usadas](#️-tecnologías-usadas)
- [Estructura del repositorio](#-estructura-del-repositorio)
- [Cómo ejecutar](#-cómo-ejecutar)

---

## 🟩 PUNTO 1: Tipos de Datos, Excel y Sistemas

### 1. Tipos de datos más comunes

| Tipo | ¿Qué guarda? |
|------|--------------|
| **INT** | Números enteros |
| **VARCHAR** | Texto variable |
| **DATE** | Fechas |
| **DECIMAL** | Decimales exactos |
| **BOOLEAN** | True / False |
| **FLOAT** | Decimales aproximados |
| **TEXT** | Textos largos |

### 2. Ejemplos de cada tipo

- **INT:** edad (25), documento (1023456789), stock (150)
- **VARCHAR:** nombre ("Ana Gómez"), correo ("ana@x.com"), dirección ("Calle 45")
- **DATE:** nacimiento (2000-05-14), compra (2026-10-02), cita (2026-11-15)
- **DECIMAL:** precio (19.99), salario (2500.50), impuesto (0.19)
- **BOOLEAN:** activo (true), pagó (false), admin (true)

### 3. ¿Qué pienso de "No hay sistema"?

Caos, frustración y pérdida de tiempo: datos perdidos, procesos lentos, errores, filas largas, decisiones equivocadas.

### 4. Impacto en banca, salud y comercio

| Sector | Ejemplo histórico |
|--------|-------------------|
| 🏦 Banca | Años 70: libros contables manuales |
| 🏥 Salud | Años 50: carpetas que se perdían |
| 🛒 Comercio | Años 60: Sears con tarjetas perforadas |

### 5. Antes de las computadoras

- **Banca:** libro manual, sello, firma, días de espera.
- **Salud:** ficha en papel, historia clínica física.

### 6. Cuadro comparativo

| Proceso | Antes | Ahora |
|---------|-------|-------|
| Transacción bancaria | Libro manual | App, inmediato |
| Historia clínica | Carpeta física | BD digital |
| Inventario | Cuadernos | Sistema automatizado |
| Errores | Frecuentes | Menos, con validaciones |

### 7-10. Tablas en Excel

**🚗 Automóvil:** Mustang GT (Ford), 911 Carrera (Porsche), Model S (Tesla)

**🧑‍⚕️ Paciente:** Juan Pérez (20), María López (22), Carlos Ruiz (21)

**🎮 Producto:** PlayStation 5 (499.99), Laptop Gamer (1200), iPhone 16 (999.99)

### 11. Filtros y modificaciones

- **Filtrar:** `Ctrl + T` → flecha del encabezado → ordenar A-Z.
- **Modificar:** clic en la celda.
- **Eliminar:** clic derecho en la fila → Eliminar.

### 12. Excel vs. Base de datos

| Excel | BD real |
|-------|---------|
| Un archivo por persona | Multiusuario |
| Se corrompe fácil | Muy segura |
| Sin validaciones | Reglas y restricciones |
| Sin relaciones | Relaciones entre tablas |

---

## 🐍 PUNTO 2: El Zen de Python y MySQL

### 2.1 Filosofía de Python

19 aforismos que guían el diseño del lenguaje. Los más importantes:

- **Beautiful is better than ugly** → código bonito
- **Explicit is better than implicit** → sin adivinar
- **Simple is better than complex** → lo simple gana
- **Readability counts** → que se entienda

🌟 **El que más me gustó:** *"Simple is better than complex"* — porque lo simple funciona mejor, se entiende rápido y tiene menos errores.

### 2.2 Desarrollo en Python + MySQL

**En Google Colab:**

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
