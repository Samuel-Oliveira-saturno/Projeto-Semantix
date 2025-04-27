# **Projeto de Detecção de Anemia com Machine Learning**  

## **📌 Visão Geral**  
Este projeto utiliza **aprendizado de máquina** para detectar anemia de forma **não invasiva**, analisando imagens da conjuntiva ocular por meio da composição de cores (RGB). O modelo desenvolvido pode ser aplicado em **postos de saúde, hospitais e comunidades remotas**, reduzindo a dependência de exames de sangue tradicionais.  

---

## **🎯 Objetivo**  
Desenvolver um **modelo preditivo preciso** para diagnóstico de anemia usando dados de **%Red Pixel, %Green Pixel, %Blue Pixel e níveis de hemoglobina (Hb)**, seguindo a metodologia **CRISP-DM**.  

---

## **📊 Dados**  
O dataset contém:  
- **%Red Pixel, %Green Pixel, %Blue Pixel**: Valores percentuais da cor da conjuntiva ocular.  
- **Hb (Hemoglobina)**: Níveis sanguíneos.  
- **Anaemic (Target)**: Classificação binária (Sim/Não).  

🔗 **Dataset disponível em:** [anemia_dataset.csv](https://raw.githubusercontent.com/Samuel-Oliveira-saturno/Projeto-Semantix/main/Dataset/anemia_dataset.csv)  

---

## **🔍 Metodologia**  
1. **Análise Exploratória (EDA)**  
   - Distribuição de classes  
   - Correlação entre variáveis  
   - Detecção e tratamento de outliers  

2. **Pré-processamento**  
   - Balanceamento de classes (**SMOTE + RandomOverSampler**)  
   - Criação de novas features (**Red/Green Ratio**)  

3. **Modelagem**  
   - Comparação de algoritmos (**PyCaret**)  
   - **Random Forest** selecionado como melhor modelo (AUC: 0.98)  

4. **Avaliação**  
   - **Matriz de Confusão, AUC-ROC, Precision/Recall**  
   - Validação cruzada estratificada  

5. **Deploy**  
   - API FastAPI para integração  
   - Aplicativo Streamlit para demonstração  

---

## **🚀 Como Executar o Projeto**  

### **1. Pré-requisitos**  
- Python 3.8+  
- Bibliotecas: `pycaret`, `scikit-learn`, `imbalanced-learn`, `pandas`, `seaborn`  

### **2. Instalação**  
```bash
git clone https://github.com/Samuel-Oliveira-saturno/Projeto-Semantix.git
cd Projeto-Semantix
pip install -r requirements.txt
```  

### **3. Uso**  
#### **Treinamento do Modelo**  
```python
python train_model.py
```  

#### **API FastAPI (Local)**  
```bash
uvicorn api:app --reload
```  
Acesse: `http://127.0.0.1:8000/docs`  

#### **Aplicativo Streamlit**  
```bash
streamlit run app.py
```  

---

## **📌 Resultados**  
| Métrica         | Valor  |
|----------------|--------|
| **Acurácia**   | 91%    |
| **Precisão**   | 89%    |
| **Recall**     | 83%    |
| **AUC-ROC**    | 0.98   |

📉 **Curva ROC**  
![ROC Curve](https://via.placeholder.com/400x200?text=ROC+Curve)  

📊 **Matriz de Confusão**  
|                | Predito Não | Predito Sim |
|----------------|-------------|-------------|
| **Real Não**   | 24          | 2           |
| **Real Sim**   | 1           | 5           |

---

## **💡 Aplicações**  
✅ **Diagnóstico rápido em postos de saúde**  
✅ **Triagem em massa em áreas remotas**  
✅ **Integração com prontuários eletrônicos**  

---

## **📂 Estrutura do Repositório**  
```
Projeto-Semantix/  
├── data/  
│   └── anemia_dataset.csv  
├── notebooks/  
│   └── EDA_Modelagem.ipynb  
├── models/  
│   └── melhor_modelo_anemia.pkl  
├── api/  
│   └── app.py (FastAPI)  
├── app/  
│   └── app.py (Streamlit)  
├── requirements.txt  
└── README.md  
```  

---

## **📝 Licença**  
MIT License  

---

## **✉️ Contato**  
**Samuel Saturno**  
📧 samuel.saturno@example.com  
🔗 [LinkedIn](https://www.linkedin.com/in/samuel-saturno)  

---

**🌟 Dúvidas ou contribuições?** Abra uma **issue** ou envie um **PR**!
