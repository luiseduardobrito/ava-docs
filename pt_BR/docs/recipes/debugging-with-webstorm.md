___
**Nota do tradutor**

Esta é a tradução de [debugging-with-webstorm.md](https://github.com/avajs/ava/blob/master/docs/recipes/debugging-with-webstorm.md). [Este link](https://github.com/avajs/ava/compare/e02bd644c2c49d3a0eb16f4a202802aaf9308335...master) compara a versão em que se baseou esta tradução com a última versão disponível no branch `master` do AVA. Se não houver mudanças em `debugging-with-webstorm.md`, então a tradução está atualizada.

Também assume-se aqui que seu IDE está em Inglês (US).
___

# Depurando testes com o WebStorm

Traduções: [Francês](https://github.com/avajs/ava-docs/blob/master/fr_FR/docs/recipes/debugging-with-webstorm.md)

Desde a versão 2016.2, [WebStorm](https://www.jetbrains.com/webstorm/) e outros IDEs  da JetBrains (IntelliJ IDEA Ultimate, PHPStorm, PyCharm Professional, e RubyMine com o plugin de Node.js instalado) permitem usar o AVA em modo de depuração.


## Configuração

Adicione uma nova configuração de *Run/Debug para Node.js*: selecione `Edit Configurations...` no menu de opções no topo direito da tela, então clique em `+` e selecione *Node.js*.

No item `JavaScript file` insira o caminho para o AVA na pasta `node_modules` do projeto: `node_modules/.bin/ava` no macOS e Linux ou `node_modules/.bin/ava.cmd` no Windows.

No item `Application parameters` passe os parâmetros de console (CLI flags) que você está usando e os arquivos de teste que deseja depurar, por exemplo `--verbose test.js`.

Salve a nova configuração.


## Depuração

Prepare o código com seus pontos de depuração, ou *breakpoints*.

Clique no botão `Debug` em verde próximo à lista de configurações disponíveis no topo direito da tela. A janela `Debug tool window` vai aparecer. Assim que a execução atingir um ponto de depuração, *breakpoint*, voc poderá avaliar variáveis e seguir o código passo a passo. Para depurar múltiplos arquivos, você pode trocar de processo usando o menu na aba de `Frames`.
