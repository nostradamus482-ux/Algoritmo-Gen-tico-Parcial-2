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

El GA recupera motivos con núcleo TATAAA (consenso aprox. TATAAA[GT]) en 7/9 corridas, donde el mejor LLR global fue a los 3.807 bits (apareció en 5 corridas). La familia de motivos tipo TATA-box (TATAAA) domina los resultados finales y explica los mayores LLR, la 101 es la más estable (3/3 con TATAAA*), la 42 y 2025 también convergen mayormente a TATAAA* (2/3). aparecen motivos alternos (ATCGATAA, TGCACAAG) con LLR menores (2.00–2.58 bits).
La figura muestra la evolución del mejor fitness por generación para cada corrida. Se observa una mejora rápida al inicio y luego mesetas hasta el final del presupuesto de generaciones. Coherente con los datos del .csv, el 95% del máximo se alcanza muy temprano (alrededor del gen 11–14). La curva del mejor individuo no decrece (propio de guardar el “best-so-far”), indicando que el elitismo evita pérdidas de solución. Tras los primeros ~10–20 pasos, las mejoras son esporádicas; esto concuerda con el aumento de std fitness al final (≈×2.09), donde coexisten élite y población promedio.
•	Gen al máximo (primera vez): mediana 13, media 14.7 (0–38).
•	Progreso temprano: fracción del máximo lograda en gen 10 ≈ 0.80 (mediana 0.774, Q3 1.0).
•	Duración típica: 31–69 generaciones por corrida; media ~45.7. 
(Apoyado del .csv)

Autores y contacto
- **Yeferson Cristancho** — *yeferson.cristancho@unipamplona.edu.co*
- **Jhonthan Contreras** — *jhonathan.contreras@unipamplona.edu.co*
