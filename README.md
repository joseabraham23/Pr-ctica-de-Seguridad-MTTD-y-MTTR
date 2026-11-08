# Laboratorio: Código Seguro y Modelo OWASP

## 1. Datos generales

- **Nombre completo:** José Abraham Peñate Martínez
- **Correo institucional:** joseabraham2307@gmail.com
- **Asignatura:** Seguridad en Aplicaciones / Ciberseguridad
- **Fecha:** 2026-11-07

## 2. Descripción

Este laboratorio consiste en desarrollar una aplicación web segura utilizando Python y Flask, implementando controles básicos de seguridad basados en buenas prácticas y principios del modelo OWASP. Se aplicaron mecanismos de validación de entradas mediante expresiones regulares, protección de credenciales con hashing (Werkzeug), consultas parametrizadas para prevenir inyección SQL, registro automatizado de eventos de autenticación (`eventos.log`) y un sistema de detección y respuesta a incidentes con el cálculo de las métricas de seguridad **MTTD** (Mean Time to Detect) y **MTTR** (Mean Time to Repair).

## 3. Estructura del proyecto

```text
laboratorio-las/
├── templates/
│   ├── login.html
│   └── registro.html
├── venv/
├── app.py
├── crearDB.py
├── detector.py
├── usuarios.db
├── eventos.log
├── respuesta.log
└── README.md

4. Requisitos y Dependencias
Python 3.x

Flask

Werkzeug (seguridad y hashing)

SQLite3

5. Ejecución del proyecto
Paso 1. Clonar o ubicarse en la carpeta del repositorio/proyecto.
cd laboratorio-las

Paso 2. Activar el entorno virtual de Python.

En Windows:

Bash
venv\Scripts\activate

Paso 3. Instalar las dependencias (si aplica).

Bash
pip install flask

Paso 4. Inicializar la base de datos.

Bash
python crearDB.py

Paso 5. Ejecutar la aplicación web Flask.

Bash
python app.py

Paso 6. Ejecutar el detector de incidentes y cálculo de métricas.

En una terminal independiente (con el entorno virtual activo):

Bash
python detector.py

6. Resultados y Métricas de Seguridad (MTTD y MTTR)
A continuación se registran los resultados obtenidos tras simular escenarios de intentos fallidos de autenticación y su respectiva respuesta de bloqueo:

Prueba MTTD (segundos)	MTTR (segundos)
1	        12.0	          5.2
2	        14.5	          6.1
3	        11.0	          4.8

MTTD promedio: 12.5 segundos

MTTR promedio: 5.37 segundos