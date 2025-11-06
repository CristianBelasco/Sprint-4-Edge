# Sprint-4-Edge

# Projeto IoT com MQTT – Contador de Passes (Arduino UNO + Ethernet Shield)
📖 Descrição

Este projeto demonstra uma aplicação de Internet das Coisas (IoT) utilizando o Arduino UNO e um Ethernet Shield (pode ser W5100 ou W5500).
O sistema coleta dados de temperatura, umidade e distância, contabiliza passagens detectadas e publica essas informações em tópicos MQTT.
Além disso, permite o controle remoto de LEDs através de mensagens MQTT recebidas.

# Funcionalidades

Comunicação via rede Ethernet com broker MQTT público;

Publicação contínua de dados de sensores (DHT22 e HC-SR04);

Contador de passagens com alternância de jogador;

Assinatura de tópico para controle de LED remoto;

Indicação visual com LEDs verde, amarelo e vermelho.

#Componentes Utilizados

Placa: Arduino UNO

Conectividade: Ethernet Shield (W5100 ou W5500)

Sensores: DHT22 (temperatura e umidade) e HC-SR04 (distância)

Atuadores: 3 LEDs (verde, amarelo, vermelho)

Broker MQTT: test.mosquitto.org (porta 1883)

Conecte o cabo de rede ao Shield e alimente o Arduino normalmente.
Caso o DHCP venha a falhar, o código usa um IP fixo configurado manualmente.

# Comunicação MQTT

Broker: test.mosquitto.org
Porta: 1883

Tópicos Publicados
Tópico	Conteúdo
futebol/passagens	Número de passagens detectadas
futebol/jogador	Jogador ativo (1 ou 2)
futebol/distancia	Distância em centímetros
futebol/temperatura	Temperatura em °C
futebol/umidade	Umidade em %
Tópico Assinado
Tópico	Função	Payload
led/control/samuel	Controle do LED verde remoto	"1" liga / "0" desliga
# Visualização:

Para visualizar em tempo real, conectar-se ao Node-red.

# Lógica dos LEDs:
Situação	LED Ativo	Significado
Passes < 5	Verde	Normal
5–9	Amarelo	Atenção
≥ 10	Vermelho	Alerta / Limite atingido

para Executar:

Abra o código no Arduino IDE.

Instale as bibliotecas: Ethernet, PubSubClient, DHT sensor library.

Conecte o Ethernet Shield ao UNO e plugue o cabo de rede.

Compile e faça upload do código.

Abra o Monitor Serial (9600 baud) para acompanhar os dados.

Monitore os tópicos no dashboard MQTT.

# grupo:
- Cristian Belasco Arancibia - RM565710.
- João Lucas Ferreira dos Santos - RM562608.
- Felipe Yamaguchi Mesquita - RM556170.
- Samuel de Oliveira da Silva - RM566245.
- Rafael Felix - RM565855.

# Arduino uno:
<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/d27855a8-f8ad-4d13-aaf4-3a050dbe09f4" />

# Node-red:
<img width="591" height="380" alt="image" src="https://github.com/user-attachments/assets/609b2add-f092-4d29-9503-e0fa11c565ef" />

<img width="864" height="712" alt="image" src="https://github.com/user-attachments/assets/cdf19aed-4885-4fca-8b1b-85f93395d85c" />

# DashBoard:
<img width="242" height="847" alt="image" src="https://github.com/user-attachments/assets/fec9e830-97e4-4ac4-bdf6-29c69648f93c" />



