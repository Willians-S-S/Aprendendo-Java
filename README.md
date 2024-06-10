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

```java
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

```java
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
## Entrada de dados pelo terminal
Em Java, a entrada de dados pelo terminal pode ser feita de várias maneiras, sendo a mais comum a utilização da classe `Scanner` da biblioteca `java.util`. Ela suporta a leitura de vários tipos de dados, tornando-a uma ferramenta poderosa para interações básicas com o usuário.. Abaixo estão exemplos de como utilizar a classe `Scanner` para ler diferentes tipos de dados do terminal.

### Importação da Classe Scanner

Primeiro, você precisa importar a classe `Scanner`:

```java
import java.util.Scanner;
```

### Exemplos de Leitura de Diferentes Tipos de Dados

#### 1. Leitura de uma String

```java
import java.util.Scanner;

public class ReadStringExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // Cria um objeto Scanner

        System.out.print("Enter a string: ");
        String input = scanner.nextLine(); // Lê uma linha completa de entrada

        System.out.println("You entered: " + input);
    }
}
```

#### 2. Leitura de um Inteiro

```java
import java.util.Scanner;

public class ReadIntExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // Cria um objeto Scanner

        System.out.print("Enter an integer: ");
        int number = scanner.nextInt(); // Lê um inteiro

        System.out.println("You entered: " + number);
    }
}
```

#### 3. Leitura de um Float

```java
import java.util.Scanner;

public class ReadFloatExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // Cria um objeto Scanner

        System.out.print("Enter a float: ");
        float number = scanner.nextFloat(); // Lê um número float

        System.out.println("You entered: " + number);
    }
}
```

#### 4. Leitura de um Double

```java
import java.util.Scanner;

public class ReadDoubleExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // Cria um objeto Scanner

        System.out.print("Enter a double: ");
        double number = scanner.nextDouble(); // Lê um número double

        System.out.println("You entered: " + number);
    }
}
```

#### 5. Leitura de um Caractere

```java
import java.util.Scanner;

public class ReadCharExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // Cria um objeto Scanner

        System.out.print("Enter a character: ");
        char character = scanner.next().charAt(0); // Lê o primeiro caractere de uma string

        System.out.println("You entered: " + character);
    }
}
```

#### 6. Leitura de um Boolean

```java
import java.util.Scanner;

public class ReadBooleanExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // Cria um objeto Scanner

        System.out.print("Enter a boolean: ");
        boolean bool = scanner.nextBoolean(); // Lê um valor booleano

        System.out.println("You entered: " + bool);
    }
}
```

### Tratamento de Erros

Ao usar a classe `Scanner`, é importante estar ciente de possíveis exceções que podem ser lançadas, como `InputMismatchException` se a entrada não for do tipo esperado. Aqui está um exemplo de como tratar essa exceção:

```java
import java.util.InputMismatchException;
import java.util.Scanner;

public class SafeReadIntExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // Cria um objeto Scanner

        System.out.print("Enter an integer: ");
        try {
            int number = scanner.nextInt(); // Lê um inteiro
            System.out.println("You entered: " + number);
        } catch (InputMismatchException e) {
            System.out.println("That's not a valid integer.");
        }
    }
}
```

### Encerrando o Scanner

Após terminar de usar o `Scanner`, é uma boa prática fechá-lo para liberar os recursos associados. Isso pode ser feito chamando o método `close()`:

```java
scanner.close();
```
No entanto, é preciso ter cuidado ao fechar o `Scanner` que lê da entrada padrão (`System.in`), pois fechá-lo também fecha a entrada padrão, o que pode causar problemas se precisar ler mais entradas posteriormente no programa.


## Saída de dados pelo terminal

Em Java, a saída de dados pelo terminal é feita principalmente usando a classe `System`, especificamente o objeto `System.out`, que é uma instância de `PrintStream`. Aqui estão algumas maneiras comuns de realizar a saída de dados pelo terminal em Java:

### Métodos Comuns de Saída

1. **System.out.print()**: Imprime texto no terminal sem uma nova linha no final.
2. **System.out.println()**: Imprime texto no terminal seguido por uma nova linha.
3. **System.out.printf()**: Imprime texto formatado no terminal.

### Exemplos Detalhados

#### 1. `System.out.print()`

O método `print()` imprime o texto sem adicionar uma nova linha no final. Se você usar múltiplas chamadas a `print()`, todas as saídas serão impressas na mesma linha.

