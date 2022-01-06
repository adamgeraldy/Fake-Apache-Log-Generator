
# Fake apache Log Generator

  

# Based On

[Fake-ELB-Log-Generator](https://github.com/kekayan/Fake-ELB-Log-Generator) library, and its Python3 update by [tuanpembual](https://github.com/tuanpembual/Fake-Apache-Log-Generator).

Logs are generated into a "logs/" folder, and generated the logs in JSON format.
  
This script generates a boatload of fake apache2 logs very quickly.
  

It can write log lines to console, to log files or directly to gzip files.

  

It utilizes the excellent [Faker](https://github.com/joke2k/faker/) library to generate realistic ip's, URI's etc.

  

***

  

## Basic Usage

  

Generate a single log line to STDOUT

```

$ python3 apache-fake-log-gen.py

```

  

Generate 100 log lines into a .log file

```

$ python3 -fake-log-gen.py -n 100 -o LOG

```

  

Generate 100 log lines into a .gz file at intervals of 10 seconds

```

$ python3 apache-fake-log-gen.py -n 100 -o GZ -s 10

```

  

Infinite log file generation (useful for testing File Tail Readers)

```

$ python3 apache-fake-log-gen.py -n 0 -o LOG

```

  

Prefix the output filename

```

$ python3 apache-fake-log-gen.py -n 100 -o LOG -p WEB1

```

  

Detailed help

```

$ python3 apache-fake-log-gen.py -h

usage: apache-fake-log-gen.py [-h] [--output {LOG,GZ,CONSOLE}]

[--num NUM_LINES] [--prefix FILE_PREFIX]

[--sleep SLEEP]

  

Fake apache Log Generator

  

optional arguments:

-h, --help show this help message and exit

--output {LOG,GZ,CONSOLE}, -o {LOG,GZ,CONSOLE}

Write to a Log file, a gzip file or to STDOUT

--num NUM_LINES, -n NUM_LINES

Number of lines to generate (0 for infinite)

--prefix FILE_PREFIX, -p FILE_PREFIX

Prefix the output file name

--sleep SLEEP, -s SLEEP

Sleep this long between lines (in seconds)

```

  
  

## Requirements

* Python 3

*  ```pip install -r requirements.txt```

  

## License

This script is released under the [Apache version 2](LICENSE) license.
