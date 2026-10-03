# Hyris Resource Pack

O pack é publicado automaticamente a cada push nas branches `dev` e `main`.
Cada commit gera uma Release com a tag `<branch>-<12 primeiros caracteres do SHA>`.
As Releases de `dev` são pré-lançamentos; as de `main` são lançamentos estáveis.

O arquivo para o Minecraft é o asset `resource-pack.zip` da Release, não o
arquivo “Source code (zip)” criado automaticamente pelo GitHub. O asset
`resource-pack.sha1` contém o hash para `resource-pack-sha1` no `server.properties`.
Cada Release também mostra a configuração completa do `server.properties` na descrição.

Exemplo de configuração:

```properties
resource-pack=https://github.com/hyris-corp/resource-pack/releases/download/main-<SHA>/resource-pack.zip
resource-pack-sha1=<conteúdo de resource-pack.sha1>
require-resource-pack=true
resource-pack-prompt={"text":"Hyris","color":"gold","extra":[{"text":" - Aceite o pacote de texturas para ver tags e itens.","color":"gray"}]}
```

O repositório precisa ser público para o cliente do Minecraft baixar o ZIP sem autenticação.
