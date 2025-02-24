# TeleNVDA #

* Autores: Asociación Comunidad Hispanohablante de NVDA e outros
  colaboradores. Obra original de Tyler Spivey e Christopher Toth
* Compatibilidade com o NVDA: 2019.3 e seguintes
* Baixar [versão estável] [1]

Bem-vindo ao extra TeleNVDA, que lhe permitirá ligar-se a outro computador a
executar o leitor de ecrã gratuito NVDA. Com este extra, pode ligar-se ao
computador de outra pessoa, ou permitir que uma pessoa de confiança se ligue
ao seu sistema para efectuar manutenção de rotina, diagnosticar um problema,
ou fornecer formação. Este extra é uma versão modificada do [NVDA Remote
add-on](https://nvdaremote.com), e é mantido pela comunidade espanhola do
NVDA. É totalmente compatível com o NVDA Remote. Estas são as diferenças
actuais:

* Uma opção permite bloquear comandos de fala remotos diferentes do texto.
* Melhor suporte para servidores proxy e serviços ocultos de TOR ([É
  necessário um add-on de suporte
  proxy](https://addons.nvda-project.org/addons/proxy.en.html)).
* Capacidade de mudar a chave f11 para outro gesto. Agora isto funciona como
  uma escritura comum, pelo que pode atribuir gestos no diálogo "Gestos de
  Entrada".
* Capacidade de ignorar completamente o próximo atalho imediato, é útil se
  precisar de enviar para a máquina remota o atalho utilizado para alternar
  entre o anfitrião e a máquina remota.
* Possibilidade de trocar pequenos ficheiros (até 10 MB) entre utilizadores
  ligados à mesma sessão.
* Ability to forward ports via UPNP.
* Ability to use a custom portcheck service.
* Várias correcções de bugs.

## Antes de Começar

Terá de ter instalado o NVDA em ambos os computadores, e obter o extra
TeleNVDA.

A instalação tanto do NVDA como do extra TeleNVDA são padrão. Se precisar de
mais informações, estas podem ser encontradas no Guia do Utilizador do NVDA.

## A actualizar

Ao actualizar o extra, se tiver instalado o TeleNVDA no ambiente de trabalho
seguro, recomenda-se que actualize também a cópia no ambiente de trabalho
seguro.

Para o fazer, primeiro actualize o seu addon existente. Depois abra o menu
do NVDA, preferências, definições gerais, e prima o botão "Use current saved
settings on the logon and other secure screens (requires administrator
privileges)".

## Iniciar uma sessão remota através de um servidor de retransmissão

### No computador a ser controlado

1. Abrir o menu do NVDA, Ferramentas, Remoto, Ligar. Ou prima directamente
   NVDA+alt+page para cima. Este atalho pode ser modificado a partir do
   diálogo definir comandos do NVDA.
2. Escolher cliente no primeiro botão de rádio.
3. Seleccionar Permitir que esta máquina seja controlada no segundo conjunto
   de botões de rádio.
4. No campo host, introduza o host do servidor ao qual se está a ligar, por
   exemplo remote.nvda.es. Quando o servidor em particular utiliza uma porta
   alternativa, pode introduzir o anfitrião na forma
   &lt;host&gt;:&lt;port&gt; por exemplo remote.nvda.es:1234. Se estiver a
   ligar a um endereço IPV6, introduza-o entre parênteses rectos, por
   exemplo [2603:1020:800:2::32].
5. Introduza uma senha no campo senha, ou prima o botão gerar senha. A senha
   é o que outros irão utilizar para controlar o seu computador. A máquina a
   ser controlada e todos os seus clientes precisam de utilizar a mesma
   senha.
6. Prima ok. Uma vez terminado, ouvirá um tom e ligar-se-á. Se o servidor
   incluir uma mensagem do dia, esta será mostrada numa caixa de
   diálogo. Verá este diálogo sempre que se ligar ou apenas na primeira vez,
   dependendo da configuração do servidor.

### Na máquina que vai ser o computador de controlo

1. Abrir o menu do NVDA, Ferramentas, Remoto, Ligar. Ou prima directamente
   NVDA+alt+page para cima. Este atalho pode ser modificado a partir do
   diálogo definir comandos do NVDA.
2. Escolher cliente no primeiro botão de rádio.
3. Seleccionar Controlar outra máquina no segundo conjunto de botões de
   rádio.
4. No campo host, introduza o host do servidor ao qual se está a ligar, por
   exemplo remote.nvda.es. Quando o servidor em particular utiliza uma porta
   alternativa, pode introduzir o anfitrião na forma
   &lt;host&gt;:&lt;port&gt; por exemplo remote.nvda.es:1234. Se estiver a
   ligar a um endereço IPV6, introduza-o entre parênteses rectos, por
   exemplo [2603:1020:800:2::32].
5. Introduza uma senha no campo senha, ou prima o botão gerar senha. A
   máquina a ser controlada e todos os seus clientes precisam de utilizar a
   mesma senha.
6. Prima ok. Uma vez terminado, ouvirá um tom e ligar-se-á. Se o servidor
   incluir uma mensagem do dia, esta será mostrada numa caixa de
   diálogo. Verá este diálogo sempre que se ligar ou apenas na primeira vez,
   dependendo da configuração do servidor.

### Aviso de Segurança da Ligação Remota do NVDA

Se se ligar a um servidor sem um certificado SSL válido, receberá um aviso
de segurança de ligação.

Isto pode significar que a sua ligação é insegura. Se confiar nesta
impressão digital do servidor, pode premir "Connect" para ligar uma vez, ou
"Connect and do not ask again for this server" para ligar e guardar a
impressão digital.

## Ligações directas

A opção servidor no diálogo de ligação permite estabelecer uma ligação
directa.

Uma vez seleccionado, seleccione em que modo o seu fim de ligação estará.

A outra pessoa ligar-se-á a si usando o oposto.

Once the mode is selected, you can use the Get External IP button to get
your external IP address and make sure the port which is entered in the port
field is forwarded correctly. If enabled on your router, you can forward the
port using UPNP before performing portcheck.

Se o portcheck detectar que a sua porta (6837 por defeito) não é alcançável,
aparecerá um aviso.

Forward your port and try again. Also, ensure that the NVDA process is
allowed through Windows firewall.

Note: The process for forwarding ports, enabling UPNP or configuring Windows
firewall is outside of the scope of this document. Please consult the
information provided with your router for further instruction.

Insira uma senha no campo senha, ou pressione gerar. A outra pessoa
precisará do seu IP externo juntamente com a senha para se ligar. Se
introduziu uma porta diferente da indicada por defeito (6837) no campo de
porta, certifique-se de que a outra pessoa anexa a porta alternativa ao
endereço de anfitrião no formulário &lt;ip&gt externo;:&lt;port&gt;.

If you want to forward the chosen port using UPNP, enable the "Use UPNP to
forward this port if possible" checkbox.

Once ok is pressed, you will be connected. When the other person connects,
you can use TeleNVDA normally.

## A controlar o computador remoto.

Uma vez a sessão ligada, o utilizador da máquina controladora pode premir
f11 para começar a controlar a máquina remota (por exemplo, enviando teclas
de teclado ou entrada em braille). Este atalho pode ser alterado a partir do
Diálogo de definir comandos no NVDA.

Quando o NVDA diz que controla a máquina remota, o teclado e as teclas de
visualização em braille que premir irão para a máquina remota. Além disso,
quando a máquina controladora estiver a utilizar um ecrã braille, a
informação da máquina remota será mostrada no mesmo. Prima novamente f11
para parar de enviar as teclas e voltar para a máquina controladora.

Para melhor compatibilidade, por favor assegurar que os layouts do teclado
em ambas as máquinas coincidem.

## A partilhar a sua sessão

To share a link so someone else can easily join your TeleNVDA session,
select Copy Link from the Remote menu. You can also assign gestures from the
NVDA Input Gestures dialog to speed up this task.

You can choose between two link formats. First one is compatible with both
NVDA Remote and TeleNVDA, and is the most recommended for now. Second one is
compatible only with TeleNVDA.

SE estiver ligado como computador de controlo, esta ligação permitirá que
outra pessoa se ligue e seja controlada.

Se, em vez disso, tiver configurado o seu computador para ser controlado, a
ligação permitirá que as pessoas com quem o partilha controlem a sua
máquina.

Muitas aplicações permitirão aos utilizadores activar esta ligação
automaticamente, mas se não for executada a partir de uma aplicação
específica, pode ser copiada para a área de transferência e executada a
partir do diálogo de execução.

Note that the shared link may not work if you copy it from a server running
in direct connection mode.

## Enviar ctrl+alt+del

Enquanto envia teclas, não é possível enviar normalmente a combinação
CTRL+Alt+del.

Se precisar de enviar CTRL+Alt+del, e o sistema remoto estiver no ambiente
de trabalho seguro, use este comando.

## Enviar tecla de alternância entre computador local e remoto

Normalmente quando se pressiona o atalho atribuído para alternar entre a
máquina local e a máquina remota, este não será enviado para a máquina
remota; em vez disso, irá alternar entre a máquina local e a máquina remota.

Se precisar de enviar este ou qualquer atalho para a máquina remota, pode
anular este comportamento para o próximo atalho imediato, activando o script
do próximo atalho ignorar.

Por defeito, este script é atribuído à tecla de controlo + f11. Este atalho
pode ser alterado a partir do Diálogo de definir comandos no NVDA.

Quando este extra for chamado, o próximo atalho será ignorado e será enviado
para a máquina remota, incluindo o atalho para activar o extra do próximo
atalho de ignorar. Uma vez que o próximo atalho tenha sido enviado, voltará
ao comportamento habitual.

## Controlo remoto de um computador desacompanhado

Por vezes, pode desejar controlar um dos seus próprios computadores à
distância. Isto é especialmente útil se estiver a viajar, e se desejar
controlar o seu PC de casa a partir do seu portátil. Ou, pode querer
controlar um computador numa divisão da sua casa enquanto está sentado ao ar
livre com outro PC. Uma preparação um pouco avançada torna isto conveniente
e possível.

1. Entrar no menu do NVDA, e escolher Ferramentas, depois
   Remoto. Finalmente, prima Enter em Opções.
2. Marque a caixa que diz, "Auto connect to control server on startup".
3. Select whether to use a remote relay server or to locally host the
   connection. If you decide to host the connection, you can try to forward
   ports using UPNP by checking the provided checkbox.
4. Seleccionar Permitir que esta máquina seja controlada no segundo conjunto
   de botões de rádio.
5. Se for o próprio anfitrião da ligação, terá de assegurar que a porta
   introduzida no campo de porta (6837 por defeito) na máquina controlada
   pode ser acedida a partir das máquinas controladoras.
6. Se desejar utilizar um servidor de retransmissão, preencha ambos os
   campos Host e senha, tab para OK, e prima Enter. A opção Gerar senha não
   está disponível nesta situação. O melhor é criar uma senha de que se
   lembre, para que a possa utilizar facilmente a partir de qualquer local
   remoto.

Para utilização avançada, pode também configurar o NVDA Remote para se ligar
automaticamente a um servidor de retransmissão local ou remoto em modo de
controlo. Se o desejar, seleccione Controlar outra máquina, no segundo
conjunto de botões de rádio.

Nota: A ligação automática nas opções relacionadas com o arranque no diálogo
de opções não se aplica até que o NVDA seja reiniciado.

## Discurso silencioso no computador remoto

Se não desejar ouvir o discurso do computador remoto ou sons específicos da
NVDA, basta aceder ao menu NVDA, Ferramentas, e Remoto. Seta para baixo para
Mute Remote, e prima Enter. Note que esta opção não irá desactivar a saída
remota em braille para o visor de controlo quando a máquina de controlo
estiver a enviar as teclas.

## Fim de uma sessão remota

Para terminar uma sessão remota, faça o seguinte:

1. No computador de controlo, prima F11 para parar de controlar a máquina
   remota. Deve ouvir ou ler a mensagem: "Controlando a máquina local" Se em
   vez disso ouvir ou ler uma mensagem de que está a controlar a máquina
   remota, premir F11 mais uma vez.
2. Aceder ao menu NVDA, depois Ferramentas, Remoto, e premir Enter em
   Desconectar.

Em alternativa, pode pressionar NVDA+alt+página para desligar directamente a
sessão. Este atalho pode ser alterado a partir do Diálogo definir comandos
do NVDA. Para manter a outra extremidade segura, pode premir este gesto
enquanto envia as teclas para desligar o computador remoto.

## Push clipboard

A opção Push clipboard no menu remoto permite-lhe enviar texto do seu
clipboard.

Quando activado, qualquer texto na área de transferência será enviado para
as outras máquinas.

## Envio de ficheiros

A opção Enviar ficheiro no menu remoto permite-lhe enviar pequenos ficheiros
para todos os membros da sessão, incluindo a máquina controlada. Note que só
pode enviar ficheiros de tamanho inferior a 10 MB. O envio ou recepção de
ficheiros em ecrãs seguros não é permitido.

Also note that sending files may consume too much network traffic on the
server, depending on the file size, the computers connected to the same
session and the amount of files sent. Contact your server administrator and
ask them if the traffic is billed. In that case, consider using another
platform to exchange files.

Quando o ficheiro é recebido nas máquinas remotas, aparecerá uma caixa de
diálogo Guardar como diálogo, permitindo-lhe escolher onde guardar o
ficheiro.

## Configuração do TeleNVDA para trabalhar num ambiente de trabalho seguro

Para que o TeleNVDA possa funcionar no ambiente de trabalho seguro, o addon
deve ser instalado no NVDA a funcionar no ambiente de trabalho seguro.

1. A partir do menu do NVDA, seleccionar Preferências e depois Definições
   Gerais.
2. Tab para o botão usar as configurações no ecrã de entrada e noutras
   janelas seguras (requer privilégios de administrador), e prima Enter.
3. Responda Sim aos pedidos relativos à cópia das suas definições e sobre a
   cópia de plugins, e responda ao pedido de Controlo de Conta de Utilizador
   que possa aparecer.
4. Quando as definições são copiadas, prima Enter para ativar o botão
   OK. Tab para OK e Enter mais uma vez para sair do diálogo.

Uma vez instalado o TeleNVDA no ambiente de trabalho seguro, se estiver
actualmente a ser controlado numa sessão remota, terá acesso à fala e ao
braille no ambiente de trabalho seguro quando mudar para ele.

## Limpeza de impressões digitais de certificados SSL

Se já não quiser confiar nas impressões digitais do servidor em que confiou,
pode apagar todas as impressões digitais de confiança premindo o botão
"Apagar todas as impressões digitais de confiança" no diálogo Opções.

## Using a custom portcheck service

By default, TeleNVDA checks open ports using a service provided by the NVDA
spanish community. You can change the service URL from the options
dialog. Ensure that the port to check is part of the custom URL and the
results are returned in the expected format. A portcheck sample script is
distributed in TeleNVDA repository, so you can host your own copy if
desired.

## A alterar o TeleNVDA

This project is covered by the GNU General Public License, version 2 or
later. You may clone [this repo][2] to make alteration to TeleNVDA, provided
that you read, understand and respect the license terms. The MiniUPNP module
is licensed under a BSD-3 clause license.

### dependências de terceiros

Podem ser instaladas com pip:

* Markdown
* scons

Para construir o manipulador de URL executável, é necessário o Visual Studio
2019 ou posterior.

### Para preparar o extra para distribuição:

1. Open a command line, change to the root of [this repo][2]
2. Executar o comando **scons***. O extra criado, se não houver erros, é
   colocado no directório actual.

[[!tag dev stable]]

[1]: https://www.nvaccess.org/addonStore/legacy?file=TeleNVDA

[2]: https://github.com/nvda-es/TeleNVDA
