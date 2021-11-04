# Jupyter Notebooks

Notebooks for prototyping and testing data pipelines and other jobs. These notebooks are not actually executed by Airflow or otherwise as recurring jobs. 

## Setup

Just make sure to add the `dags/` and `plugins/` directories to `PYTHONPATH`. Put this somewhere in your `.bash_profile` or `.zshrc` or whatever:

```bash
export PYTHONPATH=$PATH:</path/to/repo>/dags:</path/to/repo>/plugins
```
