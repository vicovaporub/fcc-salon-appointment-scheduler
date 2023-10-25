# Salon Appointment Scheduler

## This project uses a combination of Bash and PostgreSQL to create a simple Salon appointment scheduler. It is required for the Relational Database certification from [freeCodeCamp](www.freecodecamp.org/).

## Two parts required for this project, a database ("salon.sql" file) and a script that will fill the database ("salon.sh" file)

**The tasks were:**
- Create a database named `salon`
- The database needs to have tables named `customers`, `appointments`, and `services`
- Each table should have a primary key column that automatically increments
- Each primary key column should follow the naming convention `table_name_id`
- The `appointments` table should have a `service_id` foreign key that references the `service_id` column from the `services` table
- The `customers` table should have `phone` that is a `VARCHAR` and must be unique
- The `customers` and `services` tables should have a `name` column
- The `appointments` table should have a `time` column that is a `VARCHAR`
- The `services` table must have at least three rows for the different services the salon offers
- Create a script file named `salon.sh` in the project folder
- The script must have a "shebang" that uses Bash when the file is executed
- The script must have executable permissions
- There must not be a `clear` command in the script
- Should be displayed a numbered list of services the salon offers before the first prompt for input, each with the format `#) <service`. For example `1) cut`, where `1` is the `service_id`
- If a service that does not exist is picked, the numbered list of services must be shown again
- The script should prompt users to enter a `service_id`, phone number, a name if they aren't already a customer, and a time. The script should `read` these inputs into variables named `SERVICE_ID_SELECTED`, `CUSTOMER_PHONE`, `CUSTOMER_NAME`, and `SERVICE_TIME`
- If a phone number entered doesn't exist, the script should get the customers name and enter it, and then the phone number too into the `customers` table
- A row in the `appointments` table should be created when entering `1`, `555-555-5555`, `Fabio`, `10:30` at each request for input if that phone number isn't in the `customers` table. The row should have the `customer_id` for that customer, and the `service_id` for the service entered
- A row in the `appointments` table should be created when entering `2`, `555-555-5555`, `11am` at each request for input that phone number is already in the `customers` table. The row should have the `customer_id` for that customer, and the `service_id` for the service entered
- After an appointment is successfully added, the output message should be `I have you down for a <service> at <time>, <name>.` For example, if the user chooses `cut` as the service, `10:30` is entered for the time, and their name is `Fabio` in the database, the output would be `I have put you down for a cut at 10:30, Fabio`
  
