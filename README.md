# calculo_criptos

function formatarValor(valorStr) {
  // Substitui vírgula por ponto e converte para número
  return parseFloat(valorStr.replace(',', '.'));
}

function calcularLucro() {
  // Entrada de dados
  const valorInvestidoStr = prompt("Digite o valor investido (em dólares):");
  const precoInicialStr = prompt("Digite o preço da moeda na época do investimento (ex: 0,0008 ou 0.0008):");
  const precoAtualStr = prompt("Digite o preço atual da moeda (ex: 0,002 ou 0.002):");

  // Conversão para número
  const valorInvestido = formatarValor(valorInvestidoStr);
  const precoInicial = formatarValor(precoInicialStr);
  const precoAtual = formatarValor(precoAtualStr);

  // Cálculos
  const quantidadeMoedas = valorInvestido / precoInicial;
  const valorAtual = quantidadeMoedas * precoAtual;
  const lucro = valorAtual - valorInvestido;

  // Saída formatada
  alert(
    `Você comprou ${quantidadeMoedas.toFixed(6)} moedas.\n` +
    `Valor atual do seu investimento: $${valorAtual.toFixed(2)}\n` +
    `Lucro obtido: $${lucro.toFixed(2)}`
  );
}

// Executa a função
calcularLucro();

