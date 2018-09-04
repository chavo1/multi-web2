# Usage example:

This will install 2 web servers and MySQL database server

1.  Fork the copy of chavo1/multi-web1
2.  Clone it with following :

```

git clone git@github.com:chavo1/multi-web1.git

```
Then 
```
vagrant up
```
3. From you CLI, when the virtual machines are up.

4.  Open a web browser of your choice

Type 192.168.56.51 after it 192.168.56.52 on both you should see the web server with Welcome message

5. You can check if the packets are installed with a following commands:
```
﻿﻿vagrant ssh web01 -c "which nginx"
﻿﻿/usr/sbin/nginx
Connection to 127.0.0.1 closed.
﻿﻿vagrant ssh web02 -c "which nginx"
﻿﻿/usr/sbin/nginx
Connection to 127.0.0.1 closed.
﻿﻿vagrant ssh mysql -c "which mysql"
/usr/bin/mysql
Connection to 127.0.0.1 closed.
```


After this you can destroy the environments as follow:
```
vagrant destroy
```
