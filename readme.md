# Data Pro - Análise Fácil

## 📋 Descrição

Plataforma web para análise de dados sem necessidade de conhecimento técnico. Processa arquivos parquet nativamente e exporta dados de forma escalável com preview rápido.

## 🛠️ Tecnologias Utilizadas

### Frontend
- **HTML5** - Estrutura semântica
- **Tailwind CSS** - Framework CSS utilitário para estilização responsiva
- **JavaScript Vanilla** - Interatividade e manipulação do DOM

### Email
- **EmailJS** - Serviço para envio de emails sem backend próprio
  - Dashboard: https://dashboard.emailjs.com
  - Service ID: `data_pro_teste`
  - Template ID: `template_u6ayiv8`
  - Public Key: `stwDVCTq62ZDOQqpY`

## 📁 Estrutura do Projeto

```
c:\dev\data-pro\
├── index.html              # Arquivo principal
├── assets/                 # Pasta com recursos
│   ├── icon.png           # Ícone da aplicação
│   ├── hero.jpg           # Imagem do hero
│   ├── section1.jpg       # Imagem da seção
│   ├── woman.jpg          # Imagem decorativa
│   └── logo.png           # Logo da marca
└── README.md              # Este arquivo
```

## 🎨 Tailwind CSS

O Tailwind CSS é um framework CSS utilitário carregado via CDN:

```html
<script src="https://cdn.tailwindcss.com"></script>
```

**Classes principais utilizadas:**
- `grid` / `grid-cols-1` / `lg:grid-cols-2` - Layouts responsivos
- `flex` / `justify-between` / `items-center` - Flexbox
- `max-w-6xl` / `mx-auto` - Limitadores de largura e centralização
- `py-24` / `px-6` - Padding/Espaçamento
- `bg-white` / `text-white` - Cores
- `rounded-xl` / `shadow` - Bordas e sombras
- `md:hidden` / `md:border-r` - Responsividade

## 📧 Como Funciona o Envio de Email

### 1. **Inicialização**
```javascript
emailjs.init("stwDVCTq62ZDOQqpY");
```

### 2. **Captura do Formulário**
Quando o usuário clica em "Solicitar Demonstração", o formulário é capturado:
- Nome
- Email
- Empresa
- Setor

### 3. **Envio via EmailJS**
```javascript
emailjs.send("data_pro_teste", "template_u6ayiv8", templateParams)
```

### 4. **Resposta Visual**
- ✅ Loading spinner enquanto envia
- ✅ Notificação toast (sucesso ou erro)
- ✅ Botão desabilitado para evitar múltiplos cliques

### 5. **Dashboard EmailJS**
Para gerenciar templates e visualizar logs de envio, acesse:
- **URL**: https://dashboard.emailjs.com
- **Faça login** com suas credenciais
- **Abra o Service** `data_pro_teste`
- **Edite o Template** `template_u6ayiv8` conforme necessário

## 🚀 Como Usar

1. Abra `index.html` em seu navegador
2. Navegue pelos diferentes botões de CTA (Call To Action)
3. Preencha o formulário "Solicitar Demonstração"
4. Você receberá uma notificação de confirmação
5. O email será enviado para o endereço configurado no EmailJS

## ✨ Recursos Implementados

- ✅ Hover com animação nos botões
- ✅ Efeito ripple ao clicar
- ✅ Loading spinner durante envio
- ✅ Notificação toast responsiva
- ✅ Design responsivo (mobile, tablet, desktop)
- ✅ Menu mobile funcional

## 📱 Responsividade

O Tailwind CSS garante responsividade automática com breakpoints:
- Mobile: padrão
- Tablet (md): 768px+
- Desktop (lg): 1024px+

## 🔧 Como Configurar EmailJS

1. Acesse https://dashboard.emailjs.com
2. Crie uma conta ou faça login
3. Conecte um serviço de email (Gmail, Outlook, etc.)
4. Crie um template com as variáveis: `nome`, `email`, `empresa`, `setor`
5. Copie seu **Public Key**, **Service ID** e **Template ID**
6. Atualize os valores no código `index.html`

## 📝 Licença

© 2025 Data Pro – Todos os direitos reservados