```java
public class PrintExample {
    public static void main(String[] args) {
        System.out.print("Hello, ");
        System.out.print("World!");
        // Saída: Hello, World!
    }
}
```

#### 2. `System.out.println()`

O método `println()` imprime o texto seguido por uma nova linha. Cada chamada a `println()` resultará em uma nova linha no terminal.

```java
public class PrintlnExample {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
        System.out.println("Welcome to Java programming.");
        // Saída:
        // Hello, World!
        // Welcome to Java programming.
    }
}
```

#### 3. `System.out.printf()`

O método `printf()` permite a impressão de texto formatado. Ele é útil para criar saídas mais estruturadas e legíveis. Você pode usar especificadores de formato para controlar a apresentação dos dados.

```java
public class PrintfExample {
    public static void main(String[] args) {
        int age = 25;
        String name = "John";
        double salary = 12345.678;

        System.out.printf("Name: %s, Age: %d, Salary: %.2f%n", name, age, salary);
        // Saída: Name: John, Age: 25, Salary: 12345.68
    }
}
```

### Especificadores de Formato

Ao usar `printf()`, você pode utilizar vários especificadores de formato para controlar a formatação da saída:

- `%d` para inteiros
- `%s` para strings
- `%f` para números de ponto flutuante
- `%n ou \n` para nova linha (independente do sistema operacional)
- `%t` para data e hora

#### Exemplo com Diferentes Especificadores

```java
public class FormatExample {
    public static void main(String[] args) {
        int intValue = 123;
        double doubleValue = 45.6789;
        String stringValue = "Hello";

        System.out.printf("Integer: %d%n", intValue);
        System.out.printf("Double: %.2f%n", doubleValue);
        System.out.printf("String: %s%n", stringValue);
        // Saída:
        // Integer: 123
        // Double: 45.68
        // String: Hello
    }
}
```


Esses métodos cobrem as formas básicas de saída de dados pelo terminal em Java. Dependendo da necessidade, você pode usar `print()`, `println()`, ou `printf()` para produzir a saída desejada. Aqui está um resumo:

- Use `System.out.print()` para imprimir sem uma nova linha.
- Use `System.out.println()` para imprimir com uma nova linha.
- Use `System.out.printf()` para imprimir texto formatado.

### Exemplo Completo

Aqui está um exemplo completo que demonstra todas as formas de saída discutidas:

```java
public class OutputExample {
    public static void main(String[] args) {
        // Usando print
        System.out.print("Esta é uma linha sem nova linha.");
        System.out.print(" Continua na mesma linha.\n");

        // Usando println
        System.out.println("Esta é uma linha com nova linha.");
        System.out.println("Outra linha com nova linha.");

        // Usando printf
        int intValue = 42;
        double doubleValue = 3.14159;
        String stringValue = "Java";

        System.out.printf("Integer: %d%n", intValue);
        System.out.printf("Double: %.2f%n", doubleValue);
        System.out.printf("String: %s%n", stringValue);
    }
}
```

Saída:

```
Esta é uma linha sem nova linha. Continua na mesma linha.
Esta é uma linha com nova linha.
Outra linha com nova linha.
Integer: 42
Double: 3.14
String: Java
```

Esses métodos fornecem flexibilidade e controle sobre como você exibe dados no terminal em Java.



## String

Em Java, String é uma classe imutável usada para representar uma sequência de caracteres. A classe String está localizada no pacote java.lang e, por isso, é automaticamente importada em todos os programas Java. Strings são amplamente utilizadas em programas para armazenar e manipular texto.

### Características das Strings

1. **Imutabilidade**: Uma vez que um objeto `String` é criado, seu valor não pode ser alterado. Operações que parecem modificar uma `String` na verdade criam um novo objeto `String`.
2. **Pool de Strings**: Java mantém um pool de strings para reutilização de objetos `String` imutáveis. Isso ajuda a economizar memória e melhora a performance.
3. **Suporte a Unicode**: `String` em Java suporta caracteres Unicode, permitindo representar uma ampla gama de caracteres de diferentes idiomas e símbolos.

### Criação de Strings

Existem várias formas de criar strings em Java:

1. **Literais de Strings**:
   ```java
   String str1 = "Hello, World!";
   ```

2. **Usando o operador `new`**:
   ```java
   String str2 = new String("Hello, World!");
   ```

3. **Convertendo Arrays de Caracteres**:
   ```java
   char[] charArray = {'H', 'e', 'l', 'l', 'o'};
   String str3 = new String(charArray);
   ```
