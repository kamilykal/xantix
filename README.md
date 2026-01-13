# Xantix AI

![Xantix AI Demo](https://cdn.resimupload.org/2026/01/13/Kayit-2026-01-13-140356.gif)

Xantix, profesyonel yapay zeka modellerini tek bir çatı altında toplayan, yüksek güvenlikli ve gizlilik odaklı bir yapay zeka kütüphanesidir. Artık Xantix AI Cloud altyapısını kullanarak Gemini-3, Qwen3 ve DeepSeek-v3 gibi en yeni nesil 20+ modele anında erişim sağlar.

## Özellikler
- **Geniş Bulut Havuzu**: 20'den fazla özel eğitilmiş ve optimize edilmiş modele anında erişim.
- **Görsel Tasarım Modu**: Konsol üzerinden metin tarifleriyle görsel oluşturma desteği.
- **Sıfır Kurulum**: Yerel motor gereksinimi duymadan her bilgisayarda çalışabilme.

## Kurulum
```bash
npm install @labaykals/xantix
```

## Kullanım Modları

### 1. Metin Tabanlı Sohbet (CLI)
Yeni ve profesyonel flag yapısıyla kullanım:
```bash
xantix -m gemini -p "Türkiye'nin geleceği hakkında bir yorum yap"
```

### 2. Görsel Tasarım Modu
`-i` veya `--image` flag'i ile görsel üretim modunu aktif edin:
```bash
xantix -m flux -p "Neon ışıklı siberpunk bir İstanbul sokağı" -i
```

### 3. Node.js Kütüphane Kullanımı
```javascript
const xantix = require('@labaykals/xantix');

async function ask() {
    const response = await xantix.chat('Analiz raporu oluştur', 'deepseek');
    console.log(response);
}
ask();
```

## CLI Komutları
- `xantix -p <soru>` : Hızlı soru modu.
- `xantix -m <model> -p <soru>` : Belirli bir model ile soru sorma.
- `-i, --image` : Görsel tasarım modunu açar.
- `xantix models` : Kullanılabilir model adlarını listeler.

## Kullanılabilir Tüm Modeller

Xantix AI, aşağıdaki modellerin tamamını hibrit bulut altyapısı ile destekler:

### Metin ve Analiz Modelleri
- **Gemini Serisi:** `gemini` (Flash / Varsayılan)
- **DeepSeek Serisi:** `deepseek` (v3.2 - En Yeni!), `deepseek-v3.1`
- **Cogito Serisi:** `cogito` (v2.1 671b)
- **Qwen Serisi:** `qwen` (Coder 480b), `qwen3-next-80b`, `qwen3-vl-235b`
- **Gemma Serisi:** `gemma` (Gemma3-27b), `gemma3-12b`, `gemma3-4b`
- **Mistral Serisi:** `mistral` (Large), `ministral-3-14b`, `ministral-3-8b`, `ministral-3-3b`
- **Diğer:** `minimax` (m2 Cloud), `gpt-oss-120b`, `gpt-oss-20b`

### Görsel Tasarım Modelleri (-i)
- `flux` (Varsayılan Yüksek Kalite)
- `qwen3` (Multimodal Zeka)
- `gemma3` (Google Vizyonu)
- `sdxl` (Stable Diffusion XL)
- `minimax-img`

---
**Web Site:** [http://baykal.ct.ws/](http://baykal.ct.ws/)  
**Yapımcı:** labaykals / Baykal
