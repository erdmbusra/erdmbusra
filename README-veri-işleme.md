KOLON EKLER 



import pandas as pd

# Veri setini oku
file_path = r'C:\Users\Lenovo\Desktop\model\anaveriseti\gptürkçe_veri_nötr.csv'
df = pd.read_csv(file_path)

# 'sentiment' kolonunu ekleyip değerini 2 olarak ata
df.insert(0, 'sentiment', 2)

# Veriyi kontrol etmek için ilk birkaç satırı yazdır
print(df.head())

# Yeni veriyi CSV olarak kaydetmek isterseniz:
new_file_path = r'C:\Users\Lenovo\Desktop\model\anaveriseti\gptürkçe_veri_nötr_sentiment.csv'
df.to_csv(new_file_path, index=False)
