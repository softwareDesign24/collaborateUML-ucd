usecase-beta
      title Student Management System Use Cases

      actor Student
      actor Admin
      service Authentication
      service Grades as Grades Database
      service Courses

      systemboundary
        title Student Management System
        (Login) 
        (Submit Assignment)
        (View) as (View Grades)
        (Manage Users) 
        (Manage Courses)
        (Generate Reports)
        (View Grades) 
      end

      Student -> (Login) -> Authentication
      Student -> (Submit Assignment) -> Courses
      Student -> (View) -> Grades
      Admin -> (Login) -> Authentication
      Admin -> (Manage Users) -> Courses
      Admin -> (Manage Courses) -> Courses
      Admin -> (Generate Reports) -> Courses, Grades
      Admin -> (View) -> Grades
