# Xilon Alpha 10.1 "AEGIS-REDUNDANT"

**Simulator numeric complet pentru un sistem hibrid de protecție termică (TPS) destinat reintrării hipersonice la Mach 36.**

Combinație inovatoare de:
- Răcire activă prin transpirație cu azot lichid (25 kg rezervor)
- Scut magnetohidrodinamic (MHD) cu overdrive la 6 Tesla
- Material structural: Hafniu-Carbon-Azot (Hf-C-N), 65 mm grosime
- Control PID per celulă + failover automat

### Rezultate simulare (B = 1.2 T nominal)
- Consum azot: **21.995 kg** (rămân 3.005 kg)
- Temperatură maximă nas: stabilizată ~2500 K
- Temperatură coadă: ~2604 K
- Safety_Mode: niciodată activat

### Caracteristici
- Grid 12×6 celule cu control independent
- Ecuații complete de bilanț termic (conducție, radiație, flux hipersonic)
- Model MHD bazat pe numărul Stuart
- Logging complet în CSV
- Stabil numeric (DT = 0.01 s)

### Fișiere incluse
- `Molecular.cpp` — codul sursă complet (C++)
- `xilon_final_report.csv` — rezultatele simulării complete (10.001 linii)
- `simulation_results.md` — rezumat tehnic al simulărilor

### Cum se rulează
```bash
g++ Molecular.cpp -o xilon -std=c++17 -O2
./xilon
