# SICK AI Fuel Event Detection

![Python](https://img.shields.io/badge/Python-3.10+-blue) ![License](https://img.shields.io/badge/License-MIT-green) ![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)

## O projektu

Projekt je dio zajedničke suradnje studenata **Informacijskih i poslovnih sustava (IPS)** i **Ekonomike poduzetništva (EP)** u suradnji s IT tvrtkom **SICK**.

Cilj je razviti AI model koji u **stvarnom vremenu** prepoznaje događaje vezane uz gorivo iz telemetrijskih podataka kamiona:
- **Refuel** – točenje goriva
- **Withdrawal / Theft** – krađa ili neovlašteno točenje
- **Normal consumption** – normalna potrošnja
- **Oscillation** – fluktuacije senzora (bonus klasa)

Model treba smanjiti lažne alarme i pouzdano detektirati početak i kraj svakog događaja.

---

## Struktura projekta

```
sick-fuel-event-detection/
├── data/               # Dataset (lokalno, nije na GitHubu)
├── docs/               # Dokumentacija, prezentacije, predlošci
├── notebooks/          # Jupyter notebooki (EDA, modeliranje)
├── src/                # Python moduli (features.py, models.py, evaluation.py)
├── .gitignore
├── LICENSE
└── README.md
```

---

## Ulazni podaci

| Atribut | Opis |
|---|---|
| `Fuel LvL` | Razina goriva u spremniku (L) |
| `Speed` | Brzina vozila (km/h) |
| `Contact` | Status ključa / motora (0/1) |
| `Time` | Vremenska oznaka očitavanja |
| `obj_id` | Identifikator vozila |
| `label` | Klasa događaja (Refuel / Withdrawal / Normal) |

---

## Plan razvoja

| Faza | Opis | Rok |
|---|---|---|
| 1 | Planiranje i setup repozitorija | Tjd 1 (25.3.) |
| 2 | Dogovor podataka sa SICK-om | Tjd 2 (1.4.) |
| 3-4 | EDA i dokumentacija | Tjd 3-4 (7.4. – 13.4.) |
| 5 | Feature engineering i modeliranje | Tjd 5 (21.4.) |
| 6-7 | Evaluacija + međuprezentacija | 17.4.2026 |
| 8-10 | Iteracija modela i AHP vrednovanje | Tjd 8-10 |
| 11-13 | Etički aspekti i plan realizacije | Tjd 11-13 |
| 14 | Predaja završne dokumentacije | Tjd 14 |
| 15 | Završna prezentacija | Tjd 15 |

---

## Tehnologije

- **Python 3.10+**
- **pandas, numpy** – obrada podataka
- **matplotlib, seaborn** – vizualizacije
- **scikit-learn** – baseline modeli (RandomForest, XGBoost)
- **PyTorch / TensorFlow** – sekvencijski modeli (LSTM, GRU)
- **Jupyter Notebooks** – istraživanje i razvoj
- **FastAPI** – real-time servis (planirano)

---

## Metrike evaluacije

- Precision, Recall, F1 po klasi
- Event-level recall i precision
- Confusion Matrix
- Latencija modela (real-time zahtjevi)

---

## Tim

| Uloga | Studij |
|---|---|
| AI model razvoj | IPS |
| Analiza tržišta, AHP, dokumentacija | EP |
| Mentor / Partner | SICK |

---

## Dokumentacija

Svi materijali dostupni u `/docs` folderu:
- `Sick_prezentacija-2.pdf`
- `Sick_studija-slucaja.pdf`
- `Hodogram-aktivnosti_2026.pdf`
- `Predlozak-za-dokumentaciju.docx`

---

## Licenca

MIT License – vidi [LICENSE](LICENSE)
