# Cross-tabulation

**Cross-tabulation** (or **crosstab**) is a statistical tool that displays the **frequency distribution** of two or more **categorical variables** in a table format. It shows how the variables are **related** or **associated** with each other.

### Key Features:

- Each **cell** in the table shows the **count** (and optionally the **percentage**) of cases for a **combination** of the variable categories.
- It helps answer questions like:
   🔸 "Is there a relationship between gender and lateness?"
   🔸 "How does department relate to employee satisfaction level?"

### Uses of Cross-tabulation:

- Discover **patterns**, **trends**, or **associations** between variables.

- Foundation for **Chi-square test** to assess **statistical significance** of relationships.

- Common in **market research**, **HR analytics**, and **survey analysis**.

  

***

### Create Cross-tabulation

#### **Example Scenario: Cross-tab from Student Dataset**

Suppose you want to **cross-tabulate**:

- `no_of_lateness` (number of times late)
   **against**
- a **new variable** called `lateness_level` (e.g., `"Low"`, `"Moderate"`, `"High"` lateness group)

We will:

1. Create a **categorical version** of lateness called `lateness_level`
2. Run a **crosstab** on `lateness_level` vs another variable (e.g., `average_score_category`)

#### STEP 1: Categorize `no_of_lateness` into `lateness_level`

#### 🖱️ Graphical Method (Recode in SPSS):

1. Go to **Transform** → **Recode into New Variable**
2. Select `no_of_lateness`, click **→**
3. Name the new variable: `lateness_level`
4. Click **Old and New Values**:
   - `0–1` → New value: `"Low"`
   - `2–3` → New value: `"Moderate"`
   - `4–6` → New value: `"High"`
5. Click **Continue**, then **OK**

#### SPSS Syntax to Create `lateness_level`:

```spss
RECODE no_of_lateness (0 thru 1 = 1) (2 thru 3 = 2) (4 thru 6 = 3) INTO lateness_level.
VARIABLE LABELS lateness_level 'Categorical lateness: 1=Low, 2=Moderate, 3=High'.
VALUE LABELS lateness_level 1 'Low' 2 'Moderate' 3 'High'.
EXECUTE.
```

#### STEP 2: Create a Cross-tab (lateness_level × gender or performance category)

f you already have another categorical variable like `gender` or `average_score_category`, do this:

#### 🖱️ Graphical Method:

1. Go to **Analyze** → **Descriptive Statistics** → **Crosstabs**
2. Move:
   - `lateness_level` → **Row**
   - `gender` or another category variable → **Column**
3. Click **Cells...**
   - Tick **Observed**, **Row %, Column %, Total %** if needed
4. Click **Continue**, then **OK**

#### SPSS Syntax:

```spss
CROSSTABS
  /TABLES=lateness_level BY gender
  /FORMAT=AVALUE TABLES
  /CELLS=COUNT ROW COLUMN TOTAL.
```

Replace `gender` with any other categorical variable if needed.