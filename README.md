# TASK DETAILS

1. Write API to create Mentor
2. Write API to create Student
3. Write API to Assign a student to Mentor
      1. Select one mentor and Add multiple Student
      2. A student who has a mentor should not be shown in List
4. Write API to Assign or Change Mentor for particular Student
      1. Select One Student and Assign one Mentor
5. Write API to show all students for a particular mentor
6. Write an API to show the previously assigned mentor for a particular student.


Render URL --> https://assign-mentor-backend-pws4.onrender.com

# END POINTS EXPLAINED 

END POINTS - 

1. GET METNOD :
      i) FOR STUDENTS DATA :
           1. student/show --> To get all students data. It will show total student count and studentName and there currentMentorName and previous mentorNames in array.
           2. student/show/:studentID --> To get specific student data. It shows the studentName and there currentMentorName and previousMentorsName in array.
      ii) FOR MENTORS DATA :
           1. mentor/show --> To get all mentors data. It will show the total mentors count and mentorName and there assignedStudentsName in array.
           2. mentor/show/:mentorID --> To get the specific mentor data. It shows the mentorName and there assignedStudentsName in array.

2. POST METHOD :
     i) FOR STUDENT DATA :
           1. student/add --> To add initial student data. It requires only studentName to create. REQUIREMENTS (studentName should be unique).
     ii) FOR MENTOR DATA :
           1. mentor/add --> To add initial mentor data. It requires only mentorName to create. REQUIREMENTS (mentorName should be unique).

3. PUT METHOD / UPDATE :
     i) FOR STUDENT DATA :
           1. student/update/:studentID --> To assign currentMentor to the newly created student data / update the currentMentor of specific student data and the currentMentor name will be pushed into the previousMentors Array if only when the currentMentor is not already in the array.
REQUIREMENTS ("studentName":"","currentMentor":"mentorID")

    ii) FOR MENTOR DATA :
           1. mentor/update/:mentorID --> To assign multiple students for the specific mentor. REQUIREMENTS ("mentorName":"","assignedStudents":["studentID_1","studentID_2"])

