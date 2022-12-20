Plan de ataque 
Errores y correcciones realizadas al proyecto
Por: Arnold David Bernabé Jerónimo Mijangos

1. let randomNumber = Math.random() * 10
Para comenzar aqui tendriamos que cambiar el 10 por un 100 debido a que el numero que se esta generando actualmente con esta funcion solo esta dentro del
rango de 0 a 10 con lo que se estaria icumpliendo uno de los parametros principales.

2. const ATTEMPS = 5
ya que se comienza con la teoria de que attemps sera el numero de intentos, este debera incrementarse a 10 para que coincida con la cantidad de
intentos solicitados.

3. const lowOrHi = document.querySelector('lowOrHi')
Error de Sintaxis la variable 'lowOrHi' deberia de llevar punto, ademas de que se debe de declarar el estilo correspondiente tomando como ejemplo la 
variable .lastResut

4. Se debe de comprobar que el numero ingresado este entre el rango de 1 a 100 por lo tanto se debe de agregar un comprobante de tipo if con su respectivo 
else para realizar la validacion
if (userGuess > 0 && userGuess <101){
}
else{
  lastResult.textContent = 'Debe ingresar un numero entre 1 y 100';
  lastResult.style.backgroundColor = 'red';
}

5.Se debe Corregir los valores dentro del condicional if(userGuess === randomNumber) para la variable del resultado y color, ya que si el userGuess y 
el randomNumber coinciden, quiere decir que adivino el numero aleatorio, quedando el if asi:
    if(userGuess == randomNumber) {
      lastResult.textContent = 'Felicitaciones! adivinaste el número!';
      lastResult.style.backgroundColor = 'green';
      lowOrHi.textContent = '';
      setGameOver();
    }

6. se deben de editar los valores de resultado dentro de este comprobante ya que de cumplirse se estaria diciendo que llego a los 10 intentos permitidos por lo tanto perdio el juego quedando asi:
 else if(guessCount === ATTEMPS) {
      lastResult.textContent = '!!!Pérdistes!!!';
      lastResult.style.backgroundColor = 'red';
      setGameOver();
}

7. ya en el ultimo else de las comprobantes referente a que el numero que se escribio es incorrecto, se debe de cambiar el backgroundColor de lastResult
a rojo para remarcar el estado incorrecto, a su vez ya que se solicita que el mensaje de alerta de si el numero es mayor o menor tiene que estar en negro 
tenemos que añadir la variable lowOrHi.style.color = 'black'; despues de la comprobacion de si es menor o mayor para que cumpla con los requisitos.


8. corregimos la linea guessSubmit.addeventListener('click', checkGuess); que contenia un error de sintaxis 

9. igualmente corregimos la linea resetButton.addeventListener('click', resetGame); que contiene el mismo error

10. se debe corregir el randomNumber del reset para que vuelva a generar un numero aleatorio entre 1 y 100 y no entre 0 y 1 como lo estaba anteriormente
