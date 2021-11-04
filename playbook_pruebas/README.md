# Ansible - playbook_pruebas

	- Ejemplo de un playbook que llama a un rol 

	- En este caso el rol se encuentra dentro de la carpeta Roles
	- Pero podria estar referenciado en el archivo requeryment.yml y no existir la carpeta Roles


## Precondiciones:
	- Tener instalado ansible

## Ejecucion:
```
reset; ansible-playbook -i inventory/hosts playbook.yml
```
### Contenido:
	- playbook.yml  -> receta 
	- ansible.cfg -> configuracion local de ansible
	- inventory
		- hosts -> inventario propiamente dicho en formato INI
		- host_vars  -> variables espesificas a un host
		- group_vars -> variables espesificas para grupos de host
	

### Comportamiento:
	- El playbook llama al rol: multi_Pruebas y se ejecuta contra el listado de host definido
	tomando los valores de las variables de los distintos archivos 
	- Para ver que hace el rol en cuestion ver README.md del rol (dentro de la carpeta roles)
	