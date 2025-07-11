# Frequency Table

A **frequency table** shows how often each **value or category** occurs in a dataset. It typically includes:

- **Frequency** (count)
- **Percent**
- **Valid Percent** (excluding missing data)
- **Cumulative Percent**

## Example Use Cases:

- Number of students getting each **grade category**

- Employee responses to a **Likert-scale** item (e.g., satisfaction level)

- Number of students with **different lateness counts**

  

***

### Create a Frequency Table

***

#### **Graphical Steps in SPSS: **

Let's say you want the frequency table for `no_of_lateness` in the **student dataset**:

1. Go to **Analyze** → **Descriptive Statistics** → **Frequencies**
2. Move the variable(s) into the **Variable(s)** box:
   - e.g., `no_of_lateness`
3. Make sure **“Display frequency tables”** is **ticked**
4. Click **OK**

#### SPSS Syntax

```spss
FREQUENCIES VARIABLES=no_of_lateness.
```

Or for multiple variables:

```spss
FREQUENCIES VARIABLES=no_of_lateness marks_assessment1.
```

