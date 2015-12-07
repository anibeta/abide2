# abide2
Script importing fMRI DTSS 3DT1ISOTROPE data from X to Y
apophis:~ anita$ cat -n /Users/anita/Desktop/ABIDE2/abide2_list_20151207.txt |while read name; do echo $name;done
apophis:~ anita$ mkdir ~/Desktop/abide-rdb
apophis:~ anita$ for seq in fMRI DTSS 3DT1ISOTROPE; do echo $seq;cat /Users/anita/Desktop/ABIDE2/abide2_list_20151207.txt |while read name; do echo $seq $name;mkdir -p ~/Desktop/abide-rdb/$name;cp /Volumes/cinq-4/rto/data/rdb/rdb2/_converted/$name/*${seq}* ~/Desktop/abide-rdb/$name/;done;done
