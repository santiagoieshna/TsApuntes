
## ¿De que rollo va TypeScript? 

TypeScript tiene la misión de tipar los datos, cosa que no se hace en javaScript. Cuando escribimos en ts (typescript), a la hora de la verdad, lo que acaba de ejecutandose es un archivo js ( javaScript). Cuando acabamos un archivo tsc, lo convertimos a js mediante el comando tsc.

![[tscmanual.png]]

en este ejemplo pasamos de un archivo ts a js:

![[pasarTsAJs.png]]

Configuración de TypeScript 

TypeScript tiene una configuración customizable, esto quiere decir que podemos cambiar la forma de escribir en él para ser más permisivos o menos permisivos. 

Para ello, se usa un archivo de configuración llamado tsconfig.json, este archivo se genera con el comando: 
`                                 tsc -init                                     `

![[tsc-init_tsconfig.png]]

Una vez hecho esto, tendremos en nuestro directorio el archivo 

![[archivo_tsconfigJSON.png]]

En este archivo nos encontraremos tantas opciones que ni los de TypeScript se las saben…
Cuando tengamos que cambiar alguna la cambiaremos.

## Parámetros básicos en tsconfig.json

- línea 14 target: indicar a que versión de js se está transcribiendo.
- línea 29 rootDir: indica al proyecto, donde se encuentran los archivos de Typescript. 
- línea 58 outDir: indica dónde se generan los archivos js transcritos.
- línea 59 removeComments: eliminar comentarios del ts en el archivo js.
- línea 71 noEmitOnError: Si el código fuente de ts tiene algún error, este parámetro indicará si se transcribe o no a js.

##### target

![[parametro-target.png]]

##### rootDir

![[parametro-rooDir.png]]

##### outDir y removeComments

el directorio dist es una convención.

![[parametro-outDir.png]]


##### noEmitOnError

![[parametro-noEmitError.png]]


## Comando tsc

- el comando tsc sin nada mas hará las conversiones necesarias, con la configuración asignada

*Nota*: Si ahora tuviéramos un ts fuera de src (menos en dist), en el mismo nivel de tsconfig.json, nos saltara error de que no todos los archivos están en src.