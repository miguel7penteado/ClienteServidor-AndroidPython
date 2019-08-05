# Cilente Servidor - Android Python

## Enviando uma imagem para um servidor Python feito em servidor Flask:
Este repositório consiste em duas pastas:
1. **CienteAndroid**: Contém um projeto de Android Studio que constroi uma aplicação Android que faz o papel do cliente.
2. **ServidorPython**: O servidor **Python** usando o framework `Flask`.

## instalando os pré-requisitos de ferramentas de desenvolvimento
### pré-requisitos de Linux Debian (Ubuntu, Devuan)
Instalando as ferramentas de desenvolvimento Android (modo texto) no seu linux
```bash
sudo mkdir -p /opt/android/sdk
mkdir -p/tmp/android
cd /tmp/android/
wget https://dl.google.com/android/repository/sdk-tools-linux-4333796.zip
sudo unzip /home/sp-miguel/Downloads/sdk-tools-linux-4333796.zip  -d /opt/android/sdk

sudo touch /root/.android/repositories.cfg
sudo echo "y" | $ANDROID_HOME/tools/bin/sdkmanager --licenses
sudo $ANDROID_HOME/tools/bin/sdkmanager --update
export ANDROID_HOME="/opt/android/sdk"
export ANDROID_SDK_ROOT="/opt/android/sdk"

cd $ANDROID_HOME/tools/bin
sudo ./sdkmanager  "add-ons;addon-google_apis-google-15" \
"add-ons;addon-google_apis-google-16" \
"add-ons;addon-google_apis-google-17" \
"add-ons;addon-google_apis-google-18" \
"add-ons;addon-google_apis-google-19" \
"add-ons;addon-google_apis-google-21" \
"add-ons;addon-google_apis-google-22" \
"add-ons;addon-google_apis-google-23" \
"add-ons;addon-google_apis-google-24" \
"extras;android;m2repository" \
"extras;google;m2repository" \
"build-tools;19.1.0" \
"build-tools;20.0.0" \
"build-tools;21.1.2" \
"build-tools;22.0.1" \
"build-tools;23.0.1" \
"build-tools;23.0.2" \
"build-tools;23.0.3" \
"build-tools;24.0.0" \
"build-tools;24.0.1" \
"build-tools;24.0.2" \
"build-tools;24.0.3" \
"build-tools;25.0.0" \
"build-tools;25.0.1" \
"build-tools;25.0.2" \
"build-tools;25.0.3" \
"build-tools;26.0.0" \
"build-tools;26.0.1" \
"build-tools;26.0.2" \
"build-tools;26.0.3" \
"build-tools;27.0.0" \
"build-tools;27.0.1" \
"build-tools;27.0.2" \
"build-tools;27.0.3" \
"build-tools;28.0.0" \
"build-tools;28.0.0" \
"build-tools;28.0.0-rc2" \
"build-tools;28.0.1" \
"build-tools;28.0.2" \
"build-tools;28.0.3" \
"cmake;3.6.4111459" \
"docs" \
"emulator" \
"lldb;2.0" \
"lldb;2.1" \
"lldb;2.2" \
"lldb;2.3" \
"lldb;3.0" \
"lldb;3.1" \
"ndk-bundle" \
"patcher;v4" \
"platform-tools" \
"platforms;android-7" \
"platforms;android-8" \
"platforms;android-9" \
"platforms;android-10" \
"platforms;android-11" \
"platforms;android-12" \
"platforms;android-13" \
"platforms;android-14" \
"platforms;android-15" \
"platforms;android-16" \
"platforms;android-17" \
"platforms;android-18" \
"platforms;android-19" \
"platforms;android-20" \
"platforms;android-21" \
"platforms;android-22" \
"platforms;android-23" \
"platforms;android-24" \
"platforms;android-25" \
"platforms;android-26" \
"platforms;android-27" \
"platforms;android-28" \
"extras;m2repository;com;android;support;constraint;constraint-layout-solver;1.0.0" \
"extras;m2repository;com;android;support;constraint;constraint-layout-solver;1.0.1" \
"extras;m2repository;com;android;support;constraint;constraint-layout-solver;1.0.2" \
"extras;m2repository;com;android;support;constraint;constraint-layout;1.0.0" \
"extras;m2repository;com;android;support;constraint;constraint-layout;1.0.1" \
"system-images;android-10;default;armeabi-v7a" \
"system-images;android-10;default;x86" \
"system-images;android-10;google_apis;armeabi-v7a" \
"system-images;android-10;google_apis;x86" \
"system-images;android-14;default;armeabi-v7a" \
"system-images;android-15;default;armeabi-v7a" \
"system-images;android-15;default;x86" \
"system-images;android-15;google_apis;armeabi-v7a" \
"system-images;android-15;google_apis;x86" \
"system-images;android-16;default;armeabi-v7a" \
"system-images;android-16;default;mips" \
"system-images;android-16;default;x86" \
"system-images;android-16;google_apis;armeabi-v7a" \
"system-images;android-16;google_apis;x86" \
"system-images;android-17;default;armeabi-v7a" \
"system-images;android-17;default;mips" \
"system-images;android-17;default;x86" \
"system-images;android-17;google_apis;armeabi-v7a" \
"system-images;android-17;google_apis;x86" \
"system-images;android-18;default;armeabi-v7a" \
"system-images;android-18;default;x86" \
"system-images;android-18;google_apis;armeabi-v7a" \
"system-images;android-18;google_apis;x86" \
"system-images;android-19;default;armeabi-v7a" \
"system-images;android-19;default;x86" \
"system-images;android-19;google_apis;armeabi-v7a" \
"system-images;android-19;google_apis;x86" \
"system-images;android-21;android-tv;armeabi-v7a" \
"system-images;android-21;android-tv;x86" \
"system-images;android-21;default;armeabi-v7a" \
"system-images;android-21;default;x86" \
"system-images;android-21;default;x86_64" \
"system-images;android-21;google_apis;armeabi-v7a" \
"system-images;android-21;google_apis;x86" \
"system-images;android-21;google_apis;x86_64" \
"system-images;android-22;android-tv;x86" \
"system-images;android-22;default;armeabi-v7a" \
"system-images;android-22;default;x86" \
"system-images;android-22;default;x86_64" \
"system-images;android-22;google_apis;armeabi-v7a" \
"system-images;android-22;google_apis;x86" \
"system-images;android-22;google_apis;x86_64" \
"system-images;android-23;android-tv;armeabi-v7a" \
"system-images;android-23;android-tv;x86" \
"system-images;android-23;android-wear;armeabi-v7a" \
"system-images;android-23;android-wear;x86" \
"system-images;android-23;default;armeabi-v7a" \
"system-images;android-23;default;x86" \
"system-images;android-23;default;x86_64" \
"system-images;android-23;google_apis;armeabi-v7a" \
"system-images;android-23;google_apis;x86" \
"system-images;android-23;google_apis;x86_64" \
"system-images;android-24;android-tv;x86" \
"system-images;android-24;default;arm64-v8a" \
"system-images;android-24;default;armeabi-v7a" \
"system-images;android-24;default;x86" \
"system-images;android-24;default;x86_64" \
"system-images;android-24;google_apis;arm64-v8a" \
"system-images;android-24;google_apis;armeabi-v7a" \
"system-images;android-24;google_apis;x86" \
"system-images;android-24;google_apis;x86_64" \
"system-images;android-24;google_apis_playstore;x86" \
"system-images;android-25;android-tv;x86" \
"system-images;android-25;android-wear-cn;armeabi-v7a" \
"system-images;android-25;android-wear-cn;x86" \
"system-images;android-25;android-wear;armeabi-v7a" \
"system-images;android-25;android-wear;x86" \
"system-images;android-25;default;x86" \
"system-images;android-25;default;x86_64" \
"system-images;android-25;google_apis;arm64-v8a" \
"system-images;android-25;google_apis;armeabi-v7a" \
"system-images;android-25;google_apis;x86" \
"system-images;android-25;google_apis;x86_64" \
"system-images;android-25;google_apis_playstore;x86" \
"system-images;android-26;android-tv;x86" \
"system-images;android-26;android-wear-cn;x86" \
"system-images;android-26;android-wear;x86" \
"system-images;android-26;default;x86" \
"system-images;android-26;default;x86_64" \
"system-images;android-26;google_apis;x86" \
"system-images;android-26;google_apis;x86_64" \
"system-images;android-26;google_apis_playstore;x86" \
"system-images;android-27;android-tv;x86" \
"system-images;android-27;default;x86" \
"system-images;android-27;default;x86_64" \
"system-images;android-27;google_apis;x86" \
"system-images;android-27;google_apis_playstore;x86" \
"system-images;android-28;android-tv;x86" \
"system-images;android-28;android-wear-cn;x86" \
"system-images;android-28;android-wear;x86" \
"system-images;android-28;default;x86" \
"system-images;android-28;default;x86_64" \
"system-images;android-28;google_apis;x86" \
"system-images;android-28;google_apis;x86_64" \
"system-images;android-28;google_apis_playstore;x86" \
"system-images;android-28;google_apis_playstore;x86_64" \
"system-images;android-29;default;x86" \
"system-images;android-29;default;x86_64" \
"system-images;android-29;google_apis;x86" \
"system-images;android-29;google_apis;x86_64" \
"system-images;android-29;google_apis_playstore;x86" \
"system-images;android-29;google_apis_playstore;x86_64" \
"system-images;android-Q;android-tv;x86"

```
### pré-requisitos Windows
A fazer
```
```

## Compilando e construindo esta aplicação
### Cliente - Construção
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
# agora construa o pacote da aplicação com o comando ./gradlew build
./gradlew build
# pronto agora é só esperar gerar o pacote apk para instalar no seu telefone Android
```
### Servidor - Construção
* Rode a aplicação servidora python no console.

## Executando a aplicação
* Com o servidor Python rodando, entre no cliente Android, edite a caixa de texto **Endereço IPv4** para inserir o ip da sua máquina.
* No cliente Android, caixa **número da porta** entre com **5000**.
* Selecione a foto que irá ser enviada ao servidor usando o botão **Selecionar Imagem**.
* Clique no botão **Conectar ao Servidor** para estabelecer conexão e enviar a imagem ao servidor.


