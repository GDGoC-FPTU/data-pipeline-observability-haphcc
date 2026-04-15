# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600367
**Name:** Ha Hung Phuoc
**Date:** 2026-04-15

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Agent: Based on my data, the best choice is Laptop at $1200. | 9 | Du lieu da duoc loc loi, chi con record hop le nen cau tra loi on dinh va dung ngu canh. |
| Garbage Data (`garbage_data.csv`) | Agent: Based on my data, the best choice is Nuclear Reactor at $999999. | 2 | Du lieu rac co outlier rat lon va khong phu hop voi bo ngu canh thuong ngay, lam ket qua bi lech. |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Garbage data lam suy giam chat luong truy van vi no chua nhieu van de dong thoi. Duplicate IDs co the lam mo thong tin va tao ra xung dot khi chon ban ghi tot nhat. Wrong data types, nhu price dang chuoi thay vi so, lam cac phep so sanh va xep hang tro nen khong on dinh. Outliers nhu gia tri 999999 khi khong duoc loc se bi xem la lua chon tot nhat, duong nhien lam mo hinh dua ra cau tra loi sai thuc te. Null values va truong rong cung lam giam do tin cay cua du lieu dau vao. Khi agent khong co buoc validate va clean du lieu, no se suy dien tren mot tap thong tin bi bao hoa boi nhung gia tri bat thuong, nen ket qua co the “dung theo may” nhung sai trong thuc te.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** Dong y. Mot prompt tot khong the cuu mot bo du lieu kem chat luong, vi ket qua cua agent phu thuoc truoc het vao du lieu ma no quan sat. Khi du lieu sach hon, bo loc va phep so sanh trong agent co co so de ra phan hoi hop ly hon.
