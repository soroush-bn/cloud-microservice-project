# App description

describe wtf this app does.
provide link of the monilith repo


 

# Monolith to micro-service 

### list of micro services which are going to be implemented

1- user management (jwt)
2-
3-
4-

### reasons why each micro service is chosen 

### write the files which are going to be used by each micro service

### diagram of entities and their relations and dependencies to other services as the data bases are apart

### diagram of services and all the internal and external calls

### specify all internal calls like this :

    attendance-service --> course-service:
	    where: monolith/courses/models.py, class: Course
	    happened: monolith/attendance/views.py, class: AttendanceView
	    code: Courses.objects.get(id=course_id)
	    reason: imported and used
	    solution: GRPC 

    course-service --> user-management-service:
        where: monolith/users/models.py, class: User
        happened: monolith/courses/views.py, class: CourseView
        code: Users.objects.get(id=student_id)
        reason: must obtain user from database
        solution: trust user_id from jwt token
	
### list of frameworks used

### data base schema and each entity info




 

### team plan for developing each service
write wtf each one of us should do
