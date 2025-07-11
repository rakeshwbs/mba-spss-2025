## Line Charts

A **line chart** connects data points using a line to show how a **value changes over time** or across **ordered groups**.

### **When to Use:**

- To show **student marks over assessment periods**
- To display **sales, satisfaction, attendance, or performance trends**
- Compare **average scores** across **lateness levels**

***

### Create a Line Chart

***

**Example 1: Line Chart of Average Marks Across Lateness Levels**

#### **Graphical Steps in SPSS:**

1. Go to **Graphs** → **Legacy Dialogs** → **Line...**
2. Select:
   - **Simple**
   - **"Summaries for groups of cases"**
   - Click **Define**
3. In the dialog box:
   - Choose the **category axis**: e.g., `lateness_level`
   - Choose the **summary variable**: e.g., `marks_assessment1`
4. Click **OK**

#### SPSS Syntax

```spss
GRAPH
  /LINE(SIMPLE)=MEAN(marks_assessment1) BY lateness_level
  /TITLE='Line Chart of Marks vs. Lateness Level'.
```

####  Interpretation:

- Useful for showing whether **lateness affects performance**
- A **downward slope** might indicate that students with **higher lateness** perform **worse**