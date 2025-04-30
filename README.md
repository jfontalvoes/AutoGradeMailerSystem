# 📄 AutoGradeMailer System

Automated generation of personalized academic report documents for students.

---

## 📖 Description

**AutoGradeMailer System** is an interactive Python notebook designed to automate the academic task of preparing and notifying students of their grades. It allows a teacher to generate personalized Word reports for each student, detailing their individual grades in various subjects, ready to be manually sent via email or other communication channels.

### 📚 Use Case:

A teacher of **Mathematics, Physics, and Chemistry** teaches a group of **10 students**. At the end of the academic term, the teacher wants to share each student's grades in these three subjects by generating a personalized Word document report for each one.

To do this, the teacher uses:

- 📄 An Excel file (`StudentGrades.xlsx`) containing students' names, email addresses, phone numbers, and grades for Mathematics, Physics, and Chemistry.
- 📑 A Word template (`template.docx`) with a predefined format for the report, containing placeholders for the student's name, grades, date, and teacher’s details.

This system automates the data loading and document generation process, saving time and ensuring professional, organized communication ready for later distribution.

---

## 📌 How It Works

The workflow of **AutoGradeMailer.ipynb** is as follows:

1. **Load student data:**
   - Uses `pandas` to read the `StudentGrades.xlsx` file containing student records and their grades.

2. **Generate personalized reports:**
   - Uses `docxtpl` to load the `template.docx` Word template.
   - For each student, replaces the placeholders in the document (`{{student_name}}`, `{{math_grade}}`, etc.) with their corresponding data.
   - Generates a unique Word report document for each student.

3. **Save reports:**
   - The reports are saved in a designated folder, named after each student, ready to be manually emailed.

---

## 📂 Project Files
- AutoGradeMailer.ipynb → Jupyter notebook containing the full report generation workflow.

- StudentGrades.xlsx → Excel file listing students and their grades.

- template.docx → Word template used for generating personalized reports.

---

## 🚀 Usage
1. Clone this repository.

2. Install the required dependencies.

3. Optionally, customize the teacher's information or the Word template as needed.

4. Run the notebook cells step by step.

5. Check the output folder for the generated Word reports.

---

## 📌 Notes
- This notebook does not send emails. It only generates the personalized Word documents, which can later be sent manually or using a separate email-sending tool.

- You can customize the Word template content and destination folder names to suit your needs.

---

## 📜 License
This project is licensed under the MIT License. See the LICENSE file for details.

---

## ✨ Author
Developed by Jonathan Estiven Fontalvo Aparicio 📧

Feel free to copy this into your repo. If you’d like a `.gitignore` template (e.g., to ignore `*.ipynb_checkpoints/` and your generated reports), just let me know!

