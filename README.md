# Aprendendo-Java
<p style="text-align: justify;">
Java é uma linguagem de programação orientada a objetos desenvolvida na década de 90 por uma equipe de programadores chefiada por James Gosling, na empresa Sun Microsystems, que em 2008 foi adquirido pela empresa Oracle Corporation. Diferente das linguagens de programação modernas, que são compiladas para código nativo, Java é compilada para um bytecode que é interpretado por uma máquina virtual (Java Virtual Machine, abreviada JVM). A linguagem de programação Java é a linguagem convencional da Plataforma Java, mas não é a sua única linguagem. A J2ME é utilizada em jogos de computador, celular, calculadoras, ou até mesmo o rádio do carro. <a href="https://blog.formacao.dev/terminal-no-macos-linux/">Referência do texto.</a>
</p>

## Criação do primeiro programa em Java
Em Java, é uma convenção de nomenclatura (não uma regra obrigatória do compilador) que os nomes de arquivos/classes comecem com uma letra maiúscula. Essa convenção vem das práticas de programação orientada a objetos e ajuda a manter o código legível e organizado. As convenções de nomenclatura ajudam a distinguir facilmente entre tipos (classes, interfaces) e membros (variáveis, métodos). Isso torna o código mais fácil de ler e manter. Embora essas convenções não sejam tecnicamente obrigatórias, segui-las é considerado uma boa prática de programação.

### Convenções de Nomenclatura em Java

1. **Nomes de Classes**:
   - **Devem começar com uma letra maiúscula** e usar CamelCase. 
   - Exemplo: `MyClass`, `HelloWorld`.

2. **Nomes de Métodos e Variáveis**:
   - **Devem começar com uma letra minúscula** e também usar CamelCase.
   - Exemplo: `calculateSum`, `myVariable`.

3. **Nomes de Constantes**:
   - **Devem ser totalmente em maiúsculas** com palavras separadas por underscores.
   - Exemplo: `MAX_VALUE`, `PI`.

```
   public class PrimeiroPrograma {

      public static void main(String[] args) {
         System.out.println("Hello, word!!!");
      }
   }

```

Para executar um arquivo java pelo terminal primeiro é necessário fazer a compilação do arquivo com o comando: `javac PrimeiroPrograma.java`

Em seguida executar com:
`java PrimeiroPrograma`

## Comentários
No Java, os comentários são utilizados para adicionar explicações ou anotações no código, que não são executadas pelo compilador. Existem duas formas principais de fazer comentários em Java:

1. **Comentário de uma linha**: Utiliza `//` para comentar uma única linha.
2. **Comentário de múltiplas linhas**: Utiliza `/* */` para comentar várias linhas.

Aqui está um exemplo ilustrativo de como usar ambos os tipos de comentários:

```
public class PrimeiroPrograma {

      public static void main(String[] args) {
         // Comentário de uma linha

         /*
         Comentário de várias linhas
         System.out.println("Hello, word!!!");
         System.out.println("Hello, word!!!");
         System.out.println("Hello, word!!!");
         */

         System.out.println("Hello, word!!!");
      }
   }
```
## Variáveis
Java possui dois tipos de dados que são divididos em tipos primitivos e tipos por referência.


**Tipos primitivos** <br>
Em Java, os tipos de dados primitivos são os tipos de dados mais básicos que não são objetos. Eles são usados para armazenar valores simples e possuem tamanhos fixos. Existem oito tipos primitivos em Java:

1. **byte**:
   - Tamanho: 8 bits
   - Valor mínimo: -128
   - Valor máximo: 127
   - Uso: Ideal para economizar memória em grandes arrays.

   ```java
   byte b = 100;
   ```

2. **short**:
   - Tamanho: 16 bits
   - Valor mínimo: -32.768
   - Valor máximo: 32.767
   - Uso: Economiza memória em grandes arrays, melhor que `byte` quando valores maiores são necessários.

   ```java
   short s = 10000;
   ```

3. **int**:
   - Tamanho: 32 bits
   - Valor mínimo: -2^31
   - Valor máximo: 2^31 - 1
   - Uso: O tipo numérico inteiro mais comum.

   ```java
   int i = 100000;
   ```

4. **long**:
   - Tamanho: 64 bits
   - Valor mínimo: -2^63
   - Valor máximo: 2^63 - 1
   - Uso: Usado quando um intervalo maior que `int` é necessário.

   ```java
   long l = 100000L;
   ```

