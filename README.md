Implementacao_Sass_WEB1
🚀 Visão Geral do Projeto
Este projeto demonstra a aplicação prática do SCSS (Sass) para estilizar uma página web simples dedicada à exibição de livros. Nosso principal objetivo é ilustrar como o SCSS, um pré-processador CSS poderoso, pode otimizar o fluxo de trabalho de desenvolvimento web, promovendo código mais organizado, reusável e fácil de manter através de recursos como variáveis, aninhamento de seletores e compilação automatizada para CSS puro.

Ao final deste tutorial, você terá uma página web visualmente atraente, com um cabeçalho dinâmico, uma seção de livros estilizada com um layout responsivo e um rodapé informativo com os integrantes do projeto.

🛠️ Tecnologias Utilizadas
Este projeto foi desenvolvido utilizando as seguintes tecnologias e ferramentas:

HTML5: Para a estruturação semântica do conteúdo da página.

SCSS (Sass): Como pré-processador CSS para uma estilização mais avançada e organizada.

CSS3: O resultado final da compilação do SCSS, aplicado ao HTML.

Node.js e npm: Para gerenciar as dependências do projeto e rodar o compilador Sass.

Visual Studio Code (VS Code): Editor de código principal.

Live Server (Extensão VS Code): Para visualização em tempo real das alterações no navegador.

💻 Instalação e Configuração do Ambiente
Para replicar e desenvolver neste projeto, siga os passos de instalação e configuração abaixo:

1. Editor de Texto/IDE
Ferramenta: Visual Studio Code (VS Code)

Motivo: É um editor de código leve, gratuito e altamente extensível, oferecendo excelente suporte para desenvolvimento web, incluindo SCSS.

Instalação: Baixe o instalador diretamente do site oficial do VS Code e siga as instruções para o seu sistema operacional.

2. Node.js e npm (Node Package Manager)
Motivo: O Sass é distribuído como um pacote npm. A instalação do Node.js já inclui o npm, que é essencial para instalar e gerenciar o compilador Sass.

Instalação: Faça o download do instalador da versão LTS (Long Term Support) no site oficial do Node.js. Execute o instalador e siga as etapas. Verifique a instalação abrindo o terminal e digitando node -v e npm -v.

3. Extensão Live Server (para VS Code)
Motivo: Essa extensão permite que você visualize as mudanças no navegador em tempo real enquanto edita seu código, sem a necessidade de recarregar a página manualmente.

Instalação (no VS Code):

Abra o VS Code.

Vá para a aba de Extensões (ícone de quatro quadrados no menu lateral esquerdo ou use o atalho Ctrl+Shift+X).

Na barra de pesquisa, digite "Live Server" e selecione a extensão do Ritwick Dey.

Clique no botão "Install".

4. Sass (via npm)
Motivo: O Sass é o compilador que transforma seus arquivos .scss em CSS padrão, que é o que o navegador entende.

Instalação (via Terminal/Prompt de Comando):

Abra o terminal integrado do VS Code (Ctrl+' ou View > Terminal) ou o terminal do seu sistema operacional.

Execute o seguinte comando para instalar o Sass globalmente:

Bash

npm install -g sass
Este comando tornará o comando sass disponível em qualquer diretório do seu sistema.

🚀 Passo a Passo para o Desenvolvimento
Siga as etapas abaixo para configurar e desenvolver o mini projeto.

1. Estrutura do Projeto
Comece criando a seguinte estrutura de diretórios e arquivos em seu ambiente de desenvolvimento:

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
├── scss/
│   └── _variaveis.scss  (O underline indica um parcial Sass)
├── index.html
├── styles.scss
└── styles.css           (Gerado automaticamente pelo Sass)
imagens/: Contém todas as imagens usadas no projeto, como capas de livros e fotos dos integrantes. Certifique-se de que todas as imagens referenciadas no index.html e no CSS estejam presentes aqui.

scss/: Esta pasta é dedicada aos arquivos parciais SCSS. O _variaveis.scss é um exemplo de parcial, contendo variáveis globais de estilo.

index.html: O arquivo principal da página web, que carrega a estrutura HTML e referencia o styles.css compilado.

styles.scss: O arquivo SCSS principal onde você escreverá a lógica de estilização, importando parciais e utilizando os recursos do Sass.

styles.css: Este arquivo não deve ser criado ou editado manualmente. Ele é o resultado da compilação do styles.scss pelo Sass.

2. Criando o index.html
Cole o código HTML fornecido no seu arquivo index.html. Este arquivo estabelece a estrutura fundamental da sua página, dividindo-a em cabeçalho, a seção principal de livros e o rodapé.

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
    
</html>
3. Definindo Variáveis com scss/_variaveis.scss
Crie o arquivo _variaveis.scss dentro da pasta scss/. Este arquivo, identificado pelo underline inicial, é um parcial Sass e não será compilado diretamente para CSS. Ele serve para centralizar a definição de valores reutilizáveis, como cores e fontes, facilitando a consistência e manutenção do design.

SCSS

// variaveis
$fundo: rgb(36, 36, 87);
$texto-fora-da-div: rgb(173, 197, 209);
$cor-texto-dentro-da-div: #ff00a6;
$cor-rodape: rgb(36, 36, 87);
$cor-texto: #000000;
$fonte: 'Arial', sans-serif;
4. Escrevendo os Estilos com styles.scss
Agora, no arquivo styles.scss, importe o parcial de variáveis e escreva os estilos da sua página utilizando a sintaxe SCSS. Observe como o SCSS permite aninhar seletores e usar variáveis para tornar o código mais limpo e legível.

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

    .livro { // Aninhamento de seletores para maior legibilidade
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
            color: $cor-texto-dentro-da-div; // Uso de variável para cor do título
        }

        p {
            color: $cor-texto; // Uso de variável para cor do parágrafo
        }
    }
}

