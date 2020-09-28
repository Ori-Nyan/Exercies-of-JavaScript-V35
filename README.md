# Exercies-of-JavaScript-V35

Ejercicios de Javascript


// Programar una función que invierta las palabras de una cadena de texto. Ejemplo: miFuncion("Hola Mundo") devolverá "odnuM aloH"

const invierteCadena = (cadena = "") =>
    (!cadena)
        ? console.warn("No ingresaste un texto para invertir")
        : console.info(cadena.split('').reverse().join(''))

invierteCadena();
invierteCadena("Hola Mundo");





// Programar una función para contar el número de veces que se repite una palabra en un texto largo. Ejemplo: miFuncion("hola mundo adios mundo", "mundo") devolverá 2

const evaluaFrase = (frase, palabra) => {
    if (!frase) return console.warn("No se ha ingresado una frase para evaluar");
    if (!palabra) return console.warn("No se ha ingresado una palabra para evaluar en la frase");

    let contador = 0,
        posicion = frase.indexOf(palabra);

    while(posicion !== -1){
        contador ++;
        posicion = frase.indexOf(palabra, posicion + 1);
    }

    return console.info(`La palabra ${palabra} se repite ${contador} veces`)
}

evaluaFrase();
evaluaFrase("Hey Hey Hey");
evaluaFrase("Hola ave. Hola sol. Hola luna y estrellas", "Hola");





// Programar una función que valide si una palabra o frase dada es un palíndromo, que se lee igual en un sentido que en otro. Ejemplo: mifuncion("Salas") devolverá true.

const evaluaPalindromo = (palabra = "") => {
    if (!palabra) return console.warn("No se ha ingresado una palabra");

    let palabraReversa = palabra.toLowerCase().split('').reverse().join('');

    if (palabra.toLowerCase() === palabraReversa){
        return console.info(true)
    } else {
        return console.info(false)
    }
}

evaluaPalindromo();
evaluaPalindromo("hola");
evaluaPalindromo("salas");
evaluaPalindromo("hAnNaH");






// Programar una función que elimine cierto patrón de caracteres de un texto dado. Ejemplo: miFuncion("xyz1, xyz2, xyz3, xyz4 y xyz5", "xyz") devolverá  "1, 2, 3, 4 y 5.

const eliminaPatron = (texto = "", patron = undefined) =>{
    if (!texto) return console.warn("No se ingreso un texto")
    if (patron === undefined) return console.warn("No se ingreso un patrón para eliminar")

    return console.log(texto.replaceAll(patron, ''));
}

eliminaPatron();
eliminaPatron("Hola dola mola");
eliminaPatron("xyz1, xyz2, xyz3, xyz4 y xyz5", "xyz")

// Ejercicios del Curso de JavaScript de Jon Mircha: https://www.youtube.com/watch?v=Xh8p7aZBiaw       
