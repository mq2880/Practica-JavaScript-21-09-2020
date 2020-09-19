# Practica Grupal JavaScript 21/09/2020
Miembros del grupo:

- Juan Ramón Diaz Fernández
- Miguel Ángel Cabrero Luengo
- Juan José Salvador Román
- Rubén García Jiménez
- Francisco Javier Moreno Quevedo

El grupo tiene que realizar los ejercicios del 38 - 75 ambos incluidos. Yo he realizado los ejercicios del 60 al 67 ambos incluidos.



Todos los ejercicios están en una sola página HTML y tienen las siguientes características:

- Cada uno de ellos esta en un bloque div.
- Cada uno de ellos tiene un botón Ejecutar, que ejecuta el JavaScript del ejercicio y que muestra el resultado en un elemento tipo parrafo (p) 
- Los ejercicios que necesitan de algún dato se piden por pantalla utilizando un prompt()
- Se ha hecho la validación de los datos que el usuario introducido, es decir si se espera un número se valida que el usuario haya introducido un número. En caso de que no se cumpla la condición se le vuelve a pedir al usuario que introduzca el dato mostrándole un mensaje parecido a este mensaje: *El valor introducido no es valido vuelva a intentarlo. Cancelar para Salir*
- Si el usuario no introduce nada se muestra en pantalla el mensaje: *El usuario no seleccionó ningún valor.* y el programa finaliza





## Ejercicios



**Ejercicio: 60 Ref:16**
*Escriba un programa JavaScript para calcular la diferencia absoluta entre un número especificado y 19. Devuelve el triple de su diferencia absoluta si el número especificado es mayor que 19.*

```
function CalcularNumero() 
            {
                var result;
                var mensaje = "Introduzca un número"
                document.getElementById("ValEj60").innerHTML = "Solución: ";
                while (valUsuario==undefined || valUsuario=="")
                {
                    var valUsuario = prompt(mensaje);

                    //Si el usuario pulsa cancelar salimos
                    if(valUsuario == null | valUsuario ==  "") {
                        document.getElementById("ValEj60").innerHTML = "Solución: El usuario no seleccionó ningún valor." ;
                        break;
                    }

                    valUsuario = Number(valUsuario);
                    //Comprobamos que el usuario a introducido un numero
                    if(isNaN(valUsuario)){
                        valUsuario = "";
                        mensaje = "El valor introducido no es valido vuelva a intentarlo. Cancelar para Salir";
                    }
                    else{
                        if(valUsuario - 19 > 0){result = Math.abs(valUsuario - 19) * 3;}
                        else{result = Math.abs(valUsuario - 19);}
                        document.getElementById("ValEj60").innerHTML = "Solución: " + result;
                        break;
                    }
                }
            }
```

Se ha utilizado el método ABS del objeto Math para obtener el valor absoluto y realizar las operaciones oportunas.




------

**Ejercicio: 61 Ref:18**
*Escriba un programa JavaScript para verificar dos números dados y devolver verdadero si uno de los números es 50 o si su suma es 50.*

```
function Devolver50() 
                {
                    var result;
                    var mensaje1 = "Introduzca el primer número";
                    var mensaje2 = "Introduzca el segundo número";
                    document.getElementById("ValEj61").innerHTML = "Solución: ";
                    while (valUsuario1 == undefined || valUsuario1=="" || valUsuario2 == null || valUsuario2 ==  "")
                    {
                        if (valUsuario1 == undefined || valUsuario1 == ""){var valUsuario1 = prompt(mensaje1);}

                        //Si el usuario pulsa cancelar salimos
                        if(valUsuario1 == null | valUsuario1 ==  "") {
                            document.getElementById("ValEj61").innerHTML = "Solución: El usuario no seleccionó ningún valor." ;
                            break;
                        }

                        valUsuario1 = Number(valUsuario1);

                        var valUsuario2 = prompt(mensaje2);

                        //Si el usuario pulsa cancelar salimos
                        if(valUsuario2 == null | valUsuario2 ==  "") {
                            document.getElementById("ValEj61").innerHTML = "Solución: El usuario no seleccionó el segundo valor." ;
                            break;
                        }

                        valUsuario2 = Number(valUsuario2);


                        //Comprobamos que el usuario a introducido un numero en las dos ocasiones
                        if(isNaN(valUsuario1)){
                            valUsuario1 = "";
                            mensaje = "El primer valor introducido no es valido vuelva a intentarlo. Cancelar para Salir";
                        }
                        else{
                            if(isNaN(valUsuario2)){
                                valUsuario2= "";
                                mensaje = "El segundo valor introducido no es valido vuelva a intentarlo. Cancelar para Salir";
                            }

                            else{
                                if(valUsuario1 + valUsuario2 == 50 | valUsuario1 == 50 | valUsuario2 == 50){result = "Verdadero";}
                                else{result = "Falso";}
                                document.getElementById("ValEj61").innerHTML = "Solución: " + result;
                                break;
                            }
                        }
                    }
                }
```



