
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dia dos Namorados</title>
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body, html {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            background-color: white;
        }
        .full-height {
            height: 100vh;
        }
        .image-container img {
            width: 80%;
            height: auto;
        }
        .message-container {
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
            position: relative;
            overflow: hidden;
        }
        .audio-container {
            width: 0;
            height: 0;
            overflow: hidden;
            position: absolute;
            top: -10000px;
            left: -10000px;
        }
        .play-button {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-top: 18%;
        }
        .heart-button {
            width: 100px;
            height: 100px;
            background-color: red;
            position: relative;
            transform: rotate(-45deg);
            cursor: pointer;
            animation: pulse 1s infinite;
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1;
        }
        .heart-button::before,
        .heart-button::after {
            content: "";
            width: 100px;
            height: 100px;
            background-color: red;
            border-radius: 50%;
            position: absolute;
            z-index: -1;
        }
        .heart-button::before {
            top: -50px;
            left: 0;
        }
        .heart-button::after {
            top: 0;
            left: 50px;
        }
        .heart-button img {
            transform: rotate(45deg);
            width: 40px;
            height: auto;
        }
        @keyframes pulse {
            0% {
                transform: scale(1) rotate(-45deg);
            }
            50% {
                transform: scale(1.1) rotate(-45deg);
            }
            100% {
                transform: scale(1) rotate(-45deg);
            }
        }
        .particle {
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: red;
            transform: rotate(-45deg);
            animation: particle-animation 1s linear forwards;
        }
        .particle::before,
        .particle::after {
            content: "";
            width: 20px;
            height: 20px;
            background-color: red;
            border-radius: 50%;
            position: absolute;
        }
        .particle::before {
            top: -10px;
            left: 0;
        }
        .particle::after {
            top: 0;
            left: 10px;
        }
        @keyframes particle-animation {
            to {
                transform: translateY(-50px) scale(0);
                opacity: 0;
            }
        }
        .message {
            display: none;
            font-size: 18px;
            white-space: pre-wrap;
            width: 100%;
            padding: 20px;
            box-sizing: border-box;
            text-align: justify;
            margin-top: 20px;
            margin-bottom: 20px;
            overflow-y: auto;
            background-color: #ffe6e6;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            position: relative;
        }
        .hide {
            display: none;
        }
    </style>
</head>
<body>
    <div class="container-fluid full-height">
        <div class="row full-height">
            <div class="col-md-6 d-flex align-items-center justify-content-center image-container">
                <img id="image" src="449019436_1245695136804908_2205374612770250302_n.jpg" alt="Montagem de Fotos">
            </div>
            <div class="col-md-6 message-container">
                <div id="messageContent">
                    <h1>Feliz Dia dos Namorados!</h1>
                    <p>Que nosso amor continue crescendo a cada dia. Amo você!</p>
                    <div class="play-button">
                        <div id="playAudio" class="heart-button">
                            <img src="tap.png" alt="Tap">
                        </div>
                    </div>
                </div>
                <div id="typedText" class="message">
                    Vidaaaa,<br><br>
                    Só tenho a agradecer por ter você na minha vida. Você é uma namorada maravilhosa, às vezes maluquinha, mas é exatamente isso que te torna única e especial. Amo o seu jeitinho, e foi esse nosso jeito doidinho que acabou nos unindo também.<br><br>
                    A vida é engraçada, né? Às vezes estamos apenas vivendo um dia após o outro, sem grandes expectativas, e nem imaginamos que Deus está mexendo os pauzinhos para dar um rumo melhor em tudo. A forma como nos conhecemos foi muito divertida e, com certeza, não foi por acaso. Tenho certeza de que foi Deus quem cruzou nossos caminhos, e sou extremamente grato por isso, pois encontrei em você a melhor companheira que poderia desejar.<br><br>
                    Você é minha namorada, minha parceira e minha amiga. Me sinto muito privilegiado de encontrar tudo isso na pessoa que amo. Quero compartilhar minha vida inteira com você, construindo nossa família e realizando todos os nossos sonhos. E, claro, viajando muito, curtindo festivais, tomando umas brejas em algum bar por aí, fazendo uns rolês de carro, fofocando e rindo como sempre.<br><br>
                    Com certeza, você é a melhor namorada do mundo e minha melhor companhia. Que Deus continue abençoando a nossa união. Pode contar comigo para tudo que precisar; estarei sempre aqui para te ajudar e te apoiar em tudo.<br><br>
                    Você torna todos os meus dias melhores, e sou eternamente grato por isso. Obrigado por ser quem você é e por trazer tanta alegria à minha vida. Obrigado por ser sempre tão compreensiva comigo, por entender meus medos, inseguranças e até minhas chatices. Ninguém é perfeito, mas você me faz sentir que estou quase lá… brincadeira, kkkk. Acho que estou em 98%, kkkk.<br><br>
                    Te amoooo muitooooo!
                </div>
            </div>
        </div>
    </div>
    <div class="audio-container">
        <iframe id="audioPlayer" width="560" height="315" src="https://www.youtube.com/embed/ZE1yh5NoDiU?enablejsapi=1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allow="autoplay"></iframe>
    </div>

    <script src="https://www.youtube.com/iframe_api"></script>
    <script>
        var player;

        function onYouTubeIframeAPIReady() {
            player = new YT.Player('audioPlayer', {
                events: {
                    'onReady': onPlayerReady
                }
            });
        }

        function onPlayerReady(event) {
            var playButton = document.getElementById("playAudio");
            playButton.addEventListener("click", function() {
                event.target.playVideo();
                document.getElementById("playAudio").classList.add("hide");
                document.getElementById("typedText").classList.remove("hide");
                document.getElementById("typedText").style.display = "block";
                document.getElementById("messageContent").classList.add("hide");
            });
        }

        document.addEventListener('mousemove', function(e) {
            var particle = document.createElement('div');
            particle.classList.add('particle');
            particle.style.left = e.pageX + 'px';
            particle.style.top = e.pageY + 'px';
            document.body.appendChild(particle);

            setTimeout(function() {
                particle.remove();
            }, 1000);
        });

        // Ajusta a altura da div de mensagem para igualar à altura da imagem
        window.onload = function() {
            var imageHeight = document.getElementById("image").clientHeight;
            document.getElementById("typedText").style.maxHeight = imageHeight + "px";
        };
    </script>
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.5.2/dist/umd/popper.min.js"></script>
    <script src="https://stackpath.amazonaws.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
</body>
</html>
