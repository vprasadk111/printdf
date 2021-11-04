pipeline{
agent any
stages{
stage("run df"){
steps{
   sh '''gatherdetails()
{
echo "------------- Gather Details -------------"
echo "Hostname           : `hostname -f`"
echo "Private IP Address :`ifconfig|grep inet|head -1|awk \'{print $2}\'`"
echo "kernel name           : `uname -r`"
echo "OS Release           : `cat /etc/redhat-release`"
echo " "
echo " "
echo "FS Tab           : `cat /etc/fstab`"
echo " "
echo " "
echo "Disk            : `df -h`"
echo "------------------------------------------"
};gatherdetails >> detailsout.txt'''
    
}
}
}
}
