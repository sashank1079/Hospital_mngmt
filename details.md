# Hospital_mngmt
Java Swing application to manage a hospital ecosystem


![image](https://github.com/sashank1079/Hospital_mngmt/assets/122720872/f765f680-ff00-430c-bf66-0c524a9e8945)


                                                    BASE UNIVERISTY MODEL
The collection of data about departments, courses, faculty, and students is given a lot of importance in the given university model. However, it is biased in favour of research and disregards crucial elements like student and alumnus feedback, which truly determine the value of the university. Additionally, there are few resources available and performance metrics are not taken into account when faculty and students choose a university. In conclusion, the current university model includes some classes but ignores crucial factors that ought to be taken into account.

  ![image](https://github.com/sashank1079/Hospital_mngmt/assets/122720872/1e42972d-1c6c-4721-83b8-2f6817fffbb0)

The above-mentioned classes are some of the important classes that help build the university model. These classes use the traditional methods to keep track of the student and faculty data. There is no standardized format to get feedback from faculty and students and rank a particular university. Students have to refer to various sources which often leads to scepticism about which university is the best fit for them, and which university will lead them towards their goals. This report is going to help us give a better understanding of the proposed university model.

                                                      PROPOSED SOLUTION

New Features implemented to improve the base university model:

Employment History: Displaying student history for every student will

Employment Feedback: This class will help us capture the feedback from the students. This feedback will be useful to calculate the employer rating to determine the best employer.

CourseRanking: This will help in ranking the courses to calculate the effectiveness of the courses based on student reviews.

Best employer: This will capture employer feedback from the student and then we can display the best employer based on all the ratings which will enable students to make more informed decisions.

Semester system: This will help the model look closer to how an actual university works. In the base university model.

Grading: Faculty assigns grades to student which will help in calculating the GPA of the students

Including Course Schedule: Each class will have a schedule which is unique to itself.

Applying for jobs and hiring: The employer will create jobs and students can apply to them. Once a student accepts a position, they cannot accept any other position.

__*Following is the structure of our proposed solution:*__

__ApplicationSystem Package__
The package defines threeclasses: ApplicationSystem, Department, and DepartmentDirectory. ApplicationSystem has instance variables for user account directory, department, department directory, and jobs directory. It also has getter and setter methods for each instance variable and a static getInstance() method that returns a new instance of the class. It creates a default user account with the username "admin", password "admin", and a SystemAdminRole role. Department represents a department in an educational institution and has instance variables such as departmentName, coursedirectory, useraccountdirectory, facultydirectory, termDirectory, and registeredClassDirectory. The constructor initializes all the directories and provides getter and setter methods for each instance variable. DepartmentDirectory represents a directory of departments in an educational institution and has an instance variable department, which is an ArrayList of Department objects. The constructor initializes the departments list to an empty list. It provides several methods such as createDepartment(), deleteDepartment(), getDepartmentbyName(), and checkUniqueDepartment() for managing the list of departments. createDepartment() creates a new Department object with the given name, adds it to the departments list, and returns the new department object. deleteDepartment() removes the specified Department object from the departments list. getDepartmentbyName() returns the Department object with the specified name from the departments list. checkUniqueDepartment() checks if a department with the given name already exists in the departments list and returns a boolean value accordingly.

__Course Package__
This package consists of four classes: Course, CourseDirectory, Term, and TermDirectory.
The Course class has instance variables for course number, name, price, credits, faculty, and registered class directory. It has methods for getting and setting these variables, as well as a constructor that takes a Faculty object as a parameter and initializes the registered class directory.
The CourseDirectory class has an ArrayList of Course objects and methods for getting and setting this list, as well as a method for creating a new Course object and adding it to the list. It also has a method for getting a Course object by its name.
The Term class has instance variables for term name and a CourseDirectory object. It has methods for getting and setting these variables, as well as a toString method to return the term name.
The TermDirectory class has an ArrayList of Term objects and methods for getting and setting this list, as well as a method for creating a new Term object and adding it to the list. It also has methods for checking if a term exists and getting a Term object by its name.

__Department Admin Package__
This package includes two classes, DepartmentAdmin and DepartmentAdminDirectory. DepartmentAdmin is a subclass of the Person class and includes instance variables and methods to get and set those variables. DepartmentAdminDirectory includes an ArrayList of DepartmentAdmin objects and methods to get and set the list, as well as a method to create a new DepartmentAdmin object and add it to the list.

__Faculty Package__
This package defines a class Faculty that extends the Person class and has getter and setter methods for various attributes like id, name, phoneNumber, etc. It also overrides the toString() method to return the name of the faculty member.
The code also defines a class FacultyDirectory that has an ArrayList of Faculty objects and methods to get and set the list of faculty members, as well as a method to create a new faculty member and add it to the list.

__Jobs Package__
This package includes two classes: Jobs and JobsDirectory.
The Jobs class has four instance variables: jobId, jobPosition, jobDescription, and Salary. These variables are accessed using getter and setter methods. The class also has a constructor method that does not take any arguments.
The JobsDirectory class has an ArrayList instance variable named “jobs” that holds a collection of Jobs objects. It has a constructor method that initializes the ArrayList. The class also includes two methods: createJob and checkUniqueJobId.
The createJob method takes four parameters: jobId, jobPosition, jobDescription, and salary. It creates a new Jobs object, sets its instance variables using the provided arguments, adds it to the jobs ArrayList, and returns the newly created Jobs object.
The checkUniqueJobId method takes a jobId parameter and checks whether the jobId already exists in the jobs ArrayList. If the jobId already exists, the method returns false. If it does not exist, the method returns true.
Overall, these classes provide a way to create and manage Jobs objects and to check for unique job IDs.

__Registered package__
This package consists of two classes: RegisteredClass and RegisteredClassDirectory. The RegisteredClass class contains various attributes of a registered class, such as classNo, courseName, term, price, available, status, department, course, and faculty. It also includes getters and setters for these attributes.
The RegisteredClassDirectory class contains an ArrayList of RegisteredClass objects and methods to get and set this ArrayList, as well as a method to register a new class.

__Role package__
This package represents different roles in an application system, including System Admin, Faculty, Student, Employer, and Department Admin. Each role extends an abstract Role class, which has a static method to get all
roles and an abstract method to create a work area for the specific role. The work area is represented by a JFrame for each role. The Department Admin and Employer roles have their own unique JFrames, while the other roles share the same JFrame with different functionalities based on their respective roles.

__Student package__
This package consists of three classes: Person, Student, and StudentDirectory.
The Person class contains fields for id, name, phoneNumber, email, Address, date, and ssn, as well as getter and setter methods for each field.
The Student class extends the Person class and has the same fields and getter and setter methods. It also contains a default constructor that calls the constructor of the parent class.
The StudentDirectory class contains an ArrayList of Student objects, a default constructor that initializes the ArrayList, and a method createStudent() that creates a new Student object with the specified parameters and adds it to the ArrayList.

__User package__
The package consists of two classes: UserAccount and UserAccountDirectory.
The UserAccount class contains private fields such as accountId, username, password, role, experience, designation, and a static counter. It also has a RegisteredClassDirectory object as a field. The class has a constructor to initialize the fields, getter and setter methods for the fields, and methods to get and set the RegisteredClassDirectory object.
The UserAccountDirectory class contains an ArrayList of UserAccount objects. It has a constructor to initialize the ArrayList, getter and setter methods for the ArrayList, and methods to create a new UserAccount object, authenticate a user, and check if a username is unique.

__Employer package__
The package includes two classes related to Employers: Employers and EmployersDirectory. The Employers class has attributes such as name, jobRequestDirectory, and rating, and includes methods for getting and setting these attributes. The class also overrides the toString method.
The EmployersDirectory class has an ArrayList of Employers and includes methods for getting and setting this list, as well as a method for creating a new Employer and adding it to the list.

__Jobs package__
In this package, the Jobs directory maintains a list of available job positions, which include a job ID, position name, description, salary, and whether the position is currently available. It also provides methods to create, delete, and retrieve jobs, and to check if a job ID is unique.
The JobRequest directory maintains a list of job requests, which include a request ID, the job being requested, the student requesting the job, and the status of the request. It provides methods to create and retrieve job requests.
