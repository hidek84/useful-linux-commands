# useful-linux-commands

## du with percentage
```
du -m -d 1 | sort -nr | awk 'NR==1{print "total "$1"MB"; sum=$1} NR!=1{ per=$1/sum*100; if(per>=1){printf("%dMB\t%.1f\%%\t%s\n", $1, $1/sum*100, $2)}}'
```
  
% du -m -1 2 | sort -nr | awk 'NR==1{print "total "$1"MB"; sum=$1} NR!=1{ per=$1/sum*100; if(per>=1){printf("%dMB\t%.1f\%%\t%s\n", $1, $1/sum*100, $2)}}'
total 3019MB
1414MB	46.8%	./konektino
771MB	25.5%	./coreos-vagrant
548MB	18.2%	./chef_repo
86MB	2.8%	./Gyazz
