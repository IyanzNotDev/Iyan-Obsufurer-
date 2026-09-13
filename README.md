# Obsufer

Obfuscator JavaScript berbasis Babel — string encoding, string array, identifier mangling, control-flow flattening, dead code, dsb.

## Install

```bash
npm install @babel/parser @babel/generator @babel/traverse @babel/types
```

## Cara Pakai

```bash
node obsufer.js <input.js> <output.js> [flags]
```

Contoh:

```bash
node obsufer.js app.js app-obfuscated.js
node obsufer.js app.js app-obfuscated.js --mix-flags
node obsufer.js app.js app-obfuscated.js --symbol-scale 0.1
```

## Flags

| Flag | Fungsi |
|---|---|
| `--seed <nama>` | paksa nama fungsi decode (reproducible build) |
| `--no-mangle` | jangan rename variable/fungsi lokal |
| `--no-array` | jangan pakai string pool |
| `--no-split` | jangan pecah string panjang jadi chunk |
| `--no-numeric` | jangan obfuscate angka literal |
| `--no-simplify` | jangan simplifikasi kode |
| `--no-deadcode` | jangan sisipkan dead code |
| `--no-flatten` | jangan lakukan control-flow flattening |
| `--no-guard` | jangan pasang integrity/tamper guard |
| `--no-debug-protect` | jangan sisipkan `debugger;` pengganggu |
| `--no-symbols` | jangan pasang banner simbol |
| `--no-symbol-packs` | jangan selipkan pack emoji/unicode raksasa |
| `--symbol-scale <n>` | skala jumlah baris symbol pack (default 1) |
| `--mix-flags` | acak kombinasi semua flag di atas |

Developer: **Iya
nzNotDev**
