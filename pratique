import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd
import numpy as np

# Carregar o arquivo
df = pd.read_csv(r"C:\Users\marti\OneDrive\Documentos\Python\pratique grafico\ecommerce_estatistica.csv")

# -------------------------------
# 1. Histograma
plt.hist(df['Qtd_Vendidos_Cod'], bins=10, color='skyblue', edgecolor='black')
plt.title("Histograma - Quantidade Vendida")
plt.xlabel("Qtd_Vendidos_Cod")
plt.ylabel("Frequência")
plt.show()

# -------------------------------
# 2. Gráfico de dispersão
plt.scatter(df['Qtd_Vendidos_Cod'], df['Marca'], color='red')
plt.title("Dispersão - Marca vs Quantidade Vendida")
plt.xlabel("Qtd_Vendidos_Cod")
plt.ylabel("Marca")
plt.show()

# -------------------------------
# 3. Mapa de calor (correlação)
df_corr = df[['Qtd_Vendidos_Cod']].corr()
plt.figure(figsize=(6,4))
sns.heatmap(df_corr, annot=True, cmap="coolwarm", fmt=".2f")
plt.title("Mapa de Calor - Correlação")
plt.show()

# -------------------------------
# 4. Gráfico de barras
categorias = df['Marca'].value_counts()
plt.bar(categorias.index, categorias.values, color='green')
plt.title("Gráfico de Barras - Marcas")
plt.xlabel("Marca")
plt.ylabel("Quantidade")
plt.xticks(rotation=45)
plt.show()

# -------------------------------
# 5. Gráfico de pizza
plt.pie(categorias.values, labels=categorias.index, autopct='%1.1f%%')
plt.title("Gráfico de Pizza - Participação das Marcas")
plt.show()

# -------------------------------
# 6. Gráfico de densidade
sns.kdeplot(df['Qtd_Vendidos_Cod'], shade=True, color="purple")
plt.title("Gráfico de Densidade - Quantidade Vendida")
plt.show()

# -------------------------------
# 7. Gráfico de regressão
# Exemplo: regressão entre índice da linha e quantidade vendida
sns.regplot(x=df.index, y=df['Qtd_Vendidos_Cod'], color="blue")
plt.title("Gráfico de Regressão - Índice vs Quantidade Vendida")
plt.show()
