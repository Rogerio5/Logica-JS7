# Logica-JS7

# <body>
  <h1>Resolução dos Desafios do Curso de Lógica de Programação 💡</h1>

  <p>Praticar a lógica de programação, incluindo conceitos como <strong>variáveis</strong>, <strong>condicionais (if-else)</strong>, <strong>loops (while)</strong> e <strong>interações com o usuário (alert, prompt)</strong>, é essencial para sua carreira de desenvolvimento de software.</p>
  <p>Esses fundamentos fornecem a base para <em>resolver problemas de forma estruturada</em>, <em>tomar decisões no código</em>, <em>criar iterações controladas</em> e <em>interagir eficazmente com os usuários</em>.</p>
  <p>Compreender esses conceitos não apenas facilita o aprendizado de novas linguagens e tecnologias, mas também capacita você a <strong>criar soluções inovadoras</strong>, <strong>depurar eficientemente</strong> e <strong>manter a qualidade</strong> ao longo do ciclo de vida do software.</p>
  <p>Portanto, investir tempo nesses princípios desde cedo é fundamental para <strong>construir uma base sólida e bem-sucedida</strong> no campo da programação.</p>

  <!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Lista de Nomes</title>
</head>
<body>
  <h2>Gerenciador de Lista</h2>

  <input type="text" id="nomeInput" placeholder="Digite um nome">
  <button onclick="adicionarNome()">Adicionar</button><br><br>

  <input type="number" id="indiceInput" placeholder="Índice do nome">
  <button onclick="verNomePorIndice()">Ver nome pelo índice</button><br><br>

  <button onclick="exibirLista()">Exibir Lista Completa</button>

  <div id="resultado" style="margin-top: 20px;"></div>

  <script>
    let listaNomes = [];

    function adicionarNome() {
      const nome = document.getElementById("nomeInput").value;
      if (nome.trim() !== "") {
        listaNomes.push(nome);
        document.getElementById("resultado").innerText = `Nome "${nome}" adicionado!`;
      }
    }

    function exibirLista() {
      document.getElementById("resultado").innerText = `Lista completa: ${listaNomes.join(", ")}`;
    }

    function verNomePorIndice() {
      const indice = parseInt(document.getElementById("indiceInput").value);
      if (indice >= 0 && indice < listaNomes.length) {
        document.getElementById("resultado").innerText = `Nome no índice ${indice}: ${listaNomes[indice]}`;
      } else {
        document.getElementById("resultado").innerText = "Índice inválido!";
      }
    }
  </script>
</body>
</html>