### Métodos da classe String
Abaixo estão os exemplos de métodos da classe `String` em Java, com descrição, tipo de retorno e exemplo de retorno:


### 1. `charAt(int index)`
**Descrição**: Retorna o caractere no índice especificado.
**Tipo de Retorno**: `char`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello";
        char ch = str.charAt(1);
        System.out.println("charAt: " + ch); // Outputs: e
    }
}
```

### 2. `codePointAt(int index)`
**Descrição**: Retorna o valor Unicode do caractere no índice especificado.
**Tipo de Retorno**: `int`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello";
        int codePoint = str.codePointAt(1);
        System.out.println("codePointAt: " + codePoint); // Outputs: 101
    }
}
```

### 3. `codePointBefore(int index)`
**Descrição**: Retorna o valor Unicode do caractere antes do índice especificado.
**Tipo de Retorno**: `int`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello";
        int codePoint = str.codePointBefore(1);
        System.out.println("codePointBefore: " + codePoint); // Outputs: 72
    }
}
```

### 4. `codePointCount(int beginIndex, int endIndex)`
**Descrição**: Retorna o número de valores Unicode na string entre os índices especificados.
**Tipo de Retorno**: `int`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello";
        int count = str.codePointCount(0, str.length());
        System.out.println("codePointCount: " + count); // Outputs: 5
    }
}
```

### 5. `compareTo(String anotherString)`
**Descrição**: Compara duas strings lexicograficamente.
**Tipo de Retorno**: `int`

```java
public class StringExample {
    public static void main(String[] args) {
        String str1 = "Hello";
        String str2 = "World";
        int result = str1.compareTo(str2);
        System.out.println("compareTo: " + result); // Outputs a negative number
    }
}
```

### 6. `compareToIgnoreCase(String str)`
**Descrição**: Compara duas strings lexicograficamente, ignorando diferenças de maiúsculas e minúsculas.
**Tipo de Retorno**: `int`

```java
public class StringExample {
    public static void main(String[] args) {
        String str1 = "hello";
        String str2 = "HELLO";
        int result = str1.compareToIgnoreCase(str2);
        System.out.println("compareToIgnoreCase: " + result); // Outputs: 0
    }
}
```

### 7. `concat(String str)`
**Descrição**: Adiciona uma string ao final de outra string.
**Tipo de Retorno**: `String`

```java
public class StringExample {
    public static void main(String[] args) {
        String str1 = "Hello";
        String str2 = " World";
        String result = str1.concat(str2);
        System.out.println("concat: " + result); // Outputs: Hello World
    }
}
```

### 8. `contains(CharSequence s)`
**Descrição**: Verifica se uma string contém uma sequência de caracteres.
**Tipo de Retorno**: `boolean`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello World";
        boolean result = str.contains("World");
        System.out.println("contains: " + result); // Outputs: true
    }
}
```

### 9. `contentEquals(CharSequence cs)`
**Descrição**: Verifica se uma string contém a mesma sequência de caracteres que a especificada.
**Tipo de Retorno**: `boolean`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello World";
        boolean result = str.contentEquals("Hello World");
        System.out.println("contentEquals: " + result); // Outputs: true
    }
}
```

### 10. `copyValueOf(char[] data)`
**Descrição**: Retorna uma string que representa os caracteres do array de caracteres.
**Tipo de Retorno**: `String`

```java
public class StringExample {
    public static void main(String[] args) {
        char[] data = {'H', 'e', 'l', 'l', 'o'};
        String str = String.copyValueOf(data);
        System.out.println("copyValueOf: " + str); // Outputs: Hello
    }
}
```

### 11. `endsWith(String suffix)`
**Descrição**: Verifica se uma string termina com os caracteres especificados.
**Tipo de Retorno**: `boolean`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello World";
        boolean result = str.endsWith("World");
        System.out.println("endsWith: " + result); // Outputs: true
    }
}
```

### 12. `equals(Object anObject)`
**Descrição**: Compara duas strings. Retorna verdadeiro se as strings são iguais, e falso se não são.
**Tipo de Retorno**: `boolean`

```java
public class StringExample {
    public static void main(String[] args) {
        String str1 = "Hello";
        String str2 = "Hello";
        boolean result = str1.equals(str2);
        System.out.println("equals: " + result); // Outputs: true
    }
}
```

### 13. `equalsIgnoreCase(String anotherString)`
**Descrição**: Compara duas strings, ignorando considerações de maiúsculas e minúsculas.
**Tipo de Retorno**: `boolean`

```java
public class StringExample {
    public static void main(String[] args) {
        String str1 = "hello";
        String str2 = "HELLO";
        boolean result = str1.equalsIgnoreCase(str2);
        System.out.println("equalsIgnoreCase: " + result); // Outputs: true
    }
}
```

### 14. `format(String format, Object... args)`
**Descrição**: Retorna uma string formatada usando a string de formato e os argumentos especificados.
**Tipo de Retorno**: `String`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = String.format("Hello, %s!", "World");
        System.out.println("format: " + str); // Outputs: Hello, World!
    }
}
```

