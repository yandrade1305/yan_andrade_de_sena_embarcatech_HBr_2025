# Aquamatico Mini

Este projeto implementa uma versão digital da automação de um aquário, demonstrando como seria o controle da troca parcial de água, alimentação e o monitoramento dos parâmetros do aquário como: nível da água, pH e temperatura.

## Objetivo

Criar uma visualização interativa que simula a automação de um aquário utilizando:

- Display OLED
- Botões para acionar alimentação e troca parcial de água
- Matriz de LEDs

##  Lista de materiais: 

| Componente            | Conexão na BitDogLab      |
|-----------------------|---------------------------|
| BitDogLab (RP2040)    | -                         |
| Matriz WS2812B 5x5    | GPIO7                     |
| Display OLED I2C      | SDA: GPIO14 / SCL: GPIO15 |
| Botão A               | GPIO5                     |
| Botão B               | GPIO6                     |

## Execução

1. Abra o projeto no VS Code, usando o ambiente com suporte ao SDK do Raspberry Pi Pico (CMake + compilador ARM);
2. Compile o projeto normalmente (Ctrl+Shift+B no VS Code ou via terminal com cmake e make);
3. Conecte sua BitDogLab via cabo USB e coloque a Pico no modo de boot (pressione o botão BOOTSEL e conecte o cabo);
4. Copie o arquivo .uf2 gerado para a unidade de armazenamento que aparece (RPI-RP2);
5. A Pico reiniciará automaticamente e começará a executar o código;
6. O aquário irá aparecer na matriz de Leds e um breve texto de saudações no display OLED.

## Lógica

- A cada 2 segundos, o peixe representado por um led laranja irá se mover;
- Será exibido no display OLED informações de temperatura, pH e nível da água;
- Se apertar o botão A será realizado a alimentação;
- Se apertar o botão B será realizado a troca parcial de água.

##  Arquivos

- `src/aquamatico_mini.c`: Código principal do projeto;

---

## 📜 Licença
MIT License - MIT GPL-3.0.