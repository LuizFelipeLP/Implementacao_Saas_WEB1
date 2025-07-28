# Implementacao_Saas_WEB1
Desenvolvendo uma Página de Livros com SCSS
📚 Objetivo do Projeto
Este mini projeto tem como objetivo demonstrar a utilização do SCSS (Sass) para estilizar uma página web simples, focada na exibição de uma lista de livros. O principal intuito é ilustrar como o SCSS, um pré-processador CSS, pode otimizar e organizar o código de estilo através de recursos como variáveis, aninhamento e a compilação para CSS puro.

Ao final deste tutorial, você terá uma página web com um cabeçalho, uma seção de livros estilizada com um layout responsivo e um rodapé com informações dos desenvolvedores.

💻 Instalação dos Softwares Necessários
Para desenvolver este projeto, você precisará dos seguintes softwares:

Editor de Texto/IDE - Visual Studio Code (VS Code)

Por que: É um editor leve, gratuito e com uma vasta gama de extensões que facilitam o desenvolvimento web, incluindo suporte a SCSS.

Instalação: Baixe o instalador no site oficial e siga as instruções.

Node.js e npm (Node Package Manager):

Por que: O Sass é uma ferramenta que pode ser instalada globalmente via npm, o que nos permitirá compilar nossos arquivos SCSS para CSS.

Instalação: Baixe o instalador LTS (Long Term Support) no site oficial do Node.js. O npm é instalado junto com o Node.js.

Extensão Live Server (para VS Code):

Por que: Permite visualizar suas alterações no navegador em tempo real, sem precisar recarregar a página manualmente.

Instalação (no VS Code):

Abra o VS Code.

Vá para a aba de Extensões (ícone de quatro quadrados no menu lateral esquerdo ou Ctrl+Shift+X).

Procure por "Live Server" (Autor: Ritwick Dey).

Clique em "Install".

Sass (via npm):

Por que: É a ferramenta essencial para compilar seus arquivos .scss para .css.

Instalação (via Terminal/Prompt de Comando):

Abra o terminal ou prompt de comando (no VS CODE).

Execute o seguinte comando para instalar o Sass globalmente:
npm run observar
Isso permitirá que você veja comando sass em qualquer diretório.

🚀 Passo a Passo para o Desenvolvimento
Siga estes passos para recriar o projeto:

1. Estrutura do Projeto
Criamos uma pasta para o projeto e dentro dela, as seguintes subpastas e arquivos:

seu-projeto/
├── imagens/
│   ├── fundo.jpg
│   ├── l1.jpg
│   ├── l2.jpg
│   ├── l3.jpg
│   ├── l4.jpg
│   ├── alissin.png
│   ├── GALAS.PNG
│   ├── jacson.png
│   └── marelo.png
├── index.html
├── scss/
│   └── variaveis.scss
├── styles.scss
└── styles.css (Será gerado automaticamente pelo Sass)
imagens/: Guardará todas as imagens usadas na página. Certifique-se de ter essas imagens em sua pasta para que o projeto funcione corretamente.

index.html: O arquivo HTML principal da página.

scss/: Uma pasta para organizar arquivos SCSS parciais. Neste caso, variaveis.scss.

styles.scss: O arquivo SCSS principal onde está a maioria dos seus estilos.

styles.css: Este arquivo não deve ser criado manualmente. Ele será gerado pelo compilador Sass a partir do styles.scss.

2. Criando o index.html
Este arquivo define a estrutura da página, incluindo o cabeçalho, a seção de livros e o rodapé.

HTML

<!DOCTYPE html>
<html lang="pt-br">

<head>
    <title>Página Principal</title>
    <link rel="shortcut icon" href="imagens/fundo.jpg" type="image/x-icon">
    <link rel="stylesheet" href="styles.css" />
</head>

<body>
    <div class="cabecalho">
        <h1>Utilizando SCSS para estilizar a página de livros da BSI</h1>
        <h3>Esta página é voltada para mostrar LIVROS</h3>
    </div>
    <div class="biblioteca">
        <div class="livro">
            <img src="imagens/l1.jpg" alt="">
            <h2>Fundamentos de Desenvolvimento Web e Back-end</h2>
            <p>
                Fundamentos de Desenvolvimento Web e Back-end", da Editora Senac, é um guia prático sobre a
                infraestrutura
                que sustenta aplicações web. Com foco em soluções para o mercado, o livro aborda de forma objetiva a
                lógica,
                os bancos de dados e a arquitetura do lado do servidor. É ideal para iniciantes e profissionais que
                buscam
                uma base sólida para criar sistemas web eficientes.
            </p>
        </div>
        <div class="livro">
            <img src="imagens/l2.jpg" alt="">
            <h2>JavaScript & Jquery</h2>
            <p>
                JavaScript & JQuery: Desenvolvimento de Interfaces Web Interativas" é um guia famoso por ensinar
                programação
                de forma visual e intuitiva. Com um design colorido e infográficos, ele desmistifica os fundamentos do
                JavaScript e o uso da biblioteca JQuery para criar animações e interatividade em sites. É ideal para
                designers,
                iniciantes em programação e desenvolvedores front-end que preferem um aprendizado menos tradicional e
                mais
                prático.
                <hr>
            </p>
        </div>
        <div class="livro">
            <img src="imagens/l3.jpg" alt="">
            <h2>Estruturas De Dados</h2>
            <p>
                Estruturas de Dados" de Paulo Veloso é um livro clássico da computação brasileira, focado nos
                fundamentos da
                "programação não numérica". A obra apresenta as estruturas mais importantes como listas, árvores e
                grafos,
                sendo o resultado de anos de experiência em sala de aula dos autores. É um texto denso e formal, voltado
                para quem já possui conhecimentos básicos de programação e busca uma base teórica robusta.
            </p>
        </div>
        <div class="livro">
            <img src="imagens/l4.jpg" alt="">
            <h2>Plano de Carreira</h2>
            <p>
                Neste livro, Djalma de Oliveira adapta o planejamento estratégico empresarial para a gestão da carreira
                individual.
                Ele fornece um método prático para que o profissional defina seus objetivos, analise o mercado e trace
                metas para
                alcançar o sucesso. O objetivo é que você se torne o gestor de sua própria trajetória profissional de
                forma estruturada
                e planejada.
            </p>
        </div>
    </div>
    <div class="rodape">
        <div class="imagensRodape">
            <div class="integrante">
                <img src="imagens/marelo.png" alt="Gustavo">
                <span>GUSTAVO RODRIGUES MOREIRA</span>
            </div>
            <div class="integrante">
                <img src="imagens/jacson.png" alt="Jacson">
                <span>JACSON FRANCISCO VIANA SANTOS</span>
            </div>
            <div class="integrante">
                <img src="imagens/alissin.png" alt="Alisson">
                <span>ALISSON RICADY MORAIS GUIMÃRAES</span>
            </div>
            <div class="integrante">
                <img src="imagens/GALAS.PNG" alt="Felipe">
                <span>FELIPE PEREIRA DE LIMA</span>
            </div>
        </div>
    </div>
