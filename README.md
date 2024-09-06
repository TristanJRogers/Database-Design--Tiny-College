# Database_Design--Tiny_College
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
In this exercise I created a full crow’s foot notation ERD, using MS Visio to support the following business operations:

1.	Tiny College (TC) is divided into several schools: business, arts and sciences, education, and applied sciences. Each school is administered by a dean who is a professor. Each professor can be the dean of only one school, and a professor is not required to be the dean of any school.
2.	Each school comprises several departments. For example, the school of business has an accounting department, a management/marketing department, an economics/finance department, and a computer information systems department.
3.	Each department may offer courses. For example, the management/marketing department offers courses such as Introduction to Management, Principles of Marketing, and Production Management.
4.	a CLASS is a section of a COURSE. That is, a department may offer several sections (classes) of the same database course. Each of those classes is taught by a professor at a given time in a given place.  Additionally, each class is offered during a given semester. SEMESTER defines the year and the term that the class will be offered. Note that this is different from the date when the student actually enrolls in a class. For example, students are able to enroll in summer and fall term classes near the end of the spring term. It is possible that the Tiny College calendar is set with semester beginning and ending dates prior to the creation of the semester class schedule so CLASS is optional to SEMESTER. This design will also help for reporting purposes, for example, you could answer questions such as: what classes were offered X semester? Or, what classes did student Y take on semester X? Because a course may exist in Tiny College’s course catalog even when it is not offered as a class in a given semester, CLASS is optional to COURSE. 
5.	Each department should have one or more professors assigned to it. One and only one of those professors chairs the department, and no professor is required to accept the chair position. Therefore, DEPARTMENT is optional to PROFESSOR in the “chairs” relationship.
6.	Each professor may teach up to four classes; each class is a section of a course. A professor may also be on a research contract and teach no classes at all. 
7.	A student may enroll in several classes but take each class only once during any given enrollment period. For example, during the current enrollment period, a student may decide to take five classes—Statistics, Accounting, English, Database, and History—but that student would not be enrolled in the same Statistics class five times during the enrollment period! Each student may enroll in up to six classes, and each class may have up to 35 students, thus creating an M:N relationship between STUDENT and CLASS. 
8.	Each department has several (or many) students whose major is offered by that department. However, each student has only a single major and is therefore associated with a single department.  However, in the Tiny College environment, it is possible—at least for a while—for a student not to declare a major field of study. Such a student would not be associated with a department; therefore, DEPARTMENT is optional to STUDENT. It is worth repeating that the relationships between entities and the entities themselves reflect the organization’s operating environment. That is, the business rules define the ERD components.
9.	Each student has an advisor in his or her department; each advisor counsels several students. An advisor is also a professor, but not all professors advise students
10.	the CLASS entity contains a ROOM_CODE attribute. Given the naming conventions, it is clear that ROOM_CODE is an FK to another entity. Clearly, because a class is taught in a room, it is reasonable to assume that the ROOM_CODE in CLASS is the FK to an entity named ROOM. In turn, each room is located in a building. So, the last Tiny College ERD is created by observing that a BUILDING can contain many ROOMs, but each ROOM is found in a single BUILDING. In this ERD segment, it is clear that some buildings do not contain (class) rooms. For example, a storage building might not contain any named rooms at all.

## ERD Chart

![image](https://github.com/user-attachments/assets/eda709ff-1946-4368-b032-23d1bd67e9ad)

![image](https://github.com/user-attachments/assets/84faaf24-952c-48c5-a1ef-a192c6618c7f)

![image](https://github.com/user-attachments/assets/5d88278b-6605-410d-bfdf-3bc540f5a0d4)


