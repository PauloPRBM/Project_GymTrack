<h1 align="center">GymTrack</h1>

<div align="center">
  <strong>🏋🏽 ⚙️ 🏃🏽</strong>
</div>
<div align="center">
  GymTrack é uma plataforma inteligente de gestão para academias, oferecendo controle automatizado de fluxo de alunos, monitoramento de progresso físico e otimização da experiência dos usuários em tempo real!
</div>

## 🛠️ Pré-requisitos

N/A

## 🚀 Passo a passo interativo

n/a

<div align="center">
</div>

## Links Úteis:

1. <img src="https://upload.wikimedia.org/wikipedia/commons/3/33/Figma-logo.svg" alt="Figma" width="20"/> [Figma Design](https://www.figma.com/design/P3UNY8tWPJj7FW43XrU9ZE/Untitled?node-id=0-1&t=b3ow5hTyewWG7oIH-1)

2. <img src="https://cdn-icons-png.flaticon.com/512/5968/5968875.png" alt="Jira" width="20"/> [Jira Board](https://coderfullstackvinicius.atlassian.net/jira/software/projects/SCRUM/boards/1/backlog?atlOrigin=eyJpIjoiYjI0Yzc5YWNmNTJiNGIzYjhlYjg2YzJjMGEyZDdlNjYiLCJwIjoiaiJ9)

## Integrantes do Projeto:

- Vinícius S. Queiroz - [Link do LinkedIn](https://www.linkedin.com/in/viníciussilvaqueiroz/)
- Guilherme W. Nogueira - [Link do LinkedIn](https://www.linkedin.com/in/guilherme-wolf/)
- Arthur F. Campos - [Link do LinkedIn](https://www.linkedin.com/in/arthur-campos-a120472b7/)
- Dereck A. do E. Portela - [Link do LinkedIn](https://www.linkedin.com/in/dereck-portela-36682675/)
- Paulo R. de B. Mendes - [Link do LinkedIn](https://www.linkedin.com/in/paulo-mendes/)
- Pierre Costa S. de O. N. - [Link do LinkedIn](https://www.linkedin.com/in/pierre-costa-b1b51314a/)
- Ylson Santos - [Link do LinkedIn](https://www.linkedin.com/in/pierre-costa-b1b51314a/)

## Diagrama de Classes

```mermaid
classDiagram
    %% Definição das classes com seus atributos
    class Aluno {
        +int id
        +string nome
        +string cpf
        +string endereco
        +string telefone
        +string email
        +Date dataNascimento
    }
    class Treino {
        +int id
        +string nome
        +string descricao
        +Date dataInicio
        +Date dataFim
    }
    class Exercicio {
        +int id
        +string nome
        +string descricao
        +string grupoMuscular
    }
    class Instrutor {
        +int id
        +string nome
        +string cref
        +string telefone
        +string email
    }
    class AvaliacaoFisica {
        +int id
        +Date dataAvaliacao
        +float peso
        +float altura
        +float percentualGordura
        +float massaMuscular
    }
    class Pagamento {
        +int id
        +Date dataPagamento
        +float valor
        +string metodoPagamento
    }
    class Plano {
        +int id
        +string nome
        +string descricao
        +float valorMensal
    }

    %% Definição dos relacionamentos com cardinalidades
    Aluno "1" --> "0..*" AvaliacaoFisica : realiza
    Aluno "1" --> "0..*" Pagamento : efetua
    Aluno "1" --> "1" Plano : assina
    Aluno "1" --> "0..*" Treino : segue
    Treino "1" --> "1..*" Exercicio : contém
    Treino "1" --> "1" Instrutor : elaborado_por
    Instrutor "1" --> "0..*" Treino : elabora
```
