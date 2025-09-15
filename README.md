# YaguáSmash – Sistema gestión integral de pádel

**Ámbito:** Ciudad de Formosa  
**Prototipo operacional:** Java + MySQL  
**Metodología:** Proceso Unificado de Desarrollo (PUD)

## 📌 Descripción
YaguáSmash integra **reservas**, **abonos**, **POS/stock** (productos deportivos, bebidas y comidas) y una red ligera de **“me falta uno”** para clubes de pádel. Este repositorio contiene el **prototipo en Java** con **persistencia MySQL**.

## ✨ Funcionalidades (MVP)
- Reservas con disponibilidad en tiempo real (sin solapamientos).
- Abonos (mensuales / por créditos) con consumo automático.
- POS y stock de productos (deportivos, bebidas y comidas).
- Comunidad “me falta uno” (publicar/unirse a partidos).
- Notificaciones básicas.
- Reportes de ocupación, ventas y uso de abonos.
- Roles: administrador, empleado, jugador.

## 🧩 Arquitectura
- **Java (MVC)**  
  - `domain/` POJOs (Usuario, Sede, Cancha, Reserva, Abono, Producto, Venta, etc.)
  - `repository/` (JDBC/JPA) acceso a datos MySQL
  - `service/` reglas de negocio (reservas, abonos, stock, comunidad)
  - `web/` controladores REST
- **MySQL** con integridad referencial y transacciones.

## 🛠 Requisitos
- **JDK 17** (o compatible)
- **MySQL 8.x**
- **Maven** o **Gradle**
- IDE a elección (IntelliJ/Eclipse/NetBeans)

## ⚙️ Configuración
1. Crear base de datos:
   ```sql
   CREATE DATABASE yaguasmash CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
