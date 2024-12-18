

# The User Management System Final Project: Your Epic Coding Adventure Awaits! 🎉✨🔥

### Docker image on docker hub: https://hub.docker.com/repository/docker/jincheng411/event-manager/general](https://hub.docker.com/repository/docker/jincheng411/user_managment/general

### Issue 1: Docker compose start fail
Docker failed when running: docker compose up --build, fixed that by update dockerfile that allow downgrade

[See the issue](https://github.com/jincheng411/user_management/issues/11)


### Issue 2: Password is not meeting the standard
When register user, password is not meeting the standard, must be at least 8 characters and include at least one upper and lower case letters. fix that by adding password validator in user schema

[See the issue](https://github.com/jincheng411/user_management/issues/9)

### Issue 3: Not able to update user's is_professional
Not able to update is_professional field because of missing field in the user schema, add that field into user_update and user_response, solved the problem.

[See the issue](https://github.com/jincheng411/user_management/issues/7)

### Issue 4: Admin user role changed to authenticated after email verified  
After registering the first user which is an admin role, the user receives a verification email, after verifying, the user's role changes from admin to authenticated. 
need to change to email verification logic, check if the user is admin or not, only none admin user change the role to authenticated

[See the issue](https://github.com/jincheng411/user_management/issues/5)

### Issue 5: Admin should not receive a verification email
As first user admin created in the database, it should not receive verification email, add condition that send verification emails only when the users are not admin

[See the issue](https://github.com/jincheng411/user_management/issues/3)

### Issue 6: Not able to verify new user after register
After registered user and received the verification email, click "verifify email" link, it had error to verify the email with the link.Not able to verify user email is because the link doesn't have user_id, this is because it send the verification email before the user saved to database while creating the user.
To fix it we have to send the email after the user been created in the database.

[See the issue](https://github.com/jincheng411/event_manager/issues/12)

## Future implemented: User Search and Filtering
### Test cases for user Search and filtering: 
https://github.com/jincheng411/user_management/blob/main/tests/test_services/test_user_service.py

test list users search by nickname
test list users search by email
test list users filter by role
test list users filter by status
test list users filter by created date range
test list users sort by created at desc
test list users sort by created at asc
test list users invalid date_format
test list users no matching results
test list users search and role filter

### Reflection about this IS601
Throughout this comprehensive course on programming with Python and web development, I have experienced significant growth in both technical and professional competencies. This reflection outlines the key takeaways and the profound impact the course has had on my learning journey.
A cornerstone of the course was learning Python programming, which provided a versatile foundation for tackling data-driven projects. From manipulating CSV files to querying SQL databases and interacting with REST-based web services, the hands-on exercises allowed me to explore the practical applications of Python. Learning the FastAPI framework was particularly transformative, as it demonstrated the power of building high-performance web applications with minimal effort. The experience reinforced the importance of understanding the intricacies of server-side programming and laid the groundwork for future endeavors in API development.
Git, as a version control tool, became an indispensable part of the development workflow. By using Git effectively, I was able to manage changes to code, collaborate seamlessly, and ensure a robust history of my work. This practice not only enhanced my technical abilities but also underscored the value of adhering to industry standards in software development. Additionally, the emphasis on code readability and adherence to coding standards reinforced the importance of producing maintainable and scalable software solutions.
The course’s focus on object-oriented programming (OOP) principles deepened my understanding of structuring code in a modular and reusable manner. By applying OOP concepts, I developed the skills necessary to design systems that are both efficient and adaptable. Coupled with Agile development principles, I gained experience in iterative development processes, allowing me to deliver incremental improvements and respond effectively to changing requirements.
The introduction to SQL and Object-Relational Mapping (ORM) patterns proved invaluable for working with relational databases. I learned how to design and query databases efficiently, bridging the gap between data storage and application logic. These skills are crucial for developing robust systems that can handle complex data operations.
One of the most impactful lessons from the course was developing confidence in technical problem-solving. By learning to isolate issues, interpret error messages, and leverage online resources like Google effectively, I honed my ability to tackle coding challenges independently. This structured approach to debugging not only improved my efficiency but also instilled a mindset of resilience and adaptability.
This course provided a well-rounded education in python programming and web development, emphasizing both technical expertise and professional acumen. The integration of tools like VS code, pytest, and REST web services further enriched the learning experience. Most importantly, the course fostered a problem-solving mindset that will serve as a cornerstone of my future endeavors. I am confident that the knowledge and skills acquired through this course have prepared me to excel in the competitive fields of data programming and web development.




