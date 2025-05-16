
import pandas as pd

try:
    df = pd.read_csv('sentimentdataset.csv')
    display(df.head())
    print(df.shape)
except FileNotFoundError:
    print("Error: 'sentimentdataset.csv' not found.")
    df = None
except pd.errors.ParserError:
    print("Error: Could not parse the CSV file. Check the file format.")
    df = None
except Exception as e:
    print(f"An unexpected error occurred: {e}")
    df = None
    # Examine Data Shape and Types
print(f"Data shape: {df.shape}")
print("\nData Types:")
print(df.dtypes)

