# Quem sou eu? — Batalha Bíblica

Jogo em HTML, CSS e JavaScript, sem backend, fontes externas ou bibliotecas.

## Usar
Abra `dist/index.html` para jogar no modo manual. Para sensores e offline confiáveis, publique o conteúdo de `dist/` em um servidor HTTPS, como GitHub Pages. `index.html` e `sw.js` devem ficar juntos, na mesma pasta. A primeira abertura precisa de internet; aguarde o aviso de que o jogo está pronto para uso offline. Em Sites, o acesso da versão hospedada é privado por padrão.

No GitHub Pages, envie os dois arquivos à raiz da branch publicada. Não é necessário compilar ou instalar dependências.

## Dinâmica
Configure nomes, duração, rodadas, dificuldade, sons e sensores. Cada rodada inclui um turno por equipe. Na preparação, toque em Estou pronto e mantenha o aparelho parado na testa durante a contagem. Com a tela para os colegas, incline para baixo para acertar e para cima para pular; retorne à posição neutra entre ações. Os botões sempre estão disponíveis. Use pausa para recalibrar. Tela cheia, som e vibração dependem das APIs do navegador.

São 100 personagens originais (35 fáceis, 40 médios e 25 difíceis), editáveis. As duas equipes recebem nomes únicos do mesmo banco. No modo misturado, sorteamos os nomes em pares de dificuldade e distribuímos um para cada equipe. Os dois nomes restantes, de níveis diferentes porque há quantidades ímpares, são distribuídos aleatoriamente no fim do banco. Nunca repetimos personagens numa partida. Quando os nomes de uma equipe acabam, a partida é encerrada e o resultado informa o motivo. Um empate permite um turno extra por equipe se houver nomes para ambos.

Configurações, banco e progresso ficam apenas no armazenamento do navegador. Ao mudar de aplicativo ou aba durante o jogo, a partida pausa automaticamente. Recarregar permite recuperar o tempo salvo e recalibrar. Limpar os dados do navegador remove os registros. Reiniciar sorteia uma nova partida; nova partida abre configurações.

## Verificação
Testado em Chromium: banco e unicidade, pareamento das dificuldades até os nomes restantes, acerto/pulo, proteção contra duplicidade, encerramento pelo prazo, pausa e recuperação, turnos, empate/desempate, banco personalizado persistente, eventos de orientação simulados, largura móvel e recarregamento sem rede via service worker. Os sensores físicos precisam ser verificados no aparelho usado; o modo manual funciona sem eles.
