# Prueba-Virtualiacion-y-Mysql
Voy hacer una prueba en la cual voy a probar una virtualizacion y como ejecutar programas dentro de la virtualizacion hecha.
# — Virtualización con Ubuntu y MySQL
### Materia: Arquitectura y Sistemas Operativos

---

## Descripción

En este trabajo práctico instalé y configuré una máquina virtual con Ubuntu utilizando Oracle VirtualBox. Dentro del entorno virtualizado, instalé MySQL como herramienta de prueba para demostrar el correcto funcionamiento del sistema.

---

## Requisitos

- Oracle VirtualBox instalado en el sistema anfitrión
- ISO de Ubuntu 26.04
- 2 GB de RAM asignados a la VM
- 20 GB de disco virtual

---

## Comandos Utilizados

### 1. Actualizar el sistema
```bash
sudo apt update
```
Actualiza la lista de paquetes disponibles en Ubuntu.

---

### 2. Instalar MySQL
```bash
sudo apt install mysql-server
```
Instala el servidor de base de datos MySQL en la máquina virtual.

---

### 3. Acceder a MySQL
```bash
sudo mysql
```
Abre la consola de MySQL como administrador.

---

### 4. Crear la base de datos
```sql
CREATE DATABASE analisis_datos;
```
Crea una base de datos llamada `analisis_datos`.

---

### 5. Seleccionar la base de datos
```sql
USE analisis_datos;
```
Indica a MySQL que vamos a trabajar dentro de `analisis_datos`.

---

### 6. Crear la tabla ventas
```sql
CREATE TABLE ventas (
  id INT AUTO_INCREMENT PRIMARY KEY,
  producto VARCHAR(50),
  cantidad INT,
  precio DECIMAL(10,2),
  fecha DATE
);
```
Crea una tabla llamada `ventas` con 5 columnas: id, producto, cantidad, precio y fecha.

---

### 7. Insertar un registro
```sql
INSERT INTO ventas (producto, cantidad, precio, fecha) VALUES ('Laptop', 5, 999.99, '2024-01-15');
```
Inserta un producto de prueba en la tabla.

---

### 8. Consultar los datos
```sql
SELECT * FROM ventas;
```
Muestra todos los registros cargados en la tabla.

---

## Resultado

Se logró instalar y ejecutar exitosamente Ubuntu dentro de VirtualBox, instalar MySQL y crear una base de datos funcional, todo dentro de un entorno virtualizado y sin afectar el sistema operativo principal.

---

*TP realizado por: Maximiliano Alvarez*
