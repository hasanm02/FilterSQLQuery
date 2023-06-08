# FilterSQLQuery 

<h2>Project Description</h2>
My organization is attempting to increase the security of their system. My responsibility is to ensure the security of the system, look into any potential security concerns, and upgrade employee computers as necessary. Examples of how I carried out security-related tasks using SQL and filters are shown in the steps that follow.
<br />



<h2>Retrieve after hours failed login attempts</h2>

<p align="center">
After business hours (after 18:00), there was a possible security incident. All failed after-hours login attempts must be looked into.

The SQL query I made to look for failed login attempts that happened outside business hours is shown in the following code.
<br/>
  
  
<img src="https://i.imgur.com/TS1Fd8T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
This query restricts its results to failed login attempts that took place after 18:00. I began by choosing all of the information from the log_in_attempts table. Then, I filtered my data using a WHERE clause and an AND operator to output only failed login attempts that took place after 18:00. Login attempts made after 18:00 are filtered out by the first criteria, login_time > '18:00'. Success = FALSE, the second criteria, screens out unsuccessful login attempts.  <br/>
  
  
  <h2>Retrieve login attempts on specific dates</h2>

<p align="center">
On 2022-05-09, a suspicious occurrence took place. It is necessary to look into any login activity that took place on 2022-05-09 or the day prior.

The code that follows shows how I built a SQL query to search for login attempts that took place on particular dates.
<br/>
  
  
<img src="https://i.imgur.com/ClEoUyb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
This query finds all attempts to log in that took place on either 2022-05-09 or 2022-05-08. I began by choosing all of the information from the log_in_attempts table. Then, I filtered my findings using a WHERE clause and an OR operator to only show login attempts that happened on either 2022-05-09 or 2022-05-08. Logins made on or after 2022-05-09 are excluded by the first condition, login_date = '2022-05-09'. With the second condition, which reads "login_date = '2022-05-08'," only logins made on May 8, 2022 are considered. <br/>
 
  
 <h2>Retrieve login attempts outside of Mexico</h2>

<p align="center">
It appears there is a problem with the login attempts that took place outside of Mexico after looking into the company's data on login attempts. These login attempts need to be looked into.

The code that follows shows how I built a SQL query to look for login attempts outside of Mexico. 
<br/>
  
  
<img src="https://i.imgur.com/OYet0N0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
 This query retrieves all attempts at login made outside of Mexico. I began by choosing all of the information from the log_in_attempts table. I then applied a WHERE clause with a NOT to exclude all nations besides Mexico. Because the dataset refers to Mexico as MEX and MEXICO, I used LIKE with MEX% as the pattern to match. When combined with LIKE, the percentage symbol (%) stands in for any amount of arbitrary characters.  <br/>
  
  
   <h2>Retrieve employees in Marketing</h2>

<p align="center">

A few Marketing department employees' PCs need to be updated, according to my team. I need to find out which employee machines need updating in order to achieve this.

The code that follows shows how I built a SQL query to search for employee computers from staff members in the East building's Marketing department.
<br/>
  
<img src="https://i.imgur.com/5cTWjin.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
 This query produces a list of every worker in the East building's Marketing division. I began by choosing all of the information from the employees table. Then, to find workers who are employed by the Marketing division and the East building, I utilized a WHERE clause with an AND. Because the information in the office column refers to the East building with the given office number, I used LIKE with East% as the pattern to match. The first filter for personnel in the Marketing department is the component of the condition that reads "department = 'Marketing'". The office LIKE 'East%' component of the second condition filters for workers in the East building. <br/>
  
   <h2>Retrieve employees in Finance or Sales</h2>

<p align="center">

Additionally, the equipment used by staff members in the sales and finance divisions needs to be upgraded. I can only receive personnel data from these two departments because I need a different security update.

The code that follows shows how I built a SQL query to look for employee machines from workers in the sales or finance divisions.
<br/>
  
<img src="https://i.imgur.com/ehvb3Fn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
All personnel in the sales and finance departments are returned by this query. I began by choosing all of the information from the employees table. I then used an OR and a WHERE clause to select for workers in the finance and sales divisions. Because I wanted every employee in either department, I utilized the OR operator rather than the AND operator. Employees from the Finance department are filtered according to the first condition, department = "Finance". Department = 'Sales' in the second criteria excludes personnel from the Sales department. <br/>
  
  
   <h2>Retrieve all employees not in IT</h2>

<p align="center">

My group still needs to change the security settings for those who work outside the information technology division. I must first gather information on these employees before I can make the upgrade.

The example below shows how I built a SQL query to look for employee computers from people who weren't in the IT department.
<br/>
  
<img src="https://i.imgur.com/W1V44DQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
All employees who are not in the information technology department are returned by the query. I began by choosing all of the information from the employees table. Then, to filter out workers who weren't in this department, I used a WHERE clause with NOT. <br/>
  
 
<h2>Summary</h2>
To obtain detailed information on login attempts and employee workstations, I used filters to SQL queries. Employees and log_in_attempts are the two tables I used. I filtered for the precise data required for each task using the AND, OR, and NOT operators. In order to search for trends, I also used LIKE and the wildcard percentage sign (%).
<br />
  
