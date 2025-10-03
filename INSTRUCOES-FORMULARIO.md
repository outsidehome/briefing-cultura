# 🏗️ Briefing de Cultura - Instruções Completas

## 📦 O QUE VOCÊ RECEBEU

Você tem em mãos um **formulário HTML completo e gamificado** para coletar o briefing de cultura organizacional da sua construtora!

### ✨ Características:

- ✅ **24 perguntas** divididas em 4 fases temáticas
- ✅ **Design profissional** e gamificado
- ✅ **Barra de progresso** visual
- ✅ **Responsivo** (funciona perfeitamente em celular)
- ✅ **Sistema de validação** (não deixa pular perguntas)
- ✅ **Animações suaves** entre fases
- ✅ **Coleta automática** de respostas
- ✅ **100% funcional** sem necessidade de servidor

---

## 🚀 COMO USAR

### OPÇÃO 1: Usar Localmente (Mais Simples)

1. **Abra o arquivo `briefing-construtora.html`** diretamente no navegador
2. Preencha o formulário
3. As respostas ficam salvas no navegador (localStorage)

**Vantagens:**
- Funciona imediatamente
- Não precisa de internet
- Não precisa de hospedagem

**Desvantagens:**
- Só você pode acessar no seu computador
- Não envia as respostas automaticamente

---

### OPÇÃO 2: Hospedar Online (Recomendado para Clientes)

Para que seu cliente possa acessar via link, você precisa hospedar o arquivo. Aqui estão as opções **GRATUITAS**:

#### **A) Netlify Drop (Mais Fácil)**

