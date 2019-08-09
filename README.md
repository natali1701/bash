# bash
script

#!/bin/bash

cd /home/nnaumenko

find /home/nnaumenko -type f -mtime +31 -exec rm {} \;

ls -t | tail -n+11 | xargs -i rm '{}'
