# Interquartile Range (IQR)

The **Interquartile Range (IQR)** is the **range between the 1st quartile (Q1)** and the **3rd quartile (Q3)** of a dataset:

#### IQR = Q3 - Q1

**Q1 (25th percentile):** 25% of the data falls below this value

**Q3 (75th percentile):** 75% of the data falls below this value

The IQR captures the **middle 50%** of the data — removing the influence of outliers



***

### Compute Interquartile Range (via Percentiles)

***

#### **Graphical Steps in SPSS: **

1. Go to **Analyze** → **Descriptive Statistics** → **Explore**
2. Move the variables:
   - `marks_assessment1`
   - `marks_assessment2`
   - `no_of_lateness`
      into the **Dependent List**
3. Under the **Display** section, select **Statistics**
4. Click **OK**

#### SPSS Syntax to Compute IQR:

```spss
EXAMINE VARIABLES=marks_assessment1 marks_assessment2 no_of_lateness
  /STATISTICS=DESCRIPTIVES PERCENTILES
  /PERCENTILES=25 75
  /MISSING=LISTWISE.
```



***

### Create Boxplots for IQR

***

#### **Graphical Steps in SPSS: **

1. Go to **Graphs** → **Legacy Dialogs** → **Boxplot**
2. Choose:
   - **Simple** boxplot
   - Select **"Summaries of separate variables"**
   - Click **Define**
3. In the **Boxplots Dialog**:
   - Move **one variable** (e.g., `marks_assessment1`) to the **Variable** box
   - You can repeat these steps for `marks_assessment2` and `no_of_lateness`
4. Click **OK**

#### SPSS Syntax for Boxplots

```spss
EXAMINE VARIABLES=marks_assessment1 marks_assessment2 
  /COMPARE VARIABLE 
  /PLOT=BOXPLOT
```

