<h4 align="center"> 
	Amostra de como usar Flask com GraphQL
</h4>

## Objetivo
  * Construir uma pequena aplicação em Flask com GraphQL.
  * A aplicação deverá criar um autor ou uma postagem.
  * A aplicação deverá retornar todos os autores ou todas as postagens.

## Configuração para utilizar 🛠

### Linux
Primeiro passo: 
- Criar um ambiente virtual
`pip install virtualenv`
`virtualenv .ambvir --python=python3.7`
`source ambvir/bin/activate`

Segundo passo:
- Criar um arquivo `.env` apartir do `.env_exemple` na raiz do projeto.

Terceiro passo:
- Executar o comando `pip install -r requeriments.txt` na raiz do projeto.

Quarto passo:
- Executar o comando `python app.py` na raiz do projeto.

### Windowns
Primeiro passo: 
- Criar um ambiente virtual:
`pip install virtualenv`
`python -m venv .amvbir`
`.amvbir\Scripts\Activate.bat`

Segundo passo:
- Criar um arquivo `.env` apartir do `.env_exemple` na raiz do projeto.

Terceiro passo:
- Executar o comando `pip install -r requeriments.txt` na raiz do projeto.

Quarto passo:
- Executar o comando `python app.py` na raiz do projeto.


## Usando a aplicação

### Rotas
- Home `http://127.0.0.1:5000/`

- Página do GraphQL `http://127.0.0.1:5000/graphql`

### Query
***Obs***: Assim que estiver na rota `/graphql` você poderá utilizar os payloads abaixo.

* Query posts:
```python
{
  allPosts{
    edges{
      node{
        title
        body
        author{
          username
        }
      }
    }
  }
}
```
* Query users:
```python
{
  allUsers{
    edges{
      node{
        username
      }
    }
  }
}
```

### Mutation
* Mutation create user:
```python
mutation {
  createUser(username:"Alex"){
    user{
      uuid
      username
    }
  }
}
```
* Mutation create post:
```python
mutation {
  createPost(username:"Alex", title:"Aventuras", body:"Aquela aventura..."){
    post{
      title
      body
      author{
        username
      }
    }
  }
}
```

## Tecnologias

- [Python](https://www.python.org/)
- [Flask](https://flask.palletsprojects.com/en/1.1.x/)
- [GraphQl](https://graphql.org/)

## Autor
<table>
  <tr>
    <th><img src="https://avatars.githubusercontent.com/u/82416762?v=4" width=60></th>
  </tr>
  <tr>
    <td><a href="https://github.com/ClaudionorJunior">Github</a></td>
  </tr>
  <tr>
    <td><a href="https://www.linkedin.com/in/claudionorsilva">Linkedin</a></td>
  </tr>
</table>
