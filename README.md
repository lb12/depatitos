# Depatitos


## Introducción

**Depatitos** es el proyecto final del *VII Full Stack Web Bootcamp* de *Keepcoding* hecho por mi. Este repositorio contiene una aplicación completamente funcional para manejar la compra/venta de artículos. Las caracteríticas principales del proyecto realizadas son las siguientes:

* Aplicación desarrollada en el MERN Stack.
* Uso de Redux avanzado (Thunks, multiple reducers, async creators y connected middlewares).
* Aplicación completamente responsive utilizando flexbox y la librería de bootstrap.
* Uso de Google Recaptcha como primera barrera antibots.
* Internacionalización de la web y language-detector.
* Compartir anuncios via RRSS.
* Preocupación por el *SEO friendly* mediante el uso de *slugs* en los nombres de los anuncios y los usuarios en las URL.
* Documentación sencilla y dinámica de un API REST desarrollado con NodeJS y express.js utilizando Swagger.
* Autenticación vía JWT.

## ¿Cómo funciona?

El proyecto está dividido en dos: la parte backend y la parte frontend, los puedes encontrar en sus respectivas carpetas: `wc-backend` y `wc-frontend`. Cada una de las carpetas está alojada en un repositorio distinto de GitHub.

* wc-backend: `https://github.com/lb12/wc-backend`
* wc-frontend: `https://github.com/lb12/wc-frontend`

En los submódulos de cada uno tienes un **README.md** que te dará toda la información necesaria para poder arrancar individualmente cada uno. Sin embargo, el proceso se puede resumir de la siguiente manera:

* Clonar este repositorio
* En cada una de las carpetas instalar todas las dependencias utilizando `$ npm install`.
* En la carpeta de backend, añadir las variables de entorno en un archivo `.env`, instalar los datos de muestra con `$ npm run db_init` y arrancar el backend con `$ npm start`.
* En la carpeta de frontend, arrancar directamente con `$ npm start`

Una vez hecho lo anterior, deberías de poder acceder al API en dirección `http://localhost:3005/api-v1` y a su documentación en `http://localhost:3005/`.

Respecto a la parte frontend, abre una ventana del navegador y en `http://localhost:3000` tendrás el frontend arrancado.

## ¿Lo tienes desplegado en algún sitio?

Este proyecto lo puedes ver desplegado en `https://depatitos.com` y el API puedes acceder a ella en el subdominio: `https://api.depatitos.com`.

Actualmente está hosteado en una instancia EC2 de AWS. Está instalado nginx como proxy inverso que sirve las peticiones al backend y al frontend indistamente. A su vez, nginx sirve los estáticos del backend, todo ello bajo el protocolo HTTP2.

Ambos servicios utilizan certificado SSL servido vía LetsEncrypt.
