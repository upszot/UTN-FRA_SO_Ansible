# Ansible - playbook_pruebas

	- Ejemplo de un playbook que llama a dos roles y uso de tags

	- En este caso los roles se encuentra dentro de la carpeta Roles
	- Pero podria estar referenciado en el archivo requeryment.yml y no existir la carpeta Roles
	- Los roles se crearon ingresando dentro de la carpeta roles y ejecutando el comando:
```sh
ansible-galaxy role init role_01
ansible-galaxy role init role_02
```


## Precondiciones:
	- Tener instalado ansible

## Ejecucion (Parado en la carpeta "playbook_pruebas"):
```sh
reset; ansible-playbook -i inventory/hosts  playbook.yml
reset; ansible-playbook -i inventory/hosts  playbook.yml  -t role_01
reset; ansible-playbook -i inventory/hosts  playbook.yml  -t role_02
```
### Contenido:
	- playbook.yml  -> receta 
	- ansible.cfg -> configuracion local de ansible
	- inventory
		- hosts -> inventario propiamente dicho en formato INI
		- host_vars  -> variables espesificas a un host
		- group_vars -> variables espesificas para grupos de host
	

### Comportamiento:
	- Para el 1er caso el playbook ejecuta todas las tareas dentro de playbook.yml mas las tareas definidas en cada uno de los roles
	- Para el 2do y 3er caso el playbook ejecuta las tareas dentro de playbook.yml (con tag allways) , realiza el include del role segun el tag pedido en la ejecucion 
	
