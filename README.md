# Cipher-Caesar
Am implementat un codor Cezar digital care transformă o literă de la intrare într-o altă literă aflată la o distanță specificată de un offset. De exemplu, pentru inputul "abc" și offset 2, ieșirea este "cde". Proiectul a fost realizat în SystemVerilog și testat prin simulare, sinteză și implementare pe placă FPGA.
Structura circuitului:
Circuitul este construit modular și conține următoarele blocuri funcționale:
 MUX și DEMUX: direcționează datele în funcție de controlul logic.
 Comparator (comp_greater): determină dacă in0 > in1.
 Scăzător (sub_8b): efectuează scăderi pe 8 biți.
 Sumator (sum_8b): realizează adunarea rezultatului intermediar cu offset.
 Bloc de preprocesare: realizat ca modul separat, instanțiat în modulul top.
Cerințe speciale implementate:
Blocul de preprocesare este implementat ca modul separat și instanțiat în top.sv.
offset are 4 biți, dar este extins la 8 biți prin adăugarea de zerouri pe pozițiile MSB pentru a fi compatibil cu sumatorul pe 8 biți.
Testare și validare:
Proiectul a fost verificat prin simulări în ModelSim pentru funcționalitate corectă.
S-a realizat sinteza și implementarea pe o placă FPGA, testând corectitudinea funcțională prin interfață serială și afișaj.
