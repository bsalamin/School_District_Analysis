# School District Analysis: Challenge with Cheaters at Thomas High

## Skill Objectives:
1.	Open Jupyter Notebook files from local directories using a development environment.
2.	Read an external CSV file into a DataFrame.
3.	Format a DataFrame column.
4.	Determine data types of row values in a DataFrame.
5.	Retrieve data from specific columns of a DataFrame.
6.	Merge, filter, slice, and sort a DataFrame.
7.	Apply the groupby() function to a DataFrame.
8.	Use multiple methods to perform a function on a DataFrame.
9.	Perform mathematical calculations on columns of a DataFrame or Series.

## Analysis Objective:
* Using the Pandas loc method with conditional statements and comparison and logical operators, select the ninth-grade reading and math scores for Thomas High School. 
* Use the Pandas NumPy module to change the reading and math scores to NaN.
* Repeat the school district analysis you did in this module, and recreate the following metrics:
* The district summary
* The school summary
* The top 5 and bottom 5 performing schools, based on the overall passing rate
* The average math score for each grade level from each school
* The average reading score for each grade level from each school
* The scores by school spending per student, by school size, and by school type

## Results

### How is the district summary affected?
The district summary is largely unaffected…


##### Original:

<img width="934" alt="district_summary_og" src="https://user-images.githubusercontent.com/100387078/159999705-6b54890b-15e1-4a3f-a8e7-315d060fecdd.png">

##### New:

<img width="932" alt="district_summary_new" src="https://user-images.githubusercontent.com/100387078/159999730-39265401-1a01-439f-a64b-fa363c8870eb.png">

### How is the school summary affected?
The school summary changes dramatically. Thomas High School’s (THS) overall passing percentage drops nearly 30 percentage points.


##### Original:

![school_summ_og](https://user-images.githubusercontent.com/100387078/159999472-80c940f7-ec80-4dd2-87a0-7d252e1e0a07.png)

##### New:

![school_summ_new](https://user-images.githubusercontent.com/100387078/159999494-23a331e0-9fb6-4e8a-95c4-6894acb2254f.png)


### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
Thomas HS was originally ranked 2nd out of the 15 schools in the district. After removing the 9th graders scores due to allegations of academic dishonesty, THS drops down into the mid-field, far short of the top performers. However, if you only analyze THS scores for 10th thru 12th grade, then their scores drop nominally and their rank stays the same.


### How does replacing the ninth-grade scores affect the following:
#### Math and reading scores by grade
Now, there are no scores for THS in either subject under the 9th grade column.

##### Original:

![math_og](https://user-images.githubusercontent.com/100387078/159999561-8606bc9a-17d4-47a7-8e8a-7ae810552b00.png)
![reading_og](https://user-images.githubusercontent.com/100387078/159999578-30462e4b-7b66-4067-ade1-781c6e608a13.png)


##### New:

![math_new](https://user-images.githubusercontent.com/100387078/159999597-c3bf435e-8816-4ba9-8f32-444f08f6d16f.png)
![reading_new](https://user-images.githubusercontent.com/100387078/159999615-3030de09-f2e0-429c-b2e8-f90156832751.png)


#### Scores by school spending
Changes in the overall scores by school spending are nominal enough to not be detectable when compared to our original analysis.


##### Original:

![spending_og](https://user-images.githubusercontent.com/100387078/159999781-8daaa74f-3ad0-4217-8752-c8a7fe6a3093.png)


##### New:

![spending_new](https://user-images.githubusercontent.com/100387078/159999795-9a86f651-1c15-4b5a-a667-84555fa9ea4c.png)


#### Scores by school size
THS is categorized in the ‘Medium’ School Size. Changes to this table are again nominal and undetectable when compared to our original analysis.


##### Original:

![school_size_og](https://user-images.githubusercontent.com/100387078/159999903-bcbe5bcb-73c7-43a6-a7e9-1fc58f28af3e.png)


##### New:

![school_size_new](https://user-images.githubusercontent.com/100387078/159999922-08ed9a0e-7a3a-4b9d-bce6-06f6eeb42029.png)


#### Scores by school type
There was miniscule impact to our analysis at the School Type level by changing the 9th grade scores for THS.


##### Original:

![school_type_og](https://user-images.githubusercontent.com/100387078/160000025-f4b10b95-dea7-4dea-bfe1-a1b5dbcc8ec0.png)


##### New:

![school_type_new](https://user-images.githubusercontent.com/100387078/160000042-70e4d0a3-7685-45e7-99d6-237a2fa833cc.png)


## Results
1. The overall passing rate for THS dropped nearly 30 percentage points, from 91% to 65%.
2. With no data for THS 9th graders, their rank in the district drops from #2 to the mid-field.
3. If you ignore both grades and student count from the 9th grade at THS, the drop is much less dramatic and they hold their ranking in the district.
4. The effects of these changes are much more visible when looking at THS scores in comparison to the rest of the district; at the district level, the effect of nullifying reading and math grades for a few hundred students is much, much less noticable.
