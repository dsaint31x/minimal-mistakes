---
title:  "[linux] conver sqlite into ER diagram"
last_modified_at:   2020-01-01
author: dsaint31
categories: 
  - linux
use_math: false
tags: 
  - linux 
---

# How to conver sqlite into ER diagram. 

## Install SchemaCrawler

* SchemaCrawler : v16.3.0
   * (schemacrawler-16.3.0-distibution.zip](https://github.com/schemacrawler/SchemaCrawler/releases/download/v16.3.0/schemacrawler-16.3.0-distribution.zip)
* Mint linux : 19.2 (Tina) / Ubuntu bionic

## Install Graphviz

* graphviz/bionic,now 2.40.1-2 amd64

```bash
sudo apt-get install graphviz
```

## run the shell

```bash
cd _schemacrawler/
./schemacrawler.sh schemacrawler.graph.graphviz.graph.splines=ortho --command schema --output-format png -loglevel=CONFIG --server sqlite --database /home/dsaint31/Projects/DentisAI/dstagram1/db.sqlite3 --info-level=maximum --output-file test.png schemacrawler.format.no_schema_colors=true
```

## References

(https://www.schemacrawler.com/diagramming.html)
(https://scribestools.readthedocs.io/en/latest/schemacrawler/#examples)
(https://silvae86.github.io/databases/sqlite/diagrams/macos/reverse/engineering/2019/04/14/how_to_reverse_engineer_database_diagrams/)
(https://stackoverflow.com/questions/19659846/trying-to-connect-to-sqlite-db-using-schemacrawler-using-osx-why-is-it-asking)
(https://www.schemacrawler.com/database-support.html)
