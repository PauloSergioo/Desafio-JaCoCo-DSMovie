# DESAFIO: DSMovie - Backend

# Sobre o desafio

### Premissas

- É um sistema que possui um modelo de domínio relativamente simples,
porém abrangente, ou seja, que explore vários tipos de relacionamentos entre as
entidades de negócio (muitos-para-um, muitos-para-muitos, etc.).
- O sistema possibilita a aplicação de vários conhecimentos importantes das
disciplinas de fundamentos.
- O sistema contem as principais funcionalidades que se espera de um
profissional iniciante deve saber construir.


## 

### Visão geral do sistema

Este é um projeto de filmes e avaliações de filmes. A visualização dos dados dos filmes é pública (não necessita login),
porém as alterações de filmes (inserir, atualizar, deletar) são permitidas apenas para usuários ADMIN.
As avaliações de filmes podem ser registradas por qualquer usuário logado CLIENT ou ADMIN.
A entidade Score armazena uma nota de 0 a 5 (score) que cada usuário deu a cada filme. Sempre que um usuário registra uma nota, 
o sistema calcula a média das notas de todos usuários, e armazena essa nota média (score) na entidade Movie, 
juntamente com a contagem de votos (count).  Veja vídeo explicativo.

##

### Respeitando o seguinte Modelo Conceitual:

![image](https://github.com/PauloSergioo/Desafio-JaCoCo-DSMovie/assets/88008441/3eebf6ea-0173-4896-b2f2-8925f1de6405)


### Abaixo estão os testes unitários que foram implementados. Com todos os testes, o Jacoco deve reportar 100% de cobertura.

#### MovieServiceTests:

- findAllShouldReturnPagedMovieDTO
- findByIdShouldReturnMovieDTOWhenIdExists
- findByIdShouldThrowResourceNotFoundExceptionWhenIdDoesNotExist
- insertShouldReturnMovieDTO
- updateShouldReturnMovieDTOWhenIdExists
- updateShouldThrowResourceNotFoundExceptionWhenIdDoesNotExist
- deleteShouldDoNothingWhenIdExists
- deleteShouldThrowResourceNotFoundExceptionWhenIdDoesNotExist
- deleteShouldThrowDatabaseExceptionWhenDependentId

#### ScoreServiceTests:

- saveScoreShouldReturnMovieDTO
- saveScoreShouldThrowResourceNotFoundExceptionWhenNonExistingMovieId

#### UserServiceTests:

- authenticatedShouldReturnUserEntityWhenUserExists
- authenticatedShouldThrowUsernameNotFoundExceptionWhenUserDoesNotExists
- loadUserByUsernameShouldReturnUserDetailsWhenUserExists
- loadUserByUsernameShouldThrowUsernameNotFoundExceptionWhenUserDoesNotExists


# Educador

[DevSuperior - Escola de programação](https://devsuperior.com.br/)

[![DevSuperior no Instagram](https://raw.githubusercontent.com/devsuperior/bds-assets/main/ds/ig-icon.png)](https://instagram.com/devsuperior.ig) ![DevSuperior no Youtube](https://raw.githubusercontent.com/devsuperior/bds-assets/main/ds/yt-icon.png)
