
# variaveis variaveis 

$bebida = "refrigerante";

$$bebida = "cerveja";

agora existe uma variavel $refigerante que seu valor é cerveja;

***************************************************************************

# tipos de daddos 

escalares:

- string
- int
- float 

compostos:

- array
  $carros = array("gol", "Uno", "camaro");
 
- objeto

  class cliente{
    public $nome;
    
    public function atribuirNome($nome){
      $this->nome = "nome";
    }
  }
  
  $c = new Cliente();
  
  - especiais
    NULL
  
***************************************************


# aspas e concatenação 
  - aspas simples são literais
      echo 'meu nome é $nome'; saida -->  meu nome é $nome
      para concatenar usar o ponto 
  - aspas duplas são interpretativas:
      echo 'meu nome é $nome'; saida -->  meu nome é wislla
      
      
*******************************************************************

#Escopo de variavéis
   - escopo global:
   
    ```
      $nome = "wislla";
      function exibeNome(){
        $global $nome;

      }

      function atribuiNome(){
        $global $nome;
        $nome = "wislla";
      }
      echo $nome;

      function soma(){
        echo $GLOBALS['a'] + $GLOBALS['b'] +$GLOBALS['c'];
      }
    
    ```
  
  
 *********************************************************************
  
  
  #constantes
  define("NOME", "wislla");
  define("NOMES", ["wislla", "Amelie"]);
  
  
 *********************************************************************
  
  #Arrays
  
    $carros = array("Fusca", "Gol", "Palio");
  
    carros[] = "Amarok"; //inserindo item no array
    $carros[10] = "Camaro"; //inserindo item e especificando o seu indice
    print_r($carros); //imprimindo array
    echo "<br>";
    echo $carros[0]; //imprimindo conteudo do array
    echo "<hr>";

    $motos = array(); //outra forma de criar array
    $motos[] = "Honda"; //inserindo item no array
    $motos[] = "Yamaha"; //inserindo item no array
    $motos[5] = "Suzuki"; //inserindo item e especificando o seu indice
    print_r($motos); //imprimindo array
    echo "<hr>";

    $clientes = ["Rodrigo", "Felipe", "Geraldo"];
    print_r($clientes);
    echo "<hr>";

    //count
    $totalClientes = count($clientes);
    echo $totalClientes;
    echo "<hr>";

    //Foreach
    foreach($clientes as $valor){
        echo $valor."<br>";
    }
    echo "<hr>";

    //Arrays associativos
    $pessoa = array("nome"=> "Felipe", "idade"=> 27, "altura"=> 1.75);
    $pessoa["cidade"] = "Pirapora";
    echo $pessoa["cidade"];
    echo "<hr>";

    foreach($pessoa as $i => $valor){
        echo $i .":". $valor."<br>";
    }
    echo "<hr>";

    //Array Multidimencional
    $times = array(
                    "cariocas"=> array("campeao"=>"vasco", "vice"=>"flamengo", "terceiro"=>"fluminense"),
                    "paulistas"=> array("santos", "palmeiras", "sao paulo"),
                    "mineiros"=> array("cruzeiro", "atletico")
                );
    foreach($times["cariocas"] as $i => $valor){
        echo $i.":".$valor."<br>";
    }


/*
 * is_array($array) = verificar se uma determinada variável é um array
 * in_array($valor, $array) = verifica se um determinado valor existe em alguma posição
 * array_keys($array) = retorna um novo array com as chaves do array passado como parametro
 * array_values($array) = retorna um novo array com os valores do array passado como parametro
 * array_merge($array1, $array2) = agrega o conteúdo dos dois arrays
 * array_pop($array) = exclui a última posição do array
 * array_shift($array) = exclui a primeira posição do array
 * array_unshift($array, "valor") = adiciona um ou mais elementos no inicio do array
 * array_push($array, "valor", "valor") = adiciona um ou mais elementos no final do array
 * array_combine($keys, $values) = mescla os dois arrays passados
 * array_sum() = calcula a soma dos elementos de um array
 * explode("/", "20/01/2001") = transforma string em um array
 * implode("-", $array) = transforma array em string
 */

$nomes = array("Eu" => "Felipe", "Namorada" => "Bruna", "Mãe" => "Marisa", "Irma" => "Fernanda");

//verifica se é um array
if (is_array($nomes)):
    echo "é um array";
else:
    echo "não é um array";
endif;
echo "<hr>";

//verifica se o conteudo existe no array
if (in_array("Felipe", $nomes)):
    echo "Nome encontrado";
else:
    echo "Nome não encontrado";
endif;
echo "<hr>";

//retorna o indice dos arrays
$keys = array_keys($nomes);
print_r($keys);
echo "<hr>";

//retorna os valores do array
$values = array_values($nomes);
print_r($values);
echo "<hr>";

$carros = array("Camaro", "Uno", "Gol");
$motos = array("Honda", "Yamaha", "Suzuki");

//Mescla dois arrays
$veiculos = array_merge($carros, $motos);
print_r($veiculos);
echo "<hr>";

//deleta o ultimo conteudo do array
print_r($veiculos);
echo "<br>";
echo array_pop($veiculos);
echo "<br>";
print_r($veiculos);
echo "<hr>";

//deleta o primeiro conteudo do array
print_r($veiculos);
echo "<br>";
echo array_shift($veiculos);
echo "<br>";
print_r($veiculos);
echo "<hr>";

$frutas = array("Uva", "Laranja", "Maçã");
print_r($frutas);
//insere itens no inicio do array
array_unshift($frutas, "Manga", "Acerola", "Morango");
echo "<br>";
print_r($frutas);
echo "<hr>";

//insere itens no final do array
array_push($frutas, "Melancia");
print_r($frutas);
echo "<hr>";

//combinação de array
$id = array("Campeão", "Vice", "Terceiro");
$values = array("Cruzeiro", "Atletico", "America");

$times = array_combine($id, $values);
print_r($times);
echo "<hr>";

//soma do conteudo do array
$soma = array(10, 35, 18);
$total = array_sum($soma);
echo $total;
echo "<hr>";

//explode, transforma uma string em arrays
$data = "16/12/2020";
$novaData = explode("/", $data);
print_r($novaData);
echo "<hr>";

//implode, transforma um array em strings
$meses = array("Janeiro", "Fevereiro", "Março");
$str = implode(", ", $meses);
print_r($str);



  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
    
