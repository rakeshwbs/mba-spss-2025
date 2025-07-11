# Mode

The **mode** is the value that occurs **most frequently** in a dataset.

------

#### Key Characteristics:

- A dataset can have:
  - **One mode** → *Unimodal*
  - **Two modes** → *Bimodal*
  - **More than two modes** → *Multimodal*
  - **No mode** → when all values occur only once
- It is **not affected by outliers** or skewed distributions.

#### **Purpose in Descriptive Statistics:**

- The mode represents the **most common response or score**.
- Especially useful for:
  - **Categorical data** (e.g., most frequent department)
  - **Ordinal data** (e.g., most common lateness level)
  - **Integer-based test scores** (e.g., most common student mark)

***

### Finding the mode

***

####  **Graphical Steps in SPSS to Calculate Mode**

1. **Open SPSS** and load the `Student_Assessment_Dataset.csv`.
2. Go to **Analyze** → **Descriptive Statistics** → **Frequencies**
3. Move the following variables into the **Variable(s)** box:
   - `marks_assessment1`
   - `marks_assessment2`
   - `no_of_lateness`
4. Click **Statistics...**
5. Tick the checkbox for **Mode**
6. Click **Continue**, then **OK**

 SPSS will display the **mode** (most frequent value) for each of the selected variables.

#### SPSS Syntax to Compute Mode:

```spss
FREQUENCIES VARIABLES=marks_assessment1 marks_assessment2 no_of_lateness
  /STATISTICS=MODE.
```

