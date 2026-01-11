<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Painel Robo BR Fiscal - Autoridade Cristian</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @media print { .no-print { display: none; } #cupom-fiscal { display: block !important; } }
        .thermal-font { font-family: 'Courier New', Courier, monospace; }
    </style>
</head>
<body class="bg-gray-100 p-6">
    <div class="max-w-4xl mx-auto bg-white rounded-3xl shadow-xl overflow-hidden no-print">
        <div class="bg-black p-8 text-white flex justify-between items-center">
            <div>
                <h1 class="text-3xl font-bold tracking-tighter">ROBÔ BR FISCAL</h1>
                <p class="opacity-70 text-sm uppercase tracking-widest">Sentinela Governamental Cristian</p>
            </div>
            <div class="text-right">
                <span class="text-xs block opacity-50">CNPJ MONITORADO</span>
                <input type="text" id="cnpjInput" placeholder="00.000.000/0000-00" class="bg-transparent border-b border-white outline-none text-xl font-mono text-right">
            </div>
        </div>

        <div class="p-8 grid grid-cols-1 md:grid-cols-2 gap-8">
            <div>
                <h2 class="font-bold text-lg mb-4 flex items-center gap-2">
                    <span class="w-3 h-3 bg-green-500 rounded-full animate-pulse"></span> Situação na Receita/PGFN
                </h2>
                <div class="space-y-4" id="resultadoFisico">
                    <div class="p-4 bg-gray-50 border-l-4 border-gray-300">
                        <p class="text-xs text-gray-500 font-bold uppercase">Aguardando Varredura...</p>
                    </div>
                </div>
            </div>

            <div class="bg-gray-50 p-6 rounded-2xl">
                <h2 class="font-bold text-lg mb-4">Ações do Fiscal</h2>
                <button onclick="consultarAWS()" id="btnConsultar" class="w-full mb-3 bg-black text-white py-3 rounded-xl font-bold shadow-lg hover:bg-gray-800 transition">
                    Executar Varredura AWS
                </button>
                <button onclick="window.print()" class="w-full mb-3 bg-blue-600 text-white py-3 rounded-xl font-bold shadow-lg hover:bg-blue-700 transition">
                    Emitir NF-e & Imprimir Térmica
                </button>
            </div>
        </div>
    </div>

    <div id="cupom-fiscal" class="hidden thermal-font text-xs p-2 w-full max-w-[80mm] text-black bg-white">
        <center>
            <p class="font-bold text-lg">ROBO BR FISCAL</p>
            <p>CONFORMIDADE GOVERNAMENTAL</p>
            <p>--------------------------------</p>
        </center>
        <p>CNPJ: <span id="cupomCnpj">---</span></p>
        <p>DATA: <span id="cupomData">---</span></p>
        <p>ORIGEM: API INFINITEPAY / GOV</p>
        <p>--------------------------------</p>
        <div id="cupomConteudo">
            </div>
        <p>--------------------------------</p>
        <p class="text-center text-[10px]">Autenticado pelo Ciclo de Autoridade Cristian</p>
    </div>

    <script>
        async function consultarAWS() {
            const cnpj = document.getElementById('cnpjInput').value;
            const btn = document.getElementById('btnConsultar');
            const resDiv = document.getElementById('resultadoFisico');

            if(!cnpj) { alert("Digite o CNPJ primeiro!"); return; }

            btn.innerText = "VARRENDO GOVERNO...";
            btn.disabled = true;

            try {
                // SEU LINK DA AWS AQUI
                const response = await fetch('https://x7rrkmlue3fbvk5j5awpfzy3he0jwoeq.lambda-url.sa-east-1.on.aws/', {
                    method: 'POST',
                    body: JSON.stringify({ cnpj: cnpj }),
                    headers: { 'Content-Type': 'application/json' }
                });

                const data = await response.json();

                // Atualiza a tela
                resDiv.innerHTML = `
                    <div class="p-4 bg-green-50 border-l-4 border-green-500">
                        <p class="text-xs text-green-600 font-bold uppercase">RESULTADO AWS</p>
                        <p class="text-lg font-bold text-green-800">${data.diagnostico.receita_federal}</p>
                        <p class="text-sm text-green-700">${data.diagnostico.pgfn_divida}</p>
                    </div>
                `;

                // Prepara o Cupom para Impressão
                document.getElementById('cupomCnpj').innerText = cnpj;
                document.getElementById('cupomData').innerText = new Date().toLocaleString();
                document.getElementById('cupomConteudo').innerHTML = `
                    <p>STATUS: ${data.diagnostico.receita_federal}</p>
                    <p>DIVIDA: ${data.diagnostico.pgfn_divida}</p>
                    <p>SISTEMA: ${data.autoridade}</p>
                `;

                alert("Varredura Concluída! O cupom está pronto para imprimir.");

            } catch (error) {
                alert("Erro ao falar com o Robô AWS: " + error);
            } finally {
                btn.innerText = "Executar Varredura AWS";
                btn.disabled = false;
            }
        }
    </script>
</body>
</html>
