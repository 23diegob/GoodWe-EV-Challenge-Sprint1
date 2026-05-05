# GoodWe EV Search - Sprint 1 (EV Challenge 2026)

## 👥 Integrantes
* Lucca Bertolini - RM: 569552
* Diego de Oliveira Brandão - RM: 569773
* Raphaello Caffettani - RM: 572334
* Cristhian Henrique Clementino - RM: 574117
* Fabio Pena Vieira - RM: 570441

## 📝 Problema Abordado
No contexto do **EV Challenge 2026**, identificamos que a expansão da eletromobilidade enfrenta um gargalo crítico: a gestão eficiente da infraestrutura de recarga. Atualmente, faltam mecanismos integrados para orquestrar potência e gerenciar o uso compartilhado, especialmente em ambientes complexos como condomínios. O problema central é a dificuldade de comunicação entre o hardware (eletroposto) e o usuário final/gestor, resultando em subutilização ou falhas operacionais.

## 🤖 Proposta do Chatbot: "GoodWe EV ChargeOps Assistant"
Nosso chatbot foi desenvolvido com foco na persona **Síndico/Gestor de Condomínio** (Foco: *EV ChargeOps*).
A solução visa automatizar o suporte técnico de primeiro nível, facilitar a gestão de reservas de carga e orientar sobre o faturamento e ciclos de uso dos moradores, reduzindo a carga operacional humana.

### Justificativa da Persona:
Escolhemos o cenário condominial pois é onde ocorre o maior conflito de uso de potência e necessidade de regras claras de rateio, tornando o chatbot uma ferramenta essencial para a harmonia e eficiência do sistema.

## 🛠 Tecnologias Selecionadas
* **Linguagem:** Python
* **Modelo de IA:** Gemini 1.5 Pro (Google) via API.
* **Justificativa:** O Gemini oferece uma janela de contexto ampla para processar manuais de instalação e regras de condomínio, além de possuir integração nativa e eficiente com o ambiente de desenvolvimento utilizado.
* **Ferramentas:** Google Colab para prototipagem e Mermaid.ai para modelagem de processos.

## 📊 Fluxograma de Funcionamento
O fluxo lógico consiste em:
1.  **Entrada:** Usuário envia dúvida (ex: "Como cadastro um novo morador?").
2.  **Processamento:** O System Prompt condiciona o LLM ao contexto GoodWe.
3.  **Saída:** Resposta técnica estruturada e contextualizada.

[Link para o Fluxograma Interativo](COLOQUE_AQUI_O_SEU_LINK_DO_MERMAID)

---

## 🧠 System Prompt (Contexto-Base)
*Este é o prompt que configura o comportamento da IA:*

> "Você é o 'GoodWe EV Assistant', um especialista técnico e operacional em soluções de carregamento elétrico da GoodWe, especificamente no módulo EV ChargeOps para condomínios. Sua missão é auxiliar síndicos e administradores. 
> 
> Suas diretrizes são:
> 1. Seja profissional, técnico e resolutivo.
> 2. Se o assunto for sobre orquestração de potência, explique que o sistema prioriza a segurança da rede elétrica do prédio.
> 3. Se for sobre faturamento, oriente sobre a extração de relatórios de ciclos de recarga.
> 4. Nunca forneça informações fora do contexto de mobilidade elétrica da GoodWe.
> 5. Caso não saiba uma resposta técnica específica, oriente o usuário a abrir um chamado no portal oficial GoodWe."

---

## 🧪 Modelo de Teste (Avaliação)
Abaixo, os cenários de teste para validar a consistência do modelo na Sprint 2:

| Pergunta do Usuário | Resposta Esperada (Ideal) |
| :--- | :--- |
| Como faço para limitar a potência de um carregador no horário de pico? | Você deve acessar o painel de Orquestração de Potência no ChargeOps e definir o teto de kW para o horário desejado, visando evitar sobrecarga. |
| Um morador novo chegou, como registro o ciclo dele? | O registro é feito vinculando a TAG RFID do morador ao CPF dele no sistema, permitindo o rastreio individual de cada kWh consumido. |
| O carregador está com uma luz vermelha piscando, o que fazer? | Verifique o código de erro no manual. Geralmente, indica falta de aterramento ou falha de comunicação. Recomendo reiniciar o disjuntor ou contatar um técnico. |
| Como é feito o faturamento das recargas no final do mês? | O sistema gera um relatório CSV com o consumo total por unidade. Esses dados podem ser integrados à planilha de custos do condomínio para rateio. |
| O chatbot pode me ajudar a comprar um carro elétrico? | Sinto muito, sou um assistente especializado na gestão de carregadores GoodWe. Para compra de veículos, recomendo procurar uma concessionária autorizada. |