------

**Ejercicio: 62 Ref:19**
**Escriba un programa JavaScript para verificar si un número entero está dentro de 20 de 100 o 400.*

```
  function EstaEntre() 
                {
                    var result;
                    var mensaje1 = "Introduzca un número";
                    document.getElementById("ValEj62").innerHTML = "Solución: ";
                    while (valUsuario1 == undefined || valUsuario1=="")
                    {
                        if (valUsuario1 == undefined || valUsuario1 == ""){var valUsuario1 = prompt(mensaje1);}

                        //Si el usuario pulsa cancelar salimos
                        if(valUsuario1 == null | valUsuario1 ==  "") {
                            document.getElementById("ValEj62").innerHTML = "Solución: El usuario no seleccionó ningún valor." ;
                            break;
                        }

                        valUsuario1 = Number(valUsuario1);

                        //Comprobamos que el usuario a introducido un numero 
                        if(isNaN(valUsuario1)){
                            valUsuario1 = "";
                            mensaje = "El valor introducido no es valido vuelva a intentarlo. Cancelar para Salir";
                        }
                        else{
                            if(valUsuario1 <= 20){
                                result = "Valor comprendido entre 0 y 20"
                            }
                            else if(valUsuario1>20 && valUsuario1<=100){
                                result = "Valor comprendido entre 21 y 100"
                            }
                            else if(valUsuario1>100 && valUsuario1<=400){
                                result = "Valor comprendido entre 101 y 400";
                            }
                            else{result = "Valor mayor de 400";}
                        }
                        document.getElementById("ValEj62").innerHTML = "Solución: " + result;
                        break;
                    }
                }
```



------

**Ejercicio: 63 Ref:2**
*Escriba un programa JavaScript para imprimir el contenido de la ventana actual.*

```
 function Imprimir()
                {
                    window.print();
                } 
            
```

Se ha utilizado el método *print* del objeto *window*



------

**Ejercicio: 64 Ref:20**
*Escriba un programa JavaScript para verificar a partir de dos números enteros dados, si uno es positivo y otro negativo.*

```
function Evaluar()
                {
                    var result;
                    var mensaje1 = "Introduzca el primer número";
                    var mensaje2 = "Introduzca el segundo número";
                    document.getElementById("ValEj64").innerHTML = "Solución: ";
                    while (valUsuario1 == undefined || valUsuario1=="" || valUsuario2 == null || valUsuario2 ==  "")
                    {
                        if (valUsuario1 == undefined || valUsuario1 == ""){var valUsuario1 = prompt(mensaje1);}

                        //Si el usuario pulsa cancelar salimos
                        if(valUsuario1 == null | valUsuario1 ==  "") {
                            document.getElementById("ValEj64").innerHTML = "Solución: El usuario no seleccionó ningún valor." ;
                            break;
                        }

                        valUsuario1 = Number(valUsuario1);

                        var valUsuario2 = prompt(mensaje2);

                        //Si el usuario pulsa cancelar salimos
                        if(valUsuario2 == null | valUsuario2 ==  "") {
                            document.getElementById("ValEj64").innerHTML = "Solución: El usuario no seleccionó el segundo valor." ;
                            break;
                        }

                        valUsuario2 = Number(valUsuario2);


                        //Comprobamos que el usuario a introducido un numero en las dos ocasiones
                        if(isNaN(valUsuario1)){
                            valUsuario1 = "";
                            mensaje = "El primer valor introducido no es valido vuelva a intentarlo. Cancelar para Salir";
                        }
                        else{
                            if(isNaN(valUsuario2)){
                                valUsuario2= "";
                                mensaje = "El segundo valor introducido no es valido vuelva a intentarlo. Cancelar para Salir";
                            }

                            else{
                                if(valUsuario1 >= 0 ){result = "El primer número introducido (" + valUsuario1 + ") es positivo ";}
                                else{result = "El primer número introducido (" + valUsuario1 + ") es negativo ";}

                                if(valUsuario2 >= 0 ){result += "y el segundo (" + valUsuario2 + ") es positivo";}
                                else{result += "y el segundo (" + valUsuario2 + ") es negativo";}

                                document.getElementById("ValEj64").innerHTML = "Solución: " + result;
                                break;
                            }
                        }
                    }
                } 
```



