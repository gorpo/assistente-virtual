# Assistente Virtual
<h2>Assistente Virtual feito em python (em construção)<h2>
  <h3>Sistema sendo desenvolvido no ArchLinux, ainda não testado em outras plataformas</h3>'

  Criador: https://www.facebook.com/tiago.r.floyd



 <h3>Dependências</h3>
 <ul>
   <li><h4>Arch Linux</h4></li>
    <ul>
        <li># pacman -S espeak espeakup alsa-utils cmake</li>
        <li># systemctl enable espeakup.service</li>
        <li># pip install --upgrade pyyaml</li>
        <li># pip install -r requirements.txt</li>
     </ul>
   <li><h4>Windows 10</h4></li>
   <ul>
     <li>Python 3.7</li>
     <ul><li>https://www.python.org/ftp/python/3.7.0/python-3.7.0-amd64.exe</li></ul>
     <li>PyAudio</li>
     <ul><li>https://www.lfd.uci.edu/~gohlke/pythonlibs/#pyaudio</li></ul>
     <li>Cmake</li>
     <ul><li>https://github.com/Kitware/CMake/releases/download/v3.16.2/cmake-3.16.2-win64-x64.msi</li></ul>
     <li>Swig</li>
     <ul><li>http://prdownloads.sourceforge.net/swig/swigwin-4.0.1.zip</li></ul>
     <li>Instalação dependcias via pip</li>
     <ul><li>python -m pip install -m requirements.txt</li></ul>
     <li><strong>Obs: O Caminho do Python, Cmake e Swig devem estar em sua variavel PATH</strong></li>
   </ul>
 </ul>

------- [+]  Como usar no Ubuntu  [+]---------

Vamos verificar nossa versao do python, precisamos deixar nossa versao do sistema como 3.6.

$python --version   

---Caso não esteja com a versão 3.6, instale ela:
$ sudo apt install python3.6
$sudo apt install python3.6-dev

---Para trocar a versão do python use o seguinte comando:
$ sudo ln -sf /usr/bin/python3.6 /usr/bin/python

-->Isto fará com que o link simbolico que era de outro python seja trocado pela versão que queremos.
Verifique novamente a versao e veja se agora responde com a sua versao setada anteriormente.
$python --version
=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=


Vamos instalar e criar um ambiente virtual para nosso projeto python, é importante que antes esteja setado o python3.6 pois senao vai da bosta, apos setado o python3.6 siga:

sudo pip install virtualenv

[+] criar um ambiente virtual [+]
---Agora criaremos uma pasta que é um ambiente virtual com o comando:
$virtualenv nome_da_pasta

---Isto fara com que uma copia do python seja criada ali nao fodendo a sua. Todos os PiPY ali instalados nao vao sujar seu python do sistema operacional, que por sinal se vc cagar ele voce caga seu ubuntu, afinal o ubuntu usa muitas coisas em python e um purge ali seria fatal para o sistema.

----Sempre que quisermos voltar usar este ambiente virtual usaremos o comando:
$source sua_pasta/bin/activate

Feito isto você ja esta de novo em seu ambiente virtual python com tudo q precisa!
-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

--Agora precisamos ter certeza de dois pacotes essenciais funcionando pra isto iremos instalar:

pip install cmake
pip install face_recognition






Precisaremos dos seguintes pacotes preinstalados:
sudo apt install swig
sudo apt install alsa-utils
sudo apt install cmake
sudo apt install espeak
-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-
Teremos um erro nesta parte pois ele instala o pacote espeakup mas nao consegue subir ele, entao iremos instalar cientes do erro:
sudo apt install espeakup
-Ele vai dar erro pois precisa ser subido para corrigir o erro basta:
1- sudo modprobe speakup_soft
2- service  espeakup restart
Verifique se o serviço esta rodando com: service  espeakup status
3- faça com que o serviço inicie com o computador:
update-rc.d  espeakup default
-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=
Agora temos esta caralhada de PiPY a mais pra por na porra e te q seguir uma ordem(nao lembro se botei na certa mas me esforcei), pois se esta caralha nao ta na ordem alguns pacotes faltam para os outros como o caso do pip3 cmake que tomei no cu.
-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

-----Failed building wheel for pocketsphinx

sudo apt-get install -y python python-dev python-pip build-essential swig git libpulse-dev

sudo apt-get install libasound2-dev
pip install pocketsphinx
-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-==-=-=-=-=-=-=-=-=-=-=-=-=-
Temos tambem que instalar o requeriments.txt fornecido pelo floyd, eu nao sei se ele ajudou em algo, eu nem li ele mas eu instalei.

$ pip3 install -r requeriments.txt
-=-=-=-=-=-=-=-=-=-=-==-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-
-- ai eu tava bem suave o bag rodou, reconheceu meu rosto e depois deu pau ai instalei:
sudo apt-get install python-pyaudio

sudo apt-get install portaudio19-dev
sudo apt install  jackd1 portaudio19-doc


pip install pyaudio

