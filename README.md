<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Gerador de QR Codes em Lote</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 40px; }
    textarea { width: 100%; height: 150px; }
    input[type=number], input[type=text] { width: 100%; padding: 8px; margin: 5px 0 15px 0; }
    input[type=submit] { padding: 10px 20px; font-size: 16px; }
    label { font-weight: bold; }
  </style>
</head>
<body>
  <h1>Gerador de QR Codes em Lote</h1>
  <form action="/generate" method="post">
    <div>
      <label for="names">Nomes (um por linha):</label><br>
      <textarea id="names" name="names" placeholder="Ex:\nJoão Silva\nMaria Oliveira"></textarea>
    </div>
    <div>
      <label for="quantity">Quantidade de QR Codes por folha (1 a 20):</label><br>
      <input type="number" id="quantity" name="quantity" min="1" max="20" value="1" required>
    </div>
    <div>
      <label for="description">Descrição (mesma para todos):</label><br>
      <input type="text" id="description" name="description" placeholder="Ex: Acesso ao evento" required>
    </div>
    <input type="submit" value="Gerar e Baixar ZIP">
  </form>
</body>
</html>
