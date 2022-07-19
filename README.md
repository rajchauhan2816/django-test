# perfometer
Student Performance System

// Tables

Table users {
  id int [pk, increment] // auto-increment
  username varchar
  email varchar
  phone varchar
  created_at datetime
  updated_at datetime
  
}

Table students {
  id int [pk, increment] // auto-increment
  user int [ref: > users.id]
  name varchar
  dob varchar
  gender varchar
  enrollment_no varchar
  created_at datetime
  updated_at datetime
}

Table subjects {
  id int [pk, increment] // auto-increment
  name varchar
  code varchar
  description varchar
  created_at datetime
  updated_at datetime
}

Table student_subjects{
  id int [pk, increment]
  year varchar
  student_id int [ref: > students.id]
  subject_id int [ref: > subjects.id]
  max_marks float
  marks float
}


