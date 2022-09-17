# Diretórios

## Listagem

Diversas funcionalidades são possíveis quando utilizamos Crystal, dentre elas a listagem de conteúdo é uma das funcionalidades que permitem gerenciar nossos diretórios. Observe o exemplo abaixo:

```cr
if ARGV.size != 1
    puts "Você precisa informar o caminho do diretório!"
    exit 1
end

path = ARGV[0]

dr = Dir.new(path)
dr.children.each { |thing|
    puts thing
}
```

O exemplo acima irá retornar o conteúdo completo de um diretório, sendo necessário informar o caminho para que se possa visualizar seu conteúdo!

## Visualizar caminho

Para visualizar o caminho completo em que você se encontra basta utilizar a seguinte função: 

```cr
puts Dir.current # Similar ao comando pwd!
```
