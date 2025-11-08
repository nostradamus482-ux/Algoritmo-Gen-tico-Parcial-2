# Algoritmo-Gen-tico-Parcial-2

**Objetivo:** Descubrir un motivo tipo k-mer que separe promotores positivos vs. negativos optimizando un fitness basado en LLR (log-likelihood ratio en bits). El fenómeno biológico modelado por el GA es selección natural y recombinación.

**Datos:** sacado del .zip AE_AB_Curso-data
promoters_neg.fasta y promoters_pos.fasta

El GA converge repetidamente a motivos con **núcleo `TATAAA`** (consenso aproximado `TATAAA[GT]`, típico de **TATA‑box**).

**Resumen cuantitativo (9 corridas)**
- **Máximo global (LLR):** **3.8074 bits** (observado en **5/9** corridas).
- **Corridas que terminan con núcleo `TATAAA`:** **7/9**.
- **Generaciones ejecutadas por corrida:** **31–69** (media **45.7**, mediana **44**).
- **Generación del máximo por corrida (gen_to_max):** mediana **13**, media **14.67**.
- **Promedio del máximo por corrida:** **3.4049 ± 0.666** bits.
- **Lectura de la figura:** ~**95%** del máximo típico se alcanza hacia **gen 11–14**; luego **mesetas**.

[Resultados GA.xlsx](https://github.com/user-attachments/files/23435022/Resultados.GA.xlsx)

<img width="2400" height="1500" alt="Fitness" src="https://github.com/user-attachments/assets/effdc3b7-d6ac-4171-ab57-db965c839ab1" />

Autores y contacto
- **Yeferson Cristancho** — *yeferson.cristancho@unipamplona.edu.co*
- **Jhonthan Contreras** — *jhonathan.contreras@unipamplona.edu.co*
