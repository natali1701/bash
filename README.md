#!/bin/bash
working_dir='/home/nnaumenko/OtusHW5'
cd $working_dir
find /home/nnaumenko/OtusHW5 -type f -mtime +31 -exec rm {} \;
for _dir in $(find -type d)
do
  cd $_dir
  ls -t -p | grep -v '/$' | tail -n+11 | xargs rm ;
  echo $_dir cleared
  cd $working_dir
done
