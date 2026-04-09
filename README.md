# Virus-Scanner-Test
# Simple Signature-Based File Scanner (Educational Project)
![Build](https://img.shields.io/badge/build-passing-brightgreen)
![Stars](https://img.shields.io/github/stars/sussybakaman14/Virus-Scanner-Test?style=social)
![License](https://img.shields.io/badge/license-MIT-blue)
![Platform](https://img.shields.io/badge/platform-Windows-blue)
![Language](https://img.shields.io/badge/language-C-blue)


Un semplice scanner antivirus didattico scritto in C per Windows, basato su firme binarie.  
Il progetto mostra come:

- leggere firme da file (`signatures.txt`)
- scansionare ricorsivamente una directory
- confrontare byte pattern nei file
- mostrare una barra di avanzamento
- escludere cartelle di sistema
- rilevare file che contengono firme note (es. EICAR)

⚠️ **Questo progetto è solo a scopo educativo.  
Non è un antivirus reale e non deve essere usato per proteggere sistemi in produzione.**

---

## ✨ Funzionalità

- ✔️ Scansione ricorsiva di directory
- ✔️ Barra di avanzamento dinamica
- ✔️ Visualizzazione del file attualmente in scansione
- ✔️ Esclusione automatica delle cartelle di sistema
- ✔️ Supporto a firme multiple
- ✔️ Compatibile con MinGW‑w64
- ✔️ Codice semplice e leggibile

---

## 📁 Struttura del progetto

scanner.c          → Codice sorgente principale
signatures.txt     → Firme binarie da rilevare
build_scanner.bat  → Script per compilare con MinGW‑w64
README.md          → Documentazione

## 🔧 Compilazione

Assicurati di avere **MinGW‑w64** installato e nel PATH.

Compilazione manuale:

```bash
gcc scanner.c -O2 -s -o scanner.exe

Oppure usa lo script incluso:
Build_scanner.bat
---
Per scansionare l’intero disco C:\:

bash
scanner.exe
Il programma:

conta i file

mostra la barra di avanzamento

salta automaticamente le cartelle di sistema

stampa i file infetti
---
## 📟 Esempio di output

Conteggio file...
Trovati 12453 file.
Inizio scansione...

[#####---------------] 23.7% (2950/12453 file)
Scansiono: C:\Users\Michele\Desktop\eicar.com
[INFETTO] C:\Users\Michele\Desktop\eicar.com -> EICAR

[############--------] 67.1% (8360/12453 file)
Scansiono: C:\Users\Michele\Documents\progetto\main.c

[####################] 100% (12453/12453 file)

Scansione completata.
---
/ |  ___  __ _ _ __ | | ___   __ _
\ \ / _ \/ | '__/ __| |/ _ \ / _ |
) |  / (| | | | (| | () | (| |
|____/ \|\,||  \||\/ \, |
|___/
Simple Signature-Based Scanner (Educational)
