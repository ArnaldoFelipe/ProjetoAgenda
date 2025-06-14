Iniciar o projeto Django

```
python -m venv venv
. venv/bin/ativar
pip instalar django
django-admin startproject projeto .
contato python manager.py startapp

```

Configurar o git

```
git config --global user.name 'Seu nome'
git config --global user.email 'seu_email@gmail.com'
git config --global init.defaultBranch principal
# Configurar o .gitignore
git init
git add .
git commit -m 'Mensagem'
git remoto adicionar URL de origem_DO_GIT

Migrando para base de dados do Django

```
migrações python manager.py
python manage.py migrar
```

Criando e modificando a senha de um super usuário Django

```
python manage.py criasuperusuário
python manage.py alterar senha NOME DE USUÁRIO
```

Trabalhando com o modelo do Django

```pitão
#Importar ou módulo
decontato.modelosimportarContato
#Criar um contato (Lazy)
#Retorna o contato
contato=Contato(**campos)
contato.salvar()
#Cria um contato (Não lazy)
#Retorna o contato
contato=Contato.objetos.criar(**campos)
#Selecione um contato com id 10
#Retorna o contato
contato=Contato.objetos.obter(pk=10)
#Edita um contato
#Retorna o contato
contato.campo_nome1= 'Novo valor 1'
contato.campo_nome2= 'Novo valor 2'
contato.salvar()
#Apaga um contato
#Depende da base de dados, geralmente retorna o número
#de valores manipulados na base de dados
contato.delete()
#Selecionamos todos os contatos ordenando por id DESC
#Retorna QuerySet[]
contatos=Contato.objetos.todos().ordenar_por('-eu ia')
#Seleciona contatos usando filtros
#Retorna QuerySet[]
contatos=Contato.objetos.filtro(**filtros).order_by('-eu ia')
```
