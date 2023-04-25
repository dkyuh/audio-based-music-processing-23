# Imports


```python
import numpy as np
import matplotlib.pyplot as plt
from IPython.display import Audio
```

# Nyquist-Grenze


```python
for freq in range(0, 100):

    sr = 100
    amp = 0.5
    t = np.arange(sr) / sr * 2 * np.pi

    x = amp * np.sin( t * freq )

    plt.figure(figsize=(12, 4))
    plt.plot(x, '-')
    plt.ylim(-1, 1)
    plt.show()
```


    
![png](output_3_0.png)
    



    
![png](output_3_1.png)
    



    
![png](output_3_2.png)
    



    
![png](output_3_3.png)
    



    
![png](output_3_4.png)
    



    
![png](output_3_5.png)
    



    
![png](output_3_6.png)
    



    
![png](output_3_7.png)
    



    
![png](output_3_8.png)
    



    
![png](output_3_9.png)
    



    
![png](output_3_10.png)
    



    
![png](output_3_11.png)
    



    
![png](output_3_12.png)
    



    
![png](output_3_13.png)
    



    
![png](output_3_14.png)
    



    
![png](output_3_15.png)
    



    
![png](output_3_16.png)
    



    
![png](output_3_17.png)
    



    
![png](output_3_18.png)
    



    
![png](output_3_19.png)
    



    
![png](output_3_20.png)
    



    
![png](output_3_21.png)
    



    
![png](output_3_22.png)
    



    
![png](output_3_23.png)
    



    
![png](output_3_24.png)
    



    
![png](output_3_25.png)
    



    
![png](output_3_26.png)
    



    
![png](output_3_27.png)
    



    
![png](output_3_28.png)
    



    
![png](output_3_29.png)
    



    
![png](output_3_30.png)
    



    
![png](output_3_31.png)
    



    
![png](output_3_32.png)
    



    
![png](output_3_33.png)
    



    
![png](output_3_34.png)
    



    
![png](output_3_35.png)
    



    
![png](output_3_36.png)
    



    
![png](output_3_37.png)
    



    
![png](output_3_38.png)
    



    
![png](output_3_39.png)
    



    
![png](output_3_40.png)
    



    
![png](output_3_41.png)
    



    
![png](output_3_42.png)
    



    
![png](output_3_43.png)
    



    
![png](output_3_44.png)
    



    
![png](output_3_45.png)
    



    
![png](output_3_46.png)
    



    
![png](output_3_47.png)
    



    
![png](output_3_48.png)
    



    
![png](output_3_49.png)
    



    
![png](output_3_50.png)
    



    
![png](output_3_51.png)
    



    
![png](output_3_52.png)
    



    
![png](output_3_53.png)
    



    
![png](output_3_54.png)
    



    
![png](output_3_55.png)
    



    
![png](output_3_56.png)
    



    
![png](output_3_57.png)
    



    
![png](output_3_58.png)
    



    
![png](output_3_59.png)
    



    
![png](output_3_60.png)
    



    
![png](output_3_61.png)
    



    
![png](output_3_62.png)
    



    
![png](output_3_63.png)
    



    
![png](output_3_64.png)
    



    
![png](output_3_65.png)
    



    
![png](output_3_66.png)
    



    
![png](output_3_67.png)
    



    
![png](output_3_68.png)
    



    
![png](output_3_69.png)
    



    
![png](output_3_70.png)
    



    
![png](output_3_71.png)
    



    
![png](output_3_72.png)
    



    
![png](output_3_73.png)
    



    
![png](output_3_74.png)
    



    
![png](output_3_75.png)
    



    
![png](output_3_76.png)
    



    
![png](output_3_77.png)
    



    
![png](output_3_78.png)
    



    
![png](output_3_79.png)
    



    
![png](output_3_80.png)
    



    
![png](output_3_81.png)
    



    
![png](output_3_82.png)
    



    
![png](output_3_83.png)
    



    
![png](output_3_84.png)
    



    
![png](output_3_85.png)
    



    
![png](output_3_86.png)
    



    
![png](output_3_87.png)
    



    
![png](output_3_88.png)
    



    
![png](output_3_89.png)
    



    
![png](output_3_90.png)
    



    
![png](output_3_91.png)
    



    
![png](output_3_92.png)
    



    
![png](output_3_93.png)
    



    
![png](output_3_94.png)
    



    
![png](output_3_95.png)
    



    
![png](output_3_96.png)
    



    
![png](output_3_97.png)
    



    
![png](output_3_98.png)
    



    
![png](output_3_99.png)
    

