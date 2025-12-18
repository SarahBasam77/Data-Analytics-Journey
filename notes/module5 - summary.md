# Module 5 Quick Reference

## Descriptive vs Inferential
| Descriptive | Inferential |
|-------------|-------------|
| Summarizes data | Makes predictions |
| Shows what is | Shows what might be |
| No comparisons | Compares groups |
| Charts, averages | Hypotheses, conclusions |

## Chart Selection Guide
**Line Chart** → Time trends
**Column Chart** → Category comparisons
**Bar Chart** → Long category names
**Pie Chart** → Parts of whole (%)
**Scatter Plot** → Relationships/correlations

## Big Data Methods
1. **Cluster**: Group similar items
2. **Association**: Find patterns (X → Y)
3. **Regression**: Predict outcomes

## Outlier Rules
1. **Investigate** all outliers
2. **Decide**: Mistake or meaningful?
3. **Handle**: Correct or analyze
4. **Document**: Why kept/removed

## Key Questions
- Descriptive or inferential needed?
- Which chart type fits the data?
- Sample representative of population?
- Outliers present? How handled?

## Pro Tips
- Start y-axis at 0 for accurate proportions
- Limit pie chart segments to ≤10
- Use scatter plots for outlier detection
- Always label charts clearly

# VLOOKUP:
is a powerful Excel function for finding and retrieving data from large tables. It searches the leftmost column of a table for a specified value and returns information from the same row in another column.

## Key Details
- Stands for "vertical lookup"
- Requires 4 arguments: lookup value, table range, return column number, and match type (exact=FALSE, approximate=TRUE)
- Searches only the first column of the specified range
- Defaults to approximate match unless FALSE is specified

## Common Uses:
1. Finding specific data - Like retrieving a movie's budget when given its title
2. Data cleaning - Identifying duplicates between two lists/columns

# Comparison with XLOOKUP:
XLOOKUP is newer, searches any column (not just the leftmost), and defaults to exact matches
XLOOKUP is not backward compatible with older Excel versions

## Advanced Tip:
Combine with IF and ISNA functions to display custom messages (like "Duplicate"/"Unique") instead of error codes.
