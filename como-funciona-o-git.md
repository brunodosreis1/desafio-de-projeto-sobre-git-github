# COMO FUNCIONA O GIT? 

#### ◘ 4 tópicos fundamentais:

1.  SHA1 
2.  Objetos fundamentais
3.  Sistemas distribuidos
4.  Segurança (porque o Git é seguro?)

###   1- SHA1 (Secure Hash Algorithm)

   traduzido: Algaritmo de Hash Seguro.

#### o que é:

é um método de codificação bastante seguro, sendo utilizado comumente em diversas aplicações importantes, inclusive em aplicações governamentais. Esse conjunto de funções HASH criptografados foram projetados pela NSA (Agência de Segurança Nacional)

* <u>Esses dados criptografados geram um conjunto de caracteres identificados de 40 dígitos.</u> 

* Serve como identificação, é uma forma curta de representa um arquivo. 

  ### 2- Objetos internos do GIT

  São 3 tipos básicos de objeto do GIT, responsáveis pelo versionamento do código. 

  1. <u>**BLOOBS**:</u> Apenas conteúdos, fluxo binário de dados. 

     * Um BLOOBS não registra sua data de criação, seu nome ou nada além do conteúdo. 

     * Cada BLOOB em GIT é identificado por seu HASH SHA1, os Hash sha1 consistem em 20 bytes, representados por 40 caracteres. 

     * O Bloob contem metodos do GIT, que são: 

       • Tipo de objeto

       • Tamanho da string

       • Tamanho do Arquivo

  2. **<u>TREES:</u> (arvores)** - Armazenam Bloobs. 

     * contem também metadados 

     * Guarda nome do arquivo

     * tem o SHA1

     * Responsável por montar toda estrutura de onde esta os arquivos (de onde estão localizados esses arquivos)

       

  3. **<u>COMMITS</u>**: Objeto que vai juntar tudo, que vai dar sentido para alteração que esta fazendo. 

     * Estrutura: 

       • Tree (arvore);

       • Parente (ultimo commit realizado antes dele) ;

       • Autor (quem esta fazendo o commit);

       • Mensagem (Um autor pode escrever uma mensagem dentro do commit, que vai explicar e dar significado para esses conjuntos de arquivos dentro desse conjunto de pastas);

       • Timestamp: Carimbo de tempo (Data, horário de quando ele foi criado).

       • Também possui SHA1

  O Commit significa exatamente o que você quer dizer com o código que não tem interferência de outras pessoas. 

  

  ### 3- GIT é um sistema distribuído seguro;

  Ex: Tenho meu código hosteado no meu repositório em um servidor (github), o código que esta lá representa o estado final do meu código, a versão mais recente. Se ele esta em um servidor que tem varias pessoas, contribuindo com ele, essas pessoas também tem uma versão desse código. Pelo fato de todos commits serem difíceis de serem alterados, tanto a versão mais recente, quanto as outras, também são versões confiáveis. Se der um problema no servidor e acontecer algo com seu código, também ira acontecer com os outros, porque as versões disponíveis dos outros também são super confiáveis devido as estruturas que o GIT mantem e são super confiáveis..
