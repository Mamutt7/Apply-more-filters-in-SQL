# Apply-more-filters-in-SQL

## Activity overview
As a security analyst, you’ll often need to query numbers and dates.

For example, you may need to filter patch dates to find machines that need an update. Or you might filter login attempts made during a certain period of time to investigate a security incident.

Common operators for working with numeric or date and time data will help you accurately filter data. These are some of the operators you'll use:

- `=` (equal)
- `>` (greater than)
- `<` (less than)
- `<>` (not equal to)
- `>=` (greater than or equal to)
- `<=` (less than or equal to)

## Scenario
In this scenario, you’re investigating a recent security incident.

You need to gather information about login attempts for certain dates and times. This will help in resolving a security incident.

Here’s how you’ll do this task: First, you’ll retrieve login events made after a certain date. Second, you’ll narrow the focus of the search to filter logins in a date range. Third, you’ll investigate logins that were made at certain times. Finally, you’ll filter login attempts based on their event IDs.

### Task 1. Retrieve login attempts after a certain date
In this task, you need to investigate a recent security incident. To do this, you need to gather information about login attempts made after a certain date.

1. Complete the SQL query to retrieve data for login attempts made after '2022-05-09'. Replace X with the correct operator:

```
SELECT * 
FROM log_in_attempts 
WHERE login_date X '2022-05-09';
```

![image](https://github.com/user-attachments/assets/72714ddd-4f56-4cbb-8959-99906404a04e)

Now, based on your first query, you find a need to expand the date range to include 2022-05-09 in your search.

2. Complete the SQL query to retrieve data for login attempts that were made on or after '2022-05-09'. Replace X with the correct operator:

```
SELECT * 
FROM log_in_attempts 
WHERE login_date X '2022-05-09';
```
![image](https://github.com/user-attachments/assets/bd4d27ee-dfc2-429c-8077-8833273bce07)


### Task 2. Retrieve logins in a date range

In this task, you need to narrow the focus of the search. Login attempts made after 2022-05-11 shouldn't be included. Use the BETWEEN and AND operators to return results between '2022-05-09' and '2022-05-11'.

- Run the query to retrieve the required records. You must insert the required dates X and Y:

```
SELECT * 
FROM log_in_attempts 
WHERE login_date BETWEEN 'X' AND 'Y';
```
![image](https://github.com/user-attachments/assets/b127d4cd-61c1-4ce7-9d06-b22a303fa1e3)


### Task 3. Investigate logins at certain times

In this task, you need to investigate logins that were made at certain times. To do this, filter the data in the log_in_attempts table by login time (login_time).

First, your organization's typical work hours begin at 07:00:00. Retrieve all login attempts made before 07:00:00 to learn more about the users who are logging in outside of typical hours.

1. Write a SQL query to retrieve data for login attempts made before '07:00:00'.
![image](https://github.com/user-attachments/assets/a35ada37-6701-415c-9833-faa2af2ab672)


2. Modify the query to return logins between '06:00:00' and '07:00:00'.
![image](https://github.com/user-attachments/assets/105ce987-7f1f-414e-90c5-7723fdda4e4e)


### Task 4. Investigate logins by event ID

In this task, you need to investigate login attempts based on event ID numbers. With this query, you want to return only the event_id, username, and login_date fields from the log_in_attempts table.

1. Write a query to return login attempts with event_id greater than or equal to 100.
![image](https://github.com/user-attachments/assets/6ad9dcc7-9d2f-4641-a9a4-ee639fa905c3)


The query in the previous step returned more data than required.

2. Modify the query to return only login attempts with event_id between 100 and 150.
![image](https://github.com/user-attachments/assets/bef49712-49df-40a7-8071-0f47b3c9a447)


### Conclusion

You have completed this activity and practiced applying

- the `WHERE` keyword
- the `BETWEEN` and `AND` operators, and
- operators for working with numeric or date and time data types (for example, =, >, >=)

to filter data from a table.
