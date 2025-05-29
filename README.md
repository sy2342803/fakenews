# fakenews
import kagglehub

# Download latest version
path = kagglehub.dataset_download("razanaqvi14/real-and-fake-news")

print("Path to dataset files:", path)


import pandas as pd
import os

csv = pd.read_csv(os.path.join(path, "Fake.csv"))

fake_df = pd.DataFrame(csv)

fake_df

csv = pd.read_csv(os.path.join(path, "True.csv"))

real_df = pd.DataFrame(csv)

real_df
