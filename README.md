# Web_Engineering_Final_Project_Hospital_Management_System


CREATE DATABASE hms


CREATE TABLE admin (
  id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(255) NOT NULL,
  password VARCHAR(255) NOT NULL,
  updationDate VARCHAR(255)
);


CREATE TABLE doctors (
  id INT AUTO_INCREMENT PRIMARY KEY,
  specilization VARCHAR(255),
  doctorName VARCHAR(255),
  address TEXT,
  docFees VARCHAR(255),
  contactno BIGINT,
  docEmail VARCHAR(255),
  password VARCHAR(255),
  creationDate TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updationDate TIMESTAMP NULL ON UPDATE CURRENT_TIMESTAMP
);

CREATE TABLE doctorspecilization (
  id INT AUTO_INCREMENT PRIMARY KEY,
  specilization VARCHAR(255),
  creationDate TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updationDate TIMESTAMP NULL ON UPDATE CURRENT_TIMESTAMP
);


CREATE TABLE tblpatient (
  ID INT AUTO_INCREMENT PRIMARY KEY,
  Docid INT,
  PatientName VARCHAR(200),
  PatientContno BIGINT,
  PatientEmail VARCHAR(200),
  PatientGender VARCHAR(50),
  PatientAdd TEXT,
  PatientAge INT,
  PatientMedhis TEXT,
  CreationDate TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  UpdationDate TIMESTAMP NULL ON UPDATE CURRENT_TIMESTAMP
);


CREATE TABLE appointment (
  id INT AUTO_INCREMENT PRIMARY KEY,
  doctorSpecialization VARCHAR(255),
  doctorId INT,
  userId INT,
  consultancyFees INT,
  appointmentDate VARCHAR(255),
  appointmentTime VARCHAR(255),
  postingDate TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  userStatus INT,
  doctorStatus INT,
  updationDate TIMESTAMP NULL ON UPDATE CURRENT_TIMESTAMP
);


CREATE TABLE tblmedicalhistory (
  ID INT AUTO_INCREMENT PRIMARY KEY,
  PatientID INT,
  BloodPressure VARCHAR(200),
  BloodSugar VARCHAR(200),
  Weight VARCHAR(100),
  Temperature VARCHAR(200),
  MedicalPres TEXT,
  CreationDate TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);


CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  fullName VARCHAR(255),
  address TEXT,
  city VARCHAR(255),
  gender VARCHAR(255),
  email VARCHAR(255),
  password VARCHAR(255),
  regDate TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updationDate TIMESTAMP NULL ON UPDATE CURRENT_TIMESTAMP
);

CREATE TABLE tblcontactus (
  id INT AUTO_INCREMENT PRIMARY KEY,
  fullname VARCHAR(255),
  email VARCHAR(255),
  contactno BIGINT,
  message TEXT,
  PostingDate TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  AdminRemark TEXT,
  LastupdationDate TIMESTAMP NULL ON UPDATE CURRENT_TIMESTAMP,
  IsRead INT
);