1. Acesse [https://app.netlify.com/drop](https://app.netlify.com/drop)
2. Arraste o arquivo `briefing-construtora.html` para a área indicada
3. Aguarde o upload
4. Copie o link gerado (ex: `https://seu-site.netlify.app`)
5. Envie o link para seu cliente!

**Tempo:** 2 minutos  
**Custo:** Gratuito  
**Validade:** Permanente

---

#### **B) GitHub Pages (Mais Profissional)**

1. Crie uma conta no [GitHub](https://github.com) (se não tiver)
2. Crie um novo repositório público
3. Faça upload do arquivo `briefing-construtora.html`
4. Vá em Settings → Pages
5. Ative o GitHub Pages
6. Seu link será: `https://seu-usuario.github.io/nome-do-repo/briefing-construtora.html`

**Tempo:** 5 minutos  
**Custo:** Gratuito  
**Validade:** Permanente

---

#### **C) Vercel (Mais Rápido)**

1. Acesse [https://vercel.com](https://vercel.com)
2. Faça login com GitHub
3. Clique em "New Project"
4. Faça upload do arquivo
5. Deploy automático!

**Tempo:** 3 minutos  
**Custo:** Gratuito  
**Validade:** Permanente

---

## 📊 COMO COLETAR AS RESPOSTAS

O formulário atual salva as respostas no **localStorage** do navegador. Para enviar as respostas para você, existem 3 opções:

### **OPÇÃO 1: Usar Formspree (Mais Simples)**

1. Acesse [https://formspree.io](https://formspree.io)
2. Crie uma conta gratuita
3. Crie um novo formulário
4. Copie o endpoint (ex: `https://formspree.io/f/XXXXX`)
5. Edite o arquivo HTML na linha onde está o comentário `// Opcional: Enviar para um endpoint`
6. Substitua por:

```javascript
fetch('https://formspree.io/f/SEU_ID', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify(responses)
}).then(() => {
    alert('Respostas enviadas com sucesso!');
});
```

**Resultado:** Você recebe as respostas por email automaticamente!

---

### **OPÇÃO 2: Usar Google Sheets (Mais Organizado)**

1. Use o serviço [SheetDB](https://sheetdb.io/) ou [Sheet.best](https://sheet.best/)
2. Conecte com uma planilha do Google Sheets
3. Copie a API URL
4. Adicione no código conforme instruções do serviço

**Resultado:** Respostas vão direto para uma planilha!

---

### **OPÇÃO 3: Pedir para o Cliente Copiar (Mais Manual)**

1. Adicione um botão "Copiar Respostas" no final
2. O cliente copia e cola em um email para você

**Código para adicionar:**

```javascript
// Adicionar após o submit
const copyButton = document.createElement('button');
copyButton.textContent = 'Copiar Respostas';
copyButton.onclick = () => {
    const text = JSON.stringify(responses, null, 2);
    navigator.clipboard.writeText(text);
    alert('Respostas copiadas! Cole em um email para nós.');
};
document.querySelector('.completion').appendChild(copyButton);
```

---

## 🎨 PERSONALIZAR O FORMULÁRIO

### Mudar as Cores:

Edite o arquivo HTML nas linhas de CSS:

```css
/* Cor do cabeçalho */
background: linear-gradient(135deg, #003366 0%, #004d99 100%);

/* Cor da barra de progresso */
background: linear-gradient(90deg, #00C853 0%, #00E676 100%);

/* Cor dos botões */
background: linear-gradient(135deg, #FF9900 0%, #FFB84D 100%);
```

### Adicionar Logo da Construtora:

Adicione dentro do `<div class="header">`:

```html
<img src="logo-construtora.png" alt="Logo" style="max-width: 200px; margin-bottom: 20px;">
```

### Mudar Textos:

Todos os textos estão em português e podem ser editados diretamente no HTML.

---

## 📱 COMPARTILHAR COM O CLIENTE

### Mensagem Sugerida:

```
Olá! 👋

Preparamos uma experiência especial para mapear o DNA da sua construtora.

🎮 É um briefing gamificado dividido em 4 fases
⏱️ Leva apenas 15-20 minutos
🎯 Suas respostas vão gerar o Manual de Cultura

Link: [SEU_LINK_AQUI]

Seja sincero nas respostas - não existe certo ou errado!

Vamos construir algo incrível juntos! 🚀
```

---

## 🔧 SOLUÇÃO DE PROBLEMAS

### O formulário não abre?
- Certifique-se de que o arquivo tem extensão `.html`
- Tente abrir com Chrome, Firefox ou Edge
- Clique com botão direito → Abrir com → Navegador

### As respostas não estão sendo salvas?
- Verifique se o JavaScript está habilitado no navegador
- Abra o Console (F12) e veja se há erros

### O cliente não consegue acessar o link?
- Verifique se o arquivo foi hospedado corretamente
- Teste o link em modo anônimo do navegador
- Certifique-se de que o link está completo (com https://)

---

## 📈 PRÓXIMOS PASSOS

Após coletar as respostas:

1. **Analise os dados** das 20 perguntas de escala (média por fase)
2. **Identifique padrões** nos valores, operações e marca
3. **Use as 4 respostas abertas** como base para o Manual de Cultura
4. **Crie o Manual** seguindo a estrutura dos PDFs de referência (RNO)

---

## 🎁 BÔNUS: Análise Automática

Quer analisar as respostas automaticamente? Adicione este código no final do JavaScript:

```javascript
function analyzeResponses(responses) {
    // Calcular médias por fase
    const fase1 = ['q1', 'q2', 'q3', 'q4', 'q5', 'q6', 'q7'];
    const fase2 = ['q8', 'q9', 'q10', 'q11', 'q12', 'q13', 'q14'];
    const fase3 = ['q15', 'q16', 'q17', 'q18', 'q19', 'q20'];
    
    const calcMedia = (questions) => {
        const sum = questions.reduce((acc, q) => acc + parseInt(responses[q] || 0), 0);
        return (sum / questions.length).toFixed(2);
    };
    
    console.log('Força dos Valores:', calcMedia(fase1));
    console.log('Eficiência das Operações:', calcMedia(fase2));
    console.log('Percepção de Marca:', calcMedia(fase3));
}
```

---

## 💡 DICAS PROFISSIONAIS

1. **Teste você mesmo** antes de enviar para o cliente
2. **Envie em horário comercial** para melhor taxa de resposta
3. **Faça follow-up** após 2-3 dias se não responder
4. **Ofereça ajuda** se o cliente tiver dúvidas
5. **Agradeça** após o preenchimento

---

## 🆘 PRECISA DE AJUDA?

Se tiver qualquer dúvida ou problema:

1. Verifique se seguiu todos os passos
2. Teste em outro navegador
3. Verifique a conexão com internet (se hospedado)
4. Entre em contato comigo para suporte

---

## ✅ CHECKLIST FINAL

Antes de enviar para o cliente:

- [ ] Testei o formulário do início ao fim
- [ ] Todas as 24 perguntas estão corretas
- [ ] O formulário está hospedado e acessível
- [ ] Configurei o sistema de coleta de respostas
- [ ] Personalizei cores/logo (opcional)
- [ ] Testei em celular
- [ ] Preparei a mensagem para o cliente
- [ ] Tenho um plano de follow-up

---

## 🎉 PRONTO!

Seu formulário está 100% funcional e pronto para uso!

Boa sorte com o projeto do Manual de Cultura! 🚀🏗️
