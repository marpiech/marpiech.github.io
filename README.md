## Contents
### Gists
[Add user](#adduser)  
[Set .htpasswd](#htpasswd)  


## Gists
<a name="adduser"/>
#### Add user
```
curl https://gist.githubusercontent.com/marpiech/1c601a1595324e10393a0fc56635ef5d/raw/9b291f62888266fbbf4ddb0c0710ad0c1097df18/adduser.sh | bash /dev/stdin [username] [github username]
```
<script src="https://gist.github.com/marpiech/1c601a1595324e10393a0fc56635ef5d.js"></script>

<a name="htpasswd"/>
#### Set .htpasswd
```
sudo htpasswd -c /etc/apache2/.htpasswd marpiech
```
