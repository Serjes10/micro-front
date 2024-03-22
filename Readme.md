#Pasos para instalar proyecto
Se requiere Angular 14 en adelante y nodeJs.
Ejecutar en cada uno de los proyectos: `npm install`.
Ejecutar en cada uno de los proyectos: `ng serve mf-host` `ng serve mf-contabilidad`.

#Pasos configurar MicroFront
# Crear Proyectos

ng new mf-shell
ng new mf-contabilidad

# Instalar Angular Module Federation en cada proyecto

npm i -D @angular-architects/module-federation@16.0.4

# Configurar host y remote

ng add @angular-architects/module-federation --project mf-shell --port 4200 --type host
ng add @angular-architects/module-federation --project mf-contabilidad --port 4201 --type host

# Configurar Webpack del host y remote
En el host quitar la importacion de los remote.
En el Remote configurar que cargue el module

# Configurar AppRouting Host y del Remote
