# Proyecto de Encurtamiento de URLs con AWS Lambda

Este proyecto es un sistema de **encurtamiento de URLs** utilizando **AWS** como infraestructura serverless. Permite a los usuarios generar URLs cortas que redirigen a URLs originales, con un tiempo de expiración configurable.

## Arquitectura del Sistema

El sistema está compuesto por dos funciones **Lambda**:

1. **CreateURLShortLambda**:
   - Genera y almacena las URLs cortas en un bucket de **Amazon S3**, junto con la URL original y el tiempo de expiración.
   
2. **RedirectShortURLLambda**:
   - Gestiona el redireccionamiento, verificando el código de la URL corta y validando si sigue dentro del período de expiración antes de redirigir al usuario.

### Diagrama del Proyecto

![image drawio](https://github.com/user-attachments/assets/3ee298ae-2758-4e63-9859-4f1de72370ca)




## Requisitos Previos

Antes de comenzar, asegúrate de tener instaladas las siguientes herramientas:

- [Java 17](https://www.notion.so/Instalando-Java-17-a6636205fb13442d86998dda72710fdc?pvs=21)
- [Maven](https://www.notion.so/Instalando-o-Maven-c8c4867618ed40c8a2a9e41e4a420714?pvs=21)
- [IntelliJ IDEA o VScode]
- [Insomnia](https://insomnia.rest/download)

---

## Configuración del Entorno

1. **Crear una Cuenta en AWS**: Si no tienes una cuenta de AWS, crea una en [AWS](https://aws.amazon.com/).
2. **Configurar el Proyecto**:
   - Crear la función **Hello World** en AWS Lambda para familiarizarte con su funcionamiento.
   - Desarrollar la función `createShortUrlLambda` para generar URLs cortas dinámicamente.
   - Configurar el bucket de S3 para almacenar los datos de las URLs.
3. **Enviar Solicitudes**:
   - Usar herramientas como Insomnia o Postman para probar las solicitudes y los redireccionamientos.

---

## Objetivo del Proyecto

- **Crear URLs cortas**: Los usuarios podrán generar enlaces acortados que redirijan a URLs originales.
- **Configurar expiración**: Se incluirá un tiempo de expiración para cada URL generada.
- **Escalabilidad serverless**: Usar funciones AWS Lambda para garantizar un sistema eficiente y escalable.


