# Óptica Cul d'Ampolla

## 📄 Descripción
Este proyecto tiene como objetivo gestionar la información de gafas, proveedores, clientes y ventas en la óptica "Cul d'Ampolla" utilizando una base de datos MongoDB. La estructura se basa en referencias para conectar las diferentes entidades, lo que permite una gestión eficiente y escalable de los datos.

---

## 🗃️ Estructura de la Base de Datos

### Colecciones Principales

#### 1. Gafas (Glasses)
**Descripción:** Almacena la información de las gafas disponibles en la óptica.

**Campos:**
- `_id`: Identificador único de las gafas (ObjectId).
- `brand`: Marca de las gafas (string).
- `frameType`: Tipo de montura (string).
- `price`: Precio de las gafas (double).
- `supplier_id`: Referencia al proveedor de las gafas (ObjectId).
- `client_id`: Referencia al cliente que compró las gafas (ObjectId).

---

#### 2. Ventas (Sales)
**Descripción:** Registra las ventas realizadas, conectando clientes, empleados y gafas.

**Campos:**
- `_id`: Identificador único de la venta (ObjectId).
- `client_id`: Referencia al cliente que realizó la compra (ObjectId).
- `employee_id`: Referencia al empleado que realizó la venta (ObjectId).
- `glasses_id`: Referencia a las gafas vendidas (ObjectId).
- `saleDate`: Fecha de la venta (date).
- `saleTime`: Hora de la venta (string).

---

#### 3. Clientes (Clients)
**Descripción:** Almacena la información de los clientes de la óptica.

**Campos:**
- `_id`: Identificador único del cliente (ObjectId).
- `name`: Nombre del cliente (string).
- `address`: Dirección del cliente (string).
- `phone`: Teléfono del cliente (string).
- `email`: Correo electrónico del cliente (string).
- `registerDate`:  Fecha de registro del cliente (date).
---

#### 4. Proveedores (Suppliers)
**Descripción:** Almacena la información de los proveedores de las gafas.

**Campos:**
- `_id`: Identificador único del proveedor (ObjectId).
- `name`: Nombre del proveedor (string).
- `address`: Dirección completa del proveedor (objeto embebido).
  - `street`: Calle (string).
  - `number`: Número (string).
  - `floor`: Piso (string).
  - `door`: Puerta (string).
  - `city`: Ciudad (string).
  - `postal code`: Código postal (string).
  - `number`: País (string).
- `phone`: Teléfono del proveedor (string).
- `fax`: Fax del proveedor (string).
- `NIF`: Número de identificación fiscal (string).

---

## 💻 Tecnologías Utilizadas
- **JSON:** Formato de intercambio de datos.
- **MongoDB:** Base de datos NoSQL para almacenar la información.
- **MongoDB Compass:** Herramienta gráfica para gestionar MongoDB.
- **Moon Modeler:** Herramienta para diseñar y documentar la estructura de la base de datos.

---

## 📊 Requisitos
- **Java 11+:** Para ejecutar aplicaciones que interactúen con la base de datos.
- **MongoDB:** Servidor de base de datos en ejecución.

---

## 🛠️ Instalación
1. Clonar este repositorio:
   ```bash
   git clone https://github.com/eze-ms/MongoDB_N1-E2
   ```
2. Configurar la conexión a MongoDB en la clase correspondiente.

---

## ✨ Características Adicionales
- Validación de datos en cada inserción y actualización.
- Estructura de base de datos diseñada con Moon Modeler.
- Cumple estrictamente con el enunciado proporcionado.

---

## 📢 Notas
- Asegúrate de tener MongoDB ejecutándose en `localhost:27017`.
- Si surge algún error, revisar la conexión a la base de datos y la existencia de los documentos.

---
© 2025. Proyecto desarrollado por Ezequiel Macchi Seoane

