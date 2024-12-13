```python
import pandas as pd

file_path = open('C:/Users/dinar/OneDrive/Documents/web_clienrs.csv', 'r', encoding='utf-8') 
data = pd.read_csv(file_path)

def analyze_age(age):
    if age > 25:
        return "Старше 25"
    else:
        return "Младше или равен 25"

data['Возраст_анализ'] = data['age'].apply(analyze_age)

print(data)

data.to_csv("customers_updated.csv", index=False)
```

                                                    name device_type  \
    0                      Allen  Miss. Elisabeth Walton      mobile   
    1                     Allison  Master. Hudson Trevor      tablet   
    2                       Allison  Miss. Helen Loraine      laptop   
    3               Allison  Mr. Hudson Joshua Creighton     desktop   
    4    Allison  Mrs. Hudson J C (Bessie Waldo Daniels)      laptop   
    ..                                               ...         ...   
    910                       Kallio  Mr. Nikolai Erland      tablet   
    911                   Kalvik  Mr. Johannes Halvorsen      mobile   
    912                                Karaic  Mr. Milan     desktop   
    913                    Karlsson  Mr. Einar Gervasius     desktop   
    914                Karlsson  Mr. Julius Konrad Eugen      laptop   
    
                   browser     sex   age  bill                           region  \
    0               Chrome  female  29.0   885                     St Louis: MO   
    1                Opera    male  48.0   850  Montreal: PQ / Chesterville: ON   
    2              Firefox  female  48.0  1034  Montreal: PQ / Chesterville: ON   
    3    Internet Explorer    male  30.0   214  Montreal: PQ / Chesterville: ON   
    4              Firefox  female  25.0   993  Montreal: PQ / Chesterville: ON   
    ..                 ...     ...   ...   ...                              ...   
    910              Opera    male  17.0  1273                                -   
    911              Opera    male  21.0  1136                                -   
    912              Opera    male  30.0   465                                -   
    913  Internet Explorer    male  21.0   275                                -   
    914              Opera    male  33.0   798                                -   
    
              Возраст_анализ  
    0              Старше 25  
    1              Старше 25  
    2              Старше 25  
    3              Старше 25  
    4    Младше или равен 25  
    ..                   ...  
    910  Младше или равен 25  
    911  Младше или равен 25  
    912            Старше 25  
    913  Младше или равен 25  
    914            Старше 25  
    
    [915 rows x 8 columns]
    


```python
file_path = open('C:/Users/dinar/OneDrive/Documents/web_clienrs.csv', 'r', encoding='utf-8') 
data = pd.read_csv(file_path)

filtered_data = data[(data['sex'] == 'male') & (data['age'] > 30)]

print(filtered_data)


```

                                              name device_type            browser  \
    1               Allison  Master. Hudson Trevor      tablet              Opera   
    5                          Anderson  Mr. Harry      mobile            Firefox   
    7                       Andrews  Mr. Thomas Jr      tablet  Internet Explorer   
    9                      Artagaveytia  Mr. Ramon      mobile            Firefox   
    10                      Astor  Col. John Jacob     desktop             Chrome   
    ..                                         ...         ...                ...   
    900  Johnston  Master. William Arthur "Willie"     desktop             Chrome   
    902                     Johnston  Mr. Andrew G      tablet  Internet Explorer   
    905                          Jonsson  Mr. Carl     desktop            Firefox   
    909                        Jussila  Mr. Eiriik     desktop            Firefox   
    914          Karlsson  Mr. Julius Konrad Eugen      laptop              Opera   
    
          sex   age  bill                           region  
    1    male  48.0   850  Montreal: PQ / Chesterville: ON  
    5    male  48.0   371                     New York: NY  
    7    male  39.0   867                      Belfast: NI  
    9    male  71.0   926              Montevideo: Uruguay  
    10   male  47.0   100                     New York: NY  
    ..    ...   ...   ...                              ...  
    900  male  33.0   840                                -  
    902  male  33.0   762                                -  
    905  male  32.0  1136                                -  
    909  male  32.0   280                                -  
    914  male  33.0   798                                -  
    
    [374 rows x 7 columns]
    


```python

```
