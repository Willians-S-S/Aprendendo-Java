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

Para executar um arquivo java pelo terminal primeiro é necessário fazer a compilação do arquivo com o comando:

`javac PrimeiroPrograma.java`

Em seguida executar com:
`java PrimeiroPrograma`




