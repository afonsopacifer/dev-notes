# Shell Script
[Awesome Shell Script](https://github.com/alebcay/awesome-shell#shell-script-development) / [Learn Ruby in Y minutes](https://learnxinyminutes.com/docs/bash/)

>

- [Notes](#notes)
- [References](#references)

## Notes
- [Introdução](#introducao)
- [Variáveis](#variaveis)
- [If](#if)
- [Operadores](#operadores)
- [Comandos](#comandos)
- [<s>Case</s>](#case)
- [<s>Parâmetros</s>](#parametros)
- [<s>For</s>](#for)
- [<s>While</s>](#while)
- [<s>Until</s>](#until)
- [<s>Modulos</s>](#modulos)
- [<s>Variáveis especiais</s>](#variaveis-especiais)
- [<s>Funções</s>](#funcoes)

#### Introdução

Crie um arquivo com a extenção `.sh` e adicione a linha `#!/bin/bash`:

```sh
#!/bin/bash
# hello.sh

echo 'Hello World'
```

Atribuir o comando de executável:

```sh
$ chmod +x arquivo
```

Para executar use:

```sh
$ ./hello.sh
```

ou

```sh
$ sh hello.sh
```

### Variáveis

```sh
#!/bin/bash

variavel="valor"

echo $variavel
```

### If
```sh
#!/bin/bash

if [ -e $variavel ]
then
  echo 'A variável existe.'
else
  echo 'A variável não existe.'
fi
```

### Operadores

Oper. | Descrição
--- | ---
-eq	| Igual
-ne	| Diferente
-gt	| Maior
-lt	| Menor
-o	| Ou
-d	| Se for um diretório
-e	| Se existir
-z	| Se estiver vazio
-f	| Se conter texto
-o	| Se o usuário for o dono
-r	| Se o arquivo pode ser lido
-w	| Se o arquivo pode ser alterado
-x	| Se o arquivo pode ser executado

### Comandos

Comando | Descrição
--- | ---
echo | Imprime texto na tela
read	| Captura dados do usuário e coloca numa variável
exit	| Finaliza o script
sleep	| Dá uma pausa em segundos no script
clear	| Limpa a tela
stty	| Configura o terminal temporariamente
tput	| Altera o modo de exibição
if	| Controle de fluxo que testa uma ou mais expressões
case	| Controle de fluxo que testa várias expressões ao mesmo tempo
for	| Controle de fluxo que testa uma ou mais expressões
while	| Controle de fluxo que testa uma ou mais
expressões

### Case
```sh
#!/bin/bash

echo ''
```

### Parâmetros
```sh
#!/bin/bash

echo ''
```

### For
```sh
#!/bin/bash

echo ''
```

### While
```sh
#!/bin/bash

echo ''
```

### Until
```sh
#!/bin/bash

echo ''
```

### Modulos
```sh
#!/bin/bash

echo ''
```

### Variáveis especiais
```sh
#!/bin/bash

echo ''
```

### Funções
```sh
#!/bin/bash

echo ''
```

## References
- [[Guide] - Programando em shell script - Devim - PT-BR](http://www.devin.com.br/shell_script/)
