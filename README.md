# AutoGradeMailerSystem

## 📖 Descripción

**AutoGradeMailer System** es un cuaderno interactivo en Python diseñado para automatizar la labor docente de calificación y notificación de resultados académicos. Permite a un profesor enviar reportes personalizados a cada estudiante, generando documentos Word con sus notas individuales y distribuyéndolos por correo electrónico de manera masiva pero personalizada.

### 📚 Caso de uso:

Un profesor de **Matemáticas, Física y Química** dicta clases a un grupo de **10 estudiantes**. Al finalizar el periodo académico, desea informar a cada estudiante sus calificaciones en las tres asignaturas, adjuntando un reporte en formato Word con los resultados y enviando un correo individualizado.

Para lograr esto, el profesor cuenta con:

- 📄 Un archivo Excel (`StudentGrades.xlsx`) que contiene los nombres, correos electrónicos, teléfonos y las calificaciones de Matemáticas, Física y Química de cada estudiante.
- 📑 Una plantilla Word (`template.docx`) con un formato preestablecido para el reporte, en el que se sustituyen dinámicamente los datos de cada estudiante: nombre, calificaciones, fecha y datos del profesor.

El sistema automatiza la carga de datos, generación de reportes y envío de correos, reduciendo tiempos y asegurando una comunicación profesional y ordenada.

---

## 📌 Explicación

El flujo de trabajo de **AutoGradeMailer.ipynb** es el siguiente:

1. **Carga de datos:**
   - Se utiliza `pandas` para leer el archivo `StudentGrades.xlsx`, que contiene una tabla con la información de los estudiantes y sus notas.

2. **Generación de reportes personalizados:**
   - Se usa `docxtpl` para cargar la plantilla `template.docx`.
   - Para cada estudiante, se reemplazan las variables del documento (`{{student_name}}`, `{{math_grade}}`, etc.) con los valores correspondientes de su registro.
   - Se genera un archivo Word único para cada estudiante con su reporte de calificaciones.

3. **Creación de mensajes de correo:**
   - Se construye un correo personalizado para cada estudiante usando el módulo `email`, incluyendo su nombre y un mensaje motivador.
   - Se adjunta el reporte Word generado.

4. **Envío de correos:**
   - A través de `smtplib`, el sistema se conecta a un servidor SMTP autenticado.
   - Se envía un correo a cada estudiante con su reporte adjunto de forma individual.

5. **Registro de actividad (opcional):**
   - El sistema puede llevar un log de los correos enviados correctamente o de los fallidos en caso de errores.

---

## 📦 Dependencias

Para ejecutar este proyecto, asegúrate de tener instaladas las siguientes dependencias:

```bash
pip install pandas docxtpl openpyxl
