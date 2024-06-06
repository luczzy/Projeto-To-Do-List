# **Projeto-To-Do-List**

## ``HTML``
O HTML estrutura a aplicação, definindo os elementos que compõem a interface do usuário.

**Formulários:** #todo-form para adicionar novas tarefas e #edit-form para editar tarefas existentes.
Toolbar: #toolbar contém a barra de pesquisa e o seletor de filtro.
Lista de Tarefas: #todo-list onde as tarefas são exibidas.

## ``CSS``
O CSS estiliza a aplicação, dando aparência e posicionamento aos elementos.

``Estilos principais:``

**Botões:** Estilização de botões para aparência consistente e interação com o usuário.
Formulários e Entradas: Estilização de formulários e campos de entrada.
Lista de Tarefas: Estilização das tarefas, diferenciando tarefas concluídas com a classe .done.

## ``JavaScript``
Esse código JavaScript cria uma aplicação de lista de tarefas interativa, permitindo adicionar, editar, remover, pesquisar e filtrar tarefas, com persistência usando o localStorage.

### ``Funções``

*saveTodo*
Essa função cria uma nova tarefa e a adiciona à lista de tarefas.

**Parâmetros:** text (texto da tarefa), done (estado de conclusão da tarefa), save (flag para salvar no localStorage).

**Criação do Elemento:** Cria uma div para a tarefa com botões de conclusão, edição e remoção.

``LocalStorage:`` Se a flag save estiver ativada, salva a tarefa no localStorage.

**Reset:** Limpa o campo de entrada após adicionar a tarefa.

*toggleForms*
Alterna a visibilidade entre o formulário de adição e o de edição.

*updateTodo*
Atualiza o texto de uma tarefa existente.

**Parâmetros:** text (novo texto da tarefa).
Busca e Atualização: Encontra a tarefa com o texto antigo (oldInputValue) e atualiza o texto.

*getSearchedTodos*
Filtra as tarefas com base no texto de pesquisa.

**Parâmetros:** search (texto de pesquisa).

**Filtro:** Mostra apenas as tarefas cujo título contém o texto de pesquisa.

*filterTodos*
Filtra as tarefas com base no estado (todas, feitas, a fazer).

**Parâmetros:** filterValue (valor do filtro).

**Filtro:** Mostra as tarefas de acordo com o filtro selecionado.

### **Eventos**
Adicionar Tarefa

**Evento:** Submit do formulário de adição.

**Ação:** Adiciona uma nova tarefa.

### **Manipulação de Tarefas**

**Evento:** Click em elementos do documento.

**Ações:** Alterna estado de conclusão, remove ou edita a tarefa.

### **Cancelar Edição**

**Evento:** Click no botão de cancelar edição.

**Ação:** Cancela a edição e volta ao formulário de adição.

### **Submeter Edição**

**Evento:** Submit do formulário de edição.

**Ação:** Atualiza a tarefa com o novo texto.

### **Pesquisa de Tarefas**

**Evento:** Digitação no campo de pesquisa.

**Ação:** Filtra as tarefas com base no texto de pesquisa.

### **Limpar Pesquisa**

**Evento:** Click no botão de apagar pesquisa.

**Ação:** Limpa o campo de pesquisa e refaz a pesquisa.

### **Filtro de Tarefas**

**Evento:** Mudança no seletor de filtro.

**Ação:** Filtra as tarefas com base no valor selecionado.

### **Local Storage**
Funções para interação com o localStorage, permitindo persistência das tarefas.

``getTodosLocalStorage``
Obtém as tarefas do localStorage.

``loadTodos``
Carrega as tarefas do localStorage ao iniciar a aplicação.

``saveTodoLocalStorage``
Salva uma nova tarefa no localStorage.

``removeTodoLocalStorage``
Remove uma tarefa do localStorage.

``updateTodoStatusLocalStorage``
Atualiza o estado de conclusão de uma tarefa no localStorage

``updateTodoLocalStorage``
Atualiza o texto de uma tarefa no localStorage.

``Inicialização``
Carrega as tarefas ao carregar a página.