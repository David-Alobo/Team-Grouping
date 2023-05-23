# Team-Grouping
This project provides a solution to an SQL Challenge from an interview test question for a Data Engineer on Hacker Rank

### Employee details
There is a table of employee location information called emp_details. Each record contains a person’s name and the city where they live.

Write a query to return a list of items,

### Teams are formed within these rules:

- Team members must live in the city they represent.

- For each city, create teams of 3 until there are fewer than 3 who are unassigned.

- When there are fewer than 3 people unassigned in a city, they form a team.(See New York in the sample data tables section.)

### Report requirements:

- There should be 3 columns: the city name, a comma-delimited list of upto 3 players, and the team’s name.

- The cities should be ordered alphabetically.

- Players are selected in the order they occur in the table.

- Their names should be in order alphabetically within the comma-delimited list.

- Team names are ‘Team’ plus a number. For example, the first row’s team is Team1, then Team2, and so on through Team20.

- Only show the first 20 rows.

### Schema

| Name | Type | Description |
|---|---|---|
| EMP_NAME | Varchar | Employee Name |
| CITY | Varchar | Name of the City |


### Sample Data Tables

### emp_details

|EMP_NAME|	CITY |
|---|---|
| Sam |	New York |
| David	| New York |
| Peter	| New York |
| Chris	| New York |
| John	| New York |
| Steve	| San Francisco |
| Rachel |	San Francisco |
| Robert	| Los Angeles |

### Output:

| CITY | EMP_NAME	| Team |
|---|---|---|
| Los Angeles	| Robert | Team1 |
| New York	| David, Peter, Sam	| Team2 |
| New York |	Chris, John	| Team3 |
| San Francisco	| Rachel, Steve	| Team4 |

Explanation:

It will group the employees based on cities and restrict the number of employees as per row to 3 at max, also team names are to be given for each row.

New York Is an example of a city with 2 teams. Grab the first 3 names, Sam, David, Peter for the first team, sort the names and report: David, Peter, Sam. Noe grab the last 2, Chris, John, sort them: Chris, John.
