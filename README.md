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
- Paulo R. de B. Mendes - [Link do LinkedIn](https://www.linkedin.com/in/paulo-mendes)

## Diagrama de Classes

```mermaid
classDiagram
    class User {
        +String username
        +String email
        +String password
    }
    class Profile {
        +int age
        +float weight
        +float height
        +String phone_number
    }
    class WorkoutPlan {
        +String name
        +String description
    }
    class Exercise {
        +String name
        +String muscle_group
        +int sets
        +int reps
    }
    class Attendance {
        +Date date
        +boolean present
    }

    User --> Profile : has
    User --> WorkoutPlan : assigned
    WorkoutPlan --> Exercise : includes
    User --> Attendance : logs
  ```
