# GPS tracker system

GPS tracker system based on LoRa transceiver.


# Hardware

* GNSS Module RYS8830 Datasheet: http://reyax.com/tw/wp-content/uploads/2020/02/RYS8830.pdf
* Transceiever LoRa
* MCU: STM32L051KB6
* OLED streen


# System overview

```mermaid
sequenceDiagram
  Base->>+Module1: Hello, Module1. Do you hear me?;
  Module1->>+Base: Hello, Base. Yes, I do;
  Base->>+Module2: Hello, Module2. Do you hear me?;
  Base->>+Module1: Hello, Module1. Do you hear Module2?;
  Module1->>+Module2: Hello, Module2. Do you hear me?
  Module2->>+Module1: Hello, Module1. Yes, I do;
  Module1->>+Base: Hello, Base. Yes, I can hear Module2?;
```


# Module overview

```mermaid
graph LR
  MCU[MCU]--I2C-->OLED[OLED Display];
  OLED--I2C-->MCU;
  MCU--RS232-->GNSS[GNSS Module];
  MCU--SPI-->LORA[LoRa Module];
```


# Software


# Communication protocol



* In progress...


## Release History


* 0.0.1
    * Work in progress

## Meta

Your Name - Ilya Deryabin

## Contributing

