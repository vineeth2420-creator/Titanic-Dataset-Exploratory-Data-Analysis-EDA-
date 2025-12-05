# Titanic-Dataset-Exploratory-Data-Analysis-EDA-
import os
os.makedirs("outputs", exist_ok=True)
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

df = pd.read_csv("titanic.csv")

print(df.head())
print(df.info())
print(df.isnull().sum())

# Age bucket feature
df["AgeBucket"] = pd.cut(
    df["Age"],
    bins=[0, 12, 18, 40, 60, 100],
    labels=["Child", "Teen", "Adult", "MidAge", "Senior"]
)

# Survival by Sex
print("\nSurvival by Sex:")
print(df.groupby("Sex")["Survived"].mean())

# Survival by Class
print("\nSurvival by Class:")
print(df.groupby("Pclass")["Survived"].mean())

# Survival by Age Bucket
print("\nSurvival by AgeBucket:")
print(df.groupby("AgeBucket")["Survived"].mean())

# PLOTS
sns.barplot(x="Sex", y="Survived", data=df)
plt.title("Survival by Sex")
plt.savefig("outputs/survival_by_sex.png")
plt.clf()

sns.barplot(x="Pclass", y="Survived", data=df)
plt.title("Survival by Class")
plt.savefig("outputs/survival_by_class.png")
plt.clf()

sns.violinplot(x="Survived", y="Age", data=df)
plt.title("Age Distribution by Survival")
plt.savefig("outputs/survival_age_violin.png")
plt.clf()

print("All plots saved in /outputs folder.")
