## Airflow Operators

### Operators

- Represent a single task in a workflow, typically run independently.
- Generally do not share information.
- Various operators available to perform different tasks.
```example_task = BashOperator(task_id='bash_example',
bash_command='echo "Example!"', dag=dag)
```
#### BashOperator

- Executes a given Bash command or script.
- Runs the command in a temporary directory.
- Can specify environment variables for the command.
- Not guaranteed to run in the same location/environment and may require extensive use of environment variables.
- Can be challenging to run tasks with elevated privileges.
```python
from airflow.operators.bash_operator import BashOperator

example_task = BashOperator(task_id='bash_ex', bash_command='echo 1', dag=dag)
bash_task = BashOperator(task_id='clean_addresses', bash_command='cat addresses.txt | awk "NF==10" > cleaned.txt', dag=dag)
```
## Tasks

- Instances of operators, usually assigned to a variable in Python.
- Referred to by the `task_id` within Airflow tools.
- Define a given order of task completion.
- Can be upstream or downstream tasks.
  - In Airflow 1.8 and later, defined using bitshift operators (`>>` for upstream, `<<` for downstream).
  
#### Example Tasks

```python
task1 = BashOperator(task_id='first_task', bash_command='echo 1', dag=example_dag)
task2 = BashOperator(task_id='second_task', bash_command='echo 2', dag=example_dag)

# Set first_task to run before second_task
task1 >> task2
```

#### Chained Dependencies

- `task1 >> task2` or `task3 >> task2`

## Additional Operators

#### PythonOperator

- Executes a Python function/callable.
- Similar to BashOperator but with more options.
- Supports passing arguments to the Python code.

```python
def sleep(length_of_time):
    time.sleep(length_of_time)

sleep_task = PythonOperator(
    task_id='sleep',
    python_callable=sleep,
    op_kwargs={'length_of_time': 5},
    dag=example_dag
)
```

#### EmailOperator

- Sends an email.
- Supports HTML content and attachments.
- Requires Airflow system to be configured with email server details.

```python
from airflow.operators.email_operator import EmailOperator

email_task = EmailOperator(
    task_id='email_sales_report',
    to='sales_manager@example.com',
    subject='Automated Sales Report',
    html_content='Attached is the latest sales report',
    files='latest_sales.xlsx',
    dag=example_dag
)
```

## Airflow Scheduling

- Represents a specific instance of a workflow at a point in time.
- Can be run manually or via a schedule.
- Maintains state for each workflow and its tasks.

### Scheduling Attributes

When scheduling a DAG, several attributes of note:

- Initial date/time to schedule the DAG run.
- Optional attributes for stopping new DAG instances and the number of attempts to make.
- Frequency of running the DAG.

#### Schedule Interval

- Represents how often to schedule the DAG.
- Defined using cron syntax or built-in presets.

#### Cron Format

- Consists of 5 fields separated by a space.
- Asterisk (*) represents running for every interval.
- Comma-separated values in fields for a list of values.

#### Presets

- Cron equivalents:
  - `@hourly: 0 * * * *`
  - `@daily: 0 0 * * *`
  - `@weekly: 0 0 * * 0`
  - `@monthly: 0 0 1 * *`
  - `@yearly: 0 0 1 1 *`

- Airflow special presets:
  - Don't schedule ever (for manually triggered DAGs).
  - Schedule only once.
**NOTE: When scheduling a DAG, Airflow will use the schedule and earliest possible value to determine when to run the task.
**
