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
  a. db.clientes.find({ nombre: { $regex: "^Ana", $options: "i" } }) - Busca clientes cuyos nombres comienzan con "Ana"
  b. db.clientes.find({ correo: { $regex: "@hotmail\\.com$", $options: "i" } }) - Filtra clientes que usan correo electrónico Hotmail
  c. db.productos.find({ nombre: { $regex: ".*Jarabe.*", $options: "i" } }) - Busca productos que tengan "Jarabe" en el nombre
  d. db.productos.find({ etiquetas: { $regex: ".*analgésico.*", $options: "i" } }) - Encuentra productos etiquetados como "analgésico".
  e. db.empleados.find({ correo: { $regex: "^juan", $options: "i" } }) - Busca empleados con correo que empieza con "juan"
  f. db.pedidos.find({ estado: { $regex: "Pendiente|Enviado", $options: "i" } }) - Encuentra pedidos en estado pendiente o enviado
  g. db.proveedores.find({ ciudad: { $regex: ".*Cali.*", $options: "i" } }) - Busca proveedores en ciudades que incluyen "Cali"
  h. db.clientes.find({ telefono: { $regex: "^300" } }) - Filtra clientes con teléfonos que empiezan con 300
  i. db.productos.find({ descripcion: { $regex: "antiinflamatorio", $options: "i" } }) - Encuentra productos cuya descripción contenga "antiinflamatorio"
  j. db.productos.find({ codigo_barras: { $regex: "^789" } }) - Busca productos con código de barras que comienzan con 789
  k. db.clientes.find({ ciudad: { $regex: ".*a$", $options: "i" } }) - Filtra clientes cuyas ciudades terminan en "a" (ej. Barranquilla)
  l. db.empleados.find({ turno: { $regex: "Mañana|Noche", $options: "i" } }) - Encuentra empleados que trabajan en turno mañana o noche
  m. db.productos.find({ fecha_vencimiento: { $regex: "^2025" } }) - Busca productos que vencen en 2025
  n. db.pedidos.find({ "cliente.nombre": { $regex: "Carlos", $options: "i" } }) - Filtra pedidos de clientes cuyo nombre incluye "Carlos".
  o. db.productos.find({ etiquetas: { $regex: "sin receta", $options: "i" } }) - Filtra productos que no requieren receta médica.
  p. db.proveedores.find({ productos_suministrados: { $regex: "Paracetamol", $options: "i" } }) - Busca proveedores que suministran productos que contengan "Paracetamol"
  q. db.clientes.find({ correo: { $regex: "^[a-z]+\\.[a-z]+@drogueria\\.com$", $options: "i" } }) - Filtra clientes con correo institucional siguiendo formato
  r. db.empleados.find({ cargo: { $regex: "Farmacéutico", $options: "i" } }) - Encuentra empleados con cargo que contiene "Farmacéutico"
  s. db.productos.find({ nombre: { $regex: ".*500mg$", $options: "i" } }) - Filtra productos cuyo nombre termina con "500mg"
  t. db.pedidos.find({ productos: { $elemMatch: { nombre: { $regex: "Ibuprofeno", $options: "i" } } } }) - Encuentra pedidos que incluyen "Ibuprofeno"
  u. db.proveedores.find({ nombre: { $regex: "^Laboratorios", $options: "i" } }) - Busca proveedores cuyo nombre empieza con "Laboratorios"
  v. db.clientes.find({ nombre: { $regex: ".*a$", $options: "i" } }) - Filtra clientes cuyos nombres terminan en "a"
  w. db.productos.find({ descripcion: { $regex: "hidratante", $options: "i" } }) - Busca productos que mencionan "hidratante" en su descripción
  x. db.empleados.find({ correo: { $regex: "@drogueria\\.com$", $options: "i" } }) - Filtra empleados con correo corporativo de la droguería
  y. db.pedidos.find({ estado: { $regex: "^Entregado$", $options: "i" }, fecha: { $regex: "^2025-06" } }) - Busca pedidos entregados en junio de 2025











  




  






  
