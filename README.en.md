# emissao-passagens-trem

[Português](README.md) | **English**

A terminal train ticketing system written in C. It was one of my first programs, built in 2021 in college, and it stays here as a record of where I started.

## What it does

1. **Setup:** asks for the railway company, the train code, the car number, the departure and arrival terminals and the times. It validates the format (3-letter uppercase codes, car number from 1 to 999) and lets you redo the setup before moving on.
2. **Ticket menu**, for a single car with 10 seats:
   - issue a ticket: passenger name and seat, refusing a taken seat;
   - cancel a ticket: frees the seat;
   - check occupancy: shows each seat as free (0) or taken (1);
   - exit.

The setup data is appended to `Informacoes.txt`. Tickets live only in memory while the program runs.

## Run

A Code::Blocks project (`.cbp`), written for Windows: it calls `system("pause")` and `system("cls")`.

```bash
gcc Passagens_Trem_Pedro_Schell/main.c -o passagens
./passagens
```

It compiles on macOS or Linux, but the Windows screen commands won't work there.

## Stack

C, standard library only (`stdio`, `string`, `ctype`).
