# Algoritmos-e-Estrutura-de-Dados
1. O que é estrutura de dados?
Estrutura de dados é uma maneira de organizar, gerenciar e armazenar dados de modo a permitir o acesso eficiente e a manipulação eficaz desses dados, é um conjunto de formatos e regras que define como os dados são organizados e como diferentes operações podem ser realizadas neles.

2.Qual sua importância?
A estrutura de dados é importante para otimizar o tempo de execução e o uso de memória para operações comuns, como inserção, busca, remoção e atualização de dados, além de organizar os dados de uma forma que faça sentido para a aplicação em questão.

3.Explique e exemplifique as estruturas
**Array**
*Um array é uma estrutura de dados que permite armazenar uma coleção de elementos do mesmo tipo sob um único nome, são definidos como estáticos e dinâmicos.
*Quando utilizar: 
-Quando você precisa de acesso rápido aos elementos por índice. 
-Quando o tamanho da coleção é conhecido e fixo antecipadamente. 
-Quando a ordem dos elementos é importante. 

**Array Estático:**
-Definimos a quantidade máxima de registros permitidos na criação do array.
Exemplo:

public class Exemplo {
        int numeros[] = new int[5]; //array definido com capacidade máxima de 5 registros
}

**Array Dinâmico:**
-Podemos aumentar a capacidade máxima dinâmicamente utilizando métodos.
Exemplo:

public class Exemplo {
        int numeros[]; 
    public Exemplo(){ //metodo para definir a capacidade do array
        this.numeros = new int[5];
    }
}

==================================================================
**Lista**
*Define um contrato para uma lista ordenada de elementos, onde cada elemento tem um índice associado. Através do índice, podemos selecionar um registro em alguma posição da lista, além de removermos e alterarmos os registros.
*Quando Utilizar: 
-Quando você precisa de uma coleção ordenada de elementos e não se preocupa com o tempo de acesso por índice. 
-Quando precisa adicionar e remover elementos com frequência. 
-Quando a ordem dos elementos é importante, mas o acesso por índice não é crítico. 

**ArrayList**
-Implementa a interface List e fornece uma implementação de um vetor dinâmico, ou seja, um array que pode crescer e diminuir de tamanho dinamicamente conforme necessário.
Exemplo:
public class Exemplo {
public static void main(String[] args) {
    List<String> nomes = new ArrayList<String>();
    nomes.add("nome1");
    nomes.add("nome2");
    System.out.println(nomes.get(1)); //seleção de registro por índice
    System.out.println("Nomes: " + nomes);
}
}

==================================================================
**Fila***
*O padrão fila ou queue é uma estrutura de dados que segue o princípio "primeiro a entrar, primeiro a sair", ou seja, o primeiro elemento inserido na fila será o primeiro a ser removido, uma Queue não permite elementos duplicados.
*Quando Utilizar: 
-Quando você precisa processar itens na ordem em que foram adicionados. 
-Quando há uma necessidade de controle de recursos compartilhados. 
-Para agendar tarefas em um sistema de computação distribuído. 
Exemplo:
public class Exemplo {
public static void main(String[] args) {
    Queue<String> nomes = new LinkedList<String>();
    nomes.add("nome1");
    nomes.add("nome2");
    nomes.add("nome3");
    System.out.println("Fila inicial: " + nomes);
    String removido = nomes.remove();
    System.out.println(removido); //primeiro elemento adicionado foi removido
    System.out.println("Nova fila: " + nomes);
}
}

==================================================================
**Pilha**
*O padrão de pilha (Stack) em programação segue o princípio "último a entrar, primeiro a sair", ou seja, o último elemento adicionado à pilha será o primeiro a ser removido, é comumente utilizado em programação para realizar operações como desfazer ações, rastreamento de chamadas de função, análise de expressões matemáticas e muito mais.
*Quando Utilizar: 
-Quando você precisa processar itens em ordem reversa (LIFO - Last-In-First-Out). 
-Quando precisa rastrear chamadas de funções em um programa. 
-Para desfazer ações em um aplicativo (undo). 
Exemplo:
public class Exemplo {
public static void main(String[] args) {
    Stack<String> nomes = new Stack<String>();
    nomes.push("Nome1");
    nomes.push("Nome2");
    nomes.push("Nome3");
    System.out.println("Topo da pilha: " + nomes.peek());
    String removido = nomes.pop(); //ultimo elemento adicionado foi removido
    System.out.println("Elemento removido: " + removido);
    System.out.println("Nova pilha: "+ nomes);
}
}