.rodape {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    flex-direction: column;
    background-color: $cor-rodape; // Uso de variável para cor do rodapé
    padding: 20px;

    .imagensRodape { // Aninhamento de seletores
        display: flex;
        gap: 16px;
        justify-content: center;
        margin-top: 10px;

        .integrante { // Aninhamento para estilos dos integrantes
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 5px;
            font-size: 0.8em;
            color: $texto-fora-da-div; // Cor dos nomes dos integrantes

            img {
                width: 60px;
                height: 60px;
                border-radius: 50%;
                object-fit: cover;
                border: 2px solid $cor-texto-dentro-da-div; // Borda da imagem
                box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
                transition: transform 0.2s;

                &:hover { // Pseudoclasse aninhada para efeito hover
                    transform: scale(1.1);
                }
            }
        }
    }
}
Observações sobre o SCSS:

@import 'scss/variaveis';: Esta linha é fundamental para importar as variáveis definidas no arquivo _variaveis.scss, tornando-as acessíveis em todo o styles.scss.

Aninhamento de Seletores: Observe como seletores como .livro e .imagensRodape são aninhados dentro de seus pais (.biblioteca e .rodape respectivamente). Isso simula a hierarquia do HTML e torna o código CSS mais organizado e legível, eliminando a repetição de seletores.

Uso de Variáveis: As variáveis (prefixadas com $) permitem que você defina valores de cores, fontes e outros atributos em um único lugar e os reutilize em toda a folha de estilo. Isso facilita muito a manutenção e a padronização visual.

Pseudoclasses Aninhadas: Exemplo de :hover aninhado diretamente dentro do seletor img, aplicando um efeito de transição ao passar o mouse.

5. Compilando o SCSS para CSS
Para que o navegador entenda seus estilos SCSS, eles precisam ser compilados para CSS puro. Use o comando sass --watch para automatizar este processo.

Abra o terminal integrado do VS Code (Ctrl+') ou o prompt de comando/terminal na raiz do seu projeto (onde estão index.html e styles.scss).

Execute o seguinte comando:

Bash

sass --watch styles.scss:styles.css
sass: Invoca o compilador Sass.

--watch: Instrução para o Sass monitorar o styles.scss em busca de alterações e recompilá-lo automaticamente sempre que uma modificação for salva.

styles.scss: O arquivo SCSS de origem.

styles.css: O arquivo CSS de destino que será gerado e atualizado.

Você verá uma mensagem no terminal indicando que o Sass está "observando" os arquivos. Mantenha este terminal aberto enquanto estiver desenvolvendo para que as compilações aconteçam em tempo real.

6. Visualizando o Projeto
Com o comando sass --watch em execução e as imagens devidamente posicionadas na pasta imagens/, você pode visualizar sua página no navegador.

No VS Code, clique com o botão direito no arquivo index.html e selecione "Open with Live Server".

Isso abrirá a página em seu navegador padrão e a manterá atualizada automaticamente a cada alteração salva nos seus arquivos SCSS ou HTML.

📸 Capturas de Tela (Resultados e Processo)
Para ilustrar o projeto e o processo de desenvolvimento, considere adicionar as seguintes capturas de tela ao seu README.md:

Estrutura de Pastas no VS Code: Uma imagem mostrando a organização dos arquivos e diretórios do projeto no explorador de arquivos do VS Code.
*

Conteúdo do _variaveis.scss: Uma captura de tela exibindo o código do arquivo scss/_variaveis.scss, destacando as variáveis definidas.
*

Trecho do styles.scss (Aninhamento/Variáveis): Uma imagem mostrando um trecho do styles.scss que demonstre o uso de aninhamento de seletores e variáveis.
*

Terminal com sass --watch: Uma captura da tela do terminal ou prompt de comando mostrando o comando sass --watch em execução.
*

Página Final - Visão Geral: Uma imagem da página index.html completamente estilizada, aberta no navegador, mostrando o layout geral.
*

Página Final - Detalhe da Seção de Livros: Uma captura focando na seção biblioteca, destacando como os livros são exibidos em um layout responsivo.
*

Página Final - Detalhe do Rodapé: Uma imagem que exiba o rodapé com as fotos e nomes dos integrantes do projeto.
*

👨‍💻 Desenvolvedores
GUSTAVO RODRIGUES MOREIRA

JACSON FRANCISCO VIANA SANTOS

ALISSON RICADY MORAIS GUIMÃRAES

FELIPE PEREIRA DE LIMA