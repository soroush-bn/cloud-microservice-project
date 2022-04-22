# App description

blog application which provides api to sign up and login for users.
users can create articles, add comments to articles. 

# Monolith to micro-service 

### list of micro services which are going to be implemented

1- user management (jwt)
2- article
3- user
4- comment

### reasons why each micro service is chosen 

article: as articles are more likely to be developed in future -> scalibility requirement
comment: as there might be a lot of comment being posted by users and there we be a lot of load on this service
user: for security requirements 

### write the files which are going to be used by each micro service

article: ArticleHandler.kt, ArticleRepository.kt, Article.kt, TagHandler.kt, TagRepository.kt
comment: CommentRepository.kt, Comment.kt
user: UserHandler.kt, ProfileHandler.kt, UserRepository.kt, User.kt


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


![photo1650650248](https://user-images.githubusercontent.com/45733433/164769225-b8bf0f4a-440b-41fd-8242-05dc672b82f2.jpeg)


 

### team plan for developing each service
write wtf each one of us should do
