Click to visit the [Seaborn](https://seaborn.pydata.org/#) and [Matplotlib](https://matplotlib.org/index.html) websites.

The manuscript of journal paper usually has a page width of 16 cm. As the final article has two columns, the figure for one column will have a width of 8 cm while the figure accrossing two columns will have a width of 16 cm.

**Change font size**
```
from matplotlib import rc
rc={'font.size':10, 
    'axes.labelsize': 10,   
    'legend.fontsize': 10, 
    'axes.titlesize': 10, 
    'xtick.labelsize': 10, 
    'ytick.labelsize': 10}
sns.set(font = 'Arial', rc=rc)
```

**Set figure size**
```
fig, ax = plt.subplots(1,1,figsize=(6,4))
```
Here, the unit of figure size is inches. So the 16*16 cm, 16*10.7 (aspect ratio is 6:4) cm, 8*8 cm and 8*5.3 cm is about 6.3*6.3 inch, 6.3*4.2 inch, 3.15*3.15 inch and 3.15*2.1 inch.