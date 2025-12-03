# 💸 App de Finanças Pessoais do Joaquim, com Vibe Coding.

PRD Refinado no Gemini

```markdown
# PRD: App de Finanças via Conversa (Versão Final e Corrigida)

## 1. Visão do Produto
Criar o aplicativo de Organização de Finanças Pessoais mais simples e natural do mercado, transformando o tedioso controle de gastos em uma conversa leve e educativa. O produto visa desmistificar as finanças e capacitar iniciantes a alcançar a estabilidade financeira sem esforço manual.

## 2. Público-Alvo (Foco na Vibe)
* Perfil: Iniciantes em finanças, pessoas que odeiam planilhas, usuários que buscam praticidade.
* Foco na Vibe: Usuários que precisam de um guia amigável, não de um auditor financeiro.

## 3. Funcionalidades-Chave (Priorizadas e Estruturais)

3.1. Autenticação e Gestão de Usuário: Implementar um sistema de cadastro (Sign-up) e login (Sign-in) robusto, utilizando e-mail e senha. Cada transação e meta deve estar obrigatoriamente vinculada a um User_ID. O onboarding deve ser conversacional e rápido.
3.2. Registro e Classificação Natural de Transações:
    * Registro via Chat (Core): Capacidade de registrar despesas e receitas em linguagem natural.
    * Tratamento de Receitas: Receitas devem ser categorizadas e tratadas como categoria de saldo positivo, separada das despesas.
    * Classificação Automática: O sistema deve sugerir categorias para despesas e receitas.
3.3. Agente Financeiro Inteligente (Lógica de Negócio): A IA deve responder a consultas que exigem cálculo e contexto dos dados (Ex: "Quanto preciso economizar para minha meta?"). Dicas Proativas baseadas no histórico.
3.4. Metas e Acompanhamento Conversacional: Permite que o usuário defina metas e receba updates e incentivos diários via chat sobre o progresso.
3.5. Relatórios Visuais e Estruturados: Visualização Clara de dados (Ex: Pizza para distribuição de gastos). O relatório deve sempre apresentar Receita e Despesa de forma distinta.

## 4. Princípios de Design e Arquitetura

* Design Universal e Inclusivo: Utilizável por pessoas de todas as habilidades, com alto contraste e uso mínimo de jargões técnicos.
* Controle de Tema (Dark Mode): Opção de alternar para o Tema Escuro.
* Arquitetura de Dados: Requer um backend com base de dados relacional para gerenciar o relacionamento entre Usuário, Transação e Categoria.
* Conversa como Interface: A interação primária é o chat.

## 5. Plano de MVP (Mínimo Produto Viável)

* Critério de Sucesso: Taxa de retenção de 7 dias acima de 40%.
* Telas Essenciais: Tela de Login/Cadastro, Tela Principal/Chat e Tela de Relatório Simplificado.
* Funcionalidades Mínimas:
    * Autenticação Básica (e-mail/senha).
    * Registro via Chat para Receitas e Despesas simples.
    * Classificação de categorias de forma automática (para despesas E receitas).
    * Agente Financeiro com Lógica de Resposta Contextual: A IA deve ser capaz de consultar os dados do usuário para responder a pelo menos 3 perguntas contextuais usando o tom de voz definido.



# Persona do Agente Financeiro: O Analista

## 1. Dados da Persona

* Nome/Função: O Analista (Ou simplesmente o Assistente).
* Arquétipo: O Conselheiro Sábio / O Professor Calmo.
* Personalidade: Factual, Objetivo, Calmo e Extremamente Confiável. Foca em dados e tendências.
* Missão: Oferecer clareza financeira por meio de fatos e insights.
* Valor Central: Acreditamos na autonomia do usuário, baseada em dados transparentes.

## 2. Tom de Voz (Diretrizes)

* Formalidade: Acessível, mas com respeito (usa "você" com maturidade).
* Atitude: Factual, calmante, focado em ação e correção.
* Linguagem: Objetiva, usando termos financeiros apenas quando necessário e explicando-os.

## 3. Diretrizes Práticas de Interação

* Registro de Transação: “Transação registrada: R$200,00 em Lazer. O saldo atual da categoria está em [R$XX,XX]. Posso te ajudar com algo mais?”
* Alerta de Alto Gasto (Crítico): “Alerta de Tendência: Seu gasto na categoria Lazer está 30% acima da média histórica deste mês. Sugestão: Gostaria de reavaliar o restante do orçamento desta categoria para o fechamento do mês?”
* Sucesso e Encorajamento: “Excelente progresso! Você está 5% abaixo da meta de gastos definida para este período. Se mantivermos este ritmo, o prazo para atingir [Nome da Meta] pode ser antecipado.”

```
Interações com o Google AI Studio
1.
	Adicionar a funcionalidade de alterar categorias e remover despesa, conforme a solicitação do usuário.
	Ao pedir dicas sobre otimização de gastos em uma categoria específica, o assistente repete a informação de quanto foi o gasto com aquela categoria no mês, isso torna o texto excessivamente longo e repetitivo.
	Ao passar o mouse sobre o gráfico, na aba relatórios, não é possível ver valor nenhum, apenas uma caixa preta.
	Ainda sobre o gráfico, mude para um gráfico de barras.
2.
	Renomeado para "Sage".
	Atualizada a função analyzeMessage para aceitar history.
	O Prompt agora inclui o histórico das últimas 6 mensagens para entender o contexto (perguntas e respostas).
	Instrução específica adicionada: Se o usuário estiver respondendo a uma pergunta sobre metas, classificar como GOAL ou pedir confirmação, nunca registrar transação direta sem certeza.

Prints de interação
<img width="1351" height="710" alt="image" src="https://github.com/user-attachments/assets/b6a283fd-a1ec-4def-bca1-4f05ba6212ca" />
<img width="1363" height="796" alt="image" src="https://github.com/user-attachments/assets/7a47fd28-b0f6-4d4e-99b8-7555365c938d" />
<img width="1338" height="570" alt="image" src="https://github.com/user-attachments/assets/6dd5d544-54f8-4fdf-af18-023359c6d15a" />

Resumo do App
  *O aplicativo possui um assistente que registra receita e despesa, além de fornecer dicas de gerenciamento financeiro, gestão de metas e etc.
  *Na aba de relatórios temos acesso a parte gráfica, que mostra quanto temos, quanto gastamos, um grafico com as despesas agrupadas por categoria.
  *Registro das transações
  *Metas financeiras, onde você pode adicionar manualmente ou via chat
  *É possível renoomear categorias, via chat ou manualmente. Inserir ou remover fundos nas metas financeiras

Link da aplicação:
https://ai.studio/apps/drive/1g3XbSnt17Cw0-1XaSB0-LgUg0yI5beXP?fullscreenApplet=true
  
Reflexão sobre o processo:
  - Foi bem fluído o processo de criação do código através do chat com a IA.
  - A primeira preview no lovable ficou bem ruim, tive que procurar outro lugar pra fazer o vibe coding (Fiz no google AI studio).
  - Exercitei um pouco de engenharia de prompt no processo, foi bem produtivo.

