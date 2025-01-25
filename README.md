<<<<<<< HEAD
# Optical Management System

## 📄 Description
This project manages the process of optical product sales using a MongoDB database. It performs CRUD (Create, Read, Update, Delete) operations for clients, glasses, sales, employees, and suppliers, facilitating the management and traceability of optical sales and customer relationships.

### Features
1. **Database Connection:**
    - MongoDB is used to manage collections related to glasses, clients, suppliers, employees, and sales.
2. **Data Model:**
    - **Client:** Contains basic client information (name, address, email, phone, etc.).
    - **Glasses:** Represents optical products with details such as brand, lens power, frame type, frame color, price, and supplier reference.
    - **Supplier:** Contains details about the suppliers providing the glasses.
    - **Sales:** Captures the details of sales transactions involving clients, glasses, and employees.
    - **Employee:** Information about the employees handling sales operations.
3. **Queries:**
    - Queries to retrieve clients, glasses, sales, suppliers, and employees.
    - Complex queries such as listing all clients associated with specific glasses or showing a supplier for a specific product.

4. **Relationships:**
    - **Client and Glasses:** Multiple clients can be associated with the same glasses.
    - **Glasses and Supplier:** Each glasses entry references a supplier.
    - **Sales:** A sale involves a client, glasses, and an employee.

---

## 🔧 Running the Project
1. Ensure the MongoDB server is running and accessible.
2. Run the `Main.java` file to insert initial data and test CRUD operations for clients, glasses, suppliers, employees, and sales.
3. Verify the collections and documents are created correctly and that queries return the expected results.

---

## 📈 Architecture
### Repository
- The repository handles direct CRUD operations on the MongoDB database.
- Methods such as `insertClient`, `insertGlasses`, `insertSupplier`, and `insertSales` handle insertions, updates, and queries.

### Services
- **Each service handles a specific domain:**
    - `GlassesService`: Manages glasses-related operations, including supplier associations and client interactions.
    - `ClientService`: Handles client registration and data updates.
    - `SalesService`: Manages sales records and listing operations.
    - `SupplierService`: Manages supplier-related operations and data consistency.
    - `EmployeeService`: Manages employee data and relationships with sales.

**The service layer delegates database operations to the repository for better separation of concerns.**

---

## ✨ Additional Features
The system is designed to be scalable, supporting:
- Expansion to include more product types.
- Advanced reporting for sales and inventory management.

---

## 📊 Project Structure
### Models
1. **Client:** Represents a client with fields like `name`, `address`, `email`, `phone`, and `registerDate`.
2. **Glasses:** Represents glasses with fields like `brand`, `frameType`, `price`, and `supplierId`.
3. **Supplier:** Represents a supplier with `name`, `address`, `phone`, `fax`, and `NIF`.
4. **Sales:** Represents a sales record, associating `clientId`, `glassesId`, `employeeId`, and `saleDate`.
5. **Employee:** Represents an employee with fields like `name`, `lastName`, and `phone`.

### Repositories
- **DatabaseRepository:**
    - Manages CRUD operations for all entities (`client`, `glasses`, `supplier`, `sales`, and `employee`).

### Services
- **GlassesService:** Manages operations related to glasses, including supplier and client interactions.
- **ClientService:** Manages client-related operations.
- **SalesService:** Manages sales records and data validation.
- **SupplierService:** Manages supplier details and validation.
- **EmployeeService:** Manages employee data.

---

## 📌 Conclusion
This project offers a well-structured and efficient system for managing optical sales using MongoDB. It ensures data integrity, proper relationship management, and scalability for future enhancements.

---

## 💻 Technologies Used
- **Java**
- **MongoDB**
- **MongoDB Java Driver**

---

## 📊 Requirements
- **MongoDB Server:** Ensure MongoDB is installed and running.
- **Java:** Java Development Kit (JDK) 17+.

---

## 🛠️ Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/eze-ms/MongoDB_N1-E2
   ```
2. Ensure MongoDB is running locally.
3. Run the `Main.java` file to test the basic operations.

---

© 2025. Developed by Ezequiel Macchi Seoane. 
=======
# Óptica Cul d'Ampolla

## 📄 Descripción
Este proyecto implementa una base de datos para la gestión integral de una óptica. Permite administrar información de clientes, empleados, proveedores, gafas y ventas, con el objetivo de optimizar los procesos internos y proporcionar un acceso eficiente a los datos.

### Características
1. **Gestión de Clientes:**
   - Almacena información del cliente: nombre, dirección (documento embebido), teléfono, email, fecha de registro y cliente recomendador `recommendedBy`.
   - Cada cliente tiene un array de ventas embebidas `sales`, que incluyen detalles de las gafas vendidas, el empleado responsable y la fecha de la venta.

2. **Gestión de Empleados:**
   - Almacena información del empleado: nombre y apellido.
   - Cada empleado tiene un array de ventas embebidas `sales`, que incluyen detalles del cliente y las gafas vendidas.

3. **Gestión de Proveedores:**
   - Almacena información del proveedor: nombre, dirección (documento embebido), teléfono, fax y NIF.
   - Cada proveedor tiene un array de gafas embebidas `glasses`, que incluye detalles técnicos de las gafas, como marca, graduación, tipo y color de la montura, y precio.

4. **Gestión de Gafas:**
   - Las gafas no son una colección independiente, sino que están embebidas en las ventas y los proveedores.
   - Cada gafa almacena datos como marca, graduación de lentes, tipo y color de la montura, y precio.

5. **Gestión de Ventas:**
   - Las ventas están embebidas tanto en clientes como en empleados.
   - Incluyen detalles del cliente, las gafas vendidas, el proveedor de las gafas y el empleado que realizó la venta.
  

---

## 💻 Tecnologías Utilizadas
- **Java**
- **MongoDB**
- **JSON**

---

## 📊 Requisitos
- Tener instalado **Java 11+**
- Servidor **MongoDB** en ejecución.

---

## 🛠️ Instalación
1. Clonar este repositorio:
   ```bash
   git clone https://github.com/eze-ms/MongoDB_N1-E1
   ```
2. Cargar los datos iniciales en MongoDB:
   - Usa el comando mongoimport para importar el archivo JSON:

---

## ✨ Características Adicionales
- La base de datos utiliza documentos embebidos para simplificar el acceso a información relacionada.
- Estructura optimizada: La estructura está diseñada para consultas rápidas y minimización de referencias externas (ObjectId).
- Estructura de base de datos diseñada con Moon Modeler.

---

## 📢 Notas
- Asegúrate de tener MongoDB ejecutándose en `localhost:27017`.
- Si surge algún error, revisar la conexión a la base de datos y la existencia de los documentos.

---
© 2025. Proyecto desarrollado por Ezequiel Macchi Seoane
>>>>>>> a73e6284382fe5b46052e697714e6d604f8699be

