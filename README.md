🧮 Calculadora Win32 em C

Uma calculadora simples com interface gráfica para Windows, desenvolvida em C usando a API do Windows (Win32), sem nenhuma biblioteca externa. O projeto é ótimo para quem está começando a estudar programação de interfaces gráficas nativas.

✨ Funcionalidades
➕ Soma
➖ Subtração
✖️ Multiplicação
➗ Divisão (com proteção contra divisão por zero)
🧹 Botão Limpar para apagar os campos
🚪 Botão Sair para encerrar o programa
⚠️ Validação de campos vazios com mensagem de aviso
Resultado exibido em uma caixa de diálogo com 2 casas decimais
🖼️ Interface

A janela possui:

Título CALCULADORA
Dois campos de texto (Número 1 e Número 2)
Quatro botões de operação (Somar, Subtrair, Multiplicar, Dividir)
Dois botões de controle (Limpar e Sair)
Janela de tamanho fixo (450 x 300), sem botão de maximizar
<!-- Adicione aqui um print da aplicação: ![Screenshot](docs/screenshot.png) -->
🛠️ Tecnologias utilizadas
Linguagem C
Win32 API (windows.h)
Compilador GCC (MinGW) ou MSVC
📁 Estrutura do projeto
.
├── calculadora.c   # Código-fonte completo
└── README.md
⚙️ Como compilar e executar
Pré-requisitos
Windows
MinGW-w64 (GCC) ou Visual Studio / Build Tools
Com GCC (MinGW)
bash
gcc calculadora.c -o calculadora.exe -mwindows

A flag -mwindows evita que uma janela de console seja aberta junto com a aplicação.

Com MSVC (Prompt de Comando do Desenvolvedor)
bash
cl calculadora.c user32.lib gdi32.lib
Executando
bash
calculadora.exe
Code::Blocks / Dev-C++

Crie um projeto do tipo Win32 GUI Project, adicione o arquivo calculadora.c e compile normalmente.

🧠 Como o código funciona
Parte	Descrição
WinMain	Ponto de entrada:

registra a classe da janela, cria a janela principal e executa o laço de mensagens
WindowProcedure	Trata os eventos da janela (WM_CREATE, WM_COMMAND, WM_DESTROY)
WM_CREATE	Cria todos os controles (rótulos, campos de texto e botões)
WM_COMMAND	Identifica qual botão foi clicado através do ID e chama a função correspondente
somar, subtrair, multiplicar, dividir	Leem os campos, validam, convertem com atof(), calculam e exibem o resultado com MessageBox
limparCampos	Limpa o conteúdo dos dois campos de texto
Fluxo de uma operação
O usuário digita dois números.
Ao clicar em um botão, o WM_COMMAND é disparado.
A função lê os textos com GetWindowText.
Se algum campo estiver vazio, um aviso é exibido.
Os textos são convertidos para número com atof.
A operação é realizada e o resultado é mostrado com MessageBox.
📚 Conceitos aprendidos neste projeto
Registro de classe de janela (WNDCLASS / RegisterClass)
Criação de janelas e controles (CreateWindow)
Laço de mensagens (GetMessage, TranslateMessage, DispatchMessage)
Tratamento de eventos com switch em WindowProcedure
Leitura e escrita em controles (GetWindowText, SetWindowText)
Caixas de mensagem (MessageBox)
🚧 Limitações conhecidas e melhorias futuras
 Usar double em vez de float para maior precisão
 Validar entrada para aceitar apenas números (ES_NUMBER ou filtro personalizado)
 Exibir o resultado na própria janela (em vez de MessageBox)
 Refatorar as quatro funções de operação em uma única função
 Adicionar suporte a Unicode (wchar_t / UNICODE)
 Exibir acentos corretamente em todos os ambientes (salvar o arquivo em ANSI/Windows-1252 ou usar Unicode)
 Adicionar suporte ao teclado (Enter, atalhos)
🤝 Contribuindo

Este projeto está sob a licença MIT. Sinta-se livre para usar, estudar e modificar.

Desenvolvido por [Seu Nome] — github.com/seu-usuario

⭐ Se este projeto te ajudou, deixe uma estrela no repositório!
