# Network Intrusion Detection - Progress Report

## Gioi thieu
Day la bai lab ve phan tich du lieu phat hien xam nhap mang su dung bo du lieu:
- chethuhn/network-intrusion-dataset (tai qua kagglehub)

README nay mo ta dung tien do hien tai trong notebook [main.ipynb](main.ipynb), khong bao gom cac buoc chua lam.

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
- Kiem tra cau truc cot, kieu du lieu bang info().

### 3. Lam sach du lieu
- Chuan hoa ten cot (xoa khoang trang o dau/cuoi ten cot).
- Kiem tra va loai bo dong trung lap.
- Tim cac cot trung noi dung (identical columns).
- Loai bo cac cot trung noi dung (da sua loi KeyError khi drop cot da bi xoa truoc do).

### 4. Xu ly gia tri bat thuong va thieu
- Kiem tra cac cot so co gia tri vo han (+inf, -inf).
- Thay cac gia tri vo han bang NaN.
- Dem so dong co gia tri thieu.
- Loai bo cac dong chua gia tri thieu, tao bang data da lam sach.

### 5. Loai bo cot khong mang thong tin
- Tim cac cot chi co 1 gia tri duy nhat.
- Loai bo cac cot nay khoi data.

## Trang thai hien tai
Notebook da dung o giai doan tien xu ly va lam sach du lieu. Ket qua hien tai:
- Da tao duoc bo du lieu sach hon (data) de phuc vu phan tich/modeling.
- Chua thuc hien cac buoc:
	- Tao nhan nhom tan cong
	- Truc quan hoa phan phoi lop
	- Chuan hoa dac trung
	- Chia train/test
	- Huan luyen va danh gia mo hinh

## Cach chay lai notebook
1. Cai thu vien:
	 - pip install -r requirements.txt
2. Mo [main.ipynb](main.ipynb)
3. Chay lan luot cac cell tu tren xuong duoi

## Dinh huong buoc tiep theo
- Kiem tra phan bo nhan (Label) va xu ly mat can bang neu can.
- Tao tap dac trung va nhan cho bai toan phan loai.
- Chia tap train/test.
- Thu nghiem mo hinh co ban (VD: Random Forest, XGBoost, Logistic Regression).
- Danh gia bang precision, recall, F1-score, confusion matrix.
