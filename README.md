# Trabalho_Final_de_Redes

Leonardo Gonçalves

Lucas Mantuan

O trabalho consiste em três partes:(1) OpenPLC Runtime, (2) OpenPLC Editor e (3) ScadaBR

(1) OpenPLC Runtime  é um open-source PLC focado em soluções de baixo cuto industrial e está instalado em uma Raspberry Pi 3.

(2) O software Editor roda em uma máquina Windows, e suporta os cinco códigos definidos pelo padrão IEC 61131-3: FBD, IL, ST, SFC e LD
A linguagem utilizada nesse trabalho é a ladder (LD).

(3) É um software SCADA open source instalado em uma Máquina Virtual usado para criar IHMs.


# Estrutura:


A) Camada de Supervisão: ScadaBR

-> O ScadaBR se comunica com OpenPLC Runtime sobre Mobdus/TCP.

B) Camada de Controle: OpenPLC Runtime (Raspberry Pi 3)

-> O OpenPLC Runtime executa o programa gerado no OpenPLC Editor, e faz interface com a camada superior e inferior via Modbus/TCP.

C) Camada de Dispositivos de campo: ESP32

-> As placas ESP32 operam somente como dispositivos escravos, e simulam o sistema microcontrolado de um dispositivo de campo inteligente. O firmware instalado nas placas ESP32 contém a biblioteca Modbus TCP para comunicação com o host OpenPLC (Raspberry Pi 3).
como dispostivios escravos.