------

**Ejercicio: 65 Ref:21**
*Escriba un programa JavaScript para crear una nueva cadena agregando "Py" delante de una cadena dada. Si la cadena dada comienza con "Py", devuelve la cadena original.*

```
function AddPy()
                {
                    var result;
                    var mensaje1 = "Introduzca el primer número";
                    document.getElementById("ValEj65").innerHTML = "Solución: ";
                    while (valUsuario1 == undefined || valUsuario1=="")
                    {
                        if (valUsuario1 == undefined || valUsuario1 == ""){var valUsuario1 = prompt(mensaje1);}

                        //Si el usuario pulsa cancelar salimos
                        if(valUsuario1 == null | valUsuario1 ==  "") {
                            document.getElementById("ValEj64").innerHTML = "Solución: El usuario no seleccionó ningún valor." ;
                            break;}
                        
                        var patt1 = /\bPy/;
                        var posicion =  valUsuario1.search(patt1);
                        if (posicion == 0){
                            result=valUsuario1;
                            }
                        else{
                            result="Py"+valUsuario1;
                            }
                        document.getElementById("ValEj65").innerHTML = "Solución: " + result;
                        break;
                    }                  
                } 
```

Se ha utilizado las expresiones regulares (RegExp) con el patrón \b



------

**Ejercicio: 66 Ref:22**
*Escriba un programa JavaScript para eliminar un carácter en la posición especificada de una cadena dada y devolver la nueva cadena.*

```
function DelChar()
                {
                    var result;
                    var cadena;
                    var mensaje1 = "Introduzca una cadena";
                    var mensaje2 = "Introduzca la posición del caracter que quiere eliminar";
                    document.getElementById("ValEj66").innerHTML = "Solución: ";
                    while (valUsuario1 == undefined || valUsuario1=="" || valUsuario2 == null || valUsuario2 ==  "")
                    {
                        if (valUsuario1 == undefined || valUsuario1 == ""){var valUsuario1 = prompt(mensaje1);}

                        //Si el usuario pulsa cancelar salimos
                        if(valUsuario1 == null || valUsuario1 ==  "") {
                            document.getElementById("ValEj66").innerHTML = "Solución: El usuario no seleccionó ninguna cadena." ;
                            break;
                        }
                        var valUsuario2 = prompt(mensaje2);

                        //Si el usuario pulsa cancelar salimos
                        if(valUsuario2 == null || valUsuario2 ==  "") {
                        document.getElementById("ValEj66").innerHTML = "Solución: El usuario no seleccionó ninguna posición." ;
                        break;
                        }

                        valUsuario2 = Number(valUsuario2);
                        if(isNaN(valUsuario2)){
                                valUsuario2= "";
                                mensaje = "El valor de la posición introducido no es valido vuelva a intentarlo. Cancelar para Salir";
                            }

                        else{

                            result = valUsuario1.slice(0,valUsuario2);
                            result += valUsuario1.slice(valUsuario2 + 1,valUsuario1.length);

                            document.getElementById("ValEj66").innerHTML = "Solución: " + result;
                            break;
                        }
                    }
                } 
```

Se ha utilizado el método *slice* del objeto *text*.



------

**Ejercicio: 67 Ref:23**
*Escriba un programa JavaScript para crear una nueva cadena a partir de una cadena dada cambiando la posición del primer y último carácter. La longitud de la cadena debe ser mayor o igual a 1.*

```
function DelChar()
            {
                var result;
                var mensaje1 = "Introduzca un texto";
                document.getElementById("ValEj67").innerHTML = "Solución: ";
                while (valUsuario1 == undefined || valUsuario1=="" )
                {
                    if (valUsuario1 == undefined || valUsuario1 == ""){var valUsuario1 = prompt(mensaje1);}

                    //Si el usuario pulsa cancelar salimos
                    if(valUsuario1 == null || valUsuario1 ==  "") {
                        document.getElementById("ValEj67").innerHTML = "Solución: El usuario no seleccionó ningún texto." ;
                        break;
                    }
                    
                    result =valUsuario1.substr(valUsuario1.length-1,1) + valUsuario1.substr(1,valUsuario1.length-2) + valUsuario1.substr(0,1);

                    document.getElementById("ValEj67").innerHTML = "Solución: " + result;
                    break;
                }
            } 
```

Se ha utilizado el método *substr* del objeto *text*.