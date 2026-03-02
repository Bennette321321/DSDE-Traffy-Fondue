# DSDE-Traffy-Fondue

Kaggle Link: https://www.kaggle.com/competitions/2110446-dsde-2025-2

Score: 0.37750

### 1. ติดตั้ง Dependencies

```bash
conda install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia
pip install transformers datasets sentencepiece lightning scikit-learn evaluate pandas numpy tqdm matplotlib
```

### 2. เตรียมข้อมูล

วางไฟล์ `train.csv` และ `test.csv` ไว้ใน folder `data/`

### 3. รัน Notebook

รัน `main.ipynb` ตั้งแต่ต้นจนจบ โดย notebook จะทำงานดังนี้

- โหลดและ preprocess ข้อมูล
- Tokenize ข้อความด้วย PhayaThaiBERT
- Train model 2 รอบด้วย random_state = 42 และ 67
- Ensemble prob จาก 2 model แล้วหา best threshold
- สร้างไฟล์ `submission.csv` สำหรับ submit Kaggle

### 4. Submit

นำไฟล์ `submission.csv` ที่ได้ไป submit ที่ Kaggle