### 15. `getBytes()`
**Descrição**: Converte uma string em um array de bytes.
**Tipo de Retorno**: `byte[]`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello";
        byte[] bytes = str.getBytes();
        System.out.println("getBytes: " + java.util.Arrays.toString(bytes)); // Outputs byte array
    }
}
```

### 16. `getChars(int srcBegin, int srcEnd, char[] dst, int dstBegin)`
**Descrição**: Copia caracteres de uma string para um array de caracteres.
**Tipo de Retorno**: `void`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello World";
        char[] chars = new char[5];
        str.getChars(0, 5, chars, 0);
        System.out.println("getChars: " + java.util.Arrays.toString(chars)); // Outputs: [H, e, l, l, o]
    }
}
```

### 17. `hashCode()`
**Descrição**: Retorna o código hash de uma string.
**Tipo de Retorno**: `int`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello";
        int hashCode = str.hashCode();
        System.out.println("hashCode: " + hashCode); // Outputs hash code
    }
}
```

### 18. `indexOf(String str)`
**Descrição**: Retorna a posição da primeira ocorrência dos caracteres especificados em uma string.
**Tipo de Retorno**: `int`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello World";
        int index = str.indexOf("World");
        System.out.println("indexOf: " + index); // Outputs: 6
    }
}
```

### 19. `intern()`
**Descrição**: Retorna a representação canônica do objeto string.
**Tipo de Retorno**: `String`

```java
public class StringExample {
    public static void main(String[] args) {
        String str1 = new String("Hello");
        String str2 = str1.intern();
        System.out.println("intern: " + (str1 == str2)); // Outputs: false
    }
}
```

### 20. `isEmpty()`
**Descrição**: Verifica se uma string está vazia.
**Tipo de Retorno**: `boolean`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "";
        boolean result = str.isEmpty();
        System.out.println("

isEmpty: " + result); // Outputs: true
    }
}
```

### 21. `join(CharSequence delimiter, CharSequence... elements)`
**Descrição**: Junta uma ou mais strings com um delimitador especificado.
**Tipo de Retorno**: `String`

```java
public class StringExample {
    public static void main(String[] args) {
        String result = String.join(", ", "Hello", "World");
        System.out.println("join: " + result); // Outputs: Hello, World
    }
}
```

### 22. `lastIndexOf(String str)`
**Descrição**: Retorna a posição da última ocorrência dos caracteres especificados em uma string.
**Tipo de Retorno**: `int`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello World World";
        int index = str.lastIndexOf("World");
        System.out.println("lastIndexOf: " + index); // Outputs: 12
    }
}
```

### 23. `length()`
**Descrição**: Retorna o comprimento de uma string especificada.
**Tipo de Retorno**: `int`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello";
        int length = str.length();
        System.out.println("length: " + length); // Outputs: 5
    }
}
```

### 24. `matches(String regex)`
**Descrição**: Procura uma correspondência na string para uma expressão regular e retorna a correspondência.
**Tipo de Retorno**: `boolean`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "12345";
        boolean result = str.matches("\\d+");
        System.out.println("matches: " + result); // Outputs: true
    }
}
```

### 25. `offsetByCodePoints(int index, int codePointOffset)`
**Descrição**: Retorna o índice dentro desta String que está deslocado a partir do índice dado pelo número de pontos de código.
**Tipo de Retorno**: `int`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello";
        int index = str.offsetByCodePoints(0, 2);
        System.out.println("offsetByCodePoints: " + index); // Outputs: 2
    }
}
```

### 26. `regionMatches(int toffset, String other, int ooffset, int len)`
**Descrição**: Testa se duas regiões de string são iguais.
**Tipo de Retorno**: `boolean`

```java
public class StringExample {
    public static void main(String[] args) {
        String str1 = "Hello World";
        String str2 = "World";
        boolean result = str1.regionMatches(6, str2, 0, 5);
        System.out.println("regionMatches: " + result); // Outputs: true
    }
}
```

### 27. `replace(char oldChar, char newChar)`
**Descrição**: Substitui todas as ocorrências de um caractere em uma string por outro caractere.
**Tipo de Retorno**: `String`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello World";
        String result = str.replace('o', 'a');
        System.out.println("replace: " + result); // Outputs: Hella Warld
    }
}
```

