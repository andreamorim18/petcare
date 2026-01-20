# 🐾 PetCare - Sistema de Agendamentos

Sistema web responsivo para agendamento em pet shop, desenvolvido com HTML5, CSS3 e JavaScript Vanilla.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

## 📋 Sobre o Projeto

O **PetCare** é uma aplicação web que permite gerenciar agendamentos de serviços para pets. Com uma interface intuitiva e moderna, o usuário pode visualizar, adicionar e remover compromissos de forma simples e rápida.

### ✨ Funcionalidades

- ✅ **Visualização** de agendamentos organizados por horário
- ✅ **Criação** de novos agendamentos com validação de formulário
- ✅ **Remoção** de agendamentos com animação suave
- ✅ **Persistência** de dados no LocalStorage
- ✅ **Design responsivo** (Mobile First)
- ✅ **Feedback visual** nas interações

---

## 🎨 Design

O projeto utiliza a estética **"Soft Organic"** com:

- Paleta de cores pastéis acolhedoras (roxo lavanda, laranja pêssego)
- Formas orgânicas animadas no background
- Cards com bordas arredondadas e sombras suaves
- Animações e transições fluidas
- Tipografia moderna (Quicksand + Fredoka)

---

## 🚀 Como Usar

### Opção 1: Arquivo Único (Recomendado)

1. Baixe o arquivo `petcare-agendamentos.html`
2. Abra diretamente no navegador

### Opção 2: Estrutura de Pastas

```
petshop-agendamento/
├── index.html
├── css/
│   └── style.css
└── js/
    └── app.js
```

> ⚠️ Nesta opção, mantenha a estrutura de pastas intacta.

---

## 🛠️ Tecnologias

### HTML5
- Tags semânticas (`<header>`, `<main>`, `<section>`, `<article>`)
- Template element para renderização dinâmica
- Formulário com validação nativa
- Atributos de acessibilidade (ARIA)

### CSS3
- CSS Variables (Custom Properties)
- Flexbox e Grid Layout
- Animações e transições com `@keyframes`
- Media queries para responsividade
- Pseudo-elementos e pseudo-classes

### JavaScript (ES6+)
- Módulos com padrão de objeto literal
- LocalStorage API para persistência
- Template literals
- Arrow functions
- Async/await
- Event delegation
- DOM manipulation

---

## 📦 Estrutura do Código JavaScript

O código segue uma arquitetura modular inspirada em MVC:

```javascript
// 📊 MODEL - Gerencia os dados
const AppointmentManager = {
    getAll(),      // READ - Busca todos os agendamentos
    create(),      // CREATE - Adiciona novo agendamento
    delete(),      // DELETE - Remove agendamento
    getAllSorted() // Retorna ordenado por data
}

// 🎨 VIEW - Gerencia a interface
const UIController = {
    init(),        // Inicializa referências do DOM
    renderList(),  // Renderiza lista de cards
    createCard(),  // Cria elemento do card
    removeCard(),  // Remove com animação
    getFormData(), // Coleta dados do formulário
    clearForm()    // Limpa o formulário
}

// 🎮 CONTROLLER - Conecta Model e View
const App = {
    init(),                // Inicializa a aplicação
    setupEventListeners(), // Configura eventos
    handleCreate(),        // Handler de criação
    handleDelete()         // Handler de remoção
}
```

---

## 🎯 Serviços Disponíveis

| Serviço | Ícone | Cor do Badge |
|---------|-------|--------------|
| Banho | 🛁 | Azul |
| Tosa | ✂️ | Vermelho |
| Banho + Tosa | 🛁✂️ | Índigo |
| Consulta | 🩺 | Verde |
| Vacinação | 💉 | Amarelo |
| Hidratação | 💧 | Ciano |

---

## 📱 Responsividade

O layout se adapta a diferentes tamanhos de tela:

| Dispositivo | Breakpoint | Ajustes |
|-------------|------------|---------|
| Mobile | < 480px | Layout em coluna, cards compactos |
| Tablet | ≥ 640px | Formulário em grid 2 colunas |
| Desktop | ≥ 768px | Espaçamentos maiores, cards expandidos |

---

## ♿ Acessibilidade

- Labels associados aos inputs
- Atributos `aria-label` e `aria-labelledby`
- Foco visível (`focus-visible`)
- Suporte a `prefers-reduced-motion`
- Contraste adequado de cores

---

## 🗄️ Persistência de Dados

Os dados são salvos no **LocalStorage** do navegador:

```javascript
// Chave utilizada
'petcare_appointments'

// Estrutura de um agendamento
{
    id: "apt_1234567890_abc123def",
    petName: "Thor",
    tutorName: "João Silva",
    service: "banho",
    datetime: "2025-01-20T14:30",
    createdAt: "2025-01-20T10:00:00.000Z"
}
```

---

## 🖼️ Preview

### Desktop
```
┌─────────────────────────────────────────┐
│           🐾 PetCare                    │
│           Agendamentos                  │
│                                         │
│  ┌───────────────────────────────────┐  │
│  │      Novo Agendamento       🐾    │  │
│  │                                   │  │
│  │  🐕 Nome do Pet                   │  │
│  │  [____________________________]   │  │
│  │                                   │  │
│  │  👤 Nome do Tutor                 │  │
│  │  [____________________________]   │  │
│  │                                   │  │
│  │  ✨ Serviço      📅 Data e Hora   │  │
│  │  [________▼]    [______________]  │  │
│  │                                   │  │
│  │         [ + Agendar ]             │  │
│  └───────────────────────────────────┘  │
│                                         │
│  Agenda do Dia          0 agendamentos  │
│                                         │
│  ┌───────────────────────────────────┐  │
│  │     🐾 Nenhum agendamento ainda   │  │
│  └───────────────────────────────────┘  │
│                                         │
│      Feito com 💜 para os amantes       │
└─────────────────────────────────────────┘
```

---

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais.

---

## 👨‍💻 Autor

Desenvolvido como desafio técnico de front-end.

---

<p align="center">
  Feito com 💜 para os amantes de pets
</p>
