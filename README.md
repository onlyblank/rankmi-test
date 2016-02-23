# rankmi-test
Para utilizar todos los ejercicios debes clonar el repositorio
```{r, engine='bash', count_lines}
$ git clone 'git@github.com:onlyblank/rankmi-test.git'
$ cd rankmi-test
```
##Ejercicio 1

Optimización del código 

```ruby

def update_user user_data
  begin  
    if status
      if user_role.present? && process_id.present? && user_id.present?
        user_role_process_data = UserRoleProcess.where(user_id: user_id, role_id: user_role, enterprise_process_id: process_id)
        if user_role_process_data.empty?
          status = UserRoleProcess.create(user_id: user_id,role_id: user_role.to_i, enterprise_process_id: process_id.to_i)
        end
      end
    end

    if status
      if area_id.present?
        user_area = UserEnterpriseArea.where(user_id: user_id, enterprise_area_id: area_id.to_i).first

        unless user_area.present?
          status = UserEnterpriseArea.create(user_id: user_id, enterprise_area_id: area_id.to_i)
        end
      end
    end

    return status

  rescue Exception => e
    #Manejo de excepción
  end
end

```
##Ejercicio 2
- Ir a la carpeta del ejercicio
```{r, engine='bash', count_lines}
$ cd  ejercicio2
```
- Correr node
```{r, engine='bash', count_lines}
$ node
```
<sup>***Debes tener instalado node***</sup>

- Importar index.js

```{r, engine='bash', count_lines}
$ var getPosition = require "./index.js"
```

- Llamar la función con la coordenada deseada, por ejemplo "AB"

```{r, engine='bash', count_lines}
$ getPosition("AB")
```
<sup>***La entrada a la función debe contener sólo letras (a-z)***</sup>

##Ejercicio 3

##Ejercicio 4