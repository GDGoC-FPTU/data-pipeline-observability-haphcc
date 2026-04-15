[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23574019&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** phuocha@outlook.com
**Name:** Hà Hưng Phước
**Student ID:** 2A202600367

---

## Mo ta

Bai lab xay dung mot ETL pipeline don gian bang Python de doc du lieu JSON, kiem tra du lieu khong hop le, chuan hoa category, tinh discounted_price va luu ket qua ra CSV. Ngoai ra, bai lam con co phan thu nghiem do tac dong cua chat luong du lieu len ket qua cua agent khi chay voi du lieu sach va du lieu rac.

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

Lenh tren se doc `raw_data.json`, loai bo record co `price <= 0` hoac `category` rong, them `discounted_price` va `processed_at`, sau do tao `processed_data.csv`.

### Chay Agent Simulation (Stress Test)
```bash
python generate_garbage.py
python agent_simulation.py
```

`generate_garbage.py` tao `garbage_data.csv` chua duplicate IDs, wrong data types, outliers va null values. `agent_simulation.py` se so sanh cau tra loi cua agent tren du lieu sach va du lieu rac.

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

Pipeline xu ly 5 records tu JSON dau vao. Trong do 3 records hop le duoc giu lai va 2 records bi loai do gia tri khong hop le hoac category rong. File CSV dau ra co them `discounted_price` va `processed_at`. Khi stress test, agent tra loi tot hon voi du lieu sach so voi du lieu rac.
