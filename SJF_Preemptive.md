
## SJF (Shortest Job First) Preemptive (SRTF)

### Langkah-langkah SJF Preemptive:
1. Mulai dari waktu 0, pilih proses yang tiba dan memiliki **Burst Time** terpendek.
2. Jika ada proses baru yang tiba dengan **Burst Time** lebih pendek daripada proses yang sedang berjalan, lakukan preemption.
3. Ulangi hingga semua proses selesai.

### Diketahui:

| Proses | Arrival Time (AT) | Burst Time |
|--------|-------------------|------------|
| Px     | 0                 | 16         |
| Pz     | 2                 | 8          |
| Py     | 8                 | 12         |
| Pw     | 12                | 6          |
| Pt     | 18                | 10         |

### Step 1: Tentukan Urutan Berdasarkan SJF Preemptive

#### Time 0 - 2:
- **Px** tiba pada waktu **0** dan mulai dieksekusi (karena tidak ada proses lain).

#### Time 2 - 12:
- Pada waktu **2**, **Pz** tiba dengan **Burst Time** lebih pendek dari **Px** (8 < 14), sehingga **Px** di-preempt, dan **Pz** mulai dieksekusi.
- **Pz** selesai pada waktu **10**, sehingga sisa proses adalah **Px** dengan 14 - 8 = 6 waktu tersisa.

#### Time 10 - 12:
- **Px** kembali berjalan sampai waktu **12** (karena **Pw** tiba tepat pada waktu **12**).

#### Time 12 - 18:
- Pada waktu **12**, **Pw** tiba dengan **Burst Time** lebih pendek dari sisa **Px** (6 < 4). Sehingga **Pw** berjalan.
- **Pw** selesai pada waktu **18**, dan proses berikutnya adalah **Px** (4 waktu tersisa) dan **Pt** (baru tiba).

#### Time 18 - 22:
- **Px** (4 waktu tersisa) dieksekusi sebelum **Pt**, karena **Px** sudah berada di sistem lebih dulu.

#### Time 22 - 32:
- **Pt** mulai dieksekusi dan selesai pada waktu **32**.

#### Time 32 - 44:
- **Py** satu-satunya yang tersisa, sehingga dieksekusi dan selesai pada waktu **44**.

### Gantt Chart:

| Proses | Px  | Pz  | Px  | Pw  | Px  | Pt  | Py  |     |
|--------|-----|-----|-----|-----|-----|-----|-----|-----|
| Time   | 0   | 2   | 10  | 12  | 18  | 22  | 32  | 44  |

### Step 2: Hitung Completion Time (CT)

| Proses | Arrival Time (AT) | Burst Time | Completion Time (CT) |
|--------|-------------------|------------|----------------------|
| Px     | 0                 | 16         | 22                   |
| Pz     | 2                 | 8          | 10                   |
| Py     | 8                 | 12         | 44                   |
| Pw     | 12                | 6          | 18                   |
| Pt     | 18                | 10         | 32                   |

### Step 3: Hitung Turn Around Time (TAT)

\[
TAT = Completion Time (CT) - Arrival Time (AT)
\]

| Proses | CT  | AT  | TAT (CT - AT) |
|--------|-----|-----|---------------|
| Px     | 22  | 0   | 22 - 0 = 22   |
| Pz     | 10  | 2   | 10 - 2 = 8    |
| Py     | 44  | 8   | 44 - 8 = 36   |
| Pw     | 18  | 12  | 18 - 12 = 6   |
| Pt     | 32  | 18  | 32 - 18 = 14  |

### Step 4: Hitung Waiting Time (WT)

\[
WT = TAT - Burst Time
\]

| Proses | TAT | Burst Time | WT (TAT - Burst Time) |
|--------|-----|------------|-----------------------|
| Px     | 22  | 16         | 22 - 16 = 6           |
| Pz     | 8   | 8          | 8 - 8 = 0             |
| Py     | 36  | 12         | 36 - 12 = 24          |
| Pw     | 6   | 6          | 6 - 6 = 0             |
| Pt     | 14  | 10         | 14 - 10 = 4           |

### Step 5: Hitung Rata-Rata TAT dan WT

#### Rata-rata TAT:

\[
Rata-rata TAT = (22 + 8 + 36 + 6 + 14) / 5 = 86 / 5 = 17.2
\]

#### Rata-rata WT:

\[
Rata-rata WT = (6 + 0 + 24 + 0 + 4) / 5 = 34 / 5 = 6.8
\]

### Kesimpulan:

- **Rata-rata Turn Around Time (TAT): 17.2**
- **Rata-rata Waiting Time (WT): 6.8**


