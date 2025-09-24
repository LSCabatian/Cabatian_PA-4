Dataframe 1.
``` python
import pandas as pd
#Input of the board2.xlsx file
df = pd. read_excel ("board2.xlsx" )
df ['Average'] = df.mean (numeric_only=True, axis=1)
df
```
![image](https://github.com/user-attachments/assets/e9b3e1c2-d41e-4909-8ff8-93b368a2a2f5)
![image](https://github.com/user-attachments/assets/220ecb27-36f4-4f46-8371-ea651670fd39)

```python
#Function to print the instruction asked.
print("--Instru--")
Instru = df.loc[(df.Track=="Instrumentation") & (df.Hometown=="Luzon") & (df.Electronics>70), ['Name', 'GEAS' , 'Electronics']]
Instru
```
![image](https://github.com/user-attachments/assets/33aac526-78ff-4804-82b1-0a88ab8502b7)

```python
#Function to print the instruction asked.
print("—-Mindy--")
Mindy = df.loc[(df.Hometown=="Mindanao") & (df.Gender=="Female") & (df.Average>=55) , ['Name', 'Track', 'Electronics', 'Average']]
Mindy
```
![image](https://github.com/user-attachments/assets/d267b642-8d87-4ecf-a3ba-ea70f5dfe60c)

Dataframe 2.
```python
import matplotlib.pyplot as plt

#Function to print the graph that states the correlation of chosen track to grades.
plt.figure (figsize=(5,6))
plt.bar (df ['Track'], df ['Average'])
plt.xlabel ("Chosen Track in College") 
plt.ylabel ("Average")
plt.title ("Table 1.1: A bar graph showing the relationship of chosen track in college .")
```
![image](https://github.com/user-attachments/assets/89e83c0e-116f-446e-ba72-cfb4d5c9e831)

``` python
#Function to print the graph that states the correlation of gender to grades.
plt.figure (figsize=(5,6))
plt.bar (df ['Gender'], df ['Average'])
plt.xlabel ("'Gender")
plt.ylabel ("Average")
plt.title ("Table 1.2: A bar graph showing the relationship of gender and average grade.")
```
![image](https://github.com/user-attachments/assets/4d6dfc50-2e75-44e4-a813-d2613de2ac98)

```python
#Function to print the graph that states the correlation of hometown to grades.
plt.figure(figsize=(5,6))
plt.bar (df['Hometown'],df ['Average'])
plt.xlabel ("Hometown" ) 
plt.ylabel ("Average")
plt.title ("Table 1.3: A bar graph showing the relationship of hometown and average grade.")
```
![image](https://github.com/user-attachments/assets/42e54c24-8656-4617-9e12-444d670f5d66)




