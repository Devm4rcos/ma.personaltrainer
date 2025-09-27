# ma.personaltrainer


<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário de Atendimento - Treino Personalizado</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');

        <!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Marcos Alberto - Cartão Profissional</title>
    <style>
        /* Importa fontes que se assemelham ao design (Oswald e Montserrat) */
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Oswald:wght@400;700&display=swap');

        /* Cores Autênticas */
        :root {
            --cor-preto-autentico: #1a1a1a;
            --cor-verde-agua-autentico: #008080; /* Cor similar ao verde-água da imagem */
            --cor-texto-claro: #ffffff;
        }

        body {
            margin: 0;
            font-family: 'Montserrat', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background-color: #f0f0f0;
        }

        .card {
            display: flex;
            width: 78%;
            max-width: 900px;
            height: 350px; /* Altura fixa para simular o layout original */
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3); /* Sombra forte */
            border-radius: 8px;
            overflow: hidden;
            transition: transform 0.3s ease-in-out;
        }

        /* Efeito de hover no cartão */
        .card:hover {
            transform: scale(1.02);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.4);
        }

        /* --- Painel Esquerdo (Preto) --- */
        .left-panel {
            flex: 0 0 35%; /* Ocupa 35% da largura */
            background-color: var(--cor-preto-autentico);
            color: var(--cor-texto-claro);
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            padding: 40px 20px;
            text-align: center;
            position: relative;
        }

        .logo {
            font-family: 'Oswald', sans-serif;
            font-size: 8em;
            font-weight: 700;
            line-height: 0.8;
            letter-spacing: -5px;
            margin-top: 20px;
            /* Efeito CSS: Brilho sutil */
            text-shadow: 0 0 15px rgba(255, 255, 255, 0.5); 
            transition: text-shadow 0.5s ease;
        }
        
        /* Efeito no logo ao passar o mouse */
        .left-panel:hover .logo {
            text-shadow: 0 0 25px rgba(255, 255, 255, 0.8);
        }

        .contact-info {
            margin-bottom: 20px;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5); /* Sombra para destacar */
        }

        .contact-info h2 {
            font-size: 1.8em;
            margin: 0;
            font-weight: 700;
        }

        .contact-info p {
            font-size: 0.9em;
            margin: 5px 0 0 0;
            color: #ccc;
        }

        /* --- Painel Direito (Verde-Água) --- */
        .right-panel {
            flex: 1; /* Ocupa o restante da largura (65%) */
            background-color: var(--cor-verde-agua-autentico);
            color: var(--cor-texto-claro);
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            padding: 40px 20px;
            position: relative;
        }

        .title {
            font-family: 'Oswald', sans-serif;
            font-size: 3em;
            font-weight: 400;
            color: var(--cor-texto-claro);
            letter-spacing: 2px;
            margin-bottom: auto;
            /* Efeito CSS: Borda de baixo sutil */
            border-bottom: 2px solid rgba(255, 255, 255, 0.5);
            padding-bottom: 5px;
        }

        /* Simulação da Imagem do Corredor (substitua pelo seu SVG/PNG) */
        .runner-placeholder {
            width: 80%;
            max-width: 400px;
            height: 300px;
            background-image: url('C:\Users\Miguel\Desktop\Captura de tela 2025-09-26 222026.png'); /* Imagem similar para demonstração */
            background-size: contain;
            background-repeat: no-repeat;
            background-position: center bottom;
            opacity: 0.8;
            /* Efeito CSS: Deslocamento suave do background */
            transition: background-position 1s ease-out;
        }

        .right-panel:hover .runner-placeholder {
            background-position: center 90%; /* Desloca a imagem levemente para baixo no hover */
        }
        
        /* Responsividade básica para telas menores */
        @media (max-width: 100px) {
            .card {
                flex-direction: column;
                height: auto;
                width: 90%;
            }

            .left-panel, .right-panel {
                flex: none;
                padding: 30px 15px;
            }

            .logo {
                font-size: 6em;
            }

            .title {
                margin-top: 15px;
                font-size: 2.5em;
            }
        }
    </style>
</head>
<body>
    <div class="card">
        <div class="left-panel">
            <div class="logo">MA</div>
            <div class="contact-info">
                <h2>Marcos Alberto</h2>
                <p>CREF 040029-G/MG</p>
            </div>
        </div>
        
        <div class="right-panel">
            <div class="title">PERSONAL TRAINER</div>
            
            <div class="runner-placeholder"></div>
        </div>
    </div>
</body>
</html>









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
