# To-Do App (Python + Tkinter + MySQL)

**Deutsch** | [English below](#english)

---

Eine einfache, aber professionelle To-Do App mit Python.  
Die Aufgaben werden in einer MySQL-Datenbank gespeichert und können über eine grafische Oberfläche (GUI) verwaltet werden.

🚀 **Features**

- ✅ Aufgaben hinzufügen, erledigen und löschen
- 🎨 Moderne Benutzeroberfläche mit Tkinter
- 📂 Speicherung in MySQL (keine JSON-Datei mehr)
- 🔍 Filter: Alle, Offen, Erledigt
- 📊 Statistik: Anzahl erledigter Aufgaben
- 🖱️ Doppelklick auf Aufgabe → Erledigt markieren

🛠️ **Technologien**

- Python 3.13+
- Tkinter (GUI)
- MySQL / phpMyAdmin
- mysql-connector-python (für die Verbindung zur DB)

**Installation**

Repository klonen:
```sh
git clone https://github.com/GraceAkaemeh/todo-app-python.git
cd todo-app-python
```

Abhängigkeiten installieren:
```sh
pip install mysql-connector-python
```

MySQL-Datenbank einrichten:
```sql
CREATE DATABASE ToDoList;
USE ToDoList;

CREATE TABLE tasks (
    id INT AUTO_INCREMENT PRIMARY KEY,
    description VARCHAR(255) NOT NULL,
    completed BOOLEAN NOT NULL DEFAULT 0
);
```


**Datenbankkonfiguration**

Zugangsdaten in `task_db.py` anpassen:
```python
conn = mysql.connector.connect(
    host="localhost",
    user="DEINBENUTZER",
    password="DEINPASSWORT",
    database="ToDoList"
)
```

**Die Anwendung ausführen**
```sh
python task_gui.py
```
Die App öffnet sich automatisch in einem GUI-Fenster.


**Projektstruktur**

UI-Ebene (Tkinter-GUI)
Datenbankebene (MySQL-Verbindung)
Logikebene (Aufgabenbearbeitung)


**📚 Was ich gelernt habe**
Python-GUI-Entwicklung mit Tkinter
Datenbankintegration mit MySQL
CRUD-Operationen (Create, Read, Update, Delete)
Strukturierung kleiner Softwareprojekte
Verbindung von Frontend- und Backend-Logik


**📌 Anmerkungen**
Dies ist ein Lernprojekt
Passwörter und Anmeldedaten sollten in realen Anwendungen gesichert werden
Für Bildungszwecke konzipiert

---

## English

A simple but professional To-Do app with Python.  
Tasks are stored in a MySQL database and managed via a graphical user interface (GUI).

🚀 **Features**

-  Add, complete, and delete tasks
-  Modern interface with Tkinter
-  Storage in MySQL (no more JSON file)
-  Filter: All, Open, Completed
-  Statistics: Number of completed tasks
-  Double-click task → Mark as completed

🛠️ **Technologies**

- Python 3.13+
- Tkinter (GUI)
- MySQL / phpMyAdmin
- mysql-connector-python (for DB connection)

**Installation**

Clone the repository:
```sh
git clone https://github.com/GraceAkaemeh/todo-app-python.git
cd todo-app-python
```

Install dependencies:
```sh
pip install mysql-connector-python
```

**Database Setup**
```sql
CREATE DATABASE ToDoList;
USE ToDoList;

CREATE TABLE tasks (
    id INT AUTO_INCREMENT PRIMARY KEY,
    description VARCHAR(255) NOT NULL,
    completed BOOLEAN NOT NULL DEFAULT 0
);
```

**Database Configuration**
Update your credentials in task_db.py:
```python
conn = mysql.connector.connect(
    host="localhost",
    user="YOURUSER",
    password="YOURPASSWORD",
    database="ToDoList"
)
```

**Run the Application**
```sh
python task_gui.py
```
The app will open automatically in a GUI window.

**Project Structure**

UI Layer (Tkinter GUI)
Database Layer (MySQL connection)
Logic Layer (task handling)


**📚 What I Learned**
Python GUI development with Tkinter
Database integration using MySQL
CRUD operations (Create, Read, Update, Delete)
Structuring small software projects
Connecting frontend and backend logic


**📌 Notes**
This is a learning project
Passwords and credentials should be secured in real applications
Designed for educational purposes