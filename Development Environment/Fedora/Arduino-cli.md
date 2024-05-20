Instalar o arquivo tar do arduino-cli.

executar o comando:
```
tar -xzvf arduino-cli-<version>-linux64.tar.gz
```

Mover o binário para um diretório no PATH
```
sudo mv arduino-cli /usr/local/bin/
```

Para verificar se a instalação foi concluída com sucesso execute o comando 
```
sudo mv arduino-cli /usr/local/bin/
```

## Configuraçao Inicial

1 - Inicializar a configuraçao:
```
arduino-cli config init
```

2 - Atualizar a lista de núcleos disponíveis:
```
arduino-cli core update-index
```

3 - Instalar um núcleo específico (por exemplo, Arduino AVR):
```
arduino-cli core install arduino:avr
```

## Configurar para utilizar o Esp32

1 - Adicionar URL do JSON do gerenciador de pacotes do ESP32 ao arduino-cli:
```
arduino-cli core update-index --additional-urls https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json

```

2 - Instalar o núcleo do ESP32:
```
arduino-cli core install esp32:esp32 --additional-urls https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
```

3 - Verificar se o núcleo do ESP32 foi instalado corretamente:
```
arduino-cli core list
```