# Data Science Society MEF & GDG on Campus MEF - AI Agents Kodlama Atölyesi

Bu repo, Data Science Society MEF ve GDG on Campus MEF tarafından ortaklaşa düzenlenen "AI Agents Kodlama Atölyesi" için geliştirilen materyalleri içermektedir. Atölye kapsamında, AI Agent'ların temelleri, farklı kütüphanelerle uygulamaları ve Retrieval-Augmented Generation (RAG) sistemlerinin nasıl oluşturulacağı üzerine iki farklı proje ele alınmıştır.

## Atölye İçeriği ve Projeler

Bu repoda iki ana proje bulunmaktadır ve her biri kendi branch'inde yer almaktadır:

1.  **`agents` Branch'i: SmolAgents ile Agent Uygulamaları**
    *   Bu bölümde, `smolagents` kütüphanesi kullanılarak çeşitli ajan (agent) örnekleri geliştirilmiştir.
    *   Örnekler arasında temel arama, farklı dil modellerinin (Hugging Face, LiteLLM ile Gemini, Ollama) entegrasyonu, çoklu ajan sistemleri ve Agentic RAG sistemi uygulamaları bulunmaktadır.
    *   Kullanılan ana dosya: `smlag.ipynb`

2.  **`simple-rag` Branch'i: Nutuk Üzerine RAG Uygulaması**
    *   Bu bölümde, Mustafa Kemal Atatürk'ün "Nutuk" adlı eseri kullanılarak LangChain, ChromaDB ve Google Gemini API ile bir Retrieval-Augmented Generation (RAG) örneği sunulmaktadır.
    *   PDF belgelerinden metin çıkarma, vektör veritabanına kaydetme, en alakalı içerikleri getirme ve Google Gemini LLM ile soru-cevap üretme adımları incelenmektedir.
    *   Kullanılan ana dosya: `nutuk-rag-w-gemini-api-pdf-version.ipynb`

## Başlarken

Projeleri kendi bilgisayarınızda çalıştırmak için öncelikle bu repoyu klonlamanız gerekmektedir:

```bash
git clone https://github.com/EmreOzdemiroglu/DS-GDG-Etkinlik-Agents-and-RAG.git
cd DS-GDG-Etkinlik-Agents-and-RAG
```

Ardından, ilgilendiğiniz projenin branch'ine geçiş yaparak o projeye özel kurulum adımlarını takip edebilirsiniz.

---

### 1. SmolAgents ile Agent Uygulamaları (`agents` branch'i)

`smolagents` kütüphanesi ile geliştirilen ajan örneklerini incelemek ve çalıştırmak için:

1.  `agents` branch'ine geçiş yapın:
    ```bash
    git checkout agents
    ```
2.  Bu branch içerisindeki `README.md` dosyasında belirtilen kurulum ve çalıştırma adımlarını takip edin. Kısaca:
    *   Bir sanal ortam oluşturup aktive edin.
    *   Gerekli Python paketlerini yükleyin:
        ```bash
        pip install smolagents duckduckgo-search 'smolagents[litellm]' pandas langchain langchain-community sentence-transformers datasets python-dotenv rank_bm25 requests --upgrade
        ```
    *   Gerekirse Hugging Face CLI ile giriş yapın.
    *   Gemini API anahtarınız için bir `.env` dosyası oluşturun.
    *   Jupyter Lab veya Notebook üzerinden `smlag.ipynb` dosyasını açın.

---

### 2. Nutuk Üzerine RAG Uygulaması (`simple-rag` branch'i)

LangChain, ChromaDB ve Gemini API kullanarak Nutuk üzerinde RAG uygulaması geliştirmek için:

1.  `simple-rag` branch'ine geçiş yapın:
    ```bash
    git checkout simple-rag
    ```
2.  Bu branch içerisindeki `README.md` dosyasında belirtilen kurulum ve çalıştırma adımlarını takip edin. Kısaca:
    *   Bir Python sanal ortamı oluşturup aktive edin.
    *   `requirements.txt` dosyasındaki bağımlılıkları yükleyin:
        ```bash
        pip install -r requirements.txt
        ```
    *   Google API anahtarınız için bir `.env` dosyası oluşturun.
    *   `nutuk.pdf` dosyasını proje kök dizinine yerleştirin.
    *   Jupyter Notebook üzerinden `nutuk-rag-w-gemini-api-pdf-version.ipynb` dosyasını açın.

## Katkıda Bulunma

Bu projeler atölye kapsamında geliştirilmiş olup, topluluk katkılarına açıktır. Eğer bir hata bulur veya bir iyileştirme yapmak isterseniz, lütfen bir "issue" açın veya "pull request" gönderin.

## Lisans

Bu projedeki materyaller, aksi belirtilmedikçe MIT Lisansı altında lisanslanmıştır. Detaylar için ilgili branch'lerdeki lisans dosyalarına bakabilirsiniz.

---

Umarız bu atölye materyalleri AI Agent'lar ve RAG sistemleri konusundaki anlayışınızı geliştirmenize yardımcı olur!

