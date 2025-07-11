# Bar Charts

A **bar chart** displays the **frequency** or **summary values** (like mean) for each category of a **categorical variable** using **rectangular bars**. Each bar's height reflects the value it represents.

### **When to Use:**

- To show the **number of students** in each **lateness level** (`Low`, `Moderate`, `High`)
- To compare **average marks by department**, **sales by region**, or **responses on a Likert scale**



***

### Create a Bar Chart

***

####  Graphical Steps in SPSS: 

Suppose you want to show the **number of students by `lateness_level`**:

1. Go to **Graphs** → **Legacy Dialogs** → **Bar...**
2. Select:
   - **Simple**
   - **"Summaries for groups of cases"**
   - Click **Define**
3. In the **Define Bar Chart** dialog:
   - Select `lateness_level` as the **Category Axis**
   - Click **OK**

#### SPSS Syntax

```spss
GRAPH
  /BAR(SIMPLE)=COUNT BY lateness_level
  /TITLE='Bar Chart of Lateness Level'.
```



***

### Clustered Bar Chart

***

#### **Objective:**

We want to see how **lateness_level** varies by a grouping variable like:

- `gender` (if available)
- or a new one like `grade_band` or `score_category` (can be created from marks)

------

####  **Assumption for This Example:**

Let’s assume we’re comparing:

- `lateness_level` (**row/group**)
   **by**
- `gender` (**column**)

####  **Graphical Steps in SPSS: Clustered Bar Chart**

1. Go to **Graphs** → **Legacy Dialogs** → **Bar…**
2. Choose:
   - **Clustered**
   - **"Summaries for groups of cases"**
   - Click **Define**
3. In the **Define Clustered Bar Chart** dialog:
   - Set `lateness_level` as the **Category Axis**
   - Set `gender` as the **Define Clusters by** variable
4. Click **OK**

#### SPSS Syntax

```spss
GRAPH
  /BAR(GROUPED)=COUNT BY lateness_level BY gender
  /TITLE='Clustered Bar Chart of Lateness Level by Gender'.
```

### How to Interpret:

- Each **cluster** shows the comparison between groups **within one category**
- Useful for identifying patterns like:
  - "Are **males** more frequently in the 'High' lateness category?"
  - "Do **females** dominate the 'Low' category?"