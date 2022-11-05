# Lab5_Cinematica_Inversa

## Caracterización
### Marcos de referencia

En un principio se empleó el modelo nuevo del robot pincher PhantomX. Se hizo un esquema del manipulador y se ubicaron los marcos de referencia de cada junta.

<p align="center">
  <img src="https://user-images.githubusercontent.com/51519737/200101876-8b6b4f5a-664a-4654-92b0-01a6e7c7200f.jpeg" width="350" />
</p>

### Parámetros de Denavit-Hartenberg

Posteriormente se realizó la tabla de parámetros DH 
<div align="center">

| $\mathbf{i}$ | $\mathbf{\theta_i}$ | $\mathbf{d_i}$ | $\mathbf{a_i}$ | $\mathbf{\alpha_i}$ |
|:------------:|:-------------------:|:--------------:|:--------------:|:-------------------:|
|      $1$     |         $q_1$       |      $L_1$     |       $0$      |   $\frac{\pi}{2}$  |
|      $2$     |         $q_2+\alpha$       |       $0$      |      $L_r$     |         $0$         |
|      $3$     |         $q_3-\alpha$       |       $0$      |      $L_3$     |         $0$         |
|      $4$     |         $q_4$       |       $0$      |      $L_4$     |         $-\frac{\pi}{2}$         |
</div>

## Cinemática inversa
Suponiendo que la herramienta siempre se encuentre en orientación [0,0,0], las siguientes dos ecuaciones salen de forma directa por la geometría y la morfología del manipulador:
<p align="center">
  <img src="https://user-images.githubusercontent.com/51519737/200101800-d63f8b1f-a88c-48c2-a34d-f72db8a827b5.jpeg" width="350" />
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/51519737/200101850-deb8bfc3-951c-464a-b54d-68121377564e.jpeg" width="350" />
</p>

Costruyendo un triángulo con los eslabones 2 y 3, y gracias a la ley del coseno, es posible hallar la expresión para la junta 3.
<p align="center">
  <img src="https://user-images.githubusercontent.com/51519737/200101836-8a0fccd2-ce70-4324-9a81-b7f589234343.jpeg" width="350" />
</p>

Donde r es la distancia entre el inicio del eslabón 2 y el final del estabón 3:
<p align="center">
  <img src="https://user-images.githubusercontent.com/51519737/200101870-4361ceff-9fd8-4bd5-94af-224e22e38942.jpeg" width="350" />
</p>

Por ultimo, por leyes de senos y cosenos podemos hallar la expresión de la junto 2 en términos de los ángulos internos del triángulo anteriormente descrito:

<p align="center">
  <img src="https://user-images.githubusercontent.com/51519737/200101821-695f13cb-07b6-4570-ac95-98cd3000092d.png" width="350" />
</p>

Donde los ángulos beta y psi se calculan de la siguiente manera:

<p align="center">
  <img src="https://user-images.githubusercontent.com/51519737/200101859-6d574ce4-66ff-498e-8bb4-85e3bceca294.jpeg" width="350" />
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/51519737/200101888-78500ea8-5d61-4021-8606-990d16cd7e9d.png" width="350" />
</p>

Siendo H:
<p align="center">
  <img src="https://user-images.githubusercontent.com/51519737/200101783-af6128ee-3008-498e-9342-793c3926e1a3.jpeg" width="350" />
</p>
## Espacio alcanzable
En la orientación anteriormente descrita, se ubica un marcador en el gripper del manipulador y se dibujan 2 arcos de circunferencia con los radios máximos y mínimos físicamente alcanzables en esta configuración.

<p align="center">
  <img src="https://user-images.githubusercontent.com/51519737/200101900-4d4d0a9e-9b05-4be3-81b0-6bdc9ec9935d.jpeg" width="350" />
</p>

## Figuras

Se construyen una serie de figuras, para tal fin se emplea AutoCad, allí se dibujan las diferentes geometrías. Posteriormente se toman diferentes puntos de estas a fin de  construir las trayectorias con estos. Finalmente se usan los algoritmos de cinemática inversa para calcular la postura del robot.

## Resultados
A continuación se muestra el dibujo del triángulo

[![Alt text](https://img.youtube.com/vi/4movyg7vbMI/0.jpg)](https://youtu.be/4movyg7vbMI)

En este video se intentó dibujar las iniciales JO

[![Alt text](https://img.youtube.com/vi/RhO1lrqDqtg/0.jpg)](https://youtu.be/RhO1lrqDqtg)

Por último se muestra cómo el robot realizó el dibujo del circulo

[![Alt text](https://img.youtube.com/vi/oC8Gb0cnQ9Q/0.jpg)](https://youtu.be/oC8Gb0cnQ9Q)

## Integrantes
- Juan Andres Bueno Hortua
- Oscar Javier Manrique Merchan

## Profesores
- Ricardo Emiro Ramirez Heredia
- Jhoan Sebastian Rodriguez Rodriguez
