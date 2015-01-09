# Ciclos

Los ciclos o bucles se utilizan para ejecutar un bloque de codigo una cantidad limitada de veces o en algunas oportunidades ilimitada. En caso de ser limitada, el ciclo al igual que el IF, UNLESS y CASE, toma una condicion, la cual sera la que decidira si el ciclo debe parar o no.

Es importante que la condicion de parada del ciclo este bien definida para el ciclo pare, en caso contrario quedara en un ciclo infinito.

** Ejemplo: **

Supongamos que estamos jugando 21 o Blackjack, en dicho juego hay un ciclo "infinito" en el cual el dealer entrega una carta a el jugador, pero dicho ciclo para cuando el usuario dice que no quiere que le den mas cartas o cuando la sumatoria de los valores de las cartas es mayor a 21.

En Ruby existe soporte a los ciclos tradicionales como son:

- WHILE
- FOR
- UNTIL
- REPEAT

## WHILE

El ciclo while ejecuta un bloque de codigo mientras la condicion retorne TRUE.

```ruby
# Ejemplo del blackjack con un while

# Cuando la condicion de parada depende a su vez de dos elementos
# como son la sumatoria <= 21 o que el usuario pida mas cartas
# Esto es una operacion Boleana entre dos condiciones donde:
#  
# || significa "o", es decir, que cualquiera de las dos condiciones sea cierta
# && significa "y", es decir, que las dos condiciones sea cierta al mismo tiempo

while suma_de_cartas <=  21 || usuario_pida_otra_carta  do
  puts "Tiene una carta nueva"
end
```

Otro ejemplo del uso de ciclo puede ser realizar operaciones matematicas o cuentas numericas. Donde una accion se debe ejecutar N cantidad de veces, donde N es un numero entero.

Los ciclos o bucles se utilizan para ejecutar un bloque de código una cantidad limitada de veces. Es importante que la condicion de parada del ciclo esté bien definida para que el ciclo se detenga, en caso contrario quedara en un ciclo infinito.

```ruby
#!/usr/bin/ruby

iterador = 0

while iterador <  5  do
  puts "el número es: #{numero}"
  iterador = iterador + 1
end
```

Al ejecutar el archivo obtendremos este resultado.

```bash
ruby ~/Desktop/ejemplo_while.rb

el número es: 0
el número es: 1
el número es: 2
el número es: 3
el número es: 4
```

## REPEAT

El repeat funciona de manera similar a el while pero la condición se ejecuta al final del bloque

```ruby
#!/usr/bin/ruby

iterador = 0

begin
  puts "el número es: #{numero}"
  
  # existen operadores matematicos especiales para incrementar o decrementar una variable
  # como lo es += X y el -= X. Donde X es un Entero o Flotante. 
  iterador += 1
end while iterador <  5
```

Al ejecutar el archivo obtendremos este resultado.

```bash
ruby ~/Desktop/ejemplo_repeat.rb

el número es: 0
el número es: 1
el número es: 2
el número es: 3
el número es: 4
```

## UNTIL

El until ejecuta un bloque de código hasta que se cumpla la condición, es decir, hasta que la condición retorne TRUE

```ruby
#!/usr/bin/ruby

iterador = 0

until iterador > 5
  puts "el número es: #{iterador}"
  iterador += 1
end
```

Al ejecutar el archivo obtendremos este resultado.

```bash
ruby ~/Desktop/ejemplo_until.rb

el número es: 0
el número es: 1
el número es: 2
el número es: 3
el número es: 4
el número es: 5
```

## FOR

El método for ejecuta un bloque de código por cada elemento dentro de un rango o un array (el rango y el array no son lo mismo)

Ejemplo

```ruby
#!/usr/bin/ruby

for i in 0..5
  puts "El valor de la variable es: #{i}"
end

puts 'En caso de ser un arreglo'
arreglo = ['uno', 'dos', 'tres', 'cuatro', 'cinco', 'seis']

for i in arreglo
  puts "El valor de la variable es: #{i}"
end
```

El resultado de ejecutar este archivo sería.

```bash
ruby ~/Desktop/ejemplo_for.rb

El valor de la variable es: 0
El valor de la variable es: 1
El valor de la variable es: 2
El valor de la variable es: 3
El valor de la variable es: 4
El valor de la variable es: 5
En caso de ser un arreglo
El valor de la variable es: uno
El valor de la variable es: dos
El valor de la variable es: tres
El valor de la variable es: cuatro
El valor de la variable es: cinco
El valor de la variable es: seis
```

## Conclusión

En ruby podemos ejecutar un código N cantidad de veces usando las estructuras de ciclos antes mencionadas, aunque en Ruby generalmente estos ciclos no son usados regularmente
