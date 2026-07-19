# 🏔️ Llanquihue Tour - Sistema de Gestión Turística

## Información del proyecto

**Proyecto:** Llanquihue Tour  
**Lenguaje:** Java  
**Tipo de aplicación:** Sistema modular orientado a objetos  
**Autor:** Vicente Estrada  
**Fecha:** 19/07/2026  

---

# 📌 Descripción del sistema

Llanquihue Tour es un prototipo de software desarrollado en Java para apoyar la gestión de una agencia turística ubicada en la Región de Los Lagos.

El sistema permite administrar clientes, servicios turísticos y órdenes de compra mediante una estructura modular basada en Programación Orientada a Objetos.

El proyecto representa una solución reutilizable y escalable para la digitalización de procesos turísticos, aplicando conceptos fundamentales de desarrollo como encapsulamiento, composición, herencia, polimorfismo, interfaces, colecciones y manejo de archivos.

---

# 🎯 Objetivo del proyecto

El objetivo principal es desarrollar un sistema modular que permita:

- Registrar clientes.
- Buscar clientes mediante RUT.
- Gestionar servicios turísticos.
- Crear órdenes de compra.
- Mantener historial de órdenes realizadas.
- Leer información desde archivos de texto.
- Aplicar principios de Programación Orientada a Objetos.
- Mantener una estructura organizada mediante paquetes.

---

# 📂 Estructura del proyecto

```
LlanquihueTour
│
├── src
│
├── app
│   └── Main.java
│
├── model
│   ├── Persona.java
│   ├── Cliente.java
│   ├── Empleado.java
│   ├── Proveedor.java
│   ├── Rut.java
│   ├── Direccion.java
│   ├── Tarjeta.java
│   ├── ServicioTuristico.java
│   ├── RutaGastronomica.java
│   ├── PaseoLacustre.java
│   ├── ExcursionCultural.java
│   └── OrdenDeCompra.java
│
├── data
│   ├── GestorDatos.java
│   └── clientes.txt
│
├── utils
│   ├── LectorArchivo.java
│   └── ValidadorRut.java
│
├── interfaces
│   └── Registrable.java
│
└── exceptions
    └── RutInvalidoException.java
```

---

# 📦 Paquetes utilizados

## 📁 model

Contiene las clases principales del dominio del sistema.

### Persona

Clase base que almacena información común:

- Nombre.
- Apellido.
- RUT.
- Dirección.
- Tarjeta.
- Teléfono.
- Correo.

### Cliente

Representa a los clientes de Llanquihue Tour.

Características:

- Hereda de Persona.
- Implementa la interfaz Registrable.
- Administra puntos acumulados.

### Empleado

Representa trabajadores de la agencia.

Características:

- Hereda de Persona.
- Implementa Registrable.
- Maneja información del cargo.

### Proveedor

Representa empresas asociadas.

Características:

- Hereda de Persona.
- Implementa Registrable.
- Maneja información de empresa.

### ServicioTuristico

Clase abstracta que representa los servicios ofrecidos.

Clases derivadas:

- RutaGastronomica.
- PaseoLacustre.
- ExcursionCultural.

### OrdenDeCompra

Representa una compra realizada por un cliente y almacena los servicios contratados.

---

# 📁 data

Contiene las clases encargadas de administrar información.

## GestorDatos

Administra las colecciones principales del sistema:

- `ArrayList` para clientes.
- `ArrayList` para servicios turísticos.
- `HashMap` para búsqueda rápida por RUT.
- `Stack` para historial de órdenes.

---

# 📁 utils

Contiene clases auxiliares.

## LectorArchivo

Permite cargar clientes desde un archivo `.txt` y convertir la información en objetos Java.

## ValidadorRut

Realiza validaciones del formato del RUT mediante excepciones personalizadas.

---

# 📁 interfaces

Contiene interfaces reutilizables.

## Registrable

Define métodos comunes para entidades registrables:

```java
void registrar();

void mostrarDatos();
```

Implementada por:

- Cliente.
- Empleado.
- Proveedor.

---

# 📁 exceptions

Contiene excepciones personalizadas del sistema.

## RutInvalidoException

Controla errores relacionados con el ingreso de RUT inválidos.

---

# 🧩 Principios de Programación Orientada a Objetos aplicados

## Encapsulamiento

Los atributos de las clases son privados:

```java
private String nombre;
```

y se gestionan mediante métodos getters y setters.

---

## Herencia

Se implementó la siguiente jerarquía:

```
Persona
│
├── Cliente
├── Empleado
└── Proveedor
```

Esto permite reutilizar atributos y comportamientos.

---

## Composición

Se utilizaron objetos dentro de otras clases.

Ejemplo:

```
Persona
│
├── Rut
├── Direccion
└── Tarjeta
```

---

## Polimorfismo

Los servicios turísticos utilizan una referencia común:

```
ServicioTuristico
│
├── RutaGastronomica
├── PaseoLacustre
└── ExcursionCultural
```

Esto permite manejar distintos tipos de servicios mediante una misma estructura.

---

## Interfaces

La interfaz `Registrable` permite definir comportamientos comunes entre diferentes clases.

---

# 📄 Archivo de datos

El sistema utiliza un archivo:

```
clientes.txt
```

Ubicación:

```
src/data/clientes.txt
```

Formato utilizado:

```
rut;nombre;apellido;telefono;correo
```

Ejemplo:

```
12345678-9;Vicente;Estrada;987654321;vicente@email.com
```

---

# ▶️ Instrucciones para ejecutar el programa

1. Abrir el proyecto en IntelliJ IDEA o NetBeans.

2. Verificar que los paquetes estén correctamente ubicados.

3. Ejecutar la clase principal:

```
app.Main
```

4. Utilizar el menú del sistema:

```
======================================
        SISTEMA LLANQUIHUE TOUR
======================================

1. Registrar cliente
2. Buscar cliente por RUT
3. Mostrar clientes
4. Cargar clientes desde TXT
5. Mostrar servicios turísticos
6. Registrar orden de compra
7. Mostrar historial de órdenes
0. Salir
```

---

# 🛠️ Tecnologías utilizadas

- Java JDK 17 o superior.
- Programación Orientada a Objetos.
- Colecciones Java:
  - ArrayList.
  - HashMap.
  - Stack.
- Manejo de archivos TXT.
- Excepciones personalizadas.

---

# ✅ Estado del proyecto

Proyecto funcional desarrollado como prototipo académico para la gestión de una agencia turística.

El sistema implementa una arquitectura modular, reutilizable y extensible aplicando buenas prácticas de Programación Orientada a Objetos.

---

# 👤 Autor

**Vicente Estrada**

Evaluación Final Transversal (EFT)  
Proyecto: Llanquihue Tour
