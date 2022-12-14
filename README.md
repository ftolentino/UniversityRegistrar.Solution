# University Registrar

#### By _**Filmer Tolentino & Seung Lee**_   

#### _This website allows you to manage a University Registrar to add Enrollments, Departments, Courses, and Students to a SQL database using a many to many relationship._  

---


## Technologies Used

* _C#_
* _.NET_
* _HTML_
* _CSS_
* _SQL Workbench_
* _Entity Framework_
* _MVC_

---
## Description

_This is an MVC application that was built using C#._

---
## Setup and Installation Requirements
This Setup assumes you have GitBash and MySQL Workbench pre-installed. 
<br><small>If you do not have one or both installed, please begin with that setup below. 
<br>If you _do_ have both installed, move onto "initial setup".</small>

<details>
<summary><strong>GitBash and MySQL Workbench Setup</strong></summary>
<ol>
<li>https://git-scm.com/download/  
<li>Download Git and follow the setup wizard. 
<li>https://dev.mysql.com/downloads/workbench/     
<li>Download MySQL Workbench
<li>Follow the setup wizard & create a localhost server on port 3306.
<li>Keep track of your username and password, this will be used in the connection steps of <strong>"SQL Workbench Configuration"</strong>  
</details>
<details>
<summary><strong>Initial Setup</strong></summary>
<ol>
<li>Copy the git repository url: https://github.com/ftolentino/UniversityRegistrar.Solution.git
<li>Open a terminal and navigate to your Desktop with <strong>cd</strong> command
<li>Run,   
<strong>$ git clone https://github.com/ftolentino/UniversityRegistrar.Solution.git</strong>
<li>In the terminal, navigate into the root directory of the cloned project folder "UniversityRegistrar.Solution".
<li>Navigate to the projects root directory, "UniversityRegistrar".
<li>Move onto "SQL Workbench Configuration" instructions below to build the necessary database.
<br>
</details>

<details>
<summary><strong>SQL Workbench Configuration</strong></summary>
<ol>
<li>Create an appsetting.json file in the "UniversityRegistrar" directory  
   <pre>UniversityRegistrar.Solution
   └── UniversityRegistrar
    └── appsetting.json</pre>
<li> Insert the following code: <br>

<pre>{
  "ConnectionStrings": {
      "DefaultConnection": "Server=localhost;Port=3306;database=university_registrar;uid=root;pwd=epicodus;"
  }
}</pre>
<small>*Note: you must include your password in the code block section labeled "YOUR-PASSWORD-HERE".</small><br>
<small>**Note: you must include your username in the code block section labeled "YOUR-USERNAME-HERE".</small><br>
<small>***Note: if you plan to push this cloned project to a public-facing repository, remember to add the appsettings.json file to your .gitignore before doing so.</small>

<li>In root directory of project folder "UniversityRegistrar", run  
<strong>$ dotnet ef migrations add restoreDatabase</strong>
<li>Then run <strong>$ dotnet ef database update</strong>

<ol> 
  <li>Open SQL Workbench.
  <li>Navigate to "university_registrar" schema.
  <li>Click the drop down, select "Tables" drop down.
  <li>Verify the tables, you should see <strong>course</strong>, <strong>department</strong>, <strong>student</strong>,& <strong>enrollment</strong>.
  
</details>

<details>
<summary><strong>To Run</strong></summary>
Navigate to:  
   <pre>UniversityRegistrar.Solution
   └── <strong>UniversityRegistrar</strong></pre>

Run ```$ dotnet restore``` in the terminal.<br>
Run ```$ dotnet run``` in the terminal.
</details>
<br>

This program was built using *`Microsoft .NET SDK 5.0.401`*, and may not be compatible with other versions. Cross-version performance is neither implied nor guaranteed, your actual mileage may vary.

---
## Known Bugs

* _WIP Styling_

## License

_None_

Copyright (c) 8/5/2022 Filmer Tolentino & Seung Lee
