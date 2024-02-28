# outliers
```
import pandas as pd
import seaborn as sns
age=[1,3,28,27,25,92,30,39,40,50,26,24,29,94]
af=pd.DataFrame(age)
af
```

<img width="199" alt="image" src="https://github.com/Jeevapriya14/outliers/assets/121003043/8f16c272-c5c8-4d99-87c5-67b2e8317f3b">

```
sns.boxplot(data=af)
```

<img width="331" alt="image" src="https://github.com/Jeevapriya14/outliers/assets/121003043/e33c5787-17f3-4eb9-9ab4-d1c417c84c9d">

```
sns.scatterplot(data=af)
```

<img width="420" alt="image" src="https://github.com/Jeevapriya14/outliers/assets/121003043/e74150c6-744a-4526-a99a-41e20f844b32">

```
q1=af.quantile(0.25)
q2=af.quantile(0.5)
q3=af.quantile(0.75)
iqr=q3-q1
iqr
```

<img width="80" alt="image" src="https://github.com/Jeevapriya14/outliers/assets/121003043/162037a7-d24e-40fa-9b9d-94f231cc64b3">

```
low=q1-1.5*iqr
low
```

<img width="88" alt="image" src="https://github.com/Jeevapriya14/outliers/assets/121003043/4eb0c2c0-ec8f-45f9-a220-1492df6da1b3">

```
high=q3+1.5*iqr
high
```

<img width="96" alt="image" src="https://github.com/Jeevapriya14/outliers/assets/121003043/48213a8a-6851-4236-a71a-aed5a7e688ff">

```
af=af[((af>=low)&(af<=high))]
af
```

<img width="152" alt="image" src="https://github.com/Jeevapriya14/outliers/assets/121003043/d7152c2f-03dd-4a6c-bbd3-f8b20029dac4">

```
af.dropna()
```

<img width="116" alt="image" src="https://github.com/Jeevapriya14/outliers/assets/121003043/fd1a33de-45ef-4c29-8dab-76c45cded230">

```
sns.boxplot(data=af)
```

<img width="319" alt="image" src="https://github.com/Jeevapriya14/outliers/assets/121003043/245eadda-7184-4224-ba33-02562d399bcf">

```
data=[1,12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,72,75,78,81,84,87,90,93,96,99,158]
df=pd.DataFrame(data)
df
```

<img width="92" alt="image" src="https://github.com/Jeevapriya14/outliers/assets/121003043/5301b7b2-4d45-4de9-8325-977728782e28">
