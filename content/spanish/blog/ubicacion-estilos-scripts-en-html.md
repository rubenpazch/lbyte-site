---
title: Ubicación de hojas de estilos y scripts en un archivo HTML
meta_title: Ubicación de hojas de estilos y scripts en un archivo HTML
description: En HTML, la ubicación de las hojas de estilos (<link>) y los scripts (<script>) tiene un impacto significativo en el rendimiento y la experiencia del usuario
date: 2022-03-27T05:00:00.000Z
image: /images/css-html-js.png
categories: [Referencias, Javascript, css, HTML]
author: LBYTE
tags: [javascript, html, css]
draft: false
---


En HTML, la ubicación de las hojas de estilos (\<link>\) y los scripts \(\<script>\) tiene un impacto significativo en el rendimiento y la experiencia del usuario. Aquí está una explicación más detallada:

## Hojas de Estilo en el \<head>


### Razón Principal: Renderizado Inicial Correcto

* Las hojas de estilo se colocan en el **\<head>** para que el navegador las cargue y aplique antes de renderizar el contenido de la página. Esto asegura que la página se muestre correctamente estilizada desde el principio.

* Si las hojas de estilo se cargaran después del contenido, los usuarios podrían ver un "flash of unstyled content" (FOUC), donde el contenido aparece sin estilos por un breve momento.

### Bloqueo de Renderizado

* Los navegadores detienen el renderizado de la página hasta que las hojas de estilo en el **\<head>** se cargan completamente. Esto es necesario porque los estilos afectan cómo se muestra el contenido.

## Scripts al Final del \<body>

### Razón Principal: Rendimiento

* Los scripts bloquean el renderizado de la página mientras se descargan y ejecutan. Si se colocan en el **\<head>**, el navegador no puede mostrar el contenido hasta que los scripts terminen de ejecutarse.

* Al colocarlos al final del **\<body>**, el navegador puede cargar y renderizar el contenido HTML primero, mejorando el tiempo de carga percibido por el usuario.
Interacción con el DOM

Muchos scripts necesitan que el DOM esté completamente cargado antes de ejecutarse. Colocarlos al final del **\<body>** asegura que el DOM ya esté disponible.

## Excepciones

### Scripts Asíncronos o Diferidos

* Si necesitas cargar scripts en el \<head>, puedes usar los atributos **async** o **defer**:
    * **async**: El script se descarga en paralelo al HTML, pero se ejecuta tan pronto como se descarga, lo que puede interrumpir el renderizado.
    * **defer**: El script se descarga en paralelo, pero se ejecuta después de que el HTML se haya cargado completamente.

## Resumen

* Hojas de estilo: Siempre en el **\<head>** para garantizar un renderizado correcto y estilizado.
* Scripts: Preferiblemente al final del **\<body>** para evitar bloquear el renderizado y mejorar el rendimiento. Si es necesario, usa async o defer para scripts en el **\<head>**.