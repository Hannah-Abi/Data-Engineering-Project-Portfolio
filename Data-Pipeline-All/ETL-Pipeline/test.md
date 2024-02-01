## Applying advanced transformations to DataFrames
- pandas has a plethora of built-in transformation tools, but sometimes, more advanced logic needs to be used in a transformation. The apply function lets you apply a user-defined function to a row or column of a DataFrame, opening the door for advanced transformation and feature generation.
- The find_street_name() function parses the street name from the "street_address", dropping the street number from the string. This function has been loaded into memory, and is ready to be applied to the raw_testing_scores DataFrame.
- ```
  def transform(raw_data):
	# Use .loc[] to only return the needed columns
	raw_data = raw_data.loc[:, ["city", "math_score", "reading_score", "writing_score"]]
	
    # Group the data by city, return the grouped DataFrame
	grouped_data = raw_data.groupby(by=["city"], axis=0).mean()
	return grouped_data

# Transform the data, print the head of the DataFrame
grouped_testing_scores = transform(raw_testing_scores)
print(grouped_testing_scores.head())
```