### 28. `replaceAll(String regex, String replacement)`
**Descrição**: Substitui cada substring desta string que coincide com a expressão regular fornecida pelo substituto fornecido.
**Tipo de Retorno**: `String`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "abc123abc";
        String result = str.replaceAll("\\d", "X");
        System.out.println("replaceAll: " + result); // Outputs: abcXXXabc
    }
}
```

### 29. `replaceFirst(String regex, String replacement)`
**Descrição**: Substitui a primeira ocorrência de uma substring que coincide com a expressão regular fornecida pelo substituto fornecido.
**Tipo de Retorno**: `String`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "abc123abc";
        String result = str.replaceFirst("\\d", "X");
        System.out.println("replaceFirst: " + result); // Outputs: abcX23abc
    }
}
```

### 30. `split(String regex)`
**Descrição**: Divide uma string em um array de substrings.
**Tipo de Retorno**: `String[]`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "apple,orange,banana";
        String[] fruits = str.split(",");
        System.out.println("split: " + java.util.Arrays.toString(fruits)); // Outputs: [apple, orange, banana]
    }
}
```

### 31. `startsWith(String prefix)`
**Descrição**: Verifica se uma string começa com os caracteres especificados.
**Tipo de Retorno**: `boolean`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello World";
        boolean result = str.startsWith("Hello");
        System.out.println("startsWith: " + result); // Outputs: true
    }
}
```

### 32. `subSequence(int beginIndex, int endIndex)`
**Descrição**: Retorna uma nova sequência de caracteres que é uma subsequência desta sequência.
**Tipo de Retorno**: `CharSequence`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello World";
        CharSequence subSeq = str.subSequence(0, 5);
        System.out.println("subSequence: " + subSeq); // Outputs: Hello
    }
}
```

### 33. `substring(int beginIndex)`
**Descrição**: Retorna uma nova string que é uma substring da string especificada.
**Tipo de Retorno**: `String`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello World";
        String subStr = str.substring(6);
        System.out.println("substring: " + subStr); // Outputs: World
    }
}
```

### 34. `toCharArray()`
**Descrição**: Converte esta string em um novo array de caracteres.
**Tipo de Retorno**: `char[]`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello";
        char[] chars = str.toCharArray();
        System.out.println("toCharArray: " + java.util.Arrays.toString(chars)); // Outputs: [H, e, l, l, o]
    }
}
```

### 35. `toLowerCase()`
**Descrição**: Converte uma string para letras minúsculas.
**Tipo de Retorno**: `String`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "HELLO";
        String lowerStr = str.toLowerCase();
        System.out.println("toLowerCase: " + lowerStr); // Outputs: hello
    }
}
```

### 36. `toString()`
**Descrição**: Retorna o valor de um objeto String.
**Tipo de Retorno**: `String`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "Hello";
        String toString = str.toString();
        System.out.println("toString: " + toString); // Outputs: Hello
    }
}
```

### 37. `toUpperCase()`
**Descrição**: Converte uma string para letras maiúsculas.
**Tipo de Retorno**: `String`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "hello";
        String upperStr = str.toUpperCase();
        System.out.println("toUpperCase: " + upperStr); // Outputs: HELLO
    }
}
```

### 38. `trim()`
**Descrição**: Remove espaços em branco dos dois lados de uma string.
**Tipo de Retorno**: `String`

```java
public class StringExample {
    public static void main(String[] args) {
        String str = "  Hello World  ";
        String trimmedStr = str.trim();
        System.out.println("trim: " + trimmedStr); // Outputs: Hello World
    }
}
```

### 39. `valueOf(Object obj)`
**Descrição**: Retorna a representação em string do valor especificado.
**Tipo de Retorno**: `String`

```java
public class StringExample {
    public static void main(String[] args) {
        int value = 123;
        String str = String.valueOf(value);
        System.out.println("valueOf: " + str); // Outputs: 123
    }
}
```








