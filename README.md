# Óptica Cul d'Ampolla  

## 📄 Descripción  
Este proyecto tiene como objetivo gestionar la información de gafas, proveedores, clientes y ventas en la óptica "Cul d'Ampolla" utilizando **MongoDB**. La base de datos ha sido diseñada con **documentos embebidos** para optimizar el acceso a la información y reducir la dependencia de referencias entre colecciones.  

---  

## 🗃️ Estructura de la Base de Datos  

### 📌 Colección: Gafas (Glasses)  
Almacena la información de las gafas disponibles en la óptica, incluyendo detalles de sus clientes, proveedor y venta.  

#### **Campos:**  
- `_id` (**ObjectId**) → Identificador único de las gafas.  
- `brand` (**string**) → Marca de las gafas.  
- `frame` (**objeto**) → Información sobre la montura.  
  - `type` (**string**) → Tipo de montura (*flotante, pasta o metálica*).  
  - `color` (**string**) → Color de la montura.  
- `price` (**double**) → Precio de las gafas.  
- `lenses` (**objeto**) → Información de los lentes.  
  - `right_eye` (**objeto**)  
    - `graduation` (**double**) → Graduación del ojo derecho.  
    - `color` (**string**) → Color del vidrio derecho.  
  - `left_eye` (**objeto**)  
    - `graduation` (**double**) → Graduación del ojo izquierdo.  
    - `color` (**string**) → Color del vidrio izquierdo.  
- `provider` (**objeto embebido**) → Datos del proveedor.  
  - `name` (**string**) → Nombre del proveedor.  
  - `address` (**objeto**) → Dirección completa.  
  - `phone` (**string**) → Teléfono del proveedor.  
  - `fax` (**string**) → Fax del proveedor.  
  - `nif` (**string**) → Número de identificación fiscal.  
- `clients` (**array de objetos embebidos**) → Lista de clientes que han comprado las gafas.  
  - `name` (**string**) → Nombre del cliente.  
  - `address` (**objeto**) → Dirección del cliente.  
  - `phone` (**string**) → Teléfono del cliente.  
  - `email` (**string**) → Correo electrónico del cliente.  
  - `register_date` (**date**) → Fecha de registro del cliente.  
  - `recommended_by` (**string | null**) → Cliente que recomendó (si aplica).  
- `sold_by` (**objeto embebido**) → Información sobre la venta.  
  - `employee` (**string**) → Nombre del empleado que realizó la venta.  
  - `sale_date` (**date**) → Fecha y hora de la venta.  

---  

## 💻 Tecnologías Utilizadas  
- **JSON** → Formato de intercambio de datos.  
- **MongoDB** → Base de datos NoSQL utilizada para almacenar la información.  
- **MongoDB Compass** → Herramienta gráfica para gestionar MongoDB.  
- **Moon Modeler** → Software para diseñar y documentar la estructura de la base de datos.  

---  

## 📊 Requisitos  
- **MongoDB** → Servidor de base de datos en ejecución.  
- **Java 11+ (opcional)** → Para ejecutar aplicaciones que interactúen con la base de datos.  

---  

## 🛠️ Instalación  
1. Clonar este repositorio:  
   ```bash
   git clone https://github.com/eze-ms/MongoDB_N1-E2

   ```
2. Configurar la conexión a MongoDB en la clase correspondiente.

---
© 2025. Proyecto desarrollado por Ezequiel Macchi Seoane

