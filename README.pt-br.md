# SwanStation - Mais conhecido como emulador de PlayStation 1
[Caracteristicas](#Características) | [Requisitos do sistema](Requisitos-do-sistema) | [Avisos](#avisos)

**Lista de compatibilidade de jogos:** https://docs.google.com/spreadsheets/d/1H66MxViRjjE5f8hOl5RQmF5woS1murio2dsLn14kEqo/edit

SwanStation é um garfo da DuckStation, que é um emulador do console da Sony Playstation 1, com foco na jogabilidade, velocidade e manutenção de longo prazo. O objetivo é ser o mais preciso possível, mantendo o desempenho adequado para dispositivos de baixo custo. As funções de 'hacks' (modificações) não são muito recomendadas por serem instáveis na maioria dos casos. as configurações padrão já oferecem suporte aos jogos já categorizados como jogáveis até o momento.

Um arquivo de "BIOS" é obrigátorio para inicar o emulador para que os jogos iniciem. Você pode usar qualquer arquivo de diversas regiões de consoles, embora regiões de jogo diferentes e regiões de BIOS possam ter problemas de compatibilidade entre si. O arquivo de BIOS não pode ser compartilhado junto com o emulador de forma nenhuma por questões legais, você deve fazer o processo chamado de 'dump' ou despejo do arquivo do seu próprio console; usando o Caetla ou outros meios disponíveis.

## Características

As características da SwanStation incluem:

 - CPU Recompilador/JIT (x86-64, armv7/AArch32 e também para AArch64)
 - Hardware (D3D11, OpenGL, Vulkan) e renderizador por software
 - Aumento de resolução, filtragem de textura, "função true color" (24-bit) nos renderizadores baseados por hardware (placa de vídeo)
 - PGXP para precisão de geometria, correção de textura, e profundidade de campo
 - Filtro adaptativo de resolução
 - Opções de pós-processamento
 - "Inicialização rápida" para pular a tela de BIOS ou introdução da Sony
 - Suporte para salvamento rápido
 - Supporte aos arquivos bin/cue, bin/img, e formato CHD do Mame.
 - Inicialização direta de arquivos homebrew
 - Carregamento de arquivos (psf)
 - Controles analógicos e digitais
 - Controles NeGcon são suportados
 - Aceleração do CPU emulado
 - Controle multitap (até 8 no total)
 - RetroAchievements
 - Carregamento de modificações PPF - feito para tradução de jogos do Playstation 1.

## Requisitos do sistema
 - Um processador rápido ou não tão antigo. Mas precisa ter instrução x86_64, AArch32/armv7, ou AArch64/ARMv8, caso contrário você não conseguirá usar de maneira devida nem mesmo com opção recompilador ativada.
 - Para renderizadores por hardware, uma GPU (placa de vídeo) que seja capaz de rodar OpenGL 3.1/ou OpenGL ES 3.0/Direct3D 11 Na versão 10.0 (ou versão Vulkan 1.0) ou mais recente. Sendo assim qualquer coisa feita nos últimos 10 anos ou mais.

### Detecção de região e imagens BIOS
Por padrão, o SwanStation irá emular a verificação de região presente no controlador de CD-ROM do console. Isto significa que quando a versão do console não bater com a do disco, o mesmo não vai iniciar, apresentando a seguinte mensagem "Please insert PlayStation CD-ROM". DuckStation suporta detecção automática das regiões dos discos, e se você definir a região do console para detecção automática também, isso nunca será um problema.

A verificação da região pode ser desligada na guia de opções do console. Esta é a única maneira de jogar jogos não licenciados ou homebrews que não fornecem uma linha de região correta no disco, além de usar a inicialização rápida que ignora a verificação completamente.

A verificação de discos incompativeis é suportada, mas pode interromper os jogos se eles estiverem sendo lidos pelo BIOS e esperando algum conteúdo específico.

### Proteção LibCrypt e arquivos SBI

Vários jogos de região Européia usam proteção LibCrypt, exigindo informações adicionais do subcanal do CD para funcionar corretamente. Quando o libcrypt não funciona corretamente, é notável por travamentos, carregaemntos infinitos, mas às vezes também afetando a jogabilidade, dependendo de como o jogo o implementou.

Para esses jogos, certifique-se de que a imagem do CD e seu respectivo arquivo SBI (.sbi) correspondente tenham o mesmo nome e sejam colocados no mesmo diretório. SwanStation irá carregar automaticamente o arquivo SBI quando ele for encontrado próximo à imagem do CD.

Por exemplo, se a imagem do seu disco foi nomeada `Spyro3.cue`, você deve colocar o arquivo SBI no mesmo diretório, nomeando o meso assim: `Spyro3.sbi`.

## Tests
 - Passes amidog's CPU and GTE tests in both interpreter and recompiler modes, partial passing of CPX tests

## Avisos

Ícone feito icons8: https://icons8.com/icon/74847/platforms.undefined.short-title

"PlayStation" e "PSX" são marcas registradas da Sony Interactive Entertainment Europe Limited. 
Este projeto não é afiliado de forma alguma com a Sony Interactive Entertainment.
