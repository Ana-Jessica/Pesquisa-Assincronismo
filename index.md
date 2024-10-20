Codigos de Exemplo:

AJAX:
![alt text](image.png)

var xhr = new XMLHttpRequest();
xhr.open("GET", "https://api.exemplo.com/dados", true);
xhr.onreadystatechange = function () {
  if (xhr.readyState == 4 && xhr.status == 200) {
    console.log(xhr.responseText);
  }
};
xhr.send();

Promisses:
![alt text](image-1.png)
let promise = new Promise(function(resolve, reject) {
  setTimeout(() => resolve("Sucesso!"), 1000);
});
promise.then(result => console.log(result));

Fetch API:
![alt text](image-2.png)
fetch("https://api.exemplo.com/dados")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error(error));

Async e Await:
![alt text](image-3.png)
async function fetchData() {
  try {
    let response = await fetch("https://api.exemplo.com/dados");
    let data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}
fetchData();


Hoisting:
![alt text](image-4.png)
console.log(minhaFuncao());
function minhaFuncao() {
  return "Função elevada";
}

Arrow Functions:
![alt text](image-5.png)
// Função normal
function normalFunction() {
  return "Função normal";
}

// Arrow function
const arrowFunction = () => "Função arrow";

Desestruturação (Destructuring):
![alt text](image-6.png)
const pessoa = { nome: "João", idade: 25 };
const { nome, idade } = pessoa;
console.log(nome, idade);

Closure:
![alt text](image-7.png)
function criaContador() {
  let contador = 0;
  return function() {
    contador++;
    return contador;
  };
}
const contador1 = criaContador();
console.log(contador1()); // 1
console.log(contador1()); // 2