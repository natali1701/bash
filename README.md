# bash
script

#!/bin/bash

cd /home/nnaumenko/test

find /home/nnaumenko/test -type f -mtime +31 -exec rm {} \;

ls -t | tail -n+11 | xargs -i rm '{}'
