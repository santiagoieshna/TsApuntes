## Pasos

Hay que seguir una serie de pasos a seguir para depurar typescript en VsCode

### Habilitar mapeo de js
configuracion [[01_Configuracion#sourceMap|sourceMap]]   
### Colocar BreakPoint

![[breakpoint.png]]

### depurador de VsCode 

-  Pinchar en la opción *create a laucnh.json file*

![[depuradorvscode.png]]

- Elegir la opción node.js 

![[depurar-opciones.png]]

Una vez elegida la opción , se genera un archivo launch.json. 

![[archivo-launch.json.png]]

#### launch.json

**IMPORTANTE**: configurar tal cual. no improvisar aquí.

añadir entre *"program"* y *"outFiles"* el parámetro -> ****preLaunchTask***  

`"preLaunchTask":"tsc: build - tsconfig.json"                          `

Copiarlo tal cual con los espacios.

![[modificar-launch.json.png]]


