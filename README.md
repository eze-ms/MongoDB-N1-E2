# Óptica Cul d'Ampolla

## 📄 Descripción
Este proyecto gestiona la base de datos de una óptica, permitiendo administrar clientes, gafas, proveedores, empleados y ventas de forma eficiente con **Java** y **MongoDB**.

### Características
1. **Gestión de Proveedores:**
   - Almacena información del proveedor: nombre, dirección, teléfono, fax y NIF.
   - Identifica el proveedor de cada gafa con `supplierId`.

2. **Gestión de Gafas:**
   - Guarda marca, graduación de lentes, tipo y color de montura, color de lentes y precio.
   - Relaciona cada gafa con un proveedor a través de `supplierId`.

3. **Gestión de Clientes:**
   - Registra nombre, dirección, teléfono, email, fecha de registro y cliente recomendador (`recommendedBy`).

4. **Gestión de Empleados:**
   - Almacena el nombre y apellido del empleado.
   - Identifica quién realizó cada venta a través del campo `soldBy` en la colección `sales`.

5. **Gestión de Ventas:**
   - Asocia cada venta con un cliente y una gafa a través de `clientId` y `glassesId`.
   - Registra quién realizó la venta (`soldBy`) referenciado al empleado.
   - Guarda la fecha de la venta con `saleDate`.

---

## 💻 Tecnologías Utilizadas
- **Java**
- **MongoDB**

---

## 📊 Requisitos
- Tener instalado **Java 11+**
- Servidor **MongoDB** en ejecución.

---

## 🛠️ Instalación
1. Clonar este repositorio:
   ```bash
   git clone https://github.com/eze-ms/MongoDB_N1-E1.git
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

