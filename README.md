# Cilente Servidor - Android Python

## Enviando uma imagem para um servidor Python feito em servidor Flask:
Este repositório consiste em duas pastas:
1. **CienteAndroid**: Contém um projeto de Android Studio que constroi uma aplicação Android que faz o papel do cliente.
2. **ServidorPython**: O servidor **Python** usando o framework `Flask`.

## Compilando esta aplicação
### Cliente
#### Se vocẽ tiver o Android Studio instalado:
* Gere a aplicação a partir do projeto no **AndroidStudio**
#### Se vocẽ não tiver o Android Studio instalado:

```bash
# linux entre na pasta ClienteAndroid
cd ClienteAndroid
# exporte a variável ANDROID contendo o caminho do SDK (SDK **com as APIs instaladas**)
# na minha máquina linux, o SDK está instalado no /opt/android/sdk
export ANDROID_HOME="/opt/android/sdk"
# execute o comando gradlew
./gradlew
# pronto agora é só esperar gerar o pacote apk para instalar no seu telefone Android
```

* Rode a aplicação servidora python no console.
* Com o servidor Python rodando, entre no cliente Android, edite a caixa de texto **Endereço IPv4** para inserir o ip da sua máquina.
* No cliente Android, caixa **número da porta** entre com **5000**.
* Selecione a foto que irá ser enviada ao servidor usando o botão **Selecionar Imagem**.
* Clique no botão **Conectar ao Servidor** para estabelecer conexão e enviar a imagem ao servidor.


