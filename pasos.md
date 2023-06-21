# PRIMEROS PASOS EN NPM

Desde una terminal o línea de comandos, crea un directorio con el nombre de tu proyecto. Después, como buena práctica, inicia un repositorio local de Git dentro de la carpeta creada.

El símbolo $ representa la línea de entrada para los comandos en la terminal.

```

Terminal
$ mkdir npm $ cd npm $ git init Initialized empty Git repository in /pruebas/.git/ ```

Una vez creado el espacio correspondiente al proyecto de JavaScript. Deberás tener un archivo de configuración llamado package.json.

Cómo estructurar un archivo de configuración package.json
El archivo package.json es un archivo de configuración que contiene la información más importante de tu proyecto como: datos específicos, dependencias, dependencias de desarrollo y archivos de ejecución.

Este archivo, como su extensión lo indica, está estructurado en formato JSON (JavaScript Object Notation) que sirve para una mejor lectura e interpretación para los usuarios y las máquinas.

Datos específicos del archivo package.json
Los datos específicos ayudan a identificar el proyecto y actúan como una base para que los usuarios y los contribuidores obtengan información sobre el proyecto.

El archivo package.json estaría estructurado inicialmente por las siguientes propiedades:

"name": Indica el nombre del proyecto.
"version": Indica la versión del proyecto.
"description": Indica una breve descripción del proyecto.
"main": Indica el archivo principal del proyecto.
"scripts": Indica los comandos a ejecutar del proyecto (no te preocupes por el comando test por ahora).
"keywords": Indica las palabras clave del proyecto.
"author": Indica el nombre y dirección de correo electrónico del propietario del proyecto.
"license": Indica la licencia del proyecto.
El archivo package.json estaría estructurado de la siguiente manera:

json // archivo package.json

{ "name": "npm", "version": "1.0.0", "description": "Constuir un paquete para node", "main": "src/index.js", "scripts": { "test": "echo \"Error no test specified\" && exit 1" }, "keywords": [ "javascript", "node", "package" ], "author": "TuNombre tucorreo@gmail.com", "license": "MIT" } ```

Cómo utilizar el comando npm init
Aunque puedes crear el archivo de configuración manualmente, NPM te ayuda a crearlo rápidamente mediante el comando npm init. Este comando te permite ingresar los datos específicos del proyecto y genera el archivo package.json en tu directorio.

```bash $ npm init This utility will walk you through creating a package.json file. It only covers the most common items, and tries to guess sensible defaults.

See npm help init for definitive documentation on these fields and exactly what they do.

Use npm install <pkg> afterwards to install a package and save it as a dependency in the package.json file.

Press ^C at any time to quit. package name: (npm) ```

Puedes ingresar tus propios datos, o utilizar la recomendación de NPM (lo que está entre paréntesis) y solamente dar enter. Al final, te preguntará si la configuración del package.json es correcta para generar el archivo.

```bash version: (1.0.0) description: Constuir un paquete para node entry point: (index.js) src/index.js test command: npm test git repository: keywords: javascript, node, package author: TuNombre tucorreo@gmail.com license: (MIT) About to write to /npm/package.json:

{ "name": "npm", "version": "1.0.0", "description": "Constuir un paquete para node", "main": "src/index.js", "scripts": { "test": "echo \"Error no test specified\" && exit 1" }, "keywords": [ "javascript", "node", "package" ], "author": "TuNombre tucorreo@gmail.com", "license": "MIT" }

Is this OK? (yes) ```

Cómo utilizar el comando npm init --yes
El comando npm init --yes o npm init -y te ayudará a crear un archivo package.json de manera rápida con una configuración por defecto, sin la necesidad de ingresar los datos.

Para establecer esta configuración por defecto, necesitarás utilizar el comando npm config set init-<atributo>. Te comparto algunas de las configuraciones por defecto más comunes:

bash $ npm config set init-author-name "Tu Nombre" $ npm config set init-author-email "TuEmail@email.com" $ npm config set init-author-url "https://tuWeb.com" $ npm config set init-license "MIT" $ npm config set init-version "0.0.1"

De esta manera ya estás listo para gestionar dependencias de tu proyecto con NPM.