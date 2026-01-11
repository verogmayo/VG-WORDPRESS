[volver al menú principal](README.md)  
[ir a Instalación de Wordpress](InstalacionWordpress.md)  
[ir a Estructura de Carpetas](EstructuraDeCarpetas.md)  
[ir a Guía de paso a Plesk](GuiaPasoAPlesk.md)  


# CREACIÓN DEL CRUD DE LA TABLA DEPARTAMENTOS
## INSERSIÓN DE LA TABLA DEPARTAMENTOS EN LA BASE DE DATOS DE WP
* Se añade la tabla departamentos a la base de datos de wordpress.
* Se abre la base de datos con phpMyadmin.  
![phpMyadminWordpress](images/crud-CreacionTablaDpts.png)   
* Se crea la tabla y se cargar.
![creación de la tabla departamentos](images/crud-CreacionTablaDpts2.png)  
* Aparecerá en la lista de tablas de la base de datos de wordpress.
![tabla Dptos en bd wordpress](images/crud-TablaDptosENDBWP.png) 

## INSTALACIÓN DEL PLUGIN NECESARIO PARA HACER EL CRUD EN WP
* Para realizar el CRUD de departamentos, utilizaré el plugin de CRUDIATOR(he elegido este porque es el más utilizado para hacer CRUDs pero se podría utilizar otro).  
Se instala y activa el plugin.  
![pluginCrudiator](images/crud-Plugin.png)  


## CREACIÓN DEL CRUD
* Se accede a Crudiator-Add a New Table en el menú principal de wordpress.  
![alt text](images/crud-CrudiatorAddNewTable.png)
* Se elige la tabla en el desplegable que contiene todas las tablas de la base de datos.  
![alt text](images/crud-EleccionTabla.png)  
* Se va elgiendo las opciones en función de lo que se necesite.  
![alt text](images/crud-ConfiguracionCRUD.png) 
* Al darle a publicar, aparece el menú de Mantenimiento de departamentos en el menu de Worpress debajo de Crudiator
![alt text](images/crud-ElementoMtoDptos.png)  
* Si pinchas en él te aparece la tabla de mantenimiento de departamentos.
![alt text](images/crud-TablaMtoDptos.png)  
La documentación de Crudiator se encuentra aquí:
https://crudiator.com/document/

## UTILIZACIÓN DEL CRUD DE MANTENIMIENTO DE DEPARTAMENTOS

### CREATE : CREACIIÔN DE DEPARTAMENTO
* Para crear un departamento se hace clic en Add New
![alt text](images/crud-AddNuevoDptos.png)  
* Se rellenan los campos del nuevo departamento.  
![alt text](images/crud-AddNuevoDptoCampos.png)
* Se indica que el departamento se ha creado bien.  
![alt text](images/crud-AddNewDptoOK.png)  
* El nuevo departamento apararece en la tabla.  
![alt text](images/crud-AddNuevoDptoOk2.png)
* Si se introduce un codigo repetido sale un error de Database.  
![alt text](images/crud-AddNuevoDptoErrorDB.png)    
al darle al boton volver los campos siguen con la información.  
El campo de volumen de negocio, no admite coma, solo punto. **La coma no da error, no se escribe**.  


### READ : CONSULTA DE UN DEPARTAMENTO
* Para consultar un departamento se hace clic en Filter Data en la parte de arriba d ela página de mantenimiento.  
![alt text](images/crud-ReadDptoFiltro.png)  
Sale una ventana donde se  puede indicar el elemento de filtrado, que puede ser cualquiera de los campos.  
![alt text](images/crud-ReadDptoFiltros.png)  
En la parte central se elige el elemento de comparación (igual, mayor que, menos que, contiene...)  
![alt text](images/crud-ReadElementoComparacion.png)  
En la ultima parte se indica el criterio de busqueda y se hace clisc en Start.  
![alt text](images/crud-ReadCriterioBusqueda.png)  
* Aparece la tabla con los departamentos que correspondan al filtro.   
![alt text](images/crud-ReadConsultaDpto.png)  
* Al pasar el raton por encima del departamento aparece un menu. Al hacer clic en View.  
![alt text](images/crud-READMenu.png)  
![alt text](images/crud-READDpto.png)  


### UPDATE : MODIFICACIÓN DE UN DEPARTAMENTO
* Para modificar un elemento pasar el raton en la linea del departamento, aparece un menu.  
![alt text](images/crud-UPDATEMenu.png)    
Tambien se puede editar desde la consulta del Departamento.  
![alt text](images/crud-UPDATEDpto.png)  
* Se modifican los campos que se necesite.  
* ![alt text](images/crud-UPDATEEditar.png)  

### DELETE : BORRAR DEPARTAMENTO
* Para borrar un departamentose elige Delete en el menu del departamento.   
![alt text](images/crud-DELETE.png)  

**Con este plugin solo podrá tener acceso los usuarios con rol de administrador**
El plugin permite elegir el rol pero Wordpress no le da permiso.