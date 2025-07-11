# Range

The **range** is the **difference between the maximum and minimum values** in a dataset.

Range = Maximum value - Minimum value



***

### Finding Range

***

#### **Graphical Steps in SPSS: Compute Range**

1. Open your student dataset in SPSS.
2. Go to **Analyze** → **Descriptive Statistics** → **Frequencies**
3. Move the following variables into the **Variable(s)** box:
   - `marks_assessment1`
   - `marks_assessment2`
   - `no_of_lateness`
4. Click **Statistics...**
   - Tick **Minimum**
   - Tick **Maximum**
5. Click **Continue**, then **OK**

#### SPSS Syntax to Get Min and Max (for Range):

```spss
FREQUENCIES VARIABLES=marks_assessment1 marks_assessment2 no_of_lateness
  /STATISTICS=MINIMUM MAXIMUM.
```

