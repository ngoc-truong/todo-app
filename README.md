# To-Do-App

This project is a to-do app with advanced assistant functionalities. 

(Planned) main functionalities: 

- The app should be a personal assistant. That means that a user can create a new task and dump it into a large list of tasks. The user specifies a task's urgency, difficulty and duration and the app will create a day plan for the user. Furthermore, the user specifies at which time of the day he has got the most energy. In this phases the assistant will schedule difficult and time-consuming tasks. In times in which the user is not concentrated, the assistant will schedule easy-to-solve tasks and tasks which only require a short amount of time (e.g. making a doctor's appointment).

- The app shows a user how much time (in days) is left in order to solve a task. It also considers regular schedules (like hobbies or weekends) so that the estimated time is more realistic.

- User authentification

- Social function? In order that friends can help and support a user, a social function will be implemented. The friend can actually see the to-dos of the other person and comment on a task (e.g. giving advice or tipps how to solve it)

## Data scheme

### Users
* name:string
* email:string
* concentrated: datetime (array?)
* unconcentrated: datetime (array?)
* has_many :posts

### Task
* description:text
* expiration:datetime
* difficulty:string
* duration:integer
* belongs_to :user

### Comments
* description:text
* belongs_to :user
* belongs_to :task