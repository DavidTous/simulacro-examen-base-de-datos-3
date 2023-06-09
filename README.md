# simulacro-examen-base-de-datos-3
1.-
SELECT * 
FROM Piezas 
WHERE color = 'rojo';

2.-
SELECT * 
FROM Proveedores 
WHERE ciudad_proveedor = 'Madrid';

3.-
SELECT nombre_pieza 
FROM Piezas 
WHERE MAX(peso);

5.-
SELECT DISTINCT nombre_proveedor
FROM Proveedores 
INNER JOIN Piezas ON proveedores.id_proveedor = piezas.id_proveedor
WHERE pz.color = 'azul';

6.-
SELECT p.nombre_proveedor
FROM Proveedores 
INNER JOIN Piezas ON proveedores.id_proveedor = piezas.id_proveedor
WHERE piezas.peso = (
  SELECT MAX(peso) FROM Piezas
);

7.-
SELECT *
FROM Piezas
INNER JOIN Proveedores ON proveedores.id_proveedor = piezas.id_proveedor
WHERE proveedores.ciudad_proveedor = 'Barcelona';