5. **float**:
   - Tamanho: 32 bits
   - Valor mínimo: Aproximadamente 1.4E-45
   - Valor máximo: Aproximadamente 3.4E+38
   - Uso: Usado para valores de ponto flutuante precisos.

   ```java
   float f = 10.5f;
   ```

6. **double**:
   - Tamanho: 64 bits
   - Valor mínimo: Aproximadamente 4.9E-324
   - Valor máximo: Aproximadamente 1.7E+308
   - Uso: O tipo numérico de ponto flutuante mais comum.

   ```java
   double d = 10.5;
   ```

7. **char**:
   - Tamanho: 16 bits
   - Valor mínimo: '\u0000' (ou 0)
   - Valor máximo: '\uffff' (ou 65.535)
   - Uso: Armazena um único caractere Unicode.

   ```java
   char c = 'A';
   ```

8. **boolean**:
   - Tamanho: 1 bit (a especificação não define o tamanho exato)
   - Valores possíveis: `true` e `false`
   - Uso: Armazena valores booleanos.

   ```java
   boolean flag = true;
   ```

**Tipos por referência**

Os tipos de referência são usados para armazenar referências a objetos em vez dos próprios valores. Eles são mais complexos e flexíveis que os tipos primitivos. Aqui estão os principais tipos de referência em Java:

**Exemplos de tipos de referência:**

1. **Classes**
   - Classes são os principais tipos de referência em Java. Uma classe define a estrutura e o comportamento de objetos.
   - Exemplo:
     ```java
     public class Person {
         String name;
         int age;

         Person(String name, int age) {
             this.name = name;
             this.age = age;
         }
     }
     ```

2. **Interfaces**
   - Interfaces definem um contrato que outras classes devem seguir. Elas não podem conter implementação de métodos (até o Java 8, que introduziu métodos `default`).
   - Exemplo:
     ```java
     public interface Animal {
         void makeSound();
     }
     ```

3. **Arrays**
   - Arrays são tipos de referência que armazenam múltiplos valores do mesmo tipo.
   - Exemplo:
     ```java
     int[] numbers = {1, 2, 3, 4, 5};
     ```

4. **Enumerations (Enums)**
   - Enums são tipos de referência que definem um conjunto fixo de constantes.
   - Exemplo:
     ```java
     public enum Day {
         SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY
     }
     ```

5. **Strings**
   - Strings são objetos que representam sequências de caracteres. Elas são imutáveis, o que significa que uma vez criada, a sequência de caracteres não pode ser alterada.
   - Exemplo:
     ```java
     String greeting = "Hello, World!";
     ```
6. **Referências dos tipos primitivos**

Em Java existem tipos de referência correspondentes aos tipos primitivos, chamados de classes wrapper. As classes wrapper permitem tratar os tipos primitivos como objetos, o que é útil em diversas situações, como ao trabalhar com coleções do framework `java.util`, que só podem armazenar objetos. Aqui estão os tipos primitivos e suas correspondentes classes wrapper:

| Tipo Primitivo | Classe Wrapper |
|----------------|----------------|
| `byte`         | `Byte`         |
| `short`        | `Short`        |
| `int`          | `Integer`      |
| `long`         | `Long`         |
| `float`        | `Float`        |
| `double`       | `Double`       |
| `char`         | `Character`    |
| `boolean`      | `Boolean`      |

**Diferenças entre Tipos Primitivos e Tipos de Referência**

1. **Armazenamento**:
   - **Tipos Primitivos**: Armazenam valores reais e são alocados na stack.
   - **Tipos de Referência**: Armazenam referências (endereços) a objetos reais que são alocados na heap.

2. **Operações**:
   - **Tipos Primitivos**: Operações são executadas diretamente sobre os valores.
   - **Tipos de Referência**: Operações são executadas chamando métodos dos objetos referenciados.

3. **Valor Padrão**:
   - **Tipos Primitivos**: Têm valores padrão específicos (`0` para numéricos, `false` para booleanos, `\u0000` para char).
   - **Tipos de Referência**: Têm o valor padrão `null`.

4. **Imutabilidade**:
   - **Tipos Primitivos**: Os valores são imutáveis.
   - **Tipos de Referência**: Podem ser mutáveis ou imutáveis, dependendo da implementação da classe (por exemplo, `String` é imutável, mas `StringBuilder` é mutável).

   Obs: Quando dizemos que variáveis de tipos primitivos são "imutáveis", o que realmente queremos dizer é que, quando você atribui um valor a uma variável de tipo primitivo, esse valor é armazenado diretamente na variável, e qualquer modificação na variável altera o valor diretamente. No entanto, isso não significa que a variável em si não possa ser modificada, mas sim que o valor armazenado na variável é diretamente alterado e não há referências indiretas ou mutações em locais de memória diferentes.


