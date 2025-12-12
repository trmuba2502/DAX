# DAX
This is my note while discovering DAX language

#### What does DAX stand for
* D: Data 
* A: Analysis 
* X: eXpressions
 
## Understanding the data model

DAX is specifically designed to compute business formulas over a data model

#### Data model
* Data model is a set of tables, linked by relationships.

#### Tables
* Set of rows containing data, each row divided into columns, each column has a data type and contains a single piece of information

#### Aspects of relaionships
* Two tables in a relationship do not have the same role
* One-side: 1-1 relationships
* Many-side: weak relationships
* The columns used to create the relationship, which usually have the same name in both tables **keys of the relationship**

| one-side      | many side     |
| ------------- |-------------|
| column needs to have a unique value for each row      | the same value can be repeated in many different rows     |
| cannot contain blanks      |      |

* **key for the table:**  a column has a unique value for each row
* **Relationships can form a chain:** product ---> subcategory ---> category => each product has a category
* In each relationship, one or two small arrows can determine the cross filter direction. The **arrow** indicates the **direction** of the automatic filtering of the relationship `cross filter`

<figure>
  <img src="Images\1_1.png" alt="Mô tả ảnh">
  <figcaption> Figure 1-1 This data model is made up of six tables.</figcaption>
</figure>

e.g. relationship between `Sales` and `Product`: 2 arrows; all others relationship: 1 arrow

### Understanding the direction of a relationship
* `Unidirectional cross filter`
* `Bidirectional cross filter`: 2 arrows

