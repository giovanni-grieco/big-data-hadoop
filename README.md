# Big Data Hadoop (Università degli Studi Roma Tre)
## What's inside this repository?
Helper scripts to setup the environment and run hdfs (and in the future Spark) on your machine

## Requirements
- Docker engine and docker compose
- Java 8 or 11 (only version supported by hadoop) and JAVA_HOME setup properly
- wget (should be available by default on most distros)
- tar (should be available by default on most distros)

## How to use?
Download the repository
```bash
[git clone https://github.com/giovanni-grieco/big-data-hadoop.git](https://github.com/giovanni-grieco/big-data.git)
```

To setup the environment (installing hadoop and declaring environment variables) run:
```bash
source setup_environment.sh
```

To start hadoop services
```bash
./start.sh
```

To stop hadoop services
```
./stop.sh
```

## Setup Environment
Important thing to know is that the script will setup environment variables to use hadoop locally. 

The environment variables live only inside the current terminal session where the script was run.

If the terminal is closed and re-opened, you need to re-run ```source setup_environment.sh.```

You can edit your .bashrc (or equivalent) to have everything already setup from the start of your terminal.

Hadoop folder will be put in your $HOME folder (for example /home/yourusername/hadoop-3.4.1).

If you want to edit .bashrc you need to "export HADOOP_BASE="$HOME/hadoop-3.4.1" (assuming 3.4.1 is the version of the example) and then "export PATH="$HADOOP_BASE/bin:$PATH"

## Delete hadoop
Simply go to $HOME and remove the hadoop-$VERSION folder. You can also remove the hadoop-$VERSION.tar.gz
