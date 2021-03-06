# :elephant: Curso de PHP!
 
<img src="./assets/logo.png" width="100%">

:thinking: Atualmente comecei a estudar a linguagem PHP, e percebi que é muito fácil de aprender, uma simples linguagem que era utilizada para template, agora virou uma das linguagens mais usadas na internet. Comecei a ver a Playlist do [Curso em Vídeo](https://www.youtube.com/channel/UCrWvhVmt0Qac3HgsjQK62FQ).

## :tv: Dia `15/07/2021`:

Aprendi sobre a definição de variáveis, como envia-las para o corpo de website, concatenar uma variável com uma frase e os tipos de variáreis. O PHP já realiza a tipagem das variáveis de forma geral, mais caso você queira forçar essa tipagem, você pode ver os exemplos abaixo:

```php
<?php
    $NomeDaVariavel = valor;

    // Exemplo

    $nome = "Tiago";
    $idade = 15;
    
    // Tipagem de variáveis
    // Após o sinal de =, você poderá abrir um () e definir o tipo da variável, como string se for uma String ou int se for um valor numérico.

    $nome1 = (string) "Tiago";
    $idade1 = (int) 15;
    
    // Enviar as variáveis para o corpo do site

    echo $nome;

    // Dois meios de concatenação

    // Podemos fazer a concatenação das variáveis usando o . para realizar a separação de uma variável com uma String no PHP
    echo $nome. " tem ". $idade " anos!"; 

    // Para meios mais simples, podemos usar as "" duplas para enviar as variáveis sem precisar usar os .

    echo "$nome tem $idade anos!";

    // Lembrando que '' não conseguem enviar variáveis em uma String!
?>
``` 

## :tv: Dia `16/07/2021`:

Nesse dia eu aprendi sobre as funções aritméticas no PHP, que foi algo muito simples:
- Somar: `+`
- Subtrair: `-`
- Multiplicar: `*`
- Dividir: `/`
- Modulo: `%`

Aprendi a como fazer a busca de dados dentro de uma **Query** na **URL**:
```php
<?php
    $numero1 = $_GET["Numero1"];
    $numero2 = $_GET["Numero2"];
    $resultado = $numero1 + $numero2;

    // http://localhost/curso-php/aula5.php?Numero1=10%Numero2=10

    echo "<h1>Resultado é $resultado</h1>";
?>
```

E as funções matemáticas, onde possui meios de pegar valores absolutos, potenciação, aiz quadrada, arredondamento, buscar a parte inteira de um valor real e realizar a formatação de um valor numérico!
```php
<?php
    $absoluto = abs($numero1);
    $potenciacao = pow($numero1, $numero2);
    $raiz = sqrt($numero1);
    $arredondamento = round($numero1); // ceil ou floor

    $inteira = intval($numero1);
    $formatarMoney = number_format($numero1, 2, ",", ".");
?>
```

## :tv: Dia `17/07/2021`:

Nessa aula foi meio chato, pois aprendi apenas os operadores de atribuição, referência de variáveis e variáveis de variáveis. é bem difícil de entender mais irei pegar o jeito.

```php
<?php
    // Atribuição de Variáveis

    $valor = 10;
    $valor = $valor + 10; // Redefine o valor para o Valor + 10
    $valor += 10; // Adiciona + 10
    $valor++; // Adiciona 1

    // Referência de Variáveis

    $a = 10;
    $b = &$a; // Faz referência a a
    $c = $b + 10;

    // Variáveis de Variáveis

    $site = "cursoemvideo";
    $$site = "cursophp";

    echo "$site tem $cursoemvideo"; // Cria uma variável com o nome do valor da primeira variável                                             
?>
```

## :tv: Dia `18/07/2021`:
Aprendi sobre operadores no PHP, aprendi rápido pois a syntax é muito parecida com javascript.

```php
<?php
    $a > $b; // a maior que b
    $a < $b; // a menor que b
    $a >= $b; // a maior ou igual a b
    $a <= $b; // a menor ou igual a b
    $a == $b; // a igual b
    $a === $b; // a com tipo e valor igual a b
?>
```

## :tv: Dia `01/09/2021`:

Depois de muito tempo eu voltei e já assisti mais uma aula do curso de PHP, onde aprendi a enviar dados de um formulário para um arquivo PHP.

Onde você pode criar um formulário e redireciona-se os dados para um arquivo PHP. Onde você pode usar os métodos `$_GET` para requisições GET e `$_POST` para requisições POST.

E por fim, aprendi um pouco sobre condições no PHP, onde usamos o `isset` para verificar se um valor enviado em uma Query da URL está setada.

```php
<?php
    $valor = isset($_GET["v"]) ? $_GET["v"] : "nenhum valor setado";

    echo $valor;
?>
```

# :tv: Dia `02/09/2021`:

Hoje eu aprendi sobre os Operadores Condicionais, os famosos `IF`, `ELSE` e `ELSEIF`. Que é relativamente igual ao JavaScript.

```php
<?php
    if (1 > 2) {
        echo "1 é maior que 2";
    } else {
        echo "2 é maior que 1";
    };

    // imprime 2 é maior que 1
?>
```

# :tv: Dia `03/09/2021`:

Nesse dia foi bem interessante, pois aprendi sobre os `Switch` e `Case`, que também é idêntico a syntax do JavaScript.


```php
<?php
    $tipo = 1;

    switch ($tipo) {
        case 1:
            echo "O tipo é 1";
            break;
        case 2:
            echo "O tipo é 2";
            break;
        default: 
            echo "O tipo é diferente de 1 e 2";
            break; 
    }
?>
```

# :tv: Dia `04/09/2021`:

Hoje aprendi sobre estruturas de repetição no PHP, `While` onde eu posso realizar uma ação várias vezes. E a estrutura inversa do `While`, o `Do`.

```php
<?php
    $n = 10;

    while ($n >= 0) {
        echo "$n <br>";
        $n-=2;
    }
?>
```

```php
<?php
    $c = 1;

    do {
        echo $c;
        $c++;
    } while ($c < 10);
?>
```

# :tv: Dia `05/09/2021`:

Para finalizar a parte de estrutura de repetições, aprendi sobre o `For` onde é uma opção mais fácil para realizar a repetição.

```php
<?php
    for ($c = 0; $c < 10; $c++) {
        echo "Contagem: $c";
    }
?>
```

# :tv: Dia `06/09/2021`:

Nessa aula estudei sobre Rotinas ou Funções no PHP, onde existe tipo de funções que retornam valores ou não retornam nada.

```php
<?
    function naoRetorna ($a, $b) {
        echo $a + $b;
    };

    naoRetorna(1, 2); // Imprime 3

    function soma ($a, $b) {
        $r = $a  $b;

        return $r;
    };

    $resultado = soma(10, 10);

    echo $resultado; // Imprime 20

    // FUNÇÕES NATIVAS DO PHP

    func_get_args(); // Retorna um Array com todos os argumentos da função
    func_num_args(); // Retorna a quantidade de argumentos da função
?>
```

# :tv: Dia `07/09/2021`:

Hoje aprendi sobre redefinição de variáveis em funções, inclusão e requisição de arquivos no PHP.
```php
<?php
    function naoMuda ($a) {
        $a = $a + 5;
        echo $a;
    };

    $valor = 10;
    naoMuda($valor); // imprime 15
    echo $valor; // imprime 10

    function muda (&$a) {
        $a = $a + 5;
        echo $a;
    }; // O & faz referência á variável que será passada na função

    $valor2 = 10;
    muda($valor2); // imprime 15
    echo $valor2; // imprime 15
?>
```
Diferença entre o `INCLUDE` e `REQUIRE`:
```php
// ARQUIVO functions.php
<?php
    function somar ($a, $b) {
        $x = $a + $b;
        echo $x;
    }
?>

// ARQUIVO index.php
<?php
    include "functions.php"; // Caso ocorra um erro no arquivo, o PHP não continuar o processo
    require "functions.php"; // Caso tenha um erro no arquivo, o PHP para a execução do script

    somar(1, 4);
?>
```

# :tv: Dia `08/09/2021`:

Hoje eu aprendi sobre `String Functions` ou **Funções String**, onde elas manipulam uma String no PHP. Existem várias, mais nesse dia aprendi algumas bem interessantes;

`printF("Texto %tipo", $variável)` - Faz uma substituição de uma caracteres que começa com o `%` e seu tipo por uma variável.
> Á vários tipos para usar, como d(Decimal), u(Decimal sem Sinal), f(Numero Real), s(String) e Etc.

`print_r($variável)` - Mostra o tipo da variável.
> também tem o `var_dump` e `var_export` que são variações dessa função.

`wordwrap($texto, Numero de Letras para a Quebra, Quebra Visual, Pode quebrar uma palavra)` - Faz a quebra de uma String.

`strlen($texto)` - Mostra a quantidade de caracteres de uma String.

`trim($texto)` - Remove os espaços repetidos de uma String.
> Também existe o `ltrim` para remover apenas espaços da esquerda (Left) e `rtrim` para remover espaços da direita (right).

`str_word_count($frase, $tipo)` - Contar ou Gerar vetores de uma String.
> 0 => Contar as palavras
> 1 => Gerar um Vetor
> 2 => Gerar um Vetor com o posicionamento das palavras

`str_split($texto)` - Separar cada letra de uma String.

`join($texto, "Conteúdo entre cada Array")` - Juntar cada letra ou palavra de um vetor

# :tv: Dia `09/09/2021`:

Mais 12 Funções Strings:

`strtolower($frase)` - Deixa tudo em Minúsculo;

`strtoupper($frase)` - Deixa tudo Maiúsculo;

`ucfirst($nome)` - Deixa a primeira letra da fase em Maiúscula;

`ucwords($nome)` - Deixa a primeira letra das palavras em Maiúsculas;

`strrev($nome)` - Reverte uma string;

`strpos($frase, "PHP")` - Posição da palavra;

`stripos($frase, "php")` - Posição da palavra mesmo sendo maiúsculas ou minúsculas;

`substr_count($frase, "PHP")` - Quantas vezes a string PHP foi encontrada na frase;

`substr($site, 0, 5)` - Corta uma frase do começo 0 até a 5 letra;

`str_pad($nome, 30, " ", STR_PAD_RIGHT)` - Adicionar conteúdo entre frases de direção esquerda, centro ou direita;

`str_repeat("Php", 5)` - Realizar a repetição de strings;

`str_replace("PHP", "php", $frase)` - Realizar a substituição de uma palavra em uma string;

# :tv: Dia `09/09/2021`:

Hoje é a penúltima aula do curso de php, e estudei a primeira parte de vetores e matrizes, onde no php não existe matrizes como no javascript. Mais é possível fazer uma espécie de matriz usando vetores:

```php
    <?php
    $n = array(0, 10, 10);
    $n[] = 15;
    print_r($n);

    echo "<br><br>";

    $c = range(5, 20, 5);
    print_r($c);

    echo "<br><br>";

    foreach ($c as $valor) {
        echo "$valor ";
    };

    echo "<br><br>";

    $v = array(
        "test" => "a", 
        3 => "b", 
        6 => "c", 
        8 => "d"
    );
    unset($v[1]);
    print_r($v["test"]);

    echo "<br><br>";

    $cad = array(
        "nome" => "tiago",
        "idade" => 16
    );

    foreach($cad as $campo => $valor) {
        echo "O campo $campo é $valor<br>";
    };

    $objeto = array(
        "nomes" => array("tiago", "pedro")
    );

    print_r($objeto);

?>
```

# :tv: Dia `10/09/2021`:

**ULTIMA AULA**, e aprendi mais algumas funções para a manipulação de um array!
```php
<?php
    $v = array(80, 160, 30);
    $v[] = 80; // adicionar um valor no final
    array_push($v, 90); // adicionar um novo valor no final
    array_pop($v); // remover o ultimo valor do final

    array_unshift($v, 40); // adiciona na primeira área do array
    array_shift($v); // remove o primeiro valor

    sort($v); // ordena os valores crescente
    rsort($v); // ordena os valores decrescente

    asort($v); // ordena os valores e indexes 
    arsort($v); // ordena os valores e indexes reverso

    ksort($v); // ordenar os valores pela chaves
    krsort($v); // ordenar os valores pela chave de forma reversa
        
    var_dump($v);
?>
```

# :heart: Agradecimentos:

Ao professor **Gustavo Guanabara** que fez esse curso grátis, onde aprendi a syntax da linguagem PHP, Obrigado! :heart: