# Arquivos

## Edição

A leitura e edição de arquivos utilizando um código em Crystal pode ser uma ferramenta muito poderosa! Veja um exemplo para leitura de um arquivo em Crystal:

```cr
if ARGV.size != 1 # Definimos se existem argumentos passados! É necessário informar o nome do arquivo que deseja visualizar o conteúdo!
    puts "É necessário passar o nome do arquivo como parâmetro!"
    exit 1
end

file = ARGV[0]

conteudo = File.read(file) # Nesta etapa é lido o conteúdo do arquivo e passado para uma variável!

puts conteudo
```

Perceba que no exemplo acima conseguimos armazenar o conteúdo de um arquivo em uma variável!

Para adicionar texto em um arquivo podemos utilizar a função "File.write"!

```cr
if ARGV.size != 2
    puts "É necessário informar o nome do arquivo e o conteúdo a ser escrito!"
    exit 1
end

file, conteudo = ARGV

File.write(file, conteudo)
```

Inicialmente realizamos uma verificação para verificar se são passados o nome do arquivo a ser alterado seguido do conteúdo a ser adicionado! Assim, conseguimos facilmente alterar o conteúdo de um arquivo qualquer utilizando Crystal, porém, tome cuidado! Utilizando da forma apresentada no exemplo anterior realizamos uma substituição de conteúdo, ou seja, o conteúdo que havia no arquivo antes da alteração foi simplesmente excluído... Se você quiser adicionar algum conteúdo em um arquivo basta utilizar um parâmetro a mais na função "File.write":

```cr
if ARGV.size != 2
    puts "É necessário informar o nome do arquivo e o conteúdo a ser escrito!"
    exit 1
end

file, conteudo = ARGV

File.write(file, conteudo, mode: "a") # Aqui é adicionado mais um parâmetro!
```

## Propriedades
