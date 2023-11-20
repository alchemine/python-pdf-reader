# Python PDF Reader
Example codes for reading and processing PDF files with python 


# 1. Tabular PDF
## 1.1 Download Dataset
- [script/download_tabular_pdf.sh](https://github.com/alchemine/python-pdf-reader/blob/main/script/download_tabular_pdf.sh) 

## 1.2 Processing Data
- [python_pdf_reader/read_summary_layout.ipynb](https://github.com/alchemine/python-pdf-reader/blob/main/python_pdf_reader/read_tabular_pdf.ipynb) 

### 1.2.1 Split Columns
- **Automatic**
   ```python
   from tabula import read_pdf
   
   columns   = [93, 126, 150, 200, 320, 390, 660, 703]  # point
   raw_datas = read_pdf(summary_path, columns=columns, guess=False, pages='all', silent=True)
   ``` 
- **Manual**
   ```python
   from tabula import read_pdf
   
   raw_datas = read_pdf(summary_path, guess=True, pages='all', silent=True)
   ```

### 1.2.2 Processing Output DataFrame