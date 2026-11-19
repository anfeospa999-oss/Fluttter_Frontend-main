<div align="center">

# ✈️ Aviation Inventory (Flutter Multiplatform)
### **Sistema Multiplataforma para Gestión de Inventario Aeronáutico**

[![Demo en Producción](https://img.shields.io/badge/Demo_En_Línea-flutter.proyecto.lol-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.proyecto.lol)
[![Flutter](https://img.shields.io/badge/Flutter_Web-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev/)
[![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Nginx](https://img.shields.io/badge/Nginx-Reverse_Proxy-009639?style=for-the-badge&logo=nginx&logoColor=white)](https://nginx.org/)
[![Coolify](https://img.shields.io/badge/Coolify-Self--Hosted-6B46C1?style=for-the-badge&logo=serverfault&logoColor=white)](https://coolify.io/)

<p align="center">
  Aplicación desarrollada con Flutter y Dart para el control, catálogo y trazabilidad de piezas y componentes en el sector aeronáutico, con despliegue web contenerizado en Docker y Nginx.
</p>

</div>

---

## 📌 Descripción General

**Aviation Inventory** es una solución multiplataforma diseñada para optimizar el registro, búsqueda y categorización de repuestos y piezas aeronáuticas. Implementando la reactividad y versatilidad de **Flutter**, ofrece una interfaz consistente tanto en navegadores web como en plataformas móviles y de escritorio, garantizando un flujo ágil de control de inventario y consulta de componentes críticos.

---

## ✨ Características Principales

- 📦 **Control de Inventario de Aviación:** Registro detallado de piezas, números de parte (P/N), números de serie (S/N) y estados de inspección.
- 🔍 **Búsqueda y Filtros Rápidos:** Localización ágil de componentes por categorías de aeronaves y ubicación en almacén.
- 📱 **Multiplataforma Nativa:** Código base unificado listo para compilar en Web, Android, iOS, Windows, macOS y Linux.
- 🐳 **Despliegue Web Automatizado:** Proceso de compilación multi-etapa (*multi-stage Docker build*) que genera los activos web estáticos y los sirve con un servidor Nginx ultraligero y seguro.
- 🛠️ **CLI de Gestión Local:** Script de utilidad `run.py` para levantar, detener e inspeccionar el estado del entorno contenerizado en segundos.

---

## 🛠️ Stack Tecnológico

- **Framework:** Flutter (Web & Multiplatform).
- **Lenguaje:** Dart.
- **Servidor Web & Proxy:** Nginx Alpine.
- **Contenerización & Orquestación:** Docker, Docker Compose, Coolify.
- **Herramientas de Soporte:** Python 3 (CLI auxiliar `run.py`).

---

## 📁 Estructura del Proyecto

```text
Fluttter_Frontend-main/
├── lib/               # Código fuente de la app en Flutter (Widgets, Modelos, Vistas)
├── web/               # Plantilla y configuración para compilación web
├── android/           # Configuración nativa Android
├── ios/               # Configuración nativa iOS
├── linux/ & macos/    # Soporte para entornos de escritorio Unix
├── windows/           # Soporte nativo para Windows
├── Dockerfile         # Compilación multi-stage (Flutter SDK -> Nginx Web)
├── docker-compose.yml # Configuración de servicios y puertos
├── nginx.conf         # Configuración del servidor web Nginx
├── pubspec.yaml       # Gestión de dependencias y paquetes de Flutter
└── run.py             # Script de automatización para ejecución local
```

---

## 🚀 Despliegue y Ejecución

### Opción 1: Con Docker (Recomendada)
El proyecto incluye un script en Python para simplificar el flujo con Docker:

```bash
# Iniciar contenedor en segundo plano (puerto por defecto: 8044)
python run.py up

# Ver estado del servicio
python run.py status

# Ver logs en tiempo real
python run.py logs

# Detener contenedor
python run.py down
```
Luego abre tu navegador en `http://localhost:8044`.

> **Nota:** Puedes cambiar el puerto pasando la variable de entorno:  
> `APP_PORT=9000 python run.py up`

### Opción 2: Con Flutter SDK Local
```bash
# Obtener dependencias
flutter pub get

# Ejecutar en el navegador
flutter run -d chrome
```

---

## 👨‍💻 Autor

- **Andrés Felipe Ospina Pardo**
- GitHub: [@anfeospa999-oss](https://github.com/anfeospa999-oss)
- LinkedIn: [Andrés Ospina](https://www.linkedin.com/in/andres-ospina-5a382b413)

