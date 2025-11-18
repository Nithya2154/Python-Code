'''
Students mark analysis.py
-------------------------
1. Average by Subject and Student
2. Highest and Lowest Per Subject
3. Overall class Topper
4. Pass Count per Subject
5. Which Subject is Difficult
6. Ranking Students
 
'''
import numpy as np

np.random.seed(2)
students_mark_list = np.random.randint(10, 101, size=(20, 5))

# print("Student Mark Lists", '\n', students_mark_list)


# 1. Average by Subject and Student-------------------------------
avg_by_subjects = np.mean(students_mark_list, axis=0)
avg_by_students = np.mean(students_mark_list, axis=1)
print("Average by Subjects:", avg_by_subjects)
print("Average by Students:", avg_by_students)
# -----------------------------------------------------------------

# 2. Highest and Lowest Per Subject--------------------------------
highest = np.max(students_mark_list, axis=0)
lowest = np.min(students_mark_list, axis=0)
print("Highest Marks of Subject:", highest)
print("Lowest Marks of Subject:", lowest)
# -----------------------------------------------------------------

# 3. Overall class Topper with Average-----------------------------
over_all_class_topper = np.argmax(avg_by_students)
print("Topper of the Class:", over_all_class_topper,
      "with Average of", avg_by_students[over_all_class_topper])
# 3. Overall class Topper with Mark-------------------------------
total = np.sum(students_mark_list, axis=1)
over_all_class_topper = np.argmax(total)
print("Topper of the Class:", over_all_class_topper,
      "with Average of", total[over_all_class_topper])
# -----------------------------------------------------------------

# 4. Pass Count per Subject----------------------------------------
pass_fail = students_mark_list >= 40
pass_count = np.sum(pass_fail, axis=0)
print("Pass Count By Subject:", pass_count)
# -----------------------------------------------------------------

# 5. Which Subject is Difficult------------------------------------
diff_sub = np.argmin(avg_by_subjects)
print("The Difficult Subject Is:", diff_sub)
# -----------------------------------------------------------------

# 6. Ranking Students----------------------------------------------
ranks = np.argsort(np.argsort(-total)) + 1
print(ranks)
# -----------------------------------------------------------------
