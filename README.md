
<div align="center">
  <img width="200"  alt="5968214" src="https://github.com/user-attachments/assets/db667a3f-fb11-419d-98db-88d4c118f29e" />
  <h1>Sistema De Inventario em Haskell</h1>
  

  <p>
    Sistema desenvolvido em Haskell para por em pratica conceitos de programação funcional, manipulação de estado e operações de I/O em Haskell
para desenvolver um programa que gerencie um sistema de inventário.
  </p>
</div>



## :globe_with_meridians:	Rodar em ambiente virtual

- Para utilizar o programa, abra o link do projeto hospedado em [OnlineGDB](https://onlinegdb.com/3yNQBvhQYM)
- Para rodar o programa aperte o botão verde escrito "Run" acima do editor de texto
<img width="304" height="94" alt="Screenshot 2025-11-14 203642" src="https://github.com/user-attachments/assets/c0c5e0c6-4c3f-4a41-9ad0-dba46a8aa971" />

- Ou aperte a tecla f9 no teclado como atalho.


## :runner: Utilização


Ao abrir o projeto você terá acesso à três arquivos
- main.hs
  - Esse arquivo é o ponto inicial da aplicação, responsavel pela logica de Inicialização, Sincronização, e os funções de I/O
- LogicaPura.hs
  - Armazena funções puras de transação, opera em cima do estado atual do Inventario de acordo com os parametros da operação
- Tipo.hs
  - Define os tipos de dados utilizados ao decorrer da execução do programa 

Na primeira execução do codido serão criados dois arquivos:

- Auditoria.log
  - Guarda todas as informações das operações feitas no sistema, tanto as realizadas com sucesso quanto as que falharam. Efetivamente um historico de operações
- Inventario.dat
  - Guarda o estado de todos os itens do sistema
 
Esses dois arquivos de armazenamento são abertos no inicio de toda execução, mas caso sejam apagados ou seja a primeira vez rodando o programa, eles serão criados automaticamente.  

```javascript
Inventário não encontrado. Criando novo.
Comandos disponíveis:
  add <id> <nome> <categoria> <quantidade>    -- Adiciona um item
  remove <id> <quantidade>                    -- Reduz a quantidade unitaria de um item
  update <id> <nome> <categoria> <quantidade> -- Atualiza um item (pelo id)
  report                                      -- Gera relatórios do inventário e logs
  sair                                        -- Encerra o programa
```

Para executar um comando, clique no terminal, digite o comando seguido de seus argumentos como no exemplo abaixo e aperte enter para enviar

```haskell
> add 4 MSI-Cyborg Notebook-Gamer 14
-- add <id> <nome> <categoria> <quantidade>
```

Então você recebera uma confirmação do estado final do seu comando, tanto se houve exito ou não, acompanhado do motivo

Sucesso na inserção:
```haskell
[Add] Adicionado item: Item {itemID = "00001", nome = "IdeaPad-S145", categoria = "Notebook", quantidade = 90}
Inventário atual:
- ID: 00001, Nome: IdeaPad-S145, Cat: Notebook, Qtde: 90
```
Falha no update:
```haskell
> update 731282 MSI-Cyborg Notebook-Gamer 14

FALHA NA OPERACAO ATUALIZAR
O id deve ter no máximo 5 caracteres.
Tentativa: de entradaItem {itemID = "731282", nome = "MSI-Cyborg", categoria = "Laptop", quantidade = 14}
```

E você pode conferir a persistencia dos dados nos arquivos mesmo após o encerramento do programa abrindo Inventario.dat e Auditoria.log
<img width="1180" height="102" alt="Screenshot 2025-11-14 212729" src="https://github.com/user-attachments/assets/1579b90e-6fe7-4f70-9e75-c8bb70b37466" />
<img width="1677" height="102" alt="Screenshot 2025-11-14 213156" src="https://github.com/user-attachments/assets/79ce7d42-33e7-48ec-b846-f17e1ec5b39f" />

## :school: Instituiçao

Pontifícia Universidade Católica do Paraná (PUCPR)

Disciplina: Programação Lógica e Funcional

Curso: Ciência da Computação

Turma: 4º U

Professor: Frank Coelho de Alcantara

## :bust_in_silhouette:	 Integrantes

Gustavo Botan Mizuguti - GitHub: GMizuguti


