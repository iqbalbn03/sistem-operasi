| Proses | Px  | Pz  | Py  | Pw  | Pt  |
|--------|-----|-----|-----|-----|-----|
| Arrival   | 0   | 2  | 8  | 12  | 18  |   
| Time   | 16   | 8  | 12  | 6  | 10  |


## FCFS
### Gantt Chart



| Proses | Px  | Pz  | Py  | Pw  | Pt  |     |
|--------|-----|-----|-----|-----|-----|-----|
| Arrival   | 0   | 2  | 8  | 12  | 18  |   |
| Burst Time | 0   | 16  | 24  | 36  | 42  | 52  |

### Tabel Perhitungan Waiting Time (WT)

| Proses | Perhitungan |
|--------|-------------|
| Px     | 0           |
| Pz     | 16          |
| Py     | 24          |
| Pw     | 36          |
| Pt     | 42          |

_Total WT_:  
\[
0 + 16 + 24 + 36 + 42 = 118 / 5 = 23.6
\]

### Tabel Perhitungan Turn Around Time (TAT)

| Proses | CT  | AT  | TAT (CT - AT) |
|--------|-----|-----|---------------|
| Px     | 16  | 0   | 16            |
| Pz     | 24  | 2   | 22            |
| Py     | 36  | 8   | 28            |
| Pw     | 42  | 12  | 30            |
| Pt     | 52  | 18  | 34            |

_Total TAT_:  
\[
16 + 22 + 28 + 30 + 34 = 130
\]

### Rata-rata Turn Around Time (TAT):

\[
Rata-rata TAT = 130 / 5 = 26
\]


