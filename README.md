# Sistema de Alerta de Stock Crítico
---

---
# Imagenes 
---
### Flujo Anterior 
---
![alt text](image.png)
---
### Flujo Nuevo
---
Nodos nuevos, conectados justo después de "Actualizar Stock":

Stock Crítico?(SI): compara nuevoStock <= 3(operador numérico lte). Se evalúa por cada producto del pedido.
Alerta Stock Crítico(Telegram → rama TRUE): envía al Chat ID del admin ( 6794936273) el mensaje exacto:
⚠️ ALERTA DE STOCK: El producto [Nombre] solo tiene [Cantidad] unidades. Favor reabastecer.
¿Stock en 0?(SI, opcional/puntos extra, tras enviar la alerta): comprueba nuevoStock <= 0.
Marcar AGOTADO en Menú(Actualización de Google Sheets → rama TRUE): si el stock llegó a 0, actualiza la columna Nombre de la hoja Menú anteponiendo el prefijo (AGOTADO)al nombre del producto.
![alt text](image-1.png)
![alt text](image-2.png)
---
# Logica
---

---

# Estructura 