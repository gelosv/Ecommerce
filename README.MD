# ECOMMERCE usando microservicios

## Introducción

E-commerce desarrollado utilizando la arquitectura de microservicios, conformado por varios microservicios que se comunican entre sí a través de un sistema de mensajería (NATS)

## Microservicios principales

### Auth

  Microservicio que maneja la autenticación y autorización de los usuarios.

### Products

  Microservicio que gestiona los productos, sus categorías e inventario.

### Payments

  Microservicio que gestiona las transacciones de pago, a través de Stripe como pasarela de pago.

### Orders

  Microservicio que gestiona las órdenes de compra, incluyendo la creación e historial de las órdenes por usuario o periodo.

> Estos microservicios pueden ser accedidos a través de una API RESTful (API GATEWAY).

## Características

- Desarrollado utilizando NestJS.
- Uso de NATS como sistema de mensajería para comunicación entre los microservicios.
- Desarrollo de un API GATEWAY para facilitar la comunicación hacia los microservicios.
- Creación de imagenes Docker para facilitar la implementación y despliegue de los microservicios.
- Uso de bases de datos PostgreSQL y MongoDB dependiento de la necesidad de cada microservicio.
- Uso de JWT para autenticación y autorización de los usuarios.

## Tecnologías utilizadas

- NestJS
- NATS
- PostgreSQL
- MongoDB
- JWT
- Docker
- Stripe
- Prisma
- AWS ECS

## Ejecución proyecto

1. Primero es necesario configurar las variables de entorno de los microservicios
2. Ejecutar docker compose

  docker compose -f docker-compose.yml up

El archivo docker compose tiene todas las configuraciones necesarias para que el proyecto funcione correctamente en localhost:4000

