import pandas as pd

# Load the dataset (update the filename if necessary)
df = pd.read_csv("spotify(3).csv")

# Display the first few rows to check the data structure
print("Initial dataset preview:")
print(df.head())

# Step 1: Remove unnecessary index columns (if present)
if 'Unnamed: 0' in df.columns:
    df.drop(columns=['Unnamed: 0'], inplace=True)

# Step 2: Handle duplicate tracks by keeping the most popular version
# Sorting by 'popularity' in descending order ensures the most popular track is retained
df = df.sort_values(by='popularity', ascending=False)
df = df.drop_duplicates(subset=['track_id'], keep='first')

# Step 3: Handle missing values
# Drop rows with missing essential values (adjust columns as needed)
df.dropna(subset=['popularity', 'track_name', 'artists', 'duration_ms'], inplace=True)

# Step 4: Convert categorical columns to lowercase and remove special characters for consistency
categorical_cols = ['artists', 'album_name', 'track_name', 'track_genre']
for col in categorical_cols:
    if col in df.columns:
        df[col] = df[col].str.lower().str.strip()

# Step 5: Save the cleaned dataset
df.to_csv("spotify_cleaned_fixed.csv", index=False)
print("Data cleaning complete. Saved as 'spotify_cleaned_fixed.csv'")
