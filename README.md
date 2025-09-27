# ma.personaltrainer


<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário de Atendimento - Treino Personalizado</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');

      






    <script>
        // JavaScript para adicionar um efeito de fade-in ao carregar a página
        document.addEventListener('DOMContentLoaded', () => {
            const card = document.getElementById('profileCard');
            card.classList.add('fade-in');
        });
    </script>
</body>
</html>



        

        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f0f2f5;
            color: #333;
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        .container {
            width: 100%;
            max-width: 600px;
            background: #fff;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }

        h1 {
            text-align: center;
            color: #1a1a1a;
            margin-bottom: 25px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            font-weight: 600;
            margin-bottom: 8px;
            color: #495057;
        }

        .form-group input, .form-group select {
            width: 100%;
            padding: 12px;
            border: 1px solid #ced4da;
            border-radius: 8px;
            box-sizing: border-box;
            font-size: 1em;
            transition: border-color 0.3s ease;
        }
        
        .form-group input:focus, .form-group select:focus {
            outline: none;
            border-color: #007bff;
        }

        .whatsapp-button {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 100%;
            padding: 15px;
            background-color: #25D366;
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 1.2em;
            font-weight: 600;
            cursor: pointer;
            text-decoration: none;
            transition: background-color 0.3s ease, transform 0.2s ease;
        }

        .whatsapp-button:hover {
            background-color: #128C7E;
            transform: translateY(-2px);
        }

        .whatsapp-button img {
            width: 24px;
            height: 24px;
            margin-right: 10px;
        }

        #payment-options {
            display: none;
            margin-top: 15px;
            padding: 15px;
            border-left: 4px solid #007bff;
            background-color: #f8f9fa;
            border-radius: 8px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Treino Personalizado</h1>
        <p style="text-align: center; color: #6c757d;">Preencha os dados abaixo e clique no botão para ser direcionado ao WhatsApp do Personal Trainer e agendar seu atendimento presencial, ou on-line!
        </p>
        <div class="form-group">
            <label for="nome">Nome Completo:</label>
            <input type="text" id="nome" required>
        </div>
        <div class="form-group">
            <label for="telefone">Telefone/WhatsApp:</label>
            <input type="tel" id="telefone" required>
        </div>
        <div class="form-group">
            <label for="frequencia">Frequência:</label>
            <select id="frequencia" onchange="togglePaymentOptions()">
                <option value="" disabled selected>Escolha uma opção</option>
                <option value="1x">1x por semana</option>
                <option value="2x">2x por semana</option>
                <option value="3x">3x por semana</option>
                <option value="5x">5x por semana</option>
                <option value="avulso">Aula Avulsa ou On-line</option>
            </select>
        </div>
        <div id="payment-options">
            <label>Seu interesse é em um plano mensal. Qual sua preferência para o pagamento?</label>
            <div class="form-group" style="margin-top: 10px;">
                <label style="font-weight: normal;">
                    <input type="radio" name="paymentDay" value="5th" checked>
                    Todo 5º dia útil do mês
                </label>

                <label style="font-weight: normal;">
                    <input type="radio" name="paymentDay" value="specific">
                    Tenho uma data específica para o pagamento
                </label>
            </div>
            <div class="form-group" id="specific-date" style="display: none;">
                <label for="data">Qual a data de pagamento?</label>
                <input type="date" id="data">
            </div>
        </div>
        <a href="#" id="whatsapp-link" class="whatsapp-button" onclick="generateLink()">
            <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="WhatsApp Logo">
            Entrar em Contato Via WhatsApp
        </a>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const radioSpecific = document.querySelector('input[name="paymentDay"][value="specific"]');
            const radio5th = document.querySelector('input[name="paymentDay"][value="5th"]');
            const specificDateDiv = document.getElementById('specific-date');

            radioSpecific.addEventListener('change', () => {
                if (radioSpecific.checked) {
                    specificDateDiv.style.display = 'block';
                }
            });

            radio5th.addEventListener('change', () => {
                if (radio5th.checked) {
                    specificDateDiv.style.display = 'none';
                }
            });
        });

        function togglePaymentOptions() {
            const frequencia = document.getElementById('frequencia').value;
            const paymentOptionsDiv = document.getElementById('payment-options');

            if (frequencia !== 'avulso' && frequencia !== '') {
                paymentOptionsDiv.style.display = 'block';
            } else {
                paymentOptionsDiv.style.display = 'none';
            }
        }

        function generateLink() {
            const nome = document.getElementById('nome').value;
            const telefone = document.getElementById('telefone').value;
            const frequencia = document.getElementById('frequencia').value;
            const whatsappLink = document.getElementById('whatsapp-link');

            if (nome === '' || telefone === '' || frequencia === '') {
                alert("Por favor, preencha seu nome, telefone e frequência desejada antes de continuar.");
                return;
            }

            let mensagem = `Olá, Personal Trainer! Meu nome é ${nome} e meu telefone é ${telefone}. Tenho interesse realizar aula presencial de treinamento personalizado.`;

            if (frequencia === 'avulso') {
                mensagem += `\n\nEstou interessado(a) em uma aula avulsa ou on-line.`;
            } else {
                mensagem += `\n\nDesejo treinar ${frequencia} por semana e estou interessado(a) no pacote mensal.`;

                const paymentDay = document.querySelector('input[name="paymentDay"]:checked').value;
                if (paymentDay === '5th') {
                    mensagem += ` Minha preferência de pagamento é todo 5º dia útil do mês.`;
                } else if (paymentDay === 'specific') {
                    const data = document.getElementById('data').value;
                    if (data) {
                        const formattedDate = new Date(data).toLocaleDateString('pt-BR');
                        mensagem += ` A data de pagamento que me atende é ${formattedDate}.`;
                    } else {
                        mensagem += ` Não preenchi a data, mas tenho uma data específica em mente.`;
                    }
                }
            }
            
            mensagem += `\n\nAguardo seu contato para agendarmos!`;

            const encodedMessage = encodeURIComponent(mensagem);
            const whatsappUrl = `https://wa.me/5531985319584?text=${encodedMessage}`;
            
            whatsappLink.href = whatsappUrl;
            whatsappLink.target = "_blank"; // Abre em uma nova aba

            // A navegação acontece automaticamente devido ao href, então não é necessário window.location.
        }
    </script>
</body>
</html>
