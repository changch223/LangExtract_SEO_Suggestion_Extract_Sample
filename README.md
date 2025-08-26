# LangExtract SEO Suggestion Extract Sample

Sample notebook: A workflow using **LangExtract + Gemini** to **extract and analyze SEO suggestion keywords from competitor articles, then automatically generate article outlines and drafts**.

## 📌 Overview
This repository demonstrates an **automated research & content generation pipeline** for SEO article creation.  
By providing top-ranked competitor articles (e.g., 3 URLs), the workflow executes the following steps:

1. **Fetch Articles**  
   - Scrape the full text from the specified competitor article URLs  

2. **Heading (Title/H2/H3) Analysis**  
   - Use LangExtract to extract **suggestion keywords** directly from article titles and headings  

3. **Full-Text Analysis**  
   - Count the **full-text occurrences** of extracted suggestion keywords  
   - Count occurrences of the main query keywords  

4. **Article Outline Generation**  
   - Use Gemini to propose an **H2/H3-level article outline**  
   - Automatically generate FAQs, internal link ideas, and CTAs  

5. **Article Draft Generation**  
   - Generate the article body (with HTML structure) using Gemini, based on the outline and keyword statistics  

6. **Report Export**  
   - Save results in **Excel / CSV / JSON** formats  
   - Visualize with an **HTML report**  
   - *(Optional)* Publish directly to WordPress via API  

---

## 🛠️ Setup

### 1. Install Dependencies
```bash
pip install -r requirements.txt
````

(Main libraries)

* `langextract`
* `google-generativeai`
* `beautifulsoup4`
* `pandas`
* `openpyxl`
* `xlsxwriter`
* `python-dotenv`

### 2. Set API Key

Configure your Gemini API key via environment variable or `.env` file:

```bash
export LANGEXTRACT_API_KEY="your-api-key"
```

Or create a `.env` file:

```
LANGEXTRACT_API_KEY=your-api-key
```

### 3. Run Notebook

```bash
jupyter notebook LangExtract_SEO_Keyword_Intent_Demo.ipynb
```

---

## 📊 Output Examples

* **Excel Reports**

  * `suggestions_raw.csv`
  * `suggestions_agg.csv`
  * `query_counts.csv`
  * `seo_keywords_report.xlsx`

* **HTML Report**

  * `seo_keywords_report.html`


---

## 📌 Notes

* For dynamic information such as prices or schedules, always add a note like *“Check the official website for the latest details.”*
* Do not commit your `.env` file; make sure it is listed in `.gitignore`
* Usage of LangExtract / Gemini API will consume credits

---

## 📄 License

MIT
