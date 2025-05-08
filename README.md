# Nutuk RAG with LangChain, Chroma ve Gemini

Bu proje, Mustafa Kemal Atatürk'ün "Nutuk" adlı eserini kullanarak LangChain, Chroma ve Google Gemini API ile Retrieval-Augmented Generation (RAG) örneğini sunar. PDF belgelerinden metin parçaları çıkarır, vektör veri tabanına kaydeder, en alakalı içerikleri getirir ve Google Gemini LLM ile soru-cevap cevapları üretir.

## Özellikler
- PDF yükleme (PyPDFLoader)
- Metin parçalama (RecursiveCharacterTextSplitter)
- Google Generative AI Embeddings ile vektör oluşturma
- ChromaDB vektör veritabanı ile veri saklama ve retrieval
- Google Gemini LLM (ChatGoogleGenerativeAI) ile soru-cevap zinciri

## Gereksinimler
- Python 3.10 veya üzeri
- `pip` paket yöneticisi
- Google Cloud hesabı ve Generative AI API erişimi
- `nutuk.pdf` (Nutuk eserinin PDF dosyası)
- İnternet bağlantısı

## Kurulum
1. Depoyu klonlayın:
   ```bash
   git clone <repository_url>
   cd <repository_klasoru>
   ```
2. Python sanal ortam oluşturun ve aktive edin:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```
3. Gerekli bağımlılıkları yükleyin:
   ```bash
   pip install -r requirements.txt
   ```
4. Ortam değişkenlerini ayarlayın:
   - Proje kök dizininde bir `.env` dosyası oluşturun ve aşağıdakini ekleyin:
     ```
     GOOGLE_API_KEY=<API_ANAHTARINIZ>
     ```
     veya
     ```
     GOOGLE_APPLICATION_CREDENTIALS=/path/to/credentials.json
     ```

## Kullanım
1. `nutuk.pdf` dosyasını proje kök dizinine yerleştirin.
2. Jupyter Notebook'u başlatın:
   ```bash
   jupyter notebook
   ```
3. `nutuk-rag-w-gemini-api-pdf-version.ipynb` dosyasını açın ve hücreleri sırayla çalıştırın.

## Örnek Sorgu
```python
response = rag_chain.invoke({"input": "Samsun'a neden çıktınız?"})
print(response['answer'])
```

## Proje Yapısı
```
.
├── nutuk.pdf
├── nutuk-rag-w-gemini-api-pdf-version.ipynb
├── requirements.txt
└── README.md
```

## Lisans
Bu proje MIT lisansı ile lisanslanmıştır.
