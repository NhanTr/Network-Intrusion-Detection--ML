# Network Intrusion Detection - Progress Report

## Gioi thieu
Day la bai lab ve phan tich du lieu phat hien xam nhap mang su dung bo du lieu:
- chethuhn/network-intrusion-dataset (tai qua kagglehub)

README nay mo ta tien do hien tai trong notebook [main.ipynb](main.ipynb), chi ghi den dung buoc da thuc hien.

## Cau truc thu muc
- [main.ipynb](main.ipynb): Notebook xu ly va phan tich du lieu
- [requirements.txt](requirements.txt): Danh sach thu vien can cai dat
- [kernel-metadata.json](kernel-metadata.json): Thong tin kernel

## Moi truong va thu vien
Da su dung cac thu vien chinh:
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- kagglehub

## Tien do da hoan thanh

### 1. Nap va tong hop du lieu
- Tai dataset tu Kaggle bang kagglehub.
- Liet ke file trong thu muc dataset.
- Doc tat ca file CSV va luu vao danh sach DataFrame.
- Gop cac DataFrame thanh mot bang du lieu chung (combined_df).

### 2. Kham pha so bo
- Xem mau ngau nhien du lieu.
- Kiem tra cau truc cot va kieu du lieu bang info().

### 3. Lam sach du lieu co ban
- Chuan hoa ten cot (xoa khoang trang o dau/cuoi ten cot).
- Kiem tra va loai bo dong trung lap.
- Tim cac cot trung noi dung (identical columns).
- Loai bo cac cot trung noi dung.
- Sua loi KeyError khi drop cot da bi xoa truoc do.

### 4. Xu ly gia tri bat thuong va thieu
- Kiem tra cac cot so co gia tri vo han (+inf, -inf).
- Thay cac gia tri vo han bang NaN.
- Dem so dong co gia tri thieu.
- Loai bo cac dong chua gia tri thieu, tao bang data da lam sach.

### 5. Loai bo cot khong mang thong tin
- Tim cac cot chi co 1 gia tri duy nhat.
- Loai bo cac cot nay khoi data.

### 6. Tao nhan va phan tich nhom tan cong
- Tao mapping tu nhan goc sang cac nhom tan cong: Normal Traffic, DoS, DDoS, Port Scanning, Brute Force, Bots, Web Attacks.
- Gan cot `Attack Type` tu cot `Label`.
- Loai bo 2 nhom `Infiltration` va `Miscellaneous`.
- Kiem tra lai phan bo so luong mau cua tung nhom.

### 7. Truc quan hoa du lieu
- Ve countplot phan bo cac loai tan cong.
- Ve histogram cho mot so dac trung so.
- Ve boxplot theo tung nhom tan cong.
- Ve heatmap tuong quan cua cac dac trung so.
- Tinh cosine distance giua cac dac trung so de tim cac cot co mau tuong tu.
- Ve so sanh cap dac trung co cosine distance nho hon nguong.

### 8. Kiem tra gia tri bat thuong nang cao
- Kiem tra outlier cho mot so dac trung so bang IQR.
- Kiem tra cac gia tri am trong tap du lieu so.
- Tao tap du lieu da lam sach bo sung (`data_cleaned`) bang cach loai bo cac dong co gia tri am o cac cot can kiem tra.

### 9. Chuan bi cho mo hinh
- Xac dinh cac dac trung so va dac trung phan loai.
- Tach tap normal va tap tan cong.
- Downsample lop `Normal Traffic` de giam mat can bang.
- Gop lai thanh `balanced_data`.
- Chia du lieu thanh `X`, `y`, va train/test theo ty le 70/30.

### 10. Huan luyen mo hinh ban dau
- Chuan hoa dac trung bang `StandardScaler`.
- Huan luyen mo hinh `LogisticRegression` voi `class_weight='balanced'`.

## Trang thai hien tai
Notebook hien da di den buoc huan luyen mo hinh ban dau. Ket qua hien tai:
- Da co du lieu sach hon de phuc vu modeling.
- Da co tap can bang va tap train/test.
- Da huan luyen xong baseline Logistic Regression.
- Chua thuc hien phan danh gia mo hinh nhu accuracy, classification report, confusion matrix.

## Cach chay lai notebook
1. Cai thu vien:
   - pip install -r requirements.txt
2. Mo [main.ipynb](main.ipynb)
3. Chay lan luot cac cell tu tren xuong duoi

## Dinh huong buoc tiep theo
- Danh gia Logistic Regression bang accuracy, precision, recall, F1-score.
- Ve confusion matrix.
- Thu them cac mo hinh khac nhu Random Forest hoac XGBoost.
- So sanh ket qua cac mo hinh va chon mo hinh tot nhat.