</body>

</html>
3. Definindo Variáveis com _variaveis.scss
No arquivo scss/_variaveis.scss (o underline _ indica que é um arquivo parcial e não será compilado diretamente para CSS), insira as variáveis Sass. Isso centraliza as definições de cores e fontes, facilitando futuras alterações.

SCSS

// variaveis
$fundo: rgb(36, 36, 87);
$texto-fora-da-div: rgb(173, 197, 209);
$cor-texto-dentro-da-div: #ff00a6;
$cor-rodape: rgb(36, 36, 87);
$cor-texto: #000000;
$fonte: 'Arial', sans-serif;
4. Escrevendo os Estilos com styles.scss
Agora, no arquivo styles.scss, você importará as variáveis e escreverá os estilos da sua página usando a sintaxe SCSS.

SCSS

// Importa as variáveis do arquivo _variaveis.scss
@import 'scss/variaveis';

body {
    background-color: $fundo;
    color: $texto-fora-da-div;
    background-size: cover;
    font-family: $fonte;
}

.cabecalho {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    flex-direction: column;
}

.biblioteca {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 20px;
    padding: 20px;
    margin: auto;

    .livro { // Aninhamento de seletores
        background-color: white;
        border: 1px solid #ccc;
        padding: 15px;
        border-radius: 10px;

        img {
            width: 100%;
            height: auto;
            border-radius: 5px;
        }

        h2 {
            color: $cor-texto-dentro-da-div; // Uso de variável
        }

        p {
            color: $cor-texto; // Uso de variável
        }
    }
}

.rodape {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    flex-direction: column;
    background-color: $cor-rodape; // Uso de variável
    padding: 20px;

    .imagensRodape { // Aninhamento de seletores
        display: flex;
        gap: 16px;
        justify-content: center;
        margin-top: 10px;

        .integrante { // Aninhamento de seletores
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 5px;
            font-size: 0.8em;
            color: $texto-fora-da-div; // Cor dos nomes

            img {
                width: 60px;
                height: 60px;
                border-radius: 50%;
                object-fit: cover;
                border: 2px solid $cor-texto-dentro-da-div; // Uso de variável
                box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
                transition: transform 0.2s;

                &:hover { // Exemplo de seletor aninhado e pseudoclasse
                    transform: scale(1.1);
                }
            }
        }
    }
}
Observações sobre o SCSS:

@import 'scss/variaveis';: Esta linha importa o arquivo de variáveis, tornando-as disponíveis em styles.scss.

.biblioteca .livro { ... }: Observe o aninhamento. No CSS puro, você teria .biblioteca .livro. Com SCSS, você pode aninhar o seletor .livro dentro de .biblioteca, refletindo a estrutura HTML e tornando o código mais legível.

color: $cor-texto-dentro-da-div;: As variáveis são usadas para definir as cores e a fonte, tornando o código mais fácil de manter.

5. Compilando o SCSS para CSS
Abra o terminal (ou prompt de comando) na raiz do seu projeto (na mesma pasta onde estão index.html e styles.scss).

Execute o seguinte comando para que o Sass observe as mudanças no styles.scss e o compile automaticamente para styles.css a cada alteração:

npm run observar
Indica ao Sass para "observar" o arquivo de origem e recompilá-lo a cada alteração.

styles.scss: O arquivo de origem SCSS.

styles.css: O arquivo de destino CSS que será gerado.

Você verá uma mensagem no terminal indicando que o Sass está observando os arquivos. Mantenha este terminal aberto enquanto estiver desenvolvendo.

6. Visualizando o Projeto
Com o sass npm run observar em execução e as imagens na pasta imagens/, você pode abrir o index.html no seu navegador.

Se estiver usando o VS Code, clique com o botão direito no arquivo index.html e selecione "Open with Live Server". Isso abrirá a página em seu navegador e atualizará automaticamente a cada modificação.

