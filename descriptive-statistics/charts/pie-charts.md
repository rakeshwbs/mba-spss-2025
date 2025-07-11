# Pie-Charts

A **pie chart** is a circular graph divided into slices, where each slice represents a **category's proportion or percentage** of the total.

### **When to Use:**

- To show the **distribution of students** by:

  - `gender`
  - `lateness_level`
  - `grade_band`

- Ideal for visualizing how much **each group contributes to a whole**

  

***

### Create a Pie Chart

***

#### **Graphical Steps in SPSS:**

Let’s create a **pie chart for `lateness_level`**:

1. Go to **Graphs** → **Legacy Dialogs** → **Pie...**
2. Choose:
   - **"Summaries for groups of cases"**
   - Click **Define**
3. In the **Define Pie Chart** dialog:
   - Move `lateness_level` into the **Define Slices by** box
   - Choose **Frequencies** (to count the number of cases)
4. Click **OK**

#### SPSS Syntax

```spss
GRAPH
  /PIE=COUNT BY lateness_level
  /TITLE='Pie Chart of Lateness Level'.
```

#### Interpretation:

- The **larger the slice**, the more students fall into that category.
- Great for quickly understanding **dominant groups** or **imbalances** (e.g., many students in "Moderate" lateness).