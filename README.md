import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Student data
data = {
    "Name": ["Ali", "Sara", "Omar", "Ayesha", "Hassan"],
    "Math": [85, 90, 78, 92, 88],
    "Science": [80, 85, 75, 95, 82],
    "English": [78, 92, 88, 85, 80]
}

# DataFrame
df = pd.DataFrame(data)

# --- NumPy calculations ---
math_scores = np.array(df["Math"])
science_scores = np.array(df["Science"])
english_scores = np.array(df["English"])

print("📊 Statistics using NumPy:")
print("Average Math Marks:", np.mean(math_scores))
print("Highest Science Marks:", np.max(science_scores))
print("Lowest English Marks:", np.min(english_scores))
print("Standard Deviation (Math):", np.std(math_scores))

# Line plot using Seaborn
plt.figure(figsize=(8,6))
sns.lineplot(data=df.set_index("Name"))
plt.title("Student Marks Comparison", fontsize=14)
plt.xlabel("Students")
plt.ylabel("Marks")
plt.show()

# Bar chart using Matplotlib
df.plot(x="Name", kind="bar", figsize=(8,6))
plt.title("Marks of Students in Different Subjects")
plt.ylabel("Marks")
plt.show()
