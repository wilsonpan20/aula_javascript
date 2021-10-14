//Crie uma função que recebar dois valores como paramentros.
//confira se os numeros são iguais
//confira se a soma dos numeros e maior que 10 ou menor que 20
//Retone uma string dizedo Os numeros num1 e num2 não /são iguais sua soma,que e maior /menor que 10 20
//exemplo
// Output:ps numeros 1 e 2 não sao iguais .sua soam e 3,que e menor que 10 e memor que 20.
function comparaNumero(num1 , num2){
    if(!num1 || !num2) return 'Defina dois numero'
 const primeiraFrase = criaPrimeiraFrase(num1 , num2);
 const segundaFrase = criasegundaFrase(num1 , num2);
 
 return `${primeiraFrase} ${segundaFrase}`

}

function criaPrimeiraFrase(num1 , num2){
  let saoIguais = "";

    if(num1 !== num2){
        saoIguais = "não";
    }
    return `Os números ${num1} e ${num2} ${saoIguais} são iguais.`
}

function criasegundaFrase(num1,num2){
    const soma = num1 + num2;

    let resultado10 = 'menor'
    let resultado20 = 'menor'
    const compara10 = soma > 10;
    const compara20 = soma > 20;
    if(compara10){
        resultado10 = 'maior';
    }

    if(compara20){
        resultado20 ='maior';
    }
    return `Sua soma é ${soma}, que é ${resultado10} que 10 e ${resultado20} que 20 e`
}


console.log(comparaNumero(10,10));

