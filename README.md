# 📑 Facilitador Contábil - Organização para IRPF

Este projeto consiste em uma aplicação desenvolvida em Microsoft Excel, voltada para a área contábil. O objetivo principal é facilitar a coleta e organização de dados para a declaração do Imposto de Renda Pessoa Física (IRPF), oferecendo uma interface limpa, intuitiva e segura contra erros de preenchimento.

O foco do desenvolvimento foi a experiência do usuário, utilizando navegação por menus e formulários com validações robustas.

---

## 📸 Galeria do Projeto

Abaixo, uma visão geral das principais telas da aplicação.

### 1. Menu Principal
A porta de entrada da aplicação, com navegação centralizada e identidade visual.
![Tela do Menu Principal](images/print_menu.png)

### 2. Planilha Titular (Dados Pessoais)
Formulário para preenchimento de dados cadastrais com máscaras de entrada.
![Tela da Planilha Titular](images/print_titular.png)

### 3. Planilha Informes (Financeiro)
Controle de saldos bancários com seleção validada de instituições.
![Tela da Planilha Informes](images/print_informes.png)

### 4. Planilha Notas (Despesas)
Registro simples e direto de entradas e despesas dedutíveis.
![Tela da Planilha Notas](images/print_notas.png)

### 5. Planilha Tabelas (Apoio Oculto)
Base de dados auxiliar para validações (esta planilha fica oculta para o usuário final).
![Tela da Planilha Tabelas de Apoio](images/print_tabelas.png)

---

## 🛠️ Estrutura e Funcionalidades Técnicas

O projeto foi estruturado para se comportar como um "sistema", ocultando a interface padrão do Excel (linhas de grade, títulos, barra de fórmulas e guias de planilha) para focar no conteúdo.

### 🏠 Menu Principal
* **Identidade Visual:** O logo principal (criado via IA Gemini) foi inserido na célula A1 com a propriedade "Não mover ou dimensionar com células" habilitada, garantindo que a identidade visual permaneça intacta mesmo se houver ajuste de colunas.
* **Navegação:** Botões interativos criados a partir de formas levam o usuário às planilhas TÍTULAR, INFORMES e NOTAS através de hiperlinks.
* **Rodapé Interativo:** Assinatura contendo uma logo pessoal, com link direcionando para o perfil profissional.

### 👤 Planilha TÍTULAR
Destinada aos dados cadastrais. O foco aqui foi a integridade do dado inserido.
* **Campos:** Nome, CPF, Nascimento, Título de Eleitor, Cônjuge, Rua, Rua Abreviada, CEP, Contatos (Telefone, Celular, E-mail) e questões fiscais.
* **Máscaras de Entrada:** Implementadas nos campos CPF, CEP, Telefone, Celular e E-mail para garantir a padronização do formato.
* **Validação de Dados (Lista):** As perguntas finais ("Houve alterações...", "Dependente Cônjuge", "Residente do Exterior") possuem validação restrita às opções "SIM" e "NÃO", evitando respostas ambíguas.

### 💰 Planilha INFORMES
Focada em saldos e investimentos.
* **Validação Cruzada:** A coluna "BANCO" possui uma validação de dados em lista. Ela busca as informações diretamente da planilha de apoio "TABELAS".
* **Alerta de Erro:** Caso o usuário tente digitar um banco que não esteja na lista pré-definida, o sistema exibe um alerta de erro impeditivo.

### 📝 Planilha NOTAS
Tabela simples para lançamento de despesas.
* **Formatação:** Coluna de DATA com máscara (dd/mm/aa) e coluna VALOR com formatação contábil/moeda.

### ⚙️ Planilha TABELAS (Apoio)
Esta é a estrutura de "backend" da planilha. Ela contém a lista dos bancos utilizados na validação da planilha INFORMES. Ela permanece **oculta** para manter a interface limpa e evitar alterações acidentais nos dados base.

---

## 🧩 UX e Navegação
* **Foco no Usuário:** Para melhorar a visualização e a sensação de "aplicativo", foram ocultadas as guias das planilhas, linhas de grade, títulos e barras de fórmulas.
* **Navegação Fluida:** Todas as planilhas de interação contam com botões de navegação claros para retornar ao Menu ou acessar áreas relacionadas.

---
**Desenvolvido por Philipe Daryl**
