#!/usr/bin/env python
import socket
import subprocess
import sys
from datetime import datetime


subprocess.call('clear', shell=True)

print "+" * 140
print
print "                                                            PORT SCANNER BY afr0"
print "                                                              www.darksan.tk"
print "                                                           darksan.altervista.org"
print "                                                               PyrosSoftware"
print
print "+" * 140



remoteServer    = raw_input(" scan: ")
remoteServerIP  = socket.gethostbyname(remoteServer)


print "-" * 60
print "Please wait, scanning remote host", remoteServerIP
print "-" * 60


t1 = datetime.now()





try:
    for port in range(1,100000):  
        sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
        result = sock.connect_ex((remoteServerIP, port))
        if result == 0:
            print "Port {}: \t Open".format(port)
        sock.close()

except KeyboardInterrupt:
    print "You pressed Ctrl+C"
    sys.exit()

except socket.gaierror:
    print 'Hostname could not be resolved. Exiting'
    sys.exit()

except socket.error:
    print "Couldn't connect to server"
    sys.exit()


t2 = datetime.now()


total =  t2 - t1


print 'Scanning Completed in: ', total
