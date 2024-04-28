# Myproject2024

### Palmer Penguins
***
#### Overview: 

The Palmer Penguin dataset provides information about penguins observed in Palmer Station, Antarctica. This dataset includes various features related to the penguins' physical characteristics and habitats. Here's an overview of the dataset:

![](https://allisonhorst.github.io/palmerpenguins/reference/figures/lter_penguins.png)

### Penguins Dataset:
***

https://raw.githubusercontent.com/mwaskom/seaborn-data/master/penguins.csv
***

### Libraries:

* **Pandas:**
Pandas is a powerful data manipulation and analysis library for Python. It provides data structures and functions to efficiently manipulate and analyze structured data.

* **Seaborn:**
Seaborn is a statistical data visualization library built on top of Matplotlib. It provides a high-level interface for creating informative and visually appealing statistical graphics.

* **Matplotlib:** 
Matplotlib is a comprehensive plotting library for Python. It provides a wide range of plotting functions to create static, interactive, and publication-quality visualizations.

* **NumPy:**
NumPy is a fundamental package for scientific computing with Python. It provides support for large, multi-dimensional arrays and matrices, along with a collection of mathematical functions to operate on these arrays efficiently.
***
<img width="642" alt="Screenshot 2024-04-26 at 21 07 18" src="https://github.com/CarlosRigueti/Myproject2024/assets/159485788/8bb177a1-858e-4176-bb5b-1ce71763c33f">

### Load Data:
***

* #### Load the penguins dataset
  
**penguins_df = pd.read_csv:**("https://raw.githubusercontent.com/mwaskom/seaborn-data/master/penguins.csv")

* #### Have a look.
  
**penguins_df:**

* Species: The species of penguins observed, such as Adelie, Chinstrap, or Gentoo.
* Island: The island where the penguins were observed, such as Torgersen, Biscoe, or Dream.
* Bill Length (mm): The length of the penguins' bills, measured in millimeters.
* Bill Depth (mm): The depth of the penguins' bills, measured in millimeters.
 *Flipper Length (mm): The length of the penguins' flippers, measured in millimeters.
* Body Mass (g): The body mass or weight of the penguins, typically measured in grams.
* Sex: The gender of the penguins, represented as categorical data (e.g., male, female).
* Age: The age category of the penguins, indicating whether they are 'adult' or 'juvenile'.
* Year: The year in which the penguin observations were recorded.
* Region: The region or location where the observations were made, which could include specific research stations or geographical coordinates.
***
<img width="697" alt="Screenshot 2024-04-26 at 21 10 59" src="https://github.com/CarlosRigueti/Myproject2024/assets/159485788/09c07dfa-704a-490a-a078-f4cbae851883">


***
* #### Inspect types.
penguins_df.dtypes

* Species: This column contains categorical data represented as strings (object data type). It likely specifies the species of penguins observed, such as Adelie, Chinstrap, or Gentoo.
* Island: Another categorical column represented as strings (object data type). It indicates the island where the penguins were observed, such as Torgersen, Biscoe, or Dream.
* Bill Length (mm): This column contains numerical data represented as floating-point numbers (float64 data type). It represents the length of the penguins' bills, measured in millimeters (mm).
* Bill Depth (mm): Similar to the previous column, this column also contains numerical data represented as floating-point numbers (float64 data type). It represents the depth of the penguins' bills, measured in millimeters (mm).
* Flipper Length (mm): Another numerical column represented as floating-point numbers (float64 data type). It indicates the length of the penguins' flippers, measured in millimeters (mm).
* Body Mass (g): This column contains numerical data represented as floating-point numbers (float64 data type). It specifies the body mass or weight of the penguins, typically measured in grams (g).
* Sex: Another categorical column represented as strings (object data type). It indicates the gender of the penguins observed, such as Male, Female, or possibly Unknown.

<div class="container">
    <div class="column">
        <pre>
species               object
island                object
bill_length_mm       float64
bill_depth_mm        float64
flipper_length_mm    float64
body_mass_g          float64
sex                   object
dtype: object
        </pre>
    </div>
</div>

</body>
</html>

***
* ### Summary.
penguins_df.describe()

The overview provides descriptive statistics for four numerical features related to penguins:

#### Bill Length (mm):
* *Count*: 342 penguins have measurements for bill length.
* *Mean*: The average bill length is approximately 43.92 millimeters.
* *Standard Deviation*: The variability in bill length is approximately 5.46 millimeters.
* *Minimum*: The shortest bill length observed is 32.1 millimeters.
* *25th Percentile*: 25% of the penguins have a bill length of 39.23 millimeters or less.
* *Median (50th Percentile)*: 50% of the penguins have a bill length of 44.45 millimeters or less.
* *75th Percentile*: 75% of the penguins have a bill length of 48.5 millimeters or less.
* *Maximum*: The longest bill length observed is 59.6 millimeters.
#### Bill Depth (mm):
* Similar statistics to bill length, but for bill depth measurements.
#### Flipper Length (mm):
* Similar statistics to bill length, but for flipper length measurements.
#### Body Mass (g):
* Similar statistics to bill length, but for body mass measurements in grams.


  
<img width="573" alt="Screenshot 2024-04-26 at 21 39 39" src="https://github.com/CarlosRigueti/Myproject2024/assets/159485788/7808df6a-4986-402a-b092-e4cd20e51ca4">

***

### Display:
***
<img width="565" alt="Screenshot 2024-04-26 at 22 23 16" src="https://github.com/CarlosRigueti/Myproject2024/assets/159485788/6bcf341a-7aea-47d6-be94-7069de827f65">


* Overall, displaying information about dataset, including samples of categorical data and verifying the presence of specific columns, is crucial for ensuring data quality, facilitating data exploration, and gaining initial insights into the dataset's content. It forms the foundation for further analysis and interpretation of the data.


| Categorical data |       |
|------------------|-------|
| Species          | Island|
| Adelie           | Torgersen |
| Adelie           | Torgersen |
| Adelie           | Torgersen |
| Adelie           | Torgersen |
| Adelie           | Torgersen |

***

<img width="993" alt="Screenshot 2024-04-28 at 08 55 48" src="https://github.com/CarlosRigueti/Myproject2024/assets/159485788/84d32560-578d-4119-8835-f371149b8a75">


These commands work together to select specific columns from the original DataFrame, assign them to a new variable for easier manipulation, and then print the first few rows of the selected columns to provide an overview of the data. They are commonly used in exploratory data analysis to understand the dataset's content and structure.

#### *selected_columns = penguins_df*:
* It creates a reference to the original DataFrame rather than making a copy. Therefore, any changes made to selected_columns will affect the original penguins_df DataFrame.

#### *print(selected_columns.head())*:

* This command prints the first few rows of the DataFrame selected_columns

* By using print(), the output of selected_columns.head() is displayed in the console or notebook cell output.



<table>
  <tr>
    <th>Species</th>
    <th>Island</th>
    <th>Bill Length (mm)</th>
    <th>Bill Depth (mm)</th>
    <th>Flipper Length (mm)</th>
    <th>Body Mass (g)</th>
    <th>Sex</th>
  </tr>
  <tr>
    <td>Adelie</td>
    <td>Torgersen</td>
    <td>39.1</td>
    <td>18.7</td>
    <td>181.0</td>
    <td>3750.0</td>
    <td>MALE</td>
  </tr>
  <tr>
    <td>Adelie</td>
    <td>Torgersen</td>
    <td>39.5</td>
    <td>17.4</td>
    <td>186.0</td>
    <td>3800.0</td>
    <td>FEMALE</td>
  </tr>
  <tr>
    <td>Adelie</td>
    <td>Torgersen</td>
    <td>40.3</td>
    <td>18.0</td>
    <td>195.0</td>
    <td>3250.0</td>
    <td>FEMALE</td>
  </tr>
  <tr>
    <td>Adelie</td>
    <td>Torgersen</td>
    <td>NaN</td>
    <td>NaN</td>
    <td>NaN</td>
    <td>NaN</td>
    <td>NaN</td>
  </tr>
  <tr>
    <td>Adelie</td>
    <td>Torgersen</td>
    <td>36.7</td>
    <td>19.3</td>
    <td>193.0</td>
    <td>3450.0</td>
    <td>FEMALE</td>
  </tr>
</table>

</body>
</html>

### Two Variables:
***

<img width="775" alt="Screenshot 2024-04-28 at 09 29 04" src="https://github.com/CarlosRigueti/Myproject2024/assets/159485788/5fc2e449-ca64-49c2-a683-cebc125843e7">

The main purpose of these two variables, flipper_length and body_mass, in the context of the given code, is to analyze the relationship between two specific characteristics of penguins:

* ***flipper_length:***
This variable represents the flipper lengths (in millimeters) of the penguins in the dataset.
The flipper length is a physical characteristic of penguins that can vary among different species and individuals.
Analyzing flipper length can provide insights into the morphological differences or adaptations among penguin species, as well as potential relationships with other variables such as body mass or habitat.
* ***body_mass:***
This variable represents the body masses (in grams) of the penguins in the dataset.
Body mass is another important physical characteristic of penguins, which is closely related to their overall health, fitness, and ecological niche.
Analyzing body mass can help understand the energetic requirements, reproductive strategies, and ecological roles of different penguin species.


*The correlation coefficient between **flipper_length** and **body_mass**, the code aims to quantify the strength and direction of the linear relationship between these two variables.* 

***

### Add a Best Fit Line:
***