## Package (Pacote) e Import (Importação)
Em Java, um pacote (package) é um mecanismo que agrupa classes e interfaces relacionadas. Pacotes são usados para organizar o código de maneira modular e hierárquica, evitando conflitos de nomes e facilitando a manutenção e reutilização do código.

**Benefícios de Usar Pacotes**

1. **Organização**: Pacotes ajudam a organizar classes e interfaces em namespaces relacionados, tornando o projeto mais fácil de navegar e gerenciar.
2. **Evitar Conflitos de Nome**: Pacotes evitam conflitos de nome, permitindo que diferentes desenvolvedores trabalhem em classes com os mesmos nomes sem colisões.
3. **Controle de Acesso**: Pacotes fornecem um mecanismo para controle de acesso, permitindo especificar quais classes e membros são acessíveis fora do pacote.
4. **Modularidade**: Pacotes facilitam a modularização do código, permitindo a separação de funcionalidades em componentes distintos.

**Declaração de um Pacote**

Para declarar que uma classe pertence a um pacote, usa-se a palavra-chave `package` no início do arquivo Java, seguida pelo nome do pacote. O nome do pacote deve corresponder à estrutura de diretórios onde o arquivo está localizado.

**Exemplo** 

1. Estrutura de Diretórios:
    ```plaintext
    src/
     ├── com/
     │    ├── mycompany/
     │    │    ├── myapp/
     │    │    │    ├── Main.java
     │    │    │    └── utils/
     │    │    │         ├── MathUtils.java
     │    │    │         └── StringUtils.java
    ```

2. `Main.java`:
    ```java
    package com.mycompany.myapp;

    import com.mycompany.myapp.utils.MathUtils;
    import com.mycompany.myapp.utils.StringUtils;

    public class Main {
        public static void main(String[] args) {
            int sum = MathUtils.add(5, 10);
            String reversed = StringUtils.reverse("Hello");

            System.out.println("Sum: " + sum);
            System.out.println("Reversed: " + reversed);
        }
    }
    ```

3. `MathUtils.java`:
    ```java
    package com.mycompany.myapp.utils;

    public class MathUtils {
        public static int add(int a, int b) {
            return a + b;
        }
    }
    ```

4. `StringUtils.java`:
    ```java
    package com.mycompany.myapp.utils;

    public class StringUtils {
        public static String reverse(String str) {
            return new StringBuilder(str).reverse().toString();
        }
    }
    ```

**Pacotes Java Padrão**

Java possui muitos pacotes padrão que fornecem diversas funcionalidades. Alguns dos mais comuns incluem:

1. **java.lang**: Inclui classes fundamentais como `String`, `Math`, `Integer`, `System`, etc. Este pacote é importado automaticamente.
2. **java.util**: Inclui classes utilitárias como `ArrayList`, `HashMap`, `Date`, `Calendar`, etc.
3. **java.io**: Inclui classes para entrada e saída, como `File`, `InputStream`, `OutputStream`, etc.
4. **java.nio**: Inclui classes para entrada e saída de alta performance e operações de buffer.
5. **java.net**: Inclui classes para operações de rede, como `Socket`, `ServerSocket`, `URL`, etc.

**Importação de Pacotes**

Para usar classes de um pacote diferente, você precisa importá-las usando a palavra-chave `import`.

**Importação Específica**

```java
import java.util.ArrayList;

public class ImportExample {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
    }
}
```

**Importação de Pacote Inteiro**

```java
import java.util.*;

public class ImportExample {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        HashMap<String, Integer> map = new HashMap<>();
    }
}
```

**Controle de Acesso com Pacotes**

Java permite controlar a visibilidade de classes e membros de classes (métodos, variáveis) usando modificadores de acesso:

1. **public**: A classe ou membro é acessível de qualquer outro pacote.
2. **protected**: O membro é acessível dentro do mesmo pacote e por subclasses.
3. **default (sem modificador)**: O membro é acessível apenas dentro do mesmo pacote.
4. **private**: O membro é acessível apenas dentro da mesma classe.

**Exemplo de Controle de Acesso**

```java
package com.mycompany.myapp;

public class MyClass {
    public int publicVar;
    protected int protectedVar;
    int defaultVar; // Acesso de pacote
    private int privateVar;
}
```
##






