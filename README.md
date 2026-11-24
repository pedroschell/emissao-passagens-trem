# emissao-passagens-trem

**Português** | [English](README.en.md)

Sistema de terminal em C para emitir passagens de trem. Foi um dos meus primeiros programas, feito em 2021 na faculdade, e fica aqui como registro de onde comecei.

## O que faz

1. **Configuração:** pede a companhia ferroviária, o prefixo do trem, o número do vagão, os terminais de partida e chegada e os horários. Valida o formato (códigos de 3 letras maiúsculas, vagão de 1 a 999) e permite refazer o cadastro antes de seguir.
2. **Menu de passagens**, com um vagão de 10 assentos:
   - emitir passagem: nome do passageiro e assento, recusando assento ocupado;
   - excluir passagem: libera o assento;
   - consultar a ocupação: mostra cada assento como livre (0) ou ocupado (1);
   - encerrar.

Os dados da configuração são gravados em `Informacoes.txt`. As passagens ficam só na memória enquanto o programa roda.

## Como rodar

Projeto do Code::Blocks (`.cbp`), escrito para Windows: usa `system("pause")` e `system("cls")`.

```bash
gcc Passagens_Trem_Pedro_Schell/main.c -o passagens
./passagens
```

Em macOS ou Linux compila, mas os comandos de tela do Windows não funcionam.

## Stack

C, biblioteca padrão (`stdio`, `string`, `ctype`).
