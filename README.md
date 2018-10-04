# DSC-Workshop-D3-Todo
Assignment for DSC workshop day 3

## Assignment

Using NodeJS and the express framework, build a minimal record system. This system should hold the first and last names of random students, along with their ages.

Create an object with 10 students inside. The keys should be the matric numbers of the students (000 - 999), while the values should be objects containing the information about the students as shown in the code below. The table below contains a few students' info your record should hold. Come up with 7 more.

S/N | Matric number | First name | Last name | Age
--------------------------------------------------
1   | 001           | Sola       | Adesokan  | 17
--------------------------------------------------
2   | 002           | Femi       | Omolaja   | 17
--------------------------------------------------
3   | 003           | Obinna     | Ejiofor   | 19
--------------------------------------------------

```javascript
var records = {
	"001": {
		firstName: "Sola",
		lastName: "Adesokan",
		age: 17
	},

	"002": {
		firstName: "Femi",
		lastName: "Omolaja",
		age: 19
	}
	// fill in the rest
};
```

The API implemented should be capable of doing the following:


**Creating a student's info**

Sample endpoint: _/students/create/001/David/Sanda/12_

Expected result: A new student with name David Sanda, and age 12, has been created.

If the matric number already belongs to a student, user should receive the message, "Matric number already exists".


**Retrieving a student's info**

Sample endpoint: _/students/001_

Expected result: Sola Adesokan - 17 years


Sample endpoint: _/students/001/firstName_

Expected result: Sola


Sample endpoint: _/students/001/lastName_

Expected result: Adesokan


Sample endpoint: _/students/001/age_

Expected result: 17


**Editing a student's info**

Sample endpoint: _/students/edit/001/firstName/Jude_

Expected result: Sola Adesokan has been changed to Jude Adesokan

The endpoint above should change Sola's first name to Jude

Sample endpoint: _/students/edit/001/lastName/King_

Expected result: Sola Adesokan has been changed to Sola King

The endpoint above should change Sola's last name to King

Sample endpoint: _/students/edit/001/age/16_

Expected result: Sola's age has been changed to 16

The endpoint above should change Sola's age to 16


**Deleting a student's info**

Sample endpoint: _/students/delete/001_

Expected result: The student with matric number 001 has been removed.
