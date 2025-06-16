# DrogueriaDataBase

1. Para este ejercicio elegi hacer un sistema de gestión de una droguería. El sistema administra productos, clientes, empleados, pedidos y proveedores. Permite realizar búsquedas avanzadas y filtrados con el fin de apoyar la gestión diaria.

## Como ejecutar la base de datos
- Crear la base de datos con el comando: use drogueria_db
- Importa los datos con los archivos .json existentes en este repositorio: usa el comando mongoimport de esta manera
mongoimport --db drogueria_db --collection productos --file productos.json --jsonArray
mongoimport --db drogueria_db --collection clientes --file clientes.json --jsonArray
mongoimport --db drogueria_db --collection empleados --file empleados.json --jsonArray
mongoimport --db drogueria_db --collection pedidos --file pedidos.json --jsonArray
mongoimport --db drogueria_db --collection proveedores --file proveedores.json --jsonArray


- Consultas:
1. db.clientes.find({ nombre: { $regex: "^Ana", $options: "i" } })
   - Busca clientes cuyos nombres comienzan con "Ana"

2. db.clientes.find({ correo: { $regex: "@hotmail\\.com$", $options: "i" } })
   - Filtra clientes que usan correo electrónico Hotmail

3. db.productos.find({ nombre: { $regex: ".*Jarabe.*", $options: "i" } })
   - Busca productos que tengan "Jarabe" en el nombre

4. db.productos.find({ etiquetas: { $regex: ".*analgésico.*", $options: "i" } })
   - Encuentra productos etiquetados como "analgésico"

5. db.empleados.find({ correo: { $regex: "^juan", $options: "i" } })
   - Busca empleados con correo que empieza con "juan"

6. db.pedidos.find({ estado: { $regex: "Pendiente|Enviado", $options: "i" } })
   - Encuentra pedidos en estado pendiente o enviado

7. db.proveedores.find({ ciudad: { $regex: ".*Cali.*", $options: "i" } })
   - Busca proveedores en ciudades que incluyen "Cali"

8. db.clientes.find({ telefono: { $regex: "^300" } })
   - Filtra clientes con teléfonos que empiezan con 300

9. db.productos.find({ descripcion: { $regex: "antiinflamatorio", $options: "i" } })
   - Encuentra productos cuya descripción contenga "antiinflamatorio"

10. db.productos.find({ codigo_barras: { $regex: "^789" } })
    - Busca productos con código de barras que comienzan con 789

11. db.clientes.find({ ciudad: { $regex: ".*a$", $options: "i" } })
    - Filtra clientes cuyas ciudades terminan en "a"

12. db.empleados.find({ turno: { $regex: "Mañana|Noche", $options: "i" } })
    - Encuentra empleados que trabajan en turno mañana o noche

13. db.productos.find({ fecha_vencimiento: { $regex: "^2025" } })
    - Busca productos que vencen en 2025

14. db.pedidos.find({ "cliente.nombre": { $regex: "Carlos", $options: "i" } })
    - Filtra pedidos de clientes cuyo nombre incluye "Carlos"

15. db.productos.find({ etiquetas: { $regex: "sin receta", $options: "i" } })
    - Filtra productos que no requieren receta médica

16. db.proveedores.find({ productos_suministrados: { $regex: "Paracetamol", $options: "i" } })
    - Busca proveedores que suministran productos que contengan "Paracetamol"

17. db.clientes.find({ correo: { $regex: "^[a-z]+\\.[a-z]+@drogueria\\.com$", $options: "i" } })
    - Filtra clientes con correo institucional siguiendo formato nombre.apellido@drogueria.com

18. db.empleados.find({ cargo: { $regex: "Farmacéutico", $options: "i" } })
    - Encuentra empleados con cargo que contiene "Farmacéutico"

19. db.productos.find({ nombre: { $regex: ".*500mg$", $options: "i" } })
    - Filtra productos cuyo nombre termina con "500mg"

20. db.pedidos.find({ productos: { $elemMatch: { nombre: { $regex: "Ibuprofeno", $options: "i" } } } })
    - Encuentra pedidos que incluyen "Ibuprofeno"

21. db.proveedores.find({ nombre: { $regex: "^Laboratorios", $options: "i" } })
    - Busca proveedores cuyo nombre empieza con "Laboratorios"

22. db.clientes.find({ nombre: { $regex: ".*a$", $options: "i" } })
    - Filtra clientes cuyos nombres terminan en "a"

23. db.productos.find({ descripcion: { $regex: "hidratante", $options: "i" } })
    - Busca productos que mencionan "hidratante" en su descripción

24. db.empleados.find({ correo: { $regex: "@drogueria\\.com$", $options: "i" } })
    - Filtra empleados con correo corporativo de la droguería

25. db.pedidos.find({ estado: { $regex: "^Entregado$", $options: "i" }, fecha: { $regex: "^2025-06" } })
    - Busca pedidos entregados en junio de 2025


  






  
