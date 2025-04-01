# revis-oPOO
Revisão feita em aula de POO

Revisão de POO

// Classe base
class Animal {
constructor(nome, especie, idade) {
this.nome = nome;
this.especie = especie;
this.idade = idade;
}
exibirInformacoes() {
return `Nome: ${this.nome}, Espécie: ${this.especie}, Idade: ${this.idade}`;
}
}
// Classe derivada
class AnimalSelvagem extends Animal {
constructor(nome, especie, idade, habitat) {
super(nome, especie, idade);
this.habitat = habitat;
}
exibirHabitat() {
return `Habitat natural: ${this.habitat}`;
}
}

// Instâncias e retornos
const animal1 = new Animal("Tico", "Macaco", 4);
const animal2 = new AnimalSelvagem("Nala", "Leoa", 5, "Savana Africana");
console.log(animal1.exibirInformacoes());
console.log(animal2.exibirInformacoes());
console.log(animal2.exibirHabitat());

Perguntas:

1. Estrutura de Classes e Objetos

A) Na classe animal, os atributos definidos são: nome, espécie e idade;

B) A classe AnimalSelvagem amplia a estrutura de animal utilizando um super fazendo referência ao primeiro construtor da class Animal original, que é constructor(nome, especie, idade), ou seja, contém nome, espécie e idade de determinado animal. No novo constructor da class AnimalSelvagem, além de usar um extends para estender a classe Animal, é implementado um novo constructor que adiciona o atributo de habitat.

2. Herança

C) A linha class AnimalSelvagem extends Animal é uma extensão da class Animal, ou seja, reutiliza parte da primeira estrutura mas com um complemento.
D) Quando utilizamos o comando super dentro do constructor de uma subclasse, estamos destacando o constructor da primeira classe (class Animal), ou seja, estamos tornando o constructor original superior aos demais em nível de importância, tornando possível seu reaproveitamento no código.

3. Instanciação

E) O que ocorre ao executar o comando new AnimalSelvagem("Nala",
"Leoa", 5, "Savana Africana”) é a adição dos atributos da const animal2, em que os atributos de animal2 são informados (nome, espécie, idade e habitat) de uma novo animal.

F) A diferença entre a criação dos objetos animal1 e animal2 é que na segunda é adicionado o atributo habitat,  fazendo então o uso do novo atributo this.habitat = habitat; adicionado ao super(nome, especie, idade); .

4.  Acesso a Métodos

G) O método exibirInformacoes() pode ser utilizado tanto em animal1 quanto em animal2 porque ele se refere às const.
H) O método exibirHabitat() não está disponível em animal1 pois ele não é um atributo da class Animal e o animal1 pertence à ela.

5. Reutilização de Código

I) Nesse exemplo, a herança contribui pois, ao implementá-la, não é necessário reescrever os métodos e atributos que são reutilizados.
J) Ele deveria ser implementado na classe Animal, que é a classe que serve de base para as demais subclasses.

6. Retorno e Impressão

K) A saída exata é: Tico Macaco 4 Nala Leoa 5 Savana Africana

L) O código não rodaria, pois uma extension sem o super da class Animal não funciona.

7. 
