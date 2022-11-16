import requests
import re
import json
f = open('IPs.txt', 'a')
f.close()
f = open('IPs.txt', 'r')
ipstring = f.read()
f.close()
iplist = re.findall(r'(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})', ipstring)
if iplist:
    f = open('result.txt', 'w')
    for i in iplist:
        r = requests.get('http://ip-api.com/json/' + str(i))
        print(r.text)
        f.write(str(r.text.encode('UTF-8'))[2:-1] + '\n')
    f.close()
    print('done!')
else:
    print('There is no IP in IPs.txt')
