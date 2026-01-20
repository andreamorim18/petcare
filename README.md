# 🐾 Mundo Pet - Sistema de Agendamentos

Sistema web responsivo de agendamento para Pet Shop, desenvolvido como desafio da formação Full-Stack da **Rocketseat**.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

## 📋 Sobre o Projeto

O **Mundo Pet** é uma aplicação web que permite gerenciar agendamentos de serviços para pets, organizados por período do dia (Manhã, Tarde e Noite).

### ✨ Funcionalidades

- ✅ Visualização de agendamentos por data
- ✅ Organização por períodos (Manhã, Tarde, Noite)
- ✅ Adicionar novos agendamentos via modal
- ✅ Remover agendamentos existentes
- ✅ Persistência de dados no LocalStorage
- ✅ Design responsivo (Mobile First)
- ✅ Interface dark mode

---

## 🎨 Design System

O projeto segue fielmente o design do Figma da Rocketseat.

### Cores

| Tipo | Hex |
|------|-----|
| Background Primary | `#1B1B1E` |
| Background Secondary | `#232326` |
| Brand | `#9282FA` |
| Accent Blue | `#027DF0` |
| Accent Yellow | `#F0DC02` |
| Accent Orange | `#F09102` |

### Tipografia

- **Títulos:** Inter Tight (Bold, 24px)
- **Corpo:** Inter (Regular/Medium, 14px)

---

## 🚀 Como Usar

1. Baixe o arquivo `mundo-pet-agendamento.html`
2. Abra diretamente no navegador
3. Pronto! 🎉

---

## 📱 Telas

### Lista de Agendamentos (Dark)
- Header com logo "MUNDO PET"
- Seletor de data
- Seções: Manhã (09h-12h), Tarde (13h-18h), Noite (18h-21h)
- Cards de agendamento com horário, pet, tutor e serviço
- Botão "NOVO AGENDAMENTO"

### Modal de Cadastro (Light)
- Campos: Nome do tutor, Nome do pet, Telefone
- Descrição do serviço
- Data e Hora
- Botão "AGENDAR"

---

## 🛠️ Tecnologias

### HTML5
- Estrutura semântica
- Formulários com validação nativa
- Atributos de acessibilidade

### CSS3
- CSS Variables para Design Tokens
- Flexbox e Grid Layout
- Animações e transições
- Media queries para responsividade
- Dark mode

### JavaScript (ES6+)
- LocalStorage API
- Event Delegation
- DOM Manipulation
- Módulos com padrão de objeto literal

---

## 📦 Estrutura do Código

```javascript
// 📊 DATA MANAGER - Gerencia os dados
const DataManager = {
    getAll(),       // Busca todos os agendamentos
    create(),       // Cria novo agendamento
    delete(),       // Remove agendamento
    getByDate()     // Filtra por data
}

// 🎨 UI - Gerencia a interface
const UI = {
    init(),                 // Inicializa elementos
    renderAppointments(),   // Renderiza lista
    openModal(),            // Abre modal
    closeModal()            // Fecha modal
}

// 🎮 APP - Controle principal
const App = {
    init(),                 // Inicializa app
    setupEventListeners(),  // Configura eventos
    handleCreate(),         // Cria agendamento
    handleDelete()          // Remove agendamento
}
```

---

## 🎯 Períodos de Atendimento

| Período | Horário | Ícone |
|---------|---------|-------|
| Manhã | 09h - 12h | ☀️ (azul) |
| Tarde | 13h - 18h | 🌅 (laranja) |
| Noite | 18h - 21h | 🌙 (amarelo) |

---

## 🗄️ Dados no LocalStorage

```javascript
// Chave
'mundopet_appointments'

// Estrutura
{
    id: "apt_1705123456789",
    tutorName: "Helena Souza",
    petName: "Thor",
    phone: "(27) 9 9999-9999",
    service: "Banho e Tosa",
    date: "2024-01-10",
    time: "09:00",
    createdAt: "2024-01-10T08:00:00.000Z"
}
```

---

## 📄 Licença

Projeto desenvolvido para fins educacionais - Desafio Rocketseat.

---

## 🔗 Links

- [Figma do Projeto](https://www.figma.com/community/file/1402272413594042585/agendamento-de-petshop)
- [Rocketseat](https://www.rocketseat.com.br/)

---

<p align="center">
  Feito com 💜 por André Amorim
</p>
