## SJF (Shortest Job First) Non-Preemptive

### Langkah-langkah:
1. Urutkan proses berdasarkan **Arrival Time (AT)**.
2. Pilih proses yang memiliki **Burst Time** terpendek dari proses yang sudah tiba (available).
3. Setelah proses selesai, lanjutkan ke proses berikutnya yang sudah tiba dan memiliki **Burst Time** terpendek.

### Diketahui:

| Proses | Arrival Time (AT) | Burst Time |
|--------|-------------------|------------|
| Px     | 0                 | 16         |
| Pz     | 2                 | 8          |
| Py     | 8                 | 12         |
| Pw     | 12                | 6          |
| Pt     | 18                | 10         |

### Step 1: Tentukan Urutan Berdasarkan SJF Non-Preemptive

1. Pada waktu **0**, hanya **Px** yang tersedia, sehingga **Px** dieksekusi dulu.
2. Setelah **Px** selesai pada waktu **16**, proses yang tersedia adalah **Pz** (tiba pada waktu 2) dan **Pw** (tiba pada waktu 12). Karena **Pw** memiliki burst time lebih kecil (6), maka **Pw** dipilih.
3. Setelah **Pw** selesai pada waktu **22**, proses yang tersedia adalah **Pz**, **Py**, dan **Pt**. **Pz** dipilih karena memiliki burst time terpendek (8).
4. Setelah **Pz** selesai pada waktu **30**, proses yang tersedia adalah **Py** dan **Pt**, dan **Pt** dipilih karena burst time-nya lebih kecil (10).
5. Terakhir, **Py** diselesaikan.

### Gantt Chart:

| Proses | Px  | Pw  | Pz  | Pt  | Py  |     |
|--------|-----|-----|-----|-----|-----|-----|
| Time   | 0   | 16  | 22  | 30  | 40  | 52  |

### Step 2: Hitung Completion Time (CT)

| Proses | Arrival Time (AT) | Burst Time | Completion Time (CT) |
|--------|-------------------|------------|----------------------|
| Px     | 0                 | 16         | 16                   |
| Pw     | 12                | 6          | 22                   |
| Pz     | 2                 | 8          | 30                   |
| Pt     | 18                | 10         | 40                   |
| Py     | 8                 | 12         | 52                   |

### Step 3: Hitung Turn Around Time (TAT)

\[
TAT = CT - AT
\]

| Proses | CT  | AT  | TAT (CT - AT) |
|--------|-----|-----|---------------|
| Px     | 16  | 0   | 16 - 0 = 16   |
| Pw     | 22  | 12  | 22 - 12 = 10  |
| Pz     | 30  | 2   | 30 - 2 = 28   |
| Pt     | 40  | 18  | 40 - 18 = 22  |
| Py     | 52  | 8   | 52 - 8 = 44   |

### Step 4: Hitung Waiting Time (WT)

\[
WT = TAT - Burst Time
\]

| Proses | TAT | Burst Time | WT (TAT - Burst Time) |
|--------|-----|------------|-----------------------|
| Px     | 16  | 16         | 16 - 16 = 0           |
| Pw     | 10  | 6          | 10 - 6 = 4            |
| Pz     | 28  | 8          | 28 - 8 = 20           |
| Pt     | 22  | 10         | 22 - 10 = 12          |
| Py     | 44  | 12         | 44 - 12 = 32          |

### Step 5: Hitung Rata-Rata TAT dan WT

#### Rata-rata TAT:

\[
Rata-rata TAT = 16 + 10 + 28 + 22 + 44 / 5 = 120 / 5 = 24
\]

#### Rata-rata WT:

\[
Rata-rata WT = 0 + 4 + 20 + 12 + 32 / 5 = 68 / 5 = 13.6
\]

### Kesimpulan:

- **Rata-rata Turn Around Time (TAT): 24**
- **Rata-rata Waiting Time (WT): 13.6**
