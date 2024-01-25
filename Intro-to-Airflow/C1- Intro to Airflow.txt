# Introduction to Airflow

## Data Engineering

Data engineering involves transforming any data-related action into a reliable, repeatable, and maintainable process.

### Workflow

A workflow is a set of steps to achieve a data engineering task, varying in complexity and meaning based on context.

### Airflow Platform

Airflow is a platform for programming workflows, providing capabilities for creation, scheduling, and monitoring. It allows the implementation of workflows in any language, but workflows are written in Python. Workflows are represented as Directed Acyclic Graphs (DAGs), which can be accessed via code, command-line, or web interface.

#### Other Tools

- [Luigi](https://luigi.readthedocs.io/en/stable/)
- [SSIS](https://docs.microsoft.com/en-us/sql/integration-services/sql-server-integration-services?view=sql-server-ver15)
- Bash scripting

## Directed Acyclic Graphs (DAGs)

### Definition

A DAG represents the set of tasks within an Airflow workflow, depicting dependencies between components.

### Airflow DAGs

Within Airflow, DAGs:

- Are written in Python (can use components from other languages).
- Comprise components (tasks, operators, sensors, etc.) to be executed.
- Explicitly or implicitly define dependencies, ensuring tasks are executed in the correct order.

#### Example DAG

```python
from airflow.models import DAG
from datetime import datetime

default_arguments = {
    'owner': 'jdoe',
    'email': 'jdoe@datacamp.com',
    'start_date': datetime(2020, 1, 20)
}

etl_dag = DAG('etl_workflow', default_args=default_arguments)
```

### Command Line Interface

The command-line program provides subcommands related to DAGs. Some functionalities include starting Airflow processes, manually running DAGs/tasks, and retrieving logging information.

### Web Interface

In most cases, the web interface is equally powerful or more accessible depending on needs.

---

*Let's practice! Introduction to Airflow in Python.*